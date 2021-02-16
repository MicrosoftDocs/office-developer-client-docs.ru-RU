---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Этот метод больше не используется в OSC 1.1.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439298"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="f843b-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="f843b-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="f843b-104">Этот метод больше не используется в OSC 1.1.</span><span class="sxs-lookup"><span data-stu-id="f843b-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="f843b-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="f843b-105">Remarks</span></span>

<span data-ttu-id="f843b-106">Начиная с OSC 1.1, OSC больше не вызывает **GetActivities.**</span><span class="sxs-lookup"><span data-stu-id="f843b-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="f843b-107">OSC игнорирует значение **dynamicActivitiesLookup.**</span><span class="sxs-lookup"><span data-stu-id="f843b-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="f843b-108">Чтобы поддерживать динамический подыском действий, реализуем метод [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md)</span><span class="sxs-lookup"><span data-stu-id="f843b-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="f843b-109">Установите **для cacheActivities** как **false** и **getActivities** и **dynamicActivitiesLookupEx** как **true,** что позволит OSC вызвать **ISocialSession2::GetActivitiesEx** вместо этого.</span><span class="sxs-lookup"><span data-stu-id="f843b-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f843b-110">См. также</span><span class="sxs-lookup"><span data-stu-id="f843b-110">See also</span></span>

- [<span data-ttu-id="f843b-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f843b-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

