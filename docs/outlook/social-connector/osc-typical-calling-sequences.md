---
title: Типичные последовательности вызовов OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: В этом разделе описываются типичные последовательности вызовов Outlook social Connector (OSC) членов в интерфейсах extensibility поставщика OSC, которые реализует поставщик OSC.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413614"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="f4552-103">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="f4552-103">OSC typical calling sequences</span></span>

<span data-ttu-id="f4552-104">В этом разделе описываются типичные последовательности вызовов Outlook social Connector (OSC) членов в интерфейсах extensibility поставщика OSC, которые реализует поставщик OSC.</span><span class="sxs-lookup"><span data-stu-id="f4552-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="f4552-105">Типичные последовательности вызовов иллюстрируют, как и когда OSC использует такие интерфейсы и методы, чтобы лучше определить, как реализовать данный член в интерфейсе extensibility поставщика.</span><span class="sxs-lookup"><span data-stu-id="f4552-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="f4552-106">Фактическая последовательность вызовов может варьироваться в зависимости от возможностей, возвращаемого методом [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="f4552-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="f4552-107">Примеры возможностей включают следующие:</span><span class="sxs-lookup"><span data-stu-id="f4552-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="f4552-108">Поддержка поставщика для получения, кэшинга или динамического получения друзей и действий из социальной сети.</span><span class="sxs-lookup"><span data-stu-id="f4552-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="f4552-109">Пользовательский интерфейс, который OSC должен отображать для логоса пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4552-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="f4552-110">Тип проверки подлинности (например, проверка подлинности на основе форм), который должен использовать OSC.</span><span class="sxs-lookup"><span data-stu-id="f4552-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="f4552-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="f4552-111">In this section</span></span>

- <span data-ttu-id="f4552-112">[Базовая](basic-authentication.md)проверка подлинности. Описывает типичную последовательность вызовов OSC для поддержки пользователя, который Office, войдя в социальную сеть, если поставщик OSC поддерживает базовую проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="f4552-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="f4552-113">[Проверка](forms-based-authentication.md)подлинности на основе форм. Описывает типичную последовательность вызовов OSC для поддержки пользователя Office, который входит в социальную сеть, если поставщик OSC поддерживает проверку подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="f4552-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="f4552-114">[Получение действий](getting-activities.md). Описывает типичную последовательность вызовов OSC для синхронизации действий друзей пользователя Office из социальной сети, если поставщик osc социальной сети поддерживает синхронизацию действий.</span><span class="sxs-lookup"><span data-stu-id="f4552-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="f4552-115">[Получение сведений](getting-friends-information.md)о друзьях. Описывает типичную последовательность вызовов OSC для синхронизации списка друзей Office пользователя из социальной сети, если поставщик osc социальной сети поддерживает кэширование контактов.</span><span class="sxs-lookup"><span data-stu-id="f4552-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="f4552-116">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="f4552-116">Reference</span></span>

- [<span data-ttu-id="f4552-117">Outlook Справка о поставщике социальных соединители</span><span class="sxs-lookup"><span data-stu-id="f4552-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="f4552-118">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="f4552-118">Related sections</span></span>

- [<span data-ttu-id="f4552-119">Начало работы с разработкой Outlook поставщика социальных соединители</span><span class="sxs-lookup"><span data-stu-id="f4552-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="f4552-120">Шаблоны образцов OSC</span><span class="sxs-lookup"><span data-stu-id="f4552-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="f4552-121">Разработка поставщика с помощью схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="f4552-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="f4552-122">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="f4552-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="f4552-123">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="f4552-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="f4552-124">Лучшие практики для разработки поставщика</span><span class="sxs-lookup"><span data-stu-id="f4552-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="f4552-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f4552-125">See also</span></span>

- [<span data-ttu-id="f4552-126">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="f4552-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

