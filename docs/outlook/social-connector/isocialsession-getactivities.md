---
title: ИсоЦиалсессионжетактивитиес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Этот метод не рекомендуется использовать в OSC 1,1.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285457"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="b733f-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="b733f-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="b733f-104">Этот метод не рекомендуется использовать в OSC 1,1.</span><span class="sxs-lookup"><span data-stu-id="b733f-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="b733f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b733f-105">Remarks</span></span>

<span data-ttu-id="b733f-106">Начиная с OSC 1,1, OSC больше не вызывает **операции**с операциями.</span><span class="sxs-lookup"><span data-stu-id="b733f-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="b733f-107">OSC игнорирует значение параметра **динамикактивитиеслукуп**.</span><span class="sxs-lookup"><span data-stu-id="b733f-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="b733f-108">Для поддержки поиска динамических действий реализуйте метод [ISocialSession2:: жетактивитиесекс](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="b733f-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="b733f-109">Задайте для параметра **качеактивитиес** **значение false**, а для **динамикактивитиеслукупекс** — **значение true**, после чего OSC будет вызывать **ISocialSession2:: жетактивитиесекс** . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b733f-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b733f-110">См. также</span><span class="sxs-lookup"><span data-stu-id="b733f-110">See also</span></span>

- [<span data-ttu-id="b733f-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b733f-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

