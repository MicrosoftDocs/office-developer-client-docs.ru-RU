---
title: Contents Tables
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 491381c771cae65e682acc8033b6558523847d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435588"
---
# <a name="contents-tables"></a>Contents Tables

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В таблице содержимого содержатся сведения об объектах в контейнере MAPI. Поставщики адресных книг реализуют таблицы содержимого для каждого из своих контейнеров, а поставщики хранения сообщений и удаленных поставщиков транспорта реализуют таблицы содержимого для своих папок. В таблице содержимого контейнера адресной книги перечислены сведения об объектах пользователей сообщений и списков рассылки, а в таблице содержимого папки перечислены сведения о сообщениях. Таблицы содержимого в основном используются клиентских приложений. 
  
Существует два типа таблиц содержимого папок:
  
- Стандартные таблицы содержимого содержат стандартные сообщения, которые могут передаваться и делаться видимыми пользователю. 
    
- Связанные таблицы содержимого содержат скрытые непередаваемые сведения, созданные клиентом для определенной цели, например для хранения альтернативного представления стандартного сообщения. Связанные сведения создаются путем передачи флага MAPI_ASSOCIATED в вызов [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) 
    
Таблицы содержимого большинства контейнеров адресной книги и многих папок не поддерживают сортировку по категориям. 
  
Доступ к таблице содержимого можно получить с помощью вызова:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Или -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)или **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)(только для папок), указанных в качестве тега свойства и IID_IMAPITable в качестве идентификатора интерфейса.
    
Поставщики хранения сообщений и адресных книг должны поддерживать оба метода искомые свойства таблицы. Недопустимо, чтобы поставщики поддерживают только один из способов доступа к этим таблицам, так как клиенты ожидают выбора. 
  
 **GetContentsTable** принимает в качестве входных несколько флагов, которые определяют параметры. При этом флаг MAPI_ASSOCIATED извлекает связанную таблицу содержимого. Так как некоторые папки не поддерживают связанное содержимое и клиенты не могут определить это заранее, **GetContentsTable** иногда возвращает ошибку MAPI_E_NO_SUPPORT при запросе связанной таблицы содержимого. 
  
Флаг MAPI_DEFERRED_ERRORS указывает реализации таблицы, что все ошибки, которые произошли во время вызова, не должны быть указаны до некоторого времени. 
  
Вызов  **IMAPIProp::OpenProperty** включает доступ к таблице содержимого путем открытия соответствующего свойства, **PR_CONTAINER_CONTENTS** для таблиц содержимого адресной книги и стандартных таблиц содержимого папок и PR_FOLDER_ASSOCIATED_CONTENTS для связанных таблиц содержимого. Хотя ни одно, ни одно из этих свойств не может быть извлечено с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) папки или контейнера, они включаются в массив тегов свойств, возвращаемого методом [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_CONTENTS** также можно использовать для включаемой или исключаемой из операции копирования таблицы содержимого. Если клиент указывает  PR_CONTAINER_CONTENTS в параметре *lpExcludeProps* для **IMAPIProp::CopyTo** в операции копирования, новая папка или контейнер не будет поддерживать таблицу содержимого исходной папки или контейнера. 
  
Таблицы содержимого контейнеров и папок адресной книги имеют длительный список необходимых столбцов — столбцов, которые клиенты могут ожидать получить после получения таблицы из **GetContentsTable** или **OpenProperty.** Поставщики могут при необходимости добавить этот набор, а клиенты с помощью метода **SetColumns** также могут запросить изменения. 
  
Для каждого типа таблиц содержимого требуются столбцы:
  
|**Необходимый столбец**|**Тип таблицы содержимого**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |Все таблицы содержимого  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments)](pidtaghasattachments-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Все таблицы содержимого  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature)](pidtagmappingsignature-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)  <br/> |Таблицы папок удаленного транспорта  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize)](pidtagmessagesize-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Все таблицы содержимого  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId)](pidtagparententryid-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)  <br/> |Таблицы папок контейнера и хранения сообщений в адресной книге  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Таблицы папок удаленного транспорта  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey)](pidtagstorerecordkey-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
   
Идентификатор записи, доступный в каждой строке, может быть краткосрочным или долгосрочным идентификатором записи в зависимости от реализации таблицы. Краткосрочные идентификаторы записей обычно используются в ситуациях, когда производительность является проблемой. Для доступа к соответствующему объекту можно использовать любой тип идентификатора записи. 
  
В таблицах содержимого также есть набор столбцов, которые являются необязательными, но часто включаются поставщиками служб в свои реализации. Эти необязательные столбцы:
  
|**Необязательный столбец**|**Тип таблицы содержимого**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount)](pidtagcontentcount-canonical-property.md)  <br/> |Стандартные таблицы содержимого папок  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)  <br/> |Стандартные таблицы содержимого папок  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance)](pidtagimportance-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_PRIORITY** ([PidTagPriority)](pidtagpriority-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity)](pidtagsensitivity-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
   
Поставщики содержимого для хранения **сообщений также должны включать PR_PARENT_DISPLAY** ([PidTagParentDisplay)](pidtagparentdisplay-canonical-property.md)только для таблиц содержимого папок результатов поиска.
  
Именные свойства можно добавлять в набор столбцов таблицы содержимого папки, только если все сообщения в папке имеют одинаковые подписи сопоставления, то есть одно и то же сопоставление имен свойств с идентификаторами свойств. Таблицы содержимого папок должны поддерживать добавление свойств класса сообщений в набор столбцов, если они поддерживают создание произвольных сообщений в папке.
  
Клиенты могут сохранить порядок сортировки по умолчанию для таблицы содержимого папки, вызывая метод [IMAPIFolder::SaveContentsSort.](imapifolder-savecontentssort.md) Если флаг RECURSIVE_SORT указан в вызове, можно применить порядок сортировки для всех вложенных папок в папке. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

