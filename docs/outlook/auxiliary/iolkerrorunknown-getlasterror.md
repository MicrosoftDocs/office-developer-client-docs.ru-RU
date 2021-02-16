---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Получает строку сообщения для указанной ошибки.
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431703"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="a87d4-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a87d4-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="a87d4-104">Получает строку сообщения для указанной ошибки.</span><span class="sxs-lookup"><span data-stu-id="a87d4-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a87d4-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a87d4-105">Quick info</span></span>

<span data-ttu-id="a87d4-106">См. [IOlkErrorUnknown.](iolkerrorunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a87d4-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="a87d4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a87d4-107">Parameters</span></span>

<span data-ttu-id="a87d4-108">_hr_</span><span class="sxs-lookup"><span data-stu-id="a87d4-108">_hr_</span></span>
  
> <span data-ttu-id="a87d4-109">[in] Код ошибки, который необходимо найти.</span><span class="sxs-lookup"><span data-stu-id="a87d4-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="a87d4-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="a87d4-110">_ppwszError_</span></span>
  
> <span data-ttu-id="a87d4-111">[out] Сообщение об ошибке, соответствующее  *hr*  .</span><span class="sxs-lookup"><span data-stu-id="a87d4-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a87d4-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a87d4-112">Return values</span></span>

|<span data-ttu-id="a87d4-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a87d4-113">**HRESULT**</span></span>|<span data-ttu-id="a87d4-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="a87d4-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a87d4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a87d4-115">S_OK</span></span>  <br/> |<span data-ttu-id="a87d4-116">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="a87d4-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="a87d4-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a87d4-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="a87d4-118">Один или несколько аргументов недопустимы.</span><span class="sxs-lookup"><span data-stu-id="a87d4-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a87d4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a87d4-119">See also</span></span>

- [<span data-ttu-id="a87d4-120">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="a87d4-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

