---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Получает строку, представляюную коллекцию действий каждого из пользователей, указанных с помощью параметра hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404339"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="cb0fe-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="cb0fe-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="cb0fe-104">Получает строку, представляюную коллекцию действий каждого из пользователей, указанных с помощью параметра _hashedAddresses._</span><span class="sxs-lookup"><span data-stu-id="cb0fe-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="cb0fe-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb0fe-105">Parameters</span></span>

<span data-ttu-id="cb0fe-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="cb0fe-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="cb0fe-107">[in] Структура, которая определяет массив адресов SMTP с hashed для набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="cb0fe-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="cb0fe-108">_startTime_</span></span>
  
> <span data-ttu-id="cb0fe-109">[in] Время, после которого будут возвращены созданные действия.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="cb0fe-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="cb0fe-110">_activities_</span></span>
  
> <span data-ttu-id="cb0fe-111">[out] Строка XML, которая представляет набор действий пользователей, указанных с помощью _hashedAddresses_ в социальной сети, начиная _с startTime._</span><span class="sxs-lookup"><span data-stu-id="cb0fe-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb0fe-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb0fe-112">Remarks</span></span>

<span data-ttu-id="cb0fe-113">OsC вызывает **GetActivitiesEx,** если поставщик OSC поддерживает синхронизацию действий по требованию.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="cb0fe-114">OsC сохраняет сведения, возвращаемую в  _действиях,_ в памяти.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="cb0fe-115">Дополнительные сведения о том, как OSC использует и обновляет эти сведения в памяти, см. в подсети "Синхронизация друзей [и действий".](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="cb0fe-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="cb0fe-116">Начиная с Outlook Social Connector 2013, OSC поддерживает только синхронизацию действий по требованию и вызывает **только GetActivitiesEx** для получения действий.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="cb0fe-117">Чтобы поддерживать подыскать действия по запросу, установите **для cacheActivities** как **false** и **getActivities** и **dynamicActivitiesLookupEx** как **true,** и OSC будет вызывать **GetActivitiesEx**.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="cb0fe-118">Возвращенная строка XML должна соответствовать определению схемы для **activityFeed,** как определено в схеме для возможности extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="cb0fe-119">_Сррес hashedAddresses_ представляет собой набор адресов с hashed для каждого пользователя, отображаемого в области "Люди".</span><span class="sxs-lookup"><span data-stu-id="cb0fe-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="cb0fe-120">Hashed SMTP-адреса шифруются с помощью функции hashing, указанной элементом **hashFunction** в **XML** возможностей поставщика.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="cb0fe-121">Пользователь не должен быть другом во время входа пользователя, представленного свойством [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md)</span><span class="sxs-lookup"><span data-stu-id="cb0fe-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="cb0fe-122">Параметр  _startTime_ — это значение **Date** в UTC.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cb0fe-123">Значения местного времени должны быть преобразованы в значения **даты** в UTC.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="cb0fe-124">Действия, возвращаемые методом **GetActivitiesEx,** должны иметь значение времени создания, которое больше _значения startTime_ и меньше или равно **Now.**</span><span class="sxs-lookup"><span data-stu-id="cb0fe-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="cb0fe-125">Если между **startTime** и **Now** не произошло никаких изменений, поставщик должен вернуть OSC_E_NO_CHANGES ошибку.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb0fe-126">См. также</span><span class="sxs-lookup"><span data-stu-id="cb0fe-126">See also</span></span>

- [<span data-ttu-id="cb0fe-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb0fe-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="cb0fe-128">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="cb0fe-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

