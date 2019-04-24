---
title: Иенумфбблоккклоне
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Создает копию перечислителя с использованием того же ограничения времени, но устанавливая курсор в начало перечислителя.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317600"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="58b66-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="58b66-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="58b66-104">Создает копию перечислителя с использованием того же ограничения времени, но устанавливая курсор в начало перечислителя.</span><span class="sxs-lookup"><span data-stu-id="58b66-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="58b66-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="58b66-105">Quick info</span></span>

<span data-ttu-id="58b66-106">Обратитесь к разделу [иенумфбблокк](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="58b66-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="58b66-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="58b66-107">Parameters</span></span>

<span data-ttu-id="58b66-108">_ппклоне_</span><span class="sxs-lookup"><span data-stu-id="58b66-108">_ppclone_</span></span>
  
> <span data-ttu-id="58b66-109">вышли Указатель на копию интерфейса [иенумфбблокк](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="58b66-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="58b66-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="58b66-110">Return values</span></span>

|<span data-ttu-id="58b66-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="58b66-111">**HRESULT**</span></span>|<span data-ttu-id="58b66-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="58b66-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58b66-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="58b66-113">S_OK</span></span>  <br/> |<span data-ttu-id="58b66-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="58b66-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="58b66-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="58b66-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="58b66-116">Недостаточно памяти для создания копии.</span><span class="sxs-lookup"><span data-stu-id="58b66-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58b66-117">См. также</span><span class="sxs-lookup"><span data-stu-id="58b66-117">See also</span></span>

- [<span data-ttu-id="58b66-118">Константы (API сведений о доступности)</span><span class="sxs-lookup"><span data-stu-id="58b66-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="58b66-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="58b66-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="58b66-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="58b66-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="58b66-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="58b66-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="58b66-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="58b66-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

