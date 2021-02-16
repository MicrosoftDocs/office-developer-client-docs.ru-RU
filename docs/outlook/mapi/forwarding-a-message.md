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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Пересылание сообщения подразумевает выполнение многих из тех же задач, что и отправка исходного сообщения. Во-первых, необходимо открыть хранилище сообщений по умолчанию и папку, которая предназначена для хранения исходяющих сообщений, как правило, папки "Исходящие", и вызвать метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) этой папки, чтобы создать сообщение, которое необходимо переназначить. Необходимо также открыть папку, в которую находится исходное сообщение, как правило, папка "Входящие". Сведения об открытии различных папок см. в [открываемой папке магазина сообщений.](opening-a-message-store-folder.md)
  
Основное различие между созданием переадренного сообщения и созданием исходного сообщения состоит в том, что при переназначенном сообщении большинство свойств основаны на свойствах исходного сообщения или копируются непосредственно из него. 
  
**Переад сообщений**
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения см. в [открываемом хранилище сообщений по умолчанию.](opening-the-default-message-store.md)
    
2. Откройте папку "Outbox". Дополнительные сведения [см. в открываемой папке магазина сообщений.](opening-a-message-store-folder.md)
    
3. Вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания нового перенаправляемого сообщения. 
    
4. Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) исходного сообщения, чтобы скопировать следующие свойства в переад. 
    
   - **PR \_ BODY** ([PidTagBody),](pidtagbody-canonical-property.md)PR HTML ([PidTagHtml)](pidtaghtml-canonical-property.md)или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed),](pidtagrtfcompressed-canonical-property.md)в зависимости от того, поддерживаете ли вы формат RTF, обычный текст или HTML. **\_**
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md) 
    
5. Скопируйте вложения из исходного сообщения либо путем вызова метода **IMAPIProp::CopyTo** исходного сообщения для копирования свойства **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments),](pidtagmessageattachments-canonical-property.md)либо путем вызова следующей трехшаговой процедуры для копирования каждого вложения:
    
   1. Вызовите метод [IMessage::CreateAttach](imessage-createattach.md) нового перенаправляемого сообщения, чтобы создать новое вложение. 
      
   2. Вызовите метод [IMessage::OpenAttach](imessage-openattach.md) исходного сообщения, чтобы открыть вложение для копирования. 
      
   3. Вызовите метод **IMAPIProp::CopyTo** исходного сообщения, чтобы скопировать все свойства вложения из старого вложения в новое. 
    
6. Не включайте в вызов **IMAPIProp::CopyTo** следующие свойства: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested)](pidtagoriginatordeliveryreportrequested-canonical-property.md)  <br/> |**PR_RCVD_REPRESENTING** свойств  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId)](pidtagreadreceiptentryid-canonical-property.md)  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)  <br/> |
|**PR_RECEIVED_BY** свойств  <br/> |**PR_REPLY_RECIPIENT** свойств  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId)](pidtagreportentryid-canonical-property.md)  <br/> |**PR_SENDER** свойств  <br/> |
|**PR_SENT_REPRESENTING** свойств  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Отформатирование текста сообщения путем добавления отступа и абзаца загона, который включает исходного отправитель, дату передачи, тему и список получателей. Не включаем в содержимое символы префикса в стиле Интернета.
    
2. Вызовите [ScCreateConversationIndex,](sccreateconversationindex.md)передав значение свойства **PR_CONVERSATION_INDEX** исходного сообщения ([PidTagConversationIndex).](pidtagconversationindex-canonical-property.md)
    
3. Задай префикс для переадоваемой почты. Если вы используете стандартное "FW:", совмедом  эти символы в начале PR_NORMALIZED_SUBJECT и задайте для PR_SUBJECT **(** [PidTagSubject)](pidtagsubject-canonical-property.md)новую строку. Не **задав PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix).](pidtagsubjectprefix-canonical-property.md) Если вы используете нестандартный префикс, например строку длиной более трех символов, храните его **в** PR_SUBJECT_PREFIX. 
    
4. Установите для **PR_SENT_REPRESENTING** свойства соответствующие значения в PR_RCVD_REPRESENTING **свойств.** 
    
5. Создание списка получателей. Дополнительные сведения см. [в теме "Создание списка получателей".](creating-a-recipient-list.md)
    
6. Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) переадружаемого сообщения, чтобы сохранить его или [IMessage::SubmitMessage,](imessage-submitmessage.md) чтобы сохранить и отправить его. 
    
## <a name="see-also"></a>См. также

- [Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

