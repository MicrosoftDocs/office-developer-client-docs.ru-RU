---
title: Вход в систему поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408988"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Вход в систему поставщика упакованного PST-хранилища

**Относится к**: Outlook 2013 | Outlook 2016 
  
Прежде чем войти в MAPI у поставщика упакованного PST-магазина, необходимо инициализировать и настроить поставщика упакованного файла личных папок (PST). Дополнительные сведения см. в [инициализации поставщика упакованного PST-магазина.](initializing-a-wrapped-pst-store-provider.md)
  
После инициализации и настройки поставщика упакованного PST-магазина необходимо реализовать две процедуры. Функция **[IMSProvider::Logon](imsprovider-logon.md)** занося в mapI в журнал поставщика упакованного PST-магазина. Функция **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** занося в пул MAPI поставщика упакованного PST-магазина. 
  
В этом разделе функции **IMSProvider::Logon** и **IMSProvider::SpoolerLogon** демонстрируются с помощью примеров кода из примера поставщика упакованного PST-магазина. В примере реализован упакованный поставщик PST,который предназначен для использования в сочетании с API репликации. Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-магазина см. в примере установки поставщика упакованного [PST-магазина.](installing-the-sample-wrapped-pst-store-provider.md) Дополнительные сведения об API репликации см. в сведениях об [API репликации.](about-the-replication-api.md)
  
После входа MAPI и пула MAPI к поставщику упакованного PST-магазина его можно использовать. Дополнительные сведения см. в сведениях об использовании поставщика упакованного [PST-магазина.](using-a-wrapped-pst-store-provider.md)
  
## <a name="mapi-logon-routine"></a>MapI Logon routine

После инициализации поставщика упакованного PST-магазина необходимо реализовать функцию **[IMSProvider::Logon](imsprovider-logon.md)** для входа в MAPI в упакованное хранилище PST. Эта функция проверяет учетные данные пользователя и получает свойства конфигурации для поставщика. Необходимо также реализовать функцию, чтобы установить сведения об автономном `SetOLFIInOST` файле **[(OLFI).](olfi.md)** **OLFI** — это очередь структур долгосрочных ИД, которая используется поставщиком упакованного PST-магазина для назначения ИД записи для нового сообщения или папки в автономном режиме. Наконец, функция **IMSProvider::Logon** возвращает объект хранения сообщений, в который могут войти пул mapi и клиентские приложения в  `ppMDB` параметре. 
  
### <a name="cmsproviderlogon-example"></a>Пример CMSProvider::Logon()

```cpp
STDMETHODIMP CMSProvider::Logon( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG * pcbSpoolSecurity, 
    LPBYTE * ppbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMDB lpPSTMDB = NULL; 
    CMsgStore* pWrappedMDB = NULL; 
 
    Log(true,"CMSProvider::Logon Pst logon Called\n"); 
 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        ulFlags = (ulFlags & ~MDB_OST_LOGON_ANSI) | MDB_OST_LOGON_UNICODE; 
        hRes = m_pPSTMS->Logon( 
            pMySup, 
            ulUIParam,  
            pszProfileName,  
            cbEntryID, 
            pEntryID,  
            ulFlags,  
            pInterface,  
            pcbSpoolSecurity, 
            ppbSpoolSecurity,  
            ppMAPIError,  
            ppMSLogon,  
            &lpPSTMDB); 
    } 
    Log(true,"CMSProvider::Logon returned 0x%08X\n", hRes); 
 
    // Set up the MDB to allow synchronization 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = SetOLFIInOST(lpPSTMDB); 
        Log(true,"SetOLFIInOST returned 0x%08X\n", hRes); 
    } 
    // Wrap the outgoing MDB 
    pWrappedMDB = new CMsgStore (lpPSTMDB); 
    if (NULL == pWrappedMDB) 
    { 
        Log(true,"CMSProvider::Logon: Failed to allocate new CMsgStore object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    // Copy pointer to the allocated object back into the return LPMDB object pointer 
    *ppMDB = pWrappedMDB; 
    if (lpProfSect) lpProfSect->Release(); 
 
    return hRes; 
}
```

## <a name="mapi-spooler-logon-routine"></a>MapI Spooler Logon routine

Как и **в IMSProvider::Logon,** необходимо реализовать функцию **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** для входа в пульер MAPI в упакованное хранилище PST. В параметре возвращается объект хранения сообщений, в который может войти пул MAPI и клиентские  `ppMDB` приложения. 
  
### <a name="cmsproviderspoolerlogon-example"></a>Пример CMSProvider::SpoolerLogon()

```cpp
STDMETHODIMP CMSProvider::SpoolerLogon ( 
    LPMAPISUP pSupObj, 
    ULONG ulUIParam, 
    LPTSTR pszProfileName, 
    ULONG cbEntryID, 
    LPENTRYID pEntryID, 
    ULONG ulFlags, 
    LPCIID pInterface, 
    ULONG cbSpoolSecurity, 
    LPBYTE pbSpoolSecurity, 
    LPMAPIERROR * ppMAPIError, 
    LPMSLOGON * ppMSLogon, 
    LPMDB * ppMDB) 
{ 
    HRESULT hRes = S_OK; 
     
    Log(true,"CMSProvider::SpoolerLogon\n"); 
    LPPROFSECT lpProfSect = NULL; 
    CSupport * pMySup = NULL; 
    hRes = GetGlobalProfileObject(pSupObj,&lpProfSect); 
    pMySup = new CSupport(pSupObj, lpProfSect); 
    if (!pMySup) 
    { 
        Log(true,"CMSProvider::SpoolerLogon: " + 
            "Failed to allocate new CSupport object\n"); 
        hRes = E_OUTOFMEMORY; 
    } 
    if (SUCCEEDED(hRes)) 
    { 
        hRes = m_pPSTMS->SpoolerLogon(  
            pMySup,//pSupObj, 
            ulUIParam, 
            pszProfileName, 
            cbEntryID, 
            pEntryID, 
            ulFlags, 
            pInterface, 
            cbSpoolSecurity, 
            pbSpoolSecurity, 
            ppMAPIError, 
            ppMSLogon, 
            ppMDB); 
    } 
    Log(true,"CMSProvider::SpoolerLogon returned 0x%08X\n", hRes); 
 
    return hRes; 
}
```

## <a name="see-also"></a>См. также

- [Пример поставщика упакованного PST-магазина](about-the-sample-wrapped-pst-store-provider.md) 
- [Установка примера поставщика упакованного PST-магазина](installing-the-sample-wrapped-pst-store-provider.md) 
- [Инициализация поставщика упакованного PST-магазина](initializing-a-wrapped-pst-store-provider.md)
- [Использование поставщика упакованного PST-магазина](using-a-wrapped-pst-store-provider.md)
- [Завершение работы поставщика упакованного PST-магазина](shutting-down-a-wrapped-pst-store-provider.md)

