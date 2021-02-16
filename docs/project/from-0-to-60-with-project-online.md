---
title: Быстрое начало разработки для Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Разработчик приложений может настраивать сайт Project Online (с хостингом SharePoint) с помощью автономных приложений и/или надстройки Project. Существует множество приложений, которые могут быть в диапазоне от решения потребностей тех, кто участвует в проекте, до функций поддержки PMO, таких как любое из следующих:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344410"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="0345d-103">Быстрое начало разработки для Project Online</span><span class="sxs-lookup"><span data-stu-id="0345d-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="0345d-104">Разработчик приложений может настраивать сайт Project Online (с хостингом SharePoint) с помощью автономных приложений и/или надстройки Project. Существует множество приложений, которые могут быть в диапазоне от решения потребностей тех, кто участвует в проекте, до функций поддержки PMO, таких как любое из следующих:</span><span class="sxs-lookup"><span data-stu-id="0345d-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="0345d-105">Упрощенная запись данных системы времени для сотрудников</span><span class="sxs-lookup"><span data-stu-id="0345d-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="0345d-106">Эффективное утверждение систем времени для руководителей</span><span class="sxs-lookup"><span data-stu-id="0345d-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="0345d-107">Надзор за разрешениями (закупками и состоянием), необходимыми для проекта</span><span class="sxs-lookup"><span data-stu-id="0345d-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="0345d-108">Проверка состояния и состояния активных проектов</span><span class="sxs-lookup"><span data-stu-id="0345d-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="0345d-109">Отчет о проблемах</span><span class="sxs-lookup"><span data-stu-id="0345d-109">Issues report</span></span>
- <span data-ttu-id="0345d-110">Отчет о состоянии управления изменениями</span><span class="sxs-lookup"><span data-stu-id="0345d-110">Change Management Status report</span></span>
    
<span data-ttu-id="0345d-111">Project Online включает поддержку API для реализации следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="0345d-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="0345d-112">Для надстройки, которая находится в Project (SharePoint):</span><span class="sxs-lookup"><span data-stu-id="0345d-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="0345d-113">Код (JavaScript, HTML, CSS), который находится в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0345d-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="0345d-114">Ресурсы, загруженные в браузер и выполненные в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="0345d-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="0345d-115">Бизнес-логика в JavaScript</span><span class="sxs-lookup"><span data-stu-id="0345d-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="0345d-116">Доступ к данным, хранимым в Project Online или SharePoint, например (но не ограничивается):</span><span class="sxs-lookup"><span data-stu-id="0345d-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="0345d-117">настраиваемые поля;</span><span class="sxs-lookup"><span data-stu-id="0345d-117">Custom fields</span></span>  
  - <span data-ttu-id="0345d-118">Списки</span><span class="sxs-lookup"><span data-stu-id="0345d-118">Lists</span></span>
    
