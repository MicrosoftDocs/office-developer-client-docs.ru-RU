---
title: Состояние простоя
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: dbe81a2a27f302a38eba6f3c5045df905d8db682
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808794"
---
# <a name="idle-state"></a><span data-ttu-id="14b97-103">Состояние простоя</span><span class="sxs-lookup"><span data-stu-id="14b97-103">Idle State</span></span>

  
  
<span data-ttu-id="14b97-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14b97-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="14b97-105">В этом разделе описывается, что происходит во время простоя состояние конечного автомата репликации.</span><span class="sxs-lookup"><span data-stu-id="14b97-105">This topic describes what happens during the idle state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="14b97-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="14b97-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14b97-107">Идентификатор состояний:</span><span class="sxs-lookup"><span data-stu-id="14b97-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="14b97-108">**LR_SYNC_IDLE**</span><span class="sxs-lookup"><span data-stu-id="14b97-108">**LR_SYNC_IDLE**</span></span> <br/> |
|<span data-ttu-id="14b97-109">Структура связанных данных:</span><span class="sxs-lookup"><span data-stu-id="14b97-109">Related Data Structure:</span></span>  <br/> | <span data-ttu-id="14b97-110">*None*</span><span class="sxs-lookup"><span data-stu-id="14b97-110">*None*</span></span>  <br/> |
|<span data-ttu-id="14b97-111">Из этого состояния:</span><span class="sxs-lookup"><span data-stu-id="14b97-111">From this state:</span></span>  <br/> | <span data-ttu-id="14b97-112">*Неприменимо*</span><span class="sxs-lookup"><span data-stu-id="14b97-112">*Not applicable*</span></span>  <br/> |
|<span data-ttu-id="14b97-113">Это состояние:</span><span class="sxs-lookup"><span data-stu-id="14b97-113">To this state:</span></span>  <br/> |[<span data-ttu-id="14b97-114">Синхронизировать состояние</span><span class="sxs-lookup"><span data-stu-id="14b97-114">Synchronize state</span></span>](synchronize-state.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="14b97-115">Конечный автомат репликации является детерминированным конечного автомата.</span><span class="sxs-lookup"><span data-stu-id="14b97-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="14b97-116">Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний.</span><span class="sxs-lookup"><span data-stu-id="14b97-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="14b97-117">Описание</span><span class="sxs-lookup"><span data-stu-id="14b97-117">Description</span></span>

<span data-ttu-id="14b97-118">Ничего не происходит в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="14b97-118">Nothing happens in this state.</span></span> <span data-ttu-id="14b97-119">Локальное хранилище находится в этом состоянии до инициализации репликации и после завершения репликации.</span><span class="sxs-lookup"><span data-stu-id="14b97-119">A local store is in this state before replication is initiated and after replication is complete.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="14b97-120">См. также</span><span class="sxs-lookup"><span data-stu-id="14b97-120">See also</span></span>



[<span data-ttu-id="14b97-121">О репликации API</span><span class="sxs-lookup"><span data-stu-id="14b97-121">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="14b97-122">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="14b97-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="14b97-123">О репликации конечного автомата</span><span class="sxs-lookup"><span data-stu-id="14b97-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="14b97-124">СОСТОЯНИЕ</span><span class="sxs-lookup"><span data-stu-id="14b97-124">SYNCSTATE</span></span>](syncstate.md)

