---
title: иенумфбблоккклоне
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Создает копию перечислителя с использованием того же ограничения времени, но устанавливая курсор в начало перечислителя.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413404"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="9c0e8-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="9c0e8-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="9c0e8-104">Создает копию перечислителя с использованием того же ограничения времени, но устанавливая курсор в начало перечислителя.</span><span class="sxs-lookup"><span data-stu-id="9c0e8-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9c0e8-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9c0e8-105">Quick info</span></span>

<span data-ttu-id="9c0e8-106">Обратитесь к разделу [иенумфбблокк](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="9c0e8-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="9c0e8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c0e8-107">Parameters</span></span>

<span data-ttu-id="9c0e8-108">_ппклоне_</span><span class="sxs-lookup"><span data-stu-id="9c0e8-108">_ppclone_</span></span>
  
> <span data-ttu-id="9c0e8-109">вышли Указатель на копию интерфейса [иенумфбблокк](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="9c0e8-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="9c0e8-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9c0e8-110">Return values</span></span>

|<span data-ttu-id="9c0e8-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c0e8-111">**HRESULT**</span></span>|<span data-ttu-id="9c0e8-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="9c0e8-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c0e8-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c0e8-113">S_OK</span></span>  <br/> |<span data-ttu-id="9c0e8-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="9c0e8-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="9c0e8-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="9c0e8-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="9c0e8-116">Недостаточно памяти для создания копии.</span><span class="sxs-lookup"><span data-stu-id="9c0e8-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c0e8-117">См. также</span><span class="sxs-lookup"><span data-stu-id="9c0e8-117">See also</span></span>

- [<span data-ttu-id="9c0e8-118">Константы (API сведений о доступности)</span><span class="sxs-lookup"><span data-stu-id="9c0e8-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="9c0e8-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="9c0e8-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="9c0e8-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="9c0e8-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="9c0e8-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="9c0e8-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="9c0e8-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="9c0e8-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

