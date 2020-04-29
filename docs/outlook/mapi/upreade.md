---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434146"
---
# <a name="upreade"></a><span data-ttu-id="9cf61-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="9cf61-103">UPREADE</span></span>

<span data-ttu-id="9cf61-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cf61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cf61-105">Расширенные сведения для отправки состояния чтения элемента во время [отправки состояния прочтения](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="9cf61-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9cf61-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9cf61-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="9cf61-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="9cf61-107">Members</span></span>

<span data-ttu-id="9cf61-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9cf61-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="9cf61-109">[out]/[in] флаги для определения надлежащего поведения при отправке.</span><span class="sxs-lookup"><span data-stu-id="9cf61-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="9cf61-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="9cf61-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="9cf61-111">вышли Элемент скрыт.</span><span class="sxs-lookup"><span data-stu-id="9cf61-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="9cf61-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="9cf61-112">UPR_READ</span></span>
    
    - <span data-ttu-id="9cf61-113">вышли Состояние чтения элемента изменилось.</span><span class="sxs-lookup"><span data-stu-id="9cf61-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="9cf61-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="9cf61-114">UPR_OK</span></span>
    
    - <span data-ttu-id="9cf61-115">возврата Отправка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9cf61-115">[in] Upload was successful.</span></span> <span data-ttu-id="9cf61-116">Клиент устанавливает это после отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="9cf61-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="9cf61-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="9cf61-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="9cf61-118">возврата Отправить состояние чтения элемента теперь, не дожидаясь окончания [состояния таблицы отправки](upload-table-state.md) , в пакетную обработку нескольких элементов.</span><span class="sxs-lookup"><span data-stu-id="9cf61-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="9cf61-119">_скэй_</span><span class="sxs-lookup"><span data-stu-id="9cf61-119">_skey_</span></span>
  
> <span data-ttu-id="9cf61-120">вышли Ключ источника элемента.</span><span class="sxs-lookup"><span data-stu-id="9cf61-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cf61-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9cf61-121">See also</span></span>

- [<span data-ttu-id="9cf61-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="9cf61-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="9cf61-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="9cf61-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="9cf61-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="9cf61-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="9cf61-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="9cf61-125">UPREAD</span></span>](upread.md)

