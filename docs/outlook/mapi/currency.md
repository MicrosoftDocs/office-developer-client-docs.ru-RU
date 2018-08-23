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
ms.openlocfilehash: b5a2cd09942559167300d8a921987864b8c5e48f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576465"
---
# <a name="currency"></a>CURRENCY

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит подписанные 64-разрядное целое, представляющее значение типа currency. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>Members

 **Lo**
  
> Младшие 32 разряда к денежному значению. 
    
 **Привет**
  
> Старшие 32 разряда к денежному значению.
    
## <a name="remarks"></a>Замечания

Структура **валюты** является масштабируемое целое число представлением десятичного числа с четырех цифр справа от десятичной запятой. Например хранимое значение 327500 будет рассматриваться как представление денежной суммы 32.7500. 
  
Структура **CURRENCY** используется для описания свойства типа PT_CURRENCY. Для получения сведений о типах свойств видеть [Обзор типа свойств MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

