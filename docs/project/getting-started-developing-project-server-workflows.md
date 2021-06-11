---
title: Начало разработки рабочих процессов Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 735bbb04-a8c1-46c0-a346-42050f0ac9b1
description: Процессы управления спросом в Project Server 2013 включают в себя процессы, которые помогают управлять предложениями по проектам и анализом портфеля. В этот раздел включены статьи, показывающие, как можно создавать рабочие процессы для Project Server.
ms.openlocfilehash: 0a09022e63528f50ee4f0c8bd69bd6c34c5d8753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344473"
---
# <a name="getting-started-developing-project-server-workflows"></a><span data-ttu-id="971be-104">Начало разработки рабочих процессов Project Server</span><span class="sxs-lookup"><span data-stu-id="971be-104">Getting started developing Project Server workflows</span></span>

<span data-ttu-id="971be-105">Процессы управления спросом в Project Server 2013 включают в себя процессы, которые помогают управлять предложениями по проектам и анализом портфеля.</span><span class="sxs-lookup"><span data-stu-id="971be-105">Demand management processes in Project Server 2013 include workflows that help you manage project proposals and portfolio analyses.</span></span> <span data-ttu-id="971be-106">В этот раздел включены статьи, показывающие, как можно создавать рабочие процессы для Project Server.</span><span class="sxs-lookup"><span data-stu-id="971be-106">This section includes articles that show how to create workflows for Project Server.</span></span>
  
<span data-ttu-id="971be-107">Project Рабочий процесс Server 2013 использует платформу рабочего процесса SharePoint Server 2013, которая построена на версии 4 Windows Workflow Foundation (WF4).</span><span class="sxs-lookup"><span data-stu-id="971be-107">Project Server 2013 workflows use the SharePoint Server 2013 workflow platform, which is built on version 4 of Windows Workflow Foundation (WF4).</span></span> <span data-ttu-id="971be-108">Рабочие процессы на основе WF4 являются декларативными, что означает, что средство создания рабочего процесса сохраняет стадии, действия, условия и другие элементы рабочего процесса в код XAML, который интерпретируется во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="971be-108">WF4-based workflows are declarative, which means that the workflow design tool saves workflow stages, actions, conditions, and other elements to XAML code, which is interpreted at run-time.</span></span> <span data-ttu-id="971be-109">Вы можете использовать SharePoint Designer 2013 или Visual Studio 2012 для создания декларативных рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="971be-109">You can use either SharePoint Designer 2013 or Visual Studio 2012 to create declarative workflows.</span></span> <span data-ttu-id="971be-110">Рабочий процесс требует Workflow Manager клиент 1.0, который может быть на локальном сервере для локальных решений или на удаленном сервере для Project Online решений.</span><span class="sxs-lookup"><span data-stu-id="971be-110">A workflow requires the Workflow Manager Client 1.0 execution engine, which can be on a local server for on-premises solutions or on a remote server for Project Online solutions.</span></span>
  
<span data-ttu-id="971be-111">Вы можете использовать SharePoint Designer 2013 для создания относительно простых декларативных рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="971be-111">You can use SharePoint Designer 2013 to create relatively simple declarative workflows.</span></span> <span data-ttu-id="971be-112">Для сложных процессов и шаблонов рабочего процесса, которые можно использовать повторно, вы можете использовать Visual Studio 2012 для разработки и отлаговки рабочего процесса для Project Web App.</span><span class="sxs-lookup"><span data-stu-id="971be-112">For complex workflows, and workflow templates that can be reused, you can use Visual Studio 2012 to develop and debug workflows for Project Web App.</span></span> <span data-ttu-id="971be-113">Дополнительные сведения см. [в Project рабочих процессов с Visual Studio 2012 г.](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)</span><span class="sxs-lookup"><span data-stu-id="971be-113">For more information, see [Creating Project Workflows using Visual Studio 2012](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="971be-114">Рекомендуется разрабатывать и тестировать рабочие процессы не в рабочей, а в тестовой установке Project Server.</span><span class="sxs-lookup"><span data-stu-id="971be-114">Use a test installation of Project Server, not a production installation, to develop and test workflows.</span></span> <span data-ttu-id="971be-115">Рабочий процесс, разработанный для предзапустимых версий Project Server 2013, должен быть протестирован для версии выпуска и может быть создан заново и передислокирован.</span><span class="sxs-lookup"><span data-stu-id="971be-115">Workflows that are developed for pre-release versions of Project Server 2013 must be tested for the release version, and may have to be created again and redeployed.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="971be-116">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="971be-116">In this section</span></span>

[<span data-ttu-id="971be-117">Создание рабочего Project Server для управления запросами</span><span class="sxs-lookup"><span data-stu-id="971be-117">Create a Project Server workflow for Demand Management</span></span>](create-a-project-server-workflow-for-demand-management.md)
  
## <a name="see-also"></a><span data-ttu-id="971be-118">См. также</span><span class="sxs-lookup"><span data-stu-id="971be-118">See also</span></span>



[<span data-ttu-id="971be-119">Массовое обновление пользовательских полей и создание сайтов проектов из Project Online рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="971be-119">Bulk update custom fields and create project sites from a Project Online workflow</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)


[<span data-ttu-id="971be-120">Разработка рабочих процессов в SharePoint Designer 2013 и Visio 2013</span><span class="sxs-lookup"><span data-stu-id="971be-120">Workflow development in SharePoint Designer 2013 and Visio 2013</span></span>](https://msdn.microsoft.com/library/jj163272%28office.15%29.aspx)
  
[<span data-ttu-id="971be-121">Что нового в рабочих процессах для SharePoint 2013</span><span class="sxs-lookup"><span data-stu-id="971be-121">What's new in workflows for SharePoint 2013</span></span>](https://msdn.microsoft.com/library/jj163177.aspx)
  
[<span data-ttu-id="971be-122">Разработка рабочих процессов в SharePoint 2013 с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="971be-122">Develop SharePoint 2013 workflows using Visual Studio</span></span>](https://msdn.microsoft.com/library/jj163199.aspx)
  
[<span data-ttu-id="971be-123">Создание Project рабочих процессов с Visual Studio 2012 г.</span><span class="sxs-lookup"><span data-stu-id="971be-123">Creating Project Workflows using Visual Studio 2012</span></span>](https://blogs.msdn.com/b/project_programmability/archive/2012/11/07/creating-project-workflows-using-visual-studio-2012.aspx)
  
[<span data-ttu-id="971be-124">Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="971be-124">Windows Workflow Foundation</span></span>](https://msdn.microsoft.com/library/dd489441.aspx)
  
[<span data-ttu-id="971be-125">Введение разработчика в Windows workflow Foundation (WF) в .NET 4</span><span class="sxs-lookup"><span data-stu-id="971be-125">A developer's introduction to Windows Workflow Foundation (WF) in .NET 4</span></span>](https://msdn.microsoft.com/library/ee342461.aspx)
  
[<span data-ttu-id="971be-126">Руководство автостопщика по управлению запросами (белый документ)</span><span class="sxs-lookup"><span data-stu-id="971be-126">Hitchhiker's guide to demand management (white paper)</span></span>](https://msdn.microsoft.com/library/ff973112.aspx)

