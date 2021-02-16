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
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412837"
---
# <a name="prop_type"></a>PROP_TYPE

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает тип свойства указанного тега свойства.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Параметры

 _ulPropTag_
  
> Тег свойства, содержащий возвращаемого типа свойства.
    
## <a name="remarks"></a>Примечания

Макрос **PROP_TYPE** можно использовать для определения типа свойства. Например, вызов PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) приводит к PT_BINARY возвращаемой.
  
Каждый тег свойства содержит тип свойства в слове низкого порядка (биты от 0 до 15) и идентификатор свойства в слове высокого порядка (биты от 16 до 31). Макрос **PROP_TYPE** извлекает тип свойства и помещает его в биты от 0 до 15 возвращаемого integer. Оставшиеся биты возвращаемого значения имеют нулевое значение. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

