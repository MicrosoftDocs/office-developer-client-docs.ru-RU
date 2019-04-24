---
title: Каноническое свойство PidTagOriginalAuthorEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329241"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a>Каноническое свойство PidTagOriginalAuthorEmailAddress

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит адрес электронной почты автора первой версии сообщения, то есть сообщение перед пересылкой или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ОРИГИНАЛ_АУСОР_ЕМАИЛ_АДДРЕСС, ПР_ОРИГИНАЛ_АУСОР_ЕМАИЛ_АДДРЕСС_А, ПР_ОРИГИНАЛ_АУСОР_ЕМАИЛ_АДДРЕСС_В  <br/> |
|Идентификатор:  <br/> |0x007A  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Сервер  <br/> |
   
## <a name="remarks"></a>Комментарии

Эти свойства являются примерами свойств адреса для автора сообщения. При первой отправке сообщения клиентское приложение должно задать для этих свойств значение свойства **пр_сендер_емаил_аддресс** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)). Он никогда не изменяется при пересылке сообщения или ответе на него.
  
Исходные свойства автора допускают сохранение данных извне локального домена обмена сообщениями. Когда сообщение поступает из другого домена обмена сообщениями (например, из Интернета), эти свойства предоставляют способ гарантировать, что исходные данные не будут потеряны.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

