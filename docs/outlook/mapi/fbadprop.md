---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578852"
---
# <a name="fbadprop"></a>FBadProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет определенное свойство. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a>Параметры

 _lpprop_
  
> [in] Структура [SPropValue](spropvalue.md) определяет свойство, которое необходимо проверить. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указанное свойство недопустимо. 
    
FALSE 
  
> Указанное свойство допустимо.
    
## <a name="remarks"></a>Замечания

Существует несколько причин для вызова функции **FBadProp** поставщиком услуг. Например, это может быть сделано для подготовки вызова метода [IMAPIProp::SetProps](imapiprop-setprops.md), задающего свойство. **FBadProp** выбирает ход проверки для указанного свойства в зависимости от его типа. Например, если свойство является логическим, **FBadProp** необходимо убедиться, что ему присвоено одно из значений: TRUE или FALSE. Для двоичных свойств **FBadProp** проверяет указатель, размер и правильность выделения. 
  
## <a name="see-also"></a>См. также



[FBadPropTag](fbadproptag.md)

