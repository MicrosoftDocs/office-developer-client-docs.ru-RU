---
title: Каноническое свойство PidTagFlagCompleteTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagCompleteTime
api_type:
- HeaderDef
ms.assetid: effc738a-30f4-4a5e-b21d-04b50dad1f45
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6e1c2783abd186146fe738a3396e098711893d3a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583984"
---
# <a name="pidtagflagcompletetime-canonical-property"></a>Каноническое свойство PidTagFlagCompleteTime

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает дату и время в формате универсального времени (UTC), который объект message был помечен как выполненное.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FLAG_COMPLETE_TIME  <br/> |
|Идентификатор:  <br/> |0x1091  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство удаляется, если объект сообщения не имеет флаг завершена. Разрешение наименьшее время должно быть минут (значение должно быть множитель 600,000,000). Это свойство не должна существовать, если объект является объектом, связанные с собрания и не должно быть для объекта задачи.
  
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

