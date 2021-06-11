---
title: Каноническое свойство PidLidReminderDelta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 86a0203f930661452bb143e247c17ef6da8ed436
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315892"
---
# <a name="pidlidreminderdelta-canonical-property"></a>Каноническое свойство PidLidReminderDelta

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает интервал в минутах между временем, когда напоминание впервые становится просроченным, и временем начала объекта календаря.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidReminderDelta  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008501  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть заданной для объектов календаря. Для всех не календарных объектов это свойство должно быть заданной на 0x00000000 и игнорируется. При отклонении напоминания для одного экземпляра повторяющегося объекта календаря значение этого свойства используется при вычислении времени сигнала для следующего экземпляра. Сведения о создании объектов календаря см. в материале [[MS-OXOCAL].](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Указывает свойства и модель взаимодействия для электронной почты и других напоминаний объектов.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

