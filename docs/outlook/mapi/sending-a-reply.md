---
title: Отправка ответа
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f47741369b1091c0dd24358e063de8f4675000fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437450"
---
# <a name="sending-a-reply"></a>Отправка ответа

**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения обычно поддерживают два типа ответов: один, который отправляется только отправителю исходного сообщения, а другой — всем другим получателям, включенным в список получателей исходного сообщения в дополнение к отправителю. Этот второй тип ответа обычно называется ответом на все сообщения.
  
Чтобы отправить ответ любого типа, необходимо реализовать некоторые из тех же задач, что и при отправке исходного сообщения. Например, чтобы создать ответ, откройте хранилище сообщений по умолчанию и папку исходяющих сообщений , как правило, папку "Исходящие", и вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) исходящие папки. Кроме того, открывается папка, в которую находится исходное сообщение, как правило, папка "Входящие". Сведения об открытии различных папок см. в [открываемой папке магазина сообщений.](opening-a-message-store-folder.md)
  
Основное различие между созданием ответа и созданием исходного сообщения состоит в том, что большинство свойств основаны на свойствах исходного сообщения или скопируются непосредственно из него. Вложения — свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)— специально исключаются. Список получателей для ответа на все сообщения создается из списка исходного сообщения с получателем, представленным свойством **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey),](pidtagreceivedbysearchkey-canonical-property.md)и все получатели с незрячими копиями удалены. Свойство **PR_RECEIVED_BY_SEARCH_KEY** представляет текущего пользователя. 
  
### <a name="to-send-a-reply"></a>Отправка ответа
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения см. в [открываемом хранилище сообщений по умолчанию.](opening-the-default-message-store.md)
    
2. Откройте папку "Outbox". Дополнительные сведения [см. в открываемой папке магазина сообщений.](opening-a-message-store-folder.md)
    
3. Вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для создания ответа. 
    
4. Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) исходного сообщения, чтобы скопировать в ответное сообщение следующие свойства: 
    
   - **PR \_ BODY** [(PidTagBody)](pidtagbody-canonical-property.md)или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed),](pidtagrtfcompressed-canonical-property.md)в зависимости от того, поддерживается ли формат RTF.
    
   - **PR \_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients),](pidtagmessagerecipients-canonical-property.md)если ответ будет перейти на весь список получателей.
    
   - **PR \_ NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Не включайте в вызов **IMAPIProp::CopyTo** следующие свойства:
    
    |||
    |:-----|:-----|
    |**ВРЕМЯ \_ ОТПРАВКИ \_ \_ PR-КЛИЕНТА** <br/> |**ВРЕМЯ \_ ДОСТАВКИ \_ \_ PR-СООБЩЕНИЙ** <br/> |
    |**ВРЕМЯ \_ СКАЧИВАНИЯ \_ \_ PR-СООБЩЕНИЙ** <br/> |**ФЛАГИ \_ \_ PR-СООБЩЕНИЙ** <br/> |
    |**PR \_ ORIGINATOR \_ DELIVERY \_ REPORT\REQUESTED** <br/> |**PR \_ RCVD \_ REPRESENTING** properties  <br/> |
    |**PR \_ READ \_ RECEIPT \_ ENTRYID** <br/> |**PR \_ READ \_ RECEIPT \_ REQUESTED** <br/> |
    |**PR \_ Свойства RECEIVED \_ BY**  <br/> |**PR \_ Свойства \_ ПОЛУЧАТЕЛЯ ОТВЕТА**  <br/> |
    |**PR \_ REPORT \_ ENTRYID** <br/> |**PR \_ Свойства SENDER**  <br/> |
    |**PR \_ SENT \_ REPRESENTING** properties  <br/> |**PR \_ SENTMAIL \_ ENTRYID** <br/> |
    |**ПРЕФИКС \_ PR SUBJECT \_** <br/> | <br/> |
   
6. Добавьте текст в то, какое свойство текста сообщения поддерживаете — **PR_BODY,** **PR_HTM** L **или PR_RTF_COMPRESSED.**
    
