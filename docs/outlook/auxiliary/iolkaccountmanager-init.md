---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Инициализирует диспетчер учетной записи для использования.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322038"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Инициализирует диспетчер учетной записи для использования.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parameters

_pAcctHelper_
  
> [in] Интерфейс [IOlkAccountHelper,](iolkaccounthelper.md) который предоставляет функции помощника учетной записи. 
    
_dwFlags_
  
> [in] Flags to modify behavior.
    
   - **ACCT_INIT_NO_STORES_CHECK** — предотвращает синхронизацию учетной записи (например, учетной записи IMAP) со связанным хранилищем. 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** — предотвращает синхронизацию служб MAPI с учетными записями. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** — предотвращает перехват диспетчером учетных записей сообщений, предназначенных для других приложений. 
   
   - **OLK_ACCOUNT_NO_FLAGS** — синхронизирует службы MAPI с учетными записями. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Init** уже был вызван.  <br/> |
|E_OLK_REGISTRY  <br/> |Менеджер учетной записи не мог получить доступ к требуемой настройке реестра.  <br/> |
   
## <a name="remarks"></a>Примечания

Клиент должен вызвать **IOlkAccountManager:::Init,** чтобы инициализировать диспетчер учетной записи перед использованием диспетчера учетных записей для доступа к учетным записям или настройка уведомлений. Поскольку Outlook автоматически синхронизирует службы MAPI с учетными записями при запуске, используйте ACCT_INIT_NOSYNCH_MAPI_ACCTS, если нет конкретной причины для синхронизации.  
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)

