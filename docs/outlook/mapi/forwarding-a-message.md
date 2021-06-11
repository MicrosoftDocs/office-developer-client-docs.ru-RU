---
title: Пересылка сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d1df84c37cc2a24806c35ae0c90e4bf2a5e438d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433180"
---
# <a name="forwarding-a-message"></a>Пересылка сообщения

**Область применения**: Outlook 2013 | Outlook 2016 
  
Пересылание сообщения включает в себя многие из тех же задач, что и отправка исходного сообщения. Сначала необходимо открыть хранилище сообщений по умолчанию и папку, предназначенную для хранения исходящие сообщения, как правило, исходящие сообщения, и вызвать метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) этой папки, чтобы создать сообщение, которое будет перенаправляемо. Необходимо также открыть папку, в которую содержится исходное сообщение, как правило, папка "Входящие". Сведения об открытии различных папок см. в [сообщении Opening a Message Store Folder](opening-a-message-store-folder.md).
  
Основное отличие между созданием сообщения, которое должно быть переназначено, и созданием оригинала состоит в том, что при переназначенном сообщении большинство свойств либо основаны на свойствах исходного сообщения, либо скопируются непосредственно из них. 
  
**Для перенаадки сообщения**
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения см. в [тексте Открытие магазина сообщений по умолчанию.](opening-the-default-message-store.md)
    
2. Откройте папку "Избокс". Дополнительные сведения см. в [сообщении "Открытие папки магазина сообщений".](opening-a-message-store-folder.md)
    
3. Вызов метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания нового переададного сообщения. 
    
4. Вызов метода [IMAPIProp::CopyTo](imapiprop-copyto.md) исходного сообщения, чтобы скопировать следующие свойства в переадекнутом сообщении: 
    
   - **PR \_ BODY** [(PidTagBody),](pidtagbody-canonical-property.md) **PR \_ HTML** [(PidTagHtml),](pidtaghtml-canonical-property.md) **или PR_RTF_COMPRESSED** [(PidTagRtfCompressed),](pidtagrtfcompressed-canonical-property.md)в зависимости от того, поддерживаете ли вы формат богатого текста, простой текст или HTML.
    
   - **PR \_ NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md) 
    
5. Скопируйте вложения сообщений из исходного сообщения либо путем вызова метода **IMAPIProp::CopyTo** исходного сообщения для копирования свойства **PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)или путем вызова следующих трех этапов процедуры для копирования каждого вложения:
    
   1. Чтобы создать новое вложение, позвоните по методу [IMessage::CreateAttach](imessage-createattach.md) нового сообщения. 
      
   2. Вызов метода [IMessage::OpenAttach](imessage-openattach.md) исходного сообщения, чтобы открыть вложение для копирования. 
      
   3. Вызовите метод **IMAPIProp::CopyTo** исходного сообщения, чтобы скопировать все свойства вложений из старого вложения в новое. 
    
6. Не включите следующие свойства в вызов **в IMAPIProp::CopyTo:** 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** [(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)  <br/> |**PR_MESSAGE_DELIVERY_TIME** [(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** [(PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)  <br/> |**PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** [(PidTagOriginatorDeliveryReportReportRequested)](pidtagoriginatordeliveryreportrequested-canonical-property.md)  <br/> |**PR_RCVD_REPRESENTING** свойства  <br/> |
|**PR_READ_RECEIPT_ENTRYID** [(PidTagReadReceiptEntryId)](pidtagreadreceiptentryid-canonical-property.md)  <br/> |**PR_READ_RECEIPT_REQUESTED** [(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)  <br/> |
|**PR_RECEIVED_BY** свойства  <br/> |**PR_REPLY_RECIPIENT** свойства  <br/> |
|**PR_REPORT_ENTRYID** [(PidTagReportEntryId)](pidtagreportentryid-canonical-property.md)  <br/> |**PR_SENDER** свойства  <br/> |
|**PR_SENT_REPRESENTING** свойства  <br/> |**PR_SENTMAIL_ENTRYID** [(PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)  <br/> |
|**PR_SUBJECT_PREFIX** [(PidTagSubjectPrefix)](pidtagsubjectprefix-canonical-property.md)  <br/> | <br/> |
   
1. Формат текста сообщения, добавив в него вмятину и абзац заготавлив, который включает исходный отправитель, дату передачи, субъект и список получателей. Не включай в контент символы префикса в стиле Интернета.
    
2. Вызов [ScCreateConversationIndex,](sccreateconversationindex.md)передавая значение свойства PR_CONVERSATION_INDEX  исходного сообщения[(PidTagConversationIndex).](pidtagconversationindex-canonical-property.md)
    
3. Установите префикс для переададного сообщения. Если вы используете стандартную строку "FW:", соединять эти символы в начале PR_NORMALIZED_SUBJECT и задайте PR_SUBJECT[(PidTagSubject)](pidtagsubject-canonical-property.md)к этой новой строке.   Не **задай PR_SUBJECT_PREFIX** [(PidTagSubjectPrefix).](pidtagsubjectprefix-canonical-property.md) Если используется нестандартная префикс, например строка длиной более **трех символов,** храните ее в PR_SUBJECT_PREFIX . 
    
4. Установите **свойства PR_SENT_REPRESENTING** соответствующим значениям в свойствах **PR_RCVD_REPRESENTING.** 
    
5. Создание списка получателей. Дополнительные сведения см. в [списке "Создание списка получателей".](creating-a-recipient-list.md)
    
6. Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для его сохранения или [IMessage::SubmitMessage](imessage-submitmessage.md) для сохранения и отправки. 
    
## <a name="see-also"></a>См. также

- [Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

