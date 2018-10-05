---
title: IABContainer IMAPIContainer
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392188"
---
# <a name="iabcontainer--imapicontainer"></a>IABContainer : IMAPIContainer

**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к адресной книге контейнеров. MAPI и клиентских приложениях вызвать методы **IABContainer** выполнять разрешение имен и создание, копирование и удаление получателей. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Адресной книги контейнер объектов  <br/> |
|Реализовано в:  <br/> |Поставщиками адресных книг  <br/> |
|Вызывающая сторона:  <br/> |MAPI и клиентских приложениях  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IABContainer  <br/> |
|Тип указателя:  <br/> |LPABCONT  <br/> |
|Модель транзакций:  <br/> |В транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[CreateEntry](iabcontainer-createentry.md) <br/> |Создает новый объект, который может быть обмена сообщениями пользователя, в список рассылки или другой контейнер.  <br/> |
|[CopyEntries](iabcontainer-copyentries.md) <br/> |Копирует один или несколько операций, пользователи обычно обмена мгновенными сообщениями или списки рассылки.  <br/> |
|[Внешнее](iabcontainer-deleteentries.md) <br/> |Удаляет один или несколько операций, обычно системы обмена сообщениями пользователи, списков рассылки или других контейнеров.  <br/> |
|[ResolveNames](iabcontainer-resolvenames.md) <br/> |Выполняет разрешение имен для одного или нескольких получателей записей.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
|**Дополнительные свойства**|**Access**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Интерфейс **IABContainer** косвенно наследуется от интерфейс [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) через [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md) и [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейсов. Интерфейс **IABContainer** внедряемые поставщиками адресной книги. 
  
В контейнер адресной книги может быть любое количество обмена сообщениями объектов-пользователей, списков рассылки и других контейнеров адресной книги. Как и в любой контейнер клиентов или поставщиков услуг можно использовать контейнер адресной книги для открытия один из его записи или для получения таблицы иерархии или таблицу содержимого. Адресная книга также предоставить разрешение имен и контейнеры, в зависимости от поставщика, возможность добавления, удаления или изменения записей.
  
MAPI определяет контейнер специальные адресной книги, называется Личная адресная книга (PAB-файла), в котором содержатся элементы, скопированные из других контейнеров. Адресной книги всегда можно изменить. Пользователи обычно заполнения их адресной книги с записями, обозначение получателей, с которыми они наиболее часто общаетесь. Адресной книги, удерживая одноразовых адресов и новых получателей еще не являющихся частью любой контейнер адресной книги.
  
## <a name="see-also"></a>См. также

- [Интерфейсы MAPI](mapi-interfaces.md)

