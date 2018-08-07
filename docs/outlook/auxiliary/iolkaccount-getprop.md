---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Получает значение свойства указанной учетной записи.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807793"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Получает значение свойства указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Параметры

_dwProp_
  
> [in] Свойство tag свойства учетной записи для получения.
    
_pVar_
  
> [out] Значение указанного свойства.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |Свойство не найдено для указанной учетной записи.  <br/> |
|E_INVALIDARG  <br/> |Был указан недопустимый свойства тега.  <br/> |
   
## <a name="remarks"></a>Замечания

После этого метода значение, если значение свойства учетной записи — это двоичный файл или строковый тип, необходимо освободить *pVar* с помощью [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

