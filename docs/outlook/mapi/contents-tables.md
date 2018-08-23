---
title: Таблицы содержимого
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b8efb4e-b5be-41b8-81bb-9aa1da421433
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 923fd527eb7d04b31f15e6d8673e2e964fa0d1ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585642"
---
# <a name="contents-tables"></a>Таблицы содержимого

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержимое таблицы содержит сведения об объектах в контейнере MAPI. Содержимое таблицы для каждого из их контейнеров, реализуемые поставщиками адресных книг и поставщиков удаленных транспорта и хранение сообщений реализации содержимое таблицы для своих папок. В таблице содержимого контейнера адресной книги приведены сведения о его обмена сообщениями пользователя и распространения списка объектов, во время в таблице содержимое папки приведены сведения о его сообщения. Содержимое таблицы используются в основном в клиентских приложениях. 
  
Существует два типа таблиц содержимое папки.
  
- Стандартный содержимое таблицы содержат стандартные сообщения — сообщений, отправленных и сделать видимым для пользователя. 
    
- Связанное содержимое таблицы содержат скрытые, не являющиеся передаваемого сведения, созданные клиента для определенной цели, такие как для хранения альтернативное представление стандартные сообщения. Сведения о нем создается путем передачи флаг MAPI_ASSOCIATED для вызова [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . 
    
Содержимое, которое не поддерживают таблицы большинством контейнеров адресной книги и большое число папок категории сортировки. 
  
Содержимое таблицы может осуществляться путем вызова:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Или -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) или **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (только для папок) указан как свойство tag и ИД интерфейса _IMAPITable идентификатор интерфейса.
    
Хранение сообщений и адресной книги поставщиков должна поддерживать обоих методов для получения свойства таблицы. Он недопустим для поставщиков для поддержки только один из способов доступа к эти таблицы так, как ожидается, что выбор клиентов. 
  
 **GetContentsTable** принимает в качестве входных данных несколько флаги, определяющие параметры. Если задано, флаг MAPI_ASSOCIATED извлекает таблицу связанного содержимого. Так как некоторые папки не поддерживают связанное содержимое и нет возможности для клиентов определить это заранее, **GetContentsTable** в некоторых случаях возвращает ошибку MAPI_E_NO_SUPPORT при запросе таблицу связанного содержимого. 
  
Флаг MAPI_DEFERRED_ERRORS указывает для реализации таблицу, любые ошибки во время вызова не требуется быть выявлены до впоследствии. 
  
Вызов **IMAPIProp::OpenProperty** включает в себя доступ к таблице содержимое, открыв его соответствующего свойства **PR_CONTAINER_CONTENTS** для адресной книги содержимое таблиц и таблиц содержимое стандартные папки и **PR_FOLDER_ASSOCIATED_ СОДЕРЖИМОЕ** для связанных таблиц содержимое. Несмотря на то что ни один из них или этих свойств можно получить через папку или метод [IMAPIProp::GetProps](imapiprop-getprops.md) контейнера, их необходимо включить в массиве тега свойства, который возвращается методом [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_CONTENTS** можно также использовать для включено или исключено содержимое таблицы из операцию копирования. Если клиент указывает **PR_CONTAINER_CONTENTS** с помощью параметра *lpExcludeProps* для **IMAPIProp::CopyTo** в операцию копирования, новую папку или контейнера не будут поддерживаться в таблице содержимое исходной папки или контейнера. 
  
Адресной книги контейнер и папки содержимое таблицы имеют длинного списка обязательные столбцы — столбцов, которые будут доступны после их получения таблицы из **GetContentsTable** или **OpenProperty**может предполагать клиентов. Поставщики можно добавить этот необходимый набор при необходимости и клиентами через метод **метода SetColumns** также могут запрашивать изменения. 
  
Обязательные столбцы для каждого из типов содержимого таблицы являются:
  
|**Обязательный столбец**|**Тип содержимого таблицы**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Книга контейнер таблицы адресов  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Книга контейнер таблицы адресов  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Таблицы папки хранилища сообщений  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Книга контейнер таблицы адресов  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Все содержимое таблицы  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Все содержимое таблицы  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Таблицы папки хранилища сообщений  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Таблицы папки хранилища сообщений  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Папка таблиц удаленного транспорта  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Все содержимое таблицы  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Таблицы папки хранилища сообщений  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Контейнер адресной книги и сообщения хранить папки таблиц  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Папка таблиц удаленного транспорта  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Таблицы папки хранилища сообщений  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Таблицы папки хранилища сообщений  <br/> |
   
Идентификатор записи, доступных в каждой строке может быть short или долгосрочные идентификатор записи, в зависимости от реализации таблицы. Краткосрочные идентификаторы записей обычно используются в ситуациях, где проблемы. В каждом объекте идентификатор записи можно использовать для доступа к соответствующего объекта. 
  
Содержимое таблицы имеется набор столбцов, которые являются необязательно, но обычно включены поставщиками услуг в их реализации. Эти дополнительные столбцы — это:
  
|**Дополнительный столбец**|**Тип содержимого таблицы**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Таблицы папки хранилища сообщений  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Стандартные папки содержимого таблицы  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Стандартные папки содержимого таблицы  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Таблицы папки хранилища сообщений  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Книга контейнер таблицы адресов  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Книга контейнер таблицы адресов  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Книга контейнер таблицы адресов  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Книга контейнер таблицы адресов  <br/> |
   
Поставщики хранилища сообщений должен также включать **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) для содержимого таблиц на результат поиска папок.
  
Именованные свойства могут быть добавлены набор столбцов таблицы содержимое папки только в том случае, если все сообщения в папке совпадают сопоставления, то есть одно сопоставление имен свойств для идентификаторов свойств. Если они поддерживают создание произвольных сообщения в папке, в таблицах содержимое папки должен поддерживать задать определенные свойства для столбца, Добавление класса сообщения.
  
Клиенты можно сохранить порядок сортировки по умолчанию для таблицы содержимое папки путем вызова метода [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md) . Если флаг RECURSIVE_SORT указан на звонок, порядок сортировки может быть установлено для всех вложенных папок в папке. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

