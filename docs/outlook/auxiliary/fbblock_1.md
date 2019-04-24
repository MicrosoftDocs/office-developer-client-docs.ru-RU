---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Определяет блок данных о доступности. Это элемент календаря, представленный в приглашении на встречу или собрание.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317670"
---
# <a name="fbblock1"></a><span data-ttu-id="1e091-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="1e091-104">FBBlock_1</span></span>

<span data-ttu-id="1e091-105">Определяет блок данных о доступности.</span><span class="sxs-lookup"><span data-stu-id="1e091-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="1e091-106">Это элемент календаря, представленный в приглашении на встречу или собрание.</span><span class="sxs-lookup"><span data-stu-id="1e091-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1e091-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1e091-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="1e091-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="1e091-108">Members</span></span>

<span data-ttu-id="1e091-109">_М_тмстарт_</span><span class="sxs-lookup"><span data-stu-id="1e091-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="1e091-110">Время начала блока, выраженное в виде относительного времени.</span><span class="sxs-lookup"><span data-stu-id="1e091-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="1e091-111">Дополнительные сведения см. [в разделе Использование относительного времени для доступа к данным о занятости](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="1e091-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="1e091-112">_М_тменд_</span><span class="sxs-lookup"><span data-stu-id="1e091-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="1e091-113">Время окончания блока, выраженное в виде относительного времени.</span><span class="sxs-lookup"><span data-stu-id="1e091-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="1e091-114">_М_фбстатус_</span><span class="sxs-lookup"><span data-stu-id="1e091-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="1e091-115">Сведения о доступности этого блока, указывающие на то, что пользователь находится вне офиса, занят, находится под вопросом или свободен в течение периода времени между _м_тмстарт_ и _м_тменд_.</span><span class="sxs-lookup"><span data-stu-id="1e091-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e091-116">См. также</span><span class="sxs-lookup"><span data-stu-id="1e091-116">See also</span></span>

- [<span data-ttu-id="1e091-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="1e091-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="1e091-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="1e091-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="1e091-119">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="1e091-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

