---
title: UPDELE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c38aa8be-ae77-0c40-9843-42e07b80db6b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2361d225c07d60fab40465b27ad393ca10f6d8eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566588"
---
# <a name="updele"></a><span data-ttu-id="2484a-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="2484a-103">UPDELE</span></span>

<span data-ttu-id="2484a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2484a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2484a-105">Подробные данные для элементов, которые были удалены в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="2484a-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="2484a-106">Эти сведения используются во время [загрузки удалить состояние состояние](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="2484a-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2484a-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="2484a-107">Quick info</span></span>

```cpp
struct UPDELE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
    DWORD   dwReserved; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeyDst; 
    PUPMOV pupmov; 
};
```

## <a name="members"></a><span data-ttu-id="2484a-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="2484a-108">Members</span></span>

<span data-ttu-id="2484a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2484a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2484a-110">[out] и [in] флаги для определения соответствующего поведения во время передачи данных.</span><span class="sxs-lookup"><span data-stu-id="2484a-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="2484a-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="2484a-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="2484a-112">[out] Элемент связан.</span><span class="sxs-lookup"><span data-stu-id="2484a-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="2484a-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="2484a-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="2484a-114">[out] Элемент был перемещен в работе.</span><span class="sxs-lookup"><span data-stu-id="2484a-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="2484a-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="2484a-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="2484a-116">[in] Отправка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="2484a-116">[in] Upload was successful.</span></span> <span data-ttu-id="2484a-117">Клиент устанавливает это после отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="2484a-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="2484a-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="2484a-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="2484a-119">[in] Элемент успешно перемещен.</span><span class="sxs-lookup"><span data-stu-id="2484a-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="2484a-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="2484a-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="2484a-121">[in] Пометить исходного элемента, как изменения.</span><span class="sxs-lookup"><span data-stu-id="2484a-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="2484a-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="2484a-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="2484a-123">[in] Сохранить теперь состояние передачи (запись в 0).</span><span class="sxs-lookup"><span data-stu-id="2484a-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="2484a-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="2484a-124">_skey_</span></span>
  
> <span data-ttu-id="2484a-125">[out] Ключ исходного элемента.</span><span class="sxs-lookup"><span data-stu-id="2484a-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="2484a-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="2484a-126">_dwReserved_</span></span>
  
> <span data-ttu-id="2484a-127">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2484a-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="2484a-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="2484a-128">_binChg_</span></span>
  
> <span data-ttu-id="2484a-129">[out] Изменение ключа назначения элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="2484a-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="2484a-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="2484a-130">_binPcl_</span></span>
  
> <span data-ttu-id="2484a-131">[out] Изменение списка элемент назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="2484a-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="2484a-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="2484a-132">_skeyDst_</span></span>
  
> <span data-ttu-id="2484a-133">[out] Ключ исходного элемента назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="2484a-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="2484a-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="2484a-134">_pupmov_</span></span>
  
> <span data-ttu-id="2484a-135">[out] Сведения о папке назначения Если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="2484a-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2484a-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2484a-136">See also</span></span>

- [<span data-ttu-id="2484a-137">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="2484a-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="2484a-138">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="2484a-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="2484a-139">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="2484a-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="2484a-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="2484a-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="2484a-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="2484a-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="2484a-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="2484a-142">UPMOV</span></span>](upmov.md)

