---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Фиксирует изменения объекта учетной записи с помощью записи реестра хранилища.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807791"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Фиксирует изменения объекта учетной записи с помощью записи реестра хранилища.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameters

_dwFlags_
  
> [in] Flags to modify behavior. OLK_ACCOUNT_NO_FLAGS — это поддерживается только значение.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |Метод успешно завершена.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Не удается найти указанную учетную запись.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Remarks

После изменения значения свойства учетной записи с помощью [IOlkAccount::SetProp](iolkaccount-setprop.md), используйте **IOlkAccount::SaveChanges** для сохранения такие изменения. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

