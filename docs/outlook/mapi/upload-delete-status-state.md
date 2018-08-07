---
title: Состояние отправки статуса удаления
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ff957e649d5de64c65ac169b3bc413ac7b6c9491
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812557"
---
# <a name="upload-delete-status-state"></a><span data-ttu-id="25bce-103">Состояние отправки статуса удаления</span><span class="sxs-lookup"><span data-stu-id="25bce-103">Upload Delete Status State</span></span>

  
  
<span data-ttu-id="25bce-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="25bce-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="25bce-105">В этом разделе описывается, что происходит во время загрузки удалить состояние состояние конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="25bce-105">This topic describes what happens during the upload delete status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="25bce-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="25bce-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25bce-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="25bce-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="25bce-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span><span class="sxs-lookup"><span data-stu-id="25bce-108">**LR_SYNC_UPLOAD_MESSAGE_DEL**</span></span> <br/> |
|<span data-ttu-id="25bce-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="25bce-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="25bce-110">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="25bce-110">**[UPDEL](updel.md)**</span></span> <br/> |
|<span data-ttu-id="25bce-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="25bce-111">From this state:</span></span>  <br/> |[<span data-ttu-id="25bce-112">Отправка состояний в таблице</span><span class="sxs-lookup"><span data-stu-id="25bce-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="25bce-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="25bce-113">To this state:</span></span>  <br/> |<span data-ttu-id="25bce-114">Отправка состояний в таблице</span><span class="sxs-lookup"><span data-stu-id="25bce-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="25bce-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="25bce-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="25bce-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="25bce-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="25bce-117">Описание</span><span class="sxs-lookup"><span data-stu-id="25bce-117">Description</span></span>

<span data-ttu-id="25bce-118">Это состояние означает инициирует обновление на сервере этих элементов Outlook (почту, календарь, контактов, задач, примечание или журнала), которые были удалены в папке локального хранилища, указанных выше состояние таблицы отправить.</span><span class="sxs-lookup"><span data-stu-id="25bce-118">This state initiates updating on a server those Outlook items (mail, calendar, contact, task, note, or journal) that have been deleted in a folder on a local store specified in a preceding upload table state.</span></span> <span data-ttu-id="25bce-119">В этом состоянии Outlook инициализирует элементы в структуре данных связанного **UPDEL** сведения для элементов, которые были удалены или перемещены в папке.</span><span class="sxs-lookup"><span data-stu-id="25bce-119">During this state, Outlook initializes members in the associated **UPDEL** data structure with information for the items that have been deleted or moved from the folder.</span></span> 
  
<span data-ttu-id="25bce-120">Клиент затем удаляет заданные элементы в папке на сервере.</span><span class="sxs-lookup"><span data-stu-id="25bce-120">The client then deletes the specified items in the folder on the server.</span></span> <span data-ttu-id="25bce-121">Для различения элементов, которые были перемещены в отличие от был удален, клиент должен проверить *pupmov* элементов, определенный в структуре **UPDEL** .</span><span class="sxs-lookup"><span data-stu-id="25bce-121">To distinguish items that have been moved as opposed to having been deleted, the client must check the  *pupmov*  members identified in the **UPDEL** structure.</span></span> 
  
<span data-ttu-id="25bce-122">По окончании этого состояния Outlook очищает внутренние сведения, указывающего на то, что элемент был удален; Следовательно Outlook больше не будет предоставляться запись элемента.</span><span class="sxs-lookup"><span data-stu-id="25bce-122">When this state ends, Outlook clears the internal information indicating that the item has been deleted; consequently, Outlook will no longer have a record of the item.</span></span> <span data-ttu-id="25bce-123">Локальное хранилище возвращается в состояние таблицы отправить.</span><span class="sxs-lookup"><span data-stu-id="25bce-123">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="25bce-124">См. также</span><span class="sxs-lookup"><span data-stu-id="25bce-124">See also</span></span>



[<span data-ttu-id="25bce-125">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="25bce-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="25bce-126">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="25bce-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="25bce-127">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="25bce-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="25bce-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="25bce-128">SYNCSTATE</span></span>](syncstate.md)

