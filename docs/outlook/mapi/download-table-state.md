---
title: Состояние загрузки таблицы
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
# <a name="download-table-state"></a><span data-ttu-id="a8d19-103">Состояние загрузки таблицы</span><span class="sxs-lookup"><span data-stu-id="a8d19-103">Download Table State</span></span>

  
  
<span data-ttu-id="a8d19-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8d19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a8d19-105">В этом разделе описывается, что происходит во время загрузки состояния таблицы для конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="a8d19-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a8d19-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a8d19-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8d19-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="a8d19-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a8d19-108">**ЛР_СИНК_ДОВНЛОАД_ТАБЛЕ**</span><span class="sxs-lookup"><span data-stu-id="a8d19-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="a8d19-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="a8d19-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a8d19-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="a8d19-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="a8d19-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="a8d19-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a8d19-112">Состояние синхронизации контента</span><span class="sxs-lookup"><span data-stu-id="a8d19-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="a8d19-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="a8d19-113">To this state:</span></span>  <br/> |<span data-ttu-id="a8d19-114">Состояние синхронизации контента</span><span class="sxs-lookup"><span data-stu-id="a8d19-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a8d19-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="a8d19-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a8d19-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="a8d19-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a8d19-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a8d19-117">Description</span></span>

<span data-ttu-id="a8d19-118">Это состояние инициирует загрузку папки.</span><span class="sxs-lookup"><span data-stu-id="a8d19-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="a8d19-119">В этом состоянии Outlook инициализирует связанную структуру данных **днтбл** информацией о папке.</span><span class="sxs-lookup"><span data-stu-id="a8d19-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="a8d19-120">Клиент загружает содержимое папки и обновляет папку в локальном хранилище, используя новые содержимое, изменения или удаления с сервера.</span><span class="sxs-lookup"><span data-stu-id="a8d19-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="a8d19-121">В процессе загрузки выполняется добавочная синхронизация изменений Microsoft Exchange (ICS).</span><span class="sxs-lookup"><span data-stu-id="a8d19-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="a8d19-122">Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a8d19-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="a8d19-123">При завершении этого состояния локальное хранилище возвращается в состояние синхронизация содержимого.</span><span class="sxs-lookup"><span data-stu-id="a8d19-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8d19-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a8d19-124">See also</span></span>



[<span data-ttu-id="a8d19-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="a8d19-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a8d19-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="a8d19-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a8d19-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="a8d19-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a8d19-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a8d19-128">SYNCSTATE</span></span>](syncstate.md)

