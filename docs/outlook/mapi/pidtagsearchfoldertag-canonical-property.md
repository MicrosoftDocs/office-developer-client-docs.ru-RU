---
title: Каноническое свойство PidTagSearchFolderTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b7a88387-72ff-49e5-b73a-8bafab635658
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a4ad72c147abebfe9863d19690bc9f27f00544a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282322"
---
# <a name="pidtagsearchfoldertag-canonical-property"></a>Каноническое свойство PidTagSearchFolderTag

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, используемее для синхронизации этого сообщения определения с контейнером папки поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WB_SF_TAG  <br/> |
|Идентификатор:  <br/> |0x6847  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство меняется при смене сообщения определения. Она должна изменять каждую итерацию, но она не может быть уникальной.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Указывает свойства и операции для управления конфигурацией списка папки поиска.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

