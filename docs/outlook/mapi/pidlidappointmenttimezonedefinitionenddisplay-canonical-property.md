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
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345383"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a>Каноническое свойство PidLidAppointmentTimeZoneDefinitionEndDisplay

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который сопоставляется с сохраненным форматом структуры [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , в котором хранится описание для часового пояса, используемого при выборе времени окончания встречи с одним экземпляром или приглашения на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидаппттздефенддисплай  <br/> |
|Набор свойств:  <br/> |Псетид_аппоинтмент  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x0000825F  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Комментарии

Microsoft Office Outlook 2003 или более ранней версии, а также решения, основанные на объектах данных совместной работы (CDO) 1.2.1 и не запускают средство обновления календаря для Outlook или Microsoft Exchange Server, сохраняют время начала и окончания одного экземпляра. встречи и приглашения на собрания в формате всемирного координированного времени (UTC). Эти клиенты не хранят никакие сведения о часовом поясе, в котором создается приглашение на встречу или собрание.
  
Версии Microsoft Outlook с Microsoft Office Outlook 2007 и решения, основанные на CDO 1.2.1, на которых запущено средство обновления календаря Outlook или Exchange Server, используют **диспидаппттздефенддисплай** для хранения часового пояса времени окончания. **диспидаппттздефенддисплай** показывает встречу или собрание в исходном часовом поясе, которое было запланировано, и определяет, следует ли корректировать время окончания при изменении правил в часовом поясе. Если это свойство отсутствует, используется часовой пояс, заданный свойством **диспидаппттздефстартдисплай** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)). Если **диспидаппттздефстартдисплай** отсутствует или не является допустимым, подразумевается текущий местный часовой пояс. **диспидаппттздефенддисплай** используется только для отображения и не используется в развертывании повторений. 
  
Синтаксический анализатор должен быть внимательным при чтении потока, полученного из **диспидаппттздефенддисплай**, или при сохранении **TZDEFINITION** в потоке для фиксации в двоичном свойстве, например **диспидаппттздефенддисплай**. Дополнительные сведения [о СОХРАНЕНИИ TZDEFINITION в потоке для фиксации в двоичном свойстве](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
 **диспидаппттздефенддисплай** определяет сведения о часовом поясе для свойства **диспидапптендвхоле** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). Формат, ограничения и вычисление **диспидаппттздефенддисплай** совпадают с указанными в свойстве **диспидаппттздефстартдисплай** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
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

