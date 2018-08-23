---
title: Состояние скачивания данных таблицы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e75407f62a7e6440f6c8dca8c1d2c76843048da4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595400"
---
# <a name="download-table-state"></a><span data-ttu-id="7e4c9-103">Состояние скачивания данных таблицы</span><span class="sxs-lookup"><span data-stu-id="7e4c9-103">Download Table State</span></span>

  
  
<span data-ttu-id="7e4c9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e4c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7e4c9-105">В этом разделе описываются двоичных файлов состояния в таблице загрузки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7e4c9-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7e4c9-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e4c9-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="7e4c9-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="7e4c9-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="7e4c9-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="7e4c9-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="7e4c9-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="7e4c9-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="7e4c9-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="7e4c9-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="7e4c9-111">From this state:</span></span>  <br/> |[<span data-ttu-id="7e4c9-112">Синхронизировать состояние содержимого</span><span class="sxs-lookup"><span data-stu-id="7e4c9-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="7e4c9-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="7e4c9-113">To this state:</span></span>  <br/> |<span data-ttu-id="7e4c9-114">Синхронизировать состояние содержимого</span><span class="sxs-lookup"><span data-stu-id="7e4c9-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="7e4c9-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="7e4c9-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="7e4c9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7e4c9-117">Description</span></span>

<span data-ttu-id="7e4c9-118">Это состояние означает инициирует загрузку в папку.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="7e4c9-119">В этом состоянии Outlook инициализирует связанной структуры данных **DNTBL** со сведениями о папке.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="7e4c9-120">Клиент файлы для загрузки содержимого папки и обновляет к папке на локальном хранилище с новой содержимое, изменения или удаления с сервера.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="7e4c9-121">Процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="7e4c9-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="7e4c9-122">Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="7e4c9-123">По окончании этого состояния локального хранилища возвращается в состояние содержимое синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="7e4c9-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e4c9-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7e4c9-124">See also</span></span>



[<span data-ttu-id="7e4c9-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="7e4c9-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="7e4c9-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="7e4c9-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7e4c9-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="7e4c9-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="7e4c9-128">СОСТОЯНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e4c9-128">SYNCSTATE</span></span>](syncstate.md)

