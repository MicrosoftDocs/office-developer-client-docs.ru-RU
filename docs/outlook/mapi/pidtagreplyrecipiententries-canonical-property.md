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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355057"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a>Каноническое свойство PidTagReplyRecipientEntries

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит большой массив идентификаторов записей для получателей, которые должны получить ответ.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REPLY_RECIPIENT_ENTRIES  <br/> |
|Идентификатор:  <br/> |0x004F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит [структуру FLATENTRYLIST](flatentrylist.md) и не является многоценным свойством. 
  
Если этого свойства нет, ответ отправляется только пользователю, идентифицированным свойством **PR_SENDER_ENTRYID** [(PidTagSenderEntryId).](pidtagsenderentryid-canonical-property.md) Когда определяются свойства **PR_REPLY_RECIPIENT_NAMES** [(PidTagReplyRecipientNames),](pidtagreplyrecipientnames-canonical-property.md)ответ отправляется всем получателям, указанным этими двумя свойствами. Поставщик транспорта использует эти свойства для переопределения обычной логики ответа.
  
Если заданной PR_REPLY_RECIPIENT_NAMES  или PR_REPLY_RECIPIENT_NAMES, необходимо также установить другое свойство. Эти свойства должны содержать одинаковое число получателей и содержать их в том же порядке. Несоблюдение этих требований может привести к непредсказуемым результатам. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые в сообщениях электронной почты.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных конвенций электронной почты в объекты сообщений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

