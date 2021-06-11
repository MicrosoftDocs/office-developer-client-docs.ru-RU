---
title: Каноническое свойство PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345019"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Каноническое свойство PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который сопополагает с упорным форматом структуры [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) в котором хранится описание часового пояса, используемого при выборе времени начала встречи или собрания одного экземпляра. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x0000825E  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Microsoft Office Outlook 2003 или более ранних лет и решения, основанные на объектах данных совместной работы (CDO) 1.2.1 и не запускаемом средстве обновления календаря для Outlook или Microsoft Exchange Server, сохраняют время начала и окончания встреч и запросов на собрания в координирующем универсальном времени (UTC). Эти клиенты не хранят сведения о часовом поясе, в котором создается запрос на встречу или собрание.
  
Версии Outlook с Microsoft Office Outlook 2007 г. и решения на основе CDO 1.2.1, которые запускали средство обновления Outlook или Exchange Server календаря, используют это свойство для хранения часового пояса для начала. Свойство **dispidApptTZDefStartDisplay** показывает встречу или встречу в исходном часовом поясе, которое было запланировано. Он определяет, следует ли корректировать время начала при изменении правил часового пояса. Если этого свойства не хватает, предполагается текущий локальный часовой пояс. Это свойство используется только для отображения и не используется в расширении повторяемости. 
  
Разборщик должен быть осторожным, когда он читает поток, полученный из этого свойства, или когда он **сохраняется TZDEFINITION** в поток для приверженности двоичному свойству, такому как **dispidApptTZDefStartDisplay**. Дополнительные сведения см. в разделах О сохраняющихся [TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)в потоке для фиксации двоичного свойства.
  
Это свойство указывает сведения о часовом поясе для свойства **dispidApptStartWhole** [(PidLidAppointmentStartWhole).](pidlidappointmentstartwhole-canonical-property.md) Значение **dispidApptTZDefStartDisplay** используется для преобразования даты начала и времени из UTC в локальный часовой пояс для отображения. Для каждого **TZRULE,** указанного этим свойством, флаг TZRULE_FLAG_RECUR_CURRENT_TZREG не должен быть задан. Например, если **TZRULE** является эффективным правилом, значение **поля, TZRULE** должно быть "0x0002"; в противном случае он должен быть "0x0000". 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы..
    
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

