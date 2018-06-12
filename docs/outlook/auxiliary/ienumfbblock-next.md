---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Получает указанное количество блоков данных о доступности в перечислении.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807711"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="55deb-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="55deb-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="55deb-104">Получает указанное количество блоков данных о доступности в перечислении.</span><span class="sxs-lookup"><span data-stu-id="55deb-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="55deb-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="55deb-105">Quick info</span></span>

<span data-ttu-id="55deb-106">В разделе [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="55deb-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="55deb-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="55deb-107">Parameters</span></span>

<span data-ttu-id="55deb-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="55deb-108">_celt_</span></span>
  
> <span data-ttu-id="55deb-109">[in] Количество данных о доступности блоков *pblk* для извлечения.</span><span class="sxs-lookup"><span data-stu-id="55deb-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="55deb-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="55deb-110">_pblk_</span></span>
  
> <span data-ttu-id="55deb-111">[in] Указатель на массив сведений о доступности блоки.</span><span class="sxs-lookup"><span data-stu-id="55deb-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="55deb-112">Массив, выделяемого размер *celt* .</span><span class="sxs-lookup"><span data-stu-id="55deb-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="55deb-113">Запрошенный блоки занятости возвращаются в этот массив.</span><span class="sxs-lookup"><span data-stu-id="55deb-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="55deb-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="55deb-114">_pcfetch_</span></span>
  
> <span data-ttu-id="55deb-115">[out] Количество блоков сведений о доступности, фактически возвращаемую в *pblk* .</span><span class="sxs-lookup"><span data-stu-id="55deb-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="55deb-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="55deb-116">Return values</span></span>

|<span data-ttu-id="55deb-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="55deb-117">**HRESULT**</span></span>|<span data-ttu-id="55deb-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="55deb-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55deb-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="55deb-119">S_OK</span></span>  <br/> |<span data-ttu-id="55deb-120">Запрошенный количество блоков возвращена.</span><span class="sxs-lookup"><span data-stu-id="55deb-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="55deb-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="55deb-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="55deb-122">Запрошенный количество блоков не были возвращены.</span><span class="sxs-lookup"><span data-stu-id="55deb-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55deb-123">См. также</span><span class="sxs-lookup"><span data-stu-id="55deb-123">See also</span></span>

- [<span data-ttu-id="55deb-124">Константы (занятости API)</span><span class="sxs-lookup"><span data-stu-id="55deb-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="55deb-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="55deb-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="55deb-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="55deb-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="55deb-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="55deb-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="55deb-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="55deb-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="55deb-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="55deb-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

