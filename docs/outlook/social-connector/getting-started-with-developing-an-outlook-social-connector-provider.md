---
title: Начало разработки поставщика Outlook Social Connector
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: Справочник поставщика Outlook Social Connector (OSC) описывается, как разрабатывать поставщика OSC, используя возможности расширения поставщика OSC.
ms.openlocfilehash: 19f5ffe8987d0b19017692ddb8f7888be2140033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812702"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="7d1e3-103">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="7d1e3-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="7d1e3-104">Справочник поставщика Outlook Social Connector (OSC) описывается, как разрабатывать поставщика OSC, используя возможности расширения поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="7d1e3-105">Если вы не знакомы с разработкой решения для Outlook, статью [Выбор API или технологий для разработки решений Outlook](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) для идентификации интерфейсы API и технологии, наиболее подходящие вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](http://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="7d1e3-106">В этом разделе дается обзор OSC, как поставщика OSC может быть полезен, быстрого шаги, необходимые для разработки поставщика, технических требований, рекомендации по разработке поставщика и новые возможности этой версии.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="7d1e3-107">В этой статье</span><span class="sxs-lookup"><span data-stu-id="7d1e3-107">In this section</span></span>

- <span data-ttu-id="7d1e3-108">[Новые возможности для поставщиков](what-s-new-for-providers.md): сравнивает OSC функций в предыдущей и текущей версии, а также описание интерфейса элементы и элементы XML-схемы, которые были добавлены, изменены или не поддерживаются в этой версии.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="7d1e3-109">[Почему разработки поставщика Outlook Social Connector](why-develop-an-outlook-social-connector-provider.md): описывает, как можно использовать для распространенных сайтов социальных сетей и другие внутренние сетевые средства поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="7d1e3-110">[Связанные OSC с Outlook и социальными сетями](relating-the-osc-with-outlook-and-social-networks.md): предоставляет представления архитектуры как OSC подключается пользователи Outlook с социальными сетями.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="7d1e3-111">Также определяет способ, общие термины, как «социальных сетей», «друзья», «не друзья,» и «контакты» используются в оставшейся части этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="7d1e3-112">[Быстрый шаги, необходимые для разработки поставщика](quick-steps-for-learning-to-develop-a-provider.md): Сводка действия, чтобы сведения о разработке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="7d1e3-113">[Технические требования](technical-requirements.md): описываются поддерживаемые языки программирования, требования к обеспечению COM, метод возвращаемый тип требования и сведения о возможности расширения поставщика OSC DLL-Библиотеку.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="7d1e3-114">[Рекомендации по разработке поставщика](best-practices-for-developing-a-provider.md): предоставляет список рекомендации при разработке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="7d1e3-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="7d1e3-115">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="7d1e3-115">Reference</span></span>

- [<span data-ttu-id="7d1e3-116">Справочник поставщика по Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="7d1e3-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="7d1e3-117">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="7d1e3-117">Related sections</span></span>

- [<span data-ttu-id="7d1e3-118">Шаблоны OSC примера</span><span class="sxs-lookup"><span data-stu-id="7d1e3-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="7d1e3-119">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="7d1e3-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="7d1e3-120">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="7d1e3-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="7d1e3-121">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="7d1e3-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="7d1e3-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="7d1e3-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="7d1e3-123">Подготовка к выпуску поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="7d1e3-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="7d1e3-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7d1e3-124">See also</span></span>

- [<span data-ttu-id="7d1e3-125">Microsoft Outlook Social Connector с 32-разрядная версия</span><span class="sxs-lookup"><span data-stu-id="7d1e3-125">Microsoft Outlook Social Connector 32-bit</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="7d1e3-126">Обновление для Outlook Social Connector (KB983403), 32-разрядные версии</span><span class="sxs-lookup"><span data-stu-id="7d1e3-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="7d1e3-127">Обновление для Outlook Social Connector (KB983403), 64-разрядный выпуск</span><span class="sxs-lookup"><span data-stu-id="7d1e3-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](http://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="7d1e3-128">Outlook Social Connector 2013: Шаблоны поставщика</span><span class="sxs-lookup"><span data-stu-id="7d1e3-128">Outlook Social Connector 2013: Provider templates</span></span>](http://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

