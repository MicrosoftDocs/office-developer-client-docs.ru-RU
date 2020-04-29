---
title: Каноническое свойство PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325622"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>Каноническое свойство PidTagMessageRecipientMe

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если этот пользователь обмена сообщениями является основным (to), Recipient копия (CC) или скрытой копии (BCC) этого сообщения, но не является частью списка рассылки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Идентификатор:  <br/> |0x0059  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предоставляет удобный способ определения того, отображается ли имя пользователя явно в списке получателей, не проверяя все записи в списке. Значение представляет логическую операцию **or** для свойств **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) и **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), а также информацию скрытой копии (которая не отображается в свойстве). 
  
Это свойство помогает автоматически обрабатывать полученные сообщения на момент получения. В параметре поставщика транспорта данное свойство содержит значение FALSE или не включается, если пользователь обмена сообщениями не указан непосредственно в таблице получателей. 
  
Доставка сообщений, получаемых в результате расширения списка рассылки, не приводит к заданию этого свойства. Получатель должен быть явно именованным. 
  
Неотправленные сообщения обычно не задают это свойство, **PR_MESSAGE_CC_ME**или **PR_MESSAGE_TO_ME**. Если они присутствуют в сообщениях, которые пользователь может получить доступ к общедоступным хранилищам сообщений, в личных хранилищах других пользователей, в файлах на диске или во всех полученных сообщениях, они обычно содержат значения, которые были заданы в последний раз, когда поставщик транспорта доставил сообщение. 
  
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

