---
title: Настройка свойств для входящих сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d7043004799d534f11aa98770e2e323cbdae95a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432697"
---
# <a name="setting-properties-on-incoming-messages"></a>Настройка свойств для входящих сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения в подсистеме MAPI ожидают ряд свойств в любом полученном сообщении. Когда поставщик транспорта вносит сообщение в MAPI, он должен установить эти свойства, так как это либо единственный процесс с необходимой для этого информацией, либо, по крайней мере, лучший источник информации.
  
Поставщикам рекомендуется устанавливать значения для всех этих свойств в входящих сообщениях.
  
|**Имя свойства**|**Описание**|
|:-----|:-----|
|**PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)  <br/> |Тема сообщения.  <br/> |
|**PR_BODY** [(PidTagBody)](pidtagbody-canonical-property.md)  <br/> |Простой текстовое сообщение.  <br/> |
|**PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)  <br/> |Сжатый текст сообщения RTF.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** [(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)  <br/> |Дата и время доставки сообщения.  <br/> |
|**PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |Отображает имя источника сообщений.  <br/> |
|**PR_SENDER_ENTRYID** [(PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md)  <br/> |Запись адресной книги источника сообщения.  <br/> |
|**PR_SENDER_SEARCH_KEY** [(PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)  <br/> |Ключ поиска адресной книги для источника сообщения.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** [(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)  <br/> |Время отправки сообщения в систему обмена сообщениями клиентом отправитель сообщения.  <br/> |
|**PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)  <br/> |Имя представителя делегата для отправки.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** [(PidTagSentRepresentingEntryId)](pidtagsentrepresentingentryid-canonical-property.md)  <br/> |Запись адресной книги делегата отправки.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** [(PidTagSentRepresentingSearchKey)](pidtagsentrepresentingsearchkey-canonical-property.md)  <br/> |Ключ поиска адресной книги делегата отправки.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** [(PidTagReceivedRepresentingName)](pidtagreceivedrepresentingname-canonical-property.md)  <br/> |Имя представителя делегата для получения.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** [(PidTagReceivedRepresentingEntryId)](pidtagreceivedrepresentingentryid-canonical-property.md)  <br/> |Запись адресной книги получающие делегаты.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** [(PidTagReceivedRepresentingSearchKey)](pidtagreceivedrepresentingsearchkey-canonical-property.md)  <br/> |Ключ поиска адресной книги получающем делегате.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** [(PidTagReplyRecipientNames)](pidtagreplyrecipientnames-canonical-property.md)  <br/> |Список делегированного получателя отображает имена, разделенные полуколоном и пробелом ("; ").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** [(PidTagReplyRecipientEntries)](pidtagreplyrecipiententries-canonical-property.md)  <br/> |Список делегированных получателей для ответа.  <br/> |
|**PR_MESSAGE_TO_ME** [(PidTagMessageToMe)](pidtagmessagetome-canonical-property.md)  <br/> |Указывает, что получатель был конкретно назван получателем "к" (не в группе).  <br/> |
|**PR_MESSAGE_CC_ME** [(PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md)  <br/> |Указывает, что получатель был конкретно назван получателем "cc" (не в группе).  <br/> |
|**PR_MESSAGE_RECIP_ME** [(PidTagMessageRecipientMe)](pidtagmessagerecipientme-canonical-property.md)  <br/> |Указывает, что получатель был специально назван получателем "to", "cc" или "bcc" (не в группе).  <br/> |
   
Поставщики, которые не имеют явных сопоставлений, могут установить группу **свойств PR_SENT_REPRESENTING** к тем  же значениям, что и группа **PR_SENDER,** группа свойств PR_RCVD_REPRESENTING к тем  же значениям, что и группа **PR_RECEIVED_BY,** и может построить PR_REPLY_RECIPIENT группу свойств на основе **значений PR_SENDER группы.** Например, **PR_SENT_REPRESENTING_NAME** можно установить то же значение, что **и PR_SENDER_NAME.**
  
Свойство **PR_ENTRYID** **или PR_ENTRYLIST** при необходимости можно создать с помощью метода [IMAPISupport::CreateOneOff.](imapisupport-createoneoff.md) Группа **PR_SEARCH_KEY** свойств может быть сгенерирована путем контагенции свойства **PR_ADDRTYPE,** связанного с пользователем, двоеточия (:) и PR_EMAIL_ADDRESS, связанного с пользователем, а затем изменения результата на верхний шкаф.  Функция Windows API **CharUpperBuff** является удобной функцией, используемой для этой цели. Для этого процесса необходимо создать каноническую форму адреса, которую можно сравнить с двоичным количеством. Обратите внимание, что это необязательно, если поставщик транспорта имеет деликатный характер в отношении адресов электронной почты. 
  

