---
title: Быстрое начало разработки для Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Разработчик приложения может настроить веб-Project Online (SharePoint) с помощью автономных приложений и/или Project надстройки. Возможно множество приложений, которые варьируются от решения потребностей тех, кто участвует в проекте, до функций поддержки PMO, таких как любое из следующих ниже:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344410"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="ed96d-103">Быстрое начало разработки для Project Online</span><span class="sxs-lookup"><span data-stu-id="ed96d-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="ed96d-104">Разработчик приложения может настроить веб-Project Online (SharePoint) с помощью автономных приложений и/или Project надстройки. Возможно множество приложений, которые варьируются от решения потребностей тех, кто участвует в проекте, до функций поддержки PMO, таких как любое из следующих ниже:</span><span class="sxs-lookup"><span data-stu-id="ed96d-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="ed96d-105">Упрощение записи данных с картой времени для сотрудников</span><span class="sxs-lookup"><span data-stu-id="ed96d-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="ed96d-106">Эффективное утверждение системы времени для руководителей</span><span class="sxs-lookup"><span data-stu-id="ed96d-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="ed96d-107">Надзор за разрешениями (закупками и состоянием), необходимыми для проекта</span><span class="sxs-lookup"><span data-stu-id="ed96d-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="ed96d-108">Проверка состояния и здоровья активных проектов</span><span class="sxs-lookup"><span data-stu-id="ed96d-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="ed96d-109">Отчет о проблемах</span><span class="sxs-lookup"><span data-stu-id="ed96d-109">Issues report</span></span>
- <span data-ttu-id="ed96d-110">Отчет о состоянии управления изменениями</span><span class="sxs-lookup"><span data-stu-id="ed96d-110">Change Management Status report</span></span>
    
<span data-ttu-id="ed96d-111">Project Online включает поддержку API для размещения следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="ed96d-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="ed96d-112">Для Project (SharePoint) надстройки:</span><span class="sxs-lookup"><span data-stu-id="ed96d-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="ed96d-113">Код (JavaScript, HTML, CSS), который находится в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ed96d-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="ed96d-114">Активы, которые загружаются в браузер и выполняются SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="ed96d-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="ed96d-115">Бизнес-логика, которая находится в JavaScript</span><span class="sxs-lookup"><span data-stu-id="ed96d-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="ed96d-116">Доступ к данным, хранимым в Project Online или SharePoint, например (но не ограничивается):</span><span class="sxs-lookup"><span data-stu-id="ed96d-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="ed96d-117">настраиваемые поля;</span><span class="sxs-lookup"><span data-stu-id="ed96d-117">Custom fields</span></span>  
  - <span data-ttu-id="ed96d-118">Списки</span><span class="sxs-lookup"><span data-stu-id="ed96d-118">Lists</span></span>
    
