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
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331698"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений времени.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений в массиве, на которое указывает элемент **лпат** . 
    
 **лпат**
  
> Указатель на массив значений времени приложения. 
    
## <a name="remarks"></a>Комментарии

Структура **сапптимеаррай** используется для определения свойств типа пт_мв_апптиме. Дополнительные сведения о ПТ_МВ_АППТИМЕ приведены в разделе [список типов свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

