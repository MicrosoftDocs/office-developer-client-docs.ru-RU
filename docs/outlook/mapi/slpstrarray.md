---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361154"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив строковых значений, которые используются для описания свойства типа PT_MV_STRING8.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений в массиве, на которое указывает элемент **лппсза** . 
    
 **Лппсза**
  
> Указатель на массив 8 – разрядных символьных строк со значением NULL.
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о PT_MV_STRING8 приведены в разделе [список типов свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

