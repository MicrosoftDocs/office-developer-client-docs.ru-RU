---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Определяет блок данных о доступности. Это элемент в календаре, представленное встречи или приглашения на собрание.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807682"
---
# <a name="fbblock1"></a><span data-ttu-id="e1a2f-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="e1a2f-104">FBBlock_1</span></span>

<span data-ttu-id="e1a2f-105">Определяет блок данных о доступности.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="e1a2f-106">Это элемент в календаре, представленное встречи или приглашения на собрание.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e1a2f-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e1a2f-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="e1a2f-108">Members</span><span class="sxs-lookup"><span data-stu-id="e1a2f-108">Members</span></span>

<span data-ttu-id="e1a2f-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="e1a2f-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="e1a2f-110">Время начала для блокировки, выраженная в относительно времени.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="e1a2f-111">Дополнительные сведения можно [Использовать относительное время для доступа к сведениям о доступности данных](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="e1a2f-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="e1a2f-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="e1a2f-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="e1a2f-113">Время окончания блокировки, выраженная в относительно времени.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="e1a2f-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="e1a2f-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="e1a2f-115">Состояние сведений о доступности для этого блока, указывающее пользователя вне офиса, «занят», под вопросом или бесплатно, период времени между _m_tmStart_ и _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="e1a2f-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1a2f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e1a2f-116">See also</span></span>

- [<span data-ttu-id="e1a2f-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="e1a2f-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="e1a2f-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="e1a2f-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="e1a2f-119">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="e1a2f-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

