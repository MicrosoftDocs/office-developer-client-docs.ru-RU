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
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="391e8-103">Поиск отправленных или сохраненных сообщений</span><span class="sxs-lookup"><span data-stu-id="391e8-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="391e8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="391e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="391e8-105">**Чтобы найти все исходящие сообщения, которые отправки или сохранения**</span><span class="sxs-lookup"><span data-stu-id="391e8-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="391e8-106">Вызов [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) для сравнения папка, содержащая отправленных сообщений с папкой, включающей входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="391e8-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="391e8-107">Установите параметр _lpEntryID1_ для указания на **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) и параметр _lpEntryID2_ для указания на **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="391e8-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="391e8-108">Обратите внимание, что если сообщения либо удалить после их отправляются или любые отправленные сообщения будут перемещены в другую папку, эта стратегия не будут работать.</span><span class="sxs-lookup"><span data-stu-id="391e8-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="391e8-109">Если в анализ входящего сообщения вы Обратите внимание на то, что свойства, которые обычно задаются с помощью поставщика транспорта не указаны, предполагается, что сообщение не было обработано с помощью поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="391e8-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="391e8-110">Эти свойства включают в себя:</span><span class="sxs-lookup"><span data-stu-id="391e8-110">These properties include:</span></span>
  
- <span data-ttu-id="391e8-111">Свойства **PR_RECEIVED_BY**</span><span class="sxs-lookup"><span data-stu-id="391e8-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="391e8-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="391e8-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="391e8-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="391e8-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="391e8-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="391e8-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="391e8-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="391e8-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="391e8-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="391e8-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

