---
title: Каноническое свойство PidLidAppointmentProposedDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentProposedDuration
api_type:
- COM
ms.assetid: 37806778-a19a-4905-a845-525d3912bf9e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 56a652e630af70d4cfde12995951a352a1aa97e3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390621"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a>Каноническое свойство PidLidAppointmentProposedDuration

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, предлагаемое значение для свойства **dispidApptDuration** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) для предложение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptProposedDuration  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008256  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Meetings (собрания);  <br/> |
   
## <a name="remarks"></a>Замечания

Если задано, оно должно быть равно число минут между свойствами **dispidApptProposedEndWhole** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)) и **dispidApptProposedStartWhole** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)).
  
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

