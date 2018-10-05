---
title: Каноническое свойство PidTagSearchFolderExpiration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385948"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a>Каноническое свойство PidTagSearchFolderExpiration

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит время, по которому будет устаревших контейнер папки поиска и должен обновить или создать заново.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WB_SF_EXPIRATION  <br/> |
|Идентификатор:  <br/> |0x683A  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должен быть отформатирован в поле число минут после полночи по Гринвичу (UTC) 1 января 1601.
  
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

