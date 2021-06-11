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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который совмещая сохраняемого формата структуры [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) в котором хранится описание часового пояса, используемого при повторном назначении или запросе на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptTZDefRecur  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008260  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Версии Microsoft Outlook с Microsoft Office Outlook 2007 г. и решения на основе объектов данных совместной работы (CDO) 1.2.1, которые запускали средство обновления Outlook или Exchange Server календаря, используют **dispidApptTZDefRecur** и **dispidTimeZoneStruct** [(PidLidTimeZoneStruct),](pidlidtimezonestruct-canonical-property.md)чтобы определить, следует ли корректировать повторяющиеся собрания, если правила часового пояса изменятся. Эти свойства необходимо синхронизировать, так как более старые клиенты по-прежнему могут манипулировать **свойством dispidTimeZoneStruct.** Чтобы определить, синхронизированы ли эти два свойства, участник **wFlags** для правила, которое совпадает с **dispidTimeZoneStruct,** должен иметь TZRULE_FLAG_RECUR_CURRENT_TZREG флага. Если этот флаг не установлен или установлен, а правило в свойстве dispidTimeZoneStruct не совпадает с отмеченным правилом, свойство **dispidApptTZDefRecur** должно быть отброшено и вместо него следует использовать **dispidTimeZoneStruct.**  
  
При записи свойств **dispidApptTZDefRecur** и **dispidTimeZoneStruct** на новое повторяющееся собрание или при произвольном выборе использования свойства **dispidTimeZoneStruct** необходимо использовать текущее определение часового пояса (согласно реестру Windows). 
  
Разборщик должен быть осторожным, когда он читает поток, полученный из **dispidApptTZDefRecur**, или когда он **сохраняется TZDEFINITION** в поток для обязательств к двоичному свойству, например **dispidApptTZDefRecur**. Дополнительные сведения см. в разделах О сохраняющихся [TZDEFINITION](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx)в потоке для фиксации двоичного свойства.
  
 **dispidApptTZDefRecur** указывает сведения часового пояса, описывающие, как преобразовать дату и время собрания в повторяющейся серии в скоординированное универсальное время (UTC) и из него. Если это свойство заданной, но оно имеет данные, несовместимые с данными, представленными **dispidTimeZoneStruct,** клиент должен использовать **dispidTimeZoneStruct** вместо **dispidApptTZDefRecur**. Если **не установлено dispidApptTZDefRecur,** вместо этого будет использоваться свойство **PidLidTimeZoneStruct.** Поля в этом BLOB закодированы в порядке мало-endian byte. 
  
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

