---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344501"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив целочисленных значений без знака, которые используются для описания свойства типа ПТ_МВ_ШОРТ.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество значений в массиве, на которое указывает элемент **LPI** . 
    
 **LPI**
  
> Указатель на массив значений целых чисел без знака.
    
## <a name="remarks"></a>Комментарии

Дополнительные сведения о ПТ_МВ_ШОРТ и других типах свойств приведены в разделе [типы свойств](property-types.md). 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

