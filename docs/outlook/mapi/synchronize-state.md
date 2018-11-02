---
title: Состояние синхронизации
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d9f2a11a9ec1691863b476fed02eff1831a69207
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569724"
---
# <a name="synchronize-state"></a><span data-ttu-id="a987e-103">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="a987e-103">Synchronize State</span></span>

  
  
<span data-ttu-id="a987e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a987e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a987e-105">В этом разделе описываются двоичных файлов синхронизировать состояние конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="a987e-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a987e-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a987e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a987e-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="a987e-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a987e-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="a987e-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="a987e-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="a987e-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a987e-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="a987e-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="a987e-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="a987e-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a987e-112">Состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="a987e-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="a987e-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="a987e-113">To this state:</span></span>  <br/> |<span data-ttu-id="a987e-114">[Загрузите иерархия состояний](download-hierarchy-state.md), [синхронизировать состояние содержимого](synchronize-contents-state.md), [Отправка иерархия состояний](upload-hierarchy-state.md)или состояние простоя</span><span class="sxs-lookup"><span data-stu-id="a987e-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a987e-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="a987e-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a987e-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="a987e-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a987e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a987e-117">Description</span></span>

<span data-ttu-id="a987e-118">Это состояние означает инициирует синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a987e-118">This state initiates synchronization.</span></span> <span data-ttu-id="a987e-119">Локальное хранилище может переносить для отправки или загрузки состояния здесь.</span><span class="sxs-lookup"><span data-stu-id="a987e-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="a987e-120">Например его можно выполнить полную синхронизацию, первый Отправка иерархии и иерархии с сервера, или переместить локального хранилища состояний иерархии отправки отправка иерархии папок на сервере.</span><span class="sxs-lookup"><span data-stu-id="a987e-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="a987e-121">Во время это состояние означает Outlook инициализирует связанной структуры данных **СИНХРОНИЗАЦИИ** с путь к локальному хранилищу, поэтому Outlook видит изменения во время другие состояния.</span><span class="sxs-lookup"><span data-stu-id="a987e-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="a987e-122">[In] Задает клиент члены **СИНХРОНИЗАЦИИ**, который сообщает Outlook, как обрабатывать другие состояния.</span><span class="sxs-lookup"><span data-stu-id="a987e-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="a987e-123">Например клиента можно установить *ulFlags* **UPS_UPLOAD_ONLY** и **UPS_THESE_FOLDERS** и будут отправлены *pel* со списком идентификаторы записей из папок, чтобы сообщить, что только этих папок Outlook.</span><span class="sxs-lookup"><span data-stu-id="a987e-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="a987e-124">По окончании этого состояния локального хранилища возвращается к состояния простоя.</span><span class="sxs-lookup"><span data-stu-id="a987e-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a987e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a987e-125">See also</span></span>



[<span data-ttu-id="a987e-126">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="a987e-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a987e-127">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="a987e-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a987e-128">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="a987e-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a987e-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a987e-129">SYNCSTATE</span></span>](syncstate.md)

