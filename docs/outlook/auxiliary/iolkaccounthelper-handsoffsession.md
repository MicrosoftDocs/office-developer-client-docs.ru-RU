---
title: иолкаккаунселперхандсоффсессион
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: 'Освобождает объект сеанса MAPI, возвращенный функцией Иолкаккаунселпер:: Жетмаписессион.'
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418633"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="adcc4-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="adcc4-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="adcc4-104">Освобождает объект сеанса MAPI, возвращенный параметром – [иолкаккаунселпер:: жетмаписессион](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="adcc4-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="adcc4-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="adcc4-105">Quick info</span></span>

<span data-ttu-id="adcc4-106">Обратитесь к разделу [иолкаккаунселпер](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="adcc4-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="adcc4-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="adcc4-107">Return values</span></span>

|<span data-ttu-id="adcc4-108">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="adcc4-108">**HRESULT**</span></span>|<span data-ttu-id="adcc4-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="adcc4-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="adcc4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="adcc4-110">S_OK</span></span>  <br/> |<span data-ttu-id="adcc4-111">Если реализация **иолкаккаунселпер** создает свой собственный сеанс MAPI, который возвращается в **Иолкаккаунселпер:: жетмаписессион**, необходимо освободить сеанс здесь и возвратить S_OK.</span><span class="sxs-lookup"><span data-stu-id="adcc4-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="adcc4-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="adcc4-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="adcc4-113">Если в вашей реализации **иолкаккаунселпер** не был создан собственный сеанс MAPI, необходимо возвращать только E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="adcc4-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="adcc4-114">В этом случае поддерживается только возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="adcc4-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="adcc4-115">См. также</span><span class="sxs-lookup"><span data-stu-id="adcc4-115">See also</span></span>

- [<span data-ttu-id="adcc4-116">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="adcc4-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="adcc4-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="adcc4-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

