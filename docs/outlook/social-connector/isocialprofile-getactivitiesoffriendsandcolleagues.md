---
title: ИсоЦиалпрофилежетактивитиесоффриендсандколлеагуес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Этот метод не рекомендуется в Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285966"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="a8709-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="a8709-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="a8709-104">Этот метод не рекомендуется в Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="a8709-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="a8709-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="a8709-105">Remarks</span></span>

<span data-ttu-id="a8709-106">Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по запросу, а не кэшированную или гибридную синхронизацию действий.</span><span class="sxs-lookup"><span data-stu-id="a8709-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="a8709-107">OSC игнорирует параметр **качеактивитиес** в XML-коде возможностей и больше не вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="a8709-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="a8709-108">Для поддержки поиска динамических действий реализуйте метод [ISocialSession2:: жетактивитиесекс](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="a8709-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="a8709-109">Set \*\*\*\* динамикактивитиеслукупексs и \*\*\*\* AS **true**, что попросите OSC вызвать **ISocialSession2:: жетактивитиесекс** .</span><span class="sxs-lookup"><span data-stu-id="a8709-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="a8709-110">Дополнительные сведения о том, как OSC получает действия друзей, приведены в статье [Синхронизация друзей и действий](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="a8709-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8709-111">См. также</span><span class="sxs-lookup"><span data-stu-id="a8709-111">See also</span></span>

- [<span data-ttu-id="a8709-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="a8709-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

