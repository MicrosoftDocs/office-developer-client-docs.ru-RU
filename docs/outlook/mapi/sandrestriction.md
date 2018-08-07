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
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812189"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Относится к**: Outlook 
  
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

