---
title: Вход в систему на оболочку поставщик хранилища PST-файлов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 364bc5fd-2199-0bb2-142b-9b3b686b2268
description: 'Последнее изменение: 2 июля 2012.'
ms.openlocfilehash: 0716017788239c22f31007438089118d109010a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570480"
---
# <a name="logging-on-to-a-wrapped-pst-store-provider"></a>Вход в систему на оболочку поставщик хранилища PST-файлов

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Чтобы выполнить вход на MAPI оболочку поставщика хранилища PST-файлов, необходимо инициализировать и настроить оболочку поставщика хранилища личных папок (PST) файла. Для получения дополнительных сведений см. [В оболочку поставщика хранилища PST -файлов](initializing-a-wrapped-pst-store-provider.md).
  
После инициализации и настройки оболочку поставщика хранилища PST-файлов необходимо реализовать две процедуры входа в систему. Функция **[IMSProvider::Logon](imsprovider-logon.md)** входит MAPI оболочку поставщика хранилища PST-файлов. Функция **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** входит в систему диспетчер очереди MAPI на оболочку поставщик хранилища PST-файлов. 
  
В этом разделе функции **IMSProvider::Logon** и **IMSProvider::SpoolerLogon** демонстрируются с помощью примеров кода с переносом PST поставщик хранилища. В примере реализуется оболочку поставщика PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации. Дополнительные сведения о загрузке и установке оболочку PST поставщик хранилища [Оболочку PST поставщик хранилища](installing-the-sample-wrapped-pst-store-provider.md)см. Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).
  
После входа MAPI и диспетчер очереди MAPI на оболочку PST хранилища поставщика, его можно будет использовать. [Оболочку поставщика хранилища PST -файлов](using-a-wrapped-pst-store-provider.md)для получения дополнительных сведений см.
  
## <a name="mapi-logon-routine"></a>Процедура входа в систему MAPI

После инициализации оболочку поставщика хранилища PST-файлов, необходимо реализовать функцию **[IMSProvider::Logon](imsprovider-logon.md)** для входа на MAPI оболочку PST-хранилище. Эта функция проверяет учетные данные пользователя и получает свойства конфигурации для поставщика. Кроме того, необходимо реализовать `SetOLFIInOST` функцию, чтобы задать автономный режим сведения о файле (**[OLFI](olfi.md)** ). **OLFI** — это очереди долгосрочного структур идентификатор, используемый поставщиком хранилища оболочку PST-файлов для назначения идентификатор записи для нового сообщения или папки в автономном режиме. И, наконец, функция **IMSProvider::Logon** возвращает объект хранилища сообщений, очереди и клиентских приложений MAPI может входить в `ppMDB` параметр. 
  
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

## <a name="mapi-spooler-logon-routine"></a>Процедура входа в систему очереди MAPI

Как и **IMSProvider::Logon**, необходимо реализовать функцию **[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)** для записи в журнал очереди MAPI на оболочку PST-хранилище. Объект хранилища сообщений, очереди и клиентских приложений MAPI могут войти на возвращается в `ppMDB` параметр. 
  
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

- [Сведения о примере поставщика упакованного PST-хранилища](about-the-sample-wrapped-pst-store-provider.md) 
- [Установка примера поставщика упакованного PST-хранилища](installing-the-sample-wrapped-pst-store-provider.md) 
- [Инициализация поставщика упакованного PST-хранилища](initializing-a-wrapped-pst-store-provider.md)
- [Использование поставщика упакованного PST-хранилища](using-a-wrapped-pst-store-provider.md)
- [Завершение работы поставщика упакованного PST-хранилища](shutting-down-a-wrapped-pst-store-provider.md)

