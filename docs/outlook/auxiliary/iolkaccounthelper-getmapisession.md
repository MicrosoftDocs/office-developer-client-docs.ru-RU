---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Открытие сеанса MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.
ms.openlocfilehash: 50809a00d13fd9f2a93bebc2961a134b3625e82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807860"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="d2582-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="d2582-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="d2582-104">Открытие сеанса MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.</span><span class="sxs-lookup"><span data-stu-id="d2582-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d2582-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d2582-105">Quick info</span></span>

<span data-ttu-id="d2582-106">В разделе [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="d2582-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="d2582-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2582-107">Parameters</span></span>

<span data-ttu-id="d2582-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="d2582-108">_ppmsess_</span></span>
  
> <span data-ttu-id="d2582-109">[out] Текущий сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="d2582-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d2582-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d2582-110">Return values</span></span>

<span data-ttu-id="d2582-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="d2582-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2582-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="d2582-112">Remarks</span></span>

<span data-ttu-id="d2582-113">Из-за проблем с циклические ссылки диспетчер учетных записей самого не может поддерживать ссылку для сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="d2582-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2582-114">См. также</span><span class="sxs-lookup"><span data-stu-id="d2582-114">See also</span></span>

- [<span data-ttu-id="d2582-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="d2582-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="d2582-116">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2582-116">IMAPISession : IUnknown</span></span>](http://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

