---
title: Состояние отправки статуса чтения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812560"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="eb6d6-103">Состояние отправки статуса чтения</span><span class="sxs-lookup"><span data-stu-id="eb6d6-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="eb6d6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb6d6-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="eb6d6-105">В этом разделе описывается, что происходит во время загрузки, прочитайте состояния состояние конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="eb6d6-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="eb6d6-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="eb6d6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb6d6-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="eb6d6-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="eb6d6-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="eb6d6-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="eb6d6-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="eb6d6-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="eb6d6-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="eb6d6-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="eb6d6-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="eb6d6-111">From this state:</span></span>  <br/> |[<span data-ttu-id="eb6d6-112">Отправка состояний в таблице</span><span class="sxs-lookup"><span data-stu-id="eb6d6-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="eb6d6-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="eb6d6-113">To this state:</span></span>  <br/> |<span data-ttu-id="eb6d6-114">Отправка состояний в таблице</span><span class="sxs-lookup"><span data-stu-id="eb6d6-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="eb6d6-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="eb6d6-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="eb6d6-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="eb6d6-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="eb6d6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="eb6d6-117">Description</span></span>

<span data-ttu-id="eb6d6-118">Это состояние означает инициирует отправку состояние чтения элементов в папке, указанной в предыдущего состояния в таблице отправить.</span><span class="sxs-lookup"><span data-stu-id="eb6d6-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="eb6d6-119">В этом состоянии Outlook инициализирует связанной структуры данных **UPREAD** со сведениями для этих элементов в папке чтения, состояние которого был изменен.</span><span class="sxs-lookup"><span data-stu-id="eb6d6-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="eb6d6-120">Клиент затем обновляет состояние чтения этих элементов на сервере как прочитан или не прочитан.</span><span class="sxs-lookup"><span data-stu-id="eb6d6-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="eb6d6-121">По окончании этого состояния Outlook очищает внутренние сведения о состоянии чтение элемента, предотвращения выгружаемого еще раз состояние чтения элемента.</span><span class="sxs-lookup"><span data-stu-id="eb6d6-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="eb6d6-122">Локальное хранилище возвращается в состояние таблицы отправить.</span><span class="sxs-lookup"><span data-stu-id="eb6d6-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb6d6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="eb6d6-123">See also</span></span>



[<span data-ttu-id="eb6d6-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="eb6d6-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="eb6d6-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="eb6d6-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="eb6d6-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="eb6d6-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="eb6d6-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="eb6d6-127">SYNCSTATE</span></span>](syncstate.md)

