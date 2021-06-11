---
title: Таблицы контента
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
# <a name="contents-tables"></a>Таблицы контента

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В таблице содержимого содержатся сведения о объектах в контейнере MAPI. Поставщики адресных книг реализуют таблицы контента для каждого из контейнеров, а поставщики сообщений и поставщики удаленного транспорта реализуют таблицы контента для своих папок. В таблице содержимого контейнера адресной книги перечислены сведения о пользователях и объектах списка рассылки сообщений, а в таблице содержимого папки перечислены сведения о своих сообщениях. Таблицы контента используются в основном клиентских приложений. 
  
Существует два типа таблиц содержимого папок:
  
- Стандартные таблицы контента содержат стандартные сообщения — сообщения, которые могут передаваться и делаться видимыми пользователю. 
    
- Связанные таблицы контента содержат скрытые, непередаваемые сведения, созданные клиентом для определенной цели, например для хранения альтернативного представления стандартного сообщения. Связанные сведения создаются путем передачи флага MAPI_ASSOCIATED на вызов [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) 
    
Таблицы содержимого большинства контейнеров адресной книги и многих папок не поддерживают сортировку по категориям. 
  
К таблице содержимого можно получить доступ по вызову:
  
- [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
    - Или -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **с PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)или **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)(только для папок), указанных как тег свойства и IID_IMAPITable как идентификатор интерфейса.
    
Поставщики хранения сообщений и поставщики адресных книг должны поддерживать оба метода для ирисовки свойств таблицы. Для поставщиков недопустимо поддерживать только один способ доступа к этим таблицам, так как клиенты ожидают выбора. 
  
 **GetContentsTable** принимает в качестве ввода несколько флагов с указанием предпочтений. При наборе флаг MAPI_ASSOCIATED извлекает связанную таблицу содержимого. Так как некоторые папки не поддерживают связанное содержимое, и клиенты не могут определить это заранее, **GetContentsTable** иногда возвращает ошибку MAPI_E_NO_SUPPORT при запросе связанной таблицы содержимого. 
  
Флаг MAPI_DEFERRED_ERRORS указывает на то, что любые ошибки, с которыми столкнулся во время вызова, не должны быть указаны до более позднего времени. 
  
Вызов в **IMAPIProp::OpenProperty** включает доступ к таблице содержимого, открыв ее соответствующее свойство, **PR_CONTAINER_CONTENTS** таблицы контента адресной книги и стандартные таблицы содержимого папок и PR_FOLDER_ASSOCIATED_CONTENTS для связанных таблиц **содержимого.** Хотя эти свойства не могут быть извлечены с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) папки или контейнера, они включены в массив тегов свойств, возвращаемого методом [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_CONTENTS** можно также включить или исключить таблицу содержимого из операции копирования. Если клиент указывает  PR_CONTAINER_CONTENTS в параметре *lpExcludeProps* для **IMAPIProp::CopyTo** в операции копирования, новая папка или контейнер не будут поддерживать таблицу содержимого исходной папки или контейнера. 
  
Таблицы содержимого контейнера и папки адресной книги имеют длительный список необходимых столбцов — столбцов, которые клиенты могут ожидать, чтобы быть доступными после получения таблицы **из GetContentsTable** или **OpenProperty.** Поставщики могут добавить в этот необходимый набор при необходимости и клиенты с помощью **метода SetColumns** также могут запрашивать изменения. 
  
Необходимые столбцы для каждого из типов таблиц содержимого:
  
|**Необходимый столбец**|**Тип таблицы содержимого**|
|:-----|:-----|
|**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_DISPLAY_CC** [(PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_DISPLAY_TO** [(PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |Все таблицы содержимого  <br/> |
|**PR_HASATTACH** [(PidTagHasAttachments)](pidtaghasattachments-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |Все таблицы содержимого  <br/> |
|**PR_LAST_MODIFICATION_TIME** [(PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_MAPPING_SIGNATURE** [(PidTagMappingSignature)](pidtagmappingsignature-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** [(PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)  <br/> |Таблицы папки удаленного транспорта  <br/> |
|**PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_MESSAGE_SIZE** [(PidTagMessageSize)](pidtagmessagesize-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Все таблицы содержимого  <br/> |
|**PR_PARENT_ENTRYID** [(PidTagParentEntryId)](pidtagparententryid-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Таблицы папки контейнера адресной книги и папки для хранения сообщений  <br/> |
|**PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)  <br/> |Таблицы папки удаленного транспорта  <br/> |
|**PR_STORE_ENTRYID** [(PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_STORE_RECORD_KEY** [(PidTagStoreRecordKey)](pidtagstorerecordkey-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
   
Идентификатор записи, доступный в каждой строке, может быть краткосрочным или долгосрочным идентификатором входа в зависимости от реализации таблицы. Краткосрочные идентификаторы записей обычно используются в ситуациях, когда производительность является проблемой. Для доступа к соответствующему объекту можно использовать любой тип идентификатора входа. 
  
В таблицах контента также есть набор столбцов, которые являются необязательными, но обычно включаются поставщиками услуг в их реализации. Эти необязательные столбцы:
  
|**Необязательный столбец**|**Тип таблицы содержимого**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** [(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_CONTENT_COUNT** [(PidTagContentCount)](pidtagcontentcount-canonical-property.md)  <br/> |Таблицы содержимого стандартных папок  <br/> |
|**PR_CONTENT_UNREAD** [(PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)  <br/> |Таблицы содержимого стандартных папок  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Таблицы папок в хранилище сообщений  <br/> |
|**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_IMPORTANCE** [(PidTagImportance)](pidtagimportance-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** [(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_PRIORITY** [(PidTagPriority)](pidtagpriority-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_SEND_RICH_INFO** [(PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Таблицы контейнеров адресной книги  <br/> |
|**PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_SENSITIVITY** [(PidTagSensitivity)](pidtagsensitivity-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)  <br/> |Все таблицы содержимого папок  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** [(PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)  <br/> |Таблицы контейнеров адресной книги  <br/> |
   
Поставщики магазинов сообщений также должны **включать PR_PARENT_DISPLAY** [(PidTagParentDisplay)](pidtagparentdisplay-canonical-property.md)только для таблиц контента папок с результатами поиска.
  
Названные свойства могут быть добавлены в столбец набора содержимого папки только в том случае, если все сообщения в папке имеют ту же подпись сопоставления, то есть одно и то же сопоставление имен свойств с идентификаторами свойств. Таблицы содержимого папок должны поддерживать добавление свойств класса сообщений в набор столбцов, если они поддерживают создание произвольных сообщений в папке.
  
Клиенты могут сохранить порядок сортировки по умолчанию для таблицы содержимого папки, позвонив в [метод IMAPIFolder::SaveContentsSort.](imapifolder-savecontentssort.md) Если флаг RECURSIVE_SORT указан на вызове, можно сделать заказ сортировки, чтобы применить его во всех подмостках в папке. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

