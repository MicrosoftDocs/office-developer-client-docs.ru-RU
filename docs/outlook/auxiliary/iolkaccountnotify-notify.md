---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Сообщает клиенту об изменениях указанной учетной записи.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424569"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Сообщает клиенту об изменениях указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

См. [IOlkAccountNotify.](iolkaccountnotify.md)
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Параметры

_dwNotify_
  
> [in] Тип уведомления. Поддерживаются такие значения:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> [in] ИД учетной записи, которая была создана, изменена, удалена или предварительно удалена.
    
 _dwFlags_
  
>  [in] Не используется. OLK_ACCOUNT_NO_FLAGS это единственное поддерживаемые значения. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

