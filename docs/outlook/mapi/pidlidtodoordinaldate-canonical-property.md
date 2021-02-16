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
ms.openlocfilehash: b0c5e3019efeeb0b9788d81e8730e976bfcc9d75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345278"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a>Каноническое свойство PidLidToDoOrdinalDate

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет порядок сортировки объектов в консолидированном списке дел.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidToDoOrdinalDate  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x000085A0  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Примечания

Когда объект помечается, этому свойству следует установить текущее время в UTC. 
  
Если клиент позволяет пользователю переусортировать задачи в консолидированном списке задач с помощью перетаскиваний или других механизмов, он может использовать любой подходящий алгоритм для определения нового значения этого свойства, чтобы задача появилась в нужном месте при использовании этого свойства в качестве поля сортировки.
  
Если это свойство используется для сортировки объектов и сортировка приводит к связывать, свойство **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal)](pidlidtodosubordinal-canonical-property.md)используется в качестве разбиение на связь.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с помезданием.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

