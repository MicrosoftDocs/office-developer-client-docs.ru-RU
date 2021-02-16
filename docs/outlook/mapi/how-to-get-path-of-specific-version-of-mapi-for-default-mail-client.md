---
title: Получение пути к определенной версии MAPI для почтового клиента по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ee7fb05-cfb3-6b68-5a9a-1d6375f2e879
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1992e34a684a6b5894963eae0c299b21c064578c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346461"
---
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a>Получение пути к определенной версии MAPI для почтового клиента по умолчанию

**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе содержится пример кода на C++, в который показано, как получить путь к определенной версии MAPI, используемой почтовым клиентом по умолчанию на компьютере. Почтовые клиенты MAPI могут указать в реестре настраиваемую библиотеку DLL, на которую должна загружаться библиотека загружных файлов MAPI, и отправлять вызовы MAPI. Для этого настраиваемого DLL-файлов для почтового клиента по умолчанию задаваемый в реестре ключ **реестра MSIComponentID** находится в списке **HKLM\Software\Clients\Mail** почтового клиента по умолчанию. Функция [FGetComponentPath,](fgetcomponentpath.md) экспортируемая библиотекой загвоздки MAPI mapistub.dll, может возвращать путь к настраиваемой версии MAPI, указанной в ключе реестра **MSIComponentID.** 
  
Этот пример кода включает две функции:  `HrGetRegMultiSZValueA` и  `GetMAPISVCPath` . Функция  `GetMAPISVCPath` использует [FGetComponentPath для](fgetcomponentpath.md) получения пути к настраиваемой версии MAPI. Предполагается, что почтовый клиент по умолчанию Microsoft Office Outlook 2007, и передает **FGetComponentPath** значение, которое Outlook 2007 устанавливает в качестве ИД компонента MAPI для `{FF1D0740-D227-11D1-A4B0-006008AF820E}` **ключа реестра MSIComponentID.** 
  
> [!NOTE]
> На практике не следует предполагать значение, всегда является ИД компонента MAPI и передавать его  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` **непосредственно в FGetComponentPath**. Чтобы надежно узнать, какую версию MAPI Outlook использует на компьютере, необходимо прочитать из реестра значение **MSIComponentID** и передать его **в FGetComponentPath.** 
  
Ниже описано,  `GetMAPISVCPath` как это сделать. 
  
1. Загружает библиотеку загона MAPI mapistub.dll из системного каталога.
    
2. Предполагается, mapistub.dll экспортирует функцию **FGetComponentPath,** она пытается получить адрес этой функции из mapistub.dll. 
    
3. Если получить адрес из mapistub.dll не удается, он пытается получить адрес из mapi32.dll.
    
4. Если получение адреса **FGetComponentPath** успешно, открывается реестр и используется функция для чтения значений реестра `HrGetRegMultiSZValueA` в **HKLM\Software\Clients\Mail\Microsoft Outlook.** 
    
5. Вызывает **FGetComponentPath,** указав значение, чтобы получить путь к версии  `{FF1D0740-D227-11D1-A4B0-006008AF820E}` MAPI, которую использует Outlook 2007.
    
Обратите внимание, что для поддержки локализованных копий MAPI для английского и других региональных звонков в примере кода считыются значения для подкайтов **MSIApplicationLCID** и **MSIOfficeLCID** и **вызывается FGetComponentPath,** сначала задав **MSIApplicationLCID** как  *szQualifier,*  а затем снова указав **MSIOfficeLCID** как  *szQualifier*  . Дополнительные сведения о ключах реестра для почтовых клиентов, которые поддерживают не английский язык, см. в настройке [ключей MSI для вашей DLL MAPI.](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
  
```cpp
// HrGetRegMultiSZValueA 
// Get a REG_MULTI_SZ registry value - allocating memory using new to hold it. 
void HrGetRegMultiSZValueA( 
    IN HKEY hKey, // the key. 
    IN LPCSTR lpszValue, // value name in key. 
    OUT LPVOID* lppData) // where to put the data. 
{ 
    *lppData = NULL; 
    DWORD dwKeyType = NULL;       
    DWORD cb = NULL; 
    LONG lRet = 0; 
    
    // Get its size 
    lRet = RegQueryValueExA( 
        hKey, 
        lpszValue, 
        NULL, 
        &amp;dwKeyType, 
        NULL, 
        &amp;cb); 
 
    if (ERROR_SUCCESS == lRet &amp;&amp; cb &amp;&amp; REG_MULTI_SZ == dwKeyType) 
    { 
        *lppData = new BYTE[cb]; 
       
        if (*lppData) 
        { 
            // Get the current value 
            lRet = RegQueryValueExA( 
                hKey,  
                lpszValue,  
                NULL,  
                &amp;dwKeyType,  
                (unsigned char*)*lppData,  
                &amp;cb); 
          
            if (ERROR_SUCCESS != lRet) 
            { 
                delete[] *lppData; 
                *lppData = NULL; 
            } 
        } 
    } 
} 
 
typedef BOOL (STDAPICALLTYPE FGETCOMPONENTPATH) ( 
    LPSTR szComponent, 
    LPSTR szQualifier, 
    LPSTR szDllPath, 
    DWORD cchBufferSize, 
    BOOL fInstall); 
typedef FGETCOMPONENTPATH FAR * LPFGETCOMPONENTPATH;  
 
