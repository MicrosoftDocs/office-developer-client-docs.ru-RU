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
# <a name="upmsg"></a><span data-ttu-id="d7ed2-103">UPMSG</span><span class="sxs-lookup"><span data-stu-id="d7ed2-103">UPMSG</span></span>

<span data-ttu-id="d7ed2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7ed2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7ed2-105">Сведения для отправки элемента Outlook во время [отправки сообщения](upload-message-state.md).</span><span class="sxs-lookup"><span data-stu-id="d7ed2-105">Information for uploading an Outlook item during the [upload message state](upload-message-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d7ed2-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d7ed2-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="d7ed2-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d7ed2-107">Members</span></span>

 <span data-ttu-id="d7ed2-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-108">_ulFlags_</span></span>
  
> <span data-ttu-id="d7ed2-109">[out]/[in] флаги для определения надлежащего поведения при отправке.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-109">[out]/[in] Flags to determine appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="d7ed2-110">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="d7ed2-110">UPM_ASSOC</span></span>
    
    - <span data-ttu-id="d7ed2-111">вышли Связан элемент.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-111">[out] Item is associated.</span></span>
    
  - <span data-ttu-id="d7ed2-112">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="d7ed2-112">UPM_NEW</span></span>
    
    - <span data-ttu-id="d7ed2-113">вышли Новый элемент.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-113">[out] New item.</span></span> 
    
  - <span data-ttu-id="d7ed2-114">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="d7ed2-114">UPM_MOV</span></span>
    
    - <span data-ttu-id="d7ed2-115">вышли Элемент был перемещен здесь.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-115">[out] Item was moved here.</span></span>
    
  - <span data-ttu-id="d7ed2-116">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="d7ed2-116">UPM_MOD_PROPS</span></span>
    
    - <span data-ttu-id="d7ed2-117">вышли Изменены свойства элемента.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-117">[out] Item properties were modified.</span></span>
    
  - <span data-ttu-id="d7ed2-118">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="d7ed2-118">UPM_HEADER</span></span>
    
    - <span data-ttu-id="d7ed2-119">вышли Item — это заголовок сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-119">[out] Item is a message header.</span></span>
    
  - <span data-ttu-id="d7ed2-120">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="d7ed2-120">UPM_OK</span></span>
    
    - <span data-ttu-id="d7ed2-121">возврата Отправка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-121">[in] Upload was successful.</span></span> <span data-ttu-id="d7ed2-122">Клиент устанавливает это после отправки информации на сервер.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-122">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="d7ed2-123">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="d7ed2-123">UPM_MOVED</span></span>
    
    - <span data-ttu-id="d7ed2-124">возврата Элемент успешно перемещен.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-124">[in] Item was moved successfully.</span></span>
    
  - <span data-ttu-id="d7ed2-125">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d7ed2-125">UPM_COMMIT</span></span>
    
    - <span data-ttu-id="d7ed2-126">возврата ЗаФиксировать состояние отправки сейчас.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-126">[in] Commit upload state now.</span></span>
    
  - <span data-ttu-id="d7ed2-127">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="d7ed2-127">UPM_DELETE</span></span>
    
    - <span data-ttu-id="d7ed2-128">возврата Удалить элемент.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-128">[in] Delete item now.</span></span>
    
  - <span data-ttu-id="d7ed2-129">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="d7ed2-129">UPM_SAVE</span></span>
    
    - <span data-ttu-id="d7ed2-130">возврата Сохраните изменения элемента.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-130">[in] Save changes to the item.</span></span>
    
<span data-ttu-id="d7ed2-131">_ПМСГ_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-131">_pmsg_</span></span>
  
> <span data-ttu-id="d7ed2-132">вышли Открытие объекта Item.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-132">[out] Open item object.</span></span> <span data-ttu-id="d7ed2-133">Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-133">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
<span data-ttu-id="d7ed2-134">_MEID_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-134">_meid_</span></span>
  
> <span data-ttu-id="d7ed2-135">вышли Идентификатор элемента.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-135">[out] Entry ID of item.</span></span>
    
<span data-ttu-id="d7ed2-136">_binReserved1_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-136">_binReserved1_</span></span>
  
> <span data-ttu-id="d7ed2-137">возврата Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-137">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d7ed2-138">_binReserved2_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-138">_binReserved2_</span></span>
  
> <span data-ttu-id="d7ed2-139">возврата Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-139">[in] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d7ed2-140">_feid_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-140">_feid_</span></span>
  
> <span data-ttu-id="d7ed2-141">вышли Идентификатор записи исходной папки, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-141">[out] Entry ID of the source folder, if item was moved.</span></span>
    
<span data-ttu-id="d7ed2-142">_Бинчг_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-142">_binChg_</span></span>
  
> <span data-ttu-id="d7ed2-143">вышли Изменение ключа целевого элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-143">[out] Change key of the destination item, if item was moved.</span></span> <span data-ttu-id="d7ed2-144">Определение типа **сбинари**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-144">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="d7ed2-145">_Бинпкл_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-145">_binPcl_</span></span>
  
> <span data-ttu-id="d7ed2-146">вышли Изменение списка конечного элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-146">[out] Change list of the destination item, if item was moved.</span></span> <span data-ttu-id="d7ed2-147">Определение типа **сбинари**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-147">See mapidefs.h for the type definition of **SBinary**.</span></span> 
    
<span data-ttu-id="d7ed2-148">_Скэйсрк_</span><span class="sxs-lookup"><span data-stu-id="d7ed2-148">_skeySrc_</span></span>
  
> <span data-ttu-id="d7ed2-149">вышли Исходный ключ исходного элемента, если элемент был перемещен.</span><span class="sxs-lookup"><span data-stu-id="d7ed2-149">[out] Source key of the source item, if item was moved.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7ed2-150">См. также</span><span class="sxs-lookup"><span data-stu-id="d7ed2-150">See also</span></span>

- [<span data-ttu-id="d7ed2-151">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="d7ed2-151">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="d7ed2-152">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="d7ed2-152">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d7ed2-153">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="d7ed2-153">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="d7ed2-154">FEID</span><span class="sxs-lookup"><span data-stu-id="d7ed2-154">FEID</span></span>](feid.md)
- [<span data-ttu-id="d7ed2-155">MEID</span><span class="sxs-lookup"><span data-stu-id="d7ed2-155">MEID</span></span>](meid.md)
- [<span data-ttu-id="d7ed2-156">SKEY</span><span class="sxs-lookup"><span data-stu-id="d7ed2-156">SKEY</span></span>](skey.md)

