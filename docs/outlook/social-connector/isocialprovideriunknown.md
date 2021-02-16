---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Представляет экземпляр поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409960"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="55500-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55500-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="55500-104">Представляет экземпляр поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="55500-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="55500-105">"Участники"</span><span class="sxs-lookup"><span data-stu-id="55500-105">Members</span></span>

<span data-ttu-id="55500-106">В следующей таблице показаны члены, доступные в **интерфейсе ISocialProvider.**</span><span class="sxs-lookup"><span data-stu-id="55500-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="55500-107">**Название**</span><span class="sxs-lookup"><span data-stu-id="55500-107">**Name**</span></span>|<span data-ttu-id="55500-108">**Тип члена**</span><span class="sxs-lookup"><span data-stu-id="55500-108">**Member type**</span></span>|<span data-ttu-id="55500-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55500-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55500-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="55500-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="55500-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="55500-111">Property</span></span>  <br/> |<span data-ttu-id="55500-112">Возвращает массив строк, которые указывают URL-адреса сайта для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="55500-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="55500-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="55500-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="55500-114">Method</span><span class="sxs-lookup"><span data-stu-id="55500-114">Method</span></span>  <br/> |<span data-ttu-id="55500-115">Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="55500-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="55500-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="55500-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="55500-117">Method</span><span class="sxs-lookup"><span data-stu-id="55500-117">Method</span></span>  <br/> |<span data-ttu-id="55500-118">Получает строку, описываемую возможности поставщика.</span><span class="sxs-lookup"><span data-stu-id="55500-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="55500-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="55500-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="55500-120">Method</span><span class="sxs-lookup"><span data-stu-id="55500-120">Method</span></span>  <br/> |<span data-ttu-id="55500-121">Получает интерфейс [ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="55500-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="55500-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="55500-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="55500-123">Method</span><span class="sxs-lookup"><span data-stu-id="55500-123">Method</span></span>  <br/> |<span data-ttu-id="55500-124">Этот метод в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="55500-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="55500-125">Load</span><span class="sxs-lookup"><span data-stu-id="55500-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="55500-126">Method</span><span class="sxs-lookup"><span data-stu-id="55500-126">Method</span></span>  <br/> |<span data-ttu-id="55500-127">Инициализирует поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="55500-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="55500-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="55500-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="55500-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="55500-129">Property</span></span>  <br/> |<span data-ttu-id="55500-130">Возвращает ИДЕНТИФИКАТОР GUID, который представляет уникальный идентификатор для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="55500-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="55500-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="55500-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="55500-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="55500-132">Property</span></span>  <br/> |<span data-ttu-id="55500-133">Возвращает массив в ветвях, который представляет значок для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="55500-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="55500-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="55500-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="55500-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="55500-135">Property</span></span>  <br/> |<span data-ttu-id="55500-136">Возвращает строку, представляюную имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="55500-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="55500-137">Версия</span><span class="sxs-lookup"><span data-stu-id="55500-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="55500-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="55500-138">Property</span></span>  <br/> |<span data-ttu-id="55500-139">Возвращает строку, представляюную номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="55500-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55500-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="55500-140">Remarks</span></span>

<span data-ttu-id="55500-141">Поставщик OSC должен реализовать этот интерфейс для связи с OSC.</span><span class="sxs-lookup"><span data-stu-id="55500-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55500-142">См. также</span><span class="sxs-lookup"><span data-stu-id="55500-142">See also</span></span>

- [<span data-ttu-id="55500-143">Outlook Social Connector Provider Interfaces</span><span class="sxs-lookup"><span data-stu-id="55500-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