- <span data-ttu-id="ed96d-119">Для надстройки Project (SharePoint) поставщика:</span><span class="sxs-lookup"><span data-stu-id="ed96d-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="ed96d-120">Код, который существует на сайте, внешнем Project Online сайте</span><span class="sxs-lookup"><span data-stu-id="ed96d-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="ed96d-121">Внешний сайт, который может быть (но не ограничен):</span><span class="sxs-lookup"><span data-stu-id="ed96d-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="ed96d-122">Другой SharePoint сайт</span><span class="sxs-lookup"><span data-stu-id="ed96d-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="ed96d-123">Веб-приложение/служба, созданная на любой платформе</span><span class="sxs-lookup"><span data-stu-id="ed96d-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="ed96d-124">Внешний сайт содержит бизнес-логику</span><span class="sxs-lookup"><span data-stu-id="ed96d-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="ed96d-125">Браузер перенаправляется с Project Online на внешний сайт с маркерами доступа к Project Online</span><span class="sxs-lookup"><span data-stu-id="ed96d-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="ed96d-126">Внешний сайт может звонить на SharePoint и Project Online</span><span class="sxs-lookup"><span data-stu-id="ed96d-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="ed96d-127">Для внешней или автономных надстройки:</span><span class="sxs-lookup"><span data-stu-id="ed96d-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="ed96d-128">Пользователь выполняет приложение на своем устройстве</span><span class="sxs-lookup"><span data-stu-id="ed96d-128">User executes an application on their device</span></span>
  - <span data-ttu-id="ed96d-129">Проверка подлинности приложения и вызовы Project Online API напрямую</span><span class="sxs-lookup"><span data-stu-id="ed96d-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="ed96d-130">Тип приложения</span><span class="sxs-lookup"><span data-stu-id="ed96d-130">Type of application</span></span>|<span data-ttu-id="ed96d-131">Реализация API</span><span class="sxs-lookup"><span data-stu-id="ed96d-131">API implementation</span></span>|<span data-ttu-id="ed96d-132">Целевая среда</span><span class="sxs-lookup"><span data-stu-id="ed96d-132">Target environment</span></span>|<span data-ttu-id="ed96d-133">Примеры приложений</span><span class="sxs-lookup"><span data-stu-id="ed96d-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ed96d-134">Project хостинга</span><span class="sxs-lookup"><span data-stu-id="ed96d-134">Project hosted</span></span>  <br/> |<span data-ttu-id="ed96d-135">JSOM (объектная модель Java Script)</span><span class="sxs-lookup"><span data-stu-id="ed96d-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="ed96d-136">REST</span><span class="sxs-lookup"><span data-stu-id="ed96d-136">REST</span></span>  <br/> |<span data-ttu-id="ed96d-137">Браузер</span><span class="sxs-lookup"><span data-stu-id="ed96d-137">Browser</span></span>  <br/> |<span data-ttu-id="ed96d-138">Запись с картой времени</span><span class="sxs-lookup"><span data-stu-id="ed96d-138">Timecard entry</span></span>  <br/> <span data-ttu-id="ed96d-139">Утверждение timecard</span><span class="sxs-lookup"><span data-stu-id="ed96d-139">Timecard approval</span></span>  <br/> <span data-ttu-id="ed96d-140">Состояние проекта</span><span class="sxs-lookup"><span data-stu-id="ed96d-140">Project Status</span></span>  <br/> <span data-ttu-id="ed96d-141">Отчет о проблемах</span><span class="sxs-lookup"><span data-stu-id="ed96d-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="ed96d-142">Project Provider Hosted</span><span class="sxs-lookup"><span data-stu-id="ed96d-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="ed96d-143">Клиентская библиотека CSOM</span><span class="sxs-lookup"><span data-stu-id="ed96d-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="ed96d-144">Веб-сайт Azure/App</span><span class="sxs-lookup"><span data-stu-id="ed96d-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="ed96d-145">Нестандартная Windows (LAMP и т.д.)</span><span class="sxs-lookup"><span data-stu-id="ed96d-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="ed96d-146">Валидатор внешнего времени</span><span class="sxs-lookup"><span data-stu-id="ed96d-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="ed96d-147">Project Импортер</span><span class="sxs-lookup"><span data-stu-id="ed96d-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="ed96d-148">External/Standalone</span><span class="sxs-lookup"><span data-stu-id="ed96d-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="ed96d-149">REST</span><span class="sxs-lookup"><span data-stu-id="ed96d-149">REST</span></span>  <br/> <span data-ttu-id="ed96d-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="ed96d-150">CSOM</span></span>  <br/> |<span data-ttu-id="ed96d-151">REST — любая платформа</span><span class="sxs-lookup"><span data-stu-id="ed96d-151">REST - any platform</span></span>  <br/> <span data-ttu-id="ed96d-152">CSOM — любая поддерживаемая платформа .NET</span><span class="sxs-lookup"><span data-stu-id="ed96d-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="ed96d-153">Запись с картой времени</span><span class="sxs-lookup"><span data-stu-id="ed96d-153">Timecard entry</span></span>  <br/> <span data-ttu-id="ed96d-154">Перенос проектов на новый сайт</span><span class="sxs-lookup"><span data-stu-id="ed96d-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="ed96d-155">Изменение состояния управления.</span><span class="sxs-lookup"><span data-stu-id="ed96d-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="ed96d-156">Что нужно для начала разработки приложений для Project Online?</span><span class="sxs-lookup"><span data-stu-id="ed96d-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="ed96d-157">Общими элементами, необходимыми для разработки Project Online приложений, являются Project Online учетные записи и тестовые данные — проекты и сведения, связанные с проектами, которые включают назначения, задачи, ресурсы и настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="ed96d-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="ed96d-158">Необходима также среда разработки, но специфика среды разработки зависит от типа приложения и интерфейса API, необходимых для приложения.</span><span class="sxs-lookup"><span data-stu-id="ed96d-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="ed96d-159">В следующих нескольких разделах описываются потребности в разработке для трех интерфейсов API.</span><span class="sxs-lookup"><span data-stu-id="ed96d-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="ed96d-160">В справочной документации описывается общая для всех трех интерфейсов объектная модель, а также карта объектов, на которых показаны связи между компонентами объектной модели.</span><span class="sxs-lookup"><span data-stu-id="ed96d-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="ed96d-161">Project среды разработки надстройки</span><span class="sxs-lookup"><span data-stu-id="ed96d-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="ed96d-162">Расположенная надстройка — это надстройка, которая находится на сервере и загружается в браузер для выполнения.</span><span class="sxs-lookup"><span data-stu-id="ed96d-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="ed96d-163">Хост-надстройки могут использовать интерфейсы JSOM или REST и написаны на JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ed96d-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="ed96d-164">Project Online содержит ссылки на библиотеку JSOM для выполнения.</span><span class="sxs-lookup"><span data-stu-id="ed96d-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="ed96d-165">Если разработка находится на платформе Windows, необходимые ресурсы следуют следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ed96d-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="ed96d-166">Visual Studio 2015 (предпочтительно) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="ed96d-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="ed96d-167">Office разработки для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ed96d-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="ed96d-168">Язык JavaScript</span><span class="sxs-lookup"><span data-stu-id="ed96d-168">JavaScript language</span></span>
    
