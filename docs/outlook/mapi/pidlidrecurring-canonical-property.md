---
title: Каноническое свойство PidLidRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 36bf204823711e87ac6250f0997445f2745fbc19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810484"
---
# <a name="pidlidrecurring-canonical-property"></a>Каноническое свойство PidLidRecurring

  
  
**Относится к**: Outlook 
  
Указывает, является ли повторяющаяся сообщение встречи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidRecurring  <br/> |
|Набор свойств:  <br/> |PSETID_Appointment  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008223  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Календарь  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство имеет значение TRUE, если встреча является повторяющейся встречи и имеет значение FALSE, если оно не является повторяющимся.
  
Это свойство определяет, представляет ли объект серии повторяющихся. Значение TRUE указывает, что объект представляет серии повторяющихся. Значение FALSE или отсутствие этого свойства указывает, что объект представляет один экземпляр или исключение (включая потерянного экземпляра). Обратите внимание на разницу между этого свойства и свойства **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
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

