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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383627"
---
# <a name="pidtagconversationindex-canonical-property"></a>Каноническое свойство PidTagConversationIndex

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит двоичные значение, указывающее, относительное положение этого сообщения в рамках потока беседы. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Идентификатор:  <br/> |0x0071  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Поток беседы представляет ряд сообщения и ответы. Обычно это свойство реализуется с помощью значений составное временной метки. Ее использования является необязательным, даже в том случае, если установлено **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)). 
  
MAPI предоставляет функцию [ScCreateConversationIndex](sccreateconversationindex.md) для создания или обновления индекса беседы. Функция принимает текущее значение индекса в виде массива байтов инвентаризации и возвращает значение индекса с отметкой времени, присоединенным в конце. Сообщение, представляющий ответ на другое сообщение необходимо использовать **ScCreateConversationIndex** для обновления этого свойства. 
  
Поставщик хранения сообщений имеет возможность подтверждения, **PR_CONVERSATION_INDEX** всегда установлено для входящих или исходящих сообщений. Его можно сделать, вызвав **ScCreateConversationIndex**, существующее значение, если значение этого свойства или значение NULL, если он не установлен. Это действие следует применять до вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
  
Все сообщения, которые имеют одинаковые значения для **PR_CONVERSATION_TOPIC** можно сортировать на это свойство, чтобы показать иерархическую связь сообщений. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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

