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
ms.openlocfilehash: 24cc4b00f02c61395565fb7ddeb6a5b5a62afdc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591942"
---
# <a name="meid"></a><span data-ttu-id="4b4e0-103">MEID</span><span class="sxs-lookup"><span data-stu-id="4b4e0-103">MEID</span></span>

 
  
<span data-ttu-id="4b4e0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b4e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b4e0-105">Идентификатор элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="4b4e0-106">Он содержит идентификатор входа и другие необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4b4e0-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4b4e0-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="4b4e0-108">Members</span><span class="sxs-lookup"><span data-stu-id="4b4e0-108">Members</span></span>

 <span data-ttu-id="4b4e0-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="4b4e0-109">_abFlags_</span></span>
  
> <span data-ttu-id="4b4e0-110">Идентификатор записи 4-байтных для элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="4b4e0-111">Дополнительные сведения об идентификаторах запись MAPI можно **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="4b4e0-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="4b4e0-112">_muid_</span></span>
  
> <span data-ttu-id="4b4e0-113">GUID, идентифицирующий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="4b4e0-114">В разделе mapidefs.h для определения типа **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="4b4e0-115">_заполнитель_</span><span class="sxs-lookup"><span data-stu-id="4b4e0-115">_placeholder_</span></span>
  
> <span data-ttu-id="4b4e0-116">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="4b4e0-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="4b4e0-117">_ltidFld_</span></span>
  
> <span data-ttu-id="4b4e0-118">Долгосрочные идентификатор папки.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="4b4e0-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="4b4e0-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="4b4e0-120">Долгосрочные идентификатор элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="4b4e0-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b4e0-121">См. также</span><span class="sxs-lookup"><span data-stu-id="4b4e0-121">See also</span></span>



[<span data-ttu-id="4b4e0-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="4b4e0-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4b4e0-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="4b4e0-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4b4e0-124">LTID</span><span class="sxs-lookup"><span data-stu-id="4b4e0-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="4b4e0-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="4b4e0-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="4b4e0-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="4b4e0-126">UPMSG</span></span>](upmsg.md)

