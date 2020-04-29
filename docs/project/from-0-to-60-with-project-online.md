---
title: Быстрое начало разработки для Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Разработчик приложений может настроить сайт Project Online (SharePoint Hosted), используя автономные приложения и/или надстройки Project. Множество приложений может быть в диапазоне от требований к адресации, задействованных в проекте, для функций поддержки PMO, таких как следующие:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344410"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="6046b-103">Быстрое начало разработки для Project Online</span><span class="sxs-lookup"><span data-stu-id="6046b-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="6046b-104">Разработчик приложений может настроить сайт Project Online (SharePoint Hosted), используя автономные приложения и/или надстройки Project. Множество приложений может быть в диапазоне от требований к адресации, задействованных в проекте, для функций поддержки PMO, таких как следующие:</span><span class="sxs-lookup"><span data-stu-id="6046b-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="6046b-105">Упрощенная запись данных табеля для работников</span><span class="sxs-lookup"><span data-stu-id="6046b-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="6046b-106">Утверждение эффективного табеля для руководителей</span><span class="sxs-lookup"><span data-stu-id="6046b-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="6046b-107">Обзор разрешений (закупаемой продукции и состояния), необходимых для проекта</span><span class="sxs-lookup"><span data-stu-id="6046b-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="6046b-108">Проверка состояния и работоспособности активных проектов</span><span class="sxs-lookup"><span data-stu-id="6046b-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="6046b-109">Отчет о проблемах</span><span class="sxs-lookup"><span data-stu-id="6046b-109">Issues report</span></span>
- <span data-ttu-id="6046b-110">Изменение отчета о состоянии управления</span><span class="sxs-lookup"><span data-stu-id="6046b-110">Change Management Status report</span></span>
    
<span data-ttu-id="6046b-111">Project Online включает поддержку API для следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="6046b-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="6046b-112">Для размещенной надстройки Project (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="6046b-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="6046b-113">Код (JavaScript, HTML, CSS), размещенный в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6046b-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="6046b-114">Ресурсы, загруженные в браузер и выполняемые в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6046b-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="6046b-115">Бизнес-логика в JavaScript</span><span class="sxs-lookup"><span data-stu-id="6046b-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="6046b-116">Доступ к данным, хранящимся и хранящимся в Project Online или SharePoint (но не ограничен):</span><span class="sxs-lookup"><span data-stu-id="6046b-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="6046b-117">настраиваемые поля;</span><span class="sxs-lookup"><span data-stu-id="6046b-117">Custom fields</span></span>  
  - <span data-ttu-id="6046b-118">Списки</span><span class="sxs-lookup"><span data-stu-id="6046b-118">Lists</span></span>
    
