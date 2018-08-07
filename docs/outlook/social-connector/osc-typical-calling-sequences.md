---
title: Типичные последовательности вызовов OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: В этом разделе описываются типичные последовательности вызовов Outlook Social Connector (OSC) членов в интерфейсы возможности расширения поставщика OSC, которые реализует поставщика OSC.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812828"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="9239f-103">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="9239f-103">OSC typical calling sequences</span></span>

<span data-ttu-id="9239f-104">В этом разделе описываются типичные последовательности вызовов Outlook Social Connector (OSC) членов в интерфейсы возможности расширения поставщика OSC, которые реализует поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="9239f-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="9239f-105">Как и когда иллюстрируют типичные последовательности вызовов OSC используются такие интерфейсы и методы, позволяющие лучше определить, как реализовать данный элемент на интерфейс расширения поставщика.</span><span class="sxs-lookup"><span data-stu-id="9239f-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="9239f-106">Фактическая последовательность вызова могут различаться в зависимости от возможностей, возвращенный методом [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="9239f-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="9239f-107">Примеры возможностей:</span><span class="sxs-lookup"><span data-stu-id="9239f-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="9239f-108">Поставщик поддерживает для получения, кэширование и динамически поиск друзей и действия из социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="9239f-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="9239f-109">Пользовательский интерфейс, который OSC должны отображать для входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="9239f-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="9239f-110">Тип проверки подлинности (например, на основе форм проверки подлинности), который следует использовать OSC.</span><span class="sxs-lookup"><span data-stu-id="9239f-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="9239f-111">В этой статье</span><span class="sxs-lookup"><span data-stu-id="9239f-111">In this section</span></span>

- <span data-ttu-id="9239f-112">[Обычная проверка подлинности](basic-authentication.md): описывается типичное вызывающего последовательность OSC для поддержки для Office пользователя, вошедшего в социальной сети, если поставщик OSC поддерживает обычную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="9239f-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="9239f-113">[Проверка подлинности на основе форм](forms-based-authentication.md): описание типичная последовательность вызовов OSC для поддержки для Office пользователя, вошедшего в социальной сети, если поставщик OSC поддерживает проверку подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="9239f-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="9239f-114">[Начало действий](getting-activities.md): описывает типичное вызывающего последовательность OSC для синхронизации действий пользователя Office друзей из социальных сетей, если поставщика OSC социальной сети поддерживает синхронизацию действий.</span><span class="sxs-lookup"><span data-stu-id="9239f-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="9239f-115">[Получение сведений о друзьях](getting-friends-information.md): описывает типичное вызывающего последовательность OSC синхронизировать список друзей пользователя Office из социальных сетей, если поставщика OSC социальной сети поддерживает кэшированные синхронизации контактов.</span><span class="sxs-lookup"><span data-stu-id="9239f-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="9239f-116">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="9239f-116">Reference</span></span>

- [<span data-ttu-id="9239f-117">Справочник поставщика по Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="9239f-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="9239f-118">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="9239f-118">Related sections</span></span>

- [<span data-ttu-id="9239f-119">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="9239f-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="9239f-120">Шаблоны OSC примера</span><span class="sxs-lookup"><span data-stu-id="9239f-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="9239f-121">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="9239f-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="9239f-122">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="9239f-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="9239f-123">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="9239f-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="9239f-124">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="9239f-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="9239f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="9239f-125">See also</span></span>

- [<span data-ttu-id="9239f-126">XML-код для возможности</span><span class="sxs-lookup"><span data-stu-id="9239f-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

