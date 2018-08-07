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
ms.openlocfilehash: 6e8b618e477475e8e7f45c266791086af63d8bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808449"
---
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="52dba-103">Поиск отправленных или сохраненных сообщений</span><span class="sxs-lookup"><span data-stu-id="52dba-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="52dba-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52dba-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="52dba-105">**Чтобы найти все исходящие сообщения, которые отправки или сохранения**</span><span class="sxs-lookup"><span data-stu-id="52dba-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="52dba-106">Вызов [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) для сравнения папка, содержащая отправленных сообщений с папкой, включающей входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="52dba-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="52dba-107">Установите параметр _lpEntryID1_ для указания на **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) и параметр _lpEntryID2_ для указания на **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52dba-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="52dba-108">Обратите внимание, что если сообщения либо удалить после их отправляются или любые отправленные сообщения будут перемещены в другую папку, эта стратегия не будут работать.</span><span class="sxs-lookup"><span data-stu-id="52dba-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="52dba-109">Если в анализ входящего сообщения вы Обратите внимание на то, что свойства, которые обычно задаются с помощью поставщика транспорта не указаны, предполагается, что сообщение не было обработано с помощью поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="52dba-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="52dba-110">Эти свойства включают в себя:</span><span class="sxs-lookup"><span data-stu-id="52dba-110">These properties include:</span></span>
  
- <span data-ttu-id="52dba-111">Свойства **PR_RECEIVED_BY**</span><span class="sxs-lookup"><span data-stu-id="52dba-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="52dba-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52dba-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="52dba-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52dba-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="52dba-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52dba-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="52dba-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52dba-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="52dba-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="52dba-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

