---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Этот метод является устаревшим в Outlook Social Connector 2013.
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812717"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="7b41c-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="7b41c-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="7b41c-104">Этот метод является устаревшим в Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="7b41c-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="7b41c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b41c-105">Remarks</span></span>

<span data-ttu-id="7b41c-106">Запуск в Outlook Social Connector 2013, OSC поддерживает только по запросу синхронизации действий и кэширование не выполнено или синхронизации гибридного действий.</span><span class="sxs-lookup"><span data-stu-id="7b41c-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="7b41c-107">OSC игнорирует параметр **cacheActivities** в возможности XML и не вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="7b41c-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="7b41c-108">Для поддержки динамических действия подстановки, реализуйте метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="7b41c-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="7b41c-109">Сделать **cacheActivities** **значение false**, **getActivities** и **dynamicActivitiesLookupEx** как **значение true**, которое выводит запрос, OSC вместо этого вызов **ISocialSession2::GetActivitiesEx** .</span><span class="sxs-lookup"><span data-stu-id="7b41c-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="7b41c-110">Дополнительные сведения о как OSC получает друзей действий можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="7b41c-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7b41c-111">См. также</span><span class="sxs-lookup"><span data-stu-id="7b41c-111">See also</span></span>

- [<span data-ttu-id="7b41c-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7b41c-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

