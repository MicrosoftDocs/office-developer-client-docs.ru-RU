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
# <a name="finding-sent-or-saved-messages"></a><span data-ttu-id="61249-103">Поиск отправленных или сохраненных сообщений</span><span class="sxs-lookup"><span data-stu-id="61249-103">Finding Sent or Saved Messages</span></span>

  
  
<span data-ttu-id="61249-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61249-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="61249-105">**Поиск всех сохраненных или отправленных исходяных сообщений**</span><span class="sxs-lookup"><span data-stu-id="61249-105">**To locate all the outgoing messages that you have saved or sent**</span></span>
  
1. <span data-ttu-id="61249-106">Вызовите [IMsgStore::CompareEntryIDs,](imsgstore-compareentryids.md) чтобы сравнить папку, содержащую отправленные сообщения, с папкой, содержащую входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="61249-106">Call [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) to compare the folder that contains your sent messages with the folder that contains your incoming messages.</span></span> 
    
2. <span data-ttu-id="61249-107">Установите для параметра _lpEntryID1_ указатель на **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId),](pidtagipmsentmailentryid-canonical-property.md)а параметр _lpEntryID2_ — на **PR_PARENT_ENTRYID** ([PidTagParentEntryId).](pidtagparententryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="61249-107">Set the  _lpEntryID1_ parameter to point to **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) and the  _lpEntryID2_ parameter to point to **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="61249-108">Следует помнить, что при удалении сообщений после их удаления или перемещении любого из отправленных сообщений в другую папку эта стратегия не будет работать.</span><span class="sxs-lookup"><span data-stu-id="61249-108">Be aware that if you either delete messages after they are sent or have moved any of the sent messages to another folder, this strategy will not work.</span></span> 
  
<span data-ttu-id="61249-109">Если при проверке входящих сообщений вы заметите, что свойства, которые обычно задаются поставщиком транспорта, отсутствуют, можно предположить, что сообщение никогда не обрабатывалось поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="61249-109">If in examining an incoming message you notice that the properties that are typically set by a transport provider are missing, you can assume that the message was never handled by a transport provider.</span></span> <span data-ttu-id="61249-110">Эти свойства приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="61249-110">These properties include:</span></span>
  
- <span data-ttu-id="61249-111">**PR_RECEIVED_BY** свойств</span><span class="sxs-lookup"><span data-stu-id="61249-111">**PR_RECEIVED_BY** properties</span></span> 
    
- <span data-ttu-id="61249-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="61249-112">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="61249-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders)](pidtagtransportmessageheaders-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="61249-113">**PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))</span></span>
    
- <span data-ttu-id="61249-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61249-114">**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))</span></span>
    
- <span data-ttu-id="61249-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe)](pidtagmessageccme-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="61249-115">**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))</span></span>
    
- <span data-ttu-id="61249-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe)](pidtagmessagerecipientme-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="61249-116">**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))</span></span>
    

