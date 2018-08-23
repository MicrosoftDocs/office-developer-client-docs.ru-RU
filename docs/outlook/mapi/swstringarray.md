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
ms.openlocfilehash: e3f53a894b7f7cdaa68e66530c7bd99bf49b9ed0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581358"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

