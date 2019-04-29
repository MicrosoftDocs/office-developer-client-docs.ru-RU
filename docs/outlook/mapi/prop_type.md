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
# <a name="proptype"></a>PROP_TYPE

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает тип свойства указанного тега свойства.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a>Параметры

 _Улпроптаг_
  
> Тег свойства, который содержит возвращаемый тип свойства.
    
## <a name="remarks"></a>Примечания

Макрос **проп_типе** можно использовать для определения типа свойства. Например, вызов ПРОП_ТИПЕ (**пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))) приводит к возврату значения пт_бинари.
  
Каждый тег Property содержит тип свойства в младших словах (в битах от 0 до 15) и идентификатор свойства в высоком уровне (биты от 16 до 31). Макрос **проп_типе** Извлекает тип свойства и преобразует его в двоичные значения, возвращаемые в битах от 0 до 15. Остальные биты возвращаемого значения задаются нулевыми. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

