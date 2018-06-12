---
title: Интерфейсы поставщика Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) — это функция совместно с клиентскими приложениями Office, который подключается к социальных и business сети, чтобы пользователи могли оставаться связи с в сети, не выходя из Office.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812833"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="07017-103">Интерфейсы поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="07017-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="07017-104">Outlook Social Connector (OSC) — это функция совместно с клиентскими приложениями Office, который подключается к социальных и business сети, чтобы пользователи могли оставаться связи с в сети, не выходя из Office.</span><span class="sxs-lookup"><span data-stu-id="07017-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="07017-105">Поставщика OSC — модели компонентных объектов (COM) библиотеки DLL, которая позволяет OSC для доступа к данным социальных сетей, чтобы не зависит от API-интерфейсы каждого социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="07017-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="07017-106">В следующей таблице перечислены интерфейсы расширяемости поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="07017-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="07017-107">Четыре из пяти интерфейсы для взаимодействия с OSC должен быть реализован поставщика OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)и [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="07017-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="07017-108">Если поставщика OSC поддерживает синхронизацию мероприятий по требованию или синхронизации гибридного друзей, кэширование учетные данные для входа и войдите в систему с помощью кэширования учетных данных или возможность отслеживать человеком, поставщик должен реализовывать [ISocialSession2 ](isocialsession2iunknown.md), а также.</span><span class="sxs-lookup"><span data-stu-id="07017-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="07017-109">**Имя**</span><span class="sxs-lookup"><span data-stu-id="07017-109">**Name**</span></span>|<span data-ttu-id="07017-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="07017-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07017-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="07017-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="07017-112">Представляет человека в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="07017-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="07017-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="07017-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="07017-114">Представляет пользователя, вошедшего в систему.</span><span class="sxs-lookup"><span data-stu-id="07017-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="07017-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="07017-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="07017-116">Представляет экземпляр объекта поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="07017-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="07017-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="07017-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="07017-118">Представляет подключение к сайту социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="07017-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="07017-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="07017-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="07017-120">Синхронизация действий, Добавление друзей, поддерживает по требованию или комбинированным синхронизации друзей или выполнив вход социальной сети с помощью кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="07017-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

