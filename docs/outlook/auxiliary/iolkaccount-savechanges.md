---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Внося изменения в объект учетной записи, написав в хранилище реестра.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425836"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

Внося изменения в объект учетной записи, написав в хранилище реестра.
  
## <a name="quick-info"></a>Краткие сведения

См. [iOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>Parameters

_dwFlags_
  
> [in] Flags to modify behavior. OLK_ACCOUNT_NO_FLAGS является единственным поддерживаемым значением.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Метод был успешным.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Не удается найти указанную учетную запись.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="remarks"></a>Примечания

После изменения значения свойств учетных записей с помощью [IOlkAccount::SetProp](iolkaccount-setprop.md)используйте **IOlkAccount::SaveChanges** для сохранения таких изменений. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

