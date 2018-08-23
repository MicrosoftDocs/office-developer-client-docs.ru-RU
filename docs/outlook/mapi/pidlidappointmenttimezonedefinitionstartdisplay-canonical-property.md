---
title: Каноническое свойство PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6ca53633f0c1e5b226f7e03c8ee702d4cda7d115
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586797"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Каноническое свойство PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который соответствует сохраненного формата [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) структуры, который хранит описание часовой пояс, который используется при выборе время начала единичных встречи или приглашения на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptTZDefStartDisplay  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000825E  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Время начала и время окончания экземпляра хранилища Microsoft Office Outlook 2003 или более ранних версий и решения, основанные на объекты совместной работы (CDO) 1.2.1 и, не запускайте средство обновления календаря Outlook или Microsoft Exchange Server встречи и приглашения на собрания в формате UTC. Эти клиенты не следует хранить какие-либо сведения для часового пояса, в котором создается встречи или приглашения на собрание.
  
Версии Outlook, так как Microsoft Office Outlook 2007 и решений на основании CDO 1.2.1 (en), ранее выполненные средство обновления календаря Outlook или Exchange Server это свойство используется для хранения часовой пояс для времени начала. Свойство **dispidApptTZDefStartDisplay** показывает встречи или собрания в исходный часовой пояс, что было запланировано. Определяет корректировки время начала изменения правила часового пояса. Если данное свойство отсутствует, используется значение текущего часового пояса. Это свойство используется только для отображения и не используется в расширения повторения. 
  
Средство синтаксического анализа необходимо следить за тем, при считывании потока, полученного из этого свойства или для сохранения **TZDEFINITION** поток для, направленных на двоичного свойства, такие как **dispidApptTZDefStartDisplay**. Для получения дополнительных сведений см [Сохранение TZDEFINITION поток, чтобы зафиксировать двоичного свойства](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Это свойство определяет часовой пояс информацию для свойства **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). Значение **dispidApptTZDefStartDisplay** используется для преобразования даты начала и время в формате UTC в локальный часовой пояс для отображения. Для каждого **TZRULE** заданный этим свойством флаг TZRULE_FLAG_RECUR_CURRENT_TZREG не должно быть задано. Например если **TZRULE** эффективных правило, значение поля, **TZRULE** должен быть «0x0002»; в противном случае он должен быть «0x0000». 
  
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

