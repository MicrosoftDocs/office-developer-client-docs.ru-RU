---
title: Иолкаккаунтфримемори
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Освобождает память, выделенную интерфейсом Иолкаккаунт.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321338"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="71f22-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="71f22-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="71f22-104">Освобождает память, выделенную интерфейсом [иолкаккаунт](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="71f22-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="71f22-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="71f22-105">Quick info</span></span>

<span data-ttu-id="71f22-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="71f22-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="71f22-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="71f22-107">Parameters</span></span>

<span data-ttu-id="71f22-108">_плата_</span><span class="sxs-lookup"><span data-stu-id="71f22-108">_pv_</span></span>
  
> <span data-ttu-id="71f22-109">возврата Указатель на память, которую необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="71f22-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="71f22-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="71f22-110">Return values</span></span>

<span data-ttu-id="71f22-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="71f22-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="71f22-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="71f22-112">Remarks</span></span>

<span data-ttu-id="71f22-113">Используйте этот метод для освобождения памяти, выделенной [иолкаккаунт::-Prop](iolkaccount-getprop.md) (если значение указанного свойства учетной записи является двоичным или строковым типом), и [Иолкаккаунт:: жетаккаунтинфо](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="71f22-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="71f22-114">См. также</span><span class="sxs-lookup"><span data-stu-id="71f22-114">See also</span></span>

- [<span data-ttu-id="71f22-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="71f22-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="71f22-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="71f22-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

