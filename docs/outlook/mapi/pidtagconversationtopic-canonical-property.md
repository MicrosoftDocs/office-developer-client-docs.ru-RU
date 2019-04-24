---
title: Каноническое свойство PidTagConversationTopic
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334687"
---
# <a name="pidtagconversationtopic-canonical-property"></a>Каноническое свойство PidTagConversationTopic

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит тему первого сообщения в цепочке бесед. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_КОНВЕРСАТИОН_ТОПИК, ПР_КОНВЕРСАТИОН_ТОПИК_А, ПР_КОНВЕРСАТИОН_ТОПИК_В  <br/> |
|Идентификатор:  <br/> |0x0070  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Комментарии

Поток беседы представляет ряд сообщений и ответов. Эти свойства задаются для первого сообщения в потоке, обычно для свойства **пр_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)). Последующие сообщения в потоке должны использовать одну и ту же тему без изменения. 
  
Свойство **пр_конверсатион_индекс** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) указывает связь порядка между последовательными сообщениями и ответами. Его использование необязательно, даже если заданы эти свойства. 
  
У поставщика хранилища сообщений есть возможность гарантировать, что эти свойства всегда устанавливаются для входящих и исходящих сообщений. Если эти свойства уже заданы, их не следует изменять. В противном случае им можно присвоить значение **пр_нормализед_субжект**. Все действия должны выполняться перед [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