<span data-ttu-id="ed96d-169">Посетите https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages пример приложения.</span><span class="sxs-lookup"><span data-stu-id="ed96d-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="ed96d-170">Вы можете скачать и запустить пример в нескольких простых шагах:</span><span class="sxs-lookup"><span data-stu-id="ed96d-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="ed96d-171">Скачайте и откройте пример приложения</span><span class="sxs-lookup"><span data-stu-id="ed96d-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="ed96d-172">Обновление siteURL в окне Свойства</span><span class="sxs-lookup"><span data-stu-id="ed96d-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="ed96d-173">Project Online рассматривает область применения надстройки и разрешения пользователей для управления доступом к информации на Project Online хост.</span><span class="sxs-lookup"><span data-stu-id="ed96d-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="ed96d-174">Если доступ явно отказано в любом или обоих параметрах, Project Online не будет доступа к этой информации.</span><span class="sxs-lookup"><span data-stu-id="ed96d-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="ed96d-175">В противном случае доступ предоставляется.</span><span class="sxs-lookup"><span data-stu-id="ed96d-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="ed96d-176">Включить [побную загрузку](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="ed96d-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="ed96d-177">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="ed96d-177">Build the project.</span></span>
    
5. <span data-ttu-id="ed96d-178">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="ed96d-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="ed96d-179">Project среды разработки надстройки с хостингом поставщика</span><span class="sxs-lookup"><span data-stu-id="ed96d-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="ed96d-180">Надстройки поставщика — это приложения, написанные и проживающие на любой веб-платформе.</span><span class="sxs-lookup"><span data-stu-id="ed96d-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="ed96d-181">Они могут подключать и выполнять операции данных с помощью API REST (или CSOM для платформ Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="ed96d-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="ed96d-182">Для разработки можно использовать любой язык и среду, которая поддерживает интерфейс REST.</span><span class="sxs-lookup"><span data-stu-id="ed96d-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="ed96d-183">Пример среды разработки Windows этого типа приложения включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="ed96d-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="ed96d-184">Visual Studio 2015 (предпочтительно) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="ed96d-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="ed96d-185">Microsoft Office Средства разработки для Visual Studio (поставляются с Visual Studio 2015 Professional и Enterprise выпусками)</span><span class="sxs-lookup"><span data-stu-id="ed96d-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="ed96d-186">платформа .NET Framework 4.0 или более новые</span><span class="sxs-lookup"><span data-stu-id="ed96d-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="ed96d-187">[Пакет CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для вызовов CSOM)</span><span class="sxs-lookup"><span data-stu-id="ed96d-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="ed96d-188">Язык программирования, например C #</span><span class="sxs-lookup"><span data-stu-id="ed96d-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="ed96d-189">Посетите https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations рабочие примеры сценариев.</span><span class="sxs-lookup"><span data-stu-id="ed96d-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="ed96d-190">Пример можно выполнить в нескольких шагах:</span><span class="sxs-lookup"><span data-stu-id="ed96d-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="ed96d-191">Скачайте и откройте пример приложения</span><span class="sxs-lookup"><span data-stu-id="ed96d-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="ed96d-192">Обновление siteURL в окне Свойства</span><span class="sxs-lookup"><span data-stu-id="ed96d-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="ed96d-193">Project Online рассматривает область применения надстройки и разрешения пользователей для управления доступом к информации на Project Online хост.</span><span class="sxs-lookup"><span data-stu-id="ed96d-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="ed96d-194">Если доступ явно отказано в любом или обоих параметрах, Project Online не будет доступа к этой информации.</span><span class="sxs-lookup"><span data-stu-id="ed96d-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="ed96d-195">В противном случае доступ предоставляется.</span><span class="sxs-lookup"><span data-stu-id="ed96d-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="ed96d-196">Включить [побную загрузку](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="ed96d-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="ed96d-197">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="ed96d-197">Build the project.</span></span>
    
