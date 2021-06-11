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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения обычно поддерживают два типа ответов: один, который отправляется только отправителю исходного сообщения, и один, который отправляется всем другим получателям, включенным в список получателей исходного сообщения в дополнение к отправителю. Этот второй тип ответа обычно называется ответом всех сообщений.
  
Чтобы отправить ответ любого типа, вы реализуете те же задачи, что и при отправке исходного сообщения. Например, вы открываете хранилище сообщений по умолчанию и исходящие папки сообщений, как правило, исходящие, и вызываете метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) исходящие папки для создания ответа. Кроме того, вы открываете папку, которая содержит исходное сообщение, как правило, папку "Входящие". Сведения об открытии различных папок см. в [сообщении Opening a Message Store Folder](opening-a-message-store-folder.md).
  
Основное различие между созданием ответа и созданием исходного сообщения состоит в том, что большинство свойств либо основаны на свойствах исходного сообщения, либо копируются непосредственно из них. Вложения — свойство **PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)— специально исключены. Список получателей для ответа создается из исходного списка сообщений **с** получателем, представленным свойством [PR_RECEIVED_BY_SEARCH_KEY (PidTagReceivedBySearchKey),](pidtagreceivedbysearchkey-canonical-property.md)а все получатели слепой копии углерода удалены. Свойство **PR_RECEIVED_BY_SEARCH_KEY** представляет текущего пользователя. 
  
### <a name="to-send-a-reply"></a>Отправка ответа
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения см. в [тексте Открытие магазина сообщений по умолчанию.](opening-the-default-message-store.md)
    
2. Откройте папку "Избокс". Дополнительные сведения см. в [сообщении "Открытие папки магазина сообщений".](opening-a-message-store-folder.md)
    
3. Чтобы создать ответ, вызовите метод [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) 
    
4. Вызов метода [IMAPIProp::CopyTo](imapiprop-copyto.md) исходного сообщения, чтобы скопировать следующие свойства в ответное сообщение: 
    
   - **PR \_ BODY** [(PidTagBody)](pidtagbody-canonical-property.md)или **PR_RTF_COMPRESSED** [(PidTagRtfCompressed),](pidtagrtfcompressed-canonical-property.md)в зависимости от того, поддерживаете ли вы формат богатого текста.
    
   - **PR \_ MESSAGE_RECIPIENTS** [(PidTagMessageRecipients),](pidtagmessagerecipients-canonical-property.md)если ответ будет переходить во весь список получателей.
    
   - **PR \_ NORMALIZED_SUBJECT** [(PidTagNormalizedSubject).](pidtagnormalizedsubject-canonical-property.md)
    
5. Не включите следующие свойства в вызов **в IMAPIProp::CopyTo:**
    
    |||
    |:-----|:-----|
    |**ВРЕМЯ \_ ОТПРАВКИ КЛИЕНТОМ \_ PR \_** <br/> |**ВРЕМЯ \_ ДОСТАВКИ \_ \_ PR-СООБЩЕНИЙ** <br/> |
    |**ВРЕМЯ \_ ЗАГРУЗКИ \_ \_ PR-СООБЩЕНИЙ** <br/> |**ФЛАГИ \_ \_ СООБЩЕНИЙ PR** <br/> |
    |**ОТЧЕТ \_ О \_ ДОСТАВКЕ PR \_ ORIGINATOR\REQUESTED** <br/> |**PR \_ Свойства RCVD, \_ ПРЕДСТАВЛЯЮЩИЕ**  <br/> |
    |**PR \_ READ \_ RECEIPT \_ ENTRYID** <br/> |**ЗАПРОС \_ НА ПОЛУЧЕНИЕ ЧТЕНИЯ \_ \_ PR** <br/> |
    |**PR \_ СВОЙСТВА \_ RECEIVED BY**  <br/> |**PR \_ Свойства \_ ПОЛУЧАТЕЛЯ** ОТВЕТА  <br/> |
    |**ENTRYID \_ ОТЧЕТА \_ О PR** <br/> |**PR \_ Свойства SENDER**  <br/> |
    |**PR \_ СВОЙСТВА SENT \_ REPRESENTING**  <br/> |**ЗАПИСЬ \_ PR SENTMAIL \_** <br/> |
    |**ПРЕФИКС \_ \_ ТЕМЫ PR** <br/> | <br/> |
   
6. Добавьте текст сепаратора в какое бы свойство тела сообщений вы не **PR_BODY,** **PR_HTM** L или **PR_RTF_COMPRESSED**.
    
