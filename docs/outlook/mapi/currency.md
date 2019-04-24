---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315136"
---
# <a name="currency"></a>CURRENCY

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит подписанное 64 — разрядное целое число, представляющее значение денежной единицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>Members

 **Lo**
  
> Младшие биты 32 значения денежной единицы. 
    
 **Привет**
  
> 32 бит высокого порядка для денежного значения.
    
## <a name="remarks"></a>Замечания

Структура **валюты** — это масштабированное целое число десятичного числа с четырьмя цифрами справа от десятичной точки. Например, сохраненное значение 327500 — это представление денежного значения 32,7500. 
  
Структура **валюты** используется для описания свойства типа пт_курренци. Сведения о типах свойств приведены в разделе [Обзор типов свойств MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

