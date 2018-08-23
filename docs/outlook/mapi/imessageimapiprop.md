---
title: IMessage IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage
api_type:
- COM
ms.assetid: 7e244d40-595e-432c-aa8c-f9f62ca3c138
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b594297d364ba4f5a3ff7da603d2fe7c2fe8cf07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588533"
---
# <a name="imessage--imapiprop"></a>IMessage : IMAPIProp

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Управляет сообщения, вложения и получателей.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объект Message  <br/> |
|Реализованный:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMessage  <br/> |
|Тип указателя:  <br/> |LPMESSAGE  <br/> |
|Модель транзакций:  <br/> |В транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetAttachmentTable](imessage-getattachmenttable.md) <br/> |Возвращает таблицу вложения сообщения.  <br/> |
|[OpenAttach](imessage-openattach.md) <br/> |Открывает вложение.  <br/> |
|[CreateAttach](imessage-createattach.md) <br/> |Создает новое вложение.  <br/> |
|[DeleteAttach](imessage-deleteattach.md) <br/> |Удаляет вложения.  <br/> |
|[GetRecipientTable](imessage-getrecipienttable.md) <br/> |Возвращает таблицу получателей сообщения.  <br/> |
|[ModifyRecipients](imessage-modifyrecipients.md) <br/> |����������, �������� ��� �������� ����������� ���������.  <br/> |
|[SubmitMessage](imessage-submitmessage.md) <br/> |Сохраняет все изменения в сообщение и помечается как готовые для отправки.  <br/> |
|[SetReadFlag](imessage-setreadflag.md) <br/> |Устанавливает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения и управляет Отправка чтения отчеты.  <br/> |
   
Следующие свойства являются обязательными для сообщений в определенный момент во время их жизненного цикла. Большая часть свойств только для чтения задаются поставщиком хранилища сообщений, когда клиент вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщений. Другие свойства, доступные только для чтения задаются поставщика транспорта. 
  
|**Обязательные свойства для сообщений из всех классов**|**Access**|
|:-----|:-----|
|**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Только для чтения  <br/> |
|Свойства **PR_ORIGINATOR**  <br/> |Только для чтения  <br/> |
|**PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|Свойства **PR_RECEIVED_BY**  <br/> |Только для чтения  <br/> |
|**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|Свойства **PR_SENDER**  <br/> |Только для чтения  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
Только для чтения к клиентам, за исключением **PR_BODY**выполнение следующих условий. Клиенты создания это свойство при обработке отчета.
  
|**Свойства для сообщений отчетов**|
|:-----|
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))  <br/> |
|**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))  <br/> |
|**PR_MESSAGE_CLASS** <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DELIVERY_TIME** ([PidTagOriginalDeliveryTime](pidtagoriginaldeliverytime-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_BCC** ([PidTagOriginalDisplayBcc](pidtagoriginaldisplaybcc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_CC** ([PidTagOriginalDisplayCc](pidtagoriginaldisplaycc-canonical-property.md))  <br/> |
|**PR_ORIGINAL_DISPLAY_TO** ([PidTagOriginalDisplayTo](pidtagoriginaldisplayto-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBJECT** ([PidTagOriginalSubject](pidtagoriginalsubject-canonical-property.md))  <br/> |
|**PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md))  <br/> |
|**PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md))  <br/> |
|**PR_REPORT_TEXT** ([PidTagReportText](pidtagreporttext-canonical-property.md))  <br/> |
|**PR_REPORT_TIME** ([PidTagReportTime](pidtagreporttime-canonical-property.md))  <br/> |
|**PR_SEARCH_KEY** <br/> |
|Свойства **PR_SENDER**  <br/> |
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
|**Свойства для получателей сообщений**|**Access**|**Обязательный или необязательный**|
|:-----|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Только для чтения  <br/> |Обязательный  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |Обязательный  <br/> |
|**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |Чтение и запись  <br/> |Обязательный  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Только для чтения  <br/> |Optional  <br/> |
|**PR_ENTRYID** <br/> |Только для чтения  <br/> |Обязательный  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |Обязательный  <br/> |
|**PR_SEARCH_KEY** <br/> |Только для чтения  <br/> |Optional  <br/> |
   

