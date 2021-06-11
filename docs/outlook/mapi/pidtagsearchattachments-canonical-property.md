---
title: Каноническое свойство PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336325"
---
# <a name="pidtagsearchattachments-canonical-property"></a>Каноническое свойство PidTagSearchAttachments

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит строку Unicode, запрашиваемую в содержимом вложений в магазине.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|Идентификатор:  <br/> |0x0EA5  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

> [!NOTE]
> Этот тег ограничения MAPI, используемый при поиске содержимого вложений, может не быть определен в загружаемом файле загона, который у вас есть в настоящее время. Его можно добавить в код, используя следующее значение: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Microsoft Exchange Server протоколы.
    
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

