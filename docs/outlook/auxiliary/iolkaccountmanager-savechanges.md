---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Сохраняет изменения в указанной учетной записи.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429609"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

Сохраняет изменения в указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Параметры

_dwAcctID_
  
> [in] ИД учетной записи для сохранения. 
    
_dwFlags_
  
> [in] Flags to modify behavior. OLK_ACCOUNT_NO_FLAGS это единственное поддерживаемые значения.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов был успешным  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Не удается найти указанную учетную запись.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Примечания

После изменения значения свойств учетной записи с помощью [IOlkAccount::SetProp](iolkaccount-setprop.md)используйте **IOlkAccountManager::SaveChanges** или [IOlkAccount::SaveChanges,](iolkaccount-savechanges.md) чтобы сохранить такие изменения. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

