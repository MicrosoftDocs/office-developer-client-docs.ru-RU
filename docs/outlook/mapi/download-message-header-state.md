---
title: Загрузка состояния заголовка сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338838"
---
# <a name="download-message-header-state"></a><span data-ttu-id="9887b-103">Загрузка состояния заголовка сообщения</span><span class="sxs-lookup"><span data-stu-id="9887b-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="9887b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9887b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9887b-105">В этом разделе описывается, что происходит во время загрузки состояния заголовка сообщения для конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="9887b-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9887b-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9887b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9887b-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="9887b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9887b-108">**ЛР_СИНК_ДОВНЛОАД_ХЕАДЕР**</span><span class="sxs-lookup"><span data-stu-id="9887b-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="9887b-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="9887b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="9887b-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="9887b-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="9887b-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="9887b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="9887b-112">Состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="9887b-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="9887b-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="9887b-113">To this state:</span></span>  <br/> |<span data-ttu-id="9887b-114">Состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="9887b-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="9887b-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="9887b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9887b-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="9887b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9887b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9887b-117">Description</span></span>

<span data-ttu-id="9887b-118">В этом состоянии клиент обновляет заголовок сообщения в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="9887b-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="9887b-119">Локальное хранилище вводит это состояние при **[иосткс:: синчдрбег](iostx-synchdrbeg.md)** and exits, когда **[Иосткс:: синчдренд](iostx-synchdrend.md)** вызывается.</span><span class="sxs-lookup"><span data-stu-id="9887b-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="9887b-120">В этом состоянии Outlook инициализирует члены связанной структуры данных **хдрсинк** сведениями о заголовке сообщения.</span><span class="sxs-lookup"><span data-stu-id="9887b-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="9887b-121">Клиент сначала загружает весь элемент сообщения с сервера, а затем обновляет заголовок элемента сообщения локально.</span><span class="sxs-lookup"><span data-stu-id="9887b-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="9887b-122">Когда синхронизации завершается, клиент устанавливает результаты загрузки.</span><span class="sxs-lookup"><span data-stu-id="9887b-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="9887b-123">Локальное хранилище возвращается в состояние Idle.</span><span class="sxs-lookup"><span data-stu-id="9887b-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9887b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="9887b-124">See also</span></span>



[<span data-ttu-id="9887b-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="9887b-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9887b-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="9887b-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9887b-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="9887b-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9887b-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="9887b-128">SYNCSTATE</span></span>](syncstate.md)

