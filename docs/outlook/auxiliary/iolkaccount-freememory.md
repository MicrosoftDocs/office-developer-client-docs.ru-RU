---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Освободит память, выделенную интерфейсом IOlkAccount.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406201"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="ca28e-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="ca28e-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="ca28e-104">Освободит память, выделенную [интерфейсом IOlkAccount.](iolkaccount.md)</span><span class="sxs-lookup"><span data-stu-id="ca28e-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ca28e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ca28e-105">Quick info</span></span>

<span data-ttu-id="ca28e-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ca28e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="ca28e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="ca28e-107">Parameters</span></span>

<span data-ttu-id="ca28e-108">_pv_</span><span class="sxs-lookup"><span data-stu-id="ca28e-108">_pv_</span></span>
  
> <span data-ttu-id="ca28e-109">[in] Указатель на память, который необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="ca28e-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ca28e-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ca28e-110">Return values</span></span>

<span data-ttu-id="ca28e-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="ca28e-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca28e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca28e-112">Remarks</span></span>

<span data-ttu-id="ca28e-113">Используйте этот метод для бесплатной памяти, выделенной [IOlkAccount::GetProp](iolkaccount-getprop.md) (если значение указанного свойства учетной записи двоично или строкового типа) и [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ca28e-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca28e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ca28e-114">See also</span></span>

- [<span data-ttu-id="ca28e-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ca28e-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="ca28e-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="ca28e-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

