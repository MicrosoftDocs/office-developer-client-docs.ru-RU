---
title: Состояние простоя
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419480"
---
# <a name="idle-state"></a><span data-ttu-id="5a908-103">Состояние простоя</span><span class="sxs-lookup"><span data-stu-id="5a908-103">Idle State</span></span>

  
  
<span data-ttu-id="5a908-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a908-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5a908-105">В этом разделе описывается, что происходит во время простоя конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="5a908-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5a908-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="5a908-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a908-107">Идентификатор состояния:</span><span class="sxs-lookup"><span data-stu-id="5a908-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="5a908-108">**ЛР_СИНК_ИДЛЕ**</span><span class="sxs-lookup"><span data-stu-id="5a908-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="5a908-109">Связанная структура данных:</span><span class="sxs-lookup"><span data-stu-id="5a908-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="5a908-110">*Нет*</span><span class="sxs-lookup"><span data-stu-id="5a908-110">*None*</span></span>  <br/> |
|<span data-ttu-id="5a908-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="5a908-111">From this state:</span></span>  <br/> | <span data-ttu-id="5a908-112">*Неприменимо*</span><span class="sxs-lookup"><span data-stu-id="5a908-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="5a908-113">В это состояние:</span><span class="sxs-lookup"><span data-stu-id="5a908-113">To this state:</span></span>  <br/> |[<span data-ttu-id="5a908-114">Состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="5a908-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="5a908-115">Конечный автомат репликации — это детерминированный конечный автомат.</span><span class="sxs-lookup"><span data-stu-id="5a908-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="5a908-116">Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего.</span><span class="sxs-lookup"><span data-stu-id="5a908-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="5a908-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5a908-117">Description</span></span>

<span data-ttu-id="5a908-118">В этом состоянии ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="5a908-118">Nothing happens in this state.</span></span> <span data-ttu-id="5a908-119">Локальное хранилище находится в этом состоянии до начала репликации и после завершения репликации.</span><span class="sxs-lookup"><span data-stu-id="5a908-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5a908-120">См. также</span><span class="sxs-lookup"><span data-stu-id="5a908-120">See also</span></span>



[<span data-ttu-id="5a908-121">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="5a908-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="5a908-122">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="5a908-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5a908-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="5a908-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5a908-124">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="5a908-124">SYNCSTATE</span></span>](syncstate.md)

