---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Освободит память, выделенную интерфейсом IOlkAccountManager.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408490"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="f7b41-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="f7b41-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="f7b41-104">Освободит память, выделенную [интерфейсом IOlkAccountManager.](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="f7b41-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f7b41-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f7b41-105">Quick info</span></span>

<span data-ttu-id="f7b41-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f7b41-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="f7b41-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f7b41-107">Parameters</span></span>

<span data-ttu-id="f7b41-108">_pv_</span><span class="sxs-lookup"><span data-stu-id="f7b41-108">_pv_</span></span>
  
> <span data-ttu-id="f7b41-109">[in] Указатель на память, чтобы освободить.</span><span class="sxs-lookup"><span data-stu-id="f7b41-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f7b41-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f7b41-110">Return values</span></span>

<span data-ttu-id="f7b41-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="f7b41-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7b41-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7b41-112">Remarks</span></span>

<span data-ttu-id="f7b41-113">Используйте этот метод для выпуска памяти, выделенной [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span><span class="sxs-lookup"><span data-stu-id="f7b41-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7b41-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f7b41-114">See also</span></span>

- [<span data-ttu-id="f7b41-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="f7b41-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

