---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Получает строку, представляюную коллекцию действий каждого из пользователей, указанных параметром hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404339"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="d2432-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="d2432-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="d2432-104">Получает строку, представляюную коллекцию действий каждого из пользователей, указанных _параметром hashedAddresses._</span><span class="sxs-lookup"><span data-stu-id="d2432-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="d2432-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="d2432-105">Parameters</span></span>

<span data-ttu-id="d2432-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="d2432-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="d2432-107">[in] Структура, которая указывает массив адресов SMTP с hashed для набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="d2432-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="d2432-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="d2432-108">_startTime_</span></span>
  
> <span data-ttu-id="d2432-109">[in] Время, после которого будут возвращены созданные действия.</span><span class="sxs-lookup"><span data-stu-id="d2432-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="d2432-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="d2432-110">_activities_</span></span>
  
> <span data-ttu-id="d2432-111">[вышел] Строка XML, которая представляет набор действий пользователей, заданный _hashedAddresses_ в социальной сети со _времен startTime._</span><span class="sxs-lookup"><span data-stu-id="d2432-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2432-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2432-112">Remarks</span></span>

<span data-ttu-id="d2432-113">OsC вызывает **GetActivitiesEx,** если поставщик OSC поддерживает синхронизацию действий по запросу.</span><span class="sxs-lookup"><span data-stu-id="d2432-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="d2432-114">OsC хранит сведения, возвращаемые в  _действиях_ в памяти.</span><span class="sxs-lookup"><span data-stu-id="d2432-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="d2432-115">Дополнительные сведения о том, как OSC использует и [](synchronizing-friends-and-activities.md)обновляет эти сведения в памяти, см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="d2432-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="d2432-116">Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по запросу и вызывает только **GetActivitiesEx** для получения действий.</span><span class="sxs-lookup"><span data-stu-id="d2432-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="d2432-117">Чтобы поддерживать просмотр действий по запросу, установите **кэшАктивы** как ложные, а **getActivities** и **dynamicActivitiesLookupEx** — как истинные, и OSC будет вызывать **GetActivitiesEx.**</span><span class="sxs-lookup"><span data-stu-id="d2432-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="d2432-118">Возвращенная строка XML должна соответствовать определению схемы для **activityFeed,** как определено в схеме для extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="d2432-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="d2432-119">Сринг  _hashedAddresses_ представляет набор адресов с hashed для каждого пользователя, отображаемого в области people.</span><span class="sxs-lookup"><span data-stu-id="d2432-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="d2432-120">С помощью функции хашинга, указанной элементом **hashFunction** в XML-возможностях поставщика, шифруются ip-адреса **SMTP.**</span><span class="sxs-lookup"><span data-stu-id="d2432-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="d2432-121">Пользователю не нужно быть другом зарегистрированного пользователя, представленного свойством [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md)</span><span class="sxs-lookup"><span data-stu-id="d2432-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="d2432-122">Параметр  _startTime_ — это значение **Date** в скоординированном универсальном времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="d2432-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d2432-123">Значения местного времени должны быть преобразованы в значения даты **UTC.**</span><span class="sxs-lookup"><span data-stu-id="d2432-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="d2432-124">Действия, возвращаемые методом **GetActivitiesEx,** должны иметь значение времени создания, которое превышает _значение startTime_ и меньше или меньше, чем **сейчас.**</span><span class="sxs-lookup"><span data-stu-id="d2432-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="d2432-125">Если между **startTime** и **Now** не произошло никаких изменений, поставщик должен вернуть OSC_E_NO_CHANGES ошибку.</span><span class="sxs-lookup"><span data-stu-id="d2432-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2432-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d2432-126">See also</span></span>

- [<span data-ttu-id="d2432-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2432-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="d2432-128">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="d2432-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

