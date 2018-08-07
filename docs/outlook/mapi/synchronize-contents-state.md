---
title: Состояние синхронизации содержимого
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 216691f2c1f94d658a5aa968d6a19148a9b3c06a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812442"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="d9dbd-103">Состояние синхронизации содержимого</span><span class="sxs-lookup"><span data-stu-id="d9dbd-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="d9dbd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9dbd-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="d9dbd-105">В этом разделе описываются двоичных файлов состояния содержимое синхронизировать конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d9dbd-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d9dbd-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9dbd-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="d9dbd-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="d9dbd-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="d9dbd-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="d9dbd-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="d9dbd-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="d9dbd-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="d9dbd-111">From this state:</span></span>  <br/> |[<span data-ttu-id="d9dbd-112">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="d9dbd-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="d9dbd-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="d9dbd-113">To this state:</span></span>  <br/> |<span data-ttu-id="d9dbd-114">[Загрузить в таблице состояния](download-table-state.md), [Отправка состояний в таблице](upload-table-state.md), или синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="d9dbd-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="d9dbd-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="d9dbd-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="d9dbd-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d9dbd-117">Description</span></span>

<span data-ttu-id="d9dbd-118">Это состояние означает инициируется один из двух процессов репликации: отправка содержимого заданной папки локального хранилища или полной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="d9dbd-119">В полной синхронизации для каждой указанной папки содержимое сначала загружаются и загружаются.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="d9dbd-120">В зависимости от *ulFlags* в структуре соответствующего **[СИНХРОНИЗАЦИИ](sync.md)** в предыдущем установите синхронизировать состояние, Outlook инициализирует [элементы в структуре **SYNCCONT** для предоставления сведений о содержимом out].</span><span class="sxs-lookup"><span data-stu-id="d9dbd-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="d9dbd-121">По той же структурой **SYNCCONT** клиент получает число папок, для которых материалы для загрузки или отправки.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="d9dbd-122">Клиент будет выполняют цикл по каждой из этих папок перемещение локального хранилища в состояние таблицы отправить отправка в папку и перемещение локального хранилища в таблице состояние загрузки можно загрузить в папку.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="d9dbd-123">Кроме того клиент получает запись идентификаторы для папки, требующие репликации.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="d9dbd-124">По окончании этого состояния Outlook очищает внутренние сведения.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="d9dbd-125">Локальное хранилище возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d9dbd-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d9dbd-126">See also</span></span>



[<span data-ttu-id="d9dbd-127">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="d9dbd-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d9dbd-128">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="d9dbd-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d9dbd-129">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="d9dbd-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d9dbd-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="d9dbd-130">SYNCSTATE</span></span>](syncstate.md)