- <span data-ttu-id="0345d-119">Для надстройки Project (SharePoint), которая находится у поставщика:</span><span class="sxs-lookup"><span data-stu-id="0345d-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="0345d-120">Код, который существует на сайте, внешнем от сайта Project Online</span><span class="sxs-lookup"><span data-stu-id="0345d-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="0345d-121">Внешний сайт, который может быть (но не ограничен):</span><span class="sxs-lookup"><span data-stu-id="0345d-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="0345d-122">Другой сайт SharePoint</span><span class="sxs-lookup"><span data-stu-id="0345d-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="0345d-123">Веб-приложение или служба, построенные на любой платформе</span><span class="sxs-lookup"><span data-stu-id="0345d-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="0345d-124">Внешний сайт содержит бизнес-логику</span><span class="sxs-lookup"><span data-stu-id="0345d-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="0345d-125">Браузер перенаправляется из Project Online на внешний сайт с маркерами доступа к Project Online</span><span class="sxs-lookup"><span data-stu-id="0345d-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="0345d-126">Внешний сайт может звонить в SharePoint и Project Online</span><span class="sxs-lookup"><span data-stu-id="0345d-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="0345d-127">Для внешней или независимой надстройки:</span><span class="sxs-lookup"><span data-stu-id="0345d-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="0345d-128">Пользователь выполняет приложение на своем устройстве</span><span class="sxs-lookup"><span data-stu-id="0345d-128">User executes an application on their device</span></span>
  - <span data-ttu-id="0345d-129">Приложение непосредственно аутентификация и вызов API Project Online</span><span class="sxs-lookup"><span data-stu-id="0345d-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="0345d-130">Тип приложения</span><span class="sxs-lookup"><span data-stu-id="0345d-130">Type of application</span></span>|<span data-ttu-id="0345d-131">Реализация API</span><span class="sxs-lookup"><span data-stu-id="0345d-131">API implementation</span></span>|<span data-ttu-id="0345d-132">Целевая среда</span><span class="sxs-lookup"><span data-stu-id="0345d-132">Target environment</span></span>|<span data-ttu-id="0345d-133">Примеры приложений</span><span class="sxs-lookup"><span data-stu-id="0345d-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0345d-134">Project hosted</span><span class="sxs-lookup"><span data-stu-id="0345d-134">Project hosted</span></span>  <br/> |<span data-ttu-id="0345d-135">JSOM (объектная модель Java Script)</span><span class="sxs-lookup"><span data-stu-id="0345d-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="0345d-136">REST</span><span class="sxs-lookup"><span data-stu-id="0345d-136">REST</span></span>  <br/> |<span data-ttu-id="0345d-137">Браузер</span><span class="sxs-lookup"><span data-stu-id="0345d-137">Browser</span></span>  <br/> |<span data-ttu-id="0345d-138">Запись с картой времени</span><span class="sxs-lookup"><span data-stu-id="0345d-138">Timecard entry</span></span>  <br/> <span data-ttu-id="0345d-139">Утверждение с картой времени</span><span class="sxs-lookup"><span data-stu-id="0345d-139">Timecard approval</span></span>  <br/> <span data-ttu-id="0345d-140">Состояние проекта</span><span class="sxs-lookup"><span data-stu-id="0345d-140">Project Status</span></span>  <br/> <span data-ttu-id="0345d-141">Отчет по вопросам</span><span class="sxs-lookup"><span data-stu-id="0345d-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="0345d-142">Поставщик project Hosted</span><span class="sxs-lookup"><span data-stu-id="0345d-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="0345d-143">Клиентская библиотека CSOM</span><span class="sxs-lookup"><span data-stu-id="0345d-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="0345d-144">Веб-сайт или приложение Azure</span><span class="sxs-lookup"><span data-stu-id="0345d-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="0345d-145">Среда, не относягая к Windows (LAMP и т. д.)</span><span class="sxs-lookup"><span data-stu-id="0345d-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="0345d-146">Внешнее проверка времени</span><span class="sxs-lookup"><span data-stu-id="0345d-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="0345d-147">Импортер проектов</span><span class="sxs-lookup"><span data-stu-id="0345d-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="0345d-148">Внешняя/standalone</span><span class="sxs-lookup"><span data-stu-id="0345d-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="0345d-149">REST</span><span class="sxs-lookup"><span data-stu-id="0345d-149">REST</span></span>  <br/> <span data-ttu-id="0345d-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="0345d-150">CSOM</span></span>  <br/> |<span data-ttu-id="0345d-151">REST — любая платформа</span><span class="sxs-lookup"><span data-stu-id="0345d-151">REST - any platform</span></span>  <br/> <span data-ttu-id="0345d-152">CSOM — любая поддерживаемая платформа .NET</span><span class="sxs-lookup"><span data-stu-id="0345d-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="0345d-153">Запись с картой времени</span><span class="sxs-lookup"><span data-stu-id="0345d-153">Timecard entry</span></span>  <br/> <span data-ttu-id="0345d-154">Перенос проектов на новый сайт</span><span class="sxs-lookup"><span data-stu-id="0345d-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="0345d-155">Изменение состояния управления.</span><span class="sxs-lookup"><span data-stu-id="0345d-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="0345d-156">Что необходимо для начала разработки приложений для Project Online?</span><span class="sxs-lookup"><span data-stu-id="0345d-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="0345d-157">Общие элементы, необходимые для разработки приложений Project Online учетной записи Project Online и тестовые данные — проекты и сведения, связанные с проектами, которые включают назначения, задачи, ресурсы и настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="0345d-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="0345d-158">Кроме того, необходима среда разработки, но ее особенности зависят от типа приложения и интерфейса API, необходимого для приложения.</span><span class="sxs-lookup"><span data-stu-id="0345d-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="0345d-159">В следующих разделах описываются потребности в разработке для трех интерфейсов API.</span><span class="sxs-lookup"><span data-stu-id="0345d-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="0345d-160">В справочной документации описывается объектная модель, которая является общей для всех трех интерфейсов, а также карта объектов, которая показывает отношения между компонентами объектной модели.</span><span class="sxs-lookup"><span data-stu-id="0345d-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="0345d-161">Среда разработки надстройки, в которой находится project</span><span class="sxs-lookup"><span data-stu-id="0345d-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="0345d-162">Надстройка, которая находится на сервере и загружается в браузер для выполнения во время выполнения, — это надстройка, которая находится на сервере.</span><span class="sxs-lookup"><span data-stu-id="0345d-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="0345d-163">Надстройки с hosted могут использовать интерфейсы JSOM или REST и написаны на JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0345d-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="0345d-164">Project Online предоставляет ссылки на библиотеку JSOM для выполнения во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="0345d-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="0345d-165">Предположим, что разработка находится на платформе Windows, необходимые ресурсы следуют:</span><span class="sxs-lookup"><span data-stu-id="0345d-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="0345d-166">Visual Studio 2015 (предпочтительный) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="0345d-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="0345d-167">Средства разработки Office для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0345d-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="0345d-168">Язык JavaScript</span><span class="sxs-lookup"><span data-stu-id="0345d-168">JavaScript language</span></span>
    
