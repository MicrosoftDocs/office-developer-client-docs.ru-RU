---
title: Каноническое свойство PidTagOriginatorRequestedAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorRequestedAlternateRecipient
api_type:
- COM
ms.assetid: c85b7862-18bc-4e17-94db-9097e0ac4a02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 463f2eb6e730c9250861ce50515a7f662bb75d23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588869"
---
# <a name="pidtagoriginatorrequestedalternaterecipient-canonical-property"></a>Каноническое свойство PidTagOriginatorRequestedAlternateRecipient

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи альтернативного получателя, обозначенного отправителя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT  <br/> |
|Идентификатор:  <br/> |0x0C09  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется в сообщениях, автоматически переадресовано. Если не разрешается autoforwarding или обозначенный альтернативного получатели, будет создан отчет о недоставке.
  
## <a name="related-resources"></a>Связанные ресурсы

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

