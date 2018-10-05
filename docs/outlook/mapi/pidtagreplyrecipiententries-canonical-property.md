---
title: Каноническое свойство PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400966"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>Каноническое свойство PidTagReplyRecipientEntries

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив размера запись идентификаторов для получателей, которые требуется получить ответ.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|Идентификатор:  <br/> |0x004F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит структуру [FLATENTRYLIST](flatentrylist.md) и не является многозначным свойством. 
  
Если это свойство не указан, ответ отправляется только для пользователя, заданной свойством **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)). При определении свойства **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) и это ответ отправляется всех получателей, определяемую средством эти два свойства. Поставщика транспорта использует эти свойства переопределение логики обычной информации.
  
Если задано это свойство или свойство **PR_REPLY_RECIPIENT_NAMES** , необходимо также установлен другие свойства. Эти свойства должно содержать такое же число получателей, и они должны содержать их в том же порядке. Сбой выполняли этих требований может привести к непредсказуемым последствиям. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые в сообщениях электронной почты.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
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

