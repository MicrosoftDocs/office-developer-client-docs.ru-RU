---
title: Таблицы исходящих очередей
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 070377ca-ba9e-42ef-ac6b-ff7548b5ccf5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c5f136a0d26b7519bc1b7b3d8f448f5f382767ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591256"
---
# <a name="outgoing-queue-tables"></a><span data-ttu-id="2dfec-103">Таблицы исходящих очередей</span><span class="sxs-lookup"><span data-stu-id="2dfec-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="2dfec-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dfec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dfec-105">Исходящие таблице очереди содержит сведения о всех исходящих сообщений для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="2dfec-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="2dfec-106">Поставщики хранилища сообщений реализовать исходящей очереди таблицы для очереди MAPI для использования.</span><span class="sxs-lookup"><span data-stu-id="2dfec-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="2dfec-107">В этой таблице не должен реализовывать хранилищ, которые не поддерживают отправку и получение сообщений.</span><span class="sxs-lookup"><span data-stu-id="2dfec-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="2dfec-108">Для доступа к исходящим таблице очереди, диспетчер очереди MAPI вызывает метод [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="2dfec-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="2dfec-109">Является обязательной, что сообщения быть предварительно и отправленных поставщика транспорта в том же порядке, как они были отправлены в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="2dfec-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="2dfec-110">Диспетчер очереди MAPI позволяет принимать сообщения от хранилище сообщений в порядке возрастания времени отправки.</span><span class="sxs-lookup"><span data-stu-id="2dfec-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="2dfec-111">Из-за этим требованиям может быть задержка перед некоторые сообщения отображаются в таблице исходящей очереди.</span><span class="sxs-lookup"><span data-stu-id="2dfec-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="2dfec-112">Хранилищ сообщений, либо должна поддерживать Сортировка в таблице исходящей очереди, диспетчер очереди MAPI можно сортировать по времени отправки сообщения или порядок сортировки по умолчанию должны быть по времени отправки в порядке возрастания.</span><span class="sxs-lookup"><span data-stu-id="2dfec-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="2dfec-113">В таблице исходящей очереди необходимо отправлять уведомления при изменении содержимого очереди.</span><span class="sxs-lookup"><span data-stu-id="2dfec-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="2dfec-114">Следующие свойства составляют обязательный столбец, задайте в таблицах исходящей очереди:</span><span class="sxs-lookup"><span data-stu-id="2dfec-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2dfec-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2dfec-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2dfec-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2dfec-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2dfec-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2dfec-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2dfec-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2dfec-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2dfec-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="2dfec-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="2dfec-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="2dfec-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="2dfec-126">Дополнительные сведения об использовании таблицы исходящей очереди видеть [Отправка сообщений с помощью поставщиков хранилища сообщений](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="2dfec-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2dfec-127">См. также</span><span class="sxs-lookup"><span data-stu-id="2dfec-127">See also</span></span>



[<span data-ttu-id="2dfec-128">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="2dfec-128">MAPI Tables</span></span>](mapi-tables.md)

