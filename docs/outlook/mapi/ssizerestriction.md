---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 990fe49d39a73c5bf80b9fdda96d2e5997869edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595421"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описываются ограничения размера, который используется для тестирования размера значение свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a>Members

 **RelOp**
  
> Оператор, который используется для сравнения размера. Ниже приведены возможные значения: 
    
RELOP_GE 
  
> Сравнение выполняется на основе больше или равно первого значения.
    
RELOP_GT 
  
> Сравнение выполняется на основе больше первого значения.
    
RELOP_LE 
  
> Сравнение выполняется на основе меньше или равно первого значения.
    
RELOP_LT 
  
> Сравнение выполняется на основе меньшим первое значение.
    
RELOP_NE 
  
> Сравнение выполняется на основе разные значения.
    
RELOP_RE 
  
> Сравнение выполняется на основе как значения (регулярное выражение).
    
RELOP_EQ 
  
> Сравнение выполняется на основе одинаковые значения.
    
 **ulPropTag**
  
> Свойство tag идентификации свойства для тестирования.
    
 **cb**
  
> Число байт в значение свойства.
    
## <a name="remarks"></a>Замечания

Общие сведения о работе ограничения обратитесь к разделу [О ограничения](about-restrictions.md). 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

