---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Пропускает указанное число учетных записей в перечислитель.
ms.openlocfilehash: 2791f1204cedf5e91d13923e50dfc45b981b7e26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807863"
---
# <a name="iolkenumskip"></a><span data-ttu-id="8a17b-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="8a17b-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="8a17b-104">Пропускает указанное число учетных записей в перечислитель.</span><span class="sxs-lookup"><span data-stu-id="8a17b-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8a17b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8a17b-105">Quick info</span></span>

<span data-ttu-id="8a17b-106">В разделе [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="8a17b-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="8a17b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a17b-107">Parameters</span></span>

<span data-ttu-id="8a17b-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="8a17b-108">_cSkip_</span></span>
  
> <span data-ttu-id="8a17b-109">[in] Число учетных записей был пропущен.</span><span class="sxs-lookup"><span data-stu-id="8a17b-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8a17b-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8a17b-110">Return values</span></span>

<span data-ttu-id="8a17b-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="8a17b-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a17b-112">См. также</span><span class="sxs-lookup"><span data-stu-id="8a17b-112">See also</span></span>

- [<span data-ttu-id="8a17b-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="8a17b-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="8a17b-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="8a17b-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="8a17b-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="8a17b-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

