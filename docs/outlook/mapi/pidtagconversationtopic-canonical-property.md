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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тему первого сообщения в цепочке беседы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W  <br/> |
|Идентификатор:  <br/> |0x0070  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Цепочка бесед представляет серию сообщений и ответов. Эти свойства задаются для первого сообщения в потоке, как правило, для свойства **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject).](pidtagnormalizedsubject-canonical-property.md) Последующие сообщения в потоке должны использовать тот же раздел без изменений. 
  
Свойство **PR_CONVERSATION_INDEX** ([PidTagConversationIndex)](pidtagconversationindex-canonical-property.md)указывает порядок между последующими сообщениями и ответами. Его использование является необязательным, даже если за установлены эти свойства. 
  
Поставщик store сообщений может быть уверены, что эти свойства всегда задаются для входящих или исходяющих сообщений. Если эти свойства уже за установлены, их не следует изменять. Если это не так, их можно **PR_NORMALIZED_SUBJECT.** Перед тем как будет вызван [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) необходимо принять любое действие. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

