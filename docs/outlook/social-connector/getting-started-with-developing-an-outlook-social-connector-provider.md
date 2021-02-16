---
title: Начало разработки поставщика Outlook Social Connector
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: В справочнике по поставщику Outlook Social Connector (OSC) описывается разработка поставщика OSC с помощью возможности extensibility поставщика OSC.
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327162"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="ade7f-103">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="ade7f-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="ade7f-104">В справочнике по поставщику Outlook Social Connector (OSC) описывается разработка поставщика OSC с помощью возможности extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ade7f-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="ade7f-105">Если вы еще не разрабатываете решения для Outlook, см. статью "Выбор API или технологии для разработки решений Outlook для определения [API](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) и технологий, наиболее подходящих для ваших потребностей".</span><span class="sxs-lookup"><span data-stu-id="ade7f-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="ade7f-106">В этом разделе представлен обзор OSC, как поставщик OSC может быть полезен, быстрые шаги для изучения разработки поставщика, технические требования, советы и советы по разработке поставщика, а также новые возможности этого выпуска.</span><span class="sxs-lookup"><span data-stu-id="ade7f-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="ade7f-107">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="ade7f-107">In this section</span></span>

- <span data-ttu-id="ade7f-108">[Новые](what-s-new-for-providers.md)возможности для поставщиков: сравнение функций OSC в предыдущем и текущем выпусках, а также описание элементов интерфейса и элементов схемы XML, которые были добавлены, изменены или не являются неподдергодными в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="ade7f-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="ade7f-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span><span class="sxs-lookup"><span data-stu-id="ade7f-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="ade7f-110">[Связывание OSC с Outlook](relating-the-osc-with-outlook-and-social-networks.md)и социальными сетями : предоставляет архитектурное представление о том, как OSC соединяет пользователей Outlook с социальными сетями.</span><span class="sxs-lookup"><span data-stu-id="ade7f-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="ade7f-111">Кроме того, определяет способ использования общих терминов, таких как "социальные сети", "друзья", "не-друзья" и "контакты", в остальной части этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="ade7f-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="ade7f-112">[Быстрые шаги по разработке поставщика:](quick-steps-for-learning-to-develop-a-provider.md)сводка действий по разработке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ade7f-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="ade7f-113">[Технические требования](technical-requirements.md): описываются поддерживаемые языки программирования, требования к видимости COM, требования к типу возврата метода и сведения о DLL для возможности extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ade7f-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="ade7f-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span><span class="sxs-lookup"><span data-stu-id="ade7f-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="ade7f-115">Справка</span><span class="sxs-lookup"><span data-stu-id="ade7f-115">Reference</span></span>

- [<span data-ttu-id="ade7f-116">Outlook Social Connector Provider Reference</span><span class="sxs-lookup"><span data-stu-id="ade7f-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="ade7f-117">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="ade7f-117">Related sections</span></span>

- [<span data-ttu-id="ade7f-118">Примеры шаблонов OSC</span><span class="sxs-lookup"><span data-stu-id="ade7f-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="ade7f-119">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="ade7f-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="ade7f-120">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="ade7f-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="ade7f-121">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="ade7f-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="ade7f-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="ade7f-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="ade7f-123">Getting Ready to Release an OSC Provider</span><span class="sxs-lookup"><span data-stu-id="ade7f-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="ade7f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="ade7f-124">See also</span></span>

- [<span data-ttu-id="ade7f-125">Microsoft Outlook Social Connector 32-bit</span><span class="sxs-lookup"><span data-stu-id="ade7f-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="ade7f-126">Обновление для Outlook Social Connector (KB983403), 32-bit Edition</span><span class="sxs-lookup"><span data-stu-id="ade7f-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="ade7f-127">Обновление для Outlook Social Connector (KB983403), 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="ade7f-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="ade7f-128">Outlook Social Connector 2013: шаблоны поставщиков</span><span class="sxs-lookup"><span data-stu-id="ade7f-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

