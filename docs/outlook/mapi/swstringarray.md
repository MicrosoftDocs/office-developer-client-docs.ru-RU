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
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812438"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Относится к**: Outlook 
  
Содержит массив строк символов, которые используются для описания свойства типа PT_MV_UNICODE. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Количество строк в массиве, на который указывает член **lppszW** . 
    
 **lppszW**
  
> Указатель на массив строк символ Unicode завершен null.
    
## <a name="remarks"></a>Замечания

Дополнительные сведения о PT_MV_UNICODE можно [Типы свойств](property-types.md).
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

