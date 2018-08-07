---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Этот метод является устаревшим в версии 1.1 OSC.
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812738"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="90b72-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="90b72-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="90b72-104">Этот метод является устаревшим в версии 1.1 OSC.</span><span class="sxs-lookup"><span data-stu-id="90b72-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="90b72-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="90b72-105">Remarks</span></span>

<span data-ttu-id="90b72-106">Начиная с версии OSC 1.1, OSC больше не вызывает **GetActivities**.</span><span class="sxs-lookup"><span data-stu-id="90b72-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="90b72-107">OSC игнорирует значение **dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="90b72-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="90b72-108">Для поддержки динамических действия подстановки, реализуйте метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="90b72-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="90b72-109">Сделать **cacheActivities** **значение false**и **getActivities** и **dynamicActivitiesLookupEx** как **значение true**, которое выводит запрос, OSC вместо этого вызов **ISocialSession2::GetActivitiesEx** .</span><span class="sxs-lookup"><span data-stu-id="90b72-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90b72-110">См. также</span><span class="sxs-lookup"><span data-stu-id="90b72-110">See also</span></span>

- [<span data-ttu-id="90b72-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90b72-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

