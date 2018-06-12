---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Освобождает объект сеанса MAPI, возвращаемые IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807835"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="a0db5-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="a0db5-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="a0db5-104">Освобождает объект сеанса MAPI, возвращаемые - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="a0db5-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a0db5-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="a0db5-105">Quick info</span></span>

<span data-ttu-id="a0db5-106">В разделе [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="a0db5-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="a0db5-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a0db5-107">Return values</span></span>

|<span data-ttu-id="a0db5-108">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a0db5-108">**HRESULT**</span></span>|<span data-ttu-id="a0db5-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="a0db5-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0db5-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a0db5-110">S_OK</span></span>  <br/> |<span data-ttu-id="a0db5-111">Если реализация **IOlkAccountHelper** создает собственный сеанса MAPI, который возвращается в **IOlkAccountHelper::GetMapiSession**, необходимо освобождать этого сеанса и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="a0db5-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="a0db5-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="a0db5-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="a0db5-113">Если реализация **IOlkAccountHelper** не была создана сеанса MAPI, должен возвращать только значение E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a0db5-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="a0db5-114">В этом случае это поддерживается только возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="a0db5-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0db5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a0db5-115">See also</span></span>

- [<span data-ttu-id="a0db5-116">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="a0db5-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="a0db5-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="a0db5-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

