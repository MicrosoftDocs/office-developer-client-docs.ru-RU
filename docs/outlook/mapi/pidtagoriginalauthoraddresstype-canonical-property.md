---
title: Каноническое свойство PidTagOriginalAuthorAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 596e416624fb6f2bf1fdaef64c2179feb7787815
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431416"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a>Каноническое свойство PidTagOriginalAuthorAddressType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тип адреса автора первой версии сообщения, то есть сообщения перед переададащением или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W  <br/> |
|Идентификатор:  <br/> |0x0079  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства являются примерами свойств адреса для автора сообщения. При первой отправке сообщения клиентские приложения должны установить для этого свойства значение свойства **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType).](pidtagsenderaddresstype-canonical-property.md) Оно никогда не меняется, когда сообщение переадововыно или на него отвечает.
  
Исходные свойства автора позволяют сохранить сведения из-за пределов локального домена обмена сообщениями. Когда сообщение поступает из другого домена обмена сообщениями, например из Интернета, эти свойства предоставляют способ убедиться, что исходная информация не потеряна.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

