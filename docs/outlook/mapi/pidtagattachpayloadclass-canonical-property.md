---
title: Каноническое свойство PidTagAttachPayloadClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6a84e51325fcb60c54c2f6b42af0c26a0efd3382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327239"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a>Каноническое свойство PidTagAttachPayloadClass

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля загона X-Payload-Class MIME.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W  <br/> |
|Идентификатор:  <br/> |0x371A  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Приложение Outlook  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы установить значение этих свойств, клиенты MIME должны записать поле загона X-Payload-Class в объект MIME, который будет проанализирован как вложение.
  
Читатели MIME должны скопировать это значение поля в значение соответствующего свойства. Читатели MIME должны игнорировать это поле, если оно отображается в объекте MIME, который анализируется как сообщение или текст сообщения, а не как вложение.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.
    
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

