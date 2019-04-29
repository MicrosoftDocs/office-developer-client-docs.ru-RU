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
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="edb6d-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edb6d-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="edb6d-104">Представляет экземпляр поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="edb6d-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="edb6d-105">Members</span><span class="sxs-lookup"><span data-stu-id="edb6d-105">Members</span></span>

<span data-ttu-id="edb6d-106">В следующей таблице показаны элементы, доступные в интерфейсе **исоЦиалпровидер** .</span><span class="sxs-lookup"><span data-stu-id="edb6d-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="edb6d-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="edb6d-107">**Name**</span></span>|<span data-ttu-id="edb6d-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="edb6d-108">**Member type**</span></span>|<span data-ttu-id="edb6d-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="edb6d-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="edb6d-110">Дефаултситеурлс</span><span class="sxs-lookup"><span data-stu-id="edb6d-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="edb6d-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="edb6d-111">Property</span></span>  <br/> |<span data-ttu-id="edb6d-112">Возвращает массив строк, указывающих URL-адреса сайта для поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="edb6d-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-113">Жетаутоконфигуредсессион</span><span class="sxs-lookup"><span data-stu-id="edb6d-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="edb6d-114">Метод</span><span class="sxs-lookup"><span data-stu-id="edb6d-114">Method</span></span>  <br/> |<span data-ttu-id="edb6d-115">Получает автоматически настроенный интерфейс [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="edb6d-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="edb6d-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="edb6d-117">Метод</span><span class="sxs-lookup"><span data-stu-id="edb6d-117">Method</span></span>  <br/> |<span data-ttu-id="edb6d-118">Получает строку, описывающую возможности поставщика.</span><span class="sxs-lookup"><span data-stu-id="edb6d-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-119">Сеансы.</span><span class="sxs-lookup"><span data-stu-id="edb6d-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="edb6d-120">Метод</span><span class="sxs-lookup"><span data-stu-id="edb6d-120">Method</span></span>  <br/> |<span data-ttu-id="edb6d-121">Получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="edb6d-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-122">Жетстатуссеттингс</span><span class="sxs-lookup"><span data-stu-id="edb6d-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="edb6d-123">Метод</span><span class="sxs-lookup"><span data-stu-id="edb6d-123">Method</span></span>  <br/> |<span data-ttu-id="edb6d-124">В настоящее время этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="edb6d-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-125">Load</span><span class="sxs-lookup"><span data-stu-id="edb6d-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="edb6d-126">Метод</span><span class="sxs-lookup"><span data-stu-id="edb6d-126">Method</span></span>  <br/> |<span data-ttu-id="edb6d-127">Инициализирует поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="edb6d-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-128">СоЦиалнетворкгуид</span><span class="sxs-lookup"><span data-stu-id="edb6d-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="edb6d-129">Свойство</span><span class="sxs-lookup"><span data-stu-id="edb6d-129">Property</span></span>  <br/> |<span data-ttu-id="edb6d-130">Возвращает идентификатор GUID, представляющий уникальный идентификатор для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="edb6d-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-131">СоЦиалнетворкикон</span><span class="sxs-lookup"><span data-stu-id="edb6d-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="edb6d-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="edb6d-132">Property</span></span>  <br/> |<span data-ttu-id="edb6d-133">Возвращает массив байтов, представляющий значок социальной сети.</span><span class="sxs-lookup"><span data-stu-id="edb6d-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-134">СоЦиалнетворкнаме</span><span class="sxs-lookup"><span data-stu-id="edb6d-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="edb6d-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="edb6d-135">Property</span></span>  <br/> |<span data-ttu-id="edb6d-136">Возвращает строку, представляющую имя социальной сети.</span><span class="sxs-lookup"><span data-stu-id="edb6d-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="edb6d-137">Version</span><span class="sxs-lookup"><span data-stu-id="edb6d-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="edb6d-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="edb6d-138">Property</span></span>  <br/> |<span data-ttu-id="edb6d-139">Возвращает строку, представляющую номер версии поставщика для этой социальной сети.</span><span class="sxs-lookup"><span data-stu-id="edb6d-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edb6d-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="edb6d-140">Remarks</span></span>

<span data-ttu-id="edb6d-141">Поставщик OSC должен реализовать этот интерфейс для взаимодействия с OSC.</span><span class="sxs-lookup"><span data-stu-id="edb6d-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edb6d-142">См. также</span><span class="sxs-lookup"><span data-stu-id="edb6d-142">See also</span></span>

- [<span data-ttu-id="edb6d-143">Интерфейсы поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="edb6d-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

