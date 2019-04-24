---
title: Каноническое свойство PidLidTaskFRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aec9dd328e802e185c870d3ecd94cbd1d10ac67d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303054"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a>Каноническое свойство PidLidTaskFRecurring

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, содержит ли задача шаблон повторения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидтаскфрекур  <br/> |
|Набор свойств:  <br/> |Псетид_таск  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008126  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Замечания

Если это свойство не задано, используется значение по умолчанию FALSE. Если задано значение TRUE, то свойства **диспидтаскрекур** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) и **диспидтаскдеадоккур** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) также должны быть заданы в [[MS-оксотаск]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронные эквиваленты задач, назначений задач и обновлений задач.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

