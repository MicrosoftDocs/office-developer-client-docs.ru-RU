---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Задает значение свойства указанной учетной записи.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807810"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Задает значение свойства указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Параметры

_dwProp_
  
> [in] Свойство tag свойства учетной записи для установки.
    
_pVar_
  
> [in] Значение указанного свойства.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |Вызов метода прошла успешно.  <br/> |
|E_INVALIDARG  <br/> |Указан недопустимый свойства тега.  <br/> |
   
## <a name="remarks"></a>Замечания

Используйте [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) , чтобы сохранить изменения значений свойств учетной записи. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

