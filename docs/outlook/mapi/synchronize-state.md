---
title: Состояние синхронизации
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349513"
---
# <a name="synchronize-state"></a><span data-ttu-id="79832-103">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="79832-103">Synchronize State</span></span>

  
  
<span data-ttu-id="79832-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79832-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="79832-105">В этом разделе описывается, что происходит во время синхронизации конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="79832-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="79832-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="79832-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79832-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="79832-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="79832-108">**ЛР_СИНК**</span><span class="sxs-lookup"><span data-stu-id="79832-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="79832-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="79832-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="79832-110">**[Синхр](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="79832-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="79832-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="79832-111">From this state:</span></span>  <br/> |[<span data-ttu-id="79832-112">Состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="79832-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="79832-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="79832-113">To this state:</span></span>  <br/> |<span data-ttu-id="79832-114">[Загрузка состояния иерархии](download-hierarchy-state.md), [Синхронизация состояния контента](synchronize-contents-state.md), [состояние иерархии отправки](upload-hierarchy-state.md)или состояние простоя</span><span class="sxs-lookup"><span data-stu-id="79832-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="79832-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="79832-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="79832-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="79832-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="79832-117">Описание</span><span class="sxs-lookup"><span data-stu-id="79832-117">Description</span></span>

<span data-ttu-id="79832-118">Это состояние инициирует синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="79832-118">This state initiates synchronization.</span></span> <span data-ttu-id="79832-119">Локальное хранилище может перейти к отправке или состоянию загрузки отсюда.</span><span class="sxs-lookup"><span data-stu-id="79832-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="79832-120">Например, локальное хранилище может перейти в состояние иерархии отправки, чтобы отправить иерархию папок на сервер, или выполнить полную синхронизацию, предварительно отправив иерархию, а затем загрузив иерархию с сервера.</span><span class="sxs-lookup"><span data-stu-id="79832-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="79832-121">В этом состоянии Outlook инициализирует связанную структуру данных **синхронизации** с путем к локальному хранилищу, поэтому Outlook видит изменения в других состояниях.</span><span class="sxs-lookup"><span data-stu-id="79832-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="79832-122">Клиент задает элементы **синхронизации**[in], которые сообщают Outlook, как обрабатывать другие состояния.</span><span class="sxs-lookup"><span data-stu-id="79832-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="79832-123">Например, клиент может установить *ulFlags* в **упс_уплоад_онли** и **упс_сесе_фолдерс** и *PEL* в список идентификаторов записей папок, чтобы сообщить Outlook о том, что будут отправлены только эти папки.</span><span class="sxs-lookup"><span data-stu-id="79832-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="79832-124">При завершении этого состояния локальное хранилище возвращается в состояние Idle.</span><span class="sxs-lookup"><span data-stu-id="79832-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79832-125">См. также</span><span class="sxs-lookup"><span data-stu-id="79832-125">See also</span></span>



[<span data-ttu-id="79832-126">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="79832-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="79832-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="79832-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="79832-128">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="79832-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="79832-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="79832-129">SYNCSTATE</span></span>](syncstate.md)

