---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Выпускает объект сеанса MAPI, возвращенный IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418633"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="2edca-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="2edca-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="2edca-104">Выпускает объект сеанса MAPI, который был возвращен - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="2edca-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2edca-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="2edca-105">Quick info</span></span>

<span data-ttu-id="2edca-106">См. [iOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="2edca-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="2edca-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2edca-107">Return values</span></span>

|<span data-ttu-id="2edca-108">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2edca-108">**HRESULT**</span></span>|<span data-ttu-id="2edca-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="2edca-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2edca-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2edca-110">S_OK</span></span>  <br/> |<span data-ttu-id="2edca-111">Если при реализации **IOlkAccountHelper** создается собственный сеанс MAPI, который возвращается в **IOlkAccountHelper::GetMapiSession,** необходимо освободить сеанс здесь и вернуться S_OK.</span><span class="sxs-lookup"><span data-stu-id="2edca-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="2edca-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="2edca-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="2edca-113">Если реализация **IOlkAccountHelper** не создает собственную сессию MAPI, необходимо возвращать только E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="2edca-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="2edca-114">В этом случае это единственное поддерживаемые значения возврата.</span><span class="sxs-lookup"><span data-stu-id="2edca-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2edca-115">См. также</span><span class="sxs-lookup"><span data-stu-id="2edca-115">See also</span></span>

- [<span data-ttu-id="2edca-116">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="2edca-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="2edca-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="2edca-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

