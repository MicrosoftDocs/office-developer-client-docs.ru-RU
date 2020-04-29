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
  
Иерархическая таблица содержит сведения о папках в хранилище сообщений или контейнерах в контейнере адресной книги. Каждая строка таблицы иерархий содержит набор столбцов со сведениями о одной папке или адресной книге. Таблицы иерархий в основном используются клиентами и реализуются поставщиками хранилищ сообщений для отображения дерева папок и вложенных папок, а также реализованных поставщиками адресных книг для отображения дерева контейнеров в адресной книге. Контейнеры, которые не могут содержать подконтейнеры, как указано AB_SUBCONTAINERS в свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), не реализуют таблицу иерархии.
  
Доступ к таблице иерархий можно получить с помощью вызова:
  
- [IMAPIContainer:: жесиерарчитабле](imapicontainer-gethierarchytable.md).
    
    - Также
    
- [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) передает **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) как тег свойства и IID_IMAPITable как идентификатор интерфейса.
    
Контейнеры и папки должны поддерживать оба способа извлечения свойств таблицы. Он неприемлемо для поставщиков услуг, чтобы поддерживать только один способ доступа к этим таблицам, так как клиенты ожидают выбора. 
  
> [!IMPORTANT]
> Поставщики хранилища не гарантируют соблюдение порядка сортировки, указанного для таблиц иерархии. 
  
Вызов **IMAPIProp:: опенпроперти** включает доступ к таблице иерархии, открывая соответствующее свойство, **PR_CONTAINER_HIERARCHY**. Несмотря на то что **PR_CONTAINER_HIERARCHY** невозможно получить с помощью метода [IMAPIProp::-PROPS](imapiprop-getprops.md) папки или контейнера, он включается в массив тегов свойств, который возвращается методом [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_HIERARCHY** также можно использовать для включения или исключения таблицы иерархии из операции копирования. Если клиент указывает **PR_CONTAINER_HIERARCHY** в параметре *лпексклудепропс* для [IMAPIProp:: CopyTo](imapiprop-copyto.md) в операции копирования, Новая папка или контейнер не будет поддерживать таблицу иерархии исходной папки или контейнера. 
  
Следующие свойства составляют обязательный набор столбцов в таблице иерархий:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** содержит имя контейнера или папки, которые должны отображаться в иерархии. 
  
 **PR_ENTRYID** — это идентификатор записи, связанный с этим контейнером или папкой. Он должен быть долгосрочным идентификатором записи. Клиенты и MAPI могут передать этот идентификатор записи в **OpenEntry** , чтобы открыть контейнер или папку и просмотреть ее содержимое, вызвав [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** — это числовое значение, указывающее уровень отступа для этого контейнера или папки с нулевым значением верхнего уровня. На более глубоком уровне в иерархии контейнер или папка находится более высокое значение свойства **PR_DEPTH** . Клиенты используют свойство **PR_DEPTH** для отображения таблицы иерархии соответствующим образом, чтобы пользователи могли ясно видеть родительские и дочерние связи. Глубина контейнера или папки всегда относится к контейнеру или папке, реализующей таблицу иерархии. 
  
 **PR_OBJECT_TYPE** всегда имеет значение MAPI_ABCONT для таблиц иерархии адресных книг и MAPI_FOLDER для таблиц иерархии папок. 
  
 **PR_DISPLAY_TYPE** — это числовое значение, которое соответствует способу отображения контейнера или папки в таблице иерархий. Он используется в основном для отображения, чтобы визуально различать типы контейнеров или папок. Многие поставщики хранилищ сообщений и адресных книг используют значки для различных типов дисплеев. Поставщик должен предоставить эти значки. MAPI не предоставляет значения по умолчанию. 
  
MAPI определяет множество значений для **PR_DISPLAY_TYPE**, которые являются допустимыми для папок и других элементов, используемых с таблицами иерархии контейнеров адресных книг. Как правило, **PR_DISPLAY_TYPE** папки имеет значение DT_FOLDER, указывающее значок папки по умолчанию, DT_FOLDER_LINK, чтобы указать значок, представляющий ссылку на другую папку, или DT_FOLDER_SPECIAL, чтобы указать значок, зависящий от конкретного приложения. DT_FOLDER_LINK используется с папками результатов поиска. 
  
В дополнение к этим обязательным столбцам таблицы иерархии адресных книг должны включать свойство **PR_CONTAINER_FLAGS** . **PR_CONTAINER_FLAGS** указывает различные атрибуты контейнера в иерархии и используется для различения одного контейнера от другого. 
  
Необязательное свойство для таблиц иерархии адресных книг — это свойство **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
В таблицах иерархий хранилища сообщений эти свойства включаются в обязательный набор столбцов:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Поставщики адресных книг должны поддерживать следующие методы **IMAPITable** в своих реализациях таблиц иерархии, так как они необходимы для встроенной АДРЕСНОЙ книги MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

