---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Получает строку, представляющую коллекцию действий каждого из пользователей, указанных в параметре Хашедаддрессес.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404339"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="9b971-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="9b971-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="9b971-104">Получает строку, представляющую коллекцию действий каждого из пользователей, указанных в параметре _хашедаддрессес_ .</span><span class="sxs-lookup"><span data-stu-id="9b971-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="9b971-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b971-105">Parameters</span></span>

<span data-ttu-id="9b971-106">_хашедаддрессес_</span><span class="sxs-lookup"><span data-stu-id="9b971-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="9b971-107">возврата Структура, указывающая массив хэшированных SMTP-адресов для набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="9b971-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="9b971-108">_Начала_</span><span class="sxs-lookup"><span data-stu-id="9b971-108">_startTime_</span></span>
  
> <span data-ttu-id="9b971-109">возврата Время, после которого создаются действия, будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="9b971-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="9b971-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="9b971-110">_activities_</span></span>
  
> <span data-ttu-id="9b971-111">вышли Строка XML, представляющая набор действий пользователей, указанных в _хашедаддрессес_ в социальной сети с _начала_работы.</span><span class="sxs-lookup"><span data-stu-id="9b971-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b971-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b971-112">Remarks</span></span>

<span data-ttu-id="9b971-113">OSC вызывает **жетактивитиесекс** , если поставщик OSC поддерживает синхронизацию действий по требованию.</span><span class="sxs-lookup"><span data-stu-id="9b971-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="9b971-114">В файле OSC хранятся сведения, возвращенные _в памяти_ .</span><span class="sxs-lookup"><span data-stu-id="9b971-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="9b971-115">Для получения дополнительных сведений о том, как OSC использует и обновляет эти сведения в памяти, обратитесь к разделу [Синхронизация друзей и действий](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="9b971-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="9b971-116">Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по требованию и вызывает только **жетактивитиесекс** для получения действий.</span><span class="sxs-lookup"><span data-stu-id="9b971-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="9b971-117">Для поддержки поиска действий по запросу задайте для **качеактивитиес** **значение false** **, а для** динамикактивитиеслукупекс и **dynamicActivitiesLookupEx** **значение true**, а OSC вызывает **жетактивитиесекс**.</span><span class="sxs-lookup"><span data-stu-id="9b971-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="9b971-118">Возвращаемая строка XML должна соответствовать определению схемы для **activityFeed**, как определено в схеме Расширяемость поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9b971-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="9b971-119">_Хашедаддрессес_ сринг представляет набор хэшированных адресов для каждого пользователя, отображаемого в области "люди".</span><span class="sxs-lookup"><span data-stu-id="9b971-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="9b971-120">Хэшированные SMTP-адреса шифруются с помощью функции хеширования, указанной элементом **хашфунктион** в XML-файле **возможностей** поставщика.</span><span class="sxs-lookup"><span data-stu-id="9b971-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="9b971-121">Пользователь не должен быть дружественным для вошедшего в систему пользователя, представленного свойством [настроенный ISocialSession:: логжедонусернаме](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="9b971-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="9b971-122">Параметр _StartTime_ — это значение **даты** в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="9b971-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="9b971-123">Значения местного времени должны быть преобразованы в значения **даты** и времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="9b971-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="9b971-124">Действия, возвращаемые методом **жетактивитиесекс** , должны иметь значение времени создания, которое больше, чем _StartTime_ , и меньше или равно **сейчас**.</span><span class="sxs-lookup"><span data-stu-id="9b971-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="9b971-125">Если между **StartTime** и **Now**не произошло никаких изменений, поставщик должен возвратить ошибку OSC_E_NO_CHANGES.</span><span class="sxs-lookup"><span data-stu-id="9b971-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b971-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9b971-126">See also</span></span>

- [<span data-ttu-id="9b971-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b971-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="9b971-128">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="9b971-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

