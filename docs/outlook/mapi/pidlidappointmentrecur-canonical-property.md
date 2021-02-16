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
ms.openlocfilehash: de50616664048af6b931a09df7c65461e9ee3399
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331782"
---
# <a name="pidlidappointmentrecur-canonical-property"></a>Каноническое свойство PidLidAppointmentRecur

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает даты и время повторения ряда с помощью одного из шаблонов повторения и диапазонов, указанных [в [MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidApptRecur  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008216  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство указывает даты и время повторения ряда с помощью одного из шаблонов повторения и диапазонов, подробно [указанных в [MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx). Значение этого свойства также содержит сведения об измененных и удаленных исключениях; такие сведения, как даты, тема, расположение и некоторые другие свойства исключений. Двоичные данные в этом свойстве для повторяющихся элементов календаря хранятся в структуре **AppointmentRecurrencePattern.** Это свойство не должно существовать для элементов календаря одного экземпляра. 
  
Существуют некоторые ограничения для повторения:
  
- Несколько экземпляров не должны запускаться в один день.
    
- Вхождения не должны перекрываться. В частности, исключение, которое изменяет дату начала экземпляра в повторяющейся серии, должно возникать в дату, которая находится после окончания предыдущего экземпляра и начала следующего экземпляра повторяющегося ряда. То же самое справедливо, если предыдущие или следующие экземпляры повторяющегося ряда являются исключениями.
    
Расписание повторяющегося ряда определяется его расписанием повторения и диапазоном.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Указывает свойства и модель взаимодействия для электронной почты и других напоминаний об объектах.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

