---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Поддерживает добавление друзей, синхронизации по требованию или гибридной синхронизации друзей, синхронизации действий по требованию или входа в социальной сети с помощью кэшированных учетных данных.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408833"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="c6a00-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6a00-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="c6a00-104">Поддерживает добавление друзей, синхронизации по требованию или гибридной синхронизации друзей, синхронизации действий по требованию или входа в социальной сети с помощью кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c6a00-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="c6a00-105">Members</span><span class="sxs-lookup"><span data-stu-id="c6a00-105">Members</span></span>

<span data-ttu-id="c6a00-106">В следующей таблице показаны элементы, доступные в интерфейсе **ISocialSession2** .</span><span class="sxs-lookup"><span data-stu-id="c6a00-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="c6a00-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="c6a00-107">**Name**</span></span>|<span data-ttu-id="c6a00-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c6a00-108">**Member type**</span></span>|<span data-ttu-id="c6a00-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c6a00-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c6a00-110">Фолловперсонекс</span><span class="sxs-lookup"><span data-stu-id="c6a00-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="c6a00-111">Метод</span><span class="sxs-lookup"><span data-stu-id="c6a00-111">Method</span></span>  <br/> |<span data-ttu-id="c6a00-112">Добавляет пользователя, идентифицируемого параметрами _EmailAddresses_ и _DisplayName_ , как Friend для вошедшего в сеть пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="c6a00-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="c6a00-113">Жетактивитиесекс</span><span class="sxs-lookup"><span data-stu-id="c6a00-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="c6a00-114">Метод</span><span class="sxs-lookup"><span data-stu-id="c6a00-114">Method</span></span>  <br/> |<span data-ttu-id="c6a00-115">Получает строку, представляющую коллекцию действий пользователей, указанных в параметре _хашедаддрессес_ .</span><span class="sxs-lookup"><span data-stu-id="c6a00-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="c6a00-116">Жетпеопледетаилс</span><span class="sxs-lookup"><span data-stu-id="c6a00-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="c6a00-117">Метод</span><span class="sxs-lookup"><span data-stu-id="c6a00-117">Method</span></span>  <br/> |<span data-ttu-id="c6a00-118">Возвращает строку, содержащую коллекцию сведений о пользователях и изображениях для пользователей, указанных в параметре _персонсаддрессес_ .</span><span class="sxs-lookup"><span data-stu-id="c6a00-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="c6a00-119">Логонкачед</span><span class="sxs-lookup"><span data-stu-id="c6a00-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="c6a00-120">Метод</span><span class="sxs-lookup"><span data-stu-id="c6a00-120">Method</span></span>  <br/> |<span data-ttu-id="c6a00-121">Выполняет вход на сайт социальных сетей с использованием кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c6a00-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6a00-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6a00-122">Remarks</span></span>

<span data-ttu-id="c6a00-123">Поставщик Outlook Social Connector (OSC) может реализовать этот интерфейс, если поставщик поддерживает потребовать или гибридную синхронизацию друзей, синхронизацию действий по запросу или вход в социальной сети с помощью кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c6a00-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="c6a00-124">Если поставщик OSC реализует **ISocialSession2** и поддерживает в социальных сетях следующие лица, OSC вызовет [ISocialSession2:: фолловперсонекс](isocialsession2-followpersonex.md) , а не [настроенный ISocialSession:: фолловперсон](isocialsession-followperson.md), и поставщик должен реализовать **ISocialSession2:: фолловперсонекс**, а также.</span><span class="sxs-lookup"><span data-stu-id="c6a00-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6a00-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c6a00-125">See also</span></span>

- [<span data-ttu-id="c6a00-126">Интерфейсы поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="c6a00-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

