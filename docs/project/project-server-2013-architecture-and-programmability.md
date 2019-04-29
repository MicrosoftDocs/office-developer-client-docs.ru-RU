---
title: Архитектура и возможности программирования Project Server 2013
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
- проект 2013, архитектура и программируемость, программирование, программирование, Project Server, проект 2013, преимущества для EPM, архитектура и Project Server
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: Статьи в этом разделе описывают общую архитектуру решения по управлению корпоративными проектами (EPM), которое сочетает Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
ms.openlocfilehash: 44cd5a32b8d3de421ffe3b2d9bf0137146bc4c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413789"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="1941c-104">Архитектура и возможности программирования Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="1941c-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="1941c-105">Статьи в этом разделе описывают общую архитектуру решения по управлению корпоративными проектами (EPM), которое сочетает Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1941c-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="1941c-106">Project Server 2013 создан с помощью .NET Framework 4 и является третьим основным выпуском Project Server для реализации многоуровневой многоуровневой архитектуры.</span><span class="sxs-lookup"><span data-stu-id="1941c-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="1941c-107">Для облачного доступа Project Server 2013 реализует клиентскую объектную модель (CSOM) и службу OData для создания отчетов, которые можно использовать в веб-приложениях, мобильных приложениях и приложениях Silverlight.</span><span class="sxs-lookup"><span data-stu-id="1941c-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="1941c-108">Для локальных приложений клиенты могут использовать либо службы CSOM, либо службы интерфейса Project Server (PSI).</span><span class="sxs-lookup"><span data-stu-id="1941c-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="1941c-109">Общие сведения об архитектуре Project Server</span><span class="sxs-lookup"><span data-stu-id="1941c-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="1941c-110">В подразделах этого раздела описывается общая архитектура решения для управления корпоративными проектами (EPM), которая сочетает в себе Project профессиональный 2013, Project Server 2013, Project Web App и SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1941c-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="1941c-111">Для программного доступа к Project Server следует использовать CSOM или службы PSI с интерфейсом Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="1941c-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="1941c-112">Интерфейс веб-службы ASMX PSI является устаревшим в Project Server 2013, но по-прежнему работает.</span><span class="sxs-lookup"><span data-stu-id="1941c-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="1941c-113">PSI обеспечивает эффективный доступ с помощью наборов данных, и вы можете создавать обработчики для событий на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="1941c-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="1941c-114">CSOM сам использует PSI для доступа к уровню бизнес-объектов Project Server.</span><span class="sxs-lookup"><span data-stu-id="1941c-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="1941c-115">Вместо четырех баз данных Project Server 2013 в Project Server используется одна база данных на уровне доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="1941c-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="1941c-116">Project Server 2013 тесно интегрируется с SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1941c-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="1941c-117">Служба приложения Project может быть связана с другими семействами веб-сайтов SharePoint в ферме.</span><span class="sxs-lookup"><span data-stu-id="1941c-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="1941c-118">Project Server может работать с списками задач SharePoint в семействе веб-сайтов и сообщать о них, а также получать полный доступ, когда Project Server импортирует и управляет списками задач в качестве корпоративных проектов.</span><span class="sxs-lookup"><span data-stu-id="1941c-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="1941c-119">Project Server также использует версию 4 для Windows Workflow Foundation (WF4) и добавляет действия рабочего процесса для решений управления запросами.</span><span class="sxs-lookup"><span data-stu-id="1941c-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="1941c-120">Сведения о многочисленных новых возможностях, предоставляемых Project 2013 для разработчиков, а также об устаревших функциях можно узнать [в статье Updates for Developers in Project 2013](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="1941c-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="1941c-121">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="1941c-121">In this section</span></span>

<span data-ttu-id="1941c-122">[Архитектура Project Server 2013](project-server-2013-architecture.md) описывает основные части платформы Project 2013, в том числе клиенты и серверы.</span><span class="sxs-lookup"><span data-stu-id="1941c-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="1941c-123">[Программирование Project Server](project-server-programmability.md) обсуждает основные функции расширения project Server 2013, настройка Project Web App и обновление приложений, созданных для предыдущих версий Project Server.</span><span class="sxs-lookup"><span data-stu-id="1941c-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="1941c-124">[Что делает PSI и не выполняет](what-the-psi-does-and-does-not-do.md) описание сценариев, в которых можно использовать PSI, и список действий, которые не могут выполняться в PSI.</span><span class="sxs-lookup"><span data-stu-id="1941c-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="1941c-125">[Действия, выполняемЫЕ CSOM,](what-the-csom-does-and-does-not-do.md) не описывают сценарии, в которых можно использовать CSOM, и перечислены действия, которые не могут делать CSOM.</span><span class="sxs-lookup"><span data-stu-id="1941c-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="1941c-126">Неохваченные темы</span><span class="sxs-lookup"><span data-stu-id="1941c-126">Topics not covered</span></span>

<span data-ttu-id="1941c-127">В статьях раздела *архитектура и программирование* не задокументированы компоненты клиентских настольНых компьютеров Project (project стандартный 2013 и project профессиональный 2013) или Project Web App.</span><span class="sxs-lookup"><span data-stu-id="1941c-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="1941c-128">Справка по Visual Basic для приложений (VBA) доступна в редакторе Visual Basic в Project Standard и Project профессиональный.</span><span class="sxs-lookup"><span data-stu-id="1941c-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1941c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="1941c-129">See also</span></span>
<span data-ttu-id="1941c-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="1941c-130"></span></span>

- [<span data-ttu-id="1941c-131">Обновления для разработчиков в Project 2013</span><span class="sxs-lookup"><span data-stu-id="1941c-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="1941c-132">Начало разработки рабочих процессов Project Server</span><span class="sxs-lookup"><span data-stu-id="1941c-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

