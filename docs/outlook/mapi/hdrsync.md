---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 261a59e628320f384deeb760ba71c9c0386cfde6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576045"
---
# <a name="hdrsync"></a><span data-ttu-id="296ed-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="296ed-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="296ed-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="296ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="296ed-105">Сведения о синхронизации заголовок сообщения во время [загрузки состояния заголовок сообщения](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="296ed-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="296ed-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="296ed-106">Quick info</span></span>

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a><span data-ttu-id="296ed-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="296ed-107">Members</span></span>

 <span data-ttu-id="296ed-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="296ed-108">_pupmsg_</span></span>
  
- <span data-ttu-id="296ed-109">[out] Сведения о текущем заголовок сообщения в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="296ed-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="296ed-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="296ed-110">_feidPar_</span></span>
  
- <span data-ttu-id="296ed-111">[out] Идентификатор записи для родительской папки сообщения элемента.</span><span class="sxs-lookup"><span data-stu-id="296ed-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="296ed-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="296ed-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="296ed-113">[] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="296ed-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="296ed-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="296ed-114">_ulFlags_</span></span>
  
- <span data-ttu-id="296ed-115">[in] Флаги для изменения поведения:</span><span class="sxs-lookup"><span data-stu-id="296ed-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="296ed-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="296ed-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="296ed-117">[in] Все элементы находится в том же локальном хранилище, как заголовок элемента.</span><span class="sxs-lookup"><span data-stu-id="296ed-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="296ed-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="296ed-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="296ed-119">[in] Оптимизация операций внутренней копии.</span><span class="sxs-lookup"><span data-stu-id="296ed-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="296ed-120">Это может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="296ed-120">This might cause data loss.</span></span> <span data-ttu-id="296ed-121">Должно иметь значение **HSF_LOCAL** .</span><span class="sxs-lookup"><span data-stu-id="296ed-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="296ed-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="296ed-122">HSF_OK</span></span>
    
  - <span data-ttu-id="296ed-123">[in] Заголовок синхронизация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="296ed-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="296ed-124">Устанавливается клиентом после скачивания информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="296ed-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="296ed-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="296ed-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="296ed-126">[in] Полное сообщение элемента, включая заголовок сообщения загружаются с сервера.</span><span class="sxs-lookup"><span data-stu-id="296ed-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="296ed-127">В разделе mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="296ed-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="296ed-128">См. также</span><span class="sxs-lookup"><span data-stu-id="296ed-128">See also</span></span>



[<span data-ttu-id="296ed-129">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="296ed-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="296ed-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="296ed-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="296ed-131">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="296ed-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="296ed-132">FEID</span><span class="sxs-lookup"><span data-stu-id="296ed-132">FEID</span></span>](feid.md)

