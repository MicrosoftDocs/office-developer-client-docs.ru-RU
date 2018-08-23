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
ms.openlocfilehash: b943f9a3b6f63f185a1b44cfa811d010a287a3d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565818"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a>Каноническое свойство PidTagScheduleInfoFreeBusyTentative

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит блоки времени, для которых состояние доступности под вопросом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Идентификатор:  <br/> |0x6852  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Обмен сведениями о доступности  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство имеет любое количество значений количество значений в **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Каждый двоичное значение представляет месяц и соответствует значению с таким же индексом в **PR_SCHDINFO_MONTHS_TENTATIVE**. Двоичные значения сортируются в том же порядке, как значение в **PR_SCHDINFO_MONTHS_TENTATIVE**.
  
Каждый двоичное значение имеет один или несколько блоков 4-БАЙТНЫХ и каждый из них содержит время начала в первых двух байтах и время окончания в второй два байта в формате с прямым. Время начала — число минут между полночь по Гринвичу (UTC) первого дня недели, месяца и время начала события в формате UTC. Время окончания — это число минут между полночь по Гринвичу первого дня недели, месяца и время окончания события в формате UTC. 4-БАЙТНЫХ блоки сортируются в порядке возрастания.
  
Последовательные или перекрывающиеся блоки времени объединяются в один блок с время начала время начала первого блока и время окончания как время окончания последнего блока. Если событие распределить по несколько месяцев или лет, событие делится на несколько блоков, другая — для каждого месяца. Если нет под вопросом событий в диапазоне публикации, затем это свойство и **PR_SCHDINFO_MONTHS_TENTATIVE** не должен быть установлен или должен быть удален, если они существуют. В противном случае необходимо установить это свойство. 
  
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

