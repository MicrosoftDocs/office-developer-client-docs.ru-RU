---
title: Каноническое свойство PidTagScheduleInfoMonthsMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsMerged
api_type:
- COM
ms.assetid: b13b5d7b-413e-4405-8a35-0422477a9e86
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 53bc27b4ddd05b4a52328c605a6d4f673c91afd2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383823"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>Каноническое свойство PidTagScheduleInfoMonthsMerged

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список месяцев для данных о доступности типа «занят» или об отсутствии на работе (OOF) сообщения в сообщении о доступности. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|Идентификатор:  <br/> |0x684F  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Обмен сведениями о доступности  <br/> |
   
## <a name="remarks"></a>Замечания

События сведений о доступности типа под вопросом не включаются в это свойство. Синтаксис/формат и ограничения этого свойства — это то же самое, что и **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как об отсутствии на работе» или «занят на объекте связанного календаря. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
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

