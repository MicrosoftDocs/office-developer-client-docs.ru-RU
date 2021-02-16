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
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316319"
---
# <a name="pidtagfoldertype-canonical-property"></a>Каноническое свойство PidTagFolderType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит константы, которые указывают тип папки. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FOLDER_TYPE  <br/> |
|Идентификатор:  <br/> |0x3601  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство может иметь одно из следующих значений:
  
FOLDER_GENERIC 
  
> Общая папка, содержащую сообщения и другие папки.
    
FOLDER_ROOT 
  
> Корневая папка таблицы иерархии папок, то есть папка без родительской папки.
    
FOLDER_SEARCH 
  
> Папка с результатами поиска в виде ссылок на сообщения, которые соответствуют условиям поиска.
    
Корневой текст хранения сообщений не следует путать с корнем поддерево межличностного сообщения (IPM) в этом хранилище. Корневая папка магазина, которая не имеет родительского, получается путем вызова метода [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором записи null. Корневая папка поддерево IPM, которая имеет родительский объект, получается с помощью значения свойства **PR_IPM_SUBTREE_ENTRYID** [(PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)для вызова **OpenEntry.** 
  
MAPI разрешает только одну корневую папку на хранилище сообщений. Эта папка содержит сообщения и другие папки. Свойство PR_PARENT_ENTRYID корневой **папки** ([PidTagParentEntryId)](pidtagparententryid-canonical-property.md)содержит собственный идентификатор записи папки.
  
Сведения в папке результатов поиска в основном хранятся в таблице содержимого, которая содержит те же столбцы, что и обычная таблица содержимого, а также два дополнительных столбца, определяющих папку, в которой было найдено каждое сообщение: **PR_PARENT_DISPLAY** ([PidTagParentDisplay)](pidtagparentdisplay-canonical-property.md)(отображаемого имени, обязательно) и это свойство (идентификатор записи, необязательный).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции с папками.
    
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

