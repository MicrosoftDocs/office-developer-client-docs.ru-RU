---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Перечисление для состояния занятости блоков занятости.
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319728"
---
# <a name="fbstatus"></a><span data-ttu-id="9720f-103">FBStatus</span><span class="sxs-lookup"><span data-stu-id="9720f-103">FBStatus</span></span>

<span data-ttu-id="9720f-104">Перечисление для состояния занятости блоков занятости.</span><span class="sxs-lookup"><span data-stu-id="9720f-104">An enumeration for the free/busy status of free/busy blocks.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9720f-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9720f-105">Quick info</span></span>

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a><span data-ttu-id="9720f-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9720f-106">Remarks</span></span>

<span data-ttu-id="9720f-107">Сведения о доступности блока времени определяют, как он отображается в календаре: свободен, **занят**, \*\*\*\* **под вопросом**или **в офисе**.</span><span class="sxs-lookup"><span data-stu-id="9720f-107">The free/busy status of a block of time determines how it is displayed on a calendar: **Free**, **Busy**, **Tentative**, or **Out of Office**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9720f-108">См. также</span><span class="sxs-lookup"><span data-stu-id="9720f-108">See also</span></span>

- [<span data-ttu-id="9720f-109">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="9720f-109">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="9720f-110">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="9720f-110">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)

