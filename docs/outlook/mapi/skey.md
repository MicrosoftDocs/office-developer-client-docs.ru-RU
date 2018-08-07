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
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812321"
---
# <a name="skey"></a><span data-ttu-id="91bbb-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="91bbb-103">SKEY</span></span>

  
  
<span data-ttu-id="91bbb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91bbb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91bbb-105">Ключ источника для элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="91bbb-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="91bbb-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="91bbb-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="91bbb-107">Members</span><span class="sxs-lookup"><span data-stu-id="91bbb-107">Members</span></span>

 <span data-ttu-id="91bbb-108">_Идентификатор GUID_</span><span class="sxs-lookup"><span data-stu-id="91bbb-108">_guid_</span></span>
  
> <span data-ttu-id="91bbb-109">Идентификатор GUID сервера, создание объекта.</span><span class="sxs-lookup"><span data-stu-id="91bbb-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91bbb-110">См. также</span><span class="sxs-lookup"><span data-stu-id="91bbb-110">See also</span></span>



[<span data-ttu-id="91bbb-111">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="91bbb-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="91bbb-112">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="91bbb-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="91bbb-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="91bbb-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="91bbb-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="91bbb-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="91bbb-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="91bbb-115">UPREADE</span></span>](upreade.md)

