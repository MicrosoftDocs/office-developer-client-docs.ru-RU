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
ms.openlocfilehash: 5a2e4f4b248cb8eefd5ee37c0c90d5ef9c0d0cac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565020"
---
# <a name="finding-sent-or-saved-messages"></a>Поиск отправленных или сохраненных сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Чтобы найти все исходящие сообщения, которые отправки или сохранения**
  
1. Вызов [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) для сравнения папка, содержащая отправленных сообщений с папкой, включающей входящих сообщений. 
    
2. Установите параметр _lpEntryID1_ для указания на **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) и параметр _lpEntryID2_ для указания на **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).
    
Обратите внимание, что если сообщения либо удалить после их отправляются или любые отправленные сообщения будут перемещены в другую папку, эта стратегия не будут работать. 
  
Если в анализ входящего сообщения вы Обратите внимание на то, что свойства, которые обычно задаются с помощью поставщика транспорта не указаны, предполагается, что сообщение не было обработано с помощью поставщика транспорта. Эти свойства включают в себя:
  
- Свойства **PR_RECEIVED_BY** 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

