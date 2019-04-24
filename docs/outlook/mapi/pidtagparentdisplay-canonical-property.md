---
title: Каноническое свойство PidTagParentDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7aef4c1d83672033662502ad0950b7bac9f58c52
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331516"
---
# <a name="pidtagparentdisplay-canonical-property"></a>Каноническое свойство PidTagParentDisplay

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемое имя папки, в которой было найдено сообщение во время поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ПАРЕНТ_ДИСПЛАЙ, ПР_ПАРЕНТ_ДИСПЛАЙ_А, ПР_ПАРЕНТ_ДИСПЛАЙ_В  <br/> |
|Идентификатор:  <br/> |0x0E05  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Несъемный MAPI  <br/> |
   
## <a name="remarks"></a>Комментарии

Эти свойства не находятся ни в одном объекте. Они могут отображаться только в таблице содержимого папки результатов поиска.
  
Эти свойства и свойства **пр_парент_ентрид** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) не связаны друг с другом. Они относятся исключительно к разным контекстам.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

