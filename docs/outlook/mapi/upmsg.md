---
title: UPMSG
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fe3956b-819a-3edf-0e49-7a44bcfbabcd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1e0e2f9b794c4cee25488a754290922e58b7658d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427271"
---
# <a name="upmsg"></a><span data-ttu-id="41caa-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="41caa-103">UPMSG</span></span>

<span data-ttu-id="41caa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41caa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41caa-105">Сведения для отправки элемента Outlook во время [отправки сообщения](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="41caa-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="41caa-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="41caa-106">Quick info</span></span>

```cpp
struct UPMSG 
{ 
    ULONG ulFlags; 
    LPMESSAGE pmsg; 
    MEID meid; 
    SBinary binReserved1; 
    SBinary binReserved2; 
    FEID feid; 
    SBinary binChg; 
    SBinary binPcl; 
    SKEY skeySrc; 
};
```

## <a name="members"></a><span data-ttu-id="41caa-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="41caa-107">Members</span></span>

 <span data-ttu-id="41caa-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="41caa-108">_ulFlags_</span></span>
  
> <span data-ttu-id="41caa-109">[out]/[in] флаги для определения надлежащего поведения при отправке.</span><span class="sxs-lookup"><span data-stu-id="41caa-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="41caa-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="41caa-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="41caa-111">вышли Связан элемент.</span><span class="sxs-lookup"><span data-stu-id="41caa-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="41caa-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="41caa-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="41caa-113">вышли Новый элемент.</span><span class="sxs-lookup"><span data-stu-id="41caa-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="41caa-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="41caa-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="41caa-115">вышли Элемент был перемещен здесь.</span><span class="sxs-lookup"><span data-stu-id="41caa-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="41caa-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="41caa-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="41caa-117">вышли Изменены свойства элемента.</span><span class="sxs-lookup"><span data-stu-id="41caa-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="41caa-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="41caa-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="41caa-119">вышли Item — это заголовок сообщения.</span><span class="sxs-lookup"><span data-stu-id="41caa-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="41caa-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="41caa-120">UPM_OK</span></span>
    
    - <span data-ttu-id="41caa-121">возврата Отправка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="41caa-121">[in] Upload was successful.</span></span> <span data-ttu-id="41caa-122">Клиент устанавливает это после отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="41caa-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="41caa-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="41caa-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="41caa-124">возврата Элемент успешно перемещен.</span><span class="sxs-lookup"><span data-stu-id="41caa-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="41caa-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="41caa-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="41caa-126">возврата Зафиксировать состояние отправки сейчас.</span><span class="sxs-lookup"><span data-stu-id="41caa-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="41caa-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="41caa-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="41caa-128">возврата Удалить элемент.</span><span class="sxs-lookup"><span data-stu-id="41caa-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="41caa-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="41caa-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="41caa-130">возврата Сохраните изменения элемента.</span><span class="sxs-lookup"><span data-stu-id="41caa-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="41caa-131">_пмсг_</span><span class="sxs-lookup"><span data-stu-id="41caa-131">_pmsg_</span></span>
  
> <span data-ttu-id="41caa-132">вышли Открытие объекта Item.</span><span class="sxs-lookup"><span data-stu-id="41caa-132">[out] Open item object.</span></span> <span data-ttu-id="41caa-133">Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="41caa-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="41caa-134">_MEID_</span><span class="sxs-lookup"><span data-stu-id="41caa-134">_meid_</span></span>
  
> <span data-ttu-id="41caa-135">вышли Идентификатор элемента.</span><span class="sxs-lookup"><span data-stu-id="41caa-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="41caa-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="41caa-136">_binReserved1_</span></span>
  
> <span data-ttu-id="41caa-137">возврата Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41caa-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="41caa-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="41caa-138">_binReserved2_</span></span>
  
> <span data-ttu-id="41caa-139">возврата Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41caa-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="41caa-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="41caa-140">_feid_</span></span>
  
> <span data-ttu-id="41caa-141">вышли Идентификатор записи исходной папки, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="41caa-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="41caa-142">_бинчг_</span><span class="sxs-lookup"><span data-stu-id="41caa-142">_binChg_</span></span>
  
> <span data-ttu-id="41caa-143">вышли Изменение ключа целевого элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="41caa-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="41caa-144">Определение типа **сбинари**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="41caa-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="41caa-145">_бинпкл_</span><span class="sxs-lookup"><span data-stu-id="41caa-145">_binPcl_</span></span>
  
> <span data-ttu-id="41caa-146">вышли Изменение списка конечного элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="41caa-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="41caa-147">Определение типа **сбинари**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="41caa-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="41caa-148">_скэйсрк_</span><span class="sxs-lookup"><span data-stu-id="41caa-148">_skeySrc_</span></span>
  
> <span data-ttu-id="41caa-149">вышли Исходный ключ исходного элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="41caa-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41caa-150">См. также</span><span class="sxs-lookup"><span data-stu-id="41caa-150">See also</span></span>

- [<span data-ttu-id="41caa-151">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="41caa-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="41caa-152">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="41caa-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="41caa-153">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="41caa-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="41caa-154">FEID</span><span class="sxs-lookup"><span data-stu-id="41caa-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="41caa-155">MEID</span><span class="sxs-lookup"><span data-stu-id="41caa-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="41caa-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="41caa-156">SKEY</span></span>](skey.md)

