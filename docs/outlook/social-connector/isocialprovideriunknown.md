---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Представляет экземпляр поставщика Outlook(OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409960"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="82378-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82378-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="82378-104">Представляет экземпляр поставщика Outlook(OSC).</span><span class="sxs-lookup"><span data-stu-id="82378-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="82378-105">"Участники"</span><span class="sxs-lookup"><span data-stu-id="82378-105">Members</span></span>

<span data-ttu-id="82378-106">В следующей таблице показаны участники, доступные в **интерфейсе ISocialProvider.**</span><span class="sxs-lookup"><span data-stu-id="82378-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="82378-107">**Имя**</span><span class="sxs-lookup"><span data-stu-id="82378-107">**Name**</span></span>|<span data-ttu-id="82378-108">**Тип участника**</span><span class="sxs-lookup"><span data-stu-id="82378-108">**Member type**</span></span>|<span data-ttu-id="82378-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="82378-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="82378-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="82378-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="82378-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="82378-111">Property</span></span>  <br/> |<span data-ttu-id="82378-112">Возвращает массив строк, которые указывают URL-адреса сайтов для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="82378-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="82378-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="82378-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="82378-114">Метод</span><span class="sxs-lookup"><span data-stu-id="82378-114">Method</span></span>  <br/> |<span data-ttu-id="82378-115">Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="82378-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="82378-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="82378-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="82378-117">Метод</span><span class="sxs-lookup"><span data-stu-id="82378-117">Method</span></span>  <br/> |<span data-ttu-id="82378-118">Получает строку, описываемую возможностями поставщика.</span><span class="sxs-lookup"><span data-stu-id="82378-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="82378-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="82378-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="82378-120">Метод</span><span class="sxs-lookup"><span data-stu-id="82378-120">Method</span></span>  <br/> |<span data-ttu-id="82378-121">Получает [интерфейс ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="82378-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="82378-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="82378-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="82378-123">Метод</span><span class="sxs-lookup"><span data-stu-id="82378-123">Method</span></span>  <br/> |<span data-ttu-id="82378-124">Этот метод в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="82378-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="82378-125">Load</span><span class="sxs-lookup"><span data-stu-id="82378-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="82378-126">Метод</span><span class="sxs-lookup"><span data-stu-id="82378-126">Method</span></span>  <br/> |<span data-ttu-id="82378-127">Инициализирует поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="82378-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="82378-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="82378-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="82378-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="82378-129">Property</span></span>  <br/> |<span data-ttu-id="82378-130">Возвращает GUID, представляюря уникальный идентификатор для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="82378-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="82378-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="82378-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="82378-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="82378-132">Property</span></span>  <br/> |<span data-ttu-id="82378-133">Возвращает массив bytes, который представляет значок для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="82378-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="82378-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="82378-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="82378-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="82378-135">Property</span></span>  <br/> |<span data-ttu-id="82378-136">Возвращает строку, представляюную имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="82378-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="82378-137">Версия</span><span class="sxs-lookup"><span data-stu-id="82378-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="82378-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="82378-138">Property</span></span>  <br/> |<span data-ttu-id="82378-139">Возвращает строку, представляюную номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="82378-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82378-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="82378-140">Remarks</span></span>

<span data-ttu-id="82378-141">Поставщик OSC должен реализовать этот интерфейс для связи с OSC.</span><span class="sxs-lookup"><span data-stu-id="82378-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82378-142">См. также</span><span class="sxs-lookup"><span data-stu-id="82378-142">See also</span></span>

- [<span data-ttu-id="82378-143">Outlook Интерфейсы поставщиков социальных соединители</span><span class="sxs-lookup"><span data-stu-id="82378-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

