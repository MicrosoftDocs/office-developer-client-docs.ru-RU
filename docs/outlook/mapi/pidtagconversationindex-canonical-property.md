---
title: Каноническое свойство PidTagConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334722"
---
# <a name="pidtagconversationindex-canonical-property"></a>Каноническое свойство PidTagConversationIndex

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит двоичное значение, которое указывает относительное положение этого сообщения в цепочке беседы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Идентификатор:  <br/> |0x0071  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Цепочка бесед представляет серию сообщений и ответов. Как правило, это свойство реализуется с использованием совмещенных значений отметки времени. Его использование является необязательным, **даже PR_CONVERSATION_TOPIC** ([PidTagConversationTopic).](pidtagconversationtopic-canonical-property.md) 
  
MAPI предоставляет [функцию ScCreateConversationIndex](sccreateconversationindex.md) для создания или обновления индекса беседы. Функция принимает текущее значение индекса в качестве массива с подсчетом byte и возвращает значение индекса с отметкой времени, совмещенной в конце. Сообщение, представляющее ответ на другое сообщение, должно использовать **ScCreateConversationIndex** для обновления этого свойства. 
  
У поставщика store сообщений есть  возможность проверить, PR_CONVERSATION_INDEX всегда настроены для входящих или исходяющих сообщений. Это можно сделать, вызывая **ScCreateConversationIndex** либо с существующим значением, если это свойство установлено, либо с NULL, если это не так. Это действие следует сделать перед тем, как [будет вызван IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
Все сообщения с одинаковым значением **для** PR_CONVERSATION_TOPIC можно отсортировать по этому свойству для раскрытия иерархической связи сообщений. 
  
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

