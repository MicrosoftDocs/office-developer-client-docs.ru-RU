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
# <a name="upmsg"></a><span data-ttu-id="bb287-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="bb287-103">UPMSG</span></span>

<span data-ttu-id="bb287-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb287-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb287-105">Сведения о загрузке элемента Outlook во время [состояния отправки сообщения.](upload-message-state.md)</span><span class="sxs-lookup"><span data-stu-id="bb287-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bb287-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bb287-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="bb287-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="bb287-107">Members</span></span>

 <span data-ttu-id="bb287-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb287-108">_ulFlags_</span></span>
  
> <span data-ttu-id="bb287-109">[out]/[in] Флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="bb287-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="bb287-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="bb287-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="bb287-111">[вышел] Элемент связан.</span><span class="sxs-lookup"><span data-stu-id="bb287-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="bb287-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="bb287-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="bb287-113">[вышел] Новый элемент.</span><span class="sxs-lookup"><span data-stu-id="bb287-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="bb287-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="bb287-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="bb287-115">[вышел] Элемент был перемещен сюда.</span><span class="sxs-lookup"><span data-stu-id="bb287-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="bb287-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="bb287-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="bb287-117">[вышел] Изменены свойства элемента.</span><span class="sxs-lookup"><span data-stu-id="bb287-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="bb287-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="bb287-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="bb287-119">[вышел] Элемент — это заглавный элемент сообщения.</span><span class="sxs-lookup"><span data-stu-id="bb287-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="bb287-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="bb287-120">UPM_OK</span></span>
    
    - <span data-ttu-id="bb287-121">[in] Upload успешно.</span><span class="sxs-lookup"><span data-stu-id="bb287-121">[in] Upload was successful.</span></span> <span data-ttu-id="bb287-122">Клиент задает это после отправки сведений на сервер.</span><span class="sxs-lookup"><span data-stu-id="bb287-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="bb287-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="bb287-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="bb287-124">[in] Элемент был успешно перемещен.</span><span class="sxs-lookup"><span data-stu-id="bb287-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="bb287-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="bb287-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="bb287-126">[in] Зафиксировать состояние отправки.</span><span class="sxs-lookup"><span data-stu-id="bb287-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="bb287-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="bb287-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="bb287-128">[in] Удалите элемент сейчас.</span><span class="sxs-lookup"><span data-stu-id="bb287-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="bb287-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="bb287-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="bb287-130">[in] Сохранение изменений в элементе.</span><span class="sxs-lookup"><span data-stu-id="bb287-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="bb287-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="bb287-131">_pmsg_</span></span>
  
> <span data-ttu-id="bb287-132">[вышел] Откройте объект элемента.</span><span class="sxs-lookup"><span data-stu-id="bb287-132">[out] Open item object.</span></span> <span data-ttu-id="bb287-133">См. mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="bb287-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="bb287-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="bb287-134">_meid_</span></span>
  
> <span data-ttu-id="bb287-135">[вышел] ID входа элемента.</span><span class="sxs-lookup"><span data-stu-id="bb287-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="bb287-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="bb287-136">_binReserved1_</span></span>
  
> <span data-ttu-id="bb287-137">[in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bb287-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="bb287-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="bb287-138">_binReserved2_</span></span>
  
> <span data-ttu-id="bb287-139">[in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bb287-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="bb287-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="bb287-140">_feid_</span></span>
  
> <span data-ttu-id="bb287-141">[вышел] Код входа в папку источника, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="bb287-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="bb287-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="bb287-142">_binChg_</span></span>
  
> <span data-ttu-id="bb287-143">[вышел] Измените ключ элемента назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="bb287-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="bb287-144">См. mapidefs.h для определения **типа SBinary**.</span><span class="sxs-lookup"><span data-stu-id="bb287-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="bb287-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="bb287-145">_binPcl_</span></span>
  
> <span data-ttu-id="bb287-146">[вышел] Измените список элемента назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="bb287-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="bb287-147">См. mapidefs.h для определения **типа SBinary**.</span><span class="sxs-lookup"><span data-stu-id="bb287-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="bb287-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="bb287-148">_skeySrc_</span></span>
  
> <span data-ttu-id="bb287-149">[вышел] Исходный ключ элемента источника, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="bb287-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb287-150">См. также</span><span class="sxs-lookup"><span data-stu-id="bb287-150">See also</span></span>

- [<span data-ttu-id="bb287-151">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="bb287-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="bb287-152">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="bb287-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="bb287-153">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="bb287-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="bb287-154">FEID</span><span class="sxs-lookup"><span data-stu-id="bb287-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="bb287-155">MEID</span><span class="sxs-lookup"><span data-stu-id="bb287-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="bb287-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="bb287-156">SKEY</span></span>](skey.md)

