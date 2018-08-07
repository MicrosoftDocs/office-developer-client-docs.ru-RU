---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Поддерживает добавление друзей, по требованию или комбинированным синхронизации друзья, синхронизации по запросу действий или выполнив вход социальной сети с помощью кэшированных учетных данных.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812753"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="194ca-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="194ca-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="194ca-104">Поддерживает добавление друзей, по требованию или комбинированным синхронизации друзья, синхронизации по запросу действий или выполнив вход социальной сети с помощью кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="194ca-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="194ca-105">Members</span><span class="sxs-lookup"><span data-stu-id="194ca-105">Members</span></span>

<span data-ttu-id="194ca-106">В следующей таблице показаны элементы, доступные в интерфейсе **ISocialSession2** .</span><span class="sxs-lookup"><span data-stu-id="194ca-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="194ca-107">**Имя**</span><span class="sxs-lookup"><span data-stu-id="194ca-107">**Name**</span></span>|<span data-ttu-id="194ca-108">**Тип участника**</span><span class="sxs-lookup"><span data-stu-id="194ca-108">**Member type**</span></span>|<span data-ttu-id="194ca-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="194ca-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="194ca-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="194ca-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="194ca-111">Метод</span><span class="sxs-lookup"><span data-stu-id="194ca-111">Method</span></span>  <br/> |<span data-ttu-id="194ca-112">Добавляет лица, указанного с помощью параметров _emailAddresses_ и _displayName_ как friend для пользователя при входе в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="194ca-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="194ca-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="194ca-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="194ca-114">Метод</span><span class="sxs-lookup"><span data-stu-id="194ca-114">Method</span></span>  <br/> |<span data-ttu-id="194ca-115">Получает строку, представляющую коллекцию действий пользователей, указанного с помощью параметра _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="194ca-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="194ca-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="194ca-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="194ca-117">Метод</span><span class="sxs-lookup"><span data-stu-id="194ca-117">Method</span></span>  <br/> |<span data-ttu-id="194ca-118">Возвращает строку, которая содержит коллекцию сведений человека и рисунок для пользователей, указанного с помощью параметра _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="194ca-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="194ca-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="194ca-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="194ca-120">Метод</span><span class="sxs-lookup"><span data-stu-id="194ca-120">Method</span></span>  <br/> |<span data-ttu-id="194ca-121">Журналы на узел социальной сети, используя кэшированные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="194ca-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="194ca-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="194ca-122">Remarks</span></span>

<span data-ttu-id="194ca-123">Для реализации этого интерфейса, если поставщик поддерживает по требованию или комбинированным синхронизации друзей, синхронизация по запросу действий или выполнив вход социальной сети с помощью кэшированных учетных данных можно выбрать поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="194ca-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="194ca-124">Если поставщика OSC реализует **ISocialSession2** и поддержка следующих лиц в социальных сетях, OSC вызовет [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) вместо [ISocialSession::FollowPerson](isocialsession-followperson.md)и поставщик должен реализовывать **ISocialSession2::FollowPersonEx**, а также.</span><span class="sxs-lookup"><span data-stu-id="194ca-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="194ca-125">См. также</span><span class="sxs-lookup"><span data-stu-id="194ca-125">See also</span></span>

- [<span data-ttu-id="194ca-126">Интерфейсы поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="194ca-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

