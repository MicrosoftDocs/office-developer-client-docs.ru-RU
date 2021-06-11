---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Получает интерфейс ISocialPerson на основе параметра userID.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439823"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="16936-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="16936-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="16936-104">Получает интерфейс [ISocialPerson](isocialpersoniunknown.md) на основе _параметра userID._</span><span class="sxs-lookup"><span data-stu-id="16936-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="16936-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="16936-105">Parameters</span></span>

<span data-ttu-id="16936-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="16936-106">_userId_</span></span>
  
> <span data-ttu-id="16936-107">[in] Строка, которая содержит пользовательский ID или SMTP-адрес пользователя.</span><span class="sxs-lookup"><span data-stu-id="16936-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="16936-108">_result_</span><span class="sxs-lookup"><span data-stu-id="16936-108">_result_</span></span>
  
> <span data-ttu-id="16936-109">[вышел] Интерфейс **ISocialPerson.**</span><span class="sxs-lookup"><span data-stu-id="16936-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="16936-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="16936-110">Remarks</span></span>

<span data-ttu-id="16936-111">Параметр  _userID_ должен быть пользовательским ИД или SMTP-адресом.</span><span class="sxs-lookup"><span data-stu-id="16936-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16936-112">См. также</span><span class="sxs-lookup"><span data-stu-id="16936-112">See also</span></span>

- [<span data-ttu-id="16936-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16936-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

