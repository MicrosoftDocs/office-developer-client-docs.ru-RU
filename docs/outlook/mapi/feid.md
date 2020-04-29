---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Дата последнего изменения: 02 июля 2012 г.'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409813"
---
# <a name="feid"></a><span data-ttu-id="f28b4-103">FEID</span><span class="sxs-lookup"><span data-stu-id="f28b4-103">FEID</span></span>

 
  
<span data-ttu-id="f28b4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f28b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f28b4-105">Идентификатор папки.</span><span class="sxs-lookup"><span data-stu-id="f28b4-105">Identifier for a folder.</span></span> <span data-ttu-id="f28b4-106">Он содержит идентификатор записи и другую важную информацию.</span><span class="sxs-lookup"><span data-stu-id="f28b4-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f28b4-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f28b4-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="f28b4-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="f28b4-108">Members</span></span>

 <span data-ttu-id="f28b4-109">_абфлагс_</span><span class="sxs-lookup"><span data-stu-id="f28b4-109">_abFlags_</span></span>
  
> <span data-ttu-id="f28b4-110">Идентификатор записи (4 байта) для папки.</span><span class="sxs-lookup"><span data-stu-id="f28b4-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="f28b4-111">Дополнительные сведения об идентификаторах записей MAPI приведены в разделе **[EntryID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="f28b4-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="f28b4-112">_Muid_</span><span class="sxs-lookup"><span data-stu-id="f28b4-112">_muid_</span></span>
  
> <span data-ttu-id="f28b4-113">GUID, определяющий поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="f28b4-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="f28b4-114">Определение типа **мапиуид**можно найти в файле MAPIDEFS. h.</span><span class="sxs-lookup"><span data-stu-id="f28b4-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="f28b4-115">_нагляд_</span><span class="sxs-lookup"><span data-stu-id="f28b4-115">_placeholder_</span></span>
  
> <span data-ttu-id="f28b4-116">Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f28b4-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="f28b4-117">_лтид_</span><span class="sxs-lookup"><span data-stu-id="f28b4-117">_ltid_</span></span>
  
> <span data-ttu-id="f28b4-118">Долгосрочный идентификатор папки.</span><span class="sxs-lookup"><span data-stu-id="f28b4-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f28b4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f28b4-119">See also</span></span>



[<span data-ttu-id="f28b4-120">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="f28b4-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f28b4-121">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="f28b4-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="f28b4-122">LTID</span><span class="sxs-lookup"><span data-stu-id="f28b4-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="f28b4-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="f28b4-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="f28b4-124">Синхр</span><span class="sxs-lookup"><span data-stu-id="f28b4-124">SYNC</span></span>](sync.md)

