---
title: Состояние отправки папки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae8c3c4012874e1ca35761b103066cceebb1b165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576752"
---
# <a name="upload-folder-state"></a><span data-ttu-id="e59d0-103">Состояние отправки папки</span><span class="sxs-lookup"><span data-stu-id="e59d0-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="e59d0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e59d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e59d0-105">В этом разделе описываются двоичных файлов состояние папки загрузки конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="e59d0-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e59d0-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e59d0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e59d0-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="e59d0-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e59d0-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="e59d0-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="e59d0-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="e59d0-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e59d0-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="e59d0-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="e59d0-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="e59d0-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e59d0-112">Отправка иерархия состояний</span><span class="sxs-lookup"><span data-stu-id="e59d0-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="e59d0-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="e59d0-113">To this state:</span></span>  <br/> |<span data-ttu-id="e59d0-114">Отправка иерархия состояний</span><span class="sxs-lookup"><span data-stu-id="e59d0-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e59d0-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="e59d0-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e59d0-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="e59d0-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e59d0-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e59d0-117">Description</span></span>

<span data-ttu-id="e59d0-118">Это состояние означает инициирует отправку папки в иерархии, который был указан в предыдущем состоянии иерархии отправить.</span><span class="sxs-lookup"><span data-stu-id="e59d0-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="e59d0-119">Во время этого состояния Outlook предоставляет объект папки (если она не была удалена) и флаги, указывающее состояние папки (новый, перемещены, изменены или удалены) как часть соответствующего структуры данных **UPFLD** .</span><span class="sxs-lookup"><span data-stu-id="e59d0-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="e59d0-120">Затем клиент передает эти сведения на сервер.</span><span class="sxs-lookup"><span data-stu-id="e59d0-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="e59d0-121">Если загрузка прошла успешно, клиент задает *ulFlags* в **UPFLD** для **UPF_OK**.</span><span class="sxs-lookup"><span data-stu-id="e59d0-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="e59d0-122">Затем Outlook очищает внутренние сведения о запросе для передачи в папку.</span><span class="sxs-lookup"><span data-stu-id="e59d0-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="e59d0-123">После завершения загрузки папки локального хранилища возвращается в состояние иерархии отправки.</span><span class="sxs-lookup"><span data-stu-id="e59d0-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="e59d0-124">В зависимости от структуры **[UPHIER](uphier.md)** , соответствующий в предыдущем состояние иерархии отправки Outlook определяет, следует ли продолжить отправку пользователями к следующей папке и для подготовки к следующее состояние папки загрузки.</span><span class="sxs-lookup"><span data-stu-id="e59d0-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e59d0-125">Если клиент должен только одна папка отправки, клиент может отправить репликации через [синхронизировать состояние](synchronize-state.md) без ввода состояние иерархии отправки.</span><span class="sxs-lookup"><span data-stu-id="e59d0-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="e59d0-126">Клиент задает некоторые члены **[СИНХРОНИЗАЦИИ](sync.md)** — *ulFlags* **UPS_UPLOAD_ONLY** и **UPS_ONE_FOLDER** и *feid* на идентификатор папки — чтобы сообщить Outlook, только одна папка будет отправлен.</span><span class="sxs-lookup"><span data-stu-id="e59d0-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e59d0-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e59d0-127">See also</span></span>



[<span data-ttu-id="e59d0-128">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="e59d0-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e59d0-129">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="e59d0-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e59d0-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="e59d0-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e59d0-131">СОСТОЯНИЕ</span><span class="sxs-lookup"><span data-stu-id="e59d0-131">SYNCSTATE</span></span>](syncstate.md)

