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
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359516"
---
# <a name="pidtagrowtype-canonical-property"></a>Каноническое свойство PidTagRowType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, которое указывает тип строки в таблице.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROW_TYPE  <br/> |
|Идентификатор:  <br/> |0x0FF5  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |MAPI, не передаваемая  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство отображается только в таблицах контента. Категория существует только при найме элементов.
  
Это свойство может иметь одно из следующих значений:
  
TBL_LEAF_ROW 
  
> Представляет фактические данные, а не строку категории.
    
TBL_EMPTY_CATEGORY 
  
> В настоящее время не используется.
    
TBL_EXPANDED_CATEGORY 
  
> Категория расширена; пользовательский интерфейс обычно отображает это со знаком минус ( - ) рядом с ним.
    
TBL_COLLAPSED_CATEGORY 
  
> Категория свернута; пользовательский интерфейс обычно отображает это со знаком плюс (+) рядом с ним.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Включает допустимые операции для основных объектов таблицы.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagRowid](pidtagrowid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