7. Вызов [ScCreateConversationIndex,](sccreateconversationindex.md)передавая значение свойства PR_CONVERSATION_INDEX  исходного сообщения[(PidTagConversationIndex).](pidtagconversationindex-canonical-property.md)
    
8. Установите префикс для ответа. Если вы используете стандартное "RE:", соединять  эти символы в  начале PR_NORMALIZED_SUBJECT и задайте PR_SUBJECT[(PidTagSubject)](pidtagsubject-canonical-property.md)к этой новой строке. Не **задай PR_SUBJECT_PREFIX** [(PidTagSubjectPrefix).](pidtagsubjectprefix-canonical-property.md) Если используется нестандартная префикс, например строка длиной более **трех символов,** храните ее в PR_SUBJECT_PREFIX . 
    
9. Установите **свойства PR_SENT_REPRESENTING** соответствующим значениям в свойствах **PR_RCVD_REPRESENTING.** 
    
10. Установите каждую из записей в PR **\_ REPLY_RECIPIENT_ENTRIES** [(PidTagReplyRecipientEntries)](pidtagreplyrecipiententries-canonical-property.md)и **PR_REPLY \_ RECIPIENT_NAMES** [(PidTagReplyRecipientNames)](pidtagreplyrecipientnames-canonical-property.md)для идентификатора записи и отображения имени основного получателя — получателя, тип которого MAPI_TO. Синхронизуй эти свойства. То есть PR_REPLY_RECIPIENT **\_ записи** и **PR_REPLY_RECIPIENT_NAMES** должны содержать одинаковое количество записей, а запись в определенной позиции в одном из свойств должна соответствовать записи на том же месте в другом свойстве. 
    
11. Если ответ отправляется только отправителю исходного сообщения, создайте единый список получателей записи с получателем, представленным свойством PR_SENT_REPRESENTING **исходного** сообщения. Дополнительные сведения о создании списка получателей см. в дополнительных сведениях [о создании списка получателей.](creating-a-recipient-list.md)
    
12. Если ответ является ответом, создайте список получателей следующим образом:
    
    1. Чтобы получить доступ к таблице получателей, позвоните по методу [IMessage::GetRecipientTable.](imessage-getrecipienttable.md) 
        
    2. Позвоните [в HrQueryAllRows,](hrqueryallrows.md) чтобы получить все строки в таблице. Определите, представляет ли каждая строка получатель первичной или углеродной копии и должна оставаться в списке или представляет ли она слепого получателя копии углерода или пользователя и должна быть удалена из списка. 
        
    3. Дифференцируйте типы  получателей, PR_RECIPIENT_TYPE[(PidTagRecipientType).](pidtagrecipienttype-canonical-property.md) В этом столбце будет установлено MAPI_TO основных получателей, MAPI_CC получателей копий углерода и MAPI_BCC для получателей слепой копии углерода. 
        
    4. **Сравните столбец** [PR_SEARCH_KEY (PidTagSearchKey)](pidtagsearchkey-canonical-property.md)с свойством PR_RECEIVED_BY_SEARCH_KEY исходного сообщения, чтобы определить, представляет ли строка пользователя.  
        
    5. Удалите нежелательные строки из списка получателей, позвонив [в MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память, связанную с соответствующими записями в структуре [SRowSet](srowset.md) таблицы получателей. Установите все значения в массиве значений свойства к нулю, все участники **cValues** - к нулю, а все участники **lpProps** в каждой структуре [SRow](srow.md) в **SRowSet** для NULL. 
        
    6. Добавьте отправитель в список получателей, представленный pr-SENT_REPRESENTING_NAME исходного сообщения [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)и **PR_SENT_REPRESENTING_ENTRYID** [(Свойства PidTagSentRepresentingEntryId).](pidtagsentrepresentingentryid-canonical-property.md) **\_** Убедитесь, что отправитель не дублируется в списке.
        
    7. Позвоните в метод [IMessage::ModifyRecipients,](imessage-modifyrecipients.md) задав параметр  _ulFlags_ значение нулю, чтобы создать новый список получателей для ответа или перенаправляемого сообщения на основе списка из исходного сообщения. 
    
13. Вызовите метод [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) чтобы сохранить сообщение или [IMessage::SubmitMessage,](imessage-submitmessage.md) чтобы сохранить и отправить его. 
    
> [!NOTE]
> Перед вызовом **IMessage::ModifyRecipients** для хранения изменений в списке получателей можно разрешить пользователям вносить изменения через форму сообщения. Пользователи могут добавлять в список или удалять определенных участников. Разрешение пользователям вносить изменения в список получателей является необязательным клиентом. 
  

