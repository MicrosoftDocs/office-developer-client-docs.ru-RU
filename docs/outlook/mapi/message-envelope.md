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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356926"
---
# <a name="message-envelope"></a>Конверт сообщения

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Заголовки RFC 822 сопоставляются со свойствами MAPI следующим образом. ПР_СЕНДЕР_\* это сокращение для следующих 5 свойств:
  
 **Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))
  
 **Пр_сендер_аддртипе** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))
  
 **Пр_сендер_емаил_аддресс** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))
  
 **Пр_сендер_сеарч_кэй** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))
  
 **Пр_сендер_ентрид** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))
  
Аналогичные сокращения используются для ПР_СЕНТ_РЕПРЕСЕНТИНГ_\* и других групп свойств сообщений.
  
|**Заголовок SMTP**|**Свойство MAPI**|
|:-----|:-----|
|От:  <br/> |ИсХодящие:\*пр_сендер_; Входящие: ПР_СЕНДЕР_\* и пр_сент_репресентинг_\*  <br/> |
|Будущ  <br/> |ИсХодящие: текущее время; Входящие: **пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |
|Кому:  <br/> |**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и **пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) для получателей, где **пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) является мапи_то  <br/> |
|Центральной  <br/> |**Пр_дисплай_наме** и **пр_емаил_аддресс** для получателей, где **пр_реЦипиент_типе** — мапи_кк  <br/> |
|Копии  <br/> |**Пр_дисплай_наме** и **пр_емаил_аддресс** для получателей, где **пр_реЦипиент_типе** — мапи_бкк  <br/> |
|||
|Доставлен  <br/> |Нет соответствующего свойства MAPI; Укажите имя локального узла и имя компонента.  <br/> |
|Возврат — кому:  <br/> |**Пр_репорт_наме** ([PidTagReportName](pidtagreportname-canonical-property.md)) и **пр_репорт_ентрид** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md))  <br/> |
|Обратный адрес:  <br/> |**Пр_репли_реЦипиент_ентриес** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) и **пр_репли_реЦипиент_намес** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |
|Тема:  <br/> |**Пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md)) Ограничение на длину не определено.  <br/> |
|Версия MIME:  <br/> |Всегда "1,0"  <br/> |
|||
|X — вложение:  <br/> |Для обеспечения совместимости с шлюзом SMTP службы MS Mail. _филенаме размер mm – дд – YYY чч: Мм_детаилс ниже.  <br/> |
|||
| _весь конверт SMTP-сообщения_ <br/> |**Пр_транспорт_мессаже_хеадерс** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))  <br/> |
|имя заголовка не подЛЕЖИТ определению  <br/> |**Пр_сенд_рич_инфо** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) _фор только отправитель. _се тбдхеадер следует использовать, чтобы определить, может ли отправитель ИНТЕРПРЕТИРОВАТЬ содержимое TNEF в ответе.  <br/> |
|MessageID  <br/> |**Пр_тнеф_коррелатион_кэй** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))  <br/> |
|Content-Type  <br/> |Text/plain, multipart/Mixed. Раздел "содержимое сообщения".  <br/> |
   
Заголовок X-MS-вложения форматируется четырьмя маркерами, разделенными пробелом:
  
 _имя размер Дата время_
  
Первый маркер — это имя файла, которое может содержать встроенные пробелы, поэтому этот заголовок должен быть проанализирован справа от входящих сообщений. Размер в байтах; Дата форматируется как _мм-дд-гггг,_ а время — как _чч: мм._
  
> [!NOTE]
> MessageID не сопоставлен с **пр_сеарч_кэй** , так как домен SMTP имеет особые требования к формату идентификатора сообщения, что делает невозможным кодирование произвольного идентификатора сообщения MAPI. Вместо этого MessageID сопоставляется с **пр_тнеф_коррелатион_кэй**. Это свойство представляет собой определяемое транспортом свойство, которое задается транспортом для отправки исходящего сообщения и используется транспортом для получения входящего сообщения. Более подробную информацию можно узнать [в статье Разработка поставщика транспорта с поддержкой TNEF](developing-a-tnef-enabled-transport-provider.md). 
  

