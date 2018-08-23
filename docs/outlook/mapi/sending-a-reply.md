---
title: Отправки ответа
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 90dafeae-6b61-40e3-8341-d6a11799d0f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4d8c995f5fbca322fca44cdcbb0de224af6b2fbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590290"
---
# <a name="sending-a-reply"></a>Отправки ответа

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения, как правило, поддерживает два типа ответов: одного, которое отправляется только отправителя исходного сообщения и одного, которое отправляется для всех получателей, включенных в список получателей исходного сообщения в дополнение к отправителя. Это второй тип ответа обычно называемую ответ, все сообщения.
  
Чтобы отправить ответ любого типа, реализовать некоторые те же задачи, что при отправке исходное сообщение. К примеру откройте хранилище сообщений по умолчанию и папки исходящих сообщений, обычно Исходящие и вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) исходящей папки для создания ответа. Кроме того откройте папку, в которой содержатся исходное сообщение обычно папки «Входящие». Сведения об открытии разных папок в разделе [Открытие папки хранения сообщений](opening-a-message-store-folder.md).
  
Основное различие между созданием ответа и Создание исходного сообщения является с ее в ответ, большая часть свойств либо на основе или копироваться непосредственно из свойств исходного сообщения. Вложения — свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) сообщение — в частности, исключаются. Список получателей на ответ, все сообщения создается из списка исходное сообщение с получателей, представленный свойством **PR_RECEIVED_BY_SEARCH_KEY** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)) и всех получателей скрытой копии удалены. Свойство **PR_RECEIVED_BY_SEARCH_KEY** представляет текущего пользователя. 
  
### <a name="to-send-a-reply"></a>Чтобы отправить ответ
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения можно [открывать хранилище сообщений по умолчанию](opening-the-default-message-store.md).
    
2. Откройте папку "Исходящие". Дополнительные сведения можно [открывать папки хранения сообщений](opening-a-message-store-folder.md).
    
3. Вызов метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) исходящие Создание ответа. 
    
4. Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) исходное сообщение для копирования сообщения ответа следующие свойства: 
    
   - **Цена\_ТЕЛО** ([PidTagBody](pidtagbody-canonical-property.md)) или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), в зависимости от того, является ли поддерживать формат RTF.
    
   - **Цена\_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), если ответ будут поступать на весь список получателей.
    
   - **Цена\_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
    
5. Не включайте в вызове **IMAPIProp::CopyTo**следующие свойства:
    
    |||
    |:-----|:-----|
    |**Цена\_КЛИЕНТА\_SUBMIT\_времени** <br/> |**Цена\_сообщение\_ДОСТАВКИ\_времени** <br/> |
    |**Цена\_сообщение\_загрузить\_времени** <br/> |**Цена\_сообщение\_флаги** <br/> |
    |**Цена\_ИНИЦИАТОРА\_ДОСТАВКИ\_ REPORT\REQUESTED** <br/> |**Связей с Общественностью\_получено\_REPRESENTING** свойства  <br/> |
    |**Цена\_чтение\_уведомления\_ENTRYID** <br/> |**Цена\_чтение\_уведомления\_ЗАПРОШЕННАЯ** <br/> |
    |**Связей с Общественностью\_получено\_по** свойств  <br/> |**Связей с Общественностью\_ОТВЕТ\_ПОЛУЧАТЕЛЯ** свойства  <br/> |
    |**Цена\_отчет о\_ENTRYID** <br/> |**Связей с Общественностью\_ОТПРАВИТЕЛЯ** свойства  <br/> |
    |**Связей с Общественностью\_отправлено\_REPRESENTING** свойства  <br/> |**Цена\_SENTMAIL\_ENTRYID** <br/> |
    |**Цена\_ТЕМЫ\_ПРЕФИКСОВ** <br/> | <br/> |
   
6. Добавление текста разделителя групп разрядов свойство body независимо от выбранного сообщения, чем поддерживать — **PR_BODY**, **PR_HTM**L или **PR_RTF_COMPRESSED**.
    
7. Вызовите [ScCreateConversationIndex](sccreateconversationindex.md), передав в значение свойства **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) исходного сообщения.
    
8. Задайте префикс для ответа. При использовании стандартного «RE:», объедините эти символы в начале **PR_NORMALIZED_SUBJECT** и задать **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) в этом новую строку. Не устанавливайте **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)). При использовании нестандартного префикс, такие как строка более трех символов, сохраните ее в **PR_SUBJECT_PREFIX**. 
    
9. Значение свойства **PR_SENT_REPRESENTING** соответствующие значения в свойствах **PR_RCVD_REPRESENTING** . 
    
10. Установка всех записей в **связей с Общественностью\_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) и **PR_REPLY\_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) для записи идентификатор и отображаемое имя Основной получатель — получателя, тип которого не MAPI_TO. Будьте синхронизацию этих свойств. То есть **PR_REPLY_RECIPIENT\_ЗАПИСЕЙ** и **PR_REPLY_RECIPIENT_NAMES** должен содержать такое же число записей и запись в определенной позиции в одно из свойств должны соответствовать запись в одной позиции в другое свойство. 
    
11. Если ответ отправляется только отправителю исходного сообщения, создайте список получателей одной операции с получателем, представленный свойством **PR_SENT_REPRESENTING** исходного сообщения. Дополнительные сведения о создании списка получателей [Списка получателей](creating-a-recipient-list.md)см.
    
12. Если ответ ответить всем, создайте список получателей, как показано ниже:
    
    1. Вызов метода [IMessage::GetRecipientTable](imessage-getrecipienttable.md) исходное сообщение для доступа к его получателей в таблице. 
        
    2. Вызовите [HrQueryAllRows](hrqueryallrows.md) , чтобы получить все строки в таблице. Решить, каждая строка представляет основной или Скрытая копия получателя и должны оставаться в списке или если представляет получателей скрытой копии или пользователя и необходимо удалить из списка. 
        
    3. Различия между типами получателей, посмотрев столбец **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)). Этот столбец будет иметь значение MAPI_TO для получателей, MAPI_CC для получателей скрытой копии и MAPI_BCC для получателей скрытой копии. 
        
    4. Сравнение столбцов **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) со свойством **PR_RECEIVED_BY_SEARCH_KEY** исходного сообщения, чтобы определить, если строка представляет пользователя. 
        
    5. Удаление ненужных строк из списка получателей, вызвав [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить память, связанную с соответствующие записи в структуре [SRowSet](srowset.md) таблицы получателей. Установите все значения в массиве значение свойства равным нулю, все члены **cValues** равным нулю и все члены **lpProps** в каждой структуры [SRow](srow.md) в **SRowSet** значение NULL. 
        
    6. Добавить отправителя в список получателей, как представлено свойством исходное сообщение **связей с Общественностью\_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) и **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) свойства. Проверьте, что отправитель не дублируются в списке.
        
    7. Вызовите метод [IMessage::ModifyRecipients](imessage-modifyrecipients.md) ответное сообщение, установка для параметра _ulFlags_ присваивается значение 0, чтобы создать новый список получателей для ответа на или пересылать сообщения на основе списка из исходного сообщения. 
    
13. Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ответ для сохранения сообщений или [IMessage::SubmitMessage](imessage-submitmessage.md) , чтобы сохранить и отправить его. 
    
> [!NOTE]
> Прежде чем вызывать **IMessage::ModifyRecipients** для сохранения изменений в список получателей, можно разрешить пользователям вносить изменения в форме сообщения. Пользователи могут добавить в список или удалять определенные элементы. Разрешение пользователям вносить изменения в список получателей — это функция необязательно клиента. 
  

