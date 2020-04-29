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
# <a name="hdrsync"></a><span data-ttu-id="eafc5-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="eafc5-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="eafc5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eafc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eafc5-105">Сведения о синхронизации заголовка сообщения во время [загрузки состояния заголовка сообщения](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="eafc5-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="eafc5-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="eafc5-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="eafc5-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="eafc5-107">Members</span></span>

 <span data-ttu-id="eafc5-108">_пупмсг_</span><span class="sxs-lookup"><span data-stu-id="eafc5-108">_pupmsg_</span></span>
  
- <span data-ttu-id="eafc5-109">вышли Сведения о текущем заголовке сообщения в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="eafc5-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="eafc5-110">_феидпар_</span><span class="sxs-lookup"><span data-stu-id="eafc5-110">_feidPar_</span></span>
  
- <span data-ttu-id="eafc5-111">вышли Идентификатор записи для родительской папки элемента сообщения.</span><span class="sxs-lookup"><span data-stu-id="eafc5-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="eafc5-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="eafc5-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="eafc5-113">[] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eafc5-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="eafc5-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eafc5-114">_ulFlags_</span></span>
  
- <span data-ttu-id="eafc5-115">возврата Флаги для изменения поведения:</span><span class="sxs-lookup"><span data-stu-id="eafc5-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="eafc5-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="eafc5-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="eafc5-117">возврата Полный элемент находится в том же локальном хранилище, что и элемент заголовка.</span><span class="sxs-lookup"><span data-stu-id="eafc5-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="eafc5-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="eafc5-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="eafc5-119">возврата Оптимизируйте внутренние операции копирования.</span><span class="sxs-lookup"><span data-stu-id="eafc5-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="eafc5-120">Это может привести к потере данных.</span><span class="sxs-lookup"><span data-stu-id="eafc5-120">This might cause data loss.</span></span> <span data-ttu-id="eafc5-121">Необходимо задать **HSF_LOCAL** .</span><span class="sxs-lookup"><span data-stu-id="eafc5-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="eafc5-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="eafc5-122">HSF_OK</span></span>
    
  - <span data-ttu-id="eafc5-123">возврата Синхронизация заголовков выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="eafc5-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="eafc5-124">Устанавливается клиентом после скачивания информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="eafc5-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="eafc5-125">_пмсгфулл_</span><span class="sxs-lookup"><span data-stu-id="eafc5-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="eafc5-126">возврата Полный элемент сообщения, включая заголовок сообщения, загруженный с сервера.</span><span class="sxs-lookup"><span data-stu-id="eafc5-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="eafc5-127">Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="eafc5-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="eafc5-128">См. также</span><span class="sxs-lookup"><span data-stu-id="eafc5-128">See also</span></span>



[<span data-ttu-id="eafc5-129">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="eafc5-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="eafc5-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="eafc5-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="eafc5-131">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="eafc5-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="eafc5-132">FEID</span><span class="sxs-lookup"><span data-stu-id="eafc5-132">FEID</span></span>](feid.md)

