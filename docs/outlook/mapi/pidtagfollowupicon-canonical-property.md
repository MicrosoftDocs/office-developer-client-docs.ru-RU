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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает цвет флага объекта сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FOLLOWUP_ICON  <br/> |
|Идентификатор:  <br/> |0x1095  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Переименование папки сообщений  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство не должно существовать, если значение свойства **PR_FLAG_STATUS** ([PidTagFlagStatus)](pidtagflagstatus-canonical-property.md)не имеет значения "followupFlagged" или объект сообщения является объектом, связанным с собранием. Это свойство не должно существовать в объекте задачи. Если этот объект за установлен для других объектов сообщений, этому свойству необходимо установить одно из следующих значений.
  
|**Числовая величина**|**Название**|**Описание**|
|:-----|:-----|:-----|
|Нет  <br/> |Недоступно  <br/> |Без цвета  <br/> |
|1   <br/> |followupIcon1  <br/> |Сиреневый флаг  <br/> |
|2   <br/> |followupIcon2  <br/> |Оранжевый флаг  <br/> |
|3   <br/> |followupIcon3  <br/> |Зеленый флаг  <br/> |
|4   <br/> |followupIcon4  <br/> |Желтый флаг  <br/> |
|5   <br/> |followupIcon5  <br/> |Синий флаг  <br/> |
|6   <br/> |followupIcon6  <br/> |Красный флаг  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с помезданием.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

