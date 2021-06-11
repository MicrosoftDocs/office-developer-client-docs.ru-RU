---
title: Каноническое свойство PidTagScheduleInfoDisallowOverlappingAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330088"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a>Каноническое свойство PidTagScheduleInfoDisallowOverlappingAppts

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если перекрывающиеся встречи будут отсеяно.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS  <br/> |
|Идентификатор:  <br/> |0x686F  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Бесплатный/занятый  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство имеет значение только тогда, когда **значение свойства PR_SCHDINFO_AUTO_ACCEPT_APPTS** [(PidTagScheduleInfoAutoAcceptAppointments)](pidtagscheduleinfoautoacceptappointments-canonical-property.md)является TRUE. Значение TRUE указывает, что при автоматическом ответе на запросы собраний клиент или сервер должны отклонуть экземпляры, перекрывающие ранее запланированные события. Значение FALSE или отсутствие этого свойства указывает на то, что дублирующие экземпляры должны быть приняты. Это свойство не обязательно.
  
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

