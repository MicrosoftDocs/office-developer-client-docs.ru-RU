---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810035"
---
# <a name="meid"></a><span data-ttu-id="83fdd-103">MEID</span><span class="sxs-lookup"><span data-stu-id="83fdd-103">MEID</span></span>

 
  
<span data-ttu-id="83fdd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83fdd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83fdd-105">Идентификатор элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="83fdd-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="83fdd-106">Он содержит идентификатор входа и другие необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="83fdd-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="83fdd-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="83fdd-107">Quick info</span></span>

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a><span data-ttu-id="83fdd-108">Members</span><span class="sxs-lookup"><span data-stu-id="83fdd-108">Members</span></span>

 <span data-ttu-id="83fdd-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="83fdd-109">_abFlags_</span></span>
  
> <span data-ttu-id="83fdd-110">Идентификатор записи 4-байтных для элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="83fdd-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="83fdd-111">Дополнительные сведения об идентификаторах запись MAPI можно **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="83fdd-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="83fdd-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="83fdd-112">_muid_</span></span>
  
> <span data-ttu-id="83fdd-113">GUID, идентифицирующий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="83fdd-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="83fdd-114">В разделе mapidefs.h для определения типа **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="83fdd-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="83fdd-115">_заполнитель_</span><span class="sxs-lookup"><span data-stu-id="83fdd-115">_placeholder_</span></span>
  
> <span data-ttu-id="83fdd-116">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="83fdd-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="83fdd-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="83fdd-117">_ltidFld_</span></span>
  
> <span data-ttu-id="83fdd-118">Долгосрочные идентификатор папки.</span><span class="sxs-lookup"><span data-stu-id="83fdd-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="83fdd-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="83fdd-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="83fdd-120">Долгосрочные идентификатор элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="83fdd-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="83fdd-121">См. также</span><span class="sxs-lookup"><span data-stu-id="83fdd-121">See also</span></span>



[<span data-ttu-id="83fdd-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="83fdd-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="83fdd-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="83fdd-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="83fdd-124">LTID</span><span class="sxs-lookup"><span data-stu-id="83fdd-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="83fdd-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="83fdd-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="83fdd-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="83fdd-126">UPMSG</span></span>](upmsg.md)

