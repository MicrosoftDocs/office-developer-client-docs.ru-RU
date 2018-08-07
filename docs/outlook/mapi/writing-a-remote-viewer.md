---
title: Написание удаленного просмотра
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 554f98f7bda8c6616ce06b86142213c18bff1f69
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812619"
---
# <a name="writing-a-remote-viewer"></a>Написание удаленного просмотра

**Относится к**: Outlook 
  
Средство просмотра удаленных — это окно в клиентском приложении, предоставляющий управляемый доступ к сообщениям, хранящиеся на другом компьютере. Этот управляемый доступ могут работать на медленных связи. А не получить полный список доступных сообщений каждый раз, когда пользователь открывает папку, удаленного просмотра сначала отображает только заголовки. Пользователь выбирает в заголовках которого сообщений для отображения в полном объеме. Средство просмотра удаленных клиентов можно разрешить пользователям удалять сообщения, прежде чем когда-либо загрузке. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Чтобы получить заголовки сообщений, хранящихся в удаленном режиме
  
1. Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Вызов [IMAPITable::Restrict](imapitable-restrict.md) для ограничения в таблице состояния для строки, содержащие их **связей с Общественностью\_РЕСУРСОВ\_тип** столбец ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) значение MAPI\_ТРАНСПОРТА\_ПОСТАВЩИКА. 
    
3. Вызов [IMAPITable::SetColumns](imapitable-setcolumns.md) для включения в таблице состояния следующие столбцы: 
   - **Цена\_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **Цена\_РЕСУРСОВ\_МЕТОДЫ** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **Цена\_РЕСУРСОВ\_тип**, **связей с Общественностью\_ПОСТАВЩИКА\_ОТОБРАЖЕНИЯ** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **Цена\_состояние\_кода** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. Вызовите [HrQueryAllRows](hrqueryallrows.md) , чтобы получить все строки в таблице состояния. 
    
5. Передайте идентификатор входа для каждой строки в таблице в вызове [IMAPISession::OpenEntry](imapisession-openentry.md). Так как этот интерфейс упакованы из контекста процесса диспетчер очереди MAPI для процесса контекст клиента — в отличие от интерфейсов, как правило, полученный из адресной книги или сообщения хранения поставщиков — проблемы используемого многопоточность являются более важности. 
    
6. Вызовите метод [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) состояние объекта, передав IID_IMAPIFolder идентификатор интерфейса для получения удаленной папке. Удаленная папка не является реализации папок; Поддержка только подмножество папки методы и свойства. Один из необходимые методы [IMAPIProp::GetProps](imapiprop-getprops.md)поддерживает извлечения следующие свойства:
    
    |||
    |:-----|:-----|
    |**Цена\_доступа** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**Цена\_вложенных ПАПОК** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Удаленные папки также должны поддерживать методы [IMAPIProp::GetPropList](imapiprop-getproplist.md), [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)и [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) . Как правило, содержимое таблицы удаленной папке поддерживает следующие столбцы: 
        
    |||
    |:-----|:-----|
    |**Цена\_ОТОБРАЖЕНИЯ\_кому** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**Цена\_ENTRYID** <br/> |
    |**Цена\_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**Цена\_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**Цена\_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**PR_OBJECT_TYPE** <br/> |
    |**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**Цена\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. Время метод первый [IMAPIStatus::ValidateState](imapistatus-validatestate.md) поставщика транспорта, один из параметров передачи выбирается вызова. Параметр REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE процесс флаг должен быть установлен и флаг SHOW_XP_SSESSION_UI чтобы разрешить пользовательского интерфейса для отображения. 
    
   > [!NOTE]
   > Чтобы пометить заголовок определенного сообщения для загрузки или удаления, клиент вызывает [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) и устанавливает флаг MSGSTATUS_REMOTE_DOWNLOAD или MSGSTATUS_REMOTE_DELETE. 
  

