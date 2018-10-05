---
title: Состояние скачивания данных таблицы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395072"
---
# <a name="download-table-state"></a><span data-ttu-id="08211-103">Состояние скачивания данных таблицы</span><span class="sxs-lookup"><span data-stu-id="08211-103">Download Table State</span></span>

  
  
<span data-ttu-id="08211-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08211-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="08211-105">В этом разделе описываются двоичных файлов состояния в таблице загрузки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="08211-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="08211-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="08211-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08211-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="08211-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="08211-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="08211-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="08211-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="08211-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="08211-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="08211-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="08211-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="08211-111">From this state:</span></span>  <br/> |[<span data-ttu-id="08211-112">Синхронизировать состояние содержимого</span><span class="sxs-lookup"><span data-stu-id="08211-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="08211-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="08211-113">To this state:</span></span>  <br/> |<span data-ttu-id="08211-114">Синхронизировать состояние содержимого</span><span class="sxs-lookup"><span data-stu-id="08211-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="08211-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="08211-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="08211-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="08211-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="08211-117">Описание</span><span class="sxs-lookup"><span data-stu-id="08211-117">Description</span></span>

<span data-ttu-id="08211-118">Это состояние означает инициирует загрузку в папку.</span><span class="sxs-lookup"><span data-stu-id="08211-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="08211-119">В этом состоянии Outlook инициализирует связанной структуры данных **DNTBL** со сведениями о папке.</span><span class="sxs-lookup"><span data-stu-id="08211-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="08211-120">Клиент файлы для загрузки содержимого папки и обновляет к папке на локальном хранилище с новой содержимое, изменения или удаления с сервера.</span><span class="sxs-lookup"><span data-stu-id="08211-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="08211-121">Процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="08211-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="08211-122">Дополнительные сведения о ICS [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="08211-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="08211-123">По окончании этого состояния локального хранилища возвращается в состояние содержимое синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="08211-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08211-124">См. также</span><span class="sxs-lookup"><span data-stu-id="08211-124">See also</span></span>



[<span data-ttu-id="08211-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="08211-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="08211-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="08211-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="08211-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="08211-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="08211-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="08211-128">SYNCSTATE</span></span>](syncstate.md)

