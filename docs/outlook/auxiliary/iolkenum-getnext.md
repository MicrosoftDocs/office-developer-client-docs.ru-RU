---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Получает перечислитель следующего учетной записи.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807884"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="d6cdf-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="d6cdf-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="d6cdf-104">Получает перечислитель следующего учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d6cdf-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d6cdf-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d6cdf-105">Quick info</span></span>

<span data-ttu-id="d6cdf-106">В разделе [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="d6cdf-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="d6cdf-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6cdf-107">Parameters</span></span>

<span data-ttu-id="d6cdf-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="d6cdf-108">_ppunk_</span></span>
  
> <span data-ttu-id="d6cdf-109">[in] Указатель на интерфейс **IUnknown** , клиента запроса можно получить интерфейс [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="d6cdf-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d6cdf-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d6cdf-110">Return values</span></span>

|<span data-ttu-id="d6cdf-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6cdf-111">**HRESULT**</span></span>|<span data-ttu-id="d6cdf-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="d6cdf-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d6cdf-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d6cdf-113">S_OK</span></span>  <br/> |<span data-ttu-id="d6cdf-114">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="d6cdf-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="d6cdf-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d6cdf-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="d6cdf-116">Перечислитель достигнут конец.</span><span class="sxs-lookup"><span data-stu-id="d6cdf-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6cdf-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="d6cdf-117">Remarks</span></span>

<span data-ttu-id="d6cdf-118">Интерфейс, указанный *ppunk* наследует от **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="d6cdf-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="d6cdf-119">Клиент запроса этот интерфейс (с помощью **IUnknown::QueryInterface**) можно получить указатель на интерфейс **IOlkAccount** и получить или задать сведения для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d6cdf-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6cdf-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d6cdf-120">See also</span></span>

- [<span data-ttu-id="d6cdf-121">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="d6cdf-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="d6cdf-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="d6cdf-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="d6cdf-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="d6cdf-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="d6cdf-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="d6cdf-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

