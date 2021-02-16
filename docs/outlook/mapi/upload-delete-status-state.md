---
title: Отправка состояния удаления
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425843"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="9085c-103">Отправка состояния удаления</span><span class="sxs-lookup"><span data-stu-id="9085c-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="9085c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9085c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9085c-105">В этом разделе описывается, что происходит во время отправки состояния удаления конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="9085c-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="9085c-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9085c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9085c-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="9085c-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="9085c-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="9085c-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="9085c-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="9085c-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="9085c-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="9085c-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="9085c-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="9085c-111">From this state:</span></span>  <br/> |[<span data-ttu-id="9085c-112">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="9085c-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="9085c-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="9085c-113">To this state:</span></span>  <br/> |<span data-ttu-id="9085c-114">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="9085c-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="9085c-115">Этот автомат репликации является детерминируемым.</span><span class="sxs-lookup"><span data-stu-id="9085c-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="9085c-116">Клиент, который уходит из одного состояния в другое, в конечном итоге должен вернуться к одному из последних.</span><span class="sxs-lookup"><span data-stu-id="9085c-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="9085c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9085c-117">Description</span></span>

<span data-ttu-id="9085c-118">Это состояние инициирует обновление на сервере тех элементов Outlook (почты, календаря, контакта, задачи, заметки или журнала), которые были удалены в папке в локальном хранилище, указанном в предыдущем состоянии отправки таблицы.</span><span class="sxs-lookup"><span data-stu-id="9085c-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="9085c-119">В этом состоянии Outlook инициализирует элементы в связанной структуре **данных UPDEL** с информацией для элементов, которые были удалены или перемещены из папки.</span><span class="sxs-lookup"><span data-stu-id="9085c-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="9085c-120">Затем клиент удаляет указанные элементы в папке на сервере.</span><span class="sxs-lookup"><span data-stu-id="9085c-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="9085c-121">Чтобы различать элементы, которые были перемещены, а не были удалены, клиент должен проверить элементы *pupmov,* выявленные в **структуре UPDEL.**</span><span class="sxs-lookup"><span data-stu-id="9085c-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="9085c-122">Когда это состояние завершается, Outlook очищает внутренние данные, указывающие на то, что элемент был удален; следовательно, в Outlook больше не будет записи элемента.</span><span class="sxs-lookup"><span data-stu-id="9085c-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="9085c-123">Локальное хранилище возвращается в состояние отправки таблицы.</span><span class="sxs-lookup"><span data-stu-id="9085c-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9085c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="9085c-124">See also</span></span>



[<span data-ttu-id="9085c-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="9085c-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9085c-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="9085c-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9085c-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="9085c-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9085c-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="9085c-128">SYNCSTATE</span></span>](syncstate.md)

