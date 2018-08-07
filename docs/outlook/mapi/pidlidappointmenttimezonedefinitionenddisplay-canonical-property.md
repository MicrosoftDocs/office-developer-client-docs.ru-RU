---
title: Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 119cd7edc5b9b615a39cea6aa1c405c396ce2afa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810190"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay

  
  
**Относится к**: Outlook 
  
Содержит поток, который соответствует сохраненного формата [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) структуры, который хранит описание часовой пояс, который используется при выборе время окончания встречи экземпляра или приглашения на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptTZDefEndDisplay  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000825F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Время начала и время окончания экземпляра хранилища Microsoft Office Outlook 2003 или более ранних версий и решения, основанные на объекты совместной работы (CDO) 1.2.1 и, не запускайте средство обновления календаря Outlook или Microsoft Exchange Server встречи и приглашения на собрания в формате UTC. Эти клиенты не следует хранить какие-либо сведения для часового пояса, в котором создается встречи или приглашения на собрание.
  
Версии Microsoft Outlook, начиная с Microsoft Office Outlook 2007 и решения, основанные на CDO 1.2.1 (en), ранее выполненные календаря Outlook или Exchange Server обновление использования средства **dispidApptTZDefEndDisplay** для хранения часовой пояс времени окончания. **dispidApptTZDefEndDisplay** показывает встречи или собрания в исходный часовой пояс, оно было запланировано и определяет корректировки время окончания при изменении правила часового пояса. Если это свойство не найден, используется часовой пояс, указанного в свойстве **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)). Если **dispidApptTZDefStartDisplay** отсутствует или является недопустимым, используется значение текущего часового пояса. **dispidApptTZDefEndDisplay** используется только для отображения и не используется в расширения повторения. 
  
Средство синтаксического анализа необходимо следить за тем, при считывании потока, полученный из **dispidApptTZDefEndDisplay**или для сохранения **TZDEFINITION** поток для, направленных на двоичного свойства, такие как **dispidApptTZDefEndDisplay**. Для получения дополнительных сведений см [Сохранение TZDEFINITION поток, чтобы зафиксировать двоичного свойства](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **dispidApptTZDefEndDisplay** указывает часовой пояс информацию для свойства **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). Формат, ограничений и вычисление **dispidApptTZDefEndDisplay** совпадают, указанный в свойстве **dispidApptTZDefStartDisplay** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

