---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9f8da0902ea4c4a862d279ee80ba566c0473c44e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592327"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описываются ограничения **и** используется для объединения группы с помощью логическую операцию **и** . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> Число ограничения поиска в массиве, на который указывает член **lpRes** . 
    
 **lpRes**
  
> Указатель на массив структур [SRestriction](srestriction.md) , которые будут использоваться в сочетании с логическую операцию **и** . 
    
## <a name="remarks"></a>Замечания

В результате **SAndRestriction** имеет значение TRUE, если все его дочерние ограничения принимают значение TRUE. Это значение FALSE, если любое ограничение дочерних имеет значение FALSE. 
  
Описание ограничений как их, построения и пример кода, обратитесь к разделу [О ограничения](about-restrictions.md).
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

