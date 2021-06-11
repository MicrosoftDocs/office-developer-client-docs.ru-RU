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
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439088"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение размера, которое используется для проверки размера значения свойства. 
  
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

## <a name="members"></a>"Участники"

 **relop**
  
> Реляционный оператор, используемый в сопоставлении размеров. Возможные значения: 
    
RELOP_GE 
  
> Сравнение выполнено на основе большого или равного первого значения.
    
RELOP_GT 
  
> Сравнение выполнено на основе более первого значения.
    
RELOP_LE 
  
> Сравнение выполнено на основе меньшего или равного первого значения.
    
RELOP_LT 
  
> Сравнение выполнено на основе меньшего первого значения.
    
RELOP_NE 
  
> Сравнение основано на неравных значениях.
    
RELOP_RE 
  
> Сравнение основано на значениях LIKE (регулярное выражение).
    
RELOP_EQ 
  
> Сравнение основано на одинаковых значениях.
    
 **ulPropTag**
  
> Тег свойства, определяющий свойство для тестирования.
    
 **cb**
  
> Количество bytes в значении свойства.
    
## <a name="remarks"></a>Примечания

Общие вопросы о том, как работают ограничения, см. в общих [обсуждениях об ограничениях.](about-restrictions.md) 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

