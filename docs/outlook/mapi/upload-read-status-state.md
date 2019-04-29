---
title: Состояние отправки состояния чтения
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
# <a name="upload-read-status-state"></a><span data-ttu-id="6d497-103">Состояние отправки состояния чтения</span><span class="sxs-lookup"><span data-stu-id="6d497-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="6d497-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d497-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="6d497-105">В этом разделе описывается, что происходит во время отправки состояния прочтения конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="6d497-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="6d497-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="6d497-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d497-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="6d497-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="6d497-108">**ЛР_СИНК_УПЛОАД_МЕССАЖЕ_РЕАД**</span><span class="sxs-lookup"><span data-stu-id="6d497-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="6d497-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="6d497-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="6d497-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="6d497-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="6d497-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="6d497-111">From this state:</span></span>  <br/> |[<span data-ttu-id="6d497-112">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="6d497-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="6d497-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="6d497-113">To this state:</span></span>  <br/> |<span data-ttu-id="6d497-114">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="6d497-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6d497-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="6d497-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="6d497-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="6d497-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="6d497-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6d497-117">Description</span></span>

<span data-ttu-id="6d497-118">Это состояние инициирует отправку состояния чтения элементов в папке, указанной в предыдущем состоянии таблицы отправки.</span><span class="sxs-lookup"><span data-stu-id="6d497-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="6d497-119">В этом состоянии Outlook инициализирует связанную структуру \*\*\*\* данных с данными для тех элементов в папке, состояние чтения которых изменилось.</span><span class="sxs-lookup"><span data-stu-id="6d497-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="6d497-120">Затем клиент обновляет состояние чтения этих элементов на сервере как прочитанное или непрочтенное.</span><span class="sxs-lookup"><span data-stu-id="6d497-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="6d497-121">При завершении этого состояния Outlook Очищает внутреннюю информацию о состоянии чтения элемента, предотвращая отправку состояния чтения элемента.</span><span class="sxs-lookup"><span data-stu-id="6d497-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="6d497-122">Локальное хранилище возвращается в состояние таблицы отправки.</span><span class="sxs-lookup"><span data-stu-id="6d497-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d497-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6d497-123">See also</span></span>



[<span data-ttu-id="6d497-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="6d497-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="6d497-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="6d497-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="6d497-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="6d497-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="6d497-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="6d497-127">SYNCSTATE</span></span>](syncstate.md)

