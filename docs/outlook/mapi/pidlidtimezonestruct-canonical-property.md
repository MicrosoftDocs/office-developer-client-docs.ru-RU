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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401617"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Каноническое свойство PidLidTimeZoneStruct

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который соответствует сохраненного формата структуры [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , который описывает часовой пояс, который будет использоваться для времени начала и окончания повторяющейся встречи или приглашения на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTimeZoneStruct  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008233  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Microsoft Office Outlook 2003 более ранних версий Outlook и приложения, основанные на объекты совместной работы (CDO) 1.21, пользователи не запущен средства обновления календаря, реализованного в Outlook или Exchange Server хранить время начала и время окончания повторяющиеся встречи или приглашения на собрание как относительное время и сохранить часовой пояс, в котором создается встречи или приглашения на собрание в **dispidTimeZoneStruct**. Тем не менее эта схема игнорирует, что со временем часового пояса правил можно изменить, в результате чего некоторые встречи и собрания, которое пользователи, назначенные перед правила изменено и появляться в неправильные время. Пользователям и администраторам которых не установлена ОС Windows Vista или пользователей, которые не имеют включено автоматическое обновление следует использовать календарь, повторного размещения en средств, предоставляемых Outlook или Exchange Server, чтобы настроить время таких встречи и приглашения на собрания. Дополнительные сведения об этих средств сдвига календаря и API, которые перебазирование календарей в разделе [о сдвига календарей программными средствами на летнее время](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Используйте следующий формат обратным при анализе потока, полученный из **dispidTimeZoneStruct**или при сохранении в структуре **TZREG** для потока, чтобы зафиксировать двоичного свойства **dispidTimeZoneStruct** . 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Это свойство имеет значение на серии повторяющихся указать часовой пояс сведения и указывает, как преобразовать поля времени между местного времени и времени в формате UTC.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

