---
title: Каноническое свойство PidTagOriginallyIntendedRecipEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginallyIntendedRecipEmailAddress
api_type:
- COM
ms.assetid: 6a85b695-731a-4401-9c9c-fda6bc308558
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f4adbdfc041ebe5213c384db98343baa82af5b05
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572727"
---
# <a name="pidtagoriginallyintendedrecipemailaddress-canonical-property"></a>Каноническое свойство PidTagOriginallyIntendedRecipEmailAddress

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит адрес электронной почты, изначально требуемого получателя сообщения автоматически переадресовано.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_A, PR_ORIGINALLY_INTENDED_RECIP_EMAIL_ADDRESS_W  <br/> |
|Идентификатор:  <br/> |0x007C  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Сервер  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства являются примерами свойства адреса для получателя, изначально предполагаемая сообщения. Им должен иметь значение агентом автоматическое перенаправление сообщения.
  
Эти свойства соответствуют атрибут каждого получателя отчета X.400.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

