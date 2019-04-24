---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349555"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив строк символов, которые используются для описания свойства типа ПТ_МВ_УНИКОДЕ. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **Квалуес**
  
> Количество строк в массиве, на которое указывает элемент **лппсзв** . 
    
 **Лппсзв**
  
> Указатель на массив строк Юникода с символами NULL.
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о ПТ_МВ_УНИКОДЕ можно найти в статье [типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

