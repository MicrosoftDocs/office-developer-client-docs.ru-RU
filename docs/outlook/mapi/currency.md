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
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808253"
---
# <a name="currency"></a>CURRENCY

  
  
**Относится к**: Outlook 
  
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

