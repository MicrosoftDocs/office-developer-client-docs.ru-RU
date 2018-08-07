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
ms.openlocfilehash: bd1c327eb2042957c8fb043736950af3dae520b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808581"
---
# <a name="hdrsync"></a><span data-ttu-id="4f880-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="4f880-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="4f880-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f880-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f880-105">Сведения о синхронизации заголовок сообщения во время [загрузки состояния заголовок сообщения](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="4f880-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4f880-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4f880-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="4f880-107">Members</span><span class="sxs-lookup"><span data-stu-id="4f880-107">Members</span></span>

 <span data-ttu-id="4f880-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="4f880-108">_pupmsg_</span></span>
  
- <span data-ttu-id="4f880-109">[out] Сведения о текущем заголовок сообщения в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="4f880-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="4f880-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="4f880-110">_feidPar_</span></span>
  
- <span data-ttu-id="4f880-111">[out] Идентификатор записи для родительской папки сообщения элемента.</span><span class="sxs-lookup"><span data-stu-id="4f880-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="4f880-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="4f880-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="4f880-113">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4f880-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="4f880-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f880-114">_ulFlags_</span></span>
  
- <span data-ttu-id="4f880-115">[in] Флаги для изменения поведения:</span><span class="sxs-lookup"><span data-stu-id="4f880-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="4f880-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="4f880-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="4f880-117">[in] Все элементы находится в том же локальном хранилище, как заголовок элемента.</span><span class="sxs-lookup"><span data-stu-id="4f880-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="4f880-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="4f880-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="4f880-119">[in] Оптимизация операций внутренней копии.</span><span class="sxs-lookup"><span data-stu-id="4f880-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="4f880-120">Это может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="4f880-120">This might cause data loss.</span></span> <span data-ttu-id="4f880-121">Должно иметь значение **HSF_LOCAL** .</span><span class="sxs-lookup"><span data-stu-id="4f880-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="4f880-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="4f880-122">HSF_OK</span></span>
    
  - <span data-ttu-id="4f880-123">[in] Заголовок синхронизация прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="4f880-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="4f880-124">Клиент устанавливает это после загрузки информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="4f880-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="4f880-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="4f880-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="4f880-126">[in] Полное сообщение элемента, включая заголовок сообщения загружаются с сервера.</span><span class="sxs-lookup"><span data-stu-id="4f880-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="4f880-127">В разделе mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="4f880-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4f880-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4f880-128">See also</span></span>



[<span data-ttu-id="4f880-129">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="4f880-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4f880-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="4f880-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4f880-131">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="4f880-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4f880-132">FEID</span><span class="sxs-lookup"><span data-stu-id="4f880-132">FEID</span></span>](feid.md)

