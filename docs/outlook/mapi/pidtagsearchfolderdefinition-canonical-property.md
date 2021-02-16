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
ms.openlocfilehash: 3b4e5fa7228cf243c79a8ec0c9e2b73b7da21c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336360"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a>Каноническое свойство PidTagSearchFolderDefinition

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит данные, которые заданы условия поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WB_SF_DEFINITION  <br/> |
|Идентификатор:  <br/> |0x6845  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="remarks"></a>Примечания

Конкретное содержимое каждого поля двоичного большого объекта (BLOB), содержащихся в этом свойстве, зависит от кода шаблона, указанного в свойстве **PidTagSearchFolderTemplateId** [(PidTagSearchFolderTemplateId).](pidtagsearchfoldertemplateid-canonical-property.md) Сведения о структуре BLOB и шаблонах поиска см. [в [MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Указывает свойства и операции для управления конфигурацией списка папок поиска.
    
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

