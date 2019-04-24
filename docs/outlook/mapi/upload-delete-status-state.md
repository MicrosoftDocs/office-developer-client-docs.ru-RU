---
title: Состояние отправки состояния удаления
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357710"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="c8a7c-103">Состояние отправки состояния удаления</span><span class="sxs-lookup"><span data-stu-id="c8a7c-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="c8a7c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8a7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="c8a7c-105">В этом разделе описывается, что происходит во время отправки состояния удаления для конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="c8a7c-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c8a7c-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c8a7c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8a7c-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="c8a7c-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="c8a7c-108">**ЛР_СИНК_УПЛОАД_МЕССАЖЕ_ДЕЛ**</span><span class="sxs-lookup"><span data-stu-id="c8a7c-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="c8a7c-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="c8a7c-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="c8a7c-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="c8a7c-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="c8a7c-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="c8a7c-111">From this state:</span></span>  <br/> |[<span data-ttu-id="c8a7c-112">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="c8a7c-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="c8a7c-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="c8a7c-113">To this state:</span></span>  <br/> |<span data-ttu-id="c8a7c-114">Состояние отправки таблицы</span><span class="sxs-lookup"><span data-stu-id="c8a7c-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="c8a7c-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="c8a7c-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="c8a7c-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="c8a7c-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="c8a7c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c8a7c-117">Description</span></span>

<span data-ttu-id="c8a7c-118">Это состояние инициирует обновление на сервере, который содержит элементы Outlook (почта, календарь, контакт, задача, Примечание или журнал), которые были удалены в папке в локальном хранилище, указанном в предыдущем состоянии таблицы отправки.</span><span class="sxs-lookup"><span data-stu-id="c8a7c-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="c8a7c-119">В этом состоянии Outlook инициализирует элементы в связанной структуре данных **упдел** информацией об элементах, которые были удалены или перемещены из папки.</span><span class="sxs-lookup"><span data-stu-id="c8a7c-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="c8a7c-120">Затем клиент удаляет указанные элементы из папки на сервере.</span><span class="sxs-lookup"><span data-stu-id="c8a7c-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="c8a7c-121">Чтобы отличать элементы, которые были перемещены в отличие от удаления, клиент должен проверить элементы *пупмов* , определенные в структуре **упдел** .</span><span class="sxs-lookup"><span data-stu-id="c8a7c-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="c8a7c-122">При завершении этого состояния Outlook Очищает внутреннюю информацию, указывающую на то, что элемент был удален; Поэтому в Outlook больше не будет записей об элементе.</span><span class="sxs-lookup"><span data-stu-id="c8a7c-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="c8a7c-123">Локальное хранилище возвращается в состояние таблицы отправки.</span><span class="sxs-lookup"><span data-stu-id="c8a7c-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c8a7c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c8a7c-124">See also</span></span>



[<span data-ttu-id="c8a7c-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="c8a7c-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c8a7c-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="c8a7c-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c8a7c-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="c8a7c-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c8a7c-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="c8a7c-128">SYNCSTATE</span></span>](syncstate.md)

