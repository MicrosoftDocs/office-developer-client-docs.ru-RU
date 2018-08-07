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
ms.openlocfilehash: e281907931a493e82c44913a7c26f6df55876e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812570"
---
# <a name="upmsg"></a><span data-ttu-id="3ff47-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="3ff47-103">UPMSG</span></span>

<span data-ttu-id="3ff47-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ff47-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ff47-105">Сведения для отправки элемента Outlook во время [отправки сообщения состояния](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="3ff47-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3ff47-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3ff47-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="3ff47-107">Members</span><span class="sxs-lookup"><span data-stu-id="3ff47-107">Members</span></span>

 <span data-ttu-id="3ff47-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ff47-108">_ulFlags_</span></span>
  
> <span data-ttu-id="3ff47-109">[out] и [in] флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="3ff47-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="3ff47-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="3ff47-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="3ff47-111">[out] Элемент связан.</span><span class="sxs-lookup"><span data-stu-id="3ff47-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="3ff47-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="3ff47-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="3ff47-113">[out] Новый элемент.</span><span class="sxs-lookup"><span data-stu-id="3ff47-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="3ff47-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="3ff47-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="3ff47-115">[out] Переместить элемент здесь.</span><span class="sxs-lookup"><span data-stu-id="3ff47-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="3ff47-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="3ff47-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="3ff47-117">[out] Изменения свойств элемента.</span><span class="sxs-lookup"><span data-stu-id="3ff47-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="3ff47-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="3ff47-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="3ff47-119">[out] Элемент — это заголовок сообщения.</span><span class="sxs-lookup"><span data-stu-id="3ff47-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="3ff47-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="3ff47-120">UPM_OK</span></span>
    
    - <span data-ttu-id="3ff47-121">[in] Отправка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="3ff47-121">[in] Upload was successful.</span></span> <span data-ttu-id="3ff47-122">Клиент устанавливает это после отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="3ff47-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="3ff47-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="3ff47-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="3ff47-124">[in] Элемент успешно перемещен.</span><span class="sxs-lookup"><span data-stu-id="3ff47-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="3ff47-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="3ff47-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="3ff47-126">[in] Теперь сохранить отправка состояний.</span><span class="sxs-lookup"><span data-stu-id="3ff47-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="3ff47-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="3ff47-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="3ff47-128">[in] Теперь удалите элемент.</span><span class="sxs-lookup"><span data-stu-id="3ff47-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="3ff47-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="3ff47-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="3ff47-130">[in] Сохраните изменения в элемент.</span><span class="sxs-lookup"><span data-stu-id="3ff47-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="3ff47-131">_pmsg_</span><span class="sxs-lookup"><span data-stu-id="3ff47-131">_pmsg_</span></span>
  
> <span data-ttu-id="3ff47-132">[out] Открытие элементов объекта.</span><span class="sxs-lookup"><span data-stu-id="3ff47-132">[out] Open item object.</span></span> <span data-ttu-id="3ff47-133">В разделе mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="3ff47-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="3ff47-134">_meid_</span><span class="sxs-lookup"><span data-stu-id="3ff47-134">_meid_</span></span>
  
> <span data-ttu-id="3ff47-135">[out] Идентификатор элемента записи.</span><span class="sxs-lookup"><span data-stu-id="3ff47-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="3ff47-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="3ff47-136">_binReserved1_</span></span>
  
> <span data-ttu-id="3ff47-137">[in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3ff47-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3ff47-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="3ff47-138">_binReserved2_</span></span>
  
> <span data-ttu-id="3ff47-139">[in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3ff47-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3ff47-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="3ff47-140">_feid_</span></span>
  
> <span data-ttu-id="3ff47-141">[out] Идентификатор записи исходной папки, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="3ff47-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="3ff47-142">_binChg_</span><span class="sxs-lookup"><span data-stu-id="3ff47-142">_binChg_</span></span>
  
> <span data-ttu-id="3ff47-143">[out] Изменение ключа элемента назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="3ff47-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="3ff47-144">В разделе mapidefs.h для определения типа **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="3ff47-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="3ff47-145">_binPcl_</span><span class="sxs-lookup"><span data-stu-id="3ff47-145">_binPcl_</span></span>
  
> <span data-ttu-id="3ff47-146">[out] Изменить список элемент назначения, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="3ff47-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="3ff47-147">В разделе mapidefs.h для определения типа **SBinary**.</span><span class="sxs-lookup"><span data-stu-id="3ff47-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="3ff47-148">_skeySrc_</span><span class="sxs-lookup"><span data-stu-id="3ff47-148">_skeySrc_</span></span>
  
> <span data-ttu-id="3ff47-149">[out] Ключ исходного элемента источника, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="3ff47-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ff47-150">См. также</span><span class="sxs-lookup"><span data-stu-id="3ff47-150">See also</span></span>

- [<span data-ttu-id="3ff47-151">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="3ff47-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="3ff47-152">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="3ff47-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="3ff47-153">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="3ff47-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="3ff47-154">FEID</span><span class="sxs-lookup"><span data-stu-id="3ff47-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="3ff47-155">MEID</span><span class="sxs-lookup"><span data-stu-id="3ff47-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="3ff47-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="3ff47-156">SKEY</span></span>](skey.md)

