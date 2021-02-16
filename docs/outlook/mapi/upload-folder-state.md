---
title: Состояние папки отправки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419571"
---
# <a name="upload-folder-state"></a><span data-ttu-id="3a240-103">Состояние папки отправки</span><span class="sxs-lookup"><span data-stu-id="3a240-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="3a240-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a240-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3a240-105">В этом разделе описывается, что происходит во время состояния папки отправки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="3a240-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3a240-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3a240-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a240-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="3a240-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3a240-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="3a240-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="3a240-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="3a240-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3a240-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="3a240-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="3a240-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="3a240-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3a240-112">Состояние иерархии отправки</span><span class="sxs-lookup"><span data-stu-id="3a240-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="3a240-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="3a240-113">To this state:</span></span>  <br/> |<span data-ttu-id="3a240-114">Состояние иерархии отправки</span><span class="sxs-lookup"><span data-stu-id="3a240-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3a240-115">Этот автомат репликации является детерминируемым.</span><span class="sxs-lookup"><span data-stu-id="3a240-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3a240-116">Клиент, который уходит из одного состояния в другое, в конечном итоге должен вернуться к одному из последних.</span><span class="sxs-lookup"><span data-stu-id="3a240-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3a240-117">Описание</span><span class="sxs-lookup"><span data-stu-id="3a240-117">Description</span></span>

<span data-ttu-id="3a240-118">Это состояние инициирует отправку папки в иерархии, указанной в предыдущем состоянии иерархии отправки.</span><span class="sxs-lookup"><span data-stu-id="3a240-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="3a240-119">В этом состоянии Outlook предоставляет объект папки (если он не был удален) и флаги, указывающие состояние папки (новая, перемещенная, измененная или удаленная) как часть соответствующей структуры данных **UPFLD.**</span><span class="sxs-lookup"><span data-stu-id="3a240-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="3a240-120">Затем клиент передает эти сведения на сервер.</span><span class="sxs-lookup"><span data-stu-id="3a240-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="3a240-121">Если отправка прошла успешно, клиент устанавливает *для ulFlags* в **UPFLD** **UPF_OK.**</span><span class="sxs-lookup"><span data-stu-id="3a240-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="3a240-122">Затем Outlook очищает внутренние сведения о запросе на отправку папки.</span><span class="sxs-lookup"><span data-stu-id="3a240-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="3a240-123">После окончания отправки папки локальное хранилище возвращается в состояние иерархии отправки.</span><span class="sxs-lookup"><span data-stu-id="3a240-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="3a240-124">На основе структуры **[UPHIER,](uphier.md)** соответствующей предыдущему состоянии иерархии отправки, Outlook определяет, следует ли продолжить отправку следующей папки и подготовиться к следующему состоянии папки отправки.</span><span class="sxs-lookup"><span data-stu-id="3a240-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3a240-125">Если клиенту необходимо отправить только одну папку, клиент может [](synchronize-state.md) инициировать репликацию в состоянии синхронизации без ввода состояния иерархии отправки.</span><span class="sxs-lookup"><span data-stu-id="3a240-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="3a240-126">Клиент задает определенные члены **[SYNC](sync.md)** ( *ulFlags* для UPS_UPLOAD_ONLY и **UPS_ONE_FOLDER** и feid в *ID* папки), чтобы сообщить Outlook, что будет загружена только одна папка. </span><span class="sxs-lookup"><span data-stu-id="3a240-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a240-127">См. также</span><span class="sxs-lookup"><span data-stu-id="3a240-127">See also</span></span>



[<span data-ttu-id="3a240-128">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="3a240-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3a240-129">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="3a240-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3a240-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="3a240-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3a240-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="3a240-131">SYNCSTATE</span></span>](syncstate.md)

