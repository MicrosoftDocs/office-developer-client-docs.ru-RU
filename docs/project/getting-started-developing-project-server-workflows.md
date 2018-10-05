---
title: Начало разработки рабочих процессов Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Запросу, что процессы управления в Project Server 2013 включить рабочие процессы, которые помогут вам управлять предложений по проекту и анализа портфеля. В этом разделе представлены статьи, в которых показано, как для создания рабочих процессов для Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384096"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="d8b2e-104">Начало разработки рабочих процессов Project Server</span><span class="sxs-lookup"><span data-stu-id="d8b2e-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="d8b2e-105">Запросу, что процессы управления в Project Server 2013 включить рабочие процессы, которые помогут вам управлять предложений по проекту и анализа портфеля.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="d8b2e-106">В этом разделе представлены статьи, в которых показано, как для создания рабочих процессов для Project Server.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="d8b2e-107">Рабочих процессов Project Server 2013 использованию платформы рабочих процессов SharePoint Server 2013, создан на основе версии 4 Windows Workflow Foundation (WF4).</span><span class="sxs-lookup"><span data-stu-id="d8b2e-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="d8b2e-108">Рабочих процессов на основе WF4 являются декларативные, это означает, что средства создания рабочих процессов сохраняет стадии рабочего процесса, действия, условия и другие элементы кода XAML, который обрабатывается во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="d8b2e-109">Создание декларативных рабочих процессов можно использовать SharePoint Designer 2013 или Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="d8b2e-110">Рабочий процесс требует ядро выполнения 1.0 клиент диспетчера рабочих процессов, который может быть на локальном сервере для локальных решений или на удаленном сервере для Project Online решений.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="d8b2e-111">SharePoint Designer 2013 можно использовать для создания сравнительно легко декларативных рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="d8b2e-112">Для сложных рабочих процессов и шаблоны рабочих процессов, которые можно повторно использовать можно использовать Visual Studio 2012 для разработки и отладки рабочих процессов для Project Web App.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="d8b2e-113">Для получения дополнительных сведений см. [Создание рабочих процессов Project с помощью Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span><span class="sxs-lookup"><span data-stu-id="d8b2e-113">For more information, see [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d8b2e-114">Используйте пробную установку Project Server, не производственной установки для разработки и тестирования рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="d8b2e-115">Рабочие процессы, разработанных для предварительных версий Project Server 2013 должно тестироваться версии выпуска и может потребоваться создать заново и повторного развертывания.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="d8b2e-116">В этой статье</span><span class="sxs-lookup"><span data-stu-id="d8b2e-116">In this section</span></span>

[<span data-ttu-id="d8b2e-117">Создание рабочего процесса Project Server для управления запросами</span><span class="sxs-lookup"><span data-stu-id="d8b2e-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="d8b2e-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d8b2e-118">See also</span></span>



[<span data-ttu-id="d8b2e-119">Обновление настраиваемых полей в пакетном режиме и создание сайтов проектов из Project Online рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="d8b2e-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="d8b2e-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span><span class="sxs-lookup"><span data-stu-id="d8b2e-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="d8b2e-121">Что нового в рабочих процессах для SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="d8b2e-121">What's new in workflows for SharePoint 2013</span></span>](https://msdn.microsoft.com/library/jj163177.aspx)
  
[<span data-ttu-id="d8b2e-122">Разработка рабочих процессов в SharePoint 2013 с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d8b2e-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](https://msdn.microsoft.com/library/jj163199.aspx)
  
[<span data-ttu-id="d8b2e-123">Создание рабочих процессов Project, с помощью Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="d8b2e-123">Creating Project Workflows using Visual Studio 2012</span></span>](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="d8b2e-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="d8b2e-124">Windows Workflow Foundation</span></span>](https://msdn.microsoft.com/library/dd489441.aspx)
  
[<span data-ttu-id="d8b2e-125">Введение для разработчиков для Windows Workflow Foundation (WF) в .NET 4</span><span class="sxs-lookup"><span data-stu-id="d8b2e-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](https://msdn.microsoft.com/library/ee342461.aspx)
  
[<span data-ttu-id="d8b2e-126">Путеводитель по управлению запросами (технический документ)</span><span class="sxs-lookup"><span data-stu-id="d8b2e-126">Hitchhiker's guide to demand management (white paper)</span></span>](https://msdn.microsoft.com/library/ff973112.aspx)

