---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Получает интерфейс ISocialPerson на основе параметра идентификатор пользователя.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812739"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="94a60-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="94a60-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="94a60-104">Получает интерфейс [ISocialPerson](isocialpersoniunknown.md) на основе параметра _идентификатор пользователя_ .</span><span class="sxs-lookup"><span data-stu-id="94a60-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="94a60-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="94a60-105">Parameters</span></span>

<span data-ttu-id="94a60-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="94a60-106">_userId_</span></span>
  
> <span data-ttu-id="94a60-107">[in] Строка, содержащая пользователя ID или адрес SMTP пользователя.</span><span class="sxs-lookup"><span data-stu-id="94a60-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="94a60-108">_результат_</span><span class="sxs-lookup"><span data-stu-id="94a60-108">_result_</span></span>
  
> <span data-ttu-id="94a60-109">[out] Интерфейс **ISocialPerson** .</span><span class="sxs-lookup"><span data-stu-id="94a60-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="94a60-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="94a60-110">Remarks</span></span>

<span data-ttu-id="94a60-111">Параметр _идентификатор пользователя_ должен быть адрес SMTP или идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="94a60-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94a60-112">См. также</span><span class="sxs-lookup"><span data-stu-id="94a60-112">See also</span></span>

- [<span data-ttu-id="94a60-113">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94a60-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

