---
title: Каноническое свойство PidLidTimeZoneStruct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346377"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Каноническое свойство PidLidTimeZoneStruct

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который описывает сохраняющийся формат структуры [TZREG,](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) в котором описывается часовой пояс, который будет использоваться для начала и окончания времени повторяющегося запроса на встречу или встречи. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTimeZoneStruct  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008233  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Microsoft Office Outlook 2003 г. более ранние версии Outlook и приложения, основанные на объектах данных совместной работы (CDO) 1.21, пользователи которых не запускали средство обновления календаря, предоставляемого Outlook или Exchange Server, хранят время начала и окончания повторяющегося встречи или собрания в относительное время, а также сохраняют часовой пояс, в котором запрос на встречу или собрание создается в **dispidTimeZoneStruct**. Однако в этой схеме игнорируется, что со временем правила часовой зоны могут изменяться, что приводит к некоторым встречам и собраниям, запланированным пользователями до того, как правила изменились и происходят в неправильное время. Пользователи и администраторы, которые не работают Windows Vista или не имеют автоматических обновлений, должны использовать средства для повторного использования календаря, предоставляемые Outlook или Exchange Server, чтобы изменить время таких встреч и запросов на собрания. Дополнительные сведения об этих средствах для повторного анализа календарей и API, которые перезамещеют календари, см. в разделЕ О том, как программным образом ребазировать календари для [летнего времени.](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Используйте следующий малоэтапный формат при размыве потока, полученного из **dispidTimeZoneStruct,** или при сохраняющихся **структурах TZREG** в потоке для фиксации двоичного свойства **dispidTimeZoneStruct.** 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Это свойство задано в повторяющейся серии для указания сведений о часовом поясе и указывает, как преобразовать поля времени между локальным временем и согласованным универсальным временем (UTC).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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

