---
title: Каноническое свойство PidTagScheduleInfoFreeBusyBusyBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4fbf0d8b80fdb48e44480b2739a71aec43b88a05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338656"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a>Каноническое свойство PidTagScheduleInfoFreeBusyBusyBusy

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит блоки времени, на которое занят состояние.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_FREEBUSY_BUSY  <br/> |
|Идентификатор:  <br/> |0x6854  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Бесплатный/занятый  <br/> |
   
## <a name="remarks"></a>Примечания

Формат, вычисления и ограничения этого свойства такие **же,** как и у PR_SCHDINFO_FREEBUSY_TENTATIVE [(PidTagScheduleInfoFreeBusyTentative),](pidtagscheduleinfofreebusytentative-canonical-property.md)но ссылаются на встречи, отмеченные занятыми на связанном объекте календаря.
  
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

