---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344382"
---
# <a name="srealarray"></a>SRealArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений float, которые используются для описания свойства типа PT_MV_R4. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений в массиве, на которое указывает элемент **лпфлт** . 
    
 **лпфлт**
  
> Указатель на массив значений с плавающей запятой.
    
## <a name="remarks"></a>Комментарии

Более подробную информацию о типе свойства PT_MV_R4 можно узнать в статье [типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

