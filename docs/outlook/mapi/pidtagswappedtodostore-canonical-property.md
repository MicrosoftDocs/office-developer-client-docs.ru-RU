---
title: Каноническое свойство PidTagSwappedToDoStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358907"
---
# <a name="pidtagswappedtodostore-canonical-property"></a>Каноническое свойство PidTagSwappedToDoStore

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет необходимость обработки сообщения после передачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СВАППЕД_ТОДО_СТОРЕ  <br/> |
|Идентификатор:  <br/> |0x0E2C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Несъемный MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство задано для черновика сообщения, его значение должно быть равно значению свойства **пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) сообщения.
  
Для получения дополнительных сведений ознакомьтесь с разделом [[MS – оксофлаг]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) "обработка после передачи помеченного сообщения". 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с пометкой.
    
[[MS — ОКСОРМДР]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Задает свойства и модель взаимодействия для сообщений электронной почты и других объектов.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

