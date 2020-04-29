---
title: Каноническое свойство PidTagNull
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNull
api_type:
- HeaderDef
ms.assetid: 192cdab8-c615-47b9-9f04-a1414eaf0c77
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7e9c3340dfad47a811b56c86e8e6104fb6aac7c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329269"
---
# <a name="pidtagnull-canonical-property"></a>Каноническое свойство PidTagNull

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет значение null или значение свойства или резервирует пространство массива.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NULL  <br/> |
|Идентификатор:  <br/> |0x0000  <br/> |
|Тип данных:  <br/> |PT_NULL  <br/> |
|Область:  <br/> |Распространенная  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется для резервного места в массивах структур [спропвалуе](spropvalue.md) . Он используется в массиве структур [спроптагаррай](sproptagarray.md) , чтобы сообщить методу зарезервировать место в возвращенном массиве структур **спропвалуе** . Благодаря этому вычисляемые свойства можно заполнять недорогым образом. 
  
Дополнительные сведения [: Обзор типов свойств MAPI](mapi-property-type-overview.md).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

