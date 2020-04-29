---
title: Иабконтаинер IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer
api_type:
- COM
ms.assetid: 1f5ce6e0-b79a-4da2-b014-8c00cd72912e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0905fbe2ba584aef49c50152aaf448267d477c10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348960"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к контейнерам адресной книги. MAPI и клиентские приложения вызывают методы **иабконтаинер** , чтобы выполнять разрешение имен, а также создавать, копировать и удалять получателей. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объекты контейнера адресной книги  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |MAPI и клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IABContainer  <br/> |
|Тип указателя:  <br/> |лпабконт  <br/> |
|Модель транзакции:  <br/> |Транзакции  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[креатинтри](iabcontainer-createentry.md) <br/> |Создает новую запись, которая может быть пользователем обмена сообщениями, списком рассылки или другим контейнером.  <br/> |
|[копентриес](iabcontainer-copyentries.md) <br/> |Копирует одну или несколько записей, как правило, пользователи системы обмена сообщениями или списки рассылки.  <br/> |
|[делетинтриес](iabcontainer-deleteentries.md) <br/> |Удаляет одну или несколько записей, как правило, пользователи системы обмена сообщениями, списки рассылки или другие контейнеры.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Выполняет разрешение имен для одной или нескольких записей получателей.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
|**Необязательные свойства**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Интерфейс **иабконтаинер** наследует косвенно от интерфейса [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) через интерфейс [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) и [IMAPIProp: интерфейс IUnknown](imapipropiunknown.md) . Поставщики адресных книг реализуют интерфейс **иабконтаинер** . 
  
В контейнере адресной книги может существовать любое количество объектов User Messaging, списков рассылки и других контейнеров адресных книг. Как и в случае с любым контейнером, клиенты или поставщики услуг могут использовать контейнер адресной книги для открытия одной из записей или для получения таблицы иерархии или таблицы контента. Контейнеры адресных книг также обеспечивают разрешение имен и, в зависимости от поставщика, возможность добавлять, удалять или изменять записи.
  
MAPI определяет специальный контейнер адресной книги, который называется личной адресной книгой (PAB), которая содержит записи, скопированные из других контейнеров. Адрес личной адресной книги всегда является изменяемым. Обычно пользователи заполняют личную адресную книгу записями, указывающими получателям, с которыми они чаще всего часто обмениваются данными. Адресная книга также может содержать один и тот же адрес, а новые получатели не являются частью какого бы то ни было контейнера адресной книги.
  
## <a name="see-also"></a>См. также

- [Интерфейсы MAPI](mapi-interfaces.md)

