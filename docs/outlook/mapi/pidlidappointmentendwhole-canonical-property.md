---
title: Каноническое свойство PidLidAppointmentEndWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eaff90de919c1bdc04983bce32a2aa808ae56013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358900"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a>Каноническое свойство PidLidAppointmentEndWhole

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Представляет дату и время окончания встречи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспидапптендвхоле  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x0000820E  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство соответствует свойству **диспидапптендвхоле** встречи в объектной модели Microsoft Office Outlook. 
  
Указывает дату и время окончания события; Он должен быть в формате UTC и должен быть больше значения свойства **диспидапптстартвхоле** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). Для повторяющихся рядов свойство **диспидапптендвхоле** — это конечная дата и время первого экземпляра в соответствии с шаблоном повторения. 
  
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

