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
  
Заголовки RFC 822 сопоставляются со свойствами MAPI следующим образом. PR_SENDER_\* — это сокращение для следующих 5 свойств:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Аналогичные сокращения используются для PR_SENT_REPRESENTING_\* и других групп свойств сообщений.
  
|**Заголовок SMTP**|**Свойство MAPI**|
|:-----|:-----|
|От:  <br/> |Исходящие:\*PR_SENDER_; Входящие: PR_SENDER_\* и PR_SENT_REPRESENTING_\*  <br/> |
|Будущ  <br/> |Исходящие: текущее время; входящий: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Кому:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) для получателей, где **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) MAPI_TO  <br/> |
|Центральной  <br/> |**PR_DISPLAY_NAME** и **PR_EMAIL_ADDRESS** для получателей, где **PR_RECIPIENT_TYPE** MAPI_CC  <br/> |
|Копии  <br/> |**PR_DISPLAY_NAME** и **PR_EMAIL_ADDRESS** для получателей, где **PR_RECIPIENT_TYPE** MAPI_BCC  <br/> |
|||
|Доставлен  <br/> |Нет соответствующего свойства MAPI; Укажите имя локального узла и имя компонента.  <br/> |
|Возврат — кому:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) и **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Обратный адрес:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) и **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Тема:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) ограничение на длину не определено.  <br/> |
|Версия MIME:  <br/> |Всегда "1,0"  <br/> |
|||
|X — вложение:  <br/> |Для обеспечения совместимости с шлюзом SMTP службы MS Mail. _filename размер mm – дд – YYY чч: mm_Details ниже.  <br/> |
|||
| _весь конверт SMTP-сообщения_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|имя заголовка не подлежит определению  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for только отправителя. _The тбдхеадер следует использовать, чтобы определить, может ли отправитель интерпретировать содержимое TNEF в ответе.  <br/> |
|MessageID  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-Type  <br/> |Text/plain, multipart/Mixed. Раздел "содержимое сообщения".  <br/> |
   
Заголовок X-MS-вложения форматируется четырьмя маркерами, разделенными пробелом:
  
 _имя размер Дата время_
  
Первый маркер — это имя файла, которое может содержать встроенные пробелы, поэтому этот заголовок должен быть проанализирован справа от входящих сообщений. Размер в байтах; Дата форматируется как _мм-дд-гггг,_ а время — как _чч: мм._
  
> [!NOTE]
> MessageID не сопоставлен **PR_SEARCH_KEY** , так как домен SMTP имеет определенные требования в формате идентификатора сообщения, что делает невозможным кодирование произвольного идентификатора сообщения MAPI. Вместо этого MessageID сопоставляется с **PR_TNEF_CORRELATION_KEY**. Это свойство представляет собой определяемое транспортом свойство, которое задается транспортом для отправки исходящего сообщения и используется транспортом для получения входящего сообщения. Более подробную информацию можно узнать [в статье Разработка поставщика транспорта с поддержкой TNEF](developing-a-tnef-enabled-transport-provider.md). 
  

