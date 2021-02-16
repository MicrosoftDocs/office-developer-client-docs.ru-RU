---
title: Каноническое свойство PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355652"
---
# <a name="pidtagmessagesize-canonical-property"></a>Каноническое свойство PidTagMessageSize

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сумму (в bytes) размеров всех свойств объекта сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_SIZE  <br/> |
|Идентификатор:  <br/> |0x0E08  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы объекты сообщений выдали это свойство. Размер сообщения указывает приблизительное количество ветвей, которые передаются при перемещении сообщения из одного хранилище в другое. Суммы всех свойств объекта сообщения обычно значительно больше, чем текст сообщения. 
  
Большинство поставщиков store сообщений вычисляют это свойство для сообщений, которые они обрабатывают. Однако некоторые поставщики store сообщений не поддерживают это свойство. В любом случае это свойство будет доступно только после того, как будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMessage::SubmitMessage.](imessage-submitmessage.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции с папками.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для основных объектов хранения сообщений.
    
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

