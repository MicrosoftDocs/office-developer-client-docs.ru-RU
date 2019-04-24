---
title: Каноническое свойство PidTagReplyRecipientNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355176"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>Каноническое свойство PidTagReplyRecipientNames

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список отображаемых имен получателей, которые должны получить ответ.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РЕПЛИ_РЕЦИПИЕНТ_НАМЕС, ПР_РЕПЛИ_РЕЦИПИЕНТ_НАМЕС_А, ПР_РЕПЛИ_РЕЦИПИЕНТ_НАМЕС_В  <br/> |
|Идентификатор:  <br/> |0x0050  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства содержат отображаемые имена, разделенные точкой с запятой.
  
Если это свойство отсутствует, ответ отправляется только пользователю, определенному в свойстве **пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md)). Когда **пр_репли_реЦипиент_ентриес** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) и эти свойства определены, ответ отправляется всем получателям, идентифицируемым этими двумя свойствами. Поставщик транспорта использует эти свойства для переопределения обычной логики ответа.
  
Если задано значение **пр_репли_реЦипиент_ентриес** или эти свойства, то другое свойство также должно быть задано. Эти свойства должны содержать одинаковое количество получателей и должны содержать их в одном порядке. НеВозможность проследить эти требования могут привести к непредсказуемым результатам. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для сообщений электронной почты.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
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

