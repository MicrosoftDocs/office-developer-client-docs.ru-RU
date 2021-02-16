---
title: Таблицы исходяющих очередей
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4bf935f58fb20460bbf6baf4b1434be1f3ab8156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437576"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="48cca-103">Таблицы исходяющих очередей</span><span class="sxs-lookup"><span data-stu-id="48cca-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="48cca-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48cca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48cca-105">Таблица исходяющих очередей содержит сведения обо всех исходях сообщениях для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="48cca-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="48cca-106">Поставщики store сообщений реализуют таблицы исходяющих очередей для использования пулом MAPI.</span><span class="sxs-lookup"><span data-stu-id="48cca-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="48cca-107">Хранилища, которые не поддерживают отправку или получение сообщений, не должны реализовывать эту таблицу.</span><span class="sxs-lookup"><span data-stu-id="48cca-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="48cca-108">Чтобы получить доступ к таблице исходяния очереди, пулер MAPI вызывает метод [IMsgStore::GetOutgoingQueue.](imsgstore-getoutgoingqueue.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="48cca-109">Существует требование предварительной подготовки и отправки сообщений поставщику транспорта в том же порядке, в который они были отправлены клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="48cca-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="48cca-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span><span class="sxs-lookup"><span data-stu-id="48cca-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="48cca-111">В связи с этим требованием может быть некоторой задержкой, прежде чем некоторые сообщения появятся в таблице исходяния очереди.</span><span class="sxs-lookup"><span data-stu-id="48cca-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="48cca-112">Хранилища сообщений должны либо разрешать сортировку в таблице исходячих очередей, чтобы пульер MAPI можно было сортировать сообщения по времени отправки, либо порядок сортировки по умолчанию должен быть по возрастанию времени отправки.</span><span class="sxs-lookup"><span data-stu-id="48cca-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="48cca-113">При смене содержимого очереди в таблице исходяющих очередей должны отправляться уведомления.</span><span class="sxs-lookup"><span data-stu-id="48cca-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="48cca-114">Следующие свойства составляют необходимый столбец, задающийся в таблицах исходяющих очередей:</span><span class="sxs-lookup"><span data-stu-id="48cca-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48cca-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="48cca-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="48cca-117">**PR_DISPLAY_CC** ([PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="48cca-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="48cca-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="48cca-119">**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="48cca-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="48cca-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize)](pidtagmessagesize-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="48cca-122">**PR_PRIORITY** ([PidTagPriority)](pidtagpriority-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="48cca-123">**PR_SENDER_NAME** ([PidTagSenderName)](pidtagsendername-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="48cca-124">**PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="48cca-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags)](pidtagsubmitflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="48cca-126">Дополнительные сведения об использовании таблицы исходяющих очередей см. в таблице "Отправка сообщений с помощью поставщиков [store сообщений".](sending-messages-by-using-message-store-providers.md)</span><span class="sxs-lookup"><span data-stu-id="48cca-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="48cca-127">См. также</span><span class="sxs-lookup"><span data-stu-id="48cca-127">See also</span></span>



[<span data-ttu-id="48cca-128">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="48cca-128">MAPI Tables</span></span>](mapi-tables.md)

