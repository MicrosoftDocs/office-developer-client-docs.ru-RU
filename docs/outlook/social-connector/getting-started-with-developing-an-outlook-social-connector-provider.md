---
title: Начало разработки поставщика Outlook Social Connector
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c65d2df-86a3-48d5-9fec-a9040f3b878c
description: В справочнике по поставщику Outlook Social Connector (OSC) описывается разработка поставщика OSC с помощью расширяемости поставщика OSC.
ms.openlocfilehash: 24f8eabe33103f53e848f055b72fd402bc5dd89a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327162"
---
# <a name="getting-started-with-developing-an-outlook-social-connector-provider"></a><span data-ttu-id="ec1cf-103">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="ec1cf-103">Getting started with developing an Outlook Social Connector provider</span></span>

<span data-ttu-id="ec1cf-104">В справочнике по поставщику Outlook Social Connector (OSC) описывается разработка поставщика OSC с помощью расширяемости поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-104">The Outlook Social Connector (OSC) Provider Reference describes how to develop an OSC provider by using OSC provider extensibility.</span></span> <span data-ttu-id="ec1cf-105">Если вы не впервые разрабатываете решения для Outlook, ознакомьтесь со статьей [Выбор API или технологии для разработки решений Outlook](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) для определения интерфейсов API и технологий, наиболее подходящих для ваших потребностей.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-105">If you are new to developing solutions for Outlook, see [Selecting an API or Technology for Developing Outlook Solutions](https://msdn.microsoft.com/library/8295da20-e567-4d08-b8e4-5c9b4498edd4%28Office.15%29.aspx) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 

<span data-ttu-id="ec1cf-106">В этом разделе дается обзор OSC, как поставщик OSC может быть полезен, быстрые действия для изучения процесса разработки поставщика, технические требования, рекомендации по разработке поставщика и новые возможности этого выпуска.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-106">This section gives an overview of the OSC, how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="ec1cf-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="ec1cf-107">In this section</span></span>

- <span data-ttu-id="ec1cf-108">[Новые возможности для поставщиков](what-s-new-for-providers.md): Сравнение функций OSC в предыдущем и текущем выпуске, а также описание элементов интерфейса и элементов схемы XML, добавленных, измененных или устаревших в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-108">[What's New for Providers](what-s-new-for-providers.md): Compares OSC features in the previous and current release, and describes interface members and XML schema elements that have been added, changed, or deprecated in this release.</span></span> 
    
- <span data-ttu-id="ec1cf-109">[Зачем разрабатывать поставщик Outlook Social Connector](why-develop-an-outlook-social-connector-provider.md): в этой статье описывается, как поставщик OSC может быть полезен для общих сайтов социальных сетей и других средств внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-109">[Why Develop an Outlook Social Connector Provider](why-develop-an-outlook-social-connector-provider.md): Describes how an OSC provider can be useful for common social network sites and other internal networking tools.</span></span>
    
- <span data-ttu-id="ec1cf-110">[Соотнесение OSC с Outlook и социальными сетями](relating-the-osc-with-outlook-and-social-networks.md): в этой статье представлено архитектурное представление того, как OSC подключает пользователей Outlook с социальными сетями.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-110">[Relating the OSC with Outlook and Social Networks](relating-the-osc-with-outlook-and-social-networks.md): Provides an architectural view of how the OSC connects Outlook users with social networks.</span></span> <span data-ttu-id="ec1cf-111">Также определяет способ использования общих терминов, таких как "социальные сети", "друзья", "не друзья" и "Контакты", в оставшейся части этой справочной ссылки.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-111">Also defines the way that common terms, like "social networks," "friends," "non-friends," and "contacts" are used in the rest of this reference.</span></span>
    
- <span data-ttu-id="ec1cf-112">[Быстрые действия по разработке поставщика](quick-steps-for-learning-to-develop-a-provider.md): в этой статье представлен обзор действий по разработке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-112">[Quick Steps for Learning to Develop a Provider](quick-steps-for-learning-to-develop-a-provider.md): Provides a summary of steps to learn to develop an OSC provider.</span></span>
    
- <span data-ttu-id="ec1cf-113">[Технические требования](technical-requirements.md): в этой статье описываются поддерживаемые языки программирования, требования к видимости com, требования к типам возвращаемых данных методов и сведения о библиотеке DLL расширения поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-113">[Technical Requirements](technical-requirements.md): Describes the supported programming languages, COM visibility requirements, method return type requirements, and details of the OSC provider extensibility DLL.</span></span>
    
- <span data-ttu-id="ec1cf-114">Рекомендации [по разработке поставщика](best-practices-for-developing-a-provider.md): в этой статье представлен список рекомендаций, которые необходимо выполнить при разработке поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="ec1cf-114">[Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md): Provides a list of best practices to follow while developing an OSC provider.</span></span>
    
## <a name="reference"></a><span data-ttu-id="ec1cf-115">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="ec1cf-115">Reference</span></span>

- [<span data-ttu-id="ec1cf-116">Справочник по поставщику Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="ec1cf-116">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="ec1cf-117">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="ec1cf-117">Related sections</span></span>

- [<span data-ttu-id="ec1cf-118">Примеры шаблонов OSC</span><span class="sxs-lookup"><span data-stu-id="ec1cf-118">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="ec1cf-119">Переosc типичные последовательности вызовов</span><span class="sxs-lookup"><span data-stu-id="ec1cf-119">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)
  
- [<span data-ttu-id="ec1cf-120">Разработка поставщика с помощью XML-схемы OSC</span><span class="sxs-lookup"><span data-stu-id="ec1cf-120">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="ec1cf-121">Отладка поставщика</span><span class="sxs-lookup"><span data-stu-id="ec1cf-121">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="ec1cf-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="ec1cf-122">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="ec1cf-123">Подготовка к выпуску поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="ec1cf-123">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="ec1cf-124">См. также</span><span class="sxs-lookup"><span data-stu-id="ec1cf-124">See also</span></span>

- [<span data-ttu-id="ec1cf-125">Microsoft Outlook Social Connector 32 — бит</span><span class="sxs-lookup"><span data-stu-id="ec1cf-125">Microsoft Outlook Social Connector 32-bit</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=b638cc14-11e5-448a-b5a6-4f553ce81b94)
- [<span data-ttu-id="ec1cf-126">Обновление для Outlook Social Connector (KB983403), 32-разрядный выпуск</span><span class="sxs-lookup"><span data-stu-id="ec1cf-126">Update for Outlook Social Connector (KB983403), 32-Bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=9886faca-f1c5-4579-83e2-c872c7abc61a)
- [<span data-ttu-id="ec1cf-127">Обновление для Outlook Social Connector (KB983403), 64-разрядный выпуск</span><span class="sxs-lookup"><span data-stu-id="ec1cf-127">Update for Outlook Social Connector (KB983403), 64-bit Edition</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=72a506a7-8a91-4d56-8b27-bf3b3f58fe9a)
- [<span data-ttu-id="ec1cf-128">Outlook Social Connector 2013: Шаблоны поставщиков</span><span class="sxs-lookup"><span data-stu-id="ec1cf-128">Outlook Social Connector 2013: Provider templates</span></span>](https://code.msdn.microsoft.com/Outlook-Social-Connector-73fd8d2c)

