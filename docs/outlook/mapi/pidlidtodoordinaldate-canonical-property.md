---
title: Каноническое свойство PidLidToDoOrdinalDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d708424ccb15be15746fe8a33eea73a8e0f99323
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810630"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Каноническое свойство PidLidToDoOrdinalDate

  
  
**Относится к**: Outlook 
  
Определяет порядок сортировки объектов в список дел консолидированной среды.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidToDoOrdinalDate  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x000085A0  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Когда объект имеет флаг, это свойство необходимо задать текущее время в формате UTC. 
  
Если клиент позволяет пользователю изменять их порядок задач в списке консолидированной задач путем перетаскивания или другие механизмы, они могут использовать любой подходящий алгоритм для определения нового значения этого свойства, чтобы задачи отображается в нужное место, когда это свойство используется в качестве озрастанию поля области.
  
Когда это свойство используется для сортировки объектов и сортировка результатов в набор функций, как средства разбиения слов связывают используется свойство **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

