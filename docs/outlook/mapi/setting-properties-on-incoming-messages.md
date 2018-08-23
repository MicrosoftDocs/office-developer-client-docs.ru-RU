---
title: Установка свойств входящих сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 44b5b489d3efce3ecea69ccd8b7b7a638b173c13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578439"
---
# <a name="setting-properties-on-incoming-messages"></a>Установка свойств входящих сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения в подсистеме MAPI предполагается, что число свойств в любой полученного сообщения. При поставщика транспорта возвращает сообщение в MAPI, его следует задать эти свойства, поскольку он — это единственный процесс с сведения, необходимые для этого, или по крайней мере наилучшего источника данных.
  
Поставщики, рекомендуется задать значения для всех этих свойств в входящих сообщений.
  
|**Имя свойства**|**Описание**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Тема сообщения.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Текст сообщения в обычный текст.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Текст сообщения сжатый формат RTF.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Дата и время сообщение было доставлено.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Отображаемое имя этого отправитель сообщения.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Записи адресной книги после этого отправитель сообщения.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Адресной книги поиска ключ после этого отправитель сообщения.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Время, когда сообщение было отправлено системы обмена сообщениями с сообщениями клиента отправителя.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Имя представителя делегат для отправки.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Записи адресной книги, отправляющим делегата.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Ключ поиска книги адрес отправителя делегата.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Имя представителя делегат для приема.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Записи адресной книги получающей делегата.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Клавиша поиска книги адрес получающей делегата.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Список делегированных получателя отображения имен, разделенных точкой с запятой и пространства («;»).  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Список делегированных получателей на ответ.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Указывает, что получатель был намеренно с именем как получателя «кому» (не входит в группу).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Указывает, что получатель был намеренно с именем как получателя «копия» (не входит в группу).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Указывает, что получатель был намеренно с именем как «Кому», «копия» или «Скрытая копия» получатель (не входит в группу).  <br/> |
   
Поставщики, которые имеют не очевидное сопоставления можно задать группу **PR_SENT_REPRESENTING** свойств те же значения, как группа **PR_SENDER** , группа **PR_RCVD_REPRESENTING** свойств, те же значения, как **PR_RECEIVED_BY **группу, а можно создать группу **PR_REPLY_RECIPIENT** свойства на основе значений группы **PR_SENDER** . Например **PR_SENT_REPRESENTING_NAME** может быть присвоено значение **PR_SENDER_NAME**.
  
Свойство **PR_ENTRYID** или **PR_ENTRYLIST** может возникать, если это необходимо, путем вызова метода [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . Группа **PR_SEARCH_KEY** свойств могут создаваться путем объединения **PR_ADDRTYPE** свойства, связанного с пользователем, двоеточие (:) и **PR_EMAIL_ADDRESS** свойства, связанного с этим пользователем, а затем изменение результат в верхний регистр . Функции Windows API **CharUpperBuff** — это удобный функции для этой цели. Что является необходимым этого процесса состоит в форме каноническое адрес, который необходимо сравнить как двоичные количество. Обратите внимание на то, что это не требуется, если поставщик транспорта задается с учетом регистра по отношению к адреса электронной почты. 
  

