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
ms.openlocfilehash: 37a6d101f6ee9c04236253e143aff3a51a9208d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811837"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Каноническое свойство PidTagScheduleInfoAppointmentTombstone

  
  
**Относится к**: Outlook 
  
Содержит список блоков данных, которые представляют собрания, которые было отклонено.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Идентификатор:  <br/> |0x686A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Обмен сведениями о доступности  <br/> |
   
## <a name="remarks"></a>Замечания

Блоки данных начинаются с заголовком 32-разрядная версия значения, определенные как:
  
|**Значение**|**Описание**|
|:-----|:-----|
|Идентификатор  <br/> |В этом поле должно быть значение 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |В этом поле должно иметь значение 0x00000014.  <br/> |
|Версия  <br/> |В этом поле должно иметь значение 3.  <br/> |
|RecordsCount  <br/> |Количество записей, выполните.  <br/> |
|RecordsSize  <br/> |В этом поле должно иметь значение 0x00000014.  <br/> |
   
Заголовок следуют записи **RecordsCount** значений 32-разрядная версия, определенного как: 
  
|**Значение**|**Описание**|
|:-----|:-----|
|StartTime  <br/> |Время начала собрания объекта в минут, начиная с полуночи 1 января 1601 UTC.  <br/> |
|EndTime  <br/> |Время окончания собрания объекта в минут, начиная с полуночи 1 января 1601 UTC.  <br/> |
|GlobalObjectIdSize  <br/> |Размер в байтах, поля GlobalObjectId.  <br/> |
|GlobalObjectId  <br/> |Представляет значение свойства **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) данная запись собрания.  <br/> |
|Имя пользователя  <br/> |Первые два байта являются длина строки PT_STRING8, исходя из.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

