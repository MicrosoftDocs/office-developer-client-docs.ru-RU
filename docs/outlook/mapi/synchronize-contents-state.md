---
title: Синхронизация состояния содержимого
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438472"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="eca1a-103">Синхронизация состояния содержимого</span><span class="sxs-lookup"><span data-stu-id="eca1a-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="eca1a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eca1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="eca1a-105">В этом разделе описывается, что происходит во время синхронизации состояния содержимого машины состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="eca1a-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="eca1a-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="eca1a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eca1a-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="eca1a-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="eca1a-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="eca1a-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="eca1a-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="eca1a-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="eca1a-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="eca1a-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="eca1a-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="eca1a-111">From this state:</span></span>  <br/> |[<span data-ttu-id="eca1a-112">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="eca1a-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="eca1a-113">Для этого состояния:</span><span class="sxs-lookup"><span data-stu-id="eca1a-113">To this state:</span></span>  <br/> |<span data-ttu-id="eca1a-114">[Скачивание состояния таблицы,](download-table-state.md) [состояние таблицы](upload-table-state.md)загрузки или синхронизация</span><span class="sxs-lookup"><span data-stu-id="eca1a-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="eca1a-115">Машина состояния репликации — это детерминистический автомат состояния.</span><span class="sxs-lookup"><span data-stu-id="eca1a-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="eca1a-116">Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего.</span><span class="sxs-lookup"><span data-stu-id="eca1a-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="eca1a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="eca1a-117">Description</span></span>

<span data-ttu-id="eca1a-118">Это состояние инициирует один из двух процессов репликации: загрузку содержимого указанных папок в локальном магазине или полную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="eca1a-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="eca1a-119">В полной синхронизации для каждой из указанных папок сначала загружается содержимое, а затем загружается.</span><span class="sxs-lookup"><span data-stu-id="eca1a-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="eca1a-120">В зависимости от *ulFlags,* задающихся в соответствующей структуре **[SYNC](sync.md)** в предыдущем состоянии синхронизации, Outlook инициализирует [выход] членов в структуре **SYNCCONT** для предоставления сведений о содержимом.</span><span class="sxs-lookup"><span data-stu-id="eca1a-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="eca1a-121">Через ту же **структуру SYNCCONT** клиент получает количество папок, которые должны быть загружены или загружены.</span><span class="sxs-lookup"><span data-stu-id="eca1a-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="eca1a-122">Клиент будет проходить цикл через каждую из этих папок, перемещая локальный магазин в состояние таблицы загрузки для загрузки папки или перемещая локальный магазин в состояние таблицы загрузки для загрузки папки.</span><span class="sxs-lookup"><span data-stu-id="eca1a-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="eca1a-123">Кроме того, клиент получает ID-записи для папок, требующих репликации.</span><span class="sxs-lookup"><span data-stu-id="eca1a-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="eca1a-124">Когда это состояние заканчивается, Outlook очищает внутреннюю информацию.</span><span class="sxs-lookup"><span data-stu-id="eca1a-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="eca1a-125">Локальный магазин возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="eca1a-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eca1a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="eca1a-126">See also</span></span>



[<span data-ttu-id="eca1a-127">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="eca1a-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="eca1a-128">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="eca1a-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="eca1a-129">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="eca1a-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="eca1a-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="eca1a-130">SYNCSTATE</span></span>](syncstate.md)

