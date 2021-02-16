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
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419438"
---
# <a name="ltid"></a><span data-ttu-id="de719-103">LTID</span><span class="sxs-lookup"><span data-stu-id="de719-103">LTID</span></span>

  
  
<span data-ttu-id="de719-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de719-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de719-105">Универсальный долгосрочный ИД объекта в хранилище Outlook.</span><span class="sxs-lookup"><span data-stu-id="de719-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="de719-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="de719-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="de719-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="de719-107">Members</span></span>

 <span data-ttu-id="de719-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="de719-108">_guid_</span></span>
  
- <span data-ttu-id="de719-109">[out] GUID сервера, создав объект.</span><span class="sxs-lookup"><span data-stu-id="de719-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="de719-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="de719-110">_globcnt_</span></span>
  
- <span data-ttu-id="de719-111">[out] 6-byte unique number that identifies the object within the Outlook store.</span><span class="sxs-lookup"><span data-stu-id="de719-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="de719-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="de719-112">_wLevel_</span></span>
  
- <span data-ttu-id="de719-113">[out] Уровень иерархии ИД записи для папки "Избранное" в Exchange.</span><span class="sxs-lookup"><span data-stu-id="de719-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de719-114">См. также</span><span class="sxs-lookup"><span data-stu-id="de719-114">See also</span></span>



[<span data-ttu-id="de719-115">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="de719-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="de719-116">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="de719-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="de719-117">FEID</span><span class="sxs-lookup"><span data-stu-id="de719-117">FEID</span></span>](feid.md)

