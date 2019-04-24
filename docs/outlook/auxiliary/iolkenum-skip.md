---
title: Иолкенумскип
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: ПроПускает указанное число учетных записей в перечислителе.
ms.openlocfilehash: d4063b0ff4852e6932cf50789eea3caa81d4d586
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321989"
---
# <a name="iolkenumskip"></a><span data-ttu-id="65438-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="65438-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="65438-104">ПроПускает указанное число учетных записей в перечислителе.</span><span class="sxs-lookup"><span data-stu-id="65438-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="65438-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="65438-105">Quick info</span></span>

<span data-ttu-id="65438-106">Обратитесь к разделу [иолкенум](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="65438-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="65438-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="65438-107">Parameters</span></span>

<span data-ttu-id="65438-108">_Кскип_</span><span class="sxs-lookup"><span data-stu-id="65438-108">_cSkip_</span></span>
  
> <span data-ttu-id="65438-109">возврата Количество пропущенных учетных записей.</span><span class="sxs-lookup"><span data-stu-id="65438-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="65438-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="65438-110">Return values</span></span>

<span data-ttu-id="65438-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="65438-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65438-112">См. также</span><span class="sxs-lookup"><span data-stu-id="65438-112">See also</span></span>

- [<span data-ttu-id="65438-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="65438-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="65438-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="65438-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="65438-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="65438-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

