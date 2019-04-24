---
title: Каноническое свойство PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316298"
---
# <a name="pidtagflagstatus-canonical-property"></a>Каноническое свойство PidTagFlagStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает состояние флага объекта Message.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ФЛАГ_СТАТУС  <br/> |
|Идентификатор:  <br/> |0x1090  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не должно существовать в объекте, связанном с собранием, и не должно существовать в объекте Task. Если задано для других объектов Message, этому свойству необходимо присвоить одно из следующих значений:
  
|**Числовое значение**|**Имя**|**Описание**|
|:-----|:-----|:-----|
|Отсутствует  <br/> |Недоступно  <br/> |Без отметки  <br/> |
|0x00000001  <br/> |Фолловупкомплете  <br/> |Помеченные как завершенные  <br/> |
|0x00000002  <br/> |Фолловупфлагжед  <br/> |Отмеченные  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с пометкой.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

