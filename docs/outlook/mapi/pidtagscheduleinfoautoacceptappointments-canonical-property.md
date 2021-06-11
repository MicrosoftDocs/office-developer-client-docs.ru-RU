---
title: Каноническое свойство PidTagScheduleInfoAutoAcceptAppointments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330095"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a>Каноническое свойство PidTagScheduleInfoAutoAcceptAppointments

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если клиент или сервер должны автоматически отвечать на все запросы собрания для участника или ресурса.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_AUTO_ACCEPT_APPTS  <br/> |
|Идентификатор:  <br/> |0x686D  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Бесплатный/занятый  <br/> |
   
## <a name="remarks"></a>Примечания

При ответе ответ должен быть принятым, если для дополнительного  ограничения, указанного свойствами [PR_SCHDINFO_DISALLOW_RECURRING_APPTS (PidTagScheduleInfoDisallowRecurringAppts)](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)или **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** [(Свойства PidTagScheduleInfoDisallowOverlappingAppts).](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md) Значение FALSE или отсутствие этого свойства указывает на то, что клиент или сервер не должны автоматически принимать запросы на собрание. Это свойство не обязательно.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Публикует доступность пользователя или ресурса.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

