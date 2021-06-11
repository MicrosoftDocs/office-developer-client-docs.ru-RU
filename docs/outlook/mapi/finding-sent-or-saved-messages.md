---
title: Поиск отправленных или сохраненных сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 86373fae2753df66d4456cc0fc00f8b289977650
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437422"
---
# <a name="finding-sent-or-saved-messages"></a>Поиск отправленных или сохраненных сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Поиск всех исходяющих сообщений, сохраненных или отправленных**
  
1. Позвоните [в IMsgStore::CompareEntryIDs,](imsgstore-compareentryids.md) чтобы сравнить папку, содержащую отправленные сообщения, с папкой, содержащую входящие сообщения. 
    
2.  Установите параметр _lpEntryID1_ для указать на **PR_IPM_SENTMAIL_ENTRYID** [(PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)и параметр _lpEntryID2,_ чтобы указать на PR_PARENT_ENTRYID [(PidTagParentEntryId).](pidtagparententryid-canonical-property.md)
    
Следует помнить, что если после их удаления или перенесены какие-либо из отправленных сообщений в другую папку, эта стратегия не будет работать. 
  
Если при рассмотрении входящих сообщений вы заметите, что свойства, которые обычно задает поставщик транспорта, отсутствуют, можно предположить, что сообщение никогда не обрабатывалось поставщиком транспорта. Эти свойства приведены ниже.
  
- **PR_RECEIVED_BY** свойства 
    
- **PR_MESSAGE_DOWNLOAD_TIME** [(PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)
    
- **PR_TRANSPORT_MESSAGE_HEADERS** [(PidTagTransportMessageHeaders)](pidtagtransportmessageheaders-canonical-property.md)
    
- **PR_MESSAGE_TO_ME** [(PidTagMessageToMe)](pidtagmessagetome-canonical-property.md)
    
- **PR_MESSAGE_CC_ME** [(PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md)
    
- **PR_MESSAGE_RECIP_ME** [(PidTagMessageRecipientMe)](pidtagmessagerecipientme-canonical-property.md)
    

