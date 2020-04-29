---
title: Каноническое свойство PidTagDepth
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 75d390edd06aaf826f6b8c2d996e4e08bf6a7334
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360853"
---
# <a name="pidtagdepth-canonical-property"></a>Каноническое свойство PidTagDepth

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит целое число, представляющее относительный уровень отступа или глубины объекта в таблице иерархий.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DEPTH  <br/> |
|Идентификатор:  <br/> |0x3005  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие протоколы MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

В этом свойстве также можно указать уровень классификации строки в таблице содержимого или глубину иерархии в таблице иерархий. Глубина отсчета от нуля, где ноль соответствует самой левой категории. Во всех случаях значение свойства представляет относительное значение, а не абсолютное значение. Например, в таблице иерархий значение глубины задается относительно контейнера, из которого была получена таблица иерархии. Глубина не представляет абсолютную глубину из корневого контейнера. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКТАБЛ]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Включает в себя допустимые операции для основных объектов Table.
    
[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[Каноническое свойство PidTagSelectable](pidtagselectable-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

