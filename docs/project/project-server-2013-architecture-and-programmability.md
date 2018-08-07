---
title: Архитектура Project Server 2013 и Программируемость
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
- преимущества архитектуры и программирования, программирования, Project Server, Project 2013 для EPM, архитектуры и Project Server, Project 2013
localization_priority: Normal
ms.assetid: 9ea3b3c1-fb90-454a-b8e6-abc44fca663d
description: В статьях этого раздела описывается общую архитектуру решения Enterprise Project Management (EPM), который объединяет Project Professional 2013, Project Server 2013, Project Web App и SharePoint Server 2013.
ms.openlocfilehash: 6b5ab94968dbb996a370e0e5abb89813f5e41ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813062"
---
# <a name="project-server-2013-architecture-and-programmability"></a><span data-ttu-id="06ef7-104">Архитектура Project Server 2013 и Программируемость</span><span class="sxs-lookup"><span data-stu-id="06ef7-104">Project Server 2013 architecture and programmability</span></span>

<span data-ttu-id="06ef7-105">В статьях этого раздела описывается общую архитектуру решения Enterprise Project Management (EPM), который объединяет Project Professional 2013, Project Server 2013, Project Web App и SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06ef7-105">The articles in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="06ef7-106">Project Server 2013, созданных с помощью .NET Framework 4 и — это третий основной версии Project Server для обеспечения true многоуровневой архитектуре.</span><span class="sxs-lookup"><span data-stu-id="06ef7-106">Project Server 2013 is built with the .NET Framework 4 and is the third major release of Project Server to provide a true multitier architecture.</span></span> <span data-ttu-id="06ef7-107">Для доступа к облачных Project Server 2013 реализует клиентской объектной модели (CSOM) и службе OData для создания отчетов, который может использоваться веб-приложений, мобильных приложений и приложений Silverlight.</span><span class="sxs-lookup"><span data-stu-id="06ef7-107">For cloud access, Project Server 2013 implements a client-side object model (CSOM) and an OData service for reporting that can be used in web applications, mobile applications, and Silverlight applications.</span></span> <span data-ttu-id="06ef7-108">Для приложений в локальной клиенты могут использовать CSOM или службы интерфейса Project Server (PSI).</span><span class="sxs-lookup"><span data-stu-id="06ef7-108">For applications on-premises, clients can use either the CSOM or the Project Server Interface (PSI) services.</span></span> 
  
## <a name="introduction-to-project-server-architecture"></a><span data-ttu-id="06ef7-109">Общие сведения об архитектуре Project Server</span><span class="sxs-lookup"><span data-stu-id="06ef7-109">Introduction to Project Server architecture</span></span>

<span data-ttu-id="06ef7-110">В этом разделе описываются общую архитектуру решения Enterprise Project Management (EPM), который объединяет Project Professional 2013, Project Server 2013, Project Web App и SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06ef7-110">The topics in this section describe the overall architecture of the Enterprise Project Management (EPM) solution, which combines Project Professional 2013, Project Server 2013, Project Web App, and SharePoint Server 2013.</span></span>
  
<span data-ttu-id="06ef7-111">Для программного доступа к серверу Project Server с помощью интерфейса Windows Communication Foundation (WCF) следует использовать службы PSI или CSOM.</span><span class="sxs-lookup"><span data-stu-id="06ef7-111">For programmatic access to Project Server, you should use either the CSOM or the PSI services with the Windows Communication Foundation (WCF) interface.</span></span> <span data-ttu-id="06ef7-112">Интерфейс веб-службы ASMX из PSI рекомендуется использовать в Project Server 2013, но по-прежнему работает.</span><span class="sxs-lookup"><span data-stu-id="06ef7-112">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but still works.</span></span> <span data-ttu-id="06ef7-113">PSI включает эффективного доступа с помощью наборов данных и можно создать обработчики для событий на сервере.</span><span class="sxs-lookup"><span data-stu-id="06ef7-113">The PSI enables efficient access by using datasets and you can create handlers for server-side events.</span></span> <span data-ttu-id="06ef7-114">CSOM самого использует PSI для доступа к бизнес-объектов Project Server уровне.</span><span class="sxs-lookup"><span data-stu-id="06ef7-114">The CSOM itself uses the PSI to access the Project Server business object layer.</span></span> <span data-ttu-id="06ef7-115">Вместо четырех баз данных Project Server Project Server 2013 использует одну базу данных в уровень доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="06ef7-115">Instead of four Project Server databases, Project Server 2013 uses a single database in the data access layer.</span></span>
  
