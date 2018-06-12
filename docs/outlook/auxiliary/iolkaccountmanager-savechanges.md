---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Сохраняет изменения указанной учетной записи.
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807861"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Сохраняет изменения указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameters

_dwAcctID_
  
> [in] Идентификатор учетной записи, чтобы сохранить. 
    
_dwFlags_
  
> [in] Flags to modify behavior. OLK_ACCOUNT_NO_FLAGS — это поддерживается только значение.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |Вызов успешно завершен  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Не удается найти указанную учетную запись.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Remarks

После изменения значения свойства учетной записи с помощью [IOlkAccount::SetProp](iolkaccount-setprop.md), используйте **IOlkAccountManager::SaveChanges** или [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) для сохранения такие изменения. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

