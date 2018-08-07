---
title: Каноническое свойство PidTagScheduleInfoMonthsTentative
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
ms.openlocfilehash: 20620a5835e627eb7543a03037f9be75db6739ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811854"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Каноническое свойство PidTagScheduleInfoMonthsTentative

  
  
**Относится к**: Outlook 
  
Содержит месяцев, помеченные под вопросом в сообщении о доступности.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_MONTHS_TENTATIVE  <br/> |
|Идентификатор:  <br/> |0x6851  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Обмен сведениями о доступности  <br/> |
   
## <a name="remarks"></a>Замечания

Число значений в это свойство должно быть между 0 и число месяцев, к которому применяется публикации интервал, заданный период между **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) и **PR_FREEBUSY_PUBLISH_END **Свойства ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).
  
Каждое значение этого свойства имеет месяц и год, закодированный в нем. Это именно рассчитывается, используя выражение «году × 16 + месяц» где года, месяца на основе григорианский календарь. Значения сортируются в порядке возрастания и кодируются в формате с прямым. Если событие распространено на несколько месяцев или нескольких лет должно быть одно значение для каждого месяца, которые лежат в диапазоне от публикации. Если нет под вопросом событий в диапазоне публикации, затем это свойство и **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) не должен быть установлен или должен быть удален, если они существуют. В противном случае необходимо установить это свойство.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
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

