---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dc90f15835de35354a271d87a736366a4caf8dd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578782"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений времени, которые используются для описания свойства типа PT_MV_SYSTIME.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Число значений в массиве, на который указывает член **lpft** . 
    
 **lpft**
  
> Указатель на массив структур [FILETIME](filetime.md) , содержащих значения времени. 
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о PT_MV_SYSTIME увидеть [Список типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

