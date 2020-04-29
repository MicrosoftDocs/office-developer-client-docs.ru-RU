---
title: Состояние отправки сообщения
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433803"
---
# <a name="upload-message-state"></a><span data-ttu-id="5c862-103">Состояние отправки сообщения</span><span class="sxs-lookup"><span data-stu-id="5c862-103">Upload Message State</span></span>

  
  
<span data-ttu-id="5c862-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5c862-105">В этом разделе описывается, что происходит во время отправки сообщения на конечный автомат репликации.</span><span class="sxs-lookup"><span data-stu-id="5c862-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5c862-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="5c862-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c862-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="5c862-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="5c862-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="5c862-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="5c862-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="5c862-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="5c862-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="5c862-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="5c862-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="5c862-111">From this state:</span></span>  <br/> |[<span data-ttu-id="5c862-112">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="5c862-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="5c862-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="5c862-113">To this state:</span></span>  <br/> |<span data-ttu-id="5c862-114">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="5c862-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="5c862-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="5c862-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="5c862-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="5c862-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="5c862-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5c862-117">Description</span></span>

<span data-ttu-id="5c862-118">Это состояние инициирует отправку элемента Outlook ("почта", "Календарь", "контакт", "заметка" или "журнал"), который является новым или перемещен в текущую папку или изменен.</span><span class="sxs-lookup"><span data-stu-id="5c862-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="5c862-119">Outlook Инициализирует структуру данных коррепсондинг **упмсг** с соответствующей информацией о том, что элемент добавлен, перемещен или изменен.</span><span class="sxs-lookup"><span data-stu-id="5c862-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="5c862-120">Если элемент был добавлен или перемещен, клиент соответствующим образом добавляет или обновляет элемент на сервере.</span><span class="sxs-lookup"><span data-stu-id="5c862-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="5c862-121">Если элемент был изменен, Outlook дополнительно указывает в структуре данных **упмсг** , находятся ли изменения в заголовке сообщения (в случае, если элемент является заголовком сообщения), в свойствах элемента или в самом элементе, для которого требуется разрешение конфликтов.</span><span class="sxs-lookup"><span data-stu-id="5c862-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="5c862-122">Затем клиент обновляет элемент на сервере.</span><span class="sxs-lookup"><span data-stu-id="5c862-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="5c862-123">При завершении отправки элемента Outlook запишет сообщение, чтобы оно не было обработано при последующей отправке.</span><span class="sxs-lookup"><span data-stu-id="5c862-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="5c862-124">Локальное хранилище возвращается в состояние таблицы отправки.</span><span class="sxs-lookup"><span data-stu-id="5c862-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c862-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5c862-125">See also</span></span>



[<span data-ttu-id="5c862-126">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="5c862-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="5c862-127">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="5c862-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5c862-128">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="5c862-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5c862-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="5c862-129">SYNCSTATE</span></span>](syncstate.md)

