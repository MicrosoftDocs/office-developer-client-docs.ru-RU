---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Этот метод больше не используется в Outlook Social Connector 2013.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437744"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="e54a1-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="e54a1-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="e54a1-104">Этот метод больше не используется в Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="e54a1-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="e54a1-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e54a1-105">Remarks</span></span>

<span data-ttu-id="e54a1-106">Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по требованию, а не кэширование или гибридную синхронизацию действий.</span><span class="sxs-lookup"><span data-stu-id="e54a1-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="e54a1-107">OSC игнорирует параметр **cacheActivities** в XML возможностей и не вызывать этот метод.</span><span class="sxs-lookup"><span data-stu-id="e54a1-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="e54a1-108">Чтобы поддерживать динамический подыском действий, реализуем метод [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md)</span><span class="sxs-lookup"><span data-stu-id="e54a1-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="e54a1-109">Установите **для cacheActivities** как **false,** **getActivities** и **dynamicActivitiesLookupEx** как **true,** что позволит OSC вызвать **ISocialSession2::GetActivitiesEx** вместо этого.</span><span class="sxs-lookup"><span data-stu-id="e54a1-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="e54a1-110">Дополнительные сведения о том, как OSC получает действия друзей, см. в [подсети "Синхронизация друзей и действий".](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="e54a1-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e54a1-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e54a1-111">See also</span></span>

- [<span data-ttu-id="e54a1-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e54a1-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