- <span data-ttu-id="6046b-119">Для надстройки, размещаемой у поставщика Project (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="6046b-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="6046b-120">Код, который существует на сайте, который является внешним по отношению к сайту Project Online</span><span class="sxs-lookup"><span data-stu-id="6046b-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="6046b-121">Внешний сайт, который может быть (но не ограничен):</span><span class="sxs-lookup"><span data-stu-id="6046b-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="6046b-122">Другой сайт SharePoint</span><span class="sxs-lookup"><span data-stu-id="6046b-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="6046b-123">Веб-приложение или служба, созданные на любой платформе</span><span class="sxs-lookup"><span data-stu-id="6046b-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="6046b-124">Внешний сайт содержит бизнес-логику</span><span class="sxs-lookup"><span data-stu-id="6046b-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="6046b-125">Браузер перенаправляется из Project Online на внешний сайт с маркерами доступа в Project Online</span><span class="sxs-lookup"><span data-stu-id="6046b-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="6046b-126">Внешний сайт может совершать вызовы в SharePoint и Project Online</span><span class="sxs-lookup"><span data-stu-id="6046b-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="6046b-127">Для внешней или автономной надстройки:</span><span class="sxs-lookup"><span data-stu-id="6046b-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="6046b-128">Пользователь выполняет приложение на своем устройстве</span><span class="sxs-lookup"><span data-stu-id="6046b-128">User executes an application on their device</span></span>
  - <span data-ttu-id="6046b-129">Приложение выполняет проверку подлинности и вызывает API Project Online напрямую</span><span class="sxs-lookup"><span data-stu-id="6046b-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="6046b-130">Тип приложения</span><span class="sxs-lookup"><span data-stu-id="6046b-130">Type of application</span></span>|<span data-ttu-id="6046b-131">Реализация API</span><span class="sxs-lookup"><span data-stu-id="6046b-131">API implementation</span></span>|<span data-ttu-id="6046b-132">Целевая среда</span><span class="sxs-lookup"><span data-stu-id="6046b-132">Target environment</span></span>|<span data-ttu-id="6046b-133">Примеры приложений</span><span class="sxs-lookup"><span data-stu-id="6046b-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6046b-134">Размещено в проекте</span><span class="sxs-lookup"><span data-stu-id="6046b-134">Project hosted</span></span>  <br/> |<span data-ttu-id="6046b-135">JSOM (объектная модель скрипта Java)</span><span class="sxs-lookup"><span data-stu-id="6046b-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="6046b-136">REST</span><span class="sxs-lookup"><span data-stu-id="6046b-136">REST</span></span>  <br/> |<span data-ttu-id="6046b-137">Браузер</span><span class="sxs-lookup"><span data-stu-id="6046b-137">Browser</span></span>  <br/> |<span data-ttu-id="6046b-138">Запись табеля</span><span class="sxs-lookup"><span data-stu-id="6046b-138">Timecard entry</span></span>  <br/> <span data-ttu-id="6046b-139">Утверждение табеля</span><span class="sxs-lookup"><span data-stu-id="6046b-139">Timecard approval</span></span>  <br/> <span data-ttu-id="6046b-140">Состояние проекта</span><span class="sxs-lookup"><span data-stu-id="6046b-140">Project Status</span></span>  <br/> <span data-ttu-id="6046b-141">Отчет о проблемах</span><span class="sxs-lookup"><span data-stu-id="6046b-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="6046b-142">Размещенный у поставщика проект</span><span class="sxs-lookup"><span data-stu-id="6046b-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="6046b-143">Клиентская библиотека CSOM</span><span class="sxs-lookup"><span data-stu-id="6046b-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="6046b-144">Веб-сайт или приложение Azure</span><span class="sxs-lookup"><span data-stu-id="6046b-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="6046b-145">Среда, отличная от Windows (лампа и т. д.)</span><span class="sxs-lookup"><span data-stu-id="6046b-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="6046b-146">Средство проверки внешних расписаний</span><span class="sxs-lookup"><span data-stu-id="6046b-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="6046b-147">Средство импорта проектов</span><span class="sxs-lookup"><span data-stu-id="6046b-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="6046b-148">Внешний или автономный</span><span class="sxs-lookup"><span data-stu-id="6046b-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="6046b-149">REST</span><span class="sxs-lookup"><span data-stu-id="6046b-149">REST</span></span>  <br/> <span data-ttu-id="6046b-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="6046b-150">CSOM</span></span>  <br/> |<span data-ttu-id="6046b-151">REST — любая платформа</span><span class="sxs-lookup"><span data-stu-id="6046b-151">REST - any platform</span></span>  <br/> <span data-ttu-id="6046b-152">CSOM — любая платформа, поддерживаемая .NET</span><span class="sxs-lookup"><span data-stu-id="6046b-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="6046b-153">Запись табеля</span><span class="sxs-lookup"><span data-stu-id="6046b-153">Timecard entry</span></span>  <br/> <span data-ttu-id="6046b-154">Миграция проектов на новый сайт</span><span class="sxs-lookup"><span data-stu-id="6046b-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="6046b-155">Изменение состояния управления.</span><span class="sxs-lookup"><span data-stu-id="6046b-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="6046b-156">Что нужно сделать, чтобы начать разработку приложений для Project Online?</span><span class="sxs-lookup"><span data-stu-id="6046b-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="6046b-157">Общие элементы, необходимые для разработки приложений Project Online, — это учетная запись Project Online и тестовые данные проектов и связанные с проектом сведения, включающие назначения, задачи, ресурсы и настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="6046b-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="6046b-158">Среда разработки также необходима, но особенности среды разработки зависят от типа приложения и интерфейса API, необходимого для приложения.</span><span class="sxs-lookup"><span data-stu-id="6046b-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="6046b-159">В следующих разделах описываются потребности разработки для трех интерфейсов API.</span><span class="sxs-lookup"><span data-stu-id="6046b-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="6046b-160">В справочной документации описывается объектная модель, которая является общей для всех трех интерфейсов, а также сопоставление объектов, которое показывает отношения между компонентами объектной модели.</span><span class="sxs-lookup"><span data-stu-id="6046b-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="6046b-161">Среда разработки надстройки, размещаемой в проекте</span><span class="sxs-lookup"><span data-stu-id="6046b-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="6046b-162">Размещенная надстройка — это надстройка, которая размещается на сервере и загружается в браузер для выполнения среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="6046b-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="6046b-163">Размещаемые надстройки могут использовать интерфейсы JSOM или REST и написаны на JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6046b-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="6046b-164">Project Online предоставляет ссылки на библиотеку JSOM для выполнения среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="6046b-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="6046b-165">Если разработка разрабатывается на платформе Windows, необходимы следующие ресурсы:</span><span class="sxs-lookup"><span data-stu-id="6046b-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="6046b-166">Visual Studio 2015 (предпочтительно) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="6046b-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="6046b-167">Средства разработки Office для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6046b-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="6046b-168">Язык JavaScript</span><span class="sxs-lookup"><span data-stu-id="6046b-168">JavaScript language</span></span>
    
<span data-ttu-id="6046b-169">Посетите https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages пример приложения.</span><span class="sxs-lookup"><span data-stu-id="6046b-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="6046b-170">Загрузить и запустить пример можно несколькими простыми действиями:</span><span class="sxs-lookup"><span data-stu-id="6046b-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="6046b-171">Загрузка и открытие примера приложения</span><span class="sxs-lookup"><span data-stu-id="6046b-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="6046b-172">Обновление SiteURL в окне "Свойства"</span><span class="sxs-lookup"><span data-stu-id="6046b-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="6046b-173">Project Online проверяет как область приложения надстройки, так и разрешения пользователя, чтобы управлять доступом к сведениям на узле Project Online.</span><span class="sxs-lookup"><span data-stu-id="6046b-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="6046b-174">Если доступ явным образом запрещен в обоих или обоих параметрах, Project Online запрещает доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="6046b-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="6046b-175">В противном случае предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="6046b-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="6046b-176">Включите загрузку [неопубликованных приложений](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на сайте.</span><span class="sxs-lookup"><span data-stu-id="6046b-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="6046b-177">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="6046b-177">Build the project.</span></span>
    
5. <span data-ttu-id="6046b-178">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="6046b-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="6046b-179">Среда разработки надстройки, размещаемой у поставщика проекта</span><span class="sxs-lookup"><span data-stu-id="6046b-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="6046b-180">Надстройки, размещаемые у поставщика, — это приложения, написанные и размещенные на любой веб-платформе.</span><span class="sxs-lookup"><span data-stu-id="6046b-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="6046b-181">Они могут подключаться и выполнять операции с данными с помощью API REST (или CSOM для платформ Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="6046b-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="6046b-182">Для разработки можно использовать любой язык и среду, поддерживающие интерфейс REST.</span><span class="sxs-lookup"><span data-stu-id="6046b-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="6046b-183">Пример среды разработки Windows для этого типа приложения состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="6046b-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="6046b-184">Visual Studio 2015 (предпочтительно) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="6046b-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="6046b-185">Средства разработки Microsoft Office для Visual Studio (поставляется с Visual Studio 2015 Professional и Enterprise Editions)</span><span class="sxs-lookup"><span data-stu-id="6046b-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="6046b-186">.NET Framework 4,0 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="6046b-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="6046b-187">[Пакет CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для вызовов CSOM)</span><span class="sxs-lookup"><span data-stu-id="6046b-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="6046b-188">Язык программирования, например C #</span><span class="sxs-lookup"><span data-stu-id="6046b-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="6046b-189">Посетите https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations страницу Работа с примерами сценариев.</span><span class="sxs-lookup"><span data-stu-id="6046b-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="6046b-190">Пример можно выполнить несколькими шагами:</span><span class="sxs-lookup"><span data-stu-id="6046b-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="6046b-191">Загрузка и открытие примера приложения</span><span class="sxs-lookup"><span data-stu-id="6046b-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="6046b-192">Обновление SiteURL в окне "Свойства"</span><span class="sxs-lookup"><span data-stu-id="6046b-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="6046b-193">Project Online проверяет как область приложения надстройки, так и разрешения пользователя, чтобы управлять доступом к сведениям на узле Project Online.</span><span class="sxs-lookup"><span data-stu-id="6046b-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="6046b-194">Если доступ явным образом запрещен в обоих или обоих параметрах, Project Online запрещает доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="6046b-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="6046b-195">В противном случае предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="6046b-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="6046b-196">Включите загрузку [неопубликованных приложений](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на сайте.</span><span class="sxs-lookup"><span data-stu-id="6046b-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="6046b-197">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="6046b-197">Build the project.</span></span>
    
5. <span data-ttu-id="6046b-198">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="6046b-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="6046b-199">Внешняя или автономная среда разработки приложений</span><span class="sxs-lookup"><span data-stu-id="6046b-199">External/standalone application development environment</span></span>

<span data-ttu-id="6046b-200">Автономное приложение может вызывать Project Online с помощью клиентской объектной модели (CSOM) или REST для связи с Project Online для создания, получения, обновления и удаления данных, находящихся на сервере.</span><span class="sxs-lookup"><span data-stu-id="6046b-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="6046b-201">Это автономное клиентское приложение, зависящее от уровня доступа пользователя, который необходимо запустить.</span><span class="sxs-lookup"><span data-stu-id="6046b-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="6046b-202">Пример среды разработки Windows для этого типа приложения состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="6046b-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="6046b-203">Visual Studio 2015 (предпочтительно) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="6046b-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="6046b-204">Средства разработки Microsoft Office для Visual Studio (поставляется с Visual Studio 2015 Professional и Enterprise Editions)</span><span class="sxs-lookup"><span data-stu-id="6046b-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="6046b-205">.NET Framework 4,0 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="6046b-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="6046b-206">[Пакет CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для вызовов CSOM)</span><span class="sxs-lookup"><span data-stu-id="6046b-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="6046b-207">Язык программирования, например C #</span><span class="sxs-lookup"><span data-stu-id="6046b-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="6046b-208">Посетите https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields пример приложения.</span><span class="sxs-lookup"><span data-stu-id="6046b-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="6046b-209">Пример можно выполнить несколькими шагами:</span><span class="sxs-lookup"><span data-stu-id="6046b-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="6046b-210">Скачать пример приложения</span><span class="sxs-lookup"><span data-stu-id="6046b-210">Download the sample application</span></span>
    
2. <span data-ttu-id="6046b-211">Выполните два изменения, чтобы получить доступ к сайту Project Online — имя сайта, учетная запись пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="6046b-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="6046b-212">Убедитесь, что у пользователя есть доступ ко всем проектам.</span><span class="sxs-lookup"><span data-stu-id="6046b-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="6046b-213">В Project Online для управления доступом к данным в хранилище данных используются разрешения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6046b-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="6046b-214">Добавьте сборку SharePoint в ссылки с помощью консоли диспетчера пакетов NuGet, доступной в консоли NuGet, введя следующую команду в консоли NuGet:</span><span class="sxs-lookup"><span data-stu-id="6046b-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="6046b-215">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="6046b-215">Build the project.</span></span>
    
5. <span data-ttu-id="6046b-216">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="6046b-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="6046b-217">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6046b-217">Next steps</span></span>

<span data-ttu-id="6046b-218">Каждый пример приложения содержит статью, поясняющую основные аспекты работы с API отдельных проектов.</span><span class="sxs-lookup"><span data-stu-id="6046b-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="6046b-219">В приведенном ниже списке представлены статьи, а также несколько статей, описывающих связи между сущностями, сведения о системе запросов и доступ к настраиваемым полям.</span><span class="sxs-lookup"><span data-stu-id="6046b-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="6046b-220">Разработка приложения Project Online с помощью клиентской объектной модели</span><span class="sxs-lookup"><span data-stu-id="6046b-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="6046b-221">Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="6046b-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="6046b-222">Доступ к корпоративным настраиваемым полям Project Online</span><span class="sxs-lookup"><span data-stu-id="6046b-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="6046b-223">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6046b-223">See also</span></span>

<span data-ttu-id="6046b-224">Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="6046b-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

