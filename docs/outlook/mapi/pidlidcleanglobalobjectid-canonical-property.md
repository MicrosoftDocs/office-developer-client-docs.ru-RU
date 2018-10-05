---
title: Каноническое свойство PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400221"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a>Каноническое свойство PidLidCleanGlobalObjectId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает clean глобального **ObjectID**.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidCleanGlobalObjId  <br/> |
|Набор свойств:  <br/> |PSETID_Meeting  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00000023  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Meetings (собрания);  <br/> |
   
## <a name="remarks"></a>Замечания

Формат этого свойства совпадает с, **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)). Значение этого свойства должно быть равно значению **LID_GLOBAL_OBJID**, за исключением YH, YL, M, а D поля должно быть равно нулю. Все объекты, которые ссылаются на экземпляр повторяющегося ряда (в том числе потерянного экземпляра), а также ряд повторяющейся, будут иметь такое же значение для этого свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

