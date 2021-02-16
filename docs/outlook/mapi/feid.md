---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409813"
---
# <a name="feid"></a><span data-ttu-id="a6295-103">FEID</span><span class="sxs-lookup"><span data-stu-id="a6295-103">FEID</span></span>

 
  
<span data-ttu-id="a6295-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6295-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6295-105">Идентификатор папки.</span><span class="sxs-lookup"><span data-stu-id="a6295-105">Identifier for a folder.</span></span> <span data-ttu-id="a6295-106">Он содержит идентификатор записи и другую релевантную информацию.</span><span class="sxs-lookup"><span data-stu-id="a6295-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a6295-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a6295-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="a6295-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="a6295-108">Members</span></span>

 <span data-ttu-id="a6295-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="a6295-109">_abFlags_</span></span>
  
> <span data-ttu-id="a6295-110">4-byte entry identifier for the folder.</span><span class="sxs-lookup"><span data-stu-id="a6295-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="a6295-111">Дополнительные сведения об идентификаторах записей MAPI см. в **[entryID.](entryid.md)**</span><span class="sxs-lookup"><span data-stu-id="a6295-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="a6295-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="a6295-112">_muid_</span></span>
  
> <span data-ttu-id="a6295-113">GUID, идентифицирует поставщика магазина.</span><span class="sxs-lookup"><span data-stu-id="a6295-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="a6295-114">Определение типа **MAPIUID** см. в mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="a6295-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="a6295-115">_placeholder_</span><span class="sxs-lookup"><span data-stu-id="a6295-115">_placeholder_</span></span>
  
> <span data-ttu-id="a6295-116">Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a6295-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="a6295-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="a6295-117">_ltid_</span></span>
  
> <span data-ttu-id="a6295-118">Долгосрочный ИД папки.</span><span class="sxs-lookup"><span data-stu-id="a6295-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6295-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a6295-119">See also</span></span>



[<span data-ttu-id="a6295-120">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="a6295-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a6295-121">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="a6295-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a6295-122">LTID</span><span class="sxs-lookup"><span data-stu-id="a6295-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="a6295-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="a6295-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="a6295-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="a6295-124">SYNC</span></span>](sync.md)