<span data-ttu-id="0345d-169">Посетите https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages пример приложения.</span><span class="sxs-lookup"><span data-stu-id="0345d-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="0345d-170">Вы можете скачать и запустить пример в несколько простых действий:</span><span class="sxs-lookup"><span data-stu-id="0345d-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="0345d-171">Загрузка и открытие примера приложения</span><span class="sxs-lookup"><span data-stu-id="0345d-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="0345d-172">Обновление SiteURL в окне "Свойства"</span><span class="sxs-lookup"><span data-stu-id="0345d-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="0345d-173">Project Online проверяет область приложения надстройки и разрешения пользователя на управление доступом к информации на хост-сайте Project Online.</span><span class="sxs-lookup"><span data-stu-id="0345d-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="0345d-174">Если доступ явно отказано в любом из параметров или в обоих параметрах, Project Online отказано в доступе к информации.</span><span class="sxs-lookup"><span data-stu-id="0345d-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="0345d-175">В противном случае доступ предоставляется.</span><span class="sxs-lookup"><span data-stu-id="0345d-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="0345d-176">Включить [загрузку неогрузки](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на сайте.</span><span class="sxs-lookup"><span data-stu-id="0345d-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="0345d-177">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="0345d-177">Build the project.</span></span>
    
5. <span data-ttu-id="0345d-178">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="0345d-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="0345d-179">Среда разработки надстройки с хостингом у поставщика Project</span><span class="sxs-lookup"><span data-stu-id="0345d-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="0345d-180">Надстройки с хостингом поставщика — это приложения, написанные и которые находятся на любой веб-платформе.</span><span class="sxs-lookup"><span data-stu-id="0345d-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="0345d-181">Они могут подключаться и выполнять операции с данными с помощью API REST (или CSOM для платформ Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="0345d-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="0345d-182">Для разработки можно использовать любой язык и среду, поддерживают интерфейс REST.</span><span class="sxs-lookup"><span data-stu-id="0345d-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="0345d-183">Пример среды разработки Windows для этого типа приложений включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="0345d-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="0345d-184">Visual Studio 2015 (предпочтительный) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="0345d-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="0345d-185">Microsoft Office средств разработки для Visual Studio (поставляются с выпусками Visual Studio 2015 профессиональный и корпоративный)</span><span class="sxs-lookup"><span data-stu-id="0345d-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="0345d-186">.NET Framework 4.0 или более новой</span><span class="sxs-lookup"><span data-stu-id="0345d-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="0345d-187">[Пакет CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для вызовов CSOM)</span><span class="sxs-lookup"><span data-stu-id="0345d-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="0345d-188">Язык программирования, например C #</span><span class="sxs-lookup"><span data-stu-id="0345d-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="0345d-189">Посетите https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations сайт для работы с примерами сценариев.</span><span class="sxs-lookup"><span data-stu-id="0345d-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="0345d-190">Пример можно запустить в несколько этапов:</span><span class="sxs-lookup"><span data-stu-id="0345d-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="0345d-191">Загрузка и открытие примера приложения</span><span class="sxs-lookup"><span data-stu-id="0345d-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="0345d-192">Обновление SiteURL в окне "Свойства"</span><span class="sxs-lookup"><span data-stu-id="0345d-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="0345d-193">Project Online проверяет область приложения надстройки и разрешения пользователя на управление доступом к информации на хост-сайте Project Online.</span><span class="sxs-lookup"><span data-stu-id="0345d-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="0345d-194">Если доступ явно отказано в любом из параметров или в обоих параметрах, Project Online отказано в доступе к информации.</span><span class="sxs-lookup"><span data-stu-id="0345d-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="0345d-195">В противном случае доступ предоставляется.</span><span class="sxs-lookup"><span data-stu-id="0345d-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="0345d-196">Включить [загрузку неогрузки](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на сайте.</span><span class="sxs-lookup"><span data-stu-id="0345d-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="0345d-197">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="0345d-197">Build the project.</span></span>
    
