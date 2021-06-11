---
title: Upload Состояние чтения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431542"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="4ef99-103">Upload Состояние чтения</span><span class="sxs-lookup"><span data-stu-id="4ef99-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="4ef99-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ef99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4ef99-105">В этом разделе описывается, что происходит во время состояния загрузки состояния чтения на компьютере состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="4ef99-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4ef99-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4ef99-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ef99-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="4ef99-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4ef99-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="4ef99-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="4ef99-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="4ef99-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4ef99-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="4ef99-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="4ef99-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="4ef99-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4ef99-112">Upload таблицы</span><span class="sxs-lookup"><span data-stu-id="4ef99-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="4ef99-113">Для этого состояния:</span><span class="sxs-lookup"><span data-stu-id="4ef99-113">To this state:</span></span>  <br/> |<span data-ttu-id="4ef99-114">Upload таблицы</span><span class="sxs-lookup"><span data-stu-id="4ef99-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4ef99-115">Машина состояния репликации — это детерминистический автомат состояния.</span><span class="sxs-lookup"><span data-stu-id="4ef99-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4ef99-116">Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего.</span><span class="sxs-lookup"><span data-stu-id="4ef99-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4ef99-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4ef99-117">Description</span></span>

<span data-ttu-id="4ef99-118">Это состояние инициирует загрузку состояния чтения элементов в папке, указанной в предыдущем состоянии таблицы отправки.</span><span class="sxs-lookup"><span data-stu-id="4ef99-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="4ef99-119">В этом состоянии Outlook связанную структуру данных **UPREAD** с информацией для тех элементов в папке, состояние чтения которых изменилось.</span><span class="sxs-lookup"><span data-stu-id="4ef99-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="4ef99-120">Затем клиент обновляет состояние чтения этих элементов на сервере как прочитанные или непрочитанные.</span><span class="sxs-lookup"><span data-stu-id="4ef99-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="4ef99-121">Когда это состояние заканчивается, Outlook очищает внутреннюю информацию о состоянии чтения элемента, не мешая повторной загрузке состояния чтения элемента.</span><span class="sxs-lookup"><span data-stu-id="4ef99-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="4ef99-122">Локальный магазин возвращается в состояние таблицы загрузки.</span><span class="sxs-lookup"><span data-stu-id="4ef99-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ef99-123">См. также</span><span class="sxs-lookup"><span data-stu-id="4ef99-123">See also</span></span>



[<span data-ttu-id="4ef99-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="4ef99-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4ef99-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="4ef99-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4ef99-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="4ef99-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4ef99-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4ef99-127">SYNCSTATE</span></span>](syncstate.md)

