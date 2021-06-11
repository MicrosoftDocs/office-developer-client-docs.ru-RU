---
title: PidTagScheduleInfoMonthsMerged Canonical Property
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336479"
---
# <a name="pidtagscheduleinfomonthsmerged-canonical-property"></a>PidTagScheduleInfoMonthsMerged Canonical Property

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список месяцев, в течение которых в свободном/загруженном сообщении присутствуют бесплатные/загруженные данные типа занятого или неподъемного (OOF) сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_MONTHS_MERGED  <br/> |
|Идентификатор:  <br/> |0x684F  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Бесплатный/занятый  <br/> |
   
## <a name="remarks"></a>Примечания

События предварительного типа free/busy не включаются в это свойство. Синтаксис/формат и ограничения этого свойства такие же, как и у **PR_SCHDINFO_MONTHS_TENTATIVE** [(PidTagScheduleInfoMonthsTentative),](pidtagscheduleinfomonthstentative-canonical-property.md)но ссылаются на встречи, отмеченные OOF или Busy на связанном объекте календаря. 
  
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

