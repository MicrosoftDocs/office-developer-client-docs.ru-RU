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
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428370"
---
# <a name="hierarchy-tables"></a>Таблицы иерархии

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица иерархии содержит сведения о папках в хранилище сообщений или контейнерах в контейнере адресной книги. Каждая строка таблицы иерархии содержит набор столбцов с информацией об одной папке или контейнере адресной книги. Таблицы иерархии в основном используются клиентами и реализуются поставщиками store сообщений для показа дерева папок и вложенных папок и реализованы поставщиками адресных книг для показа дерева контейнеров в адресной книге. Контейнеры, которые не могут удерживать подконтайнеры, на что указывает отсутствие флага AB_SUBCONTAINERS в свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags),](pidtagcontainerflags-canonical-property.md)не реализуют таблицу иерархии.
  
Доступ к таблице иерархии можно получить с помощью вызова:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Или -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) passing **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)в качестве тега свойства и IID_IMAPITable в качестве идентификатора интерфейса.
    
Контейнеры и папки должны поддерживать оба метода искомые свойства таблицы. Недопустимо, чтобы поставщики услуг поддерживают только один из способов доступа к этим таблицам, так как клиенты ожидают выбора. 
  
> [!IMPORTANT]
> Поставщики магазина не гарантируют, что они будут соблюдать порядок сортировки, указанный для таблиц иерархии. 
  
Вызов **IMAPIProp::OpenProperty** включает доступ к таблице иерархии путем открытия соответствующего **свойства, PR_CONTAINER_HIERARCHY**. Хотя **PR_CONTAINER_HIERARCHY** не удается получить с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) папки или контейнера, он включается в массив тегов свойств, который возвращается методом [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_HIERARCHY** также можно использовать для включаемой или исключаемой таблицы иерархии из операции копирования. Если клиент указывает  PR_CONTAINER_HIERARCHY в параметре *lpExcludeProps* для [IMAPIProp::CopyTo](imapiprop-copyto.md) в операции копирования, новая папка или контейнер не будут поддерживать таблицу иерархии исходной папки или контейнера. 
  
Следующие свойства составляют необходимый набор столбцов в таблице иерархии:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment)](pidtagcomment-canonical-property.md)  <br/> |**PR_DEPTH** ([PidTagDepth)](pidtagdepth-canonical-property.md)  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)  <br/> |
|**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |**PR_STATUS** ([PidTagStatus)](pidtagstatus-canonical-property.md)  <br/> |
   
 **PR_DISPLAY_NAME** содержит имя контейнера или папки, которые должны отображаться на экране иерархии. 
  
 **PR_ENTRYID** это идентификатор записи, связанный с этим контейнером или папкой. Ожидается, что это долгосрочный идентификатор записи. Клиенты и MAPI могут передать этот идентификатор записи **в OpenEntry,** чтобы открыть контейнер или папку и просмотреть его содержимое, вызывая [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md) 
  
 **PR_DEPTH** это числовая величина, которая указывает уровень отступа для этого контейнера или папки, где нуль является верхним уровнем. Чем глубоко в иерархии находится контейнер или папка, тем выше значение его PR_DEPTH **свойства.** Клиенты используют **PR_DEPTH** для правильного отображения таблицы иерархии, чтобы пользователи могли четко видеть родительские и родительские отношения. Глубина контейнера или папки всегда относительно контейнера или папки, реализующих таблицу иерархии. 
  
 **PR_OBJECT_TYPE** для таблиц иерархии адресных книг MAPI_ABCONT и MAPI_FOLDER для таблиц иерархии папок. 
  
 **PR_DISPLAY_TYPE** это числовая величина, которая связана с отображением контейнера или папки в таблице иерархии. В основном он используется для отображения, чтобы визуально различать типы контейнеров или папок. Многие поставщики store сообщений и адресных книг используют значки для различных типов отображения. Поставщик должен предоставить эти значки; MAPI не дает значения по умолчанию. 
  
MAPI определяет множество значений для PR_DISPLAY_TYPE, некоторые из них допустимы для папок, а другие используются с таблицами иерархии контейнеров адресной книги.  Как правило, для PR_DISPLAY_TYPE  папки установлено значение DT_FOLDER, чтобы указать значок папки по умолчанию, DT_FOLDER_LINK — значок, который представляет ссылку на другую папку, или DT_FOLDER_SPECIAL, чтобы указать значок, характерный для приложения. DT_FOLDER_LINK используется с папками результатов поиска. 
  
Помимо этих необходимых столбцов, таблицы иерархии адресных книг должны включать свойство **PR_CONTAINER_FLAGS.** **PR_CONTAINER_FLAGS** указывает различные атрибуты контейнера в иерархии и используется для отличия одного контейнера от другого. 
  
Необязательным свойством для таблиц иерархии адресной книги является **PR_AB_PROVIDER_ID** ([PidTagAbProviderId).](pidtagabproviderid-canonical-property.md)
  
Таблицы иерархии хранения сообщений включают следующие свойства в требуемом наборе столбцов:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType)](pidtagfoldertype-canonical-property.md)
    
- **PR_SUBFOLDERS** ([PidTagSubfolders)](pidtagsubfolders-canonical-property.md)
    
- **PR_CONTENT_COUNT** ([PidTagContentCount)](pidtagcontentcount-canonical-property.md)
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)
    
Поставщики адресных книг должны поддерживать следующие методы **IMAPITable** в своих реализациях таблиц иерархии, так как они необходимы интегрированной адресной книге MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

