---
title: ИсоЦиалпровидер IUnknown
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
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="30267-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30267-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="30267-104">Представляет экземпляр поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="30267-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="30267-105">"Участники"</span><span class="sxs-lookup"><span data-stu-id="30267-105">Members</span></span>

<span data-ttu-id="30267-106">В следующей таблице показаны элементы, доступные в интерфейсе **исоЦиалпровидер** .</span><span class="sxs-lookup"><span data-stu-id="30267-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="30267-107">**имя**</span><span class="sxs-lookup"><span data-stu-id="30267-107">**Name**</span></span>|<span data-ttu-id="30267-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="30267-108">**Member type**</span></span>|<span data-ttu-id="30267-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="30267-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="30267-110">дефаултситеурлс</span><span class="sxs-lookup"><span data-stu-id="30267-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="30267-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="30267-111">Property</span></span>  <br/> |<span data-ttu-id="30267-112">Возвращает массив строк, указывающих URL-адреса сайта для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="30267-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="30267-113">жетаутоконфигуредсессион</span><span class="sxs-lookup"><span data-stu-id="30267-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="30267-114">Method</span><span class="sxs-lookup"><span data-stu-id="30267-114">Method</span></span>  <br/> |<span data-ttu-id="30267-115">Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="30267-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="30267-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="30267-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="30267-117">Method</span><span class="sxs-lookup"><span data-stu-id="30267-117">Method</span></span>  <br/> |<span data-ttu-id="30267-118">Получает строку, описывающую возможности поставщика.</span><span class="sxs-lookup"><span data-stu-id="30267-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="30267-119">Сеансы.</span><span class="sxs-lookup"><span data-stu-id="30267-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="30267-120">Method</span><span class="sxs-lookup"><span data-stu-id="30267-120">Method</span></span>  <br/> |<span data-ttu-id="30267-121">Получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="30267-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="30267-122">жетстатуссеттингс</span><span class="sxs-lookup"><span data-stu-id="30267-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="30267-123">Method</span><span class="sxs-lookup"><span data-stu-id="30267-123">Method</span></span>  <br/> |<span data-ttu-id="30267-124">В настоящее время этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="30267-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="30267-125">Load</span><span class="sxs-lookup"><span data-stu-id="30267-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="30267-126">Method</span><span class="sxs-lookup"><span data-stu-id="30267-126">Method</span></span>  <br/> |<span data-ttu-id="30267-127">Инициализирует поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="30267-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="30267-128">соЦиалнетворкгуид</span><span class="sxs-lookup"><span data-stu-id="30267-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="30267-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="30267-129">Property</span></span>  <br/> |<span data-ttu-id="30267-130">Возвращает идентификатор GUID, представляющий уникальный идентификатор для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="30267-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="30267-131">соЦиалнетворкикон</span><span class="sxs-lookup"><span data-stu-id="30267-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="30267-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="30267-132">Property</span></span>  <br/> |<span data-ttu-id="30267-133">Возвращает массив байтов, представляющий значок социальной сети.</span><span class="sxs-lookup"><span data-stu-id="30267-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="30267-134">соЦиалнетворкнаме</span><span class="sxs-lookup"><span data-stu-id="30267-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="30267-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="30267-135">Property</span></span>  <br/> |<span data-ttu-id="30267-136">Возвращает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="30267-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="30267-137">Версия</span><span class="sxs-lookup"><span data-stu-id="30267-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="30267-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="30267-138">Property</span></span>  <br/> |<span data-ttu-id="30267-139">Возвращает строку, представляющую номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="30267-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30267-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="30267-140">Remarks</span></span>

<span data-ttu-id="30267-141">Поставщик OSC должен реализовать этот интерфейс для взаимодействия с OSC.</span><span class="sxs-lookup"><span data-stu-id="30267-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30267-142">См. также</span><span class="sxs-lookup"><span data-stu-id="30267-142">See also</span></span>

- [<span data-ttu-id="30267-143">Интерфейсы поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="30267-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

