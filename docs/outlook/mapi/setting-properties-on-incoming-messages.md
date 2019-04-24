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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339363"
---
# <a name="setting-properties-on-incoming-messages"></a>Установка свойств для входящих сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения в подсистеме MAPI ожидают ряд свойств в любом полученном сообщении. Когда поставщик транспорта переводит сообщение в MAPI, он должен настроить эти свойства, так как это единственный процесс, в отношении которого необходима необходимая информация, или по крайней мере лучший источник информации.
  
Поставщикам рекомендуется задавать значения для всех этих свойств в входящих сообщениях.
  
|**Имя свойства**|**Описание**|
|:-----|:-----|
|**Пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Тема сообщения.  <br/> |
|**Пр_боди** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Текст сообщения в формате обычного текста.  <br/> |
|**Пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Сжатый текст сообщения в формате RTF.  <br/> |
|**Пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Дата и время доставки сообщения.  <br/> |
|**Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Отображаемое имя инициатора сообщений.  <br/> |
|**Пр_сендер_ентрид** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Запись адресной книги инициатора сообщений.  <br/> |
|**Пр_сендер_сеарч_кэй** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Ключ поиска в адресной книге инициатора сообщения.  <br/> |
|**Пр_клиент_субмит_тиме** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Время, когда сообщение было отправлено в систему обмена сообщениями от клиента обмена сообщениями отправителя.  <br/> |
|**Пр_сент_репресентинг_наме** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Имя репрезентативного делегата для отправки.  <br/> |
|**Пр_сент_репресентинг_ентрид** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Запись адресной книги делегата, отправившего сообщение.  <br/> |
|**Пр_сент_репресентинг_сеарч_кэй** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Ключ поиска адресных книг делегата, отправляющего сообщение.  <br/> |
|**Пр_рквд_репресентинг_наме** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Имя репрезентативного делегата для получения.  <br/> |
|**Пр_рквд_репресентинг_ентрид** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Запись адресной книги принимающего делегата.  <br/> |
|**Пр_рквд_репресентинг_сеарч_кэй** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Ключ поиска в адресной книге принимающего делегата.  <br/> |
|**Пр_репли_реЦипиент_намес** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Список отображаемых имен делегированных получателей, разделенных точкой с запятой и пробелом (";").  <br/> |
|**Пр_репли_реЦипиент_ентриес** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Список делегированных получателей для ответа.  <br/> |
|**Пр_мессаже_то_ме** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Указывает, что получатель был специально назван "to" (не в группе).  <br/> |
|**Пр_мессаже_кк_ме** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Указывает, что получатель был специально назван "CC" (не в группе).  <br/> |
|**Пр_мессаже_реЦип_ме** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Указывает, что получатель был специально назван как "Кому", "копия" или "СК" (не в группе).  <br/> |
   
Поставщики, не имеющие видимых сопоставлений, могут задать для группы **пр_сент_репресентинг** те же значения, что и в группе **пр_сендер** , **пр_рквд_репресентинг** группу свойств с теми же значениями, что и в **пр_рецеивед_би **и может создать группу свойств **пр_репли_реЦипиент** на основе значений группы **пр_сендер** . Например, для **пр_сент_репресентинг_наме** можно задать то же значение, что и **пр_сендер_наме**.
  
При необходимости можно создать свойство **пр_ентрид** или **пр_ентрилист** , вызвав метод [имаписуппорт:: креатеонеофф](imapisupport-createoneoff.md) . Группу свойств **пр_сеарч_кэй** можно создать с помощью сцепления свойства **пр_аддртипе** , связанного с пользователем, двоеточия (:) и свойства **пр_емаил_аддресс** , связанного с пользователем, а затем измените результат на верхний регистр. . Функция **ЧАРУППЕРБУФФ** API Windows — это удобная функция, используемая для этой цели. Для этого процесса необходимо создать каноническую форму адреса, который можно сравнить как двоичное количество. Обратите внимание, что это не требуется, если для поставщика транспорта учитывается регистр по отношению к адресам электронной почты. 
  

