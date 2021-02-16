---
title: Каноническое свойство PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359777"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>Каноническое свойство PidTagScheduleInfoFreeBusyTentative

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит блоки времени, для которого состояние занятости является под вопросом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Идентификатор:  <br/> |0x6852  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Free/Busy  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство имеет столько же значений, сколько и число значений в **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative).](pidtagscheduleinfomonthstentative-canonical-property.md) Каждое двоичное значение представляет месяц и соответствует значению в одном индексе **PR_SCHDINFO_MONTHS_TENTATIVE.** Двоичные значения сортироваться в том же порядке, что и значения в **PR_SCHDINFO_MONTHS_TENTATIVE.**
  
Каждое двоичное значение имеет один или несколько блоков 4 BYTE, каждый из которых содержит время начала в первых двухбайтах, а время окончания во втором — в мало endian формате. Время начала — это количество минут между полночью (UTC) первого дня месяца и временем начала события в UTC. Время окончания — это количество минут между полуночью в UTC первого дня месяца и временем окончания события в UTC. 4-BYTE-блоки сортироваться в порядке возрастания.
  
Последовательные или перекрывающиеся блоки времени объединяются в один блок с временем начала в качестве времени начала первого блока и временем окончания последнего блока. Если событие распространяется на несколько месяцев или лет, событие делится на несколько блоков, по одному на каждый месяц. Если в диапазоне публикации нет предварительных событий,  это свойство и PR_SCHDINFO_MONTHS_TENTATIVE не должны быть заданы или должны быть удалены, если они уже существуют. В противном случае необходимо установить это свойство. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Публикует доступность пользователя или ресурса.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

