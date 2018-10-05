---
title: Каноническое свойство PidTagOriginalSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e2c3d2c3-5451-45cb-b0ec-bdbf5b39a0ba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2530e27993163505b28fa7d08fd5caf4cc9b03be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385356"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a>Каноническое свойство PidTagOriginalSentRepresentingEmailAddress

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит адрес электронной почты, обмена мгновенными сообщениями пользователя, от чьего имени исходное сообщение было отправлено.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W  <br/> |
|Идентификатор:  <br/> |0x0069  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства являются примерами свойства адреса для исходного представленного отправителя сообщения. Он используется в потоке беседы.
  
Клиентское приложение отправку сообщения от имени другого клиента эти свойства присвоено значение свойства **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) в первой отправки сообщения. После установки, оно должно быть задано.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
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

