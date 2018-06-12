---
title: Переадресация сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0027fd5a-f30a-4025-b670-c21869b3a480
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 146c8b4d711982118fd9da185a5b095a1bae6b2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808490"
---
# <a name="forwarding-a-message"></a>Переадресация сообщения

**Применимо к**: Outlook 
  
Переадресация сообщения состоит из множества те же задачи, как и отправка исходного сообщения. Во-первых необходимо открыть хранилище сообщений по умолчанию и к папке, предназначенный для хранения исходящих сообщений, обычно Исходящие и вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) этой папки, чтобы создать сообщение для перенаправления. Также необходимо открыть папку, в которой содержатся исходное сообщение обычно папки «Входящие». Сведения об открытии разных папок в разделе [Открытие папки хранения сообщений](opening-a-message-store-folder.md).
  
Основное различие между, чтобы разрешить пересылку сообщений и создания исходной является с переадресованных сообщений, большая часть свойств либо на основе или копироваться непосредственно из свойств исходного сообщения. 
  
**Для пересылки сообщения**
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения можно [открывать хранилище сообщений по умолчанию](opening-the-default-message-store.md).
    
2. Откройте папку "Исходящие". Дополнительные сведения можно [открывать папки хранения сообщений](opening-a-message-store-folder.md).
    
3. Вызов метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) исходящие для создания новых переадресованных сообщений. 
    
4. Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) исходное сообщение для копирования следующие свойства в переадресованных сообщений: 
    
   - **Цена\_ТЕЛО** ([PidTagBody](pidtagbody-canonical-property.md)), **связей с Общественностью\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), в зависимости от того, было ли поддерживать текст в формате RTF, обычный текст или HTML.
    
   - **Цена\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) 
    
5. Скопируйте вложений сообщений из исходного сообщения с помощью метода **IMAPIProp::CopyTo** исходное сообщение для копирования свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) или путем вызова следующих три шаг процедуры для каждого вложения для копирования:
    
   1. Вызов нового перенаправлять сообщения [IMessage::CreateAttach](imessage-createattach.md) метод для создания нового вложения. 
      
   2. Вызовите метод [IMessage::OpenAttach](imessage-openattach.md) исходное сообщение для открытия вложения для копирования. 
      
   3. Вызовите метод **IMAPIProp::CopyTo** исходное сообщение, чтобы скопировать все свойства вложения из старого вложений в новую. 
    
6. Не включайте в вызове **IMAPIProp::CopyTo**следующие свойства: 
    
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
   
1. Форматирование текста сообщения путем добавления отступа и абзац заголовка, который включает в себя отправителю, Дата передачи, тему и списка получателей. Не включайте символы префикса характерном для Интернета с содержимым.
    
2. Вызовите [ScCreateConversationIndex](sccreateconversationindex.md), передав в значение свойства **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) исходного сообщения.
    
3. Задайте префикс для перенаправленного сообщения. При использовании стандартного «встроенного по:», объедините эти символы в начале **PR_NORMALIZED_SUBJECT** и задать **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) в этом новую строку. Не устанавливайте **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). При использовании нестандартного префикс, такие как строка более трех символов, сохраните ее в **PR_SUBJECT_PREFIX**. 
    
4. Значение свойства **PR_SENT_REPRESENTING** соответствующие значения в свойствах **PR_RCVD_REPRESENTING** . 
    
5. Создание списка получателей. [Список получателей](creating-a-recipient-list.md)для получения дополнительных сведений см.
    
6. Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) переадресованных сообщений для сохранения ее или [IMessage::SubmitMessage](imessage-submitmessage.md) , чтобы сохранить и отправить его. 
    
## <a name="see-also"></a>См. также

- [Каноническое свойство PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)

