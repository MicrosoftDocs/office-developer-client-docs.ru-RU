---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Получает строку, представляющую набор операций каждого из пользователей, указанных в параметре hashedAddresses.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812752"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="36ad1-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="36ad1-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="36ad1-104">Получает строку, представляющую набор операций каждого из пользователей, указанных в параметре _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="36ad1-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="36ad1-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="36ad1-105">Parameters</span></span>

<span data-ttu-id="36ad1-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="36ad1-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="36ad1-107">[in] Структура, указывает массив хэш SMTP адресов для группы пользователей.</span><span class="sxs-lookup"><span data-stu-id="36ad1-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="36ad1-108">_время начала_</span><span class="sxs-lookup"><span data-stu-id="36ad1-108">_startTime_</span></span>
  
> <span data-ttu-id="36ad1-109">[in] Время, после которого будет возвращено действия, которые создаются.</span><span class="sxs-lookup"><span data-stu-id="36ad1-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="36ad1-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="36ad1-110">_activities_</span></span>
  
> <span data-ttu-id="36ad1-111">[out] XML-строка, представляющая набор действий пользователей, указанных в _hashedAddresses_ в социальных сетях с момента _времени начала_.</span><span class="sxs-lookup"><span data-stu-id="36ad1-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36ad1-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="36ad1-112">Remarks</span></span>

<span data-ttu-id="36ad1-113">OSC вызывает **GetActivitiesEx** , если поставщик OSC поддерживает синхронизацию по требованию действий.</span><span class="sxs-lookup"><span data-stu-id="36ad1-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="36ad1-114">OSC хранит сведения, возвращаемые в _действий_ в памяти.</span><span class="sxs-lookup"><span data-stu-id="36ad1-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="36ad1-115">Дополнительные сведения о использует OSC и обновляет эти сведения в памяти можно [Синхронизация друзей и действия](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="36ad1-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="36ad1-116">Начиная с Outlook Social Connector 2013, OSC поддерживает только по запросу синхронизации действий и вызывает только **GetActivitiesEx** для получения действий.</span><span class="sxs-lookup"><span data-stu-id="36ad1-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="36ad1-117">Для поддержки поиска действий по запросу, задайте **cacheActivities** как **значение false**и **getActivities** и **dynamicActivitiesLookupEx** **значение true**, а OSC выполняется звонок **GetActivitiesEx**.</span><span class="sxs-lookup"><span data-stu-id="36ad1-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="36ad1-118">Возвращенная строка XML, должен соответствовать требованиям определение схемы для **activityFeed**, определенных в схеме для расширений поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="36ad1-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="36ad1-119">_HashedAddresses_ sring представляет набор хэш адресов для каждого пользователя, отображаемые в области пользователей.</span><span class="sxs-lookup"><span data-stu-id="36ad1-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="36ad1-120">Хэш SMTP-адреса, шифруются с помощью функции хэширования, указанных в элементе **hashFunction** **возможности** XML.</span><span class="sxs-lookup"><span data-stu-id="36ad1-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="36ad1-121">Пользователь не нужно быть друга при входе пользователя по свойству [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="36ad1-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="36ad1-122">Параметр _startTime_ является значением **даты** в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="36ad1-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="36ad1-123">Значения местного времени необходимо преобразовать в значения **даты** в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="36ad1-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="36ad1-124">Действия, которые возвращает метод **GetActivitiesEx** должен иметь значение времени создания, больше, чем _время начала_ и меньше или равно **теперь**.</span><span class="sxs-lookup"><span data-stu-id="36ad1-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="36ad1-125">Если изменений внесено не было между **startTime** и **теперь**, поставщик должен возвращать ошибку OSC_E_NO_CHANGES.</span><span class="sxs-lookup"><span data-stu-id="36ad1-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36ad1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="36ad1-126">See also</span></span>

- [<span data-ttu-id="36ad1-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36ad1-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="36ad1-128">Синхронизация друзей и действия</span><span class="sxs-lookup"><span data-stu-id="36ad1-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

