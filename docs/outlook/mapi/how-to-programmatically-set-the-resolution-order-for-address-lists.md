---
title: Приоритет разрешения для списков адресов для задания программным путем
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f9559afb-8db1-ce72-3e11-9b3d47bb80b6
description: 'Последнее изменение: 06 июля 2012 г.'
ms.openlocfilehash: 676d74c6441716203006f2db3e4a7d5777320a98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808623"
---
# <a name="programmatically-set-the-resolution-order-for-address-lists"></a>Приоритет разрешения для списков адресов для задания программным путем
  
**Применимо к**: Outlook 
  
В этом разделе содержится пример кода на C++, который программно задает порядок списков адресов в список получателей электронной почты разрешаются сообщений и участниками в рабочей области приглашений на собрания.
  
В MAPI каждый профиль может поддерживать несколько списков адресов, а каждый список адресов в свой собственный контейнер. Метод **[SetSearchPath](http://support.microsoft.com/kb/292590)** поддерживает MAPI в интерфейс, который позволяет задать новый путь для поиска профиля, который используется для разрешения имен. Чтобы использовать метод **IAddrBook::SetSearchPath** , необходимо определить порядок необходимое разрешение в массиве **[SRowSet](srowset.md)** , в котором размещается контейнеров соответствующих адресными книгами в установленном порядке, а затем укажите массив как *lpSearchPath*  параметр. Первое свойство для каждой записи в массиве **SRowSet** значения свойства **[PR_ENTRYID](pidtagentryid-canonical-property.md)** соответствующий адресной книги. 
  
Пример кода задает порядок обработки выполняются следующие шаги:
  
1. Инициализирует `numANR` число контейнеров в соответствии с и указывает имена и порядок обработки списков нужный адрес `ANROrder` массива. 
    
2. Инициализирует MAPI с помощью функции **MAPIInitialize** . 
    
3.  Вход в MAPI и пользователь может выбрать профиль. 
    
4.  Получает указатель на адресной книги из текущего сеанса. 
    
5. Открыть адресную книгу.
    
6. Открывает контейнер для корневого адресной книги.
    
7. Открывает таблицу иерархии контейнер корневого адресной книги.
    
8. Получает список адресов книги контейнеров в иерархии.
    
9. Выполняет поиск идентификаторы нужный адрес списков путем сравнения имена желаемую адресными книгами в `ANROrder` для существующих имен в иерархии адресной книги. 
    
10. Задает средством идентификаторы в массив **SRowSet** `pNewRows`.
    
11. Вызывает и передает `pNewRows` как параметр *lpSearchPath* для **IAddrBook::SetSearchPath** , чтобы задать путь для поиска. 
    
12. Очищает внутренние буферы и указатели.
    
13. Журналы отключение MAPI.
    
14. Uninitalizes MAPI.
    
В этом примере кода используется списки адресов, доступные в по умолчанию при установке Microsoft Office Outlook: **Все контакты**, **Всех групп**и **контактов**. После того как Outlook запущено и работает на инициализированный профилей необходимо запустить примера. Пример хорошо работает с именами, которые находятся в одном языке (например, все имена, на английском языке). Он не предназначен для работы в многоязычной развертываниях например папку **Контакты** , локализован для пользователя, выполняющего построения не английской Outlook. 
  
```cpp
#include "stdafx.h" 
#include <mapix.h> 
#include <mapiguid.h> 
#include <mapiutil.h> 
#include <mapidefs.h> 
#include <stdio.h> 
#include <conio.h> 
 
//Number of address lists to resolve against 
const int numANR = 3; 
WCHAR *ANROrder[numANR] = {_T("All Contacts"), _T("All Groups"), _T("Contacts")}; 
UINT  numContainersFound [numANR] = {0}; 
 
// Temporary structure to allocate buffer in MAPI. This will be used as a parent buffer to free space later. 
LPVOID tempLink; 
 
// Forward declaration of helper function to copy binary data 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent); 
 
void main() 
{ 
    // MAPI address book and session variables 
    HRESULT       hRes = S_OK;            // Result code returned from MAPI calls. 
    LPMAPISESSION lpSession = NULL;   // Pointer to MAPI session. 
    LPADRBOOK     lpAddrBook = NULL;  // Pointer to Address Book. 
 
    // Counters 
    ULONG         i = 0;                  // Index counter 
    ULONG         j = 0;                  // Index counter 
 
    // Used for querying hierarchy 
    ULONG                                   ulObjType = 0L;      // Object type returned by MAPI 
    LPMAPICONTAINER     pIABRoot = NULL;     // Root address book container 
    LPMAPITABLE              pHTable = NULL;      // Holds hierarchy table 
    LPSRowSet        pRows = NULL;        // Pointer to row set. Stores AB Address Lists 
 
    // Used for setting search path 
    LPSRowSet     pNewRows = NULL;        // Pointer to new row set 
    SizedSRowSet  (numANR, NewRows);      // New row set 
    SPropValue    sProps[numANR] = {0};   // Property tag structure 
 
    // Structures contaning MAPI Column Sets required for querying tables 
    enum { 
        abPR_ENTRYID, 
        abPR_DISPLAY_NAME_W, 
        abNUM_COLS}; 
 
    static SizedSPropTagArray(abNUM_COLS,abCols) = { 
        abNUM_COLS, 
        PR_ENTRYID, 
        PR_DISPLAY_NAME_W, 
    }; 
 
    // Initialize MAPI 
    if (FAILED ( hRes = MAPIInitialize(NULL))) goto Exit; 
 
    // Log on to MAPI and allow user to choose profile 
 
    // Note: This uses the current MAPI session if there is one 
    if (FAILED ( hRes = MAPILogonEx(NULL, NULL, NULL, MAPI_LOGON_UI, &lpSession))) goto Exit; 
 
    // Open the Address Book 
    if (FAILED (hRes = lpSession->OpenAddressBook(NULL, NULL, NULL, &lpAddrBook))) goto Cleanup; 
 
    // Open the Address Book Root container 
    if (FAILED (hRes = lpAddrBook -> OpenEntry ( 
        0L,  
        NULL, 
        NULL,  
        0L, 
        &ulObjType, 
        (LPUNKNOWN *) &pIABRoot ))) 
    goto Cleanup; 
 
    // Intentionally allocate 0 bytes. This is used for buffer management. 
    MAPIAllocateBuffer(0L, &tempLink);  
 
    // Make sure there is a Container object 
    // Query hierarchy for containers 
    if ( MAPI_ABCONT == ulObjType ) { 
        // - Call IMAPIContainer::GetHierarchyTable to open the Hierarchy 
        //   table of the root address book container 
        if ( FAILED ( hRes = pIABRoot -> GetHierarchyTable ( CONVENIENT_DEPTH | MAPI_UNICODE, 
            &pHTable ) ) ) 
        goto Cleanup; 
 
        // Get the list of address book containers first 
        if ( FAILED ( hRes = HrQueryAllRows (  
            pHTable, 
            (LPSPropTagArray) &abCols, 
            NULL, 
            NULL, 
            0L, 
            &pRows ) ) ) 
        goto Cleanup; 
 
        // Initialize the structures to set the search order 
        ZeroMemory(&NewRows, numANR * sizeof(SRow)); 
        pNewRows = (LPSRowSet)&NewRows; 
 
        // Set the number of rows you are going to set 
        pNewRows->cRows = numANR; 
 
        // Set the pointers to the structures 
        for (i=0; i<numANR; i++) 
            pNewRows->aRow[i].lpProps = &sProps[i]; 
 
        // Compare the list to the ones that of interest 
        for (i=0; i<pRows->cRows; i++) { 
            if (pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].ulPropTag == PR_DISPLAY_NAME_W) { 
                LPWSTR containerName =  pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].Value.lpszW; 
                for (j=0; j<numANR; j++) 
                    if (!wcscmp (containerName, ANROrder[j])) { 
                        // First check if a container with this name has been found already 
                        if (numContainersFound[j] == 0) { 
                            numContainersFound[j]++; 
                            pNewRows->aRow[j].cValues = 1; 
 
                            // The property being passing is PR_ENTRY_ID 
                            pNewRows->aRow[j].lpProps[0].ulPropTag = PR_ENTRYID; 
 
                            // Copy the binary data over 
                            if (FAILED (hRes = CopySBinary( 
                                &pNewRows->aRow[j].lpProps[0].Value.bin, 
                                &pRows->aRow[i].lpProps[abPR_ENTRYID].Value.bin, 
                                tempLink))) {  
                                    printf ("Fatal Error:Failed to copy entry IDs\n"); 
                                    goto Cleanup; 
                            } 
                         } 
                         // More than 1 container matched the same name 
                         else {  
                             printf ("Fatal Error: Duplicate container found, container name = %s\n", containerName); 
                             goto Cleanup; 
                         } 
                    } 
            } 
        } 
 
        // Only set the search path if all the rows have been found 
        // Check the array for any entries that were blank 
        for (i=0; i< numANR; i++) 
            if (numContainersFound [i] == 0) { 
                printf ("Fatal Error: all containers were not found\n"); 
                goto Cleanup; 
            } 
 
        // Everything is safe to set the search path now 
        if (FAILED (hRes = lpAddrBook->SetSearchPath(0, pNewRows))) {                    
            printf ("Fatal Error: failed to set the search path\n"); 
            goto Cleanup; 
        } 
    } 
 
    Cleanup: 
        MAPIFreeBuffer(tempLink); 
        UlRelease(pHTable); 
        FreeProws(pRows); 
        UlRelease (pIABRoot); 
        UlRelease(lpAddrBook); 
 
        // Log off from MAPI 
        hRes = lpSession->Logoff(NULL, NULL, 0); 
        UlRelease(lpSession); 
 
    Exit: 
        // Uninitialize MAPI 
        MAPIUninitialize(); 
} 
 
///////////////////////////////////////////////////////////// 
//    CopySBinary() 
// 
//    Parameters 
// 
//    Purpose 
//      Allocates a new SBinary and copies psbSrc into it 
// 
 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent) 
{ 
    HRESULT     hRes = S_OK; 
    psbDest->cb = psbSrc->cb; 
 
    if (psbSrc->cb) { 
        if (pParent) 
            hRes = MAPIAllocateMore( 
                 psbSrc->cb, 
                 pParent, 
                 (LPVOID*) &psbDest->lpb); 
        else 
            hRes = MAPIAllocateBuffer( 
                 psbSrc->cb, 
                 (LPVOID*) &psbDest->lpb); 
 
    if (!FAILED(hRes)) 
        CopyMemory(psbDest->lpb,psbSrc->lpb,psbSrc->cb); 
    } 
 
   return hRes; 
} 

```

## <a name="see-also"></a>См. также

- [О настройке приоритет разрешения для списков адресов в Outlook](about-setting-the-resolution-order-for-address-lists-in-outlook.md)

