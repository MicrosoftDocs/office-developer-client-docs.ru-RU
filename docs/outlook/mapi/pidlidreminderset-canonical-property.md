---
title: Каноническое свойство PidLidReminderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335156"
---
# <a name="pidlidreminderset-canonical-property"></a>Каноническое свойство PidLidReminderSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, установлено ли напоминание на объекте.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidReminderSet  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008503  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Примечания

Если повторяющийся объект календаря имеет это свойство значение TRUE, клиент может переопредить это значение для исключений.
  
Если это свойство false для повторяющегося объекта календаря, напоминания отключены для всей серии, включая исключения. Для повторяющихся объектов задач это свойство нельзя переопределять исключениями (подробнее см. [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) [и [MS-OXOTASK]).](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) 
  
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

