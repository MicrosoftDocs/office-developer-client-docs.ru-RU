---
title: Каноническое свойство PidLidAppointmentStartWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f7137e3d5712e7d7ce12800a07b860679dd099a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810206"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a>Каноническое свойство PidLidAppointmentStartWhole

  
  
**Относится к**: Outlook 
  
Представляет дату и время начала встречи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptStartWhole  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000820D  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет дату начала и время события. Это свойство должно быть в формате UTC и должен быть меньше, чем значение свойства **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)). Для серии повторяющихся это свойство является дата и время начала первого экземпляра определяется шаблон повторения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
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
