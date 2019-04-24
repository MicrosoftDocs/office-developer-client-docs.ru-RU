---
title: ИсоЦиалперсонжетактивитиес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Этот метод не рекомендуется в Outlook Social Connector 2013.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286166"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="b05a8-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="b05a8-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="b05a8-104">Этот метод не рекомендуется в Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="b05a8-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="b05a8-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b05a8-105">Remarks</span></span>

<span data-ttu-id="b05a8-106">Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по запросу, а не кэшированную или гибридную синхронизацию действий.</span><span class="sxs-lookup"><span data-stu-id="b05a8-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="b05a8-107">OSC игнорирует параметр **качеактивитиес** в XML-коде возможностей и не вызывает этот метод.</span><span class="sxs-lookup"><span data-stu-id="b05a8-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="b05a8-108">Для поддержки поиска динамических действий реализуйте метод [ISocialSession2:: жетактивитиесекс](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="b05a8-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="b05a8-109">Задайте **для качеактивитиес** **значение false**, динамикактивитиеслукупекс и \*\*\*\* как **true**, после чего OSC будет вызывать **ISocialSession2:: жетактивитиесекс** . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b05a8-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="b05a8-110">Дополнительные сведения о том, как OSC получает действия друзей, приведены в статье [Синхронизация друзей и действий](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="b05a8-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b05a8-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b05a8-111">See also</span></span>

- [<span data-ttu-id="b05a8-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b05a8-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

