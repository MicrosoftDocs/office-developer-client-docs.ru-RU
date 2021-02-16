---
title: Каноническое свойство PidTagScheduleInfoMonthsAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsAway
api_type:
- COM
ms.assetid: 282a8ba1-b786-4d17-b6c5-17e935e59a6b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 90df272a70fd4133a780f205c93b42f26ed1ae96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303411"
---
# <a name="pidtagscheduleinfomonthsaway-canonical-property"></a>Каноническое свойство PidTagScheduleInfoMonthsAway

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список месяцев, в течение которых в сообщении о занятости присутствуют сведения о занятости типа "нет на офисе" (OOF). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_MONTHS_OOF  <br/> |
|Идентификатор:  <br/> |0x6855  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Free/Busy  <br/> |
   
## <a name="remarks"></a>Примечания

Формат, вычисления и ограничения этого свойства такие же, как и формат **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative),](pidtagscheduleinfofreebusytentative-canonical-property.md)но ссылаются на встречи, помеченные как "нет на офисе" (OOF) в связанном объекте календаря.
  
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

