---
title: Состояние загрузки иерархии
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
# <a name="download-hierarchy-state"></a><span data-ttu-id="47919-103">Состояние загрузки иерархии</span><span class="sxs-lookup"><span data-stu-id="47919-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="47919-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47919-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="47919-105">В этом разделе описывается, что происходит во время загрузки состояния иерархии для конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="47919-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="47919-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="47919-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47919-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="47919-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="47919-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="47919-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="47919-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="47919-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="47919-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="47919-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="47919-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="47919-111">From this state:</span></span>  <br/> |[<span data-ttu-id="47919-112">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="47919-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="47919-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="47919-113">To this state:</span></span>  <br/> |<span data-ttu-id="47919-114">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="47919-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="47919-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="47919-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="47919-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="47919-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="47919-117">Описание</span><span class="sxs-lookup"><span data-stu-id="47919-117">Description</span></span>

<span data-ttu-id="47919-118">Это состояние инициирует загрузку иерархической структуры папок с сервера в локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="47919-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="47919-119">Outlook инициализирует связанную структуру данных **днхиер** с помощью указателя на иерархию.</span><span class="sxs-lookup"><span data-stu-id="47919-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="47919-120">Клиент загружает иерархию и вставляет новые папки или изменения в папки в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="47919-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="47919-121">В процессе загрузки выполняется добавочная синхронизация изменений Microsoft Exchange (ICS).</span><span class="sxs-lookup"><span data-stu-id="47919-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="47919-122">Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="47919-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="47919-123">При завершении этого состояния локальное хранилище возвращается в состояние Synchronize.</span><span class="sxs-lookup"><span data-stu-id="47919-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47919-124">См. также</span><span class="sxs-lookup"><span data-stu-id="47919-124">See also</span></span>



[<span data-ttu-id="47919-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="47919-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="47919-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="47919-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="47919-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="47919-127">SYNCSTATE</span></span>](syncstate.md)

