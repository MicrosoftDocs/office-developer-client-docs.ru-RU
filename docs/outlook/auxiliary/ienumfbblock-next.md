---
title: Иенумфбблоккнекст
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Получает следующее указанное количество блоков данных о занятости в перечислении.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319595"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="8d2fb-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="8d2fb-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="8d2fb-104">Получает следующее указанное количество блоков данных о занятости в перечислении.</span><span class="sxs-lookup"><span data-stu-id="8d2fb-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8d2fb-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8d2fb-105">Quick info</span></span>

<span data-ttu-id="8d2fb-106">Обратитесь к разделу [иенумфбблокк](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="8d2fb-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="8d2fb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d2fb-107">Parameters</span></span>

<span data-ttu-id="8d2fb-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="8d2fb-108">_celt_</span></span>
  
> <span data-ttu-id="8d2fb-109">возврата Количество блоков данных о занятости в *пблк* , которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="8d2fb-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="8d2fb-110">_пблк_</span><span class="sxs-lookup"><span data-stu-id="8d2fb-110">_pblk_</span></span>
  
> <span data-ttu-id="8d2fb-111">возврата Указатель на массив блоков занятости.</span><span class="sxs-lookup"><span data-stu-id="8d2fb-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="8d2fb-112">Размер массива размещается в параметре *celt* .</span><span class="sxs-lookup"><span data-stu-id="8d2fb-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="8d2fb-113">Запрошенные блоки сведений о занятости возвращаются в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="8d2fb-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="8d2fb-114">_пкфетч_</span><span class="sxs-lookup"><span data-stu-id="8d2fb-114">_pcfetch_</span></span>
  
> <span data-ttu-id="8d2fb-115">вышли Количество блоков сведений о доступности, фактически возвращенных в *пблк* .</span><span class="sxs-lookup"><span data-stu-id="8d2fb-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="8d2fb-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8d2fb-116">Return values</span></span>

|<span data-ttu-id="8d2fb-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8d2fb-117">**HRESULT**</span></span>|<span data-ttu-id="8d2fb-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="8d2fb-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d2fb-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d2fb-119">S_OK</span></span>  <br/> |<span data-ttu-id="8d2fb-120">Возвращено запрошенное число блоков.</span><span class="sxs-lookup"><span data-stu-id="8d2fb-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="8d2fb-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="8d2fb-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="8d2fb-122">Запрошенное число блоков не было возвращено.</span><span class="sxs-lookup"><span data-stu-id="8d2fb-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d2fb-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8d2fb-123">See also</span></span>

- [<span data-ttu-id="8d2fb-124">Константы (API сведений о доступности)</span><span class="sxs-lookup"><span data-stu-id="8d2fb-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="8d2fb-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="8d2fb-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="8d2fb-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="8d2fb-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="8d2fb-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="8d2fb-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="8d2fb-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="8d2fb-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="8d2fb-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="8d2fb-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

