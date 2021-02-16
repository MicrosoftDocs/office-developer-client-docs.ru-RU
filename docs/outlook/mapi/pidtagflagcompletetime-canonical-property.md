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
ms.openlocfilehash: 5dd0d4c19f30e189218b1aeddd333df58e42102a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316291"
---
# <a name="pidtagflagcompletetime-canonical-property"></a>Каноническое свойство PidTagFlagCompleteTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает дату и время в UTC, когда объект сообщения был помечен как завершенный.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FLAG_COMPLETE_TIME  <br/> |
|Идентификатор:  <br/> |0x1091  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство удаляется, если объект сообщения не помечен как завершенный. Минимальное разрешение времени должно быть в минутах (значение должно быть кратным 600 000 000). Это свойство не должно существовать, если объект является объектом, связанным со собранием, и не должно существовать в объекте задачи.
  
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

