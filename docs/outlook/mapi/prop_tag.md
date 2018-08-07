---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e53c39b713aa782eb387b85667f5ded6193006f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812059"
---
# <a name="proptag"></a>PROP_TAG

**Относится к**: Outlook 
  
Возвращает свойство тег, созданные путем объединения тип указанного свойства и идентификатор. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Параметры

_ulPropType_
  
> Тип свойства для нового свойства тега.
    
_ulPropID_
  
> Идентификатор свойства для нового свойства тега.
    
## <a name="remarks"></a>Замечания

**Свойства\_ТЕГА** макрос создает тег свойства для свойства типа _ulPropType_ и идентификатор, который указан в _ulPropID_. Например тег свойства для идентификатора записи могут создаваться с помощью макроса **PROP_TAG** следующим образом: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

16 бит низкого приоритета возвращаемого свойства тега содержит тип свойства, PT_BINARY, и старшие 16 бит содержит идентификатор свойства 0xFFFF.
  
Дополнительные сведения о тегах свойств можно [Тегов свойств MAPI](mapi-property-tags.md).
  
## <a name="see-also"></a>См. также

- [SPropValue](spropvalue.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

