---
title: Сопоставление атрибутов TNEF со свойствами MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a724fac-2e64-48a7-92b5-d7cf1528cb2c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 25647a6488fec9a39f8b41441fe9afc4c4aa0a7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405025"
---
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>Сопоставление атрибутов TNEF со свойствами MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В следующей таблице перечислены все атрибуты, определенные в реализации TNEF, и их сопоставления со свойствами MAPI. В некоторых случаях несколько свойств MAPI кодируются как один атрибут. Некоторые атрибуты имеют расширенные описания, приведенные далее в этом разделе.
  
|**Атрибут TNEF**|**Свойство или свойства MAPI**|
|:-----|:-----|
|**аттаидовнер** <br/> |**PR_OWNER_APPT_ID** ([PidTagOwnerAppointmentId](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**аттаттачкреатедате** <br/> |**PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**аттаттачдата** <br/> |**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) или **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))  <br/> |
|**аттаттачмент** <br/> |Сведения об этом сопоставлении можно найти в статье [атрибуты TNEF](tnef-attributes.md).  <br/> |
|**аттаттачметафиле** <br/> |**PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**аттаттачмодифидате** <br/> |**PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**аттаттачтитле** <br/> |**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**аттаттачтранспортфиленаме** <br/> |**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**аттбоди** <br/> |**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**аттконверсатионид** <br/> |**PR_CONVERSATION_KEY** ([PidTagConversationKey](pidtagconversationkey-canonical-property.md)) это свойство является устаревшим в Microsoft Exchange Server: его использование остается только в Outlook, для поиска **IPM. Сообщения Мессажеманажер** .  <br/> |
|**аттдатинд** <br/> |**PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) Дополнительные сведения приведены в статье [Attributes аттдате](attdate-attributes.md) .  <br/> |
|**аттдатемодифиед** <br/> |**PR_LAST_MODIFICATION_TIME** Сведения о [атрибутах аттдате](attdate-attributes.md) .  <br/> |
|**аттдатерекд** <br/> |**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) Дополнительные сведения приведены в статье [Attributes аттдате](attdate-attributes.md) .  <br/> |
|**аттдатесент** <br/> |**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) Дополнительные сведения приведены в статье [Attributes аттдате](attdate-attributes.md) .  <br/> |
|**аттдатестарт** <br/> |**PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) Дополнительные сведения приведены в статье [Attributes аттдате](attdate-attributes.md) .  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) и **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |Сведения об этом атрибуте приведены в разделе [аттмапипропс](attmapiprops.md).  <br/> |
|**аттмессажекласс** <br/> |**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**аттмессажеид** <br/> |**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) см. [корреляция TNEF в шлюзах и транспортах X. 400](tnef-correlation-in-x-400-gateways-and-transports.md).  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |* * PR_ORIG_MESSAGE_CLASS * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |Обратитесь к разделу [аттовнер](attowner.md).  <br/> |
|**аттпарентид** <br/> |**PR_PARENT_KEY** (**пидтагпаренткэй**) это свойство является устаревшим. Дополнительные сведения см. [в статье элементы API, устаревшие в этом выпуске](api-elements-deprecated-in-this-edition.md) .  <br/> |
|**attPriority** <br/> |**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**аттрекуестрес** <br/> |**PR_RESPONSE_REQUESTED** ([PidTagResponseRequested](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**аттсубжект** <br/> |**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

