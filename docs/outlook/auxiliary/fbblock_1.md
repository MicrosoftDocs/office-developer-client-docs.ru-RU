---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Определяет блок данных о занятости. Это элемент календаря, представленный встречей или запросом на собрание.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413201"
---
# <a name="fbblock_1"></a><span data-ttu-id="ddf7b-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="ddf7b-104">FBBlock_1</span></span>

<span data-ttu-id="ddf7b-105">Определяет блок данных о занятости.</span><span class="sxs-lookup"><span data-stu-id="ddf7b-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="ddf7b-106">Это элемент календаря, представленный встречей или запросом на собрание.</span><span class="sxs-lookup"><span data-stu-id="ddf7b-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ddf7b-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ddf7b-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="ddf7b-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="ddf7b-108">Members</span></span>

<span data-ttu-id="ddf7b-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="ddf7b-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="ddf7b-110">Время начала для блока, выраженного относительным временем.</span><span class="sxs-lookup"><span data-stu-id="ddf7b-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="ddf7b-111">Дополнительные сведения см. в сведениях [об использовании относительного времени для доступа к сведениям о доступности.](how-to-use-relative-time-to-access-free-busy-data.md)</span><span class="sxs-lookup"><span data-stu-id="ddf7b-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="ddf7b-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="ddf7b-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="ddf7b-113">Время окончания для блока, выраженного относительным временем.</span><span class="sxs-lookup"><span data-stu-id="ddf7b-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="ddf7b-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="ddf7b-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="ddf7b-115">Состояние занятости для этого блока, указывающее, является ли пользователь нет на должности, занят, находится под вопросом или свободен в течение периода времени между m_tmStart  _и_  _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="ddf7b-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ddf7b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ddf7b-116">See also</span></span>

- [<span data-ttu-id="ddf7b-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="ddf7b-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="ddf7b-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="ddf7b-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="ddf7b-119">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="ddf7b-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

