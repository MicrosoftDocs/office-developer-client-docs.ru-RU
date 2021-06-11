---
title: Каноническое свойство PidLidRecurrencePattern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrencePattern
api_type:
- COM
ms.assetid: ac21ba98-f16b-4365-9134-bca7748189ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d94ac430df54fc03d96ac761c53ca20201d899c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315934"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a>Каноническое свойство PidLidRecurrencePattern

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает описание шаблона повторения объекта календаря.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidRecurPattern  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008232  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство задано, оно должно быть задано в описании повторения, указанного свойством **dispidApptRecur** [(PidLidAppointmentRecur).](pidlidappointmentrecur-canonical-property.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

