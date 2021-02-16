---
title: Каноническое свойство PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345355"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Каноническое свойство PidLidAppointmentTimeZoneDefinitionRecur

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который сополагается с постоянным форматом структуры [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) в котором хранится описание часового пояса, используемого при составлении повторяющейся встречи или запроса на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptTZDefRecur  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008260  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Версии Microsoft Outlook с Microsoft Office Outlook 2007 г., а также решения на основе объектов данных совместной работы (CDO) 1.2.1, которые запускали средство обновления календаря Outlook или Exchange Server, используют свойства **dispidApptTZDefRecur** и **dispidTimeZoneStruct** [(PidLidTimeZoneStruct),](pidlidtimezonestruct-canonical-property.md)чтобы определить, следует ли корректировать повторяющееся собрание при изменении правил часового пояса. Эти свойства необходимо синхронизировать, так как старые клиенты по-прежнему могут управлять **свойством dispidTimeZoneStruct.** Чтобы определить, синхронизируются ли два свойства, член **wFlags** для правила, которое соответствует **dispidTimeZoneStruct,** должен иметь TZRULE_FLAG_RECUR_CURRENT_TZREG флага. Если этот флаг не установлен или установлен, а правило в свойстве **dispidTimeZoneStruct** не соответствует помеченным правилу, следует отменить свойство **dispidApptTZDefRecur,** а вместо него использовать **dispidTimeZoneStruct.** 
  
При записи свойств **dispidApptTZDefRecur** и **dispidTimeZoneStruct** в новое повторяющееся собрание или при произвольном выборе использования свойства **dispidTimeZoneStruct** необходимо использовать текущее определение часового пояса (в соответствии с реестром Windows). 
  
Разбор должен быть осторожным при считывате потоке, полученном от **dispidApptTZDefRecur,** или при сохраняемом **TZDEFINITION** в потоке для обязательства перед двоичным свойством, таким как **dispidApptTZDefRecur.** Дополнительные сведения см. в [разделах о том, как сохранить TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)в потоке для фиксации двоичного свойства.
  
 **dispidApptTZDefRecur** указывает сведения о часовом поясе, который описывает преобразование даты и времени собрания в повторяющийся ряд в UTC и из него. Если это свойство установлено, но имеет данные, несогласованные с данными, представленными **dispidTimeZoneStruct,** клиент должен использовать **dispidTimeZoneStruct** вместо **dispidApptTZDefRecur.** Если **dispidApptTZDefRecur** не установлен, будет использоваться свойство **PidLidTimeZoneStruct.** Поля в этом BLOB-проекте кодируются в порядок с небольшими конечнымибами. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

