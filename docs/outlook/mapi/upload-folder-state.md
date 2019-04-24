---
title: Отправка состояния папки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348428"
---
# <a name="upload-folder-state"></a><span data-ttu-id="8b761-103">Отправка состояния папки</span><span class="sxs-lookup"><span data-stu-id="8b761-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="8b761-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b761-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8b761-105">В этом разделе описывается, что происходит во время состояния папки отправки для конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="8b761-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8b761-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8b761-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b761-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="8b761-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="8b761-108">**ЛР_СИНК_УПЛОАД_ФОЛДЕР**</span><span class="sxs-lookup"><span data-stu-id="8b761-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="8b761-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="8b761-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="8b761-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="8b761-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="8b761-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="8b761-111">From this state:</span></span>  <br/> |[<span data-ttu-id="8b761-112">Состояние отправки иерархии</span><span class="sxs-lookup"><span data-stu-id="8b761-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="8b761-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="8b761-113">To this state:</span></span>  <br/> |<span data-ttu-id="8b761-114">Состояние отправки иерархии</span><span class="sxs-lookup"><span data-stu-id="8b761-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8b761-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="8b761-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="8b761-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="8b761-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="8b761-117">Описание</span><span class="sxs-lookup"><span data-stu-id="8b761-117">Description</span></span>

<span data-ttu-id="8b761-118">Это состояние инициирует отправку папки в иерархию, которая была указана в предыдущем состоянии отправки иерархии.</span><span class="sxs-lookup"><span data-stu-id="8b761-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="8b761-119">В этом состоянии Outlook предоставляет объект Folder (если он не был удален) и флаги, указывающие состояние папки ("создать", "перемещено", "изменено" или "удалено") как часть соответствующей структуры данных **упфлд** .</span><span class="sxs-lookup"><span data-stu-id="8b761-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="8b761-120">Затем клиент отправляет эти сведения на сервер.</span><span class="sxs-lookup"><span data-stu-id="8b761-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="8b761-121">Если отправка выполнена успешно, клиент устанавливает *ulFlags* в **упфлд** в **упф_ок**.</span><span class="sxs-lookup"><span data-stu-id="8b761-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="8b761-122">Затем в Outlook выполняется очистка внутренних сведений о запросе на отправку папки.</span><span class="sxs-lookup"><span data-stu-id="8b761-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="8b761-123">При завершении отправки папки локальное хранилище возвращается в состояние иерархии отправки.</span><span class="sxs-lookup"><span data-stu-id="8b761-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="8b761-124">В зависимости от структуры **[уфиер](uphier.md)** , соответствующей предшествующему состоянию иерархии отправки, Outlook определяет, следует ли продолжить отправку следующей папки и подготовку к следующей папке отправки.</span><span class="sxs-lookup"><span data-stu-id="8b761-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8b761-125">Если клиенту требуется отправить только одну папку, клиент может инициировать репликацию с помощью [состояния Synchronize](synchronize-state.md) без ввода состояния иерархии отправки.</span><span class="sxs-lookup"><span data-stu-id="8b761-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="8b761-126">Клиент устанавливает определенные элементы **[синхронизации](sync.md)** — *ulFlags* в **упс_уплоад_онли** и **упс_оне_фолдер** и *феид* в идентификатор папки, чтобы сообщить Outlook, что будет отправлена только одна папка.</span><span class="sxs-lookup"><span data-stu-id="8b761-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b761-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8b761-127">See also</span></span>



[<span data-ttu-id="8b761-128">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="8b761-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8b761-129">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="8b761-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8b761-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="8b761-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8b761-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="8b761-131">SYNCSTATE</span></span>](syncstate.md)

