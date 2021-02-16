---
title: Конверт сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 613956da-c49b-4836-9fde-4601510e8b89
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ccd14244bf7ee76396dc239437ca19f080edb170
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427194"
---
# <a name="message-envelope"></a>Конверт сообщения

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
С свойствами MAPI со свойствами MAPI со следующими свойствами соедина RFC 822. PR_SENDER_ \* аббревиатура для следующих 5 свойств:
  
 **PR_SENDER_NAME** ([PidTagSenderName)](pidtagsendername-canonical-property.md)
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType)](pidtagsenderaddresstype-canonical-property.md)
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress)](pidtagsenderemailaddress-canonical-property.md)
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md)
  
Аналогичные сокращения используются для PR_SENT_REPRESENTING_ и других групп \* свойств сообщения.
  
|**Заголок SMTP**|**Свойство MAPI**|
|:-----|:-----|
|От:  <br/> |Исходящие: \* PR_SENDER_; входящие: PR_SENDER_ \* и PR_SENT_REPRESENTING_\*  <br/> |
|Дата:  <br/> |Исходящие: текущее время; входящий: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)  <br/> |
|Кому:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и **PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)для получателей, для которых PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) MAPI_TO  <br/> |
|Cc:  <br/> |**PR_DISPLAY_NAME** и **PR_EMAIL_ADDRESS** для получателей, **для которых** PR_RECIPIENT_TYPE MAPI_CC  <br/> |
|Ск.  <br/> |**PR_DISPLAY_NAME** и **PR_EMAIL_ADDRESS** для получателей, **для которых PR_RECIPIENT_TYPE** MAPI_BCC  <br/> |
|||
|Получено:  <br/> |Нет соответствующего свойства MAPI; вставьте здесь имя локального хоста и имя компонента.  <br/> |
|Return-receipt-to:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) **и PR_REPORT_ENTRYID** ([PidTagReportEntryId)](pidtagreportentryid-canonical-property.md)  <br/> |
|Ответ на:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries)](pidtagreplyrecipiententries-canonical-property.md)и **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames)](pidtagreplyrecipientnames-canonical-property.md)  <br/> |
|Тема:  <br/> |**PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)Без определенного ограничения длины.  <br/> |
|MIME-версия:  <br/> |Всегда "1.0"  <br/> |
|||
|X-MS-Attachment:  <br/> |Для обеспечения совместимости со шлюзом SMTP почты MS. _filename mm-dd-yyy hh:mm_Details ниже.  <br/> |
|||
| _весь конверт сообщения SMTP_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders)](pidtagtransportmessageheaders-canonical-property.md)  <br/> |
|header name TBD  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for отправитель only._The TBDheader следует использовать для определения того, может ли отправитель интерпретировать содержимое TNEF в ответе.  <br/> |
|MessageID:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey)](pidtagtnefcorrelationkey-canonical-property.md)  <br/> |
|Content-Type  <br/> |Текст, обычный или многоуровневый/смешанный. См. раздел "Содержимое сообщения".  <br/> |
   
Загон X-MS-Attachment отформатирован в виде четырех маркеров, разделенных пробелом:
  
 _время даты размера имени_
  
Первый маркер — это имя файла, которое может содержать внедренные пробелы, поэтому этот загонный элемент должен быть разобрат справа на входящие сообщения. Размер — в ветвях; дата отформатирована как  _мм-дд-yyyy,_ а время —  _как чч:мм._
  
> [!NOTE]
> MessageID не соединимся с PR_SEARCH_KEY **поскольку** домен SMTP предъявляет особые требования к формату идентификатора сообщения, которые делают невозможным кодирование произвольного идентификатора сообщения MAPI. Вместо этого MessageID со картой **PR_TNEF_CORRELATION_KEY.** Это свойство является свойством, определенным транспортом, которое устанавливается транспортом, отправляя исходящие сообщения, и используется транспортом, принимающим входящие сообщения. Дополнительные сведения см. в TNEF-Enabled [поставщика транспорта.](developing-a-tnef-enabled-transport-provider.md) 
  

