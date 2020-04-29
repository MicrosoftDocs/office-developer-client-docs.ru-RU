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
  
Содержит блоки времени, для которых состояние занятости — под вопросом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_FREEBUSY_TENTATIVE  <br/> |
|Идентификатор:  <br/> |0x6852  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Сведения о доступности  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этого свойства не может быть больше числа значений в **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)). Каждое двоичное значение соответствует месяцу и соответствует значению в том же индексе в **PR_SCHDINFO_MONTHS_TENTATIVE**. Двоичные значения сортируются в том же порядке, что и значения в **PR_SCHDINFO_MONTHS_TENTATIVE**.
  
Каждое двоичное значение содержит один или несколько блоков размером 4 БАЙТа, и каждый из них содержит время начала в первых двух байтах и время окончания в двух секундах в формате с прямым порядком байтов. Время начала — это количество минут между временем в формате UTC первого дня месяца и временем начала события в формате UTC. Время окончания — это количество минут между полуночым UTC первого дня месяца и временем окончания события в формате UTC. 4 БАЙТовых блока сортируются в порядке возрастания.
  
Последовательные или перекрывающиеся блоки времени объединяются в один блок с временем начала, как время начала первого блока и время окончания последнего блока. Если событие распространяется в течение нескольких месяцев или лет, оно разбивается на несколько блоков, по одному на каждый месяц. Если в диапазоне публикации нет предварительных событий, то это свойство и **PR_SCHDINFO_MONTHS_TENTATIVE** не должны быть заданы или должны быть удалены, если они уже существуют. В противном случае необходимо задать значение этого свойства. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОПФФБ]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Публикует доступность пользователя или ресурса.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

