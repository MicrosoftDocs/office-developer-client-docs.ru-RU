---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Дата последнего изменения: 03 июля, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430310"
---
# <a name="meid"></a><span data-ttu-id="5a24c-103">MEID</span><span class="sxs-lookup"><span data-stu-id="5a24c-103">MEID</span></span>

 
  
<span data-ttu-id="5a24c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a24c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a24c-105">Идентификатор элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="5a24c-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="5a24c-106">Он содержит идентификатор записи и другую важную информацию.</span><span class="sxs-lookup"><span data-stu-id="5a24c-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5a24c-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="5a24c-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="5a24c-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5a24c-108">Members</span></span>

 <span data-ttu-id="5a24c-109">_Абфлагс_</span><span class="sxs-lookup"><span data-stu-id="5a24c-109">_abFlags_</span></span>
  
> <span data-ttu-id="5a24c-110">Идентификатор записи (4 байта) для элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="5a24c-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="5a24c-111">Дополнительные сведения об идентификаторах записей MAPI приведены в разделе **[EntryID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="5a24c-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="5a24c-112">_Muid_</span><span class="sxs-lookup"><span data-stu-id="5a24c-112">_muid_</span></span>
  
> <span data-ttu-id="5a24c-113">GUID, определяющий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="5a24c-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="5a24c-114">Определение типа **мапиуид**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="5a24c-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="5a24c-115">_нагляд_</span><span class="sxs-lookup"><span data-stu-id="5a24c-115">_placeholder_</span></span>
  
> <span data-ttu-id="5a24c-116">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5a24c-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="5a24c-117">_Лтидфлд_</span><span class="sxs-lookup"><span data-stu-id="5a24c-117">_ltidFld_</span></span>
  
> <span data-ttu-id="5a24c-118">Долгосрочный идентификатор папки.</span><span class="sxs-lookup"><span data-stu-id="5a24c-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="5a24c-119">_Лтидмсг_</span><span class="sxs-lookup"><span data-stu-id="5a24c-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="5a24c-120">Долгосрочный идентификатор элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="5a24c-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5a24c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="5a24c-121">See also</span></span>



[<span data-ttu-id="5a24c-122">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="5a24c-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="5a24c-123">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="5a24c-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="5a24c-124">LTID</span><span class="sxs-lookup"><span data-stu-id="5a24c-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="5a24c-125">Синхр</span><span class="sxs-lookup"><span data-stu-id="5a24c-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="5a24c-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="5a24c-126">UPMSG</span></span>](upmsg.md)

