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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389304"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a>Каноническое свойство PidLidAppointmentTimeZoneDefinitionRecur

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который соответствует сохраненного формата [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) структуры, который хранит описание часовой пояс, который используется при создании повторяющейся встречи или приглашения на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptTZDefRecur  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008260  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Используйте средство **dispidApptTZDefRecur** и **обновление для систем Microsoft Outlook, начиная с Microsoft Office Outlook 2007 и решения, основанные на объекты совместной работы (CDO) 1.2.1 (en), ранее выполненные календаря Outlook или Exchange Server dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) свойства, чтобы определить, должны быть настроены повторяющееся собрание, при изменении правила часового пояса. Эти свойства должны быть синхронизированы, так как старых клиентов по-прежнему могут изменить значение свойства **dispidTimeZoneStruct** . Для обнаружения синхронизированных два свойства члена **wFlags** для правила, которая соответствует **dispidTimeZoneStruct** наличие флаг TZRULE_FLAG_RECUR_CURRENT_TZREG. Если этот флаг не установлен, или оно установлено и правила в свойстве **dispidTimeZoneStruct** не соответствует помеченные правило, не следует использовать свойство **dispidApptTZDefRecur** и **dispidTimeZoneStruct** следует использовать вместо этого. 
  
При создании свойства **dispidApptTZDefRecur** и **dispidTimeZoneStruct** новое повторяющееся собрание, или, если сделать произвольный выбор с помощью свойства **dispidTimeZoneStruct** текущего определения часового пояса ( в соответствии с реестра Windows) следует использовать. 
  
Средство синтаксического анализа необходимо следить за тем, при считывании поток, полученную из **dispidApptTZDefRecur**или для сохранения **TZDEFINITION** поток для, направленных на двоичного свойства, такие как **dispidApptTZDefRecur**. Для получения дополнительных сведений см [Сохранение TZDEFINITION поток, чтобы зафиксировать двоичного свойства](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefRecur** указывает сведения часового пояса, описывающая способ преобразования собрания даты и времени на серии повторяющихся и в формате UTC. Если задано это свойство, но он содержит данные, не соответствует данных, представленному **dispidTimeZoneStruct**, клиент должен использовать **dispidTimeZoneStruct** вместо **dispidApptTZDefRecur**. Если **dispidApptTZDefRecur** не задано, будет использоваться свойство **PidLidTimeZoneStruct** . Поля в этом больших двоичных ОБЪЕКТОВ, помеченные в байтовом формате с прямым. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
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

