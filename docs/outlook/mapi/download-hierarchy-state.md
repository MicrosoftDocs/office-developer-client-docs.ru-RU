---
title: Состояние скачивания данных иерархии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e31a2a9c45a8896efbc43eb7f4b22f31f51e4013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808331"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="61a97-103">Состояние скачивания данных иерархии</span><span class="sxs-lookup"><span data-stu-id="61a97-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="61a97-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61a97-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="61a97-105">В этом разделе описываются двоичных файлов состояние иерархии загрузки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="61a97-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="61a97-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="61a97-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61a97-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="61a97-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="61a97-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="61a97-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="61a97-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="61a97-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="61a97-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="61a97-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="61a97-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="61a97-111">From this state:</span></span>  <br/> |[<span data-ttu-id="61a97-112">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="61a97-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="61a97-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="61a97-113">To this state:</span></span>  <br/> |<span data-ttu-id="61a97-114">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="61a97-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="61a97-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="61a97-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="61a97-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="61a97-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="61a97-117">Описание</span><span class="sxs-lookup"><span data-stu-id="61a97-117">Description</span></span>

<span data-ttu-id="61a97-118">Это состояние означает инициирует загрузка дерева иерархии папок с сервера в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="61a97-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="61a97-119">Outlook инициализирует связанной структуры данных **DNHIER** с указатель в иерархию.</span><span class="sxs-lookup"><span data-stu-id="61a97-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="61a97-120">Клиент загружает иерархии и вставляет новой папки или изменения папок в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="61a97-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="61a97-121">Процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="61a97-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="61a97-122">Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="61a97-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="61a97-123">По окончании этого состояния локального хранилища возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="61a97-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61a97-124">См. также</span><span class="sxs-lookup"><span data-stu-id="61a97-124">See also</span></span>



[<span data-ttu-id="61a97-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="61a97-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="61a97-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="61a97-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="61a97-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="61a97-127">SYNCSTATE</span></span>](syncstate.md)

