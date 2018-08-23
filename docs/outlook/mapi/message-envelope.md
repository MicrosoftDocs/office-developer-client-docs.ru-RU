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
ms.openlocfilehash: fd642575a3136eef3193e0bdbe884cf8f54ba337
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571299"
---
# <a name="message-envelope"></a>Конверт сообщения

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Заголовки RFC 822 сопоставляются со свойствами MAPI следующим образом. PR_SENDER_\* — Аббревиатура для 5 следующие свойства:
  
 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Аналогично аббревиатуры используются для PR_SENT_REPRESENTING_\* и других групп свойств сообщения.
  
|**Заголовок SMTP**|**Свойство MAPI**|
|:-----|:-----|
|От:  <br/> |Исходящие: PR_SENDER_\*; Входящие: PR_SENDER_\* и PR_SENT_REPRESENTING_\*  <br/> |
|Дата:  <br/> |Исходящий трафик: текущего времени; Входящие: **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Кому:  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) для получателей, где MAPI_TO **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |
|«Копия»:  <br/> |**PR_DISPLAY_NAME** и **PR_EMAIL_ADDRESS** для получателей, где **PR_RECIPIENT_TYPE** — MAPI_CC  <br/> |
|Скрытая копия:  <br/> |**PR_DISPLAY_NAME** и **PR_EMAIL_ADDRESS** для получателей, где **PR_RECIPIENT_TYPE** — MAPI_BCC  <br/> |
|||
|Получено:  <br/> |Нет соответствующего свойства MAPI; Введите здесь имя локального узла и имя компонента  <br/> |
|Возврат уведомления для:  <br/> |**PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) и **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Кому:  <br/> |**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) и **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Тема:  <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) Отсутствие ограничения определенной продолжительности.  <br/> |
|MIME-version:  <br/> |Всегда «1.0»  <br/> |
|||
|X-MS-вложений:  <br/> |Для обеспечения совместимости с шлюзом MS Mail SMTP. hh:mm_Details мм дд yyy размер _filename ниже.  <br/> |
|||
| _всего конверт сообщения SMTP_ <br/> |**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|будет определено ПОЗЖЕ имя заголовка  <br/> |**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _for отправителя только ._The TBDheader можно использовать для определения, является ли отправитель может обрабатывать контент TNEF в ответ.  <br/> |
|Код сообщения:  <br/> |**PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-Type  <br/> |Text/plain, либо multipart/mixed. Раздел «Содержимое сообщения» см.  <br/> |
   
Заголовок X-MS-вложений представлен в формате четырех маркеры, разделяя их пробелами:
  
 _Назовите размер Дата и время_
  
Первый маркер имеет имя файла, который может содержать пробелы, поэтому этот заголовок должен выполнить синтаксический анализ из правой входящих сообщений. Размер, в байтах; Дата форматируется как _мм дд гггг_ и время, равное _чч: мм._
  
> [!NOTE]
> Код сообщения не связан с **PR_SEARCH_KEY** , так как домен SMTP имеет особые требования к формат идентификатора сообщения которых не позволяют кодирования произвольный идентификатор сообщения MAPI. Вместо этого MessageID сопоставляется с **PR_TNEF_CORRELATION_KEY**. Это свойство является свойством определенные транспорта, задайте транспортом отправки исходящих сообщений и транспорта, прием входящего сообщения. Для получения дополнительных сведений см [Разработка поставщика транспорта TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  

