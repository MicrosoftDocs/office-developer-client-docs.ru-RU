---
title: Задачи программирования Project
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: ac5544e7-ff7a-4af5-ac1b-33a49bc6be0d
description: В этом разделе представлены каким-либо образом toarticles, показано, как использовать библиотеку JavaScript для клиентской объектной модели (CSOM) и выполнять другие задачи по программированию для Project Server 2013 и Project Online. Задачи программирования примеры создания приложения с размещением в SharePoint Project Server, создание рабочих процессов для управления запросами. программирование приложений Project Server с помощью Windows Communication Foundation (WCF); Настройка ленты в Project Web App; Создание веб-частей Project Server; Создание обработчиков событий Project Server и удаленные приемники событий; и обновление настраиваемых полей и создание сайтов проектов для Project Online в пакетном режиме.
ms.openlocfilehash: 79ff301b825b4eea073d5d1896e27be9e0090ba6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813058"
---
# <a name="project-programming-tasks"></a><span data-ttu-id="0740d-104">Задачи программирования Project</span><span class="sxs-lookup"><span data-stu-id="0740d-104">Project programming tasks</span></span>

<span data-ttu-id="0740d-105">В этом разделе представлены некоторые «инструкции» статьи, которые показывают, как использовать библиотеку JavaScript для клиентской объектной модели (CSOM) и выполнять другие задачи по программированию для Project Server 2013 и Project Online.</span><span class="sxs-lookup"><span data-stu-id="0740d-105">This section includes some "how-to" articles that show how to use the JavaScript library for the client-side object model (CSOM), and perform other programming tasks for Project Server 2013 and Project Online.</span></span> <span data-ttu-id="0740d-106">Задачи программирования примеры создания приложения с размещением в SharePoint Project Server, создание рабочих процессов для управления запросами. программирование приложений Project Server с помощью Windows Communication Foundation (WCF); Настройка ленты в Project Web App; Создание веб-частей Project Server; Создание обработчиков событий Project Server и удаленные приемники событий; и обновление настраиваемых полей и создание сайтов проектов для Project Online в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="0740d-106">Examples of programming tasks include creating a SharePoint-hosted Project Server app, creating workflows for demand management; programming Project Server applications with the Windows Communication Foundation (WCF); customizing the Project Web App ribbon; creating Project Server Web Parts; creating Project Server event handlers and remote event receivers; and bulk updating custom fields and creating project sites for Project Online.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0740d-107">Сведения о программировании с помощью элемента управления JS Grid видеть [JS Grid Control](http://msdn.microsoft.com/en-us/library/ee535898%28office.14%29.aspx) в ссылке на разработчика SharePoint 2010.</span><span class="sxs-lookup"><span data-stu-id="0740d-107">For information about programming with the JS Grid control, see [JS Grid Control](http://msdn.microsoft.com/en-us/library/ee535898%28office.14%29.aspx) in the SharePoint 2010 developer reference.</span></span> <span data-ttu-id="0740d-108">Справочник по управляемым кодом в разделе [Microsoft.SharePoint.JSGrid пространство имен](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0740d-108">For the managed code reference, see [Microsoft.SharePoint.JSGrid Namespace](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.jsgrid%28Office.15%29.aspx).</span></span> <span data-ttu-id="0740d-109">Веб-элементов управления JS Grid [JSGrid](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="0740d-109">For the JS Grid control web controls, see [JSGrid class](http://msdn.microsoft.com/en-us/library/microsoft.sharepoint.webcontrols.jsgrid%28Office.15%29.aspx).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0740d-110">В этой статье</span><span class="sxs-lookup"><span data-stu-id="0740d-110">In this section</span></span>

[<span data-ttu-id="0740d-111">Начало разработки рабочих процессов Project Server</span><span class="sxs-lookup"><span data-stu-id="0740d-111">Getting started developing Project Server workflows</span></span>](getting-started-developing-project-server-workflows.md)
  
[<span data-ttu-id="0740d-112">Пакетное обновление настраиваемых полей и создание сайтов проектов из рабочего процесса в Project Online</span><span class="sxs-lookup"><span data-stu-id="0740d-112">Bulk update custom fields and create project sites from a workflow in Project Online</span></span>](bulk-update-custom-fields-and-create-project-sites-from-workflow-in-project.md)
  
[<span data-ttu-id="0740d-113">Создание, получение, обновление и удаление проектов с помощью объектной модели Project Server JavaScript</span><span class="sxs-lookup"><span data-stu-id="0740d-113">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)
  
<span data-ttu-id="0740d-114">[Надстройка создание сервера Project Server размещенных в SharePoint](create-a-sharepoint-hosted-project-server-add-in.md) : включает раздел о том, как изменение ленты Project Web App</span><span class="sxs-lookup"><span data-stu-id="0740d-114">[Create a SharePoint-hosted Project Server add-in](create-a-sharepoint-hosted-project-server-add-in.md) : includes a section on how to modify the Project Web App ribbon</span></span> 
  
## <a name="reference"></a><span data-ttu-id="0740d-115">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="0740d-115">Reference</span></span>

[<span data-ttu-id="0740d-116">Справочный обзор PSI Project</span><span class="sxs-lookup"><span data-stu-id="0740d-116">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
  
## <a name="see-also"></a><span data-ttu-id="0740d-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0740d-117">See also</span></span>



[<span data-ttu-id="0740d-118">Клиентская объектная модель (CSOM) для Project 2013</span><span class="sxs-lookup"><span data-stu-id="0740d-118">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)

