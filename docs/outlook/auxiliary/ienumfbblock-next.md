---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Получает следующее указанное количество блоков данных о занятости в этом перенамеровке.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422140"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="b7ef0-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="b7ef0-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="b7ef0-104">Возвращает следующее указанное количество блоков данных о занятости в этом перенамеровке.</span><span class="sxs-lookup"><span data-stu-id="b7ef0-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b7ef0-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b7ef0-105">Quick info</span></span>

<span data-ttu-id="b7ef0-106">См. [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="b7ef0-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="b7ef0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7ef0-107">Parameters</span></span>

<span data-ttu-id="b7ef0-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="b7ef0-108">_celt_</span></span>
  
> <span data-ttu-id="b7ef0-109">[in] Количество блоков данных о занятости в  *pblk*  для извлечения.</span><span class="sxs-lookup"><span data-stu-id="b7ef0-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="b7ef0-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="b7ef0-110">_pblk_</span></span>
  
> <span data-ttu-id="b7ef0-111">[in] Указатель на массив блоков занятости.</span><span class="sxs-lookup"><span data-stu-id="b7ef0-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="b7ef0-112">Для массива выделяется  *размером 3,5*  г.</span><span class="sxs-lookup"><span data-stu-id="b7ef0-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="b7ef0-113">В этом массиве возвращаются запрашиваемые блоки занятости.</span><span class="sxs-lookup"><span data-stu-id="b7ef0-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="b7ef0-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="b7ef0-114">_pcfetch_</span></span>
  
> <span data-ttu-id="b7ef0-115">[out] Количество блоков занятости, фактически возвращаемого *в pblk.*</span><span class="sxs-lookup"><span data-stu-id="b7ef0-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b7ef0-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b7ef0-116">Return values</span></span>

|<span data-ttu-id="b7ef0-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b7ef0-117">**HRESULT**</span></span>|<span data-ttu-id="b7ef0-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="b7ef0-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7ef0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7ef0-119">S_OK</span></span>  <br/> |<span data-ttu-id="b7ef0-120">Возвращено запрашиваемого количества блоков.</span><span class="sxs-lookup"><span data-stu-id="b7ef0-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="b7ef0-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b7ef0-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="b7ef0-122">Запрашиваемая часть блоков не возвращена.</span><span class="sxs-lookup"><span data-stu-id="b7ef0-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7ef0-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b7ef0-123">See also</span></span>

- [<span data-ttu-id="b7ef0-124">Константы (API занятости)</span><span class="sxs-lookup"><span data-stu-id="b7ef0-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="b7ef0-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="b7ef0-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="b7ef0-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="b7ef0-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="b7ef0-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="b7ef0-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="b7ef0-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="b7ef0-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="b7ef0-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="b7ef0-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

