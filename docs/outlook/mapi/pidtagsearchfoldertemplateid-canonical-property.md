---
title: Каноническое свойство PidTagSearchFolderTemplateId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387204"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>Каноническое свойство PidTagSearchFolderTemplateId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор шаблона, который используется для поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|Идентификатор:  <br/> |0x6841  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="remarks"></a>Замечания

Условия папки поиска задается с помощью шаблона. Это свойство в окне сообщения, определяющий папки поиска определяет ее шаблон. В дополнение к определяется условия поиска, шаблон также определяет папок, которые следует исключить из поиска, определяет элементы, исключаемые из поиска и задает значение **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).
  
Дополнительные сведения о шаблонах папки поиска можно [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
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

