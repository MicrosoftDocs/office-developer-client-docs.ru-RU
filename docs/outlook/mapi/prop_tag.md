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
ms.openlocfilehash: cbead0a9953ae5106e1fcc7d07d965d4dc7bacb9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570991"
---
# <a name="proptag"></a>PROP_TAG

**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

