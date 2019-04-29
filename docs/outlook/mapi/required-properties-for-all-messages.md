---
title: Обязательные свойства для всех сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df7e122f-0c44-4d81-8174-3a2d51671ba9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 329841a49154763a3e73a234e28def149719cb08
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435980"
---
# <a name="required-properties-for-all-messages"></a>Обязательные свойства для всех сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В следующей таблице описываются свойства, которые клиенты могут ожидать установки или просмотра для сообщений всех классов.
  
|**Свойство**|**Описание**|
|:-----|:-----|
|**Пр_креатион_тиме** [КанонИческое свойство PidTagCreationTime](pidtagcreationtime-canonical-property.md) ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|**Пр_дисплай_бкк** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))  <br/> **Пр_дисплай_кк** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))  <br/> **Пр_дисплай_то** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|||
|**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|**Пр_ласт_модификатион_тиме** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|**Пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|**Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |Могут устанавливаться клиентами в исходящих сообщениях; должен устанавливаться поставщиками хранилища сообщений, если они не заданы клиентами.  <br/> |
|**Пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |ЗаДается клиентами в исходящих сообщениях до их сохранения и поставщиков хранилища сообщений после сохранения.  <br/> |
|**Пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|**Пр_мессаже_сизе** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|**Пр_мессаже_кк_ме** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> **Пр_мессаже_реЦип_ме** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> **Пр_мессаже_то_ме** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Устанавливаются поставщиками транспорта для входящих сообщений.  <br/> |
|||
|**Пр_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |Устанавливается поставщиками хранилища сообщений для исходящих сообщений  <br/> |
|**Пр_оригинатор_анд_дл_експансион_хистори** ([PidTagOriginatorAndDistributionListExpansionHistory](pidtagoriginatoranddistributionlistexpansionhistory-canonical-property.md))  <br/> **Пр_оригинатор_цертификате** ([PidTagOriginatorCertificate](pidtagoriginatorcertificate-canonical-property.md))  <br/> **Пр_оригинатор_деливери_репорт_рекуестед** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md))  <br/> **Пр_оригинатор_нон_деливери_репорт_рекуестед** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md))  <br/> **Пр_оригинатор_рекуестед_алтернате_реЦипиент** ([PidTagOriginatorRequestedAlternateRecipient](pidtagoriginatorrequestedalternaterecipient-canonical-property.md))  <br/> **Пр_оригинатор_ретурн_аддресс** ([PidTagOriginatorReturnAddress](pidtagoriginatorreturnaddress-canonical-property.md))  <br/> |Устанавливаются поставщиками транспорта для исходящих сообщений.  <br/> |
|**Пр_парент_ентрид** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))  <br/> **Пр_парент_дисплай** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|||
|**Пр_рквд_репресентинг_аддртипе** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))  <br/> **Пр_рквд_репресентинг_емаил_аддресс** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))  <br/> **Пр_рквд_репресентинг_ентрид** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> **Пр_рквд_репресентинг_наме** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> **Пр_рквд_репресентинг_сеарч_кэй** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Устанавливаются поставщиками транспорта для входящих сообщений.  <br/> |
|**Пр_рецеивед_би_аддртипе** ([PidTagReceivedByAddressType](pidtagreceivedbyaddresstype-canonical-property.md))  <br/> **Пр_рецеивед_би_емаил_аддресс** ([PidTagReceivedByEmailAddress](pidtagreceivedbyemailaddress-canonical-property.md))  <br/> **Пр_рецеивед_би_ентрид** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md))  <br/> **Пр_рецеивед_би_наме** ([PidTagReceivedByName](pidtagreceivedbyname-canonical-property.md))  <br/> **Пр_рецеивед_би_сеарч_кэй** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md))  <br/> |Устанавливаются поставщиками транспорта для входящих сообщений.  <br/> |
|**Пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для входящих сообщений.  <br/> |
|**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|**Пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
|**Пр_сендер_аддртипе** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))  <br/> **Пр_сендер_емаил_аддресс** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))  <br/> **Пр_сендер_ентрид** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> **Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> **Пр_сендер_сеарч_кэй** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Клиенты могут устанавливать эти свойства в исходящих сообщениях, но они должны быть заданы поставщиками транспорта.  <br/> |
|**Пр_сент_репресентинг_аддртипе** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))  <br/> **Пр_сент_репресентинг_емаил_аддресс** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))  <br/> **Пр_сент_репресентинг_ентрид** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> **Пр_сент_репресентинг_наме** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> **Пр_сент_репресентинг_сеарч_кэй** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Клиенты могут устанавливать эти свойства в исходящих сообщениях, но они должны быть заданы поставщиками транспорта.  <br/> |
|**Пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> **Пр_сторе_рекорд_кэй** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |ЗаДается поставщиками хранилищ сообщений для исходящих сообщений.  <br/> |
   

