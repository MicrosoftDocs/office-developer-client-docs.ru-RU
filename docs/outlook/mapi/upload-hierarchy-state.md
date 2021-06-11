---
title: Upload Состояние иерархии
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415427"
---
# <a name="upload-hierarchy-state"></a><span data-ttu-id="9eb31-103">Upload Состояние иерархии</span><span class="sxs-lookup"><span data-stu-id="9eb31-103">Upload Hierarchy State</span></span>

  
  
<span data-ttu-id="9eb31-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9eb31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9eb31-105">В этом разделе описывается, что происходит во время состояния иерархии загрузки машины состояния репликации.</span><span class="sxs-lookup"><span data-stu-id="9eb31-105">This topic describes what happens during the upload hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9eb31-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9eb31-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9eb31-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="9eb31-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9eb31-108">**LR_SYNC_UPLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="9eb31-108">**LR_SYNC_UPLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="9eb31-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="9eb31-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="9eb31-110">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="9eb31-110">**[UPHIER](uphier.md)**</span></span> <br/> |
|<span data-ttu-id="9eb31-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="9eb31-111">From this state:</span></span>  <br/> |[<span data-ttu-id="9eb31-112">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="9eb31-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="9eb31-113">Для этого состояния:</span><span class="sxs-lookup"><span data-stu-id="9eb31-113">To this state:</span></span>  <br/> |<span data-ttu-id="9eb31-114">[Upload состояния папки](upload-folder-state.md)или состояния синхронизации</span><span class="sxs-lookup"><span data-stu-id="9eb31-114">[Upload folder state](upload-folder-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="9eb31-115">Машина состояния репликации — это детерминистический автомат состояния.</span><span class="sxs-lookup"><span data-stu-id="9eb31-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9eb31-116">Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего.</span><span class="sxs-lookup"><span data-stu-id="9eb31-116">A client departing one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9eb31-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9eb31-117">Description</span></span>

<span data-ttu-id="9eb31-118">Это состояние инициирует отправку иерархии дерева папок, указанной в предыдущем состоянии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9eb31-118">This state initiates uploading a folder tree hierarchy that has been specified in a preceding synchronize state.</span></span> <span data-ttu-id="9eb31-119">Outlook определяет количество папок, созданных или измененных в этой иерархии, и инициализирует *cEnt* в **UPHIER.**</span><span class="sxs-lookup"><span data-stu-id="9eb31-119">Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**.</span></span> <span data-ttu-id="9eb31-120">Outlook также сохраняет количество загруженных папок с другим участником *iEnt* .</span><span class="sxs-lookup"><span data-stu-id="9eb31-120">Outlook also keeps a count of the number of uploaded folders with another member  *iEnt*  .</span></span> <span data-ttu-id="9eb31-121">Чтобы загрузить каждую из папок  *cEnt,*  клиент перемещает локальный магазин в состояние папки отправки, возвращаясь в состояние иерархии отправки после завершения загрузки папки.</span><span class="sxs-lookup"><span data-stu-id="9eb31-121">To upload each of the  *cEnt*  folders, the client moves the local store into the upload folder state, returning to the upload hierarchy state when the folder upload finishes.</span></span> 
  
<span data-ttu-id="9eb31-122">После окончания состояния иерархии загрузки локальный магазин возвращается в состояние синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9eb31-122">When the upload hierarchy state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9eb31-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9eb31-123">See also</span></span>



[<span data-ttu-id="9eb31-124">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="9eb31-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9eb31-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="9eb31-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9eb31-126">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="9eb31-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9eb31-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="9eb31-127">SYNCSTATE</span></span>](syncstate.md)

