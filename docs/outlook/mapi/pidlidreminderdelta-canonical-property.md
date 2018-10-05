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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398007"
---
# <a name="pidlidreminderdelta-canonical-property"></a>Каноническое свойство PidLidReminderDelta

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает интервал в минутах между времени, когда напоминания сначала становится просроченные и время начала объекта календаря.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidReminderDelta  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008501  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство необходимо установить на объекты календаря. Для всех объектов не календаря это свойство должно иметь значение «0x00000000» и будет пропущен. После закрытия напоминания для одного экземпляра объекта повторяющихся календаря, значение этого свойства используется в расчет времени сигнала следующего экземпляра. Для получения дополнительных сведений о создании объекта календаря в разделе [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Задает свойства и модель взаимодействия для электронной почты и других объектов напоминания.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

