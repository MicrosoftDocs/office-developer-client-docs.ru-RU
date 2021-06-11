---
title: Скачивание состояния загона сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417121"
---
# <a name="download-message-header-state"></a><span data-ttu-id="ec3cf-103">Скачивание состояния загона сообщений</span><span class="sxs-lookup"><span data-stu-id="ec3cf-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="ec3cf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec3cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ec3cf-105">В этом разделе описывается, что происходит во время состояния заголовок сообщения загрузки машины состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ec3cf-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ec3cf-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec3cf-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="ec3cf-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="ec3cf-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="ec3cf-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="ec3cf-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="ec3cf-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="ec3cf-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="ec3cf-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="ec3cf-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="ec3cf-111">From this state:</span></span>  <br/> |[<span data-ttu-id="ec3cf-112">Состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="ec3cf-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="ec3cf-113">Для этого состояния:</span><span class="sxs-lookup"><span data-stu-id="ec3cf-113">To this state:</span></span>  <br/> |<span data-ttu-id="ec3cf-114">Состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="ec3cf-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ec3cf-115">Машина состояния репликации — это детерминистический автомат состояния.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="ec3cf-116">Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="ec3cf-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ec3cf-117">Description</span></span>

<span data-ttu-id="ec3cf-118">В этом состоянии клиент обновляет заготку сообщения в локальном магазине.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="ec3cf-119">Локальный магазин вводит это состояние при **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** и выходит, когда **[называется IOSTX::SyncHdrEnd.](iostx-synchdrend.md)**</span><span class="sxs-lookup"><span data-stu-id="ec3cf-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="ec3cf-120">В этом состоянии Outlook инициализирует членов связанной структуры **данных HDRSYNC** с информацией о загоне сообщения.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="ec3cf-121">Сначала клиент загружает полный элемент сообщения с сервера, а затем обновляет заготку элемента сообщения локально.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="ec3cf-122">Когда синхронизация заканчивается, клиент задает результаты скачивания.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="ec3cf-123">Локальный магазин возвращается в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="ec3cf-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ec3cf-124">См. также</span><span class="sxs-lookup"><span data-stu-id="ec3cf-124">See also</span></span>



[<span data-ttu-id="ec3cf-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="ec3cf-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ec3cf-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="ec3cf-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ec3cf-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="ec3cf-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ec3cf-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="ec3cf-128">SYNCSTATE</span></span>](syncstate.md)

