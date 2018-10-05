---
title: Состояние скачивания данных иерархии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384859"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="16149-103">Состояние скачивания данных иерархии</span><span class="sxs-lookup"><span data-stu-id="16149-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="16149-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16149-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="16149-105">В этом разделе описываются двоичных файлов состояние иерархии загрузки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="16149-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="16149-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="16149-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16149-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="16149-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="16149-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="16149-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="16149-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="16149-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="16149-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="16149-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="16149-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="16149-111">From this state:</span></span>  <br/> |[<span data-ttu-id="16149-112">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="16149-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="16149-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="16149-113">To this state:</span></span>  <br/> |<span data-ttu-id="16149-114">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="16149-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="16149-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="16149-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="16149-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="16149-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="16149-117">Описание</span><span class="sxs-lookup"><span data-stu-id="16149-117">Description</span></span>

<span data-ttu-id="16149-118">Это состояние означает инициирует загрузка дерева иерархии папок с сервера в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="16149-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="16149-119">Outlook инициализирует связанной структуры данных **DNHIER** с указатель в иерархию.</span><span class="sxs-lookup"><span data-stu-id="16149-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="16149-120">Клиент загружает иерархии и вставляет новой папки или изменения папок в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="16149-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="16149-121">Процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="16149-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="16149-122">Дополнительные сведения о ICS [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="16149-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="16149-123">По окончании этого состояния локального хранилища возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="16149-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16149-124">См. также</span><span class="sxs-lookup"><span data-stu-id="16149-124">See also</span></span>



[<span data-ttu-id="16149-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="16149-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="16149-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="16149-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="16149-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="16149-127">SYNCSTATE</span></span>](syncstate.md)

