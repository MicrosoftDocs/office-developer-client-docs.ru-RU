---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Представляет экземпляр объекта поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812856"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="c5f32-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c5f32-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="c5f32-104">Представляет экземпляр объекта поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="c5f32-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="c5f32-105">Members</span><span class="sxs-lookup"><span data-stu-id="c5f32-105">Members</span></span>

<span data-ttu-id="c5f32-106">В следующей таблице показаны элементы, доступные в интерфейсе **ISocialProvider** .</span><span class="sxs-lookup"><span data-stu-id="c5f32-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="c5f32-107">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c5f32-107">**Name**</span></span>|<span data-ttu-id="c5f32-108">**Тип участника**</span><span class="sxs-lookup"><span data-stu-id="c5f32-108">**Member type**</span></span>|<span data-ttu-id="c5f32-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5f32-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5f32-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="c5f32-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="c5f32-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="c5f32-111">Property</span></span>  <br/> |<span data-ttu-id="c5f32-112">Возвращает массив строк, которые задают URL-адресов сайта для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="c5f32-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="c5f32-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="c5f32-114">Метод</span><span class="sxs-lookup"><span data-stu-id="c5f32-114">Method</span></span>  <br/> |<span data-ttu-id="c5f32-115">Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c5f32-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="c5f32-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="c5f32-117">Метод</span><span class="sxs-lookup"><span data-stu-id="c5f32-117">Method</span></span>  <br/> |<span data-ttu-id="c5f32-118">Получает строку, которая описывает возможности поставщика.</span><span class="sxs-lookup"><span data-stu-id="c5f32-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="c5f32-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="c5f32-120">Метод</span><span class="sxs-lookup"><span data-stu-id="c5f32-120">Method</span></span>  <br/> |<span data-ttu-id="c5f32-121">Получает интерфейс [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="c5f32-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="c5f32-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="c5f32-123">Метод</span><span class="sxs-lookup"><span data-stu-id="c5f32-123">Method</span></span>  <br/> |<span data-ttu-id="c5f32-124">Этот метод в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c5f32-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-125">Нагрузки</span><span class="sxs-lookup"><span data-stu-id="c5f32-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="c5f32-126">Метод</span><span class="sxs-lookup"><span data-stu-id="c5f32-126">Method</span></span>  <br/> |<span data-ttu-id="c5f32-127">Инициализирует поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="c5f32-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="c5f32-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="c5f32-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="c5f32-129">Property</span></span>  <br/> |<span data-ttu-id="c5f32-130">Возвращает идентификатор GUID, который представляет уникальный идентификатор для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="c5f32-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="c5f32-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="c5f32-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="c5f32-132">Property</span></span>  <br/> |<span data-ttu-id="c5f32-133">Возвращает массив байтов, который представляет значок для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="c5f32-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="c5f32-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="c5f32-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="c5f32-135">Property</span></span>  <br/> |<span data-ttu-id="c5f32-136">Возвращает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="c5f32-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="c5f32-137">Версия</span><span class="sxs-lookup"><span data-stu-id="c5f32-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="c5f32-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="c5f32-138">Property</span></span>  <br/> |<span data-ttu-id="c5f32-139">Возвращает строку, представляющую номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="c5f32-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5f32-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="c5f32-140">Remarks</span></span>

<span data-ttu-id="c5f32-141">Поставщика OSC необходимо реализовать этот интерфейс для взаимодействия с OSC.</span><span class="sxs-lookup"><span data-stu-id="c5f32-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5f32-142">См. также</span><span class="sxs-lookup"><span data-stu-id="c5f32-142">See also</span></span>

- [<span data-ttu-id="c5f32-143">Интерфейсы поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="c5f32-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

