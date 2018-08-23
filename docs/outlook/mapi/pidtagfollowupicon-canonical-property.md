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
ms.openlocfilehash: 8fa96736b5404d84c6ab48851b916c5ab987ae2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593923"
---
# <a name="pidtagfollowupicon-canonical-property"></a>Каноническое свойство PidTagFollowupIcon

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает цвет объекта message.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Идентификатор:  <br/> |0x1095  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Переименование папки сообщения  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство не должна существовать, если значение свойства **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) имеет значение «followupFlagged» или объект message — это объект, относящихся к собранию. Это свойство не должна существовать для объекта задачи. Если установлено на другие объекты сообщения, это свойство должно быть присвоено одно из следующих значений.
  
|**Числовое значение**|**Имя**|**Описание**|
|:-----|:-----|:-----|
|Этот параметр не указан  <br/> |Н/Д  <br/> |Без цвета  <br/> |
|1  <br/> |followupIcon1  <br/> |Лиловый флажок  <br/> |
|2  <br/> |followupIcon2  <br/> |Оранжевый флажок  <br/> |
|3  <br/> |followupIcon3  <br/> |Зеленый флажок  <br/> |
|4  <br/> |followupIcon4  <br/> |Желтый флажок  <br/> |
|5  <br/> |followupIcon5  <br/> |Синий флажок  <br/> |
|6  <br/> |followupIcon6  <br/> |Красный флажок  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

