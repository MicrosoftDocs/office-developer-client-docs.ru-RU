---
title: Каноническое свойство PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321324"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Каноническое свойство PidTagScheduleInfoAppointmentTombstone

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список блоков данных, которые представляют собрания, которые были отклонены.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Идентификатор:  <br/> |0x686A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Free/Busy  <br/> |
   
## <a name="remarks"></a>Примечания

Блоки данных начинаются с загона 32-битных значений, определенных как:
  
|**Значение**|**Описание**|
|:-----|:-----|
|Идентификатор  <br/> |Это поле должно быть значением 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |Это поле должно иметь значение 0x00000014.  <br/> |
|Версия  <br/> |Это поле должно иметь значение 3.  <br/> |
|RecordsCount  <br/> |Количество записей, которые следуют за ними.  <br/> |
|RecordsSize  <br/> |Это поле должно иметь значение 0x00000014.  <br/> |
   
За ним следуют записи **RecordsCount** 32-битных значений, определенные как: 
  
|**Значение**|**Описание**|
|:-----|:-----|
|StartTime  <br/> |Время начала объекта собрания в минутах с полуночи 1 января 1601 г. в UTC.  <br/> |
|EndTime  <br/> |Время окончания объекта собрания в минутах с полуночи 1 января 1601 г. в UTC.  <br/> |
|GlobalObjectIdSize  <br/> |Размер поля GlobalObjectId (в bytes).  <br/> |
|GlobalObjectId  <br/> |Значение свойства **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId)](pidlidglobalobjectid-canonical-property.md)собрания, представляемого этой записью.  <br/> |
|UserName  <br/> |Первые два bytes — это длина строки PT_STRING8, которая следует.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

