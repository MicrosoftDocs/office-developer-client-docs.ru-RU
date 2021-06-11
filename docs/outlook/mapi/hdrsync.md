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
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410254"
---
# <a name="hdrsync"></a><span data-ttu-id="f639c-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="f639c-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="f639c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f639c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f639c-105">Сведения для синхронизации загона сообщений во время состояния [заглавного сообщения для скачивания.](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="f639c-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f639c-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f639c-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="f639c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="f639c-107">Members</span></span>

 <span data-ttu-id="f639c-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="f639c-108">_pupmsg_</span></span>
  
- <span data-ttu-id="f639c-109">[вышел] Сведения для текущего загона сообщений в локальном магазине.</span><span class="sxs-lookup"><span data-stu-id="f639c-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="f639c-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="f639c-110">_feidPar_</span></span>
  
- <span data-ttu-id="f639c-111">[вышел] ID записи для родительской папки элемента сообщения.</span><span class="sxs-lookup"><span data-stu-id="f639c-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="f639c-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="f639c-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="f639c-113">[] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f639c-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="f639c-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f639c-114">_ulFlags_</span></span>
  
- <span data-ttu-id="f639c-115">[in] Флаги для изменения поведения:</span><span class="sxs-lookup"><span data-stu-id="f639c-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="f639c-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="f639c-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="f639c-117">[in] Полный элемент находится в том же локальном хранилище, что и элемент header.</span><span class="sxs-lookup"><span data-stu-id="f639c-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="f639c-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="f639c-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="f639c-119">[in] Оптимизация внутренних операций копирования.</span><span class="sxs-lookup"><span data-stu-id="f639c-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="f639c-120">Это может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="f639c-120">This might cause data loss.</span></span> <span data-ttu-id="f639c-121">**HSF_LOCAL** необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="f639c-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="f639c-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="f639c-122">HSF_OK</span></span>
    
  - <span data-ttu-id="f639c-123">[in] Синхронизация header прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="f639c-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="f639c-124">Устанавливается клиентом после скачивания информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="f639c-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="f639c-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="f639c-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="f639c-126">[in] Полный элемент сообщения, включая заглавную версию сообщения, загруженную с сервера.</span><span class="sxs-lookup"><span data-stu-id="f639c-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="f639c-127">См. mapidefs.h для определения типа **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="f639c-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f639c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f639c-128">See also</span></span>



[<span data-ttu-id="f639c-129">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="f639c-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="f639c-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="f639c-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f639c-131">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="f639c-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f639c-132">FEID</span><span class="sxs-lookup"><span data-stu-id="f639c-132">FEID</span></span>](feid.md)

