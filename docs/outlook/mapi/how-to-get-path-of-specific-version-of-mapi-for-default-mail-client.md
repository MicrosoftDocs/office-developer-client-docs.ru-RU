---
title: Получение путь к определенной версии MAPI для почтового клиента по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ee7fb05-cfb3-6b68-5a9a-1d6375f2e879
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 277505beb11dbc2b32b7e970c2bcf2a34dbdf00b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808594"
---
# <a name="get-the-path-of-a-specific-version-of-mapi-for-the-default-mail-client"></a>Получение путь к определенной версии MAPI для почтового клиента по умолчанию

**Относится к**: Outlook 
  
В этом разделе приводится пример кода c++, который показано, как получить путь к определенной версии MAPI, используемый почтового клиента по умолчанию на компьютере. Почтовые клиенты MAPI имеют возможность указать в реестре настраиваемых DLL, что библиотека заглушка MAPI загружает и отправки MAPI вызывает для. Раздел реестра, чтобы задать для этой библиотеки DLL настраиваемого для почтового клиента по умолчанию — **MSIComponentID**в раздел **HKLM\Software\Clients\Mail** почтового клиента по умолчанию. Функция [FGetComponentPath](fgetcomponentpath.md) , экспортированные библиотекой заглушка MAPI mapistub.dll, можно вернуть путь для настраиваемой версии MAPI, указанное в ключе реестра **MSIComponentID** . 
  
В этом примере кода включает в себя две функции: `HrGetRegMultiSZValueA` и `GetMAPISVCPath`. `GetMAPISVCPath` Функции [FGetComponentPath](fgetcomponentpath.md) используется для получения пути к настраиваемой версии MAPI. Предполагается, что такое Microsoft Office Outlook 2007 почтового клиента по умолчанию и передает **FGetComponentPath** значение `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, который устанавливает Outlook 2007 в качестве компонента идентификатор MAPI для раздела реестра **MSIComponentID** . 
  
> [!NOTE]
> На практике не предполагается значение `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, всегда является компонентом идентификатор MAPI и напрямую передайте в него **FGetComponentPath**. Чтобы надежно выяснить, какая версия MAPI Outlook используется на компьютере, необходимо чтение из реестра значение **MSIComponentID** и передайте в него **FGetComponentPath**. 
  
Далее описано, как `GetMAPISVCPath` выполняет следующее. 
  
1. Загружает библиотеку заглушка MAPI, mapistub.dll, из каталога системы.
    
2. Предполагается, что mapistub.dll экспортирует функцию **FGetComponentPath** , она пытается получить адрес этой функции из mapistub.dll. 
    
3. Если адрес из mapistub.dll возникает ошибка, пытается получить адрес из mapi32.dll.
    
4. Если получение адреса **FGetComponentPath** успешно, он открывается реестра и использует `HrGetRegMultiSZValueA` функция для считывания значений реестра в разделе **HKLM\Software\Clients\Mail\Microsoft Outlook**. 
    
5. Вызывает **FGetComponentPath**, указав значение `{FF1D0740-D227-11D1-A4B0-006008AF820E}`, чтобы получить путь к версии MAPI, используемый Outlook 2007.
    
Обратите внимание, что для поддержки локализованных копий MAPI для английского языка и языков, кроме английского, пример кода считывает значения для подразделов **MSIApplicationLCID** и **MSIOfficeLCID** вызывает **FGetComponentPath**, сначала указание ** MSIApplicationLCID** *szQualifier* , а затем снова указание **MSIOfficeLCID** как *szQualifier* . Дополнительные сведения о разделах реестра для почтовых клиентов, которые поддерживают языками см [параметр копирование MSI для Your MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).
  
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


