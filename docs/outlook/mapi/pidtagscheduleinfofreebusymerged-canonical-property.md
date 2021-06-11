---
title: Каноническое свойство PidTagScheduleInfoFreeBusyMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338719"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a>Каноническое свойство PidTagScheduleInfoFreeBusyMerged

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит время, в течение которого задарен статус свободного или занятого.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_FREEBUSY_MERGED  <br/> |
|Идентификатор:  <br/> |0x6850  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Бесплатный/занятый  <br/> |
   
## <a name="remarks"></a>Примечания

События предварительного типа free/busy не включаются в это свойство. Формат, вычисления и ограничения этого свойства такие же, как и у **PR_SCHDINFO_FREEBUSY_TENTATIVE** [(PidTagScheduleInfoFreeBusyTentative),](pidtagscheduleinfofreebusytentative-canonical-property.md)но ссылаются на встречи, отмеченные OOF или занятые в связанном календаре.
  
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

