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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение размера, используемое для проверки размера значения свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a>Members

 **релоп**
  
> Оператор отношения, используемый в сравнении размера. Возможны следующие значения: 
    
РЕЛОП_ЖЕ 
  
> Сравнение выполняется на основе значения, равного большему или равному первому значению.
    
РЕЛОП_ГТ 
  
> Сравнение выполняется на основе большего первого значения.
    
РЕЛОП_ЛЕ 
  
> Сравнение выполняется на основе меньшего или равного первого значения.
    
РЕЛОП_ЛТ 
  
> Сравнение выполняется на основе меньшего первого значения.
    
РЕЛОП_НЕ 
  
> Сравнение выполняется на основе неодинаковых значений.
    
РЕЛОП_РЕ 
  
> Сравнение выполняется на основе значений LIKE (регулярное выражение).
    
РЕЛОП_ЕК 
  
> Сравнение выполняется на основе равных значений.
    
 **Улпроптаг**
  
> Тег свойства, определяющий свойство для проверки.
    
 **cb**
  
> Количество байтов в значении свойства.
    
## <a name="remarks"></a>Примечания

Общие сведения о том, как действуют ограничения, можно узнать в статье [ограничения](about-restrictions.md). 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

