---
title: Типичные последовательности вызовов OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: В этом разделе описаны типичные последовательности вызовов Outlook Social Connector (OSC) для членов в интерфейсах extensibility поставщика OSC, которые реализует поставщик OSC.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413614"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="1cabf-103">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="1cabf-103">OSC typical calling sequences</span></span>

<span data-ttu-id="1cabf-104">В этом разделе описаны типичные последовательности вызовов Outlook Social Connector (OSC) для членов в интерфейсах extensibility поставщика OSC, которые реализует поставщик OSC.</span><span class="sxs-lookup"><span data-stu-id="1cabf-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="1cabf-105">Типичные последовательности вызовов иллюстрируют, как и когда OSC использует такие интерфейсы и методы, чтобы лучше определить, как реализовать заданный член в интерфейсе extensibility поставщика.</span><span class="sxs-lookup"><span data-stu-id="1cabf-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="1cabf-106">Фактическая последовательность вызовов может отличаться в зависимости от возможностей, возвращаемого методом [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="1cabf-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="1cabf-107">Примеры возможностей:</span><span class="sxs-lookup"><span data-stu-id="1cabf-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="1cabf-108">Поддержка поставщика для получения, кэшинга или динамического получения друзей и действий из социальной сети.</span><span class="sxs-lookup"><span data-stu-id="1cabf-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="1cabf-109">Пользовательский интерфейс, который osC должен отображать для пользователя.</span><span class="sxs-lookup"><span data-stu-id="1cabf-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="1cabf-110">Тип проверки подлинности (например, проверка подлинности на основе форм), который должен использовать OSC.</span><span class="sxs-lookup"><span data-stu-id="1cabf-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="1cabf-111">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="1cabf-111">In this section</span></span>

- <span data-ttu-id="1cabf-112">[Обычная проверка](basic-authentication.md)подлинности : описывает типичную последовательность вызовов OSC для поддержки пользователя Office, который входит в социальные сети, если поставщик OSC поддерживает обычную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="1cabf-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="1cabf-113">[Проверка](forms-based-authentication.md)подлинности на основе форм : описывает типичную последовательность вызовов OSC для поддержки пользователя Office, который входит в социальные сети, если поставщик OSC поддерживает проверку подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="1cabf-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="1cabf-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span><span class="sxs-lookup"><span data-stu-id="1cabf-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="1cabf-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span><span class="sxs-lookup"><span data-stu-id="1cabf-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="1cabf-116">Справка</span><span class="sxs-lookup"><span data-stu-id="1cabf-116">Reference</span></span>

- [<span data-ttu-id="1cabf-117">Outlook Social Connector Provider Reference</span><span class="sxs-lookup"><span data-stu-id="1cabf-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="1cabf-118">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="1cabf-118">Related sections</span></span>

- [<span data-ttu-id="1cabf-119">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="1cabf-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="1cabf-120">Примеры шаблонов OSC</span><span class="sxs-lookup"><span data-stu-id="1cabf-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="1cabf-121">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="1cabf-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="1cabf-122">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="1cabf-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="1cabf-123">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="1cabf-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="1cabf-124">Best Practices for Developing a Provider</span><span class="sxs-lookup"><span data-stu-id="1cabf-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="1cabf-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1cabf-125">See also</span></span>

- [<span data-ttu-id="1cabf-126">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="1cabf-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

