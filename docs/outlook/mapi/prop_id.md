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
ms.openlocfilehash: e1846b4be93bf6300ea89a9ae3133fbba82b344e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573126"
---
# <a name="propid"></a>PROP_ID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор свойства tag указанного свойства.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a>Параметры

 _ulPropTag_
  
> Тег свойства, содержащее идентификатор которого требуется получить.
    
## <a name="remarks"></a>Замечания

Каждого свойства тега содержит тип свойства в word низкого приоритета (бит 0 до 15) и идентификатор свойства в word высокого приоритета (bits 16 до 31). Макрос **PROP_ID** извлекает идентификатор свойства и помещает его в бит 0 до 15 целое число должно быть возвращено. Оставшиеся биты возвращаемое значение устанавливаются нули. 
  
Например, макрос **PROP_ID** можно использовать для получения идентификатора для передачи [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). **GetNamesFromIDs** возвращает имя свойства, связанного с идентификатором для именованного свойства. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

