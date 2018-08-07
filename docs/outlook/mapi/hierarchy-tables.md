---
title: Таблицы иерархии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 23314418836893b40cbddf3b90bd95ec061a00c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808598"
---
# <a name="hierarchy-tables"></a>Таблицы иерархии

  
  
**Относится к**: Outlook 
  
Иерархия таблица содержит сведения о папок в хранилище сообщений или контейнеров в контейнер адресной книги. Каждая строка таблицы иерархии содержит набор столбцов с сведения об одной папки или контейнер адресной книги. В основном таблиц иерархии используемого клиентами и реализации поставщиками store сообщение для отображения дерева папки и вложенные папки и реализуется поставщиками адресной книги для отображения дерево контейнеров в адресной книге. Контейнеры, которые не могут содержать субконтейнеров, как указано в отсутствие флага AB_SUBCONTAINERS в своем свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) не внедрять таблицы иерархии.
  
Доступ к таблицы иерархии можно получить путем вызова:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Или -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) передача **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) в качестве тега свойства и IID_IMAPITable идентификатор интерфейса.
    
Контейнеры и папок должны поддерживать обоих методов для получения свойства таблицы. Он недопустим для поставщиков услуг для поддержки только один способ доступа к эти таблицы, поскольку предполагается, что клиенты для выбора. 
  
> [!IMPORTANT]
> Поставщики хранилища не обязательно соблюдать порядок сортировки, указанный для таблиц иерархии набор. 
  
Вызов **IMAPIProp::OpenProperty** включает в себя доступ к таблице иерархии, открыв его соответствующего свойства **PR_CONTAINER_HIERARCHY**. Несмотря на то, что **PR_CONTAINER_HIERARCHY** не удается получить через папку или метод [IMAPIProp::GetProps](imapiprop-getprops.md) контейнера, она включена в массиве тега свойства, который возвращается методом [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_HIERARCHY** можно также использовать для включения или исключения таблицы иерархии из операцию копирования. Если клиент указывает **PR_CONTAINER_HIERARCHY** с помощью параметра *lpExcludeProps* для [IMAPIProp::CopyTo](imapiprop-copyto.md) в операцию копирования, новую папку или контейнера не будут поддерживаться в таблице иерархии исходной папки или контейнера. 
  
Следующие свойства составляют обязательный столбец, задайте в таблице иерархии:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** содержит имя для контейнера или папки, который должен отображаться в отображения иерархии. 
  
 **PR_ENTRYID** — это идентификатор записи, связанный с этим контейнер или папки. Она должна быть долгосрочного идентификатор записи. Клиенты и MAPI можно передать этот идентификатор записи **OpenEntry** откройте контейнер или папки и просмотреть его содержимое путем вызова [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** — это числовое значение, указывающее уровень отступа для этого контейнера или папки с нуля сейчас верхнего уровня. Более подробные в иерархии контейнеров или папки находится, высокое значение для свойства **PR_DEPTH** . Клиенты свойство **PR_DEPTH** используется для отображения таблицы с иерархией надлежащим образом, чтобы пользователи могли видеть четко родительские и дочерние отношения. Число уровней в контейнер или папки всегда является относительно контейнер или внедрение таблицы иерархии папок. 
  
 **PR_OBJECT_TYPE** всегда имеет MAPI_ABCONT для таблиц иерархии адресной книги и MAPI_FOLDER для таблиц иерархии папок. 
  
 **PR_DISPLAY_TYPE** — это числовое значение, связанные с как контейнер или папки отображается в таблице иерархии. Главным образом он используется для отображения, позволяет визуально различать типы контейнеров или папки. Количество сообщений хранения и адресной книги поставщиков использовать значки для отображения различных типов. Зависит от поставщика, чтобы предоставить эти значки. MAPI не поддерживает значения по умолчанию. 
  
MAPI определяет множество значений для **PR_DISPLAY_TYPE**, некоторые, допустимых для папки и другим пользователям, которые используются с таблиц иерархии контейнеров адресной книги. Как правило папка **PR_DISPLAY_TYPE** имеет значение DT_FOLDER для указания значок папки по умолчанию, DT_FOLDER_LINK, чтобы указать значок, представляющий ссылку в другую папку или DT_FOLDER_SPECIAL, чтобы указать значок, соответствующие конкретному приложению. DT_FOLDER_LINK используется с папками результатов поиска. 
  
Помимо этих обязательные столбцы таблиц иерархии адресной книги необходимо включить свойство **PR_CONTAINER_FLAGS** . **PR_CONTAINER_FLAGS** указывает различные атрибуты контейнера в иерархии и используется для различения один контейнер от другого. 
  
Необязательный свойство для таблиц иерархии адресной книги — **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Таблиц иерархии хранилища сообщений включения этих свойств в их набор необходимых столбцов:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Поставщиками адресной книги должен поддерживать следующие методы **IMAPITable** в их реализации в таблице иерархии, так как они необходимы, встроенная адресной книги MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

