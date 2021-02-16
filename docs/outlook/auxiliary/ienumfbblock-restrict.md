---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Ограничивает его указанным периодом времени.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431948"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="14cc9-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="14cc9-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="14cc9-104">Ограничивается указанным периодом времени.</span><span class="sxs-lookup"><span data-stu-id="14cc9-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="14cc9-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="14cc9-105">Quick info</span></span>

<span data-ttu-id="14cc9-106">См. [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="14cc9-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="14cc9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="14cc9-107">Parameters</span></span>

<span data-ttu-id="14cc9-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="14cc9-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="14cc9-109">[in] Время начала для ограничения этого перечня.</span><span class="sxs-lookup"><span data-stu-id="14cc9-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="14cc9-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="14cc9-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="14cc9-111">[in] Время окончания для ограничения этого перенамерения.</span><span class="sxs-lookup"><span data-stu-id="14cc9-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="14cc9-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="14cc9-112">Return values</span></span>

<span data-ttu-id="14cc9-113">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="14cc9-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14cc9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="14cc9-114">Remarks</span></span>

<span data-ttu-id="14cc9-115">Этот метод также сбрасывает enumeration.</span><span class="sxs-lookup"><span data-stu-id="14cc9-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="14cc9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="14cc9-116">See also</span></span>

- [<span data-ttu-id="14cc9-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="14cc9-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="14cc9-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="14cc9-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="14cc9-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="14cc9-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="14cc9-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="14cc9-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="14cc9-121">Использование относительного времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="14cc9-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

