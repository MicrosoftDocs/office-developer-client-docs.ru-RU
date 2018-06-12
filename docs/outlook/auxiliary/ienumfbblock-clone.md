---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Создает копию перечислителя, с помощью же ограничения времени, но установки курсора в начало перечислитель.
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807705"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="53384-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="53384-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="53384-104">Создает копию перечислителя, с помощью же ограничения времени, но установки курсора в начало перечислитель.</span><span class="sxs-lookup"><span data-stu-id="53384-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="53384-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="53384-105">Quick info</span></span>

<span data-ttu-id="53384-106">В разделе [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="53384-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="53384-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="53384-107">Parameters</span></span>

<span data-ttu-id="53384-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="53384-108">_ppclone_</span></span>
  
> <span data-ttu-id="53384-109">[out] A указателя копию интерфейс [IEnumFBBlock](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="53384-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="53384-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="53384-110">Return values</span></span>

|<span data-ttu-id="53384-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="53384-111">**HRESULT**</span></span>|<span data-ttu-id="53384-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="53384-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53384-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="53384-113">S_OK</span></span>  <br/> |<span data-ttu-id="53384-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="53384-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="53384-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="53384-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="53384-116">Не хватает памяти для создания копии.</span><span class="sxs-lookup"><span data-stu-id="53384-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53384-117">См. также</span><span class="sxs-lookup"><span data-stu-id="53384-117">See also</span></span>

- [<span data-ttu-id="53384-118">Константы (занятости API)</span><span class="sxs-lookup"><span data-stu-id="53384-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="53384-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="53384-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="53384-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="53384-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="53384-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="53384-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="53384-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="53384-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

