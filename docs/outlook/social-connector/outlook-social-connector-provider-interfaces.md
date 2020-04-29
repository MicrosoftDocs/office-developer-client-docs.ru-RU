---
title: Интерфейсы поставщика социальных соединителей Outlook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) — это компонент Office, совместно используемый клиентскими приложениями Office, которые подключаются к социальным и деловым сетям, поэтому пользователи могут оставаться на связи с людьми в своих сетях, не выходя из Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422812"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="f88d4-103">Интерфейсы поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="f88d4-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="f88d4-104">Outlook Social Connector (OSC) — это компонент Office, совместно используемый клиентскими приложениями Office, которые подключаются к социальным и деловым сетям, поэтому пользователи могут оставаться на связи с людьми в своих сетях, не выходя из Office.</span><span class="sxs-lookup"><span data-stu-id="f88d4-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="f88d4-105">Поставщик OSC — это DLL-библиотека COM, которая позволяет OSC получать доступ к данным социальных сетей так, как это не зависит от API каждой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="f88d4-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="f88d4-106">В следующей таблице перечислены интерфейсы расширяемости поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="f88d4-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="f88d4-107">Поставщик OSC должен реализовать четыре из пяти интерфейсов для общения с OSC: [исоЦиалперсон](isocialpersoniunknown.md), [исоЦиалпрофиле](isocialprofileisocialperson.md), [исоЦиалпровидер](isocialprovideriunknown.md)и [настроенный ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="f88d4-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="f88d4-108">Если поставщик OSC поддерживает синхронизацию действий, выполнение по требованию или гибридную синхронизацию друзей, кэширование учетных данных входа и вход в систему с использованием кэшированных учетных данных или возможность отслеживать человека, то поставщик также должен реализовать [ISocialSession2](isocialsession2iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="f88d4-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="f88d4-109">**Название**</span><span class="sxs-lookup"><span data-stu-id="f88d4-109">**Name**</span></span>|<span data-ttu-id="f88d4-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f88d4-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f88d4-111">исоЦиалперсон</span><span class="sxs-lookup"><span data-stu-id="f88d4-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="f88d4-112">Представляет пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="f88d4-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="f88d4-113">исоЦиалпрофиле</span><span class="sxs-lookup"><span data-stu-id="f88d4-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="f88d4-114">Представляет пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="f88d4-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="f88d4-115">исоЦиалпровидер</span><span class="sxs-lookup"><span data-stu-id="f88d4-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="f88d4-116">Представляет экземпляр поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="f88d4-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="f88d4-117">Настроенный ISocialSession</span><span class="sxs-lookup"><span data-stu-id="f88d4-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="f88d4-118">Представляет подключение к сайту социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f88d4-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="f88d4-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="f88d4-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="f88d4-120">Поддерживает синхронизацию действий, добавление друзей, по запросу или гибридную синхронизацию друзей, а также вход в социальную сеть с помощью кэшированных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="f88d4-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

