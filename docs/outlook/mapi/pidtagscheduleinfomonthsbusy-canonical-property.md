---
title: Каноническое свойство PidTagScheduleInfoMonthsBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b15447d6-89aa-40ad-93fc-21fbfa5e3d0e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 293e8648374b61784f5bda0db124506f345b2701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811859"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a>Каноническое свойство PidTagScheduleInfoMonthsBusy

  
  
**Относится к**: Outlook 
  
Содержит месяцев, для которых в сообщении о доступности данных о доступности типа «занят».
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_MONTHS_BUSY  <br/> |
|Идентификатор:  <br/> |0x6853  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Обмен сведениями о доступности  <br/> |
   
## <a name="remarks"></a>Замечания

Формат, вычисление и ограничения этого свойства — это отличается от **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), но обращайтесь к встречи, которые помечены как «занят» на объекте связанного календаря.
  
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

