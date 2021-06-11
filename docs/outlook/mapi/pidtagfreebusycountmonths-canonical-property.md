---
title: Каноническое свойство PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316193"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a>Каноническое свойство PidTagFreeBusyCountMonths

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение для вычисления дат начала и окончания диапазона бесплатных и загруженных данных, которые будут опубликованы в общедоступных папках.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FREEBUSY_COUNT_MONTHS  <br/> |
|Идентификатор:  <br/> |0x6869  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Передаваемое сообщение с определенным классом сообщений  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этого свойства должно быть больше или равно 0 и меньше или равно 36. Это свойство не обязательно.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Публикует доступность пользователя или ресурса.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.
    
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

