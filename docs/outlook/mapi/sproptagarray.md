---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5237a5c2767920bdb604bfe86603cea4fca56b84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572776"
---
# <a name="sproptagarray"></a>SPropTagArray

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив тегов свойств. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md) [SizedSPropTagArray](sizedsproptagarray.md) <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Count свойство теги в массиве, указанный в параметре члена **aulPropTag** . 
    
 **aulPropTag**
  
> Массив, содержащий тегов свойств.
    
## <a name="remarks"></a>Замечания

Свойство tag является целым числом без знака 32-разрядная версия, которая состоит из двух частей: 
  
- Идентификатор в 16 бит высокого приоритета.
    
- Тип в 16 бит низкого приоритета.
    
Идентификатор — числовое значение в определенный диапазон. Диапазоны идентификаторов для описания, для чего используется свойство и кто несет ответственность за обеспечение его определены MAPI. MAPI определяет ограничения для каждого из тегов свойств, поддерживаемых в файле заголовка Mapitags.h.
  
Тип указывает формат, для которых значение свойства. MAPI определяет константы для каждого типа свойства, поддерживаемые в файле заголовка Mapidefs.h. 
  
Дополнительные сведения о тегах свойств и их компоненты см. 
  
[Теги свойства MAPI](mapi-property-tags.md)
  
[Обзор свойств идентификатор MAPI](mapi-property-identifier-overview.md)
  
[Обзор типов свойств MAPI](mapi-property-type-overview.md)
  
Полный список типов одним значением и многозначных свойств содержатся в приложении, [типов и идентификаторы свойств](property-identifiers-and-types.md). 
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

