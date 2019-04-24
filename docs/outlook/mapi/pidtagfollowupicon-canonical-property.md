---
title: Каноническое свойство PidTagFollowupIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316284"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Каноническое свойство PidTagFollowupIcon

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает цвет флажка для объекта Message.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ФОЛЛОВУП_ИКОН  <br/> |
|Идентификатор:  <br/> |0x1095  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |ПереИменование папки сообщений  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не должно существовать, если для свойства **пр_флаг_статус** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) не задано значение "фолловупфлагжед", или объект Message является объектом, связанным с собранием. Это свойство не должно существовать для объекта Task. Если задано для других объектов Message, этому свойству необходимо присвоить одно из следующих значений.
  
|**Числовое значение**|**Имя**|**Описание**|
|:-----|:-----|:-----|
|Отсутствует  <br/> |Недоступно  <br/> |Нет цвета  <br/> |
|1,1  <br/> |followupIcon1  <br/> |Лиловый флаг  <br/> |
|2  <br/> |followupIcon2  <br/> |Оранжевый флаг  <br/> |
|4  <br/> |followupIcon3  <br/> |Зеленый флаг  <br/> |
|SP4  <br/> |followupIcon4  <br/> |Желтый флаг  <br/> |
|17:00  <br/> |followupIcon5  <br/> |Синий флажок  <br/> |
|ICMPv6  <br/> |followupIcon6  <br/> |Красный флаг  <br/> |
   
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

