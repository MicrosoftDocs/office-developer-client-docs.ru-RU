---
title: иолкаккаунтманажерфримемори
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Освобождает память, выделенную интерфейсом Иолкаккаунтманажер.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408490"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="f970e-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="f970e-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="f970e-104">Освобождает память, выделенную интерфейсом [иолкаккаунтманажер](iolkaccountmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="f970e-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f970e-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f970e-105">Quick info</span></span>

<span data-ttu-id="f970e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f970e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="f970e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f970e-107">Parameters</span></span>

<span data-ttu-id="f970e-108">_плата_</span><span class="sxs-lookup"><span data-stu-id="f970e-108">_pv_</span></span>
  
> <span data-ttu-id="f970e-109">возврата Указатель на память, которую требуется освободить.</span><span class="sxs-lookup"><span data-stu-id="f970e-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f970e-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f970e-110">Return values</span></span>

<span data-ttu-id="f970e-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="f970e-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f970e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f970e-112">Remarks</span></span>

<span data-ttu-id="f970e-113">Этот метод используется для освобождения памяти, выделенной [иолкаккаунтманажер::.](iolkaccountmanager-getorder.md)</span><span class="sxs-lookup"><span data-stu-id="f970e-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f970e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f970e-114">See also</span></span>

- [<span data-ttu-id="f970e-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="f970e-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

