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
# <a name="upreade"></a><span data-ttu-id="79931-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="79931-103">UPREADE</span></span>

<span data-ttu-id="79931-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79931-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79931-105">Расширенные сведения для загрузки состояния чтения элемента во время [состояния состояния чтения.](upload-read-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="79931-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79931-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="79931-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="79931-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="79931-107">Members</span></span>

<span data-ttu-id="79931-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79931-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="79931-109">[out]/[in] Флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="79931-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="79931-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="79931-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="79931-111">[вышел] Элемент скрыт.</span><span class="sxs-lookup"><span data-stu-id="79931-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="79931-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="79931-112">UPR_READ</span></span>
    
    - <span data-ttu-id="79931-113">[вышел] Изменено состояние чтения элемента.</span><span class="sxs-lookup"><span data-stu-id="79931-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="79931-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="79931-114">UPR_OK</span></span>
    
    - <span data-ttu-id="79931-115">[in] Upload успешно.</span><span class="sxs-lookup"><span data-stu-id="79931-115">[in] Upload was successful.</span></span> <span data-ttu-id="79931-116">Клиент задает это после отправки сведений на сервер.</span><span class="sxs-lookup"><span data-stu-id="79931-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="79931-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="79931-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="79931-118">[in] Upload состояние чтения элемента, а не ожидание окончания состояния [](upload-table-state.md) таблицы отправки для пакетной обработки более одного элемента.</span><span class="sxs-lookup"><span data-stu-id="79931-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="79931-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="79931-119">_skey_</span></span>
  
> <span data-ttu-id="79931-120">[вышел] Исходный ключ элемента.</span><span class="sxs-lookup"><span data-stu-id="79931-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79931-121">См. также</span><span class="sxs-lookup"><span data-stu-id="79931-121">See also</span></span>

- [<span data-ttu-id="79931-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="79931-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="79931-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="79931-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="79931-124">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="79931-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="79931-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="79931-125">UPREAD</span></span>](upread.md)

