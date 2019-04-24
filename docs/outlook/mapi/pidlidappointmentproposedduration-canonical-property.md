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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356380"
---
# <a name="pidlidappointmentproposedduration-canonical-property"></a>Каноническое свойство PidLidAppointmentProposedDuration

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает предлагаемое значение для свойства **диспидапптдуратион** ([PidLidAppointmentDuration](pidlidappointmentduration-canonical-property.md)) для предложения Counter.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидапптпропоседдуратион  <br/> |
|Набор свойств:  <br/> |Псетид_аппоинтмент  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008256  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Примечания

Если этот параметр установлен, он должен быть равен количеству минут между свойствами **диспидапптпропоседстартвхоле** ([PidLidAppointmentProposedStartWhole](pidlidappointmentproposedstartwhole-canonical-property.md)) и **диспидапптпропоседендвхоле** ([PidLidAppointmentProposedEndWhole](pidlidappointmentproposedendwhole-canonical-property.md)).
  
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

