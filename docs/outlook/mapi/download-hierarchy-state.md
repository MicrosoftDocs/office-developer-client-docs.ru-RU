---
title: Состояние скачивания данных иерархии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f9c334bc86bdff4abb2762642a37e3f0933a0b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589030"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="60279-103">Состояние скачивания данных иерархии</span><span class="sxs-lookup"><span data-stu-id="60279-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="60279-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60279-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="60279-105">В этом разделе описываются двоичных файлов состояние иерархии загрузки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="60279-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="60279-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="60279-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60279-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="60279-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="60279-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="60279-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="60279-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="60279-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="60279-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="60279-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="60279-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="60279-111">From this state:</span></span>  <br/> |[<span data-ttu-id="60279-112">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="60279-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="60279-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="60279-113">To this state:</span></span>  <br/> |<span data-ttu-id="60279-114">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="60279-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="60279-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="60279-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="60279-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="60279-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="60279-117">Описание</span><span class="sxs-lookup"><span data-stu-id="60279-117">Description</span></span>

<span data-ttu-id="60279-118">Это состояние означает инициирует загрузка дерева иерархии папок с сервера в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="60279-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="60279-119">Outlook инициализирует связанной структуры данных **DNHIER** с указатель в иерархию.</span><span class="sxs-lookup"><span data-stu-id="60279-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="60279-120">Клиент загружает иерархии и вставляет новой папки или изменения папок в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="60279-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="60279-121">Процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="60279-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="60279-122">Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="60279-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="60279-123">По окончании этого состояния локального хранилища возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60279-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="60279-124">См. также</span><span class="sxs-lookup"><span data-stu-id="60279-124">See also</span></span>



[<span data-ttu-id="60279-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="60279-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="60279-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="60279-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="60279-127">СОСТОЯНИЕ</span><span class="sxs-lookup"><span data-stu-id="60279-127">SYNCSTATE</span></span>](syncstate.md)