/////////////////////////////////////////////////////////////////////////////// 
// Function name   : GetMAPISVCPath 
// Description       : This will get the correct path to the MAPISVC.INF file. 
// Return type      : void  
// Argument         : LPSTR szMAPIDir - Buffer to hold the path to the MAPISVC file. 
//                    ULONG cchMAPIDir - size of the buffer 
void GetMAPISVCPath(LPSTR szMAPIDir, ULONG cchMAPIDir) 
{ 
    HRESULT hRes = S_OK; 
    UINT uiRet = 0; 
    LONG lRet = 0; 
    BOOL bRet = true; 
    
    szMAPIDir[0] = &apos;\0&apos;; // Terminate string at position 0, safer if fail below 
    
    CHAR szSystemDir[MAX_PATH+1] = {0}; 
    
    // Get the system directory path 
    // (mapistub.dll and mapi32.dll reside here) 
    uiRet = GetSystemDirectoryA(szSystemDir, MAX_PATH); 
    if (uiRet &gt; 0) 
    { 
        CHAR szDLLPath[MAX_PATH+1] = {0}; 
       
        hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, &quot;%s\\%s&quot;,  
            szSystemDir, &quot;mapistub.dll&quot;); 
        if (SUCCEEDED(hRes)) 
        { 
            LPFGETCOMPONENTPATH pfnFGetComponentPath = NULL; 
          
            HMODULE hmodStub = 0; 
            HMODULE hmodMapi32 = 0; 
          
            // Load mapistub.dll 
            hmodStub = LoadLibraryA(szDLLPath); 
            if (hmodStub) 
            {    
                // Get the address of FGetComponentPath from the mapistub 
                pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                    hmodStub, &quot;FGetComponentPath&quot;); 
            } 
          
            // If failed to get the address of FGetComponentPath, 
            // try mapi32.dll 
            if (!pfnFGetComponentPath) 
            { 
                hRes = StringCchPrintfA(szDLLPath, MAX_PATH+1, &quot;%s\\%s&quot;, 
                    szSystemDir, &quot;mapi32.dll&quot;); 
                if (SUCCEEDED(hRes)) 
                { 
                    // Load mapi32.dll 
                    hmodMapi32 = LoadLibraryA(szDLLPath); 
                    if (hmodMapi32) 
                    { 
                        // Get the address of FGetComponentPath from mapi32 
                        pfnFGetComponentPath = (LPFGETCOMPONENTPATH)GetProcAddress( 
                            hmodMapi32, &quot;FGetComponentPath&quot;); 
                    } 
                 } 
            } 
            if (pfnFGetComponentPath) 
            { 
                LPSTR szAppLCID = NULL; 
                LPSTR szOfficeLCID = NULL; 
                HKEY hMicrosoftOutlook = NULL; 
             
                lRet = RegOpenKeyEx( 
                    HKEY_LOCAL_MACHINE, 
                    _T(&quot;Software\\Clients\\Mail\\Microsoft Outlook&quot;), 
                    NULL, 
                    KEY_READ, 
                    &amp;hMicrosoftOutlook); 
             
                if (ERROR_SUCCESS == lRet &amp;&amp; hMicrosoftOutlook) 
                { 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, &quot;MSIApplicationLCID&quot;, (LPVOID*) &amp;szAppLCID); 
                    HrGetRegMultiSZValueA(hMicrosoftOutlook, &quot;MSIOfficeLCID&quot;, (LPVOID*) &amp;szOfficeLCID); 
                } 
             
                // Only passing a fixed value as the component ID for MAPI in this example 
                // In practice, must read from the registry the value of MSIComponentID 
                if (szAppLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                        &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, szAppLCID, szMAPIDir, cchMAPIDir, true); 
                } 
                if ((!bRet || szMAPIDir[0] == _T(&apos;\0&apos;)) &amp;&amp; szOfficeLCID) 
                { 
                    bRet = pfnFGetComponentPath( 
                    &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, szOfficeLCID, szMAPIDir, cchMAPIDir, true); 
                } 
                if (!bRet || szMAPIDir[0] == _T(&apos;\0&apos;)) 
                { 
                    bRet = pfnFGetComponentPath( 
                        &quot;{FF1D0740-D227-11D1-A4B0-006008AF820E}&quot;, NULL, szMAPIDir, cchMAPIDir, true); 
                } 
             
                // Got the path to msmapi32.dll - need to strip it 
                if (bRet &amp;&amp; szMAPIDir[0] != _T(&apos;\0&apos;)) 
                { 
                    LPSTR lpszSlash = NULL; 
                    LPSTR lpszCur = szMAPIDir; 
                
                    for (lpszSlash = lpszCur; *lpszCur; lpszCur = lpszCur++) 
                    { 
                        if (*lpszCur == _T(&apos;\\&apos;)) lpszSlash = lpszCur; 
                    } 
                   *lpszSlash = _T(&apos;\0&apos;); 
                } 
 
                delete[] szOfficeLCID; 
                delete[] szAppLCID; 
                if (hMicrosoftOutlook) RegCloseKey(hMicrosoftOutlook);       
            } 
             
            // If FGetComponentPath returns FALSE or if 
            // it returned nothing, or if failed to find an 
            // address of FGetComponentPath, then 
            // just default to the system directory 
            if (!bRet || szMAPIDir[0] == &apos;\0&apos;) 
            { 
                hRes = StringCchPrintfA( 
                    szMAPIDir, cchMAPIDir,&quot;%s&quot;, szSystemDir); 
            } 
          
            if (szMAPIDir[0] != _T(&apos;\0&apos;)) 
            { 
                hRes = StringCchPrintfA( 
                    szMAPIDir, cchMAPIDir, &quot;%s\\%s&quot;, szMAPIDir, &quot;MAPISVC.INF&quot;); 
            } 
          
            if (hmodMapi32) FreeLibrary(hmodMapi32); 
            if (hmodStub) FreeLibrary(hmodStub); 
        } 
    }    
}

```


