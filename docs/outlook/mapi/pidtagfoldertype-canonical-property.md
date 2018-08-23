---
title: Каноническое свойство PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8d6167a7a3c983171f2ff9cb2a54c879a14dca0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591417"
---
# <a name="pidtagfoldertype-canonical-property"></a>Каноническое свойство PidTagFolderType

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит константы, которое указывает тип папки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FOLDER_TYPE  <br/> |
|Идентификатор:  <br/> |0x3601  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство может иметь только один из следующих значений:
  
FOLDER_GENERIC 
  
> Общая папка, содержащая сообщения и другие папки.
    
FOLDER_ROOT 
  
> В корневой папке таблице иерархии папок, то есть, папки, содержащие родительской папки.
    
FOLDER_SEARCH 
  
> Папка, содержащая результаты поиска, в виде ссылок на сообщения, соответствующие критериям поиска.
    
Не следует путать с корневым поддерево электронной почты — это сообщение (IPM) в этом хранилище корневого хранилища сообщений. Хранилище корневой папке не имеет родительского, полученный путем вызова метода [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором значение null, запись. Поддерева IPM корневую папку имеет родительского объекта, полученные с помощью значение свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) для вызова **OpenEntry** . 
  
MAPI разрешает только один корневой папки на банк сообщений. В этой папке содержатся сообщения и другие папки. Свойство **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) в корневой папке содержит идентификатор записи папки собственные.
  
Сведения, приведенные в папку результатов поиска главным образом хранится в таблицу, которая содержит же столбцов, как типичное содержимое таблицы, а также два дополнительных столбца, идентифицирующий к папке, в которой каждый сообщение об ошибке: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (отображаемое имя, необходимые) и это свойство (идентификатор записи, необязательно).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папки.
    
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

