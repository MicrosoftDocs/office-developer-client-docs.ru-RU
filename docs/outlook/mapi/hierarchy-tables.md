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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Таблица иерархии содержит сведения о папках в хранилище сообщений или контейнерах в контейнере адресной книги. Каждая строка таблицы иерархии содержит набор столбцов с информацией об одной папке или контейнере адресной книги. Таблицы иерархии в основном используются клиентами и реализуются поставщиками магазинов сообщений, чтобы показать дерево папок и подмостков и реализованы поставщиками адресных книг, чтобы показать дерево контейнеров в адресной книге. Контейнеры, которые не могут удерживать подконтейнеры, как указывает отсутствие флага AB_SUBCONTAINERS в свойстве **PR_CONTAINER_FLAGS** [(PidTagContainerFlags),](pidtagcontainerflags-canonical-property.md)не реализуют таблицу иерархии.
  
К таблице иерархии можно получить доступ по вызову:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Или -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_CONTAINER_HIERARCHY** [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)в качестве тега свойства и IID_IMAPITable как идентификатор интерфейса.
    
Контейнеры и папки должны поддерживать оба метода для ирисовки свойств таблицы. Для поставщиков услуг недопустимо поддерживать только один способ доступа к этим таблицам, так как клиенты ожидают выбора. 
  
> [!IMPORTANT]
> Поставщики магазинов не гарантируют честь набора сортировки, заданного для таблиц иерархии. 
  
Вызов в **IMAPIProp::OpenProperty** включает доступ к таблице иерархии, открыв соответствующее свойство **PR_CONTAINER_HIERARCHY**. Хотя **PR_CONTAINER_HIERARCHY** не удается получить с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) папки или контейнера, он включен в массив тегов свойств, возвращаемого методом [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_HIERARCHY** можно также включить или исключить таблицу иерархии из операции копирования. Если клиент указывает  PR_CONTAINER_HIERARCHY в параметре *lpExcludeProps* для [IMAPIProp::CopyTo](imapiprop-copyto.md) в операции копирования, новая папка или контейнер не будут поддерживать таблицу иерархии исходной папки или контейнера. 
  
Следующие свойства составляют необходимый столбец, установленный в таблице иерархии:
  
|||
|:-----|:-----|
|**PR_COMMENT** [(PidTagComment)](pidtagcomment-canonical-property.md)  <br/> |**PR_DEPTH** [(PidTagDepth)](pidtagdepth-canonical-property.md)  <br/> |
|**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)  <br/> |
|**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |
|**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |**PR_STATUS** [(PidTagStatus)](pidtagstatus-canonical-property.md)  <br/> |
   
 **PR_DISPLAY_NAME** содержит имя контейнера или папки, которые должны отображаться на экране иерархии. 
  
 **PR_ENTRYID** — это идентификатор записи, связанный с этим контейнером или папкой. Предполагается, что это будет долгосрочный идентификатор записи. Клиенты и MAPI могут передать этот идентификатор записи **в OpenEntry,** чтобы открыть контейнер или папку и просмотреть его содержимое, позвонив [в IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** — это числовая величина, которая указывает уровень отступа для этого контейнера или папки с нулем верхнего уровня. Чем глубже в иерархии находится контейнер или папка, тем выше значение **для PR_DEPTH** свойства. Клиенты используют **свойство PR_DEPTH** для отображения таблицы иерархии надлежащим образом, чтобы пользователи могли четко видеть родительские и детские отношения. Глубина контейнера или папки всегда относительно контейнера или папки, реализующих таблицу иерархии. 
  
 **PR_OBJECT_TYPE** всегда MAPI_ABCONT таблицы иерархии адресных книг и MAPI_FOLDER таблицы иерархии папок. 
  
 **PR_DISPLAY_TYPE** — это числовая величина, связанная с отображением контейнера или папки в таблице иерархии. Он используется в основном для отображения, чтобы визуально различать типы контейнеров или папок. Многие поставщики хранения сообщений и адресных книг используют значки для различных типов отображения. Поставщик должен предоставить эти значки; MAPI не поставляет по умолчанию. 
  
MAPI определяет множество значений для **PR_DISPLAY_TYPE,** некоторые из них допустимы для папок и другие, которые используются в таблицах иерархии контейнеров адресной книги. Обычно для PR_DISPLAY_TYPE папки  DT_FOLDER значок папки по умолчанию, DT_FOLDER_LINK указывает значок, который представляет ссылку на другую папку, или DT_FOLDER_SPECIAL, чтобы указать значок, характерный для приложения. DT_FOLDER_LINK используется в папках результатов поиска. 
  
Помимо этих необходимых столбцов, таблицы иерархии адресных книг должны включать **свойство PR_CONTAINER_FLAGS.** **PR_CONTAINER_FLAGS** указывает различные атрибуты о контейнере в иерархии и используется для отличия одного контейнера от другого. 
  
Необязательным свойством для таблиц иерархии адресных книг является **свойство PR_AB_PROVIDER_ID** [(PidTagAbProviderId).](pidtagabproviderid-canonical-property.md)
  
Таблицы иерархии в хранилище сообщений включают эти свойства в требуемом наборе столбцов:
  
- **PR_FOLDER_TYPE** [(PidTagFolderType)](pidtagfoldertype-canonical-property.md)
    
- **PR_SUBFOLDERS** [(PidTagSubfolders)](pidtagsubfolders-canonical-property.md)
    
- **PR_CONTENT_COUNT** [(PidTagContentCount)](pidtagcontentcount-canonical-property.md)
    
- **PR_CONTENT_UNREAD** [(PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)
    
Поставщики адресных книг должны поддерживать следующие методы **IMAPITable** в реализации таблицы иерархии, так как они необходимы интегрированной адресной книге MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

