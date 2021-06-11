---
title: Сопоставление атрибутов TNEF с свойствами MAPI
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
# <a name="mapping-of-tnef-attributes-to-mapi-properties"></a>Сопоставление атрибутов TNEF с свойствами MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В следующей таблице перечислены все атрибуты, определенные в реализации TNEF, и их сопоставления с свойствами MAPI. В некоторых случаях несколько свойств MAPI кодируются как один атрибут. Некоторые атрибуты имеют расширенные описания в этом разделе.
  
|**Атрибут TNEF**|**Свойство MAPI или свойства**|
|:-----|:-----|
|**attAidOwner** <br/> |**PR_OWNER_APPT_ID** [(PidTagOwnerAppointmentId)](pidtagownerappointmentid-canonical-property.md)  <br/> |
|**attAttachCreateDate** <br/> |**PR_CREATION_TIME** [(PidTagCreationTime)](pidtagcreationtime-canonical-property.md)  <br/> |
|**attAttachData** <br/> |**PR_ATTACH_DATA_BIN** [(PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)или **PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)  <br/> |
|**attAttachment** <br/> |Сведения об этом сопоставлении см. в [tNEF Attributes.](tnef-attributes.md)  <br/> |
|**attAttachMetaFile** <br/> |**PR_ATTACH_RENDERING** [(PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**attAttachModifyDate** <br/> |**PR_LAST_MODIFICATION_TIME** [(PidTagLastModificationTime)](pidtaglastmodificationtime-canonical-property.md)  <br/> |
|**attAttachRenddata** <br/> |**PR_ATTACH_METHOD** [(PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**attAttachTitle** <br/> |**PR_ATTACH_FILENAME** [(PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**attAttachTransportFilename** <br/> |**PR_ATTACH_TRANSPORT_NAME** [(PidTagAttachTransportName)](pidtagattachtransportname-canonical-property.md)  <br/> |
|**attBody** <br/> |**PR_BODY** [(PidTagBody)](pidtagbody-canonical-property.md)  <br/> |
|**attConversationID** <br/> |**PR_CONVERSATION_KEY** [(PidTagConversationKey)](pidtagconversationkey-canonical-property.md)Это свойство было обесценилось в Microsoft Exchange Server: его использование сохраняется только в Outlook, для размещения **IPM. Сообщения MessageManager.**  <br/> |
|**attDateEnd** <br/> |**PR_END_DATE** [(PidTagEndDate)](pidtagenddate-canonical-property.md)См. [сведения о атрибутах attDate.](attdate-attributes.md)  <br/> |
|**attDateModified** <br/> |**PR_LAST_MODIFICATION_TIME** Подробные [сведения см. в материале attDate Attributes.](attdate-attributes.md)  <br/> |
|**attDateRecd** <br/> |**PR_MESSAGE_DELIVERY_TIME** [(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)См. [сведения о атрибутах attDate.](attdate-attributes.md)  <br/> |
|**attDateSent** <br/> |**PR_CLIENT_SUBMIT_TIME** [(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)См. [сведения о атрибутах attDate.](attdate-attributes.md)  <br/> |
|**attDateStart** <br/> |**PR_START_DATE** [(PidTagStartDate)](pidtagstartdate-canonical-property.md)См. [сведения о атрибутах attDate.](attdate-attributes.md)  <br/> |
|**attFrom** <br/> |**PR_SENDER_ENTRYID** [(PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md)и **PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)  <br/> |
|**attMAPIProps** <br/> |Сведения об этом атрибуте см. [в сведениях attMAPIProps.](attmapiprops.md)  <br/> |
|**attMessageClass** <br/> |**PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)  <br/> |
|**attMessageID** <br/> |**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)См. корреляцию [TNEF в X.400 Gateways and Transports](tnef-correlation-in-x-400-gateways-and-transports.md).  <br/> |
|**attMessageStatus** <br/> |**PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)  <br/> |
|**attOriginalMessageClass** <br/> |**PR_ORIG_MESSAGE_CLASS **[(PidTagOriginalMessageClass)](pidtagoriginalmessageclass-canonical-property.md)  <br/> |
|**attOwner** <br/> |См. [attOwner](attowner.md).  <br/> |
|**attParentID** <br/> |**PR_PARENT_KEY** **(PidTagParentKey)** Это свойство было обесценилось. Дополнительные сведения см. в этой версии элементов [API.](api-elements-deprecated-in-this-edition.md)  <br/> |
|**attPriority** <br/> |**PR_PRIORITY** [(PidTagPriority)](pidtagpriority-canonical-property.md)  <br/> |
|**attRecipTable** <br/> |**PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)  <br/> |
|**attRequestRes** <br/> |**PR_RESPONSE_REQUESTED** [(PidTagResponseRequested)](pidtagresponserequested-canonical-property.md)  <br/> |
|**attSentFor** <br/> |**PR_SENT_REPRESENTING_ENTRYID** [(PidTagSentRepresentingEntryId)](pidtagsentrepresentingentryid-canonical-property.md)  <br/> |
|**attSubject** <br/> |**PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)  <br/> |
   

