---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7bcaf230eed9cf21388b68f06ab678dc143f64ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571824"
---
# <a name="proptype"></a>PROP_TYPE

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает тип свойства тега указанного свойства.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Параметры

 _ulPropTag_
  
> Свойство tag, которая содержит тип свойства которого требуется получить.
    
## <a name="remarks"></a>Замечания

Макрос **PROP_TYPE** можно использовать для определения типа свойства. Например вызов результаты PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) в значении PT_BINARY, возвращаемых.
  
Каждого свойства тега содержит тип свойства в word низкого приоритета (бит 0 до 15) и идентификатор свойства в word высокого приоритета (bits 16 до 31). Макрос **PROP_TYPE** извлекает тип свойства и помещает его в бит 0 до 15 целое число должно быть возвращено. Оставшиеся биты возвращаемое значение устанавливаются нули. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

