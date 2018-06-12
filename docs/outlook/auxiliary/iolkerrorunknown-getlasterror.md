---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Получает строку сообщения для заданной ошибки.
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807874"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="68982-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="68982-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="68982-104">Получает строку сообщения для заданной ошибки.</span><span class="sxs-lookup"><span data-stu-id="68982-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="68982-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="68982-105">Quick info</span></span>

<span data-ttu-id="68982-106">В разделе [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="68982-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="68982-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="68982-107">Parameters</span></span>

<span data-ttu-id="68982-108">_управления персоналом_</span><span class="sxs-lookup"><span data-stu-id="68982-108">_hr_</span></span>
  
> <span data-ttu-id="68982-109">[in] Код ошибки для поиска.</span><span class="sxs-lookup"><span data-stu-id="68982-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="68982-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="68982-110">_ppwszError_</span></span>
  
> <span data-ttu-id="68982-111">[out] Сообщение об ошибке, соответствующее для *отдела кадров* .</span><span class="sxs-lookup"><span data-stu-id="68982-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="68982-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="68982-112">Return values</span></span>

|<span data-ttu-id="68982-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="68982-113">**HRESULT**</span></span>|<span data-ttu-id="68982-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="68982-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68982-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="68982-115">S_OK</span></span>  <br/> |<span data-ttu-id="68982-116">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="68982-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="68982-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="68982-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="68982-118">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="68982-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68982-119">См. также</span><span class="sxs-lookup"><span data-stu-id="68982-119">See also</span></span>

- [<span data-ttu-id="68982-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="68982-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

