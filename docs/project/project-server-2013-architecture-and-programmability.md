---
title: Архитектура и программируемость Project Server 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- architecture
- platform
- Project
- Project architecture
- Project programmability
- Project Server architecture
- Project Server programmability
keywords:
- project 2013, архитектура и программируемость, программируемость, Project Server,Project 2013, преимущества EPM, архитектура и Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: В статьях этого раздела описывается общая архитектура решения enterprise Project Management (EPM), объединяющего Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413789"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="bbe17-104">Архитектура и программируемость Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="bbe17-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="bbe17-105">В статьях этого раздела описывается общая архитектура решения enterprise Project Management (EPM), объединяющего Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bbe17-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="bbe17-106">Project Server 2013 создан с помощью .NET Framework 4 и является третьим основным выпуском Project Server для обеспечения настоящей многоуровневой архитектуры.</span><span class="sxs-lookup"><span data-stu-id="bbe17-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="bbe17-107">Для облачного доступа Project Server 2013 реализует клиентскую объектную модель (CSOM) и службу OData для отчетов, которые можно использовать в веб-приложениях, мобильных приложениях и приложениях Silverlight.</span><span class="sxs-lookup"><span data-stu-id="bbe17-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="bbe17-108">Для локального приложения клиенты могут использовать службы CSOM или Project Server Interface (PSI).</span><span class="sxs-lookup"><span data-stu-id="bbe17-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="bbe17-109">Введение в архитектуру Project Server</span><span class="sxs-lookup"><span data-stu-id="bbe17-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="bbe17-110">В этом разделе описывается общая архитектура решения управления корпоративными проектами (EPM), которое объединяет Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bbe17-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="bbe17-111">Для программного доступа к Project Server следует использовать CSOM или службы PSI с интерфейсом Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="bbe17-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="bbe17-112">Интерфейс веб-службы ASMX PSI является неподготовленным в Project Server 2013, но по-прежнему работает.</span><span class="sxs-lookup"><span data-stu-id="bbe17-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="bbe17-113">PSI обеспечивает эффективный доступ с помощью наборов данных, и вы можете создавать обработчики для событий на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="bbe17-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="bbe17-114">Сама CSOM использует PSI для доступа к уровне бизнес-объектов Project Server.</span><span class="sxs-lookup"><span data-stu-id="bbe17-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="bbe17-115">Вместо четырех баз данных Project Server в Project Server 2013 используется одна база данных на уровне доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="bbe17-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="bbe17-116">Project Server 2013 полностью интегрируется с SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bbe17-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="bbe17-117">Службу приложения Project можно связывать с другими коллекциями веб-сайтов SharePoint в ферме.</span><span class="sxs-lookup"><span data-stu-id="bbe17-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="bbe17-118">Project Server может работать со списками задач SharePoint в коллекции сайтов и получать отчеты о них, а также получать полный контроль над тем, где Project Server импортирует списки задач и управляет ими как корпоративными проектами.</span><span class="sxs-lookup"><span data-stu-id="bbe17-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="bbe17-119">Project Server также использует версию 4 Windows Workflow Foundation (WF4) и добавляет действия рабочего процесса для решений управления запросами.</span><span class="sxs-lookup"><span data-stu-id="bbe17-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="bbe17-120">О многих новых функций, которые Project 2013 предоставляет разработчикам, а также о неподготовленных функций см. в статьях "Обновления для разработчиков" в [Project 2013.](updates-for-developers-in-project-2013.md)</span><span class="sxs-lookup"><span data-stu-id="bbe17-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="bbe17-121">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="bbe17-121">In this section</span></span>

<span data-ttu-id="bbe17-122">[Архитектура Project Server 2013](project-server-2013-architecture.md) описывает основные части платформы Project 2013, включая клиенты и серверы.</span><span class="sxs-lookup"><span data-stu-id="bbe17-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="bbe17-123">[В](project-server-programmability.md) этой теме обсуждаются основные функции реализации возможностей возможности extensibility Project Server 2013, настройки Project Web App и обновления приложений, построенных для предыдущих версий Project Server.</span><span class="sxs-lookup"><span data-stu-id="bbe17-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="bbe17-124">[Что PSI делает и не](what-the-psi-does-and-does-not-do.md) описывает сценарии, в которых PSI можно использовать, и перечисляет то, что PSI не может делать.</span><span class="sxs-lookup"><span data-stu-id="bbe17-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="bbe17-125">[Что CSOM делает и не](what-the-csom-does-and-does-not-do.md) описывает сценарии, в которых CSOM можно использовать, и перечисляет то, что CSOM не может делать.</span><span class="sxs-lookup"><span data-stu-id="bbe17-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="bbe17-126">Темы не освещались</span><span class="sxs-lookup"><span data-stu-id="bbe17-126">Topics not covered</span></span>

<span data-ttu-id="bbe17-127">Статьи в разделе  "Архитектура и программируемость" не документировать функции классических клиентов Project (Project Стандартный 2013 и Project профессиональный 2013) или Project Web App.</span><span class="sxs-lookup"><span data-stu-id="bbe17-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="bbe17-128">Visual Basic для приложений (VBA) доступна в редакторе Visual Basic Project Standard и Project профессиональный.</span><span class="sxs-lookup"><span data-stu-id="bbe17-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bbe17-129">См. также</span><span class="sxs-lookup"><span data-stu-id="bbe17-129">See also</span></span>
<span data-ttu-id="bbe17-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="bbe17-130"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="bbe17-131">Обновления для разработчиков в Project 2013</span><span class="sxs-lookup"><span data-stu-id="bbe17-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="bbe17-132">Начало разработки рабочих процессов Project Server</span><span class="sxs-lookup"><span data-stu-id="bbe17-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

