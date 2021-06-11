---
title: Каноническое свойство PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aa92e224f10fd652078b965c8e3a0b5ab59cc388
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320043"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a>Каноническое свойство PidTagReadReceiptSearchKey

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для пользователя обмена сообщениями, которому система обмена сообщениями должна направлять отчет о считываемом сообщении.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_READ_RECEIPT_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x0053  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конверт MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство игнорируется, если **PR_READ_RECEIPT_REQUESTED** [(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)свойство true.
  
Если клиентская заявка хочет получать отчеты о прочтении, она может оставить это свойство неустановленным или установить его на ключ поиска, содержащийся в свойстве **PR_SENDER_SEARCH_KEY** [(PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)во время отправки сообщения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые в сообщениях электронной почты.
    
### <a name="header-files"></a>Файлы заголовки

Mapidef.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

