---
title: Необходимые свойства для всех сообщений
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
# <a name="required-properties-for-all-messages"></a>Необходимые свойства для всех сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В следующей таблице описываются свойства, которые клиенты могут рассчитывать на набор или поддержку в сообщениях всех классов.
  
|**Свойство**|**Описание**|
|:-----|:-----|
|**PR_CREATION_TIME**[PidTagCreationTime Canonical Property](pidtagcreationtime-canonical-property.md) [(PidTagCreationTime)](pidtagcreationtime-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|**PR_DISPLAY_BCC** [(PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)  <br/> **PR_DISPLAY_CC** [(PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)  <br/> **PR_DISPLAY_TO** [(PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|||
|**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|**PR_LAST_MODIFICATION_TIME** [(PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|**PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|**PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)  <br/> |Клиенты могут устанавливать исходяние сообщений; должны быть установлены поставщиками магазина сообщений, если не установлены клиентами.  <br/> |
|**PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |Настройка клиентами исходяющих сообщений до их сберегания и поставщиков хранения сообщений после их сберегания.  <br/> |
|**PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|**PR_MESSAGE_SIZE** [(PidTagMessageSize)](pidtagmessagesize-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|**PR_MESSAGE_CC_ME** [(PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md)  <br/> **PR_MESSAGE_RECIP_ME** [(PidTagMessageRecipientMe)](pidtagmessagerecipientme-canonical-property.md)  <br/> **PR_MESSAGE_TO_ME** [(PidTagMessageToMe)](pidtagmessagetome-canonical-property.md)  <br/> |Настройка поставщиками транспорта входящих сообщений.  <br/> |
|||
|**PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)  <br/> |Настройка поставщиками магазина сообщений исходяющих сообщений  <br/> |
|**PR_ORIGINATOR_AND_DL_EXPANSION_HISTORY** [(PidTagOriginatorAndDistributionListExpansionHistory)](pidtagoriginatoranddistributionlistexpansionhistory-canonical-property.md)  <br/> **PR_ORIGINATOR_CERTIFICATE** [(PidTagOriginatorCertificate)](pidtagoriginatorcertificate-canonical-property.md)  <br/> **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** [(PidTagOriginatorDeliveryReportReportRequested)](pidtagoriginatordeliveryreportrequested-canonical-property.md)  <br/> **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** [(PidTagOriginatorNonDeliveryReportReportRequested)](pidtagoriginatornondeliveryreportrequested-canonical-property.md)  <br/> **PR_ORIGINATOR_REQUESTED_ALTERNATE_RECIPIENT** [(PidTagOriginatorRequestedAlternateRecipient)](pidtagoriginatorrequestedalternaterecipient-canonical-property.md)  <br/> **PR_ORIGINATOR_RETURN_ADDRESS** [(PidTagOriginatorReturnAddress](pidtagoriginatorreturnaddress-canonical-property.md))  <br/> |Настройка поставщиками транспорта исходяющих сообщений.  <br/> |
|**PR_PARENT_ENTRYID** [(PidTagParentEntryId)](pidtagparententryid-canonical-property.md)  <br/> **PR_PARENT_DISPLAY** [(PidTagParentDisplay)](pidtagparentdisplay-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|||
|**PR_RCVD_REPRESENTING_ADDRTYPE** [(PidTagReceivedRepresentingAddressType)](pidtagreceivedrepresentingaddresstype-canonical-property.md)  <br/> **PR_RCVD_REPRESENTING_EMAIL_ADDRESS** [(PidTagReceivedRepresentingEmailAddress)](pidtagreceivedrepresentingemailaddress-canonical-property.md)  <br/> **PR_RCVD_REPRESENTING_ENTRYID** [(PidTagReceivedRepresentingEntryId)](pidtagreceivedrepresentingentryid-canonical-property.md)  <br/> **PR_RCVD_REPRESENTING_NAME** [(PidTagReceivedRepresentingName)](pidtagreceivedrepresentingname-canonical-property.md)  <br/> **PR_RCVD_REPRESENTING_SEARCH_KEY** [(PidTagReceivedRepresentingSearchKey)](pidtagreceivedrepresentingsearchkey-canonical-property.md)  <br/> |Настройка поставщиками транспорта входящих сообщений.  <br/> |
|**PR_RECEIVED_BY_ADDRTYPE** [(PidTagReceivedByAddressType)](pidtagreceivedbyaddresstype-canonical-property.md)  <br/> **PR_RECEIVED_BY_EMAIL_ADDRESS** [(PidTagReceivedByEmailAddress)](pidtagreceivedbyemailaddress-canonical-property.md)  <br/> **PR_RECEIVED_BY_ENTRYID** [(PidTagReceivedByEntryId)](pidtagreceivedbyentryid-canonical-property.md)  <br/> **PR_RECEIVED_BY_NAME** [(PidTagReceivedByName)](pidtagreceivedbyname-canonical-property.md)  <br/> **PR_RECEIVED_BY_SEARCH_KEY** [(PidTagReceivedBySearchKey)](pidtagreceivedbysearchkey-canonical-property.md)  <br/> |Настройка поставщиками транспорта входящих сообщений.  <br/> |
|**PR_RECIPIENT_TYPE** [(PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений для входящих сообщений.  <br/> |
|**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
|**PR_SENDER_ADDRTYPE** [(PidTagSenderAddressType)](pidtagsenderaddresstype-canonical-property.md)  <br/> **PR_SENDER_EMAIL_ADDRESS** [(PidTagSenderEmailAddress)](pidtagsenderemailaddress-canonical-property.md)  <br/> **PR_SENDER_ENTRYID** [(PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md)  <br/> **PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> **PR_SENDER_SEARCH_KEY** [(PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)  <br/> |Клиенты могут устанавливать эти свойства в исходяющих сообщениях, но поставщики транспорта должны их устанавливать.  <br/> |
|**PR_SENT_REPRESENTING_ADDRTYPE** [(PidTagSentRepresentingAddressType)](pidtagsentrepresentingaddresstype-canonical-property.md)  <br/> **PR_SENT_REPRESENTING_EMAIL_ADDRESS** [(PidTagSentRepresentingEmailAddress)](pidtagsentrepresentingemailaddress-canonical-property.md)  <br/> **PR_SENT_REPRESENTING_ENTRYID** [(PidTagSentRepresentingEntryId)](pidtagsentrepresentingentryid-canonical-property.md)  <br/> **PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)  <br/> **PR_SENT_REPRESENTING_SEARCH_KEY** [(PidTagSentRepresentingSearchKey)](pidtagsentrepresentingsearchkey-canonical-property.md)  <br/> |Клиенты могут устанавливать эти свойства в исходяющих сообщениях, но поставщики транспорта должны их устанавливать.  <br/> |
|**PR_STORE_ENTRYID** [(PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)  <br/> **PR_STORE_RECORD_KEY** [(PidTagStoreRecordKey)](pidtagstorerecordkey-canonical-property.md)  <br/> |Настройка поставщиками хранения сообщений исходяющих сообщений.  <br/> |
   

