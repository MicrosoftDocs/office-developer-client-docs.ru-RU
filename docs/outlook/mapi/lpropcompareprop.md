---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414615"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает два значения свойств, чтобы определить, равны ли они. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parameters

 _lpSPropValueA_
  
> [in] Указатель на [структуру SPropValue,](spropvalue.md) определяющей первое значение свойства, с чем следует сравнивать. 
    
 _lpSPropValueB_
  
> [in] Указатель на **структуру SPropValue,** определяющей второе значение свойства, для сравнении. 
    
## <a name="return-value"></a>Возвращаемое значение

 **LPropCompareProp** возвращает одно из следующих значений для большинства типов свойств: 
  
- Меньше нуля, если значение, которое указывает параметр _lpSPropValueA,_ меньше, чем указывает параметр _lpSPropValueB._ 
    
- Больше нуля, если значение _lpSPropValueA_ больше, чем указано _в lpSPropValueB._
    
- Ноль, если значение _lpSPropValueA_ равно значению _lpSPropValueB._ 
    
Для типов свойств, которые не имеют внутреннего порядка, таких как типы boolean или ошибки, функция **LPropCompareProp** возвращает неопределимое значение, если оба значения свойств не равны. Это неопределяемая величина является незеро и согласуется между вызовами. 
  
## <a name="remarks"></a>Примечания

Используйте **функцию LPropCompareProp** только в том случае, если типы двух свойств, которые необходимо сравнить, одинаковы. 
  
Перед вызовом **LPropCompareProp** клиентские приложения или поставщик услуг должны сначала получить свойства для сравнения с вызовом метода [IMAPIProp::GetProps.](imapiprop-getprops.md) Когда клиент или поставщик вызывает **LPropCompareProp,** функция сначала проверяет теги свойств, чтобы убедиться, что сравнение значений свойств допустимо. Затем функция сравнивает значения свойств, возвращая соответствующее значение. 
  
Если значения свойств неравны, **LPropCompareProp** определяет, какой из них больше. Свойства, которые **сравнивает LPropCompareProp,** не должны принадлежать одному объекту. 
  

