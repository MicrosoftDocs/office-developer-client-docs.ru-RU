---
title: Установка свойств для входящих сообщений
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
# <a name="setting-properties-on-incoming-messages"></a>Установка свойств для входящих сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения в подсистеме MAPI ожидают ряд свойств в любом полученном сообщении. Когда поставщик транспорта переводит сообщение в MAPI, он должен настроить эти свойства, так как это единственный процесс, в отношении которого необходима необходимая информация, или по крайней мере лучший источник информации.
  
Поставщикам рекомендуется задавать значения для всех этих свойств в входящих сообщениях.
  
|**Имя свойства**|**Описание**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Тема сообщения.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Текст сообщения в формате обычного текста.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Сжатый текст сообщения в формате RTF.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Дата и время доставки сообщения.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Отображаемое имя инициатора сообщений.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Запись адресной книги инициатора сообщений.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Ключ поиска в адресной книге инициатора сообщения.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Время, когда сообщение было отправлено в систему обмена сообщениями от клиента обмена сообщениями отправителя.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Имя репрезентативного делегата для отправки.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Запись адресной книги делегата, отправившего сообщение.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Ключ поиска адресных книг делегата, отправляющего сообщение.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Имя репрезентативного делегата для получения.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Запись адресной книги принимающего делегата.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Ключ поиска в адресной книге принимающего делегата.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Список отображаемых имен делегированных получателей, разделенных точкой с запятой и пробелом (";").  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Список делегированных получателей для ответа.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Указывает, что получатель был специально назван "to" (не в группе).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Указывает, что получатель был специально назван "CC" (не в группе).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Указывает, что получатель был специально назван как "Кому", "копия" или "СК" (не в группе).  <br/> |
   
Поставщики, не имеющие видимых сопоставлений, могут задать для **PR_SENT_REPRESENTING** группе свойств те же значения, что и группа **PR_SENDER** , **PR_RCVD_REPRESENTING** группу свойств с теми же значениями, что и группа **PR_RECEIVED_BY** , и может создавать группу **PR_REPLY_RECIPIENT** свойств на основе значений группы **PR_SENDER** . Например, для **PR_SENT_REPRESENTING_NAME** можно задать то же значение, что и **PR_SENDER_NAME**.
  
При необходимости можно создать свойство **PR_ENTRYID** или **PR_ENTRYLIST** , вызвав метод [имаписуппорт:: креатеонеофф](imapisupport-createoneoff.md) . **PR_SEARCH_KEY** группу свойств можно создать путем сцепления свойства **PR_ADDRTYPE** , связанного с пользователем, двоеточия (:) и свойства **PR_EMAIL_ADDRESS** , связанного с пользователем, а затем изменения результата на верхний регистр. Функция **ЧАРУППЕРБУФФ** API Windows — это удобная функция, используемая для этой цели. Для этого процесса необходимо создать каноническую форму адреса, который можно сравнить как двоичное количество. Обратите внимание, что это не требуется, если для поставщика транспорта учитывается регистр по отношению к адресам электронной почты. 
  

