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
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425885"
---
# <a name="prop_tag"></a>PROP_TAG

**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает тег свойства, созданный путем объединения указанного типа свойства и идентификатора. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Параметры

_улпроптипе_
  
> Тип свойства для нового тега свойства.
    
_улпропид_
  
> Идентификатор свойства для нового тега свойства.
    
## <a name="remarks"></a>Примечания

Макрос **тега\_Prop** создает тег свойства для свойства типа _улпроптипе_ и идентификатор, указанный в _улпропид_. Например, тег свойства для идентификатора записи можно создать с помощью макроса **PROP_TAG** следующим образом: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Младшие 16 бит возвращаемого тега свойства содержат тип свойства, PT_BINARY, а старшие 16 бит содержат идентификатор свойства, 0xFFFF.
  
Более подробную информацию о тегах свойств можно узнать в статье [теги свойств MAPI](mapi-property-tags.md).
  
## <a name="see-also"></a>См. также

- [SPropValue](spropvalue.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

