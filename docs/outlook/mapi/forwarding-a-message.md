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
  
Пересылка сообщения включает в себя множество таких же задач, как отправка исходного сообщения. Для начала необходимо открыть хранилище сообщений по умолчанию и папку, предназначенную для хранения исходящих сообщений, как правило, в папке "Исходящие", и вызвать метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для создания переадресованного сообщения. Кроме того, необходимо открыть папку, в которой находится исходное сообщение, обычно это папка "Входящие". Сведения о том, как открывать другие папки, можно найти [в разделе Открытие папки хранилища сообщений](opening-a-message-store-folder.md).
  
Основное различие между созданием перенаправляемого и созданием исходного сообщения заключается в том, что в переадресованном сообщении большинство свойств либо основано на, либо копируются непосредственно из свойств исходного сообщения. 
  
**Пересылка сообщения**
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения см. [в разделе Открытие хранилища сообщений по умолчанию](opening-the-default-message-store.md).
    
2. Откройте папку "Исходящие". Дополнительную информацию можно узнать в статье [Открытие папки хранилища сообщений](opening-a-message-store-folder.md).
    
3. Вызовите метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) , чтобы создать новое переадресованное сообщение. 
    
4. Вызовите метод [IMAPIProp:: CopyTo](imapiprop-copyto.md) исходного сообщения, чтобы скопировать следующие свойства в переадресованное сообщение: 
    
   - **Текст\_** ([PidTagBody](pidtagbody-canonical-property.md)) (), **\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) в зависимости от того, поддерживает ли формат RTF, обычный текст или HTML.
    
   - **NORMALIZED_SUBJECT\_PR** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Скопируйте вложения сообщения из исходного сообщения, вызвав метод **IMAPIProp:: CopyTo** исходного сообщения, чтобы скопировать свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) или выполнив следующие три шага для каждого копируемого вложения:
    
   1. Для создания нового вложения вызовите метод [iMessage:: креатеаттач](imessage-createattach.md) нового переадресованного сообщения::. 
      
   2. Вызовите метод [iMessage:: опенаттач](imessage-openattach.md) исходного сообщения, чтобы открыть вложение, которое необходимо скопировать. 
      
   3. Вызовите метод **IMAPIProp:: CopyTo** исходного сообщения, чтобы скопировать все свойства вложений из старого вложения в новое. 
    
6. Не включайте в вызов IMAPIProp следующие свойства: **: CopyTo**: 
    
|||
|:-----|:-----|
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> |Свойства **PR_RCVD_REPRESENTING**  <br/> |
|**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md))  <br/> |**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md))  <br/> |
|Свойства **PR_RECEIVED_BY**  <br/> |Свойства **PR_REPLY_RECIPIENT**  <br/> |
|**PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |Свойства **PR_SENDER**  <br/> |
|Свойства **PR_SENT_REPRESENTING**  <br/> |**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md))  <br/> |
|**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md))  <br/> | <br/> |
   
1. Форматирование текста сообщения путем добавления отступа и абзаца заголовка, включающего исходный отправитель, дату передачи, тему и список получателей. Не включайте в контент символы префиксов из Интернета.
    
2. Вызовите [сккреатеконверсатиониндекс](sccreateconversationindex.md), передав значение свойства **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) исходного сообщения.
    
3. Задайте префикс для переадресованного сообщения. Если вы используете стандарт "FW:", объедините эти символы в начало **PR_NORMALIZED_SUBJECT** и установите **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) в эту новую строку. Не задавайте **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). Если вы используете нестандартный префикс, например строку длиной более трех символов, сохраните ее в **PR_SUBJECT_PREFIX**. 
    
4. Задайте для свойств **PR_SENT_REPRESENTING** соответствующие значения в свойствах **PR_RCVD_REPRESENTING** . 
    
5. Создайте список получателей. Дополнительную информацию можно узнать [в статье Создание списка получателей](creating-a-recipient-list.md).
    
6. Вызовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) переадресованного сообщения, чтобы сохранить его или [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы сохранить и отправить его. 
    
## <a name="see-also"></a>См. также

- [Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

