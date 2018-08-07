---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Получает число учетных записей в перечислитель.
ms.openlocfilehash: dd4152a898bdaa96883bcd27ab3ec0d94e80fd90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807870"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="a9349-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="a9349-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="a9349-104">Получает число учетных записей в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="a9349-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a9349-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a9349-105">Quick info</span></span>

<span data-ttu-id="a9349-106">В разделе [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="a9349-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="a9349-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9349-107">Parameters</span></span>

<span data-ttu-id="a9349-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="a9349-108">_pulCount_</span></span>
  
> <span data-ttu-id="a9349-109">[out] Указатель на количество перечисляемых объектов.</span><span class="sxs-lookup"><span data-stu-id="a9349-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a9349-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a9349-110">Return values</span></span>

<span data-ttu-id="a9349-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="a9349-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9349-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a9349-112">See also</span></span>

- [<span data-ttu-id="a9349-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="a9349-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="a9349-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="a9349-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="a9349-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="a9349-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

