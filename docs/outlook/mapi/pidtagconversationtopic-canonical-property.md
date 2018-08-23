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
ms.openlocfilehash: ce9d13b6ecd560798cee4f79d8d62b966dc427f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586475"
---
# <a name="pidtagconversationtopic-canonical-property"></a>Каноническое свойство PidTagConversationTopic

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит раздел первого сообщения в потоке беседы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W  <br/> |
|Идентификатор:  <br/> |0x0070  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Поток беседы представляет ряд сообщения и ответы. Эти свойства задаются для первого сообщения в потоке, обычно к свойству **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)). Длина последующих сообщений в потоке следует использовать же раздел без изменений. 
  
Свойство **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) указывает порядок отношение между последующие сообщения и ответы. Ее использования является необязательным, даже в том случае, если заданы следующие свойства. 
  
Поставщик хранения сообщений имеет возможность подтверждения, которое всегда эти свойства задаются на входящих или исходящих сообщений. Если эти свойства уже установлены они не может быть изменен. В противном случае может иметь значение **PR_NORMALIZED_SUBJECT**. Должна быть переведена каких-либо действий в до вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

