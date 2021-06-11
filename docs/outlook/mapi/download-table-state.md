---
title: Состояние таблицы загрузки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338341"
---
# <a name="download-table-state"></a><span data-ttu-id="facc7-103">Состояние таблицы загрузки</span><span class="sxs-lookup"><span data-stu-id="facc7-103">Download Table State</span></span>

  
  
<span data-ttu-id="facc7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="facc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="facc7-105">В этом разделе описывается, что происходит во время состояния таблицы загрузки машины состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="facc7-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="facc7-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="facc7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="facc7-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="facc7-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="facc7-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="facc7-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="facc7-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="facc7-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="facc7-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="facc7-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="facc7-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="facc7-111">From this state:</span></span>  <br/> |[<span data-ttu-id="facc7-112">Синхронизация состояния содержимого</span><span class="sxs-lookup"><span data-stu-id="facc7-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="facc7-113">Для этого состояния:</span><span class="sxs-lookup"><span data-stu-id="facc7-113">To this state:</span></span>  <br/> |<span data-ttu-id="facc7-114">Синхронизация состояния содержимого</span><span class="sxs-lookup"><span data-stu-id="facc7-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="facc7-115">Машина состояния репликации — это детерминистический автомат состояния.</span><span class="sxs-lookup"><span data-stu-id="facc7-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="facc7-116">Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего.</span><span class="sxs-lookup"><span data-stu-id="facc7-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="facc7-117">Описание</span><span class="sxs-lookup"><span data-stu-id="facc7-117">Description</span></span>

<span data-ttu-id="facc7-118">Это состояние инициирует загрузку папки.</span><span class="sxs-lookup"><span data-stu-id="facc7-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="facc7-119">В этом состоянии Outlook инициализирует связанную структуру **данных DNTBL** с информацией о папке.</span><span class="sxs-lookup"><span data-stu-id="facc7-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="facc7-120">Клиент загружает содержимое папки и обновляет папку в локальном магазине с помощью нового содержимого, изменений или удалений с сервера.</span><span class="sxs-lookup"><span data-stu-id="facc7-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="facc7-121">Процесс загрузки принимает microsoft Exchange синхронизации изменений (ICS).</span><span class="sxs-lookup"><span data-stu-id="facc7-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="facc7-122">Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="facc7-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="facc7-123">После окончания этого состояния локальный магазин возвращается в состояние синхронизации содержимого.</span><span class="sxs-lookup"><span data-stu-id="facc7-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="facc7-124">См. также</span><span class="sxs-lookup"><span data-stu-id="facc7-124">See also</span></span>



[<span data-ttu-id="facc7-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="facc7-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="facc7-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="facc7-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="facc7-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="facc7-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="facc7-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="facc7-128">SYNCSTATE</span></span>](syncstate.md)

