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
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345019"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a>Каноническое свойство PidLidAppointmentTimeZoneDefinitionStartDisplay

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит поток, который сопоставляется с сохраненным форматом структуры [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , в котором хранится описание для часового пояса, используемого при выборе параметра время начала встречи с одним экземпляром или приглашения на собрание. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидаппттздефстартдисплай  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x0000825E  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Microsoft Office Outlook 2003 или более ранней версии, а также решения, основанные на объектах данных совместной работы (CDO) 1.2.1 и не запускают средство обновления календаря для Outlook или Microsoft Exchange Server, сохраняют время начала и окончания встреч и приглашений на собрание в формате UTC. Эти клиенты не хранят никакие сведения о часовом поясе, в котором создается приглашение на встречу или собрание.
  
Версии Outlook, начиная с Microsoft Office Outlook 2007, и решения, основанные на CDO 1.2.1, на котором запущено средство обновления календаря Outlook или Exchange Server. это свойство используется для хранения часового пояса для времени начала. Свойство **диспидаппттздефстартдисплай** показывает встречу или собрание в исходном часовом поясе, в котором оно было запланировано. Он определяет, должно ли время начала быть скорректировано при изменении правил часового пояса. Если это свойство отсутствует, подразумевается текущий местный часовой пояс. Это свойство используется только для отображения и не используется в развертывании повторений. 
  
Синтаксический анализатор должен быть внимательным при чтении потока, полученного из этого свойства, или при сохранении **TZDEFINITION** в поток для фиксации в двоичном свойстве, например **диспидаппттздефстартдисплай**. Дополнительные сведения [о СОХРАНЕНИИ TZDEFINITION в потоке для фиксации в двоичном свойстве](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).
  
Это свойство определяет сведения о часовом поясе для свойства **диспидапптстартвхоле** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). Значение **диспидаппттздефстартдисплай** используется для преобразования даты начала и времени из UTC в местный часовой пояс для отображения. Для каждого **тзруле** , указанного этим свойством, флаг TZRULE_FLAG_RECUR_CURRENT_TZREG не должен быть установлен. Например, если **тзруле** является эффективным правилом, значение поля **тзруле** должно быть "0x0002"; в противном случае он должен иметь значение "0x0000". 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server..
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