<span data-ttu-id="06ef7-116">Project Server 2013 глубоко интегрированы с SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06ef7-116">Project Server 2013 integrates deeply with SharePoint Server 2013.</span></span> <span data-ttu-id="06ef7-117">Служба приложения Project может быть связан с другим семействам сайтов SharePoint в ферме.</span><span class="sxs-lookup"><span data-stu-id="06ef7-117">The Project Application Service can be associated with other SharePoint site collections in the farm.</span></span> <span data-ttu-id="06ef7-118">Project Server можно работать с и создание отчетов по SharePoint, списки задач в семейства веб-сайтов и может также получить полный доступ, где Project Server импортирует и управляет списки задач как корпоративных проектов.</span><span class="sxs-lookup"><span data-stu-id="06ef7-118">Project Server can operate with and report on SharePoint task lists in the site collection, and can also get full control where Project Server imports and manages the task lists as enterprise projects.</span></span> <span data-ttu-id="06ef7-119">Project Server также использует версии 4 Windows Workflow Foundation (WF4) и добавляет действий рабочего процесса для решений по управлению запросами.</span><span class="sxs-lookup"><span data-stu-id="06ef7-119">Project Server also uses version 4 of the Windows Workflow Foundation (WF4) and adds workflow activities for Demand Management solutions.</span></span>
  
<span data-ttu-id="06ef7-120">Описание множество новых функций, предоставляемых Project 2013 для разработчиков и компонентов, которые поддерживаются посетите страницу [обновления в Project 2013 для разработчиков](updates-for-developers-in-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="06ef7-120">For a discussion of the many new features that Project 2013 provides for developers, and of the features that are deprecated, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="06ef7-121">В этой статье</span><span class="sxs-lookup"><span data-stu-id="06ef7-121">In this section</span></span>

<span data-ttu-id="06ef7-122">[Архитектура Project Server 2013](project-server-2013-architecture.md) описывает основные части платформы Project 2013, включая клиенты и серверы.</span><span class="sxs-lookup"><span data-stu-id="06ef7-122">[Project Server 2013 architecture](project-server-2013-architecture.md) describes the major parts of the Project 2013 platform, including the clients and servers.</span></span> 
  
<span data-ttu-id="06ef7-123">[Возможность программирования Project Server](project-server-programmability.md) рассматриваются возможности основных расширяемости Project Server 2013 Настройка Project Web App и обновление приложения, созданные для предыдущих версий Project Server.</span><span class="sxs-lookup"><span data-stu-id="06ef7-123">[Project Server programmability](project-server-programmability.md) discusses the main extensibility features of Project Server 2013, customization of Project Web App, and upgrading applications that are built for previous Project Server versions.</span></span> 
  
<span data-ttu-id="06ef7-124">[Что PSI делает и не имеет](what-the-psi-does-and-does-not-do.md) описаны сценарии использования PSI и перечислены возможности, которые не PSI.</span><span class="sxs-lookup"><span data-stu-id="06ef7-124">[What the PSI does and does not do](what-the-psi-does-and-does-not-do.md) describes scenarios where the PSI can be used and lists things that the PSI cannot do.</span></span> 
  
<span data-ttu-id="06ef7-125">[CSOM что делает и не поддерживает](what-the-csom-does-and-does-not-do.md) описаны сценарии, где можно использовать CSOM и перечислены возможности, которые не CSOM.</span><span class="sxs-lookup"><span data-stu-id="06ef7-125">[What the CSOM does and does not do](what-the-csom-does-and-does-not-do.md) describes scenarios where the CSOM can be used and lists things that the CSOM cannot do.</span></span> 
  
### <a name="topics-not-covered"></a><span data-ttu-id="06ef7-126">Темы не охватывают</span><span class="sxs-lookup"><span data-stu-id="06ef7-126">Topics not covered</span></span>

<span data-ttu-id="06ef7-127">Статьи в разделе *архитектуры и программирования* свойства проекта настольных клиентов (стандартный 2013 Project и Project Professional 2013) или Project Web App не документов.</span><span class="sxs-lookup"><span data-stu-id="06ef7-127">The articles in the  *Architecture and programmability*  section do not document features of the Project desktop clients (Project Standard 2013 and Project Professional 2013) or Project Web App.</span></span> 
  
<span data-ttu-id="06ef7-128">Visual Basic для приложений (VBA) Справка доступна в редакторе Visual Basic в Project Стандартный и Project Professional.</span><span class="sxs-lookup"><span data-stu-id="06ef7-128">Visual Basic for Applications (VBA) help is available in the Visual Basic editor within Project Standard and Project Professional.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06ef7-129">См. также</span><span class="sxs-lookup"><span data-stu-id="06ef7-129">See also</span></span>
<span data-ttu-id="06ef7-130"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="06ef7-130"></span></span>

- [<span data-ttu-id="06ef7-131">Обновления для разработчиков в Project 2013</span><span class="sxs-lookup"><span data-stu-id="06ef7-131">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md)
    
- [<span data-ttu-id="06ef7-132">Начало разработки рабочих процессов Project Server</span><span class="sxs-lookup"><span data-stu-id="06ef7-132">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
    

