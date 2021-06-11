---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Этот метод был обесценлен в Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406894"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="f9256-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="f9256-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="f9256-104">Этот метод был обесценлен в Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="f9256-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="f9256-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="f9256-105">Remarks</span></span>

<span data-ttu-id="f9256-106">Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по запросу, а не кэширование или гибридную синхронизацию действий.</span><span class="sxs-lookup"><span data-stu-id="f9256-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="f9256-107">OsC игнорирует параметр **cacheActivities** в XML-возможностях и больше не вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="f9256-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="f9256-108">Чтобы поддерживать динамические действия, реализуем [метод ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md)</span><span class="sxs-lookup"><span data-stu-id="f9256-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="f9256-109">Установите **getActivities** и **dynamicActivitiesLookupEx** как истинные, что будет побуждать OSC вызывать **ISocialSession2::GetActivitiesEx** вместо этого.</span><span class="sxs-lookup"><span data-stu-id="f9256-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="f9256-110">Дополнительные сведения о том, как OSC получает действия друзей, см. в [интернете.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="f9256-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f9256-111">См. также</span><span class="sxs-lookup"><span data-stu-id="f9256-111">See also</span></span>

- [<span data-ttu-id="f9256-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="f9256-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

