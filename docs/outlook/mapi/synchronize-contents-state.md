---
title: Состояние синхронизации контента
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349569"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="94e14-103">Состояние синхронизации контента</span><span class="sxs-lookup"><span data-stu-id="94e14-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="94e14-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94e14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="94e14-105">В этом разделе описывается, что происходит во время состояния "Синхронизация контента" для конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="94e14-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="94e14-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="94e14-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94e14-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="94e14-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="94e14-108">**ЛР_СИНК_КОНТЕНТС**</span><span class="sxs-lookup"><span data-stu-id="94e14-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="94e14-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="94e14-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="94e14-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="94e14-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="94e14-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="94e14-111">From this state:</span></span>  <br/> |[<span data-ttu-id="94e14-112">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="94e14-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="94e14-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="94e14-113">To this state:</span></span>  <br/> |<span data-ttu-id="94e14-114">[Загрузка состояния таблицы](download-table-state.md), [Отправка состояния таблицы](upload-table-state.md)или Синхронизация состояния</span><span class="sxs-lookup"><span data-stu-id="94e14-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="94e14-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="94e14-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="94e14-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="94e14-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="94e14-117">Описание</span><span class="sxs-lookup"><span data-stu-id="94e14-117">Description</span></span>

<span data-ttu-id="94e14-118">Это состояние инициирует один из двух процессов репликации: Отправка содержимого указанных папок в локальном хранилище или полная синхронизация.</span><span class="sxs-lookup"><span data-stu-id="94e14-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="94e14-119">При полной синхронизации для каждой из указанных папок содержимое загружается первыми, а затем загружается.</span><span class="sxs-lookup"><span data-stu-id="94e14-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="94e14-120">В зависимости от набора *ulFlags* в соответствующей структуре **[синхронизации](sync.md)** в предыдущем состоянии синхронизации Outlook инициализирует члены [out] структуры **синкконт** для предоставления сведений о содержимом.</span><span class="sxs-lookup"><span data-stu-id="94e14-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="94e14-121">С помощью той же структуры **синкконт** клиент получает количество папок, содержимое которых будет отправлено или загружено.</span><span class="sxs-lookup"><span data-stu-id="94e14-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="94e14-122">Клиент получит доступ к каждой из этих папок, переместив локальное хранилище в состояние таблицы отправки для отправки папки или переместив локальное хранилище в состояние загрузки таблицы, чтобы скачать эту папку.</span><span class="sxs-lookup"><span data-stu-id="94e14-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="94e14-123">Кроме того, клиент получает идентификаторы записей для папок, требующих репликации.</span><span class="sxs-lookup"><span data-stu-id="94e14-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="94e14-124">При завершении этого состояния Outlook Очищает внутреннюю информацию.</span><span class="sxs-lookup"><span data-stu-id="94e14-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="94e14-125">Локальное хранилище возвращается в состояние Synchronize.</span><span class="sxs-lookup"><span data-stu-id="94e14-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94e14-126">См. также</span><span class="sxs-lookup"><span data-stu-id="94e14-126">See also</span></span>



[<span data-ttu-id="94e14-127">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="94e14-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="94e14-128">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="94e14-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="94e14-129">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="94e14-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="94e14-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="94e14-130">SYNCSTATE</span></span>](syncstate.md)

