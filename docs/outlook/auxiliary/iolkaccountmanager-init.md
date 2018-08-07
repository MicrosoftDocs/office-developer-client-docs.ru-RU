---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Инициализирует диспетчер учетных записей для использования.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807843"
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
    
   - **OLK_ACCOUNT_NO_FLAGS** — служб MAPI синхронизируется с учетными записями. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |Уже был вызван **init** .  <br/> |
|E_OLK_REGISTRY  <br/> |Диспетчер учетных записей не удалось получить доступ к требуемые разделы реестра.  <br/> |
   
## <a name="remarks"></a>Замечания

Клиента необходимо вызвать **IOlkAccountManager::Init** для инициализации учетной записи диспетчера перед использованием диспетчера учетной записи для доступа к учетных записей или настроить уведомления. Так как Outlook автоматически синхронизирует служб MAPI с учетных записей при загрузке системы, используйте **ACCT_INIT_NOSYNCH_MAPI_ACCTS** при отсутствии определенных причина для синхронизации. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)

