---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a44974accea30b5d1406c9cc74570012f61639e5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580651"
---
# <a name="slongarray"></a>SLongArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив типов значение типа LONG, которые используются для описания свойства типа PT_MV_LONG. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Число значений в массиве, на который указывает член **lpl** . 
    
 **lpl**
  
> Указатель на массив значений времени.
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о PT_MV_LONG увидеть [Список типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

