---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Освобождает память, выделенную с помощью интерфейса IOlkAccount.
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807785"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="94060-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="94060-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="94060-104">Освобождает память, выделенную с помощью интерфейса [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="94060-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="94060-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="94060-105">Quick info</span></span>

<span data-ttu-id="94060-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="94060-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="94060-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="94060-107">Parameters</span></span>

<span data-ttu-id="94060-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="94060-108">_pv_</span></span>
  
> <span data-ttu-id="94060-109">[in] Указатель на память освобождения.</span><span class="sxs-lookup"><span data-stu-id="94060-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="94060-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="94060-110">Return values</span></span>

<span data-ttu-id="94060-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="94060-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94060-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="94060-112">Remarks</span></span>

<span data-ttu-id="94060-113">Используйте этот метод для освобождения памяти, выделенной с [IOlkAccount::GetProp](iolkaccount-getprop.md) (если значение свойства указанную учетную запись типа двоичный или строки) и [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="94060-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94060-114">См. также</span><span class="sxs-lookup"><span data-stu-id="94060-114">See also</span></span>

- [<span data-ttu-id="94060-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="94060-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="94060-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="94060-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

