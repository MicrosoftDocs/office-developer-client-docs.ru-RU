---
title: Каноническое свойство PidTagScheduleInfoDisallowRecurringAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391082"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a>Каноническое свойство PidTagScheduleInfoDisallowRecurringAppts

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, когда отклонить автоматического ответа для повторяющихся встреч.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_DISALLOW_RECURRING_APPTS  <br/> |
|Идентификатор:  <br/> |0x686E  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Обмен сведениями о доступности  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство применяется только в случае, когда значение свойства **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) имеет значение TRUE. Отсутствие этого свойства указывает, что будет принято повторяющиеся собрания. Это не обязательное свойство.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Публикует доступности пользователя или ресурса.
    
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

