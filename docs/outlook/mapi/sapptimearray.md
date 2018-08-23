---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d277908d3ec96537f63511e4d50488a694696bd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581225"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений времени.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Число значений в массиве, на который указывает член **lpat** . 
    
 **lpat**
  
> Указатель на массив значений времени приложения. 
    
## <a name="remarks"></a>Замечания

Структура **SAppTimeArray** используется для определения свойства типа PT_MV_APPTIME. Дополнительные сведения о PT_MV_APPTIME увидеть [Список типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

