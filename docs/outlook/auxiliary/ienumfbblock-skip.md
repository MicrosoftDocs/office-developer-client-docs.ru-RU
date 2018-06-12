---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Пропускает указанное число блоков данных о доступности.
ms.openlocfilehash: 63f699d09e143a879702e8dc76beb8a969a77b82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807704"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="8ce19-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="8ce19-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="8ce19-104">Пропускает указанное число блоков данных о доступности.</span><span class="sxs-lookup"><span data-stu-id="8ce19-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8ce19-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8ce19-105">Quick info</span></span>

<span data-ttu-id="8ce19-106">В разделе [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="8ce19-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="8ce19-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8ce19-107">Parameters</span></span>

<span data-ttu-id="8ce19-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="8ce19-108">_celt_</span></span>
  
>  <span data-ttu-id="8ce19-109">[in] Количество блоков сведений о доступности для пропуска.</span><span class="sxs-lookup"><span data-stu-id="8ce19-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8ce19-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8ce19-110">Return values</span></span>

<span data-ttu-id="8ce19-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="8ce19-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ce19-112">См. также</span><span class="sxs-lookup"><span data-stu-id="8ce19-112">See also</span></span>

- [<span data-ttu-id="8ce19-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="8ce19-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="8ce19-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="8ce19-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="8ce19-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="8ce19-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="8ce19-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="8ce19-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

