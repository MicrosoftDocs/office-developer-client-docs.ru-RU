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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если этот пользователь обмена сообщениями конкретно назван в качестве основного (To), углеродной копии (CC) или слепой копии углерода (BCC) получателя этого сообщения и не входит в список рассылки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Идентификатор:  <br/> |0x0059  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство позволяет определить, явно ли имя пользователя отображается в списке получателей без изучения всех записей в списке. Это значение представляет  логическую операцию или эксплуатацию свойств **PR_MESSAGE_CC_ME** [(PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md)и **PR_MESSAGE_TO_ME** [(PidTagMessageToMe)](pidtagmessagetome-canonical-property.md)и сведений BCC (которые не отображаются в свойстве). 
  
Это свойство помогает автоматизированной обработке полученных сообщений во время получения. В варианте поставщика транспорта это свойство содержит FALSE или не включается, если пользователь обмена сообщениями не указан непосредственно в таблице получателей. 
  
Доставка сообщений в результате расширения списка рассылки не вызывает задатки этого свойства. Получатель должен быть явно назван. 
  
Неуявные сообщения обычно не устанавливают это **свойство, PR_MESSAGE_CC_ME** или **PR_MESSAGE_TO_ME**. Если они присутствуют в сообщениях, к которым пользователь может получить доступ в общедоступных хранилищах сообщений, в частных магазинах других пользователей, в файлах на диске или встроенных внутри других полученных сообщений, они обычно содержат значения, которым они были заданы при последнем доставке сообщения поставщиком транспорта. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые на объектах сообщений электронной почты.
    
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

