---
title: PidTagScheduleInfoMonthsTentative Canonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359761"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>PidTagScheduleInfoMonthsTentative Canonical Property

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит месяцы, отмеченные предварительно в свободном/загруженном сообщении.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Идентификатор:  <br/> |0x6851  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Бесплатный/занятый  <br/> |
   
## <a name="remarks"></a>Примечания

Количество значений в этом свойстве должно быть от нуля до количества месяцев, охватываемых диапазоном публикации, который является периодом между свойствами **PR_FREEBUSY_PUBLISH_START** [(PidTagFreeBusyPublishStart)](pidtagfreebusypublishstart-canonical-property.md)и **PR_FREEBUSY_PUBLISH_END** [(PidTagFreeBusyPublishEnd).](pidtagfreebusypublishend-canonical-property.md)
  
Каждое значение в этом свойстве кодирует месяц и год. Это рассчитывается с помощью выражения "год × 16 + месяц", в котором год и месяц основаны на григорианском календаре. Значения сортируются в порядке восходящей и закодируются в формате little-endian. Если событие распространяется на несколько месяцев или несколько лет, для каждого из месяцев, которые попадают в диапазон публикации, должно быть одно значение. Если в диапазоне публикаций нет предварительных **событий,** то это свойство и PR_SCHDINFO_FREEBUSY_TENTATIVE [(PidTagScheduleInfoFreeBusyTentative)](pidtagscheduleinfofreebusytentative-canonical-property.md)не должны быть заданы или должны быть удалены, если они уже существуют. В противном случае необходимо установить это свойство.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
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

