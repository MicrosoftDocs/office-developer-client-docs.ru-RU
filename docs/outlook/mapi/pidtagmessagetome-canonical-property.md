---
title: Каноническое свойство PidTagMessageToMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96a0b010a8ba26a0c1b0cb409f1aaabb308a1c01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356198"
---
# <a name="pidtagmessagetome-canonical-property"></a>Каноническое свойство PidTagMessageToMe

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит true, если этот пользователь обмена сообщениями назван в качестве основного получателя (To) этого сообщения и не входит в список рассылки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_TO_ME  <br/> |
|Идентификатор:  <br/> |0x0057  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предоставляет удобный способ определить, отображается ли имя пользователя явным образом в основном списке получателей без проверки всех записей в списке. 
  
Это свойство также помогает автоматизировать обработку полученных сообщений во время получения. При указании поставщика транспорта это свойство либо содержит false, либо не включается, если пользователь обмена сообщениями не указан непосредственно в таблице получателей. 
  
Доставка сообщений в результате расширения списка рассылки или обозначений незрячих копий не приводит к задамлности этого свойства. Получатель должен иметь явное имя. 
  
Как правило, неподписаные сообщения не устанавливают PR_MESSAGE_CC_ME **(** [PidTagMessageCcMe),](pidtagmessageccme-canonical-property.md) **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe)](pidtagmessagerecipientme-canonical-property.md)или это свойство. Если они присутствуют в сообщениях, к которым пользователь может получить доступ в общедоступных хранилищах сообщений, в частных хранилищах других пользователей, в файлах на диске или внедренных в другие полученные сообщения, они обычно содержат значения, которыми они были заданы при последней доставке сообщения поставщиком транспорта. 
  
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

