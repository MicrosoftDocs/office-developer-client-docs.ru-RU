---
title: Каноническое свойство PidLidAppointmentRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentRecur
api_type:
- COM
ms.assetid: 56d6240f-d07b-48d1-aef0-bf57078ea6c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 815b4f60adb65791cdd4c7d7d00a0cfc7d9e3fdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810143"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Каноническое свойство PidLidAppointmentRecur

  
  
**Относится к**: Outlook 
  
Задает значения даты и времени, когда серии повторяющихся происходит с помощью одного из шаблоны повторения и диапазоны, которые указаны в [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptRecur  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008216  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет значения даты и времени при серии повторяющихся происходит с помощью одного из шаблоны повторения и диапазоны в [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). Значение этого свойства также приводятся сведения о измененные и удаленные исключения; сведения, такие как даты, тему, местоположение и некоторые другие свойства исключения. Двоичные данные в этом свойстве для повторяющихся элементов календаря сохраняется как структура **AppointmentRecurrencePattern** . Это свойство не должна существовать на элементах календаря один экземпляр. 
  
Существует несколько ограничений повторениями.
  
- Несколько экземпляров не должно начинаться в тот же день.
    
- Не должен перекрывать вхождений. В частности исключение, которое изменяет дату начала экземпляра из серии повторяющихся должно находиться на даты, после окончания предыдущего экземпляра и начала следующего экземпляра в повторяющейся последовательности. Это значение true, если предыдущий или следующий экземпляры из серии повторяющихся исключений.
    
Расписание для серии повторяющихся определяется его шаблона повторения и диапазон.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

