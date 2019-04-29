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
|**Аттаидовнер** <br/> |**Пр_овнер_аппт_ид** ([PidTagOwnerAppointmentId](pidtagownerappointmentid-canonical-property.md))  <br/> |
|**Аттаттачкреатедате** <br/> |**Пр_креатион_тиме** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
|**Аттаттачдата** <br/> |**Пр_аттач_дата_бин** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) или **пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))  <br/> |
|**Аттаттачмент** <br/> |Сведения об этом сопоставлении можно найти в статье [атрибуты TNEF](tnef-attributes.md).  <br/> |
|**Аттаттачметафиле** <br/> |**Пр_аттач_рендеринг** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))  <br/> |
|**Аттаттачмодифидате** <br/> |**Пр_ласт_модификатион_тиме** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))  <br/> |
|**attAttachRenddata** <br/> |**Пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), **пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |
|**Аттаттачтитле** <br/> |**Пр_аттач_филенаме** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md))  <br/> |
|**Аттаттачтранспортфиленаме** <br/> |**Пр_аттач_транспорт_наме** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md))  <br/> |
|**Аттбоди** <br/> |**Пр_боди** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |
|**Аттконверсатионид** <br/> |**Пр_конверсатион_кэй** ([PidTagConversationKey](pidtagconversationkey-canonical-property.md)) Это свойство является устаревшим в Microsoft Exchange Server: его использование остается только в Outlook, для поиска **IPM. Сообщения Мессажеманажер** .  <br/> |
|**Аттдатинд** <br/> |**Пр_енд_дате** ([PidTagEndDate](pidtagenddate-canonical-property.md)) Сведения о [атрибутАх аттдате](attdate-attributes.md) .  <br/> |
|**Аттдатемодифиед** <br/> |**Пр_ласт_модификатион_тиме** Сведения о [атрибутАх аттдате](attdate-attributes.md) .  <br/> |
|**Аттдатерекд** <br/> |**Пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) Сведения о [атрибутАх аттдате](attdate-attributes.md) .  <br/> |
|**Аттдатесент** <br/> |**Пр_клиент_субмит_тиме** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) Сведения о [атрибутАх аттдате](attdate-attributes.md) .  <br/> |
|**Аттдатестарт** <br/> |**Пр_старт_дате** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) Сведения о [атрибутАх аттдате](attdate-attributes.md) .  <br/> |
|**attFrom** <br/> |**Пр_сендер_ентрид** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) и **пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |
|**attMAPIProps** <br/> |Сведения об этом атрибуте приведены в разделе [аттмапипропс](attmapiprops.md).  <br/> |
|**Аттмессажекласс** <br/> |**Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
|**Аттмессажеид** <br/> |**Пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) Обратитесь к разделу " [корреляция TNEF" в шлюзах и транспортАх X. 400](tnef-correlation-in-x-400-gateways-and-transports.md).  <br/> |
|**attMessageStatus** <br/> |**Пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
|**attOriginalMessageClass** <br/> |* * ПР_ОРИГ_МЕССАЖЕ_КЛАСС * * ([PidTagOriginalMessageClass](pidtagoriginalmessageclass-canonical-property.md))  <br/> |
|**attOwner** <br/> |Обратитесь к разделу [аттовнер](attowner.md).  <br/> |
|**Аттпарентид** <br/> |**Пр_парент_кэй** (**Пидтагпаренткэй**) Это свойство является устаревшим. Дополнительные сведения см. [в статье элементы API, устаревшие в этом](api-elements-deprecated-in-this-edition.md) выпуске.  <br/> |
|**attPriority** <br/> |**Пр_приорити** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
|**attRecipTable** <br/> |**Пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |
|**Аттрекуестрес** <br/> |**Пр_респонсе_рекуестед** ([PidTagResponseRequested](pidtagresponserequested-canonical-property.md))  <br/> |
|**attSentFor** <br/> |**Пр_сент_репресентинг_ентрид** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |
|**Аттсубжект** <br/> |**Пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   

