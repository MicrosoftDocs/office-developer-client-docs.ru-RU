---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Поддерживает добавление друзей, гибридную синхронизацию друзей по требованию, синхронизацию действий по требованию или вход в социальные сети с помощью кэширования учетных данных.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408833"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="da401-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da401-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="da401-104">Поддерживает добавление друзей, гибридную синхронизацию друзей по требованию, синхронизацию действий по требованию или вход в социальные сети с помощью кэширования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="da401-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="da401-105">"Участники"</span><span class="sxs-lookup"><span data-stu-id="da401-105">Members</span></span>

<span data-ttu-id="da401-106">В следующей таблице показаны члены, доступные в интерфейсе **ISocialSession2.**</span><span class="sxs-lookup"><span data-stu-id="da401-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="da401-107">**Название**</span><span class="sxs-lookup"><span data-stu-id="da401-107">**Name**</span></span>|<span data-ttu-id="da401-108">**Тип члена**</span><span class="sxs-lookup"><span data-stu-id="da401-108">**Member type**</span></span>|<span data-ttu-id="da401-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="da401-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="da401-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="da401-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="da401-111">Method</span><span class="sxs-lookup"><span data-stu-id="da401-111">Method</span></span>  <br/> |<span data-ttu-id="da401-112">Добавляет пользователя, идентифицированного с помощью  _параметра emailAddresses_ и  _displayName,_ в качестве друга во время входа пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="da401-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="da401-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="da401-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="da401-114">Method</span><span class="sxs-lookup"><span data-stu-id="da401-114">Method</span></span>  <br/> |<span data-ttu-id="da401-115">Получает строку, представляюную коллекцию действий пользователей, указанных с помощью параметра _hashedAddresses._</span><span class="sxs-lookup"><span data-stu-id="da401-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="da401-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="da401-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="da401-117">Method</span><span class="sxs-lookup"><span data-stu-id="da401-117">Method</span></span>  <br/> |<span data-ttu-id="da401-118">Возвращает строку, которая содержит коллекцию сведений о пользователе и рисунке для пользователей, указанных _параметром personsAddresses._</span><span class="sxs-lookup"><span data-stu-id="da401-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="da401-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="da401-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="da401-120">Method</span><span class="sxs-lookup"><span data-stu-id="da401-120">Method</span></span>  <br/> |<span data-ttu-id="da401-121">Входит на сайт социальной сети с помощью кэшных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="da401-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da401-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="da401-122">Remarks</span></span>

<span data-ttu-id="da401-123">Поставщик Outlook Social Connector (OSC) может выбрать реализацию этого интерфейса, если поставщик поддерживает синхронизацию друзей по требованию или гибридную синхронизацию, синхронизацию действий по требованию или вход в социальные сети с помощью кэширования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="da401-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="da401-124">Если поставщик OSC реализует **ISocialSession2** и поддерживает следующих пользователей в социальной сети, OSC будет вызывать [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо [ISocialSession::FollowPerson](isocialsession-followperson.md), и поставщик должен реализовать **ISocialSession2::FollowPersonEx**, а также.</span><span class="sxs-lookup"><span data-stu-id="da401-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da401-125">См. также</span><span class="sxs-lookup"><span data-stu-id="da401-125">See also</span></span>

- [<span data-ttu-id="da401-126">Outlook Social Connector Provider Interfaces</span><span class="sxs-lookup"><span data-stu-id="da401-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

