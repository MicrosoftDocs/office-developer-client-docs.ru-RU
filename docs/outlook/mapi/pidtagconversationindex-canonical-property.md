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
  
Содержит двоичное значение, которое указывает относительное положение этого сообщения в цепочке сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Идентификатор:  <br/> |0x0071  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Поток беседы представляет ряд сообщений и ответов. Это свойство обычно реализуется с помощью сцепленных значений отметок времени. Его использование необязательно, даже если задано значение **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)). 
  
MAPI предоставляет функцию [сккреатеконверсатиониндекс](sccreateconversationindex.md) для создания или обновления индекса беседы. Функция принимает текущее значение индекса в виде массива байтов и возвращает значение индекса с отметкой времени, сцепленной с конечной областью. Сообщение, представляющее ответ на другое сообщение, должно использовать **сккреатеконверсатиониндекс** для обновления этого свойства. 
  
У поставщика хранилища сообщений есть возможность гарантировать, что **PR_CONVERSATION_INDEX** всегда устанавливаются для входящих и исходящих сообщений. Это можно сделать, вызвав **сккреатеконверсатиониндекс**, либо с существующим значением, если это свойство задано, либо со значением NULL, если это не так. Это действие следует выполнить перед [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
Все сообщения, имеющие одно и то же значение для **PR_CONVERSATION_TOPIC** , можно сортировать по этому свойству, чтобы отобразить иерархические отношения между сообщениями. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

