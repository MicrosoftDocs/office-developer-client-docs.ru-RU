---
title: Каноническое свойство PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d19904b65b95468bd38df75aa8e05afdf0075961
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811858"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a>Каноническое свойство PidTagSearchFolderDefinition

  
  
**Относится к**: Outlook 
  
Содержит данные, которые указывает условия поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WB_SF_DEFINITION  <br/> |
|Идентификатор:  <br/> |0x6845  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="remarks"></a>Замечания

Содержимое каждого поля больших двоичных объектов (BLOB) этого свойства зависит от идентификатор шаблона, который указан в свойстве **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)). Сведения о шаблонах структуры и поиска больших двоичных ОБЪЕКТОВ можно [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Задает свойства и операции для управления конфигурации список папок поиска.
    
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

