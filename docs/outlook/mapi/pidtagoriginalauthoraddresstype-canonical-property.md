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
ms.openlocfilehash: bc3c06c38f8ff8121a8503341cdd1084c036e52d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589975"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a>Каноническое свойство PidTagOriginalAuthorAddressType

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит тип адреса автора первая версия сообщения, то есть, сообщение перед пересылку и ответ.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W  <br/> |
|Идентификатор:  <br/> |0x0079  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Сервер  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства являются примерами свойства адреса для автора сообщения. В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение свойства **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)). Никогда не изменяется при сообщение будет переслано или ответ.
  
Исходные свойства author разрешить для хранения данных из других доменов обмена мгновенными сообщениями. При получении сообщения из другой домен обмена мгновенными сообщениями, например, из Интернета, эти свойства предусмотрена возможность убедитесь, что исходные данные не потеряны.
  
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

