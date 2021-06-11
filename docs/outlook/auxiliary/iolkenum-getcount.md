---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Получает количество учетных записей в этом переуметоре.
ms.openlocfilehash: 8571d5ff01501d980c8b6543607a658ad99085ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421825"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="baa26-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="baa26-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="baa26-104">Получает количество учетных записей в этом переуметоре.</span><span class="sxs-lookup"><span data-stu-id="baa26-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="baa26-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="baa26-105">Quick info</span></span>

<span data-ttu-id="baa26-106">См. [iOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="baa26-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="baa26-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="baa26-107">Parameters</span></span>

<span data-ttu-id="baa26-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="baa26-108">_pulCount_</span></span>
  
> <span data-ttu-id="baa26-109">[вышел] Указатель на количество объектов, которые будут засвещены.</span><span class="sxs-lookup"><span data-stu-id="baa26-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="baa26-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="baa26-110">Return values</span></span>

<span data-ttu-id="baa26-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="baa26-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="baa26-112">См. также</span><span class="sxs-lookup"><span data-stu-id="baa26-112">See also</span></span>

- [<span data-ttu-id="baa26-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="baa26-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="baa26-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="baa26-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="baa26-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="baa26-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

