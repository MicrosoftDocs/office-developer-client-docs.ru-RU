---
title: Иерархия состояний загрузить (en)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: e31a2a9c45a8896efbc43eb7f4b22f31f51e4013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808331"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="87385-103">Иерархия состояний загрузить (en)</span><span class="sxs-lookup"><span data-stu-id="87385-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="87385-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87385-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="87385-105">В этом разделе описываются двоичных файлов состояние иерархии загрузки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="87385-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="87385-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="87385-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87385-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="87385-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="87385-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="87385-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="87385-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="87385-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="87385-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="87385-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="87385-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="87385-111">From this state:</span></span>  <br/> |[<span data-ttu-id="87385-112">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="87385-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="87385-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="87385-113">To this state:</span></span>  <br/> |<span data-ttu-id="87385-114">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="87385-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="87385-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="87385-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="87385-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="87385-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="87385-117">Описание</span><span class="sxs-lookup"><span data-stu-id="87385-117">Description</span></span>

<span data-ttu-id="87385-118">Это состояние означает инициирует загрузка дерева иерархии папок с сервера в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="87385-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="87385-119">Outlook инициализирует связанной структуры данных **DNHIER** с указатель в иерархию.</span><span class="sxs-lookup"><span data-stu-id="87385-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="87385-120">Клиент загружает иерархии и вставляет новой папки или изменения папок в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="87385-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="87385-121">Процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="87385-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="87385-122">Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/ru-ru/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="87385-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/ru-ru/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="87385-123">По окончании этого состояния локального хранилища возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="87385-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="87385-124">См. также</span><span class="sxs-lookup"><span data-stu-id="87385-124">See also</span></span>



[<span data-ttu-id="87385-125">О репликации API</span><span class="sxs-lookup"><span data-stu-id="87385-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="87385-126">О репликации конечного автомата</span><span class="sxs-lookup"><span data-stu-id="87385-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="87385-127">СОСТОЯНИЕ</span><span class="sxs-lookup"><span data-stu-id="87385-127">SYNCSTATE</span></span>](syncstate.md)

