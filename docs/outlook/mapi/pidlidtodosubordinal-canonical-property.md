---
title: Каноническое свойство PidLidToDoSubOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoSubOrdinal
api_type:
- COM
ms.assetid: e3bc15ef-155e-49fd-88e5-64713df9b939
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c4ea125a5bde89e0885be4c04e3f106f202b1e18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344921"
---
# <a name="pidlidtodosubordinal-canonical-property"></a>Каноническое свойство PidLidToDoSubOrdinal

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выступает в качестве тай-брейка, когда **свойство dispidToDoOrdinalDate** [(PidLidToDoOrdinalDate)](pidlidtodoordinaldate-canonical-property.md)сортирует объекты и результат в галстуке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidToDoSubOrdinal  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A1  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Если используется, это свойство должно быть отсортифицировано лексикографически. Компонентные символы строки должны состоять только из цифр от нуля до девяти. Изначально это свойство должно быть заданной на "5555555". Длина этого свойства не должна превышать 254 символа (за исключением завершаемого символа NULL).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с маркировкой.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidLidToDoOrdinalDate](pidlidtodoordinaldate-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

