---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Уведомляет клиента о изменения для указанной учетной записи.
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807866"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Уведомляет клиента о изменения для указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccountNotify](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parameters

_dwNotify_
  
> [in] Тип уведомления. The value must be one of the following:
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> [in] Идентификатор учетной записи для учетной записи, которые были созданы, изменяется, удаления или предварительно удален.
    
 _dwFlags_
  
>  [in] Не используется. OLK_ACCOUNT_NO_FLAGS — это поддерживается только значение. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

