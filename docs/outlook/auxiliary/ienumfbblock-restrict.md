---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Ограничивает число перечисления для заданного периода времени.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807702"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="fd829-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="fd829-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="fd829-104">Ограничивает число перечисления для заданного периода времени.</span><span class="sxs-lookup"><span data-stu-id="fd829-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fd829-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fd829-105">Quick info</span></span>

<span data-ttu-id="fd829-106">В разделе [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="fd829-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="fd829-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="fd829-107">Parameters</span></span>

<span data-ttu-id="fd829-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="fd829-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="fd829-109">[in] Время начала, чтобы ограничить перечисления.</span><span class="sxs-lookup"><span data-stu-id="fd829-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="fd829-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="fd829-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="fd829-111">[in] Время окончания для ограничения перечисления.</span><span class="sxs-lookup"><span data-stu-id="fd829-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fd829-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="fd829-112">Return values</span></span>

<span data-ttu-id="fd829-113">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="fd829-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd829-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="fd829-114">Remarks</span></span>

<span data-ttu-id="fd829-115">Этот метод также восстанавливаются значения по умолчанию перечисления.</span><span class="sxs-lookup"><span data-stu-id="fd829-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fd829-116">См. также</span><span class="sxs-lookup"><span data-stu-id="fd829-116">See also</span></span>

- [<span data-ttu-id="fd829-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="fd829-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="fd829-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="fd829-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="fd829-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="fd829-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="fd829-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="fd829-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="fd829-121">Использование относительных времени для доступа к данным о доступности</span><span class="sxs-lookup"><span data-stu-id="fd829-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

