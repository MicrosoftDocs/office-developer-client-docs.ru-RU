---
title: Каноническое свойство PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329738"
---
# <a name="pidtagmessageccme-canonical-property"></a>Каноническое свойство PidTagMessageCcMe

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если этот пользователь системы обмена сообщениями является особым именем получателя копии этого сообщения и не входит в список рассылки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_МЕССАЖЕ_КК_МЕ  <br/> |
|Идентификатор:  <br/> |0x0058  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство предоставляет удобный способ определения того, отображается ли имя пользователя явно в списке получателей копии, не проверяя все записи в списке. 
  
Это свойство также помогает автоматически обрабатывать полученные сообщения на момент получения. В параметре поставщика транспорта данное свойство содержит значение FALSE или не задано, если пользователь обмена сообщениями не указан непосредственно в таблице получателей. 
  
При доставке сообщений из расширения списка рассылки или с помощью скрытой копии это свойство не задается. Получатель должен быть явно именованным. 
  
Неотправленные сообщения обычно не задают значение этого свойства, **пр_мессаже_реЦип_ме** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) или **пр_мессаже_то_ме** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)). Если они присутствуют в сообщениях, которые пользователь может получить доступ к хранилищам общедоступных сообщений, в частных хранилищах других пользователей, в файлах на диске или во всех полученных сообщениях, они обычно содержат значения, для которых они были заданы в последний раз, когда поставщик транспорта доставлено сообщение. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

