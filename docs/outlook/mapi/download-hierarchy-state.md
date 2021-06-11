---
title: Состояние иерархии загрузки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337011"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="11702-103">Состояние иерархии загрузки</span><span class="sxs-lookup"><span data-stu-id="11702-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="11702-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11702-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="11702-105">В этом разделе описывается, что происходит во время состояния иерархии загрузки машины состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="11702-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="11702-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="11702-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11702-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="11702-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="11702-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="11702-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="11702-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="11702-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="11702-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="11702-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="11702-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="11702-111">From this state:</span></span>  <br/> |[<span data-ttu-id="11702-112">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="11702-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="11702-113">Для этого состояния:</span><span class="sxs-lookup"><span data-stu-id="11702-113">To this state:</span></span>  <br/> |<span data-ttu-id="11702-114">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="11702-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="11702-115">Машина состояния репликации — это детерминистический автомат состояния.</span><span class="sxs-lookup"><span data-stu-id="11702-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="11702-116">Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего.</span><span class="sxs-lookup"><span data-stu-id="11702-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="11702-117">Описание</span><span class="sxs-lookup"><span data-stu-id="11702-117">Description</span></span>

<span data-ttu-id="11702-118">Это состояние инициирует загрузку иерархии папок дерева с сервера в локальный магазин.</span><span class="sxs-lookup"><span data-stu-id="11702-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="11702-119">Outlook инициализирует связанную структуру **данных DNHIER** с указателем на иерархию.</span><span class="sxs-lookup"><span data-stu-id="11702-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="11702-120">Клиент загружает иерархию и вставляет новые папки или изменения в папки в локальном магазине.</span><span class="sxs-lookup"><span data-stu-id="11702-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="11702-121">Процесс загрузки принимает microsoft Exchange синхронизации изменений (ICS).</span><span class="sxs-lookup"><span data-stu-id="11702-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="11702-122">Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="11702-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="11702-123">После окончания этого состояния локальный магазин возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="11702-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="11702-124">См. также</span><span class="sxs-lookup"><span data-stu-id="11702-124">See also</span></span>



[<span data-ttu-id="11702-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="11702-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="11702-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="11702-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="11702-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="11702-127">SYNCSTATE</span></span>](syncstate.md)

