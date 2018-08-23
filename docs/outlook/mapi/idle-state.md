---
title: Состояние бездействия
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591802"
---
# <a name="idle-state"></a><span data-ttu-id="310ee-103">Состояние бездействия</span><span class="sxs-lookup"><span data-stu-id="310ee-103">Idle State</span></span>

  
  
<span data-ttu-id="310ee-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="310ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="310ee-105">В этом разделе описывается, что происходит во время простоя состояние конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="310ee-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="310ee-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="310ee-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="310ee-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="310ee-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="310ee-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="310ee-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="310ee-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="310ee-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="310ee-110">*None*</span><span class="sxs-lookup"><span data-stu-id="310ee-110">*None*</span></span>  <br/> |
|<span data-ttu-id="310ee-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="310ee-111">From this state:</span></span>  <br/> | <span data-ttu-id="310ee-112">*Неприменимо*</span><span class="sxs-lookup"><span data-stu-id="310ee-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="310ee-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="310ee-113">To this state:</span></span>  <br/> |[<span data-ttu-id="310ee-114">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="310ee-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="310ee-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="310ee-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="310ee-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="310ee-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="310ee-117">Описание</span><span class="sxs-lookup"><span data-stu-id="310ee-117">Description</span></span>

<span data-ttu-id="310ee-118">Ничего не происходит в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="310ee-118">Nothing happens in this state.</span></span> <span data-ttu-id="310ee-119">Локальное хранилище находится в этом состоянии до инициализации репликации и после завершения репликации.</span><span class="sxs-lookup"><span data-stu-id="310ee-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="310ee-120">См. также</span><span class="sxs-lookup"><span data-stu-id="310ee-120">See also</span></span>



[<span data-ttu-id="310ee-121">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="310ee-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="310ee-122">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="310ee-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="310ee-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="310ee-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="310ee-124">СОСТОЯНИЕ</span><span class="sxs-lookup"><span data-stu-id="310ee-124">SYNCSTATE</span></span>](syncstate.md)

