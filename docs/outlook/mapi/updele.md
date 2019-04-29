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
# <a name="updele"></a><span data-ttu-id="8b3e4-103">UPDELE</span><span class="sxs-lookup"><span data-stu-id="8b3e4-103">UPDELE</span></span>

<span data-ttu-id="8b3e4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b3e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b3e4-105">Расширенные сведения об элементах, удаленных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-105">Extended information for items that have been deleted in a local store.</span></span> <span data-ttu-id="8b3e4-106">Эти сведения используются в состоянии состояния [отправки для удаления](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="8b3e4-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8b3e4-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8b3e4-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8b3e4-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="8b3e4-108">Members</span></span>

<span data-ttu-id="8b3e4-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b3e4-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8b3e4-110">[out]/[in] флаги для определения надлежащего поведения при отправке.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-110">[out]/[in] Flags to determine appropriate behavior during uploading.</span></span>
    
  - <span data-ttu-id="8b3e4-111">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="8b3e4-111">UPD_ASSOC</span></span>
    
    - <span data-ttu-id="8b3e4-112">вышли Связан элемент.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-112">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="8b3e4-113">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="8b3e4-113">UPD_MOV</span></span>
    
    - <span data-ttu-id="8b3e4-114">вышли Элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-114">[out] Item was moved out.</span></span>
    
  - <span data-ttu-id="8b3e4-115">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="8b3e4-115">UPD_OK</span></span> 
    
    - <span data-ttu-id="8b3e4-116">возврата Отправка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-116">[in] Upload was successful.</span></span> <span data-ttu-id="8b3e4-117">Клиент устанавливает это после отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-117">The client sets this after uploading information to server.</span></span>
    
  - <span data-ttu-id="8b3e4-118">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="8b3e4-118">UPD_MOVED</span></span>
    
    - <span data-ttu-id="8b3e4-119">возврата Элемент успешно перемещен.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-119">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="8b3e4-120">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="8b3e4-120">UPD_UPDATE</span></span>
    
    - <span data-ttu-id="8b3e4-121">возврата ПоМетить исходный элемент как измененный.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-121">[in] Mark source item as modified.</span></span>
    
  - <span data-ttu-id="8b3e4-122">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="8b3e4-122">UPD_COMMIT</span></span>
    
    - <span data-ttu-id="8b3e4-123">возврата ЗаФиксировать состояние отправки сейчас (запись 0).</span><span class="sxs-lookup"><span data-stu-id="8b3e4-123">[in] Commit upload state now (entry 0).</span></span>
    
<span data-ttu-id="8b3e4-124">_скэй_</span><span class="sxs-lookup"><span data-stu-id="8b3e4-124">_skey_</span></span>
  
> <span data-ttu-id="8b3e4-125">вышли Ключ источника элемента.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-125">[out] Source key of item.</span></span>
    
<span data-ttu-id="8b3e4-126">_Двресервед_</span><span class="sxs-lookup"><span data-stu-id="8b3e4-126">_dwReserved_</span></span>
  
> <span data-ttu-id="8b3e4-127">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-127">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
<span data-ttu-id="8b3e4-128">_Бинчг_</span><span class="sxs-lookup"><span data-stu-id="8b3e4-128">_binChg_</span></span>
  
> <span data-ttu-id="8b3e4-129">вышли Изменение ключа целевого элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-129">[out] Change key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="8b3e4-130">_Бинпкл_</span><span class="sxs-lookup"><span data-stu-id="8b3e4-130">_binPcl_</span></span>
  
> <span data-ttu-id="8b3e4-131">вышли Изменение списка элементов назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-131">[out] Change list of destination item if item has been moved.</span></span>
    
<span data-ttu-id="8b3e4-132">_Скэйдст_</span><span class="sxs-lookup"><span data-stu-id="8b3e4-132">_skeyDst_</span></span>
  
> <span data-ttu-id="8b3e4-133">вышли Исходный ключ целевого элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-133">[out] Source key of destination item if item has been moved.</span></span>
    
<span data-ttu-id="8b3e4-134">_пупмов_</span><span class="sxs-lookup"><span data-stu-id="8b3e4-134">_pupmov_</span></span>
  
> <span data-ttu-id="8b3e4-135">вышли Сведения о папке назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="8b3e4-135">[out] Destination folder information if item has been moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b3e4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="8b3e4-136">See also</span></span>

- [<span data-ttu-id="8b3e4-137">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="8b3e4-137">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="8b3e4-138">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="8b3e4-138">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="8b3e4-139">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="8b3e4-139">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="8b3e4-140">SKEY</span><span class="sxs-lookup"><span data-stu-id="8b3e4-140">SKEY</span></span>](skey.md)
- [<span data-ttu-id="8b3e4-141">UPDEL</span><span class="sxs-lookup"><span data-stu-id="8b3e4-141">UPDEL</span></span>](updel.md)
- [<span data-ttu-id="8b3e4-142">UPMOV</span><span class="sxs-lookup"><span data-stu-id="8b3e4-142">UPMOV</span></span>](upmov.md)

