---
title: Каноническое свойство PidTagScheduleInfoFreeBusyAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyAway
api_type:
- COM
ms.assetid: 7b5d013a-15ac-469a-98c8-3ed1e80f6faf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3535e8969ceff975077285aed89f979c24821bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811843"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a>Каноническое свойство PidTagScheduleInfoFreeBusyAway

  
  
**Относится к**: Outlook 
  
Содержит время, для которых имеет значение состояния занятости об отсутствии на работе.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_FREEBUSY_OOF  <br/> |
|Идентификатор:  <br/> |0x6856  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Обмен сведениями о доступности  <br/> |
   
## <a name="remarks"></a>Замечания

Формат, вычисление и ограничения этого свойства — это отличается от **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как об отсутствии на работе в связанной календаре.
  
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

