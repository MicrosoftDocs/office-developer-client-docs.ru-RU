---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Получает следующее указанное количество блоков бесплатных и загруженных данных в переумериях.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422140"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="8a021-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="8a021-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="8a021-104">Получает следующее указанное количество блоков бесплатных и загруженных данных в переумериях.</span><span class="sxs-lookup"><span data-stu-id="8a021-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8a021-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8a021-105">Quick info</span></span>

<span data-ttu-id="8a021-106">См. [iEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="8a021-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="8a021-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8a021-107">Parameters</span></span>

<span data-ttu-id="8a021-108">_кельт_</span><span class="sxs-lookup"><span data-stu-id="8a021-108">_celt_</span></span>
  
> <span data-ttu-id="8a021-109">[in] Количество бесплатных и загруженных блоков данных  *в pblk*  для получения.</span><span class="sxs-lookup"><span data-stu-id="8a021-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="8a021-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="8a021-110">_pblk_</span></span>
  
> <span data-ttu-id="8a021-111">[in] Указатель на массив бесплатных и занятых блоков.</span><span class="sxs-lookup"><span data-stu-id="8a021-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="8a021-112">Массиву выделяется размер *кельта.*</span><span class="sxs-lookup"><span data-stu-id="8a021-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="8a021-113">Запрашиваемая бесплатная/занятая блоки возвращаются в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="8a021-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="8a021-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="8a021-114">_pcfetch_</span></span>
  
> <span data-ttu-id="8a021-115">[вышел] Количество бесплатных и занятых блоков фактически возвращается  *в pblk*  .</span><span class="sxs-lookup"><span data-stu-id="8a021-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8a021-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8a021-116">Return values</span></span>

|<span data-ttu-id="8a021-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8a021-117">**HRESULT**</span></span>|<span data-ttu-id="8a021-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="8a021-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a021-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a021-119">S_OK</span></span>  <br/> |<span data-ttu-id="8a021-120">Возвращено запрашиваемого количества блоков.</span><span class="sxs-lookup"><span data-stu-id="8a021-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="8a021-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="8a021-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="8a021-122">Запрашиваемая часть блоков не возвращена.</span><span class="sxs-lookup"><span data-stu-id="8a021-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a021-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8a021-123">See also</span></span>

- [<span data-ttu-id="8a021-124">Константы (API free/busy)</span><span class="sxs-lookup"><span data-stu-id="8a021-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="8a021-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="8a021-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="8a021-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="8a021-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="8a021-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="8a021-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="8a021-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="8a021-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="8a021-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="8a021-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

