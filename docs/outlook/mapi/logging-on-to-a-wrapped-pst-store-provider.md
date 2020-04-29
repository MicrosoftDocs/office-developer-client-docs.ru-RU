---
title: Вход в систему поставщика упакованного PST-хранилища
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Дата последнего изменения: 02 июля 2012 г.'
ms.openlocfilehash: 96f472d67f144a451046ff61a3ed6c6ff2ff9acf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408988"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Вход в систему поставщика упакованного PST-хранилища

**Относится к**: Outlook 2013 | Outlook 2016 
  
Прежде чем войти в систему MAPI в поставщик упакованного PST-хранилища, необходимо инициализировать и настроить поставщик хранилища файлов личных папок (PST) с оболочкой. Дополнительные сведения см. [в статье инициализация поставщика упакованного PST-хранилища](initializing-a-wrapped-pst-store-provider.md).
  
После инициализации и настройки поставщика упакованного PST-хранилища необходимо реализовать две процедуры входа. Функция **[функцииimsprovider:: logon](imsprovider-logon.md)** выполняет вход в систему MAPI для поставщика УПАКОВАНного PST-хранилища. Функция **[функцииimsprovider:: спулерлогон](imsprovider-spoolerlogon.md)** регистрируется в журнале очереди MAPI для поставщика УПАКОВАНного PST-хранилища. 
  
В этом разделе Функция **функцииimsprovider:: logon** и функция **Функцииimsprovider:: спулерлогон** демонстрируются с помощью примеров кода из примера поставщика упакованного PST-хранилища. В примере реализуется упакованный поставщик PST, предназначенный для использования вместе с API репликации. Дополнительные сведения о загрузке и установке примера поставщика упакованного PST-хранилища можно найти в статье [Установка примера поставщика упакованного PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md). Более подробную информацию об API репликации можно узнать [в статье о API репликации](about-the-replication-api.md).
  
После того как MAPI и Диспетчер очереди MAPI вошли в систему поставщика упакованного PST-хранилища, он готов к использованию. Дополнительные сведения см. в разделе [Использование поставщика упакованного PST-хранилища](using-a-wrapped-pst-store-provider.md).
  
## <a name="mapi-logon-routine"></a>Процедура входа в MAPI

После инициализации поставщика упакованного PST-хранилища необходимо реализовать функцию **[функцииimsprovider:: logon](imsprovider-logon.md)** для входа в MAPI в УПАКОВАНное PST-хранилище. Эта функция проверяет учетные данные пользователя и получает свойства конфигурации для поставщика. Кроме того, необходимо реализовать `SetOLFIInOST` функцию для установки сведений о автономном файле (**[олфи](olfi.md)** ). **Олфи** — это очередь долгосрочных структур идентификаторов, которая используется поставщиком упакованного PST-хранилища для назначения идентификатора записи для нового сообщения или папки в автономном режиме. Наконец, функция **функцииimsprovider:: logon** возвращает объект хранилища сообщений, с помощью которого диспетчер очереди MAPI и клиентские приложения могут войти в этот `ppMDB` параметр. 
  
### <a name="cmsproviderlogon-example"></a>Кмспровидер:: вход () пример

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

## <a name="mapi-spooler-logon-routine"></a>Процедура входа в очередь MAPI

Аналогично **функцииimsprovider:: logon**, необходимо реализовать функцию **[Функцииimsprovider:: спулерлогон](imsprovider-spoolerlogon.md)** , чтобы ЗАносить Диспетчер очереди MAPI в упакованное PST-хранилище. Объект хранилища сообщений, с помощью которого диспетчер очереди MAPI и клиентские приложения могут войти в систему, возвращается `ppMDB` в параметре. 
  
### <a name="cmsproviderspoolerlogon-example"></a>Кмспровидер:: Спулерлогон () пример

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

- [О примере поставщика упакованного PST-хранилища](about-the-sample-wrapped-pst-store-provider.md) 
- [Установка примера поставщика упакованного PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md) 
- [Инициализация поставщика упакованного PST-хранилища](initializing-a-wrapped-pst-store-provider.md)
- [Использование поставщика упакованного PST-хранилища](using-a-wrapped-pst-store-provider.md)
- [Завершение работы поставщика упакованного PST-хранилища](shutting-down-a-wrapped-pst-store-provider.md)

