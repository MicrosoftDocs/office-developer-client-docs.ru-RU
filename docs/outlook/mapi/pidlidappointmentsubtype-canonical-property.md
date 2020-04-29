---
title: Каноническое свойство PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345418"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>Каноническое свойство PidLidAppointmentSubType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, является ли событие днем.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидапптсубтипе  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008215  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Данное свойство указывает, является ли событие на целый день, как указано пользователем. Значение TRUE указывает, что событие является событием на целый день, в этом случае время начала и время окончания должно быть в полночь, чтобы длительность составлять не более 24 часов и составлять не менее 24 часов. Значение FALSE или отсутствие этого свойства указывает на то, что событие не является событием на целый день. Клиент или сервер не должен определять значение как TRUE, если пользователь создает событие, которое составляет 24 часа, даже если событие начинается и заканчивается в полночь.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
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

