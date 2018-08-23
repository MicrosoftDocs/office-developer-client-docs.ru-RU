---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569857"
---
# <a name="ltid"></a><span data-ttu-id="9ed64-103">LTID</span><span class="sxs-lookup"><span data-stu-id="9ed64-103">LTID</span></span>

  
  
<span data-ttu-id="9ed64-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ed64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ed64-105">Универсальный длинный идентификатор термина объекта в хранилище Outlook.</span><span class="sxs-lookup"><span data-stu-id="9ed64-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9ed64-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9ed64-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="9ed64-107">Members</span><span class="sxs-lookup"><span data-stu-id="9ed64-107">Members</span></span>

 <span data-ttu-id="9ed64-108">_Идентификатор GUID_</span><span class="sxs-lookup"><span data-stu-id="9ed64-108">_guid_</span></span>
  
- <span data-ttu-id="9ed64-109">[out] Идентификатор GUID сервера, создавшее этот объект.</span><span class="sxs-lookup"><span data-stu-id="9ed64-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="9ed64-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="9ed64-110">_globcnt_</span></span>
  
- <span data-ttu-id="9ed64-111">[out] 6-байтовое уникальный номер, идентифицирующий объекта в хранилище Outlook.</span><span class="sxs-lookup"><span data-stu-id="9ed64-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="9ed64-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="9ed64-112">_wLevel_</span></span>
  
- <span data-ttu-id="9ed64-113">[out] Уровень иерархии идентификатор записи для Exchange избранные общей папки.</span><span class="sxs-lookup"><span data-stu-id="9ed64-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ed64-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9ed64-114">See also</span></span>



[<span data-ttu-id="9ed64-115">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="9ed64-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9ed64-116">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="9ed64-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9ed64-117">FEID</span><span class="sxs-lookup"><span data-stu-id="9ed64-117">FEID</span></span>](feid.md)

