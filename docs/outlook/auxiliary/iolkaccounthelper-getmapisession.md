---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Открытие сеанса MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392605"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="ef121-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="ef121-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="ef121-104">Открытие сеанса MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.</span><span class="sxs-lookup"><span data-stu-id="ef121-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ef121-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ef121-105">Quick info</span></span>

<span data-ttu-id="ef121-106">В разделе [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="ef121-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="ef121-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef121-107">Parameters</span></span>

<span data-ttu-id="ef121-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="ef121-108">_ppmsess_</span></span>
  
> <span data-ttu-id="ef121-109">[out] Текущий сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="ef121-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ef121-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ef121-110">Return values</span></span>

<span data-ttu-id="ef121-111">S_OK if the call succeeded; otherwise, an error code.</span><span class="sxs-lookup"><span data-stu-id="ef121-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef121-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="ef121-112">Remarks</span></span>

<span data-ttu-id="ef121-113">Из-за проблем с циклические ссылки диспетчер учетных записей самого не может поддерживать ссылку для сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="ef121-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef121-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ef121-114">See also</span></span>

- [<span data-ttu-id="ef121-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="ef121-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="ef121-116">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef121-116">IMAPISession : IUnknown</span></span>](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

