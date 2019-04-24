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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список блоков данных, представляющих отклоненные собрания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЧДИНФО_АППТ_ТОМБСТОНЕ  <br/> |
|Идентификатор:  <br/> |0x686A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Сведения о доступности  <br/> |
   
## <a name="remarks"></a>Замечания

Блоки данных начинаются с заголовка 32 битовых значений, заданных как:
  
|**Value**|**Описание**|
|:-----|:-----|
|Идентификатор  <br/> |Это поле должно быть значением 0xBEDEAFCD.  <br/> |
|Хеадерсизе  <br/> |Это поле должно иметь значение 0x00000014.  <br/> |
|Версия  <br/> |Это поле должно иметь значение 3.  <br/> |
|Рекордскаунт  <br/> |Количество последующих записей.  <br/> |
|Рекордссизе  <br/> |Это поле должно иметь значение 0x00000014.  <br/> |
   
За заголовком следуют записи **рекордскаунт** со значениями 32 бит, определенные как: 
  
|**Value**|**Описание**|
|:-----|:-----|
|StartTime  <br/> |Время начала объекта собрания (в минутах), начиная с полуночи 1 января 1601,, UTC.  <br/> |
|EndTime  <br/> |Время окончания объекта собрания (в минутах), начиная с полуночи 1 января 1601,, UTC.  <br/> |
|Глобалобжектидсизе  <br/> |Размер (в байтах) поля Глобалобжектид.  <br/> |
|Глобалобжектид  <br/> |Значение свойства **лид_глобал_обжид** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) собрания, представляющего эту запись.  <br/> |
|UserName  <br/> |Первые два байта — это длина строки PT_STRING8, приведенной ниже.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

