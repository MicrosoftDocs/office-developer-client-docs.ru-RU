---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 26b08535d81cb961ed0ace70ea227316b30cd526
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573462"
---
# <a name="skey"></a><span data-ttu-id="bd24c-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="bd24c-103">SKEY</span></span>

  
  
<span data-ttu-id="bd24c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd24c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd24c-105">Ключ источника для элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="bd24c-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bd24c-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bd24c-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="bd24c-107">Members</span><span class="sxs-lookup"><span data-stu-id="bd24c-107">Members</span></span>

 <span data-ttu-id="bd24c-108">_Идентификатор GUID_</span><span class="sxs-lookup"><span data-stu-id="bd24c-108">_guid_</span></span>
  
> <span data-ttu-id="bd24c-109">Идентификатор GUID сервера, создание объекта.</span><span class="sxs-lookup"><span data-stu-id="bd24c-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd24c-110">См. также</span><span class="sxs-lookup"><span data-stu-id="bd24c-110">See also</span></span>



[<span data-ttu-id="bd24c-111">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="bd24c-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bd24c-112">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="bd24c-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="bd24c-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="bd24c-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="bd24c-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="bd24c-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="bd24c-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="bd24c-115">UPREADE</span></span>](upreade.md)

