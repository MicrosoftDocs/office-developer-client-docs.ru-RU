---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Этот метод является устаревшим в Outlook Social Connector 2013.
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812755"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="2b689-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="2b689-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="2b689-104">Этот метод является устаревшим в Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="2b689-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="2b689-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="2b689-105">Remarks</span></span>

<span data-ttu-id="2b689-106">Запуск в Outlook Social Connector 2013, OSC поддерживает только по запросу синхронизации действий и кэширование не выполнено или синхронизации гибридного действий.</span><span class="sxs-lookup"><span data-stu-id="2b689-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="2b689-107">OSC игнорирует параметр **cacheActivities** в возможности XML и больше не вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="2b689-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="2b689-108">Для поддержки динамических действия подстановки, реализуйте метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="2b689-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="2b689-109">Установите **getActivities** и **dynamicActivitiesLookupEx** в качестве **значение true**, которое выводит запрос, OSC вместо этого вызов **ISocialSession2::GetActivitiesEx** .</span><span class="sxs-lookup"><span data-stu-id="2b689-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="2b689-110">Дополнительные сведения о как OSC получает друзей действий можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="2b689-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b689-111">См. также</span><span class="sxs-lookup"><span data-stu-id="2b689-111">See also</span></span>

- [<span data-ttu-id="2b689-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="2b689-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

