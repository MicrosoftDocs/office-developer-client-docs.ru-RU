---
title: Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345383"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который сопополагает с упорным форматом структуры [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) в котором хранится описание часового пояса, используемого при выборе конечного времени назначения или собрания одного экземпляра. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x0000825F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Microsoft Office Outlook 2003 или более ранних лет и решения, основанные на объектах данных совместной работы (CDO) 1.2.1 и не запускаемом средстве обновления календаря для Outlook или Microsoft Exchange Server, сохраняют время начала и окончания встреч и запросов на собрания в координирующем универсальном времени (UTC). Эти клиенты не хранят информацию о часовом поясе, в котором создается запрос на встречу или встречу.
  
Версии Microsoft Outlook с Microsoft Office Outlook 2007 г., а решения на основе CDO 1.2.1, которые запускали средство обновления Outlook или Exchange Server календаря, используют **dispidApptTZDefEndDisplay** для хранения часового пояса в течение конечного времени. **dispidApptTZDefEndDisplay** показывает встречу или собрание в исходном часовом поясе, которое было запланировано, и определяет, следует ли корректировать конечное время при изменении правил часового пояса. Если этого свойства не хватает, используется часовой пояс, указанный **свойством dispidApptTZDefStartDisplay** [(PidLidAppointmentTimeZoneDefinitionStartDisplay).](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md) Если **dispidApptTZDefStartDisplay** отсутствует или недействительна, предполагается текущий локальный часовой пояс. **dispidApptTZDefEndDisplay** используется только для отображения и не используется при расширении повторяемости. 
  
Разборщик должен быть осторожным, когда он читает поток, полученный из **dispidApptTZDefEndDisplay**, или когда он **сохраняется TZDEFINITION** в поток для приверженности двоичному свойству, такому как **dispidApptTZDefEndDisplay**. Дополнительные сведения см. в разделах О сохраняющихся [TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)в потоке для фиксации двоичного свойства.
  
 **dispidApptTZDefEndDisplay** указывает сведения о часовом поясе для свойства **dispidApptEndWhole** [(PidLidAppointmentEndWhole).](pidlidappointmentendwhole-canonical-property.md) Формат, ограничения и вычисления **dispidApptTZDefEndDisplay** те же, что и в свойстве **dispidApptTZDefStartDisplay.** 
  
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

