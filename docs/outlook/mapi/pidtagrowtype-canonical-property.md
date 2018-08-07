---
title: Каноническое свойство PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811755"
---
# <a name="pidtagrowtype-canonical-property"></a>Каноническое свойство PidTagRowType

  
  
**Относится к**: Outlook 
  
Содержит значение, которое указывает тип строки в таблице.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROW_TYPE  <br/> |
|Идентификатор:  <br/> |0x0FF5  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |MAPI передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство отображается только на содержимое таблиц. Категории существует только в том случае, если он имеет элементов.
  
Это свойство может иметь только один из следующих значений:
  
TBL_LEAF_ROW 
  
> Представляет фактические данные, а не строкой категории.
    
TBL_EMPTY_CATEGORY 
  
> В настоящее время не используется.
    
TBL_EXPANDED_CATEGORY 
  
> Категории развернут; в пользовательском интерфейсе это обычно отображается со знаком минус (-) рядом с ним.
    
TBL_COLLAPSED_CATEGORY 
  
> Категории свернута; в пользовательском интерфейсе это обычно отображается с значок "плюс" (+) рядом с ним.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Включает в себя разрешенных операций для базовых объектов в таблице.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagRowid](pidtagrowid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