5. <span data-ttu-id="0345d-198">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="0345d-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="0345d-199">Среда разработки внешних и автономных приложений</span><span class="sxs-lookup"><span data-stu-id="0345d-199">External/standalone application development environment</span></span>

<span data-ttu-id="0345d-200">Автономные приложения могут вызывать Project Online с помощью клиентской объектной модели (CSOM) или REST для связи с Project Online для создания, извлечения, обновления и удаления информации, которая находится на сервере.</span><span class="sxs-lookup"><span data-stu-id="0345d-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="0345d-201">Это приложение является автономным клиентом, которое зависит от уровня доступа пользователя для запуска.</span><span class="sxs-lookup"><span data-stu-id="0345d-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="0345d-202">Пример среды разработки Windows для этого типа приложений включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="0345d-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="0345d-203">Visual Studio 2015 (предпочтительный) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="0345d-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="0345d-204">Microsoft Office средств разработки для Visual Studio (поставляются с выпусками Visual Studio 2015 профессиональный и корпоративный)</span><span class="sxs-lookup"><span data-stu-id="0345d-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="0345d-205">.NET Framework 4.0 или более новой</span><span class="sxs-lookup"><span data-stu-id="0345d-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="0345d-206">[Пакет CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для вызовов CSOM)</span><span class="sxs-lookup"><span data-stu-id="0345d-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="0345d-207">Язык программирования, например C #</span><span class="sxs-lookup"><span data-stu-id="0345d-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="0345d-208">Посетите https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields пример приложения.</span><span class="sxs-lookup"><span data-stu-id="0345d-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="0345d-209">Пример можно запустить в несколько этапов:</span><span class="sxs-lookup"><span data-stu-id="0345d-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="0345d-210">Скачивание примера приложения</span><span class="sxs-lookup"><span data-stu-id="0345d-210">Download the sample application</span></span>
    
2. <span data-ttu-id="0345d-211">Внести несколько изменений для доступа к сайту Project Online — имя сайта, учетную запись пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="0345d-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="0345d-212">Убедитесь, что у пользователя есть доступ ко всем проектам.</span><span class="sxs-lookup"><span data-stu-id="0345d-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="0345d-213">Project Online использует разрешения пользователей для управления доступом к информации в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="0345d-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="0345d-214">Добавьте сборку SharePoint в ссылки с помощью консоли Nuget диспетчер пакетов, доступной в меню "Инструменты", введя в консоли Nuget следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="0345d-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="0345d-215">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="0345d-215">Build the project.</span></span>
    
5. <span data-ttu-id="0345d-216">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="0345d-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="0345d-217">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="0345d-217">Next steps</span></span>

<span data-ttu-id="0345d-218">В каждом примере приложения есть статья, в рамках которых объясняется, как работать с отдельным API Project.</span><span class="sxs-lookup"><span data-stu-id="0345d-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="0345d-219">Эти статьи отображаются в следующем списке, а также в нескольких статьях, описывающих связи суностей, сведения о системе запросов и доступе к настраиваемой полям.</span><span class="sxs-lookup"><span data-stu-id="0345d-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="0345d-220">Разработка приложения Project Online с помощью клиентской объектной модели</span><span class="sxs-lookup"><span data-stu-id="0345d-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="0345d-221">Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="0345d-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="0345d-222">Доступ к корпоративным настраиваемым полям Project Online</span><span class="sxs-lookup"><span data-stu-id="0345d-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="0345d-223">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0345d-223">See also</span></span>

<span data-ttu-id="0345d-224">Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="0345d-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