5. <span data-ttu-id="ed96d-198">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="ed96d-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="ed96d-199">Среда разработки внешних и автономных приложений</span><span class="sxs-lookup"><span data-stu-id="ed96d-199">External/standalone application development environment</span></span>

<span data-ttu-id="ed96d-200">Автономные приложения могут вызывать Project Online с помощью клиентской объектной модели (CSOM) или REST для связи с Project Online для создания, получения, обновления и удаления сведений, проживающих на сервере.</span><span class="sxs-lookup"><span data-stu-id="ed96d-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="ed96d-201">Это автономные клиентские приложения, которые зависят от уровня доступа пользователей к запуску.</span><span class="sxs-lookup"><span data-stu-id="ed96d-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="ed96d-202">Пример среды разработки Windows этого типа приложения включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="ed96d-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="ed96d-203">Visual Studio 2015 (предпочтительно) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="ed96d-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="ed96d-204">Microsoft Office Средства разработки для Visual Studio (поставляются с Visual Studio 2015 Professional и Enterprise выпусками)</span><span class="sxs-lookup"><span data-stu-id="ed96d-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="ed96d-205">платформа .NET Framework 4.0 или более новые</span><span class="sxs-lookup"><span data-stu-id="ed96d-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="ed96d-206">[Пакет CSOM SharePointOnline](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для вызовов CSOM)</span><span class="sxs-lookup"><span data-stu-id="ed96d-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="ed96d-207">Язык программирования, например C #</span><span class="sxs-lookup"><span data-stu-id="ed96d-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="ed96d-208">Посетите https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields пример приложения.</span><span class="sxs-lookup"><span data-stu-id="ed96d-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="ed96d-209">Пример можно выполнить в нескольких шагах:</span><span class="sxs-lookup"><span data-stu-id="ed96d-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="ed96d-210">Скачайте пример приложения</span><span class="sxs-lookup"><span data-stu-id="ed96d-210">Download the sample application</span></span>
    
2. <span data-ttu-id="ed96d-211">Внести несколько изменений для доступа к Project Online сайта, имени сайта, учетной записи пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="ed96d-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="ed96d-212">Убедитесь, что пользователь имеет доступ ко всем проектам.</span><span class="sxs-lookup"><span data-stu-id="ed96d-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="ed96d-213">Project Online для управления доступом к информации в хранилище данных с помощью пользовательских разрешений.</span><span class="sxs-lookup"><span data-stu-id="ed96d-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="ed96d-214">Добавьте сборку SharePoint ссылки с помощью консоли Nuget диспетчер пакетов, доступной в меню Tools, введя в консоль Nuget следующее:</span><span class="sxs-lookup"><span data-stu-id="ed96d-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="ed96d-215">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="ed96d-215">Build the project.</span></span>
    
5. <span data-ttu-id="ed96d-216">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="ed96d-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="ed96d-217">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="ed96d-217">Next steps</span></span>

<span data-ttu-id="ed96d-218">В каждом примере приложения есть статья, которая объясняет основные моменты работы с отдельным Project API.</span><span class="sxs-lookup"><span data-stu-id="ed96d-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="ed96d-219">Статьи отображаются в следующем списке, а также в нескольких статьях, описывающих отношения сущности, сведения о системе запросов и доступ к настраиваемой полям.</span><span class="sxs-lookup"><span data-stu-id="ed96d-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="ed96d-220">Разработка приложения Project Online с помощью клиентской объектной модели</span><span class="sxs-lookup"><span data-stu-id="ed96d-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="ed96d-221">Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="ed96d-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="ed96d-222">Доступ к корпоративным настраиваемым полям Project Online</span><span class="sxs-lookup"><span data-stu-id="ed96d-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="ed96d-223">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ed96d-223">See also</span></span>

<span data-ttu-id="ed96d-224">Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="ed96d-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

