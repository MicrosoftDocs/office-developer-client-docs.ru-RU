---
title: Написание средства удаленного просмотра
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325664"
---
# <a name="writing-a-remote-viewer"></a>Написание средства удаленного просмотра

**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаленный зритель — это окно в клиентских приложениях, которое обеспечивает контролируемый доступ к сообщениям, хранимым на другом компьютере. Этот управляемый доступ может работать на медленной связи. Вместо получения полного выбора доступных сообщений каждый раз, когда пользователь открывает папку, удаленный зритель сначала отображает только заглавные. Затем пользователь выбирает из загона, какие из сообщений отображаются в полном объеме. Клиенты удаленного просмотра могут разрешить пользователям удалять сообщения до их загрузки. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Извлечение заглавных сообщений, хранимых удаленно
  
1. Вызов [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния. 
    
2. Call [IMAPITable:::Limit](imapitable-restrict.md) to limit the status table to only those rows that have their **PR RESOURCE \_ \_ TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)column set to MAPI \_ TRANSPORT \_ PROVIDER. 
    
3. Вызов [IMAPITable::SetColumns,](imapitable-setcolumns.md) чтобы включить в таблицу состояния следующие столбцы: 
   - **PR \_ ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)
   - **PR \_ RESOURCE \_ METHODS** [(PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)
   - **PR \_ ТИП \_ РЕСУРСА,** **ДИСПЛЕЙ ПОСТАВЩИКА \_ \_ PR** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)
   - **PR \_ КОД \_ STATUS** [(PidTagStatusCode).](pidtagstatuscode-canonical-property.md)
    
4. Позвоните [в HrQueryAllRows,](hrqueryallrows.md) чтобы получить все строки в таблице состояния. 
    
5. Передай идентификатор записи для каждой строки в таблице в [вызове в IMAPISession::OpenEntry](imapisession-openentry.md). Поскольку этот интерфейс маршаличен из контекста процесса пулера MAPI в контекст процесса клиента, в отличие от интерфейсов, обычно получаемых из поставщиков адресной книги или магазина сообщений, вопросы, касающиеся многотекучестия, имеют более важное значение. 
    
6. Чтобы получить удаленную папку, позвоните по методу [IUnknown::QueryInterface,](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) IID_IMAPIFolder в качестве идентификатора интерфейса. Удаленная папка не является полной реализацией папок; он поддерживает только подмножество методов и свойств папок. Один из необходимых методов [IMAPIProp::GetProps](imapiprop-getprops.md)поддерживает ирисовку следующих свойств:
    
    |||
    |:-----|:-----|
    |**PR \_ ACCESS** [(PidTagAccess)](pidtagaccess-canonical-property.md)  <br/> |**PR_ACCESS_LEVEL** [(PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** [(PidTagContentCount)](pidtagcontentcount-canonical-property.md)  <br/> |**PR_ASSOC_CONTENT_COUNT** [(PidTagAssociatedContentCount)](pidtagassociatedcontentcount-canonical-property.md)  <br/> |
    |**PR_FOLDER_TYPE** [(PidTagFolderType)](pidtagfoldertype-canonical-property.md)  <br/> |**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |
    |**PR \_ SUBFOLDERS** [(PidTagSubfolders)](pidtagsubfolders-canonical-property.md)  <br/> |**PR_CREATION_TIME** [(PidTagCreationTime)](pidtagcreationtime-canonical-property.md)  <br/> |
    |**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)  <br/> |
    
    Удаленные папки также должны поддерживать методы [IMAPIProp::GetPropList,](imapiprop-getproplist.md) [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)и [IMAPIFolder::SetMessageStatus.](imapifolder-setmessagestatus.md) Таблицы содержимого удаленных папок обычно поддерживают следующие столбцы: 
        
    |||
    |:-----|:-----|
    |**PR \_ DISPLAY \_ TO** [(PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)  <br/> |**PR \_ ENTRYID** <br/> |
    |**PR \_ HASATTACH** [(PidTagHasAttachments)](pidtaghasattachments-canonical-property.md)  <br/> |**PR_IMPORTANCE** [(PidTagImportance)](pidtagimportance-canonical-property.md)  <br/> |
    |**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |**PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)  <br/> |
    |**PR \_ MESSAGE_DELIVERY_TIME** [(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)  <br/> |**PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |
    |**PR \_ MESSAGE_DOWNLOAD_TIME** [(PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)  <br/> |**PR_MESSAGE_SIZE** [(PidTagMessageSize)](pidtagmessagesize-canonical-property.md)  <br/> |
    |**PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)  <br/> |**PR_PRIORITY** [(PidTagPriority)](pidtagpriority-canonical-property.md)  <br/> |
    |**PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |**PR_SENSITIVITY** [(PidTagSensitivity)](pidtagsensitivity-canonical-property.md)  <br/> |
    |**PR \_ SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)  <br/> |**PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)  <br/> |
   
7. Вызов метода [IMAPIStatus::ValidateState](imapistatus-validatestate.md) поставщика транспорта при первом выборе одного из вариантов передачи. Должен быть REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE флаг процесса, а также флаг SHOW_XP_SSESSION_UI, позволяющий показывать пользовательский интерфейс. 
    
   > [!NOTE]
   > Чтобы отметить определенный заголовок сообщения для скачивания или удаления, клиент вызывает [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) и задает флаг MSGSTATUS_REMOTE_DOWNLOAD или MSGSTATUS_REMOTE_DELETE. 
  

