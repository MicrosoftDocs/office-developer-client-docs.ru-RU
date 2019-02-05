---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Инициализирует диспетчер учетных записей для использования.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: b361919ae2d3ac000d9fcaa3030713df7062ecd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/02/2019
ms.locfileid: "29715342"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

Инициализирует диспетчер учетных записей для использования.
  
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
  
> [in] Интерфейс [IOlkAccountHelper](iolkaccounthelper.md) , предоставляющая функциональные возможности модуля поддержки учетной записи. 
    
_dwFlags_
  
> [in] Flags to modify behavior.
    
   - **ACCT_INIT_NO_STORES_CHECK** — запрещает синхронизацию с связанного хранилища учетной записи (например, учетной записи IMAP). 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** — служб MAPI, не позволяет синхронизировать с учетными записями. 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** — запрещает диспетчер учетных записей перехват широковещательные сообщения, для других приложений. 
   
   - **OLK_ACCOUNT_NO_FLAGS** — служб MAPI синхронизируется с учетными записями. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |Уже был вызван **init** .  <br/> |
|E_OLK_REGISTRY  <br/> |Диспетчер учетных записей не удалось получить доступ к требуемые разделы реестра.  <br/> |
   
## <a name="remarks"></a>Комментарии

Клиента необходимо вызвать **IOlkAccountManager::Init** для инициализации учетной записи диспетчера перед использованием диспетчера учетной записи для доступа к учетных записей или настроить уведомления. Так как Outlook автоматически синхронизирует служб MAPI с учетных записей при загрузке системы, используйте **ACCT_INIT_NOSYNCH_MAPI_ACCTS** при отсутствии определенных причина для синхронизации. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)

