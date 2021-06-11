---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Создает копию этого перемерителя, используя одно и то же ограничение времени, но устанавливая курсор к началу этого.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413404"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="c4556-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="c4556-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="c4556-104">Создает копию этого перемерителя, используя одно и то же ограничение времени, но устанавливая курсор к началу этого.</span><span class="sxs-lookup"><span data-stu-id="c4556-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c4556-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c4556-105">Quick info</span></span>

<span data-ttu-id="c4556-106">См. [iEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="c4556-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="c4556-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="c4556-107">Parameters</span></span>

<span data-ttu-id="c4556-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="c4556-108">_ppclone_</span></span>
  
> <span data-ttu-id="c4556-109">[вышел] Указатель на копию интерфейса [IEnumFBBlock.](ienumfbblock.md)</span><span class="sxs-lookup"><span data-stu-id="c4556-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c4556-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c4556-110">Return values</span></span>

|<span data-ttu-id="c4556-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4556-111">**HRESULT**</span></span>|<span data-ttu-id="c4556-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="c4556-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4556-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4556-113">S_OK</span></span>  <br/> |<span data-ttu-id="c4556-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="c4556-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="c4556-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c4556-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="c4556-116">Для создания копии не хватает памяти.</span><span class="sxs-lookup"><span data-stu-id="c4556-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4556-117">См. также</span><span class="sxs-lookup"><span data-stu-id="c4556-117">See also</span></span>

- [<span data-ttu-id="c4556-118">Константы (API free/busy)</span><span class="sxs-lookup"><span data-stu-id="c4556-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="c4556-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="c4556-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="c4556-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="c4556-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="c4556-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="c4556-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="c4556-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="c4556-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

