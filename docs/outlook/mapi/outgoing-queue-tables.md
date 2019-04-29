---
title: Таблицы исХодящих очередей
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
# <a name="outgoing-queue-tables"></a><span data-ttu-id="138ef-103">Таблицы исХодящих очередей</span><span class="sxs-lookup"><span data-stu-id="138ef-103">Outgoing Queue Tables</span></span>

  
  
<span data-ttu-id="138ef-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="138ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="138ef-105">В таблице исходящие очереди содержатся сведения обо всех исходящих сообщениях для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="138ef-105">An outgoing queue table contains information about all the outgoing messages for a message store.</span></span> <span data-ttu-id="138ef-106">Поставщики хранилищ сообщений реализуют таблицы исходящих очередей для диспетчера очереди MAPI, которые необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="138ef-106">Message store providers implement outgoing queue tables for the MAPI spooler to use.</span></span> <span data-ttu-id="138ef-107">Для хранилищ, которые не поддерживают отправку или получение сообщений, не требуется реализация этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="138ef-107">Stores that do not support the sending or receiving of messages need not implement this table.</span></span> 
  
<span data-ttu-id="138ef-108">Чтобы получить доступ к таблице исходящих очередей, диспетчер очереди MAPI вызывает метод [IMsgStore:: жетаутгоингкуеуе](imsgstore-getoutgoingqueue.md) .</span><span class="sxs-lookup"><span data-stu-id="138ef-108">To access an outgoing queue table, the MAPI spooler calls the [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) method.</span></span> 
  
<span data-ttu-id="138ef-109">Требуется предварительная обработка сообщений и их отправка в поставщик транспорта в том же порядке, в котором они были отправлены клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="138ef-109">There is a requirement that messages be preprocessed and submitted to the transport provider in the same order as they were sent by the client application.</span></span> <span data-ttu-id="138ef-110">Диспетчер очереди MAPI предназначен для приема сообщений из хранилища сообщений в порядке возрастания времени отправки.</span><span class="sxs-lookup"><span data-stu-id="138ef-110">The MAPI spooler is designed to accept messages from the message store in ascending order of submission time.</span></span> <span data-ttu-id="138ef-111">В связи с этим требованием может быть определена задержка перед отображением некоторых сообщений в таблице "очередь исходящих сообщений".</span><span class="sxs-lookup"><span data-stu-id="138ef-111">Because of this requirement, there can be some delay before some messages appear in the outgoing queue table.</span></span> 
  
<span data-ttu-id="138ef-112">Хранилища сообщений должны разрешить сортировку в таблице исходящих очередей, чтобы диспетчер очереди MAPI мог отсортировать сообщения по времени отправки, или по умолчанию в качестве порядка сортировки по возрастанию время отправки.</span><span class="sxs-lookup"><span data-stu-id="138ef-112">Message stores should either allow sorting on the outgoing queue table so that the MAPI spooler can sort the messages by submission time, or the default sort order should be by ascending submission time.</span></span> 
  
<span data-ttu-id="138ef-113">Таблица очередь исходящих сообщений должна отправлять уведомления при изменении содержимого очереди.</span><span class="sxs-lookup"><span data-stu-id="138ef-113">The outgoing queue table must send notifications when the contents of the queue changes.</span></span>
  
<span data-ttu-id="138ef-114">Следующие свойства составляют обязательный набор столбцов в таблицах исходящих очередей:</span><span class="sxs-lookup"><span data-stu-id="138ef-114">The following properties make up the required column set in outgoing queue tables:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="138ef-115">**Пр_клиент_субмит_тиме** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-115">**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="138ef-116">**Пр_дисплай_бкк** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-116">**PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="138ef-117">**Пр_дисплай_кк** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-117">**PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="138ef-118">**Пр_дисплай_то** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-118">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="138ef-119">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-119">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="138ef-120">**Пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-120">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="138ef-121">**Пр_мессаже_сизе** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-121">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="138ef-122">**Пр_приорити** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-122">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="138ef-123">**Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-123">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="138ef-124">**Пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-124">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="138ef-125">**Пр_субмит_флагс** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="138ef-125">**PR_SUBMIT_FLAGS** ([PidTagSubmitFlags](pidtagsubmitflags-canonical-property.md))</span></span>  <br/> | <br/> |
   
<span data-ttu-id="138ef-126">Дополнительные сведения о том, как используется таблица исходящих очередей, приведены в разделе [Отправка сообщений с помощью поставщиков хранилища сообщений](sending-messages-by-using-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="138ef-126">For more information about how the outgoing queue table is used, see [Sending Messages by Using Message Store Providers](sending-messages-by-using-message-store-providers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="138ef-127">См. также</span><span class="sxs-lookup"><span data-stu-id="138ef-127">See also</span></span>



[<span data-ttu-id="138ef-128">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="138ef-128">MAPI Tables</span></span>](mapi-tables.md)

