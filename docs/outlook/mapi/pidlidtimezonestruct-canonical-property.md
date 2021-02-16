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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который сопоствует сохраняемому формату структуры [TZREG,](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) который описывает часовой пояс, используемый для времени начала и окончания повторяющейся встречи или собрания. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTimeZoneStruct  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008233  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Microsoft Office Outlook 2003, более ранние версии Outlook и приложения, основанные на объектах данных совместной работы (CDO) 1.21, пользователи которых не запускали средство обновления календаря, предоставленное Outlook или Exchange Server, сохраняют время начала и окончания повторяющейся встречи или собрания в качестве относительного времени и сохраняют часовой пояс, в котором создается встреча или собрание, в **dispidTimeZoneStruct.** Однако эта схема игнорирует, что со временем правила часовой пояс могут изменяться, что приводит к изменению некоторых встреч и собраний, запланированных пользователями до изменения правил и их некорректного проведения. Пользователи и администраторы, не работающие под управлением Windows Vista или не включившие автоматические обновления, должны использовать средства повторного запуска календаря, предоставляемые Outlook или Exchange Server, для настройки времени таких встреч и запросов на собрания. Дополнительные сведения об этих средствах и API для повторного изменения календарей см. в подпрограммном перезапись календарей для [летнего времени](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Используйте следующий небольшой конечный формат при разчете потока, полученного из **dispidTimeZoneStruct,** или при сохраняемой структуре **TZREG** в потоке для фиксации двоичного свойства **dispidTimeZoneStruct.** 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Это свойство задано в повторяющихся рядах, чтобы указать сведения о часовом поясе, и указывает, как преобразовывать поля времени между локальным временем и универсальным координируемым временем (UTC).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.
    
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

