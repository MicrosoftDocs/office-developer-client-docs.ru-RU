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
ms.openlocfilehash: 491381c771cae65e682acc8033b6558523847d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435588"
---
# <a name="contents-tables"></a>Таблицы содержимого

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица содержимого содержит сведения об объектах в контейнере MAPI. Поставщики адресных книг реализуют таблицы содержимого для каждого из контейнеров, а хранилище сообщений и удаленные поставщики транспорта реализуют таблицы содержимого для своих папок. В таблице содержимого контейнера адресной книги представлены сведения об объектах обмена сообщениями и списках рассылки, а в таблице содержимого папки приведена информация о сообщениях. Таблицы содержимого используются в основном клиентскими приложениями. 
  
Существует два типа таблиц содержимого папок:
  
- Стандартные таблицы содержимого содержат стандартные сообщения — сообщения, которые могут быть переданы и сделаны видимыми для пользователя. 
    
- Связанные таблицы содержимого содержат скрытые, несохраняемые сведения, созданные клиентом для определенной цели, например для хранения альтернативного представления стандартного сообщения. Связанные сведения создаются путем передачи флага MAPI_ASSOCIATED на вызов [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . 
    
Таблицы содержимого большинства контейнеров адресных книг и многих папок не поддерживают сортировку по категориям. 
  
Доступ к таблице содержимого можно получить с помощью вызова:
  
- [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md).
    
    - Также
    
- [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) с **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) или **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) (только папки), указанные в качестве тега свойства и IID_IMAPITable в качестве идентификатора интерфейса.
    
Поставщики хранилищ сообщений и адресных книг должны поддерживать оба способа извлечения свойств таблицы. Он неприемлемо для поставщиков, поддерживающих только один способ доступа к этим таблицам, так как клиенты ожидают выбора. 
  
 **Жетконтентстабле** принимает в качестве входных данных несколько флагов, определяющих предпочтения. Если этот параметр установлен, флаг MAPI_ASSOCIATED получает связанную таблицу содержимого. Так как некоторые папки не поддерживают связанное содержимое, и клиенты не могут заранее определить это время, **жетконтентстабле** иногда возвращает ошибку MAPI_E_NO_SUPPORT при запросе связанной таблицы содержимого. 
  
Флаг MAPI_DEFERRED_ERRORS указывает разработчику таблицы, что все ошибки, обнаруженные во время вызова, не нужно сообщать до появления следующего времени. 
  
Вызов **IMAPIProp:: опенпроперти** включает доступ к таблице содержимого, открывая соответствующее свойство, **PR_CONTAINER_CONTENTS** для таблиц содержимого адресных книг и таблиц содержимого стандартных папок, а **PR_FOLDER_ASSOCIATED_CONTENTS** для связанных таблиц содержимого. Несмотря на то, что эти свойства не могут быть получены с помощью метода [IMAPIProp::-PROPS](imapiprop-getprops.md) папки или контейнера, они включаются в массив тегов свойств, который возвращается методом [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_CONTENTS** также можно использовать для включения или исключения таблицы содержимого из операции копирования. Если клиент указывает **PR_CONTAINER_CONTENTS** в параметре *лпексклудепропс* для **IMAPIProp:: CopyTo** в операции копирования, Новая папка или контейнер не будет поддерживать таблицу содержимого исходной папки или контейнера. 
  
В таблицах контейнеров и папок адресной книги имеется длинный список обязательных столбцов — столбцов, которые клиенты могут ожидать после получения таблицы из **жетконтентстабле** или **опенпроперти**. Поставщики могут добавлять в этот обязательный набор, если это необходимо, а клиенты, с помощью метода **метода SetColumns** , также могут запрашивать изменения. 
  
Для каждого из типов таблиц содержимого требуются следующие столбцы:
  
|**Обязательный столбец**|**Таблица типов содержимого**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Таблицы контейнеров адресных книг  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Таблицы контейнеров адресных книг  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Таблицы папок хранилища сообщений  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Таблицы контейнеров адресных книг  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Все таблицы содержимого  <br/> |
|**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |Все таблицы содержимого  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Таблицы папок хранилища сообщений  <br/> |
|**PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))  <br/> |Таблицы папок хранилища сообщений  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |Таблицы удаленных транспортных папок  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Все таблицы содержимого  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Таблицы папок хранилища сообщений  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Таблицы папок адресных книг и папок хранилища сообщений  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Таблицы удаленных транспортных папок  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Таблицы папок хранилища сообщений  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Таблицы папок хранилища сообщений  <br/> |
   
Идентификатор записи, доступный для каждой строки, может быть коротким или долгосрочным идентификатором записи в зависимости от реализации таблицы. Краткосрочные идентификаторы записей обычно используются в ситуациях, когда производительность является неисправностью. Для доступа к соответствующему объекту можно использовать любой тип идентификатора записи. 
  
Таблицы содержимого также имеют набор необязательных столбцов, которые обычно включаются поставщиками услуг в их реализациях. Эти необязательные столбцы:
  
|**Необязательный столбец**|**Таблица типов содержимого**|
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Таблицы папок хранилища сообщений  <br/> |
|**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |Стандартные таблицы содержимого папки  <br/> |
|**PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))  <br/> |Стандартные таблицы содержимого папки  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |Таблицы папок хранилища сообщений  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Таблицы контейнеров адресных книг  <br/> |
|**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Таблицы контейнеров адресных книг  <br/> |
|**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))  <br/> |Таблицы контейнеров адресных книг  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Все таблицы содержимого папки  <br/> |
|**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))  <br/> |Таблицы контейнеров адресных книг  <br/> |
   
Поставщики хранилища сообщений также должны включать **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) только для таблиц содержимого папок результатов поиска.
  
Именованные свойства можно добавить в набор столбцов таблицы содержимого папки только в том случае, если все сообщения в папке имеют одинаковую подпись сопоставления, то есть одно сопоставление имен свойств с идентификаторами свойств. Таблицы содержимого папок должны поддерживать добавление определенных свойств класса сообщений в набор столбцов, если они поддерживают создание произвольных сообщений в папке.
  
Клиенты могут сохранить порядок сортировки по умолчанию для таблицы содержимого папки, вызвав его метод [IMAPIFolder:: савеконтентссорт](imapifolder-savecontentssort.md) . Если для вызова указан флаг RECURSIVE_SORT, то порядок сортировки можно применить ко всем вложенным папкам в папке. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

