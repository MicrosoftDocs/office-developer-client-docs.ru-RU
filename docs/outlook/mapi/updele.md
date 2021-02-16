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
ms.openlocfilehash: 9bd61739b14d0ec382a9d582689c1049fe89429b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424884"
---
# <a name="updele"></a><span data-ttu-id="31698-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="31698-103">UPDELE</span></span>

<span data-ttu-id="31698-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31698-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31698-105">Расширенная информация для элементов, удаленных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="31698-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="31698-106">Эти сведения используются во время состояния [отправки удаления.](upload-delete-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="31698-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="31698-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="31698-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="31698-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="31698-108">Members</span></span>

<span data-ttu-id="31698-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31698-109">_ulFlags_</span></span>
  
> <span data-ttu-id="31698-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span><span class="sxs-lookup"><span data-stu-id="31698-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="31698-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="31698-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="31698-112">[out] Элемент связан.</span><span class="sxs-lookup"><span data-stu-id="31698-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="31698-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="31698-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="31698-114">[out] Элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="31698-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="31698-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="31698-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="31698-116">[in] Отправка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="31698-116">[in] Upload was successful.</span></span> <span data-ttu-id="31698-117">Клиент устанавливает это после отправки сведений на сервер.</span><span class="sxs-lookup"><span data-stu-id="31698-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="31698-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="31698-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="31698-119">[in] Элемент успешно перемещен.</span><span class="sxs-lookup"><span data-stu-id="31698-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="31698-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="31698-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="31698-121">[in] Пометить исходный элемент как измененный.</span><span class="sxs-lookup"><span data-stu-id="31698-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="31698-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="31698-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="31698-123">[in] Зафиксировать состояние отправки сейчас (запись 0).</span><span class="sxs-lookup"><span data-stu-id="31698-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="31698-124">_skey_</span><span class="sxs-lookup"><span data-stu-id="31698-124">_skey_</span></span>
  
> <span data-ttu-id="31698-125">[out] Исходный ключ элемента.</span><span class="sxs-lookup"><span data-stu-id="31698-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="31698-126">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="31698-126">_dwReserved_</span></span>
  
> <span data-ttu-id="31698-127">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="31698-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="31698-128">_binChg_</span><span class="sxs-lookup"><span data-stu-id="31698-128">_binChg_</span></span>
  
> <span data-ttu-id="31698-129">[out] Измените ключ конечного элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="31698-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="31698-130">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="31698-130">_binPcl_</span></span>
  
> <span data-ttu-id="31698-131">[out] Изменение списка конечного элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="31698-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="31698-132">_skeyDst_</span><span class="sxs-lookup"><span data-stu-id="31698-132">_skeyDst_</span></span>
  
> <span data-ttu-id="31698-133">[out] Исходный ключ конечного элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="31698-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="31698-134">_pupmov_</span><span class="sxs-lookup"><span data-stu-id="31698-134">_pupmov_</span></span>
  
> <span data-ttu-id="31698-135">[out] Сведения о папке назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="31698-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31698-136">См. также</span><span class="sxs-lookup"><span data-stu-id="31698-136">See also</span></span>

- [<span data-ttu-id="31698-137">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="31698-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="31698-138">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="31698-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="31698-139">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="31698-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="31698-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="31698-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="31698-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="31698-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="31698-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="31698-142">UPMOV</span></span>](upmov.md)

