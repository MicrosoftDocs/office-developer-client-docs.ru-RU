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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401638"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a>Каноническое свойство PidTagReplyRecipientNames

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список отображаемые имена для получателей, которые требуется получить ответ.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W  <br/> |
|Идентификатор:  <br/> |0x0050  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства содержит отображаемые имена, разделенные точкой с запятой.
  
Если это свойство не указан, ответ отправляется только для пользователя, заданной свойством **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)). При определении **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) и эти свойства, ответ отправляется всех получателей, определяемую средством эти два свойства. Поставщика транспорта использует эти свойства переопределение логики обычной информации.
  
Если значение **PR_REPLY_RECIPIENT_ENTRIES** или эти свойства, необходимо также установлен другие свойства. Эти свойства должно содержать такое же число получателей, и они должны содержать их в том же порядке. Сбой выполняли этих требований может привести к непредсказуемым последствиям. 
  
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

