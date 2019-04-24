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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328569"
---
# <a name="proptag"></a>PROP_TAG

**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает тег свойства, созданный путем объединения указанного типа свойства и идентификатора. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Параметры

_Улпроптипе_
  
> Тип свойства для нового тега свойства.
    
_Улпропид_
  
> Идентификатор свойства для нового тега свойства.
    
## <a name="remarks"></a>Комментарии

Макрос **тега\_Prop** создает тег свойства для свойства типа _улпроптипе_ и идентификатор, указанный в _улпропид_. Например, тег свойства для идентификатора записи можно создать с помощью макроса **проп_таг** следующим образом: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Младшие 16 бит возвращаемого тега свойства содержат тип свойства, ПТ_БИНАРИ, и 16 бит высокого порядка содержат идентификатор свойства, 0xFFFF.
  
Более подробную информацию о тегах свойств можно узнать в статье [теги свойств MAPI](mapi-property-tags.md).
  
## <a name="see-also"></a>См. также

- [SPropValue](spropvalue.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

