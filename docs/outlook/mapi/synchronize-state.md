---
title: Состояние синхронизации
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414629"
---
# <a name="synchronize-state"></a><span data-ttu-id="0db8c-103">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="0db8c-103">Synchronize State</span></span>

  
  
<span data-ttu-id="0db8c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0db8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="0db8c-105">В этом разделе описывается, что происходит во время синхронизации состояния конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="0db8c-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="0db8c-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="0db8c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0db8c-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="0db8c-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="0db8c-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="0db8c-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="0db8c-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="0db8c-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="0db8c-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="0db8c-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="0db8c-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="0db8c-111">From this state:</span></span>  <br/> |[<span data-ttu-id="0db8c-112">Состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="0db8c-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="0db8c-113">В этом состоянии:</span><span class="sxs-lookup"><span data-stu-id="0db8c-113">To this state:</span></span>  <br/> |<span data-ttu-id="0db8c-114">[Скачивание состояния иерархии,](download-hierarchy-state.md) [синхронизация состояния содержимого,](synchronize-contents-state.md)состояние [иерархии отправки](upload-hierarchy-state.md)или состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="0db8c-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="0db8c-115">Этот автомат репликации является детерминируемым.</span><span class="sxs-lookup"><span data-stu-id="0db8c-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="0db8c-116">Клиент, который уходит из одного состояния в другое, в конечном итоге должен вернуться к одному из последних.</span><span class="sxs-lookup"><span data-stu-id="0db8c-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="0db8c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0db8c-117">Description</span></span>

<span data-ttu-id="0db8c-118">Это состояние инициирует синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="0db8c-118">This state initiates synchronization.</span></span> <span data-ttu-id="0db8c-119">Локальное хранилище может перейти в состояние отправки или скачивания отсюда.</span><span class="sxs-lookup"><span data-stu-id="0db8c-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="0db8c-120">Например, локальное хранилище может перейти в состояние иерархии отправки для отправки иерархии папок на сервер или выполнить полную синхронизацию, сначала загрузив иерархию с сервера.</span><span class="sxs-lookup"><span data-stu-id="0db8c-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="0db8c-121">В этом состоянии Outlook инициализирует связанную структуру данных **SYNC** с путем к локальному хранилище, чтобы Outlook видел изменения во время других состояниях.</span><span class="sxs-lookup"><span data-stu-id="0db8c-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="0db8c-122">Клиент задает члены SYNC [in], которые сообщает Outlook, как обрабатывать другие состояния.</span><span class="sxs-lookup"><span data-stu-id="0db8c-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="0db8c-123">Например, клиент может установить для *ulFlags* UPS_UPLOAD_ONLY и **UPS_THESE_FOLDERS** *pel* список идентификаторов записей папок, чтобы сообщить Outlook, что будут загружены только эти папки. </span><span class="sxs-lookup"><span data-stu-id="0db8c-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="0db8c-124">После окончания этого состояния локальное хранилище возвращается в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="0db8c-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0db8c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0db8c-125">See also</span></span>



[<span data-ttu-id="0db8c-126">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="0db8c-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="0db8c-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="0db8c-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0db8c-128">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="0db8c-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="0db8c-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="0db8c-129">SYNCSTATE</span></span>](syncstate.md)

