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
ms.openlocfilehash: c417e6f4412bc40e8c2ebc056514eb96f60798f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426809"
---
# <a name="skey"></a><span data-ttu-id="d9b52-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="d9b52-103">SKEY</span></span>

  
  
<span data-ttu-id="d9b52-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9b52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9b52-105">Ключ источника для элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="d9b52-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d9b52-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d9b52-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="d9b52-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d9b52-107">Members</span></span>

 <span data-ttu-id="d9b52-108">_кодом_</span><span class="sxs-lookup"><span data-stu-id="d9b52-108">_guid_</span></span>
  
> <span data-ttu-id="d9b52-109">GUID сервера, создающего объект.</span><span class="sxs-lookup"><span data-stu-id="d9b52-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9b52-110">См. также</span><span class="sxs-lookup"><span data-stu-id="d9b52-110">See also</span></span>



[<span data-ttu-id="d9b52-111">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="d9b52-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d9b52-112">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="d9b52-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d9b52-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="d9b52-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="d9b52-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="d9b52-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="d9b52-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="d9b52-115">UPREADE</span></span>](upreade.md)

