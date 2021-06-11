---
title: Upload Удаление состояния
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
# <a name="upload-delete-status-state"></a><span data-ttu-id="ff4de-103">Upload Удаление состояния</span><span class="sxs-lookup"><span data-stu-id="ff4de-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="ff4de-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff4de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ff4de-105">В этом разделе описывается, что происходит при удалении состояния удаления состояния машины репликации.</span><span class="sxs-lookup"><span data-stu-id="ff4de-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ff4de-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ff4de-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff4de-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="ff4de-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="ff4de-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="ff4de-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="ff4de-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="ff4de-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="ff4de-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="ff4de-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="ff4de-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="ff4de-111">From this state:</span></span>  <br/> |[<span data-ttu-id="ff4de-112">Upload таблицы</span><span class="sxs-lookup"><span data-stu-id="ff4de-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="ff4de-113">Для этого состояния:</span><span class="sxs-lookup"><span data-stu-id="ff4de-113">To this state:</span></span>  <br/> |<span data-ttu-id="ff4de-114">Upload таблицы</span><span class="sxs-lookup"><span data-stu-id="ff4de-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ff4de-115">Машина состояния репликации — это детерминистический автомат состояния.</span><span class="sxs-lookup"><span data-stu-id="ff4de-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="ff4de-116">Клиент, отправляющийся из одного состояния в другое, должен в конечном итоге вернуться в первое из последнего.</span><span class="sxs-lookup"><span data-stu-id="ff4de-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="ff4de-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ff4de-117">Description</span></span>

<span data-ttu-id="ff4de-118">Это состояние инициирует обновление на сервере Outlook элементов (почты, календаря, контакта, задачи, заметки или журнала), удаленных в папке локального магазина, указанной в предыдущем состоянии таблицы загрузки.</span><span class="sxs-lookup"><span data-stu-id="ff4de-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="ff4de-119">В этом состоянии Outlook инициализирует членов связанной структуры данных **UPDEL** с информацией об удаленных или перемещенных из папки элементов.</span><span class="sxs-lookup"><span data-stu-id="ff4de-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="ff4de-120">Затем клиент удаляет указанные элементы в папке на сервере.</span><span class="sxs-lookup"><span data-stu-id="ff4de-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="ff4de-121">Чтобы различать элементы, которые были перемещены, а не удалены, клиент должен проверить членов *pupmov,* идентифицированных в **структуре UPDEL.**</span><span class="sxs-lookup"><span data-stu-id="ff4de-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="ff4de-122">Когда это состояние заканчивается, Outlook удаляет внутреннюю информацию, указывающее, что элемент удален; следовательно, Outlook больше не будет иметь записи элемента.</span><span class="sxs-lookup"><span data-stu-id="ff4de-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="ff4de-123">Локальный магазин возвращается в состояние таблицы загрузки.</span><span class="sxs-lookup"><span data-stu-id="ff4de-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff4de-124">См. также</span><span class="sxs-lookup"><span data-stu-id="ff4de-124">See also</span></span>



[<span data-ttu-id="ff4de-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="ff4de-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ff4de-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="ff4de-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ff4de-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="ff4de-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ff4de-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="ff4de-128">SYNCSTATE</span></span>](syncstate.md)

