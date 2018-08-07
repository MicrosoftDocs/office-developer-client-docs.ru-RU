---
title: Каноническое свойство PidTagRecipientProposedStartTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 65d5c2f94da219fc1cb87384ebdd3c1cf34bd9a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811664"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a>Каноническое свойство PidTagRecipientProposedStartTime

  
  
**Относится к**: Outlook 
  
Указывает, предлагаемое время начала собрания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_PROPOSEDSTARTTIME  <br/> |
|Идентификатор:  <br/> |0x5FE3  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Получатель транспорта  <br/> |
   
## <a name="remarks"></a>Замечания

Если значение свойства **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) задано значение TRUE, значение этого свойства указывает значение затребованы участника, чтобы установить в качестве значения **dispidApptStartWhole** ([ PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) свойства для одного экземпляра собрания или объект исключения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
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

