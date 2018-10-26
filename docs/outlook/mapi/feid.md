---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Последнее изменение: 2 июля 2012.'
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588309"
---
# <a name="feid"></a><span data-ttu-id="5d99e-103">FEID</span><span class="sxs-lookup"><span data-stu-id="5d99e-103">FEID</span></span>

 
  
<span data-ttu-id="5d99e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d99e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d99e-105">Идентификатор для папки.</span><span class="sxs-lookup"><span data-stu-id="5d99e-105">Identifier for a folder.</span></span> <span data-ttu-id="5d99e-106">Он содержит идентификатор входа и другие необходимые сведения.</span><span class="sxs-lookup"><span data-stu-id="5d99e-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5d99e-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="5d99e-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="5d99e-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5d99e-108">Members</span></span>

 <span data-ttu-id="5d99e-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="5d99e-109">_abFlags_</span></span>
  
> <span data-ttu-id="5d99e-110">Идентификатор записи 4-байтных папки.</span><span class="sxs-lookup"><span data-stu-id="5d99e-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="5d99e-111">Дополнительные сведения об идентификаторах запись MAPI можно **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="5d99e-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="5d99e-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="5d99e-112">_muid_</span></span>
  
> <span data-ttu-id="5d99e-113">GUID, идентифицирующий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d99e-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="5d99e-114">В разделе mapidefs.h для определения типа **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="5d99e-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="5d99e-115">_заполнитель_</span><span class="sxs-lookup"><span data-stu-id="5d99e-115">_placeholder_</span></span>
  
> <span data-ttu-id="5d99e-116">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5d99e-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="5d99e-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="5d99e-117">_ltid_</span></span>
  
> <span data-ttu-id="5d99e-118">Долгосрочные идентификатор папки.</span><span class="sxs-lookup"><span data-stu-id="5d99e-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d99e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="5d99e-119">See also</span></span>



[<span data-ttu-id="5d99e-120">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="5d99e-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5d99e-121">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="5d99e-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="5d99e-122">LTID</span><span class="sxs-lookup"><span data-stu-id="5d99e-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="5d99e-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="5d99e-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="5d99e-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="5d99e-124">SYNC</span></span>](sync.md)

