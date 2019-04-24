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
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359761"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a>Каноническое свойство PidTagScheduleInfoMonthsTentative

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит месяцы, помеченные под вопросом в сообщении о занятости.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЧДИНФО_МОНСС_ТЕНТАТИВЕ  <br/> |
|Идентификатор:  <br/> |0x6851  <br/> |
|Тип данных:  <br/> |ПТ_МВ_ЛОНГ  <br/> |
|Область:  <br/> |Сведения о доступности  <br/> |
   
## <a name="remarks"></a>Примечания

Число значений в этом свойстве должно быть между нулем и числом месяцев, охваченных диапазоном публикации, который является периодом между **пр_фрибуси_публиш_старт** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) и **пр_фрибуси_публиш_енд **Свойства ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).
  
Каждое значение этого свойства содержит месяц и год, закодированный в нем. Он вычисляется с помощью выражения "Year × 16 + month", где год и месяц основываются на григорианском календаре. Значения сортируются в возрастающем порядке и кодируются в формате с прямым порядком байтов. Если событие распространяется в течение нескольких месяцев или несколько лет, для каждого из месяцев, которые попадают в диапазон публикации, должно быть по одному значению. Если в диапазоне публикации нет предварительных событий, то это свойство и **пр_счдинфо_фрибуси_тентативе** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) не должны быть заданы или должны быть удалены, если они уже существуют. В противном случае необходимо задать значение этого свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОПФФБ]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Публикует доступность пользователя или ресурса.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

