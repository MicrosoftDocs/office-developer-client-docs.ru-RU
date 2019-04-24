---
title: Иенумфбблоккскип
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: ПроПускает указанное количество блоков данных о занятости.
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317551"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="2c2d6-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="2c2d6-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="2c2d6-104">ПроПускает указанное количество блоков данных о занятости.</span><span class="sxs-lookup"><span data-stu-id="2c2d6-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2c2d6-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="2c2d6-105">Quick info</span></span>

<span data-ttu-id="2c2d6-106">Обратитесь к разделу [иенумфбблокк](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="2c2d6-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="2c2d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c2d6-107">Parameters</span></span>

<span data-ttu-id="2c2d6-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="2c2d6-108">_celt_</span></span>
  
>  <span data-ttu-id="2c2d6-109">возврата Количество пропущенных блоков сведений о занятости.</span><span class="sxs-lookup"><span data-stu-id="2c2d6-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2c2d6-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2c2d6-110">Return values</span></span>

<span data-ttu-id="2c2d6-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="2c2d6-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c2d6-112">См. также</span><span class="sxs-lookup"><span data-stu-id="2c2d6-112">See also</span></span>

- [<span data-ttu-id="2c2d6-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="2c2d6-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="2c2d6-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="2c2d6-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="2c2d6-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="2c2d6-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="2c2d6-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="2c2d6-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

