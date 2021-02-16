---
title: Настройка свойств входящих сообщений
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
# <a name="setting-properties-on-incoming-messages"></a>Настройка свойств входящих сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения в подсистеме MAPI ожидают ряд свойств в любом полученном сообщении. Когда поставщик транспорта выводит сообщение в MAPI, он должен установить эти свойства, так как это либо единственный процесс с необходимой информацией, либо по крайней мере лучший источник информации.
  
Поставщикам рекомендуется устанавливать значения для всех этих свойств во входящих сообщениях.
  
|**Имя свойства**|**Описание**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)  <br/> |Тема сообщения.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Текст обычного текстового сообщения.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)  <br/> |Сжатый текст сообщения RTF.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)  <br/> |Дата и время доставки сообщения.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |Отображаемого имени источника сообщения.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md)  <br/> |Запись адресной книги источника сообщения.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)  <br/> |Ключ поиска в адресной книге источника сообщения.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)  <br/> |Время отправки сообщения в систему обмена сообщениями клиентом отправитель.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Имя представителя для отправки.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId)](pidtagsentrepresentingentryid-canonical-property.md)  <br/> |Запись адресной книги отправляемого делегата.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey)](pidtagsentrepresentingsearchkey-canonical-property.md)  <br/> |Ключ поиска адресной книги отправляемого делегата.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Имя представителя для получения.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId)](pidtagreceivedrepresentingentryid-canonical-property.md)  <br/> |Запись адресной книги получающие делегаты.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey)](pidtagreceivedrepresentingsearchkey-canonical-property.md)  <br/> |Ключ поиска в адресной книге получающем делегате.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames)](pidtagreplyrecipientnames-canonical-property.md)  <br/> |Список делегированных получателей отображает имена, разделенные окном и пробелом ("; ").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries)](pidtagreplyrecipiententries-canonical-property.md)  <br/> |Список делегированных получателей для ответа.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Указывает, что получатель был назван в качестве получателя "to" (не в группе).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md)  <br/> |Указывает, что получатель был назван в качестве получателя "cc" (не в группе).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe)](pidtagmessagerecipientme-canonical-property.md)  <br/> |Указывает, что получатель был назван в качестве получателя "to", "cc" или "bcc" (не в группе).  <br/> |
   
Поставщики без видимых сопоставлений могут установить для группы **свойств PR_SENT_REPRESENTING** те же значения, что и для группы **PR_SENDER,** группы свойств **PR_RCVD_REPRESENTING** с одинаковыми значениями группы **PR_RECEIVED_BY** и создать группу свойств **PR_REPLY_RECIPIENT** на основе значений группы **PR_SENDER.** Например, **PR_SENT_REPRESENTING_NAME** можно установить то же значение, **что и PR_SENDER_NAME.**
  
Свойство **PR_ENTRYID** **или PR_ENTRYLIST** при необходимости можно создать с помощью вызова метода [IMAPISupport::CreateOneOff.](imapisupport-createoneoff.md) Группу **PR_SEARCH_KEY** свойств можно сгенерировать, совместив свойство **PR_ADDRTYPE,** связанное с пользователем, двоеточие (:) и свойство **PR_EMAIL_ADDRESS,** связанное с пользователем, а затем изменив результат в верхнем регистре. Функция API Windows **CharUpperBuff** — удобная функция, используемая для этой цели. Для этого необходимо создать каноническую форму адреса, которую можно сравнить с двоичным количеством. Обратите внимание, что это не требуется, если поставщик транспорта с учетом учетных записей в отношении адресов электронной почты. 
  

