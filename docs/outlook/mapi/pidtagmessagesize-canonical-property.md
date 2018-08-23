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
ms.openlocfilehash: c52fd6d6caaec6f215856daead809ceb0bd76729
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574995"
---
# <a name="pidtagmessagesize-canonical-property"></a>Каноническое свойство PidTagMessageSize

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит суммы размеров всех свойств для объекта сообщения, в байтах. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_SIZE  <br/> |
|Идентификатор:  <br/> |0x0E08  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Рекомендуется, что сообщение объекты предоставляют это свойство. Размер сообщения Указывает приблизительное число байтов, которые переносятся при перемещении сообщения из одного хранилища в другое. Что совокупного размера всех свойств объекта сообщения, это обычно значительно больше, чем сам по себе он текста сообщения. 
  
Большинство сообщений хранилища compute поставщиков этого свойства для сообщений, которые они работают. Тем не менее некоторые поставщики хранения сообщения не поддерживают это свойство. В любом случае это свойство недоступно до вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMessage::SubmitMessage](imessage-submitmessage.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папки.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для базовых объектов хранилища сообщений.
    
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