7. Вызовите [ScCreateConversationIndex,](sccreateconversationindex.md)передав значение свойства **PR_CONVERSATION_INDEX** исходного сообщения ([PidTagConversationIndex).](pidtagconversationindex-canonical-property.md)
    
8. Установите префикс для ответа. Если вы используете стандартную строку "RE:", соедините эти символы в начале PR_NORMALIZED_SUBJECT и задайте для PR_SUBJECT[(PidTagSubject)](pidtagsubject-canonical-property.md)новую строку.   Не **задав PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix).](pidtagsubjectprefix-canonical-property.md) Если вы используете нестандартный префикс, например строку длиной более трех символов, храните его **в** PR_SUBJECT_PREFIX. 
    
9. Установите для **PR_SENT_REPRESENTING** свойства соответствующие значения в PR_RCVD_REPRESENTING **свойств.** 
    
10. Установите для каждой записи в **PR \_ REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries)](pidtagreplyrecipiententries-canonical-property.md)и **PR_REPLY \_ RECIPIENT_NAMES** ([PidTagReplyRecipientNames)](pidtagreplyrecipientnames-canonical-property.md)идентификатор записи и отображаемое имя основного получателя — получателя с типом MAPI_TO. Синхронизируются эти свойства. То есть записи **PR_REPLY_RECIPIENT \_ и** **PR_REPLY_RECIPIENT_NAMES** должны содержать одинаковое количество записей, а запись в определенной позиции в одном из свойств должна соответствовать записи в той же позиции в другом свойстве. 
    
11. Если ответ отправляется только отправителю исходного сообщения, создайте один список получателей записей, где получатель представлен свойством PR_SENT_REPRESENTING исходного **сообщения.** Дополнительные сведения о создании списка получателей см. в этой [теме.](creating-a-recipient-list.md)
    
12. Если ответ является ответом всем, создайте список получателей следующим образом:
    
    1. Вызовите метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) исходного сообщения, чтобы получить доступ к таблице получателей. 
        
    2. Вызовите [HrQueryAllRows,](hrqueryallrows.md) чтобы получить все строки в таблице. Определите, представляет ли каждая строка основного получателя или получателя копии и должна ли она оставаться в списке или представляет ли она получателя или пользователя с незрячими копиями и должна быть удалена из списка. 
        
    3. Различает типы получателей, PR_RECIPIENT_TYPE **(** [PidTagRecipientType).](pidtagrecipienttype-canonical-property.md) В этом столбце будет установлено MAPI_TO для основных получателей, MAPI_CC для получателей копии и MAPI_BCC для получателей с незрячими копиями. 
        
    4. **Сравните столбец PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)со свойством **PR_RECEIVED_BY_SEARCH_KEY** исходного сообщения, чтобы определить, представляет ли строка пользователя. 
        
    5. Удалите ненужные строки из списка получателей, вызывая [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память, связанную с соответствующими записями в структуре [SRowSet таблицы](srowset.md) получателей. Установите для всех значений массива значений свойств нулевое значение, для всех членов **cValues** нулевое значение, а для всех членов **lpProps** в каждой структуре [SRow](srow.md) **в SRowSet** значение NULL. 
        
    6. Добавьте отправитель в список получателей, представленный свойствами **PR \_ SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)и **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId).](pidtagsentrepresentingentryid-canonical-property.md) Убедитесь, что отправитель не дублируется в списке.
        
    7. Вызовите метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) ответного сообщения, задав для параметра  _ulFlags_ нулевое значение, чтобы создать новый список получателей для ответа или перенаправляемого сообщения на основе списка из исходного сообщения. 
    
13. Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ответа, чтобы сохранить сообщение или [IMessage::SubmitMessage,](imessage-submitmessage.md) чтобы сохранить и отправить его. 
    
> [!NOTE]
> Перед **вызовом IMessage::ModifyRecipients** для хранения изменений в списке получателей можно разрешить пользователям вносить изменения в форму сообщения. Пользователи могут добавлять в список или удалять определенных участников. Разрешение пользователям вносить изменения в список получателей является необязательной функцией клиента. 
  

