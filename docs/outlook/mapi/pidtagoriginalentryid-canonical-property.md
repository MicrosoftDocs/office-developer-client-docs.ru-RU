---
title: Каноническое свойство PidTagOriginalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalEntryId
api_type:
- COM
ms.assetid: 8197d2c7-8665-41b8-bd3a-e9c1c2e642e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eab72c5b49ba501d8ab5516bf5a5eae9ea82abe0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588708"
---
# <a name="pidtagoriginalentryid-canonical-property"></a>Каноническое свойство PidTagOriginalEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит исходный идентификатор записи для входа, скопированные из адресной книги для Личная адресная книга или других доступным для записи адресной книги.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x3A12  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство является одним из свойств, которые содержат сведения о оригинального источника скопированной запись.
  
Для nonread отчета это свойство содержит копию идентификатор записи исходный получатель сообщения, для которого создается отчет. Если исходный получатель входит в список рассылки, идентификатор записи списка рассылки сохраняется для отчета.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.
    
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

