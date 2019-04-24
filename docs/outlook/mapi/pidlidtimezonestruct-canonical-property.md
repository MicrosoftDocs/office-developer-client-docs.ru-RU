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
  
Содержит поток, который сопоставляется с хранимым форматом структуры [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , который описывает часовой пояс, который будет использоваться для времени начала и окончания повторяющейся встречи или приглашения на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидтимезонеструкт  <br/> |
|Набор свойств:  <br/> |Псетид_аппоинтмент  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008233  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Комментарии

Microsoft Office Outlook 2003, более ранние версии Outlook и приложения, основанные на объектах данных совместной работы (CDO) 1,21, чьи пользователи не запускают средство обновления календаря, предоставленное в Outlook или Exchange Server, и время окончания повторяющееся время встречи или приглашения на собрание и сохраните часовой пояс, в котором создается приглашение на встречу или собрание в **диспидтимезонеструкт**. Тем не менее, эта схема игнорируется, так как правила для часовых поясов могут изменяться, что приводит к изменению некоторых встреч и собраний, которые пользователи запланировали до изменения правил и происходят в неправильное время. Пользователям и администраторам, не работающим под управлением Windows Vista или не включенных автоматических обновлений, следует использовать инструменты для изменения календарей, которые предоставляются в Outlook или Exchange Server для настройки времени таких встреч и приглашений на собрания. Дополнительные сведения об этих средствах и интерфейсах API для повторного создания календарей в статье сведения о возможностях [перехода на летнЕе время](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx) в календаре.
  
Используйте следующий формат с прямым порядком байтов при синтаксическом анализе потока, полученного из **диспидтимезонеструкт**, или при сохранении структуры **TZREG** в поток для фиксации в двоичном свойстве **диспидтимезонеструкт** . 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Это свойство устанавливается в повторяющихся рядах для указания сведений о часовом поясе, а также указывает способ преобразования полей времени между местным временем и всеобщим скоординированным временем (UTC).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

