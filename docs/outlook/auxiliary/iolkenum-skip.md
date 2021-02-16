---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Пропускает указанное количество учетных записей в enumerator.
ms.openlocfilehash: d4063b0ff4852e6932cf50789eea3caa81d4d586
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404780"
---
# <a name="iolkenumskip"></a><span data-ttu-id="9d454-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="9d454-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="9d454-104">Пропускает указанное количество учетных записей в enumerator.</span><span class="sxs-lookup"><span data-stu-id="9d454-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9d454-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="9d454-105">Quick info</span></span>

<span data-ttu-id="9d454-106">См. [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="9d454-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="9d454-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d454-107">Parameters</span></span>

<span data-ttu-id="9d454-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="9d454-108">_cSkip_</span></span>
  
> <span data-ttu-id="9d454-109">[in] Количество учетных записей, которые необходимо пропустить.</span><span class="sxs-lookup"><span data-stu-id="9d454-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9d454-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9d454-110">Return values</span></span>

<span data-ttu-id="9d454-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="9d454-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d454-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9d454-112">See also</span></span>

- [<span data-ttu-id="9d454-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="9d454-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="9d454-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="9d454-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="9d454-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="9d454-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

