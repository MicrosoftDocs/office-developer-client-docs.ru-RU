---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409134"
---
# <a name="prop_id"></a>PROP_ID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор указанного тега свойства.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Параметры

 _ulPropTag_
  
> Тег свойства, содержащий возвращаемую идентификатор.
    
## <a name="remarks"></a>Примечания

Каждый тег свойства содержит тип свойства в слове низкого порядка (биты от 0 до 15) и идентификатор свойства в слове высокого порядка (биты от 16 до 31). Макрос **PROP_ID** извлекает идентификатор свойства и помещает его в биты от 0 до 15 возвращаемого integer. Оставшиеся биты возвращаемого значения имеют нулевое значение. 
  
Макрос **PROP_ID** можно использовать, например, для получения идентификатора, передав его в [IMAPIProp::GetNamesFromIDs.](imapiprop-getnamesfromids.md) **GetNamesFromIDs** извлекает имя свойства, связанное с идентификатором именоваемой свойства. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

