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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит true, если этот пользователь обмена сообщениями имеет имя получателя копии этого сообщения и не входит в список рассылки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Идентификатор:  <br/> |0x0058  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предоставляет удобный способ определить, отображается ли имя пользователя явным образом в списке получателей копии копии без проверки всех записей в списке. 
  
Это свойство также помогает автоматизировать обработку полученных сообщений во время получения. При указании поставщика транспорта это свойство либо содержит false, либо не занося, если пользователь обмена сообщениями не указан непосредственно в таблице получателей. 
  
Доставка сообщений в результате расширения списка рассылки или обозначений незрячих копий не приводит к задамлности этого свойства. Получатель должен иметь явное имя. 
  
Как правило, для неавторенных сообщений это свойство не задавалось, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe)](pidtagmessagerecipientme-canonical-property.md)или **PR_MESSAGE_TO_ME** ([PidTagMessageToMe).](pidtagmessagetome-canonical-property.md) Если они присутствуют в сообщениях, к которым пользователь может получить доступ в общедоступных хранилищах сообщений, в частных хранилищах других пользователей, в файлах на диске или внедренных в другие полученные сообщения, они обычно содержат значения, которыми они были заданы при последней доставке сообщения поставщиком транспорта. 
  
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

