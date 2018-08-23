---
title: Быстрое начало разработки для Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Разработчик приложения можно настроить Project Online сайта (SharePoint hosted) с помощью автономных приложений и/или надстройки Project. Богатый набор приложений — это возможно, в диапазоне от-адресации потребностей пользователей, участвующих в проекте функции поддержки отдела управления Проектами, таких как одно из следующих:'
ms.openlocfilehash: 25a38a7c7359020058983e271067a87da29f1b3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594533"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="fd438-103">Быстрое начало разработки для Project Online</span><span class="sxs-lookup"><span data-stu-id="fd438-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="fd438-104">Разработчик приложения можно настроить Project Online сайта (SharePoint hosted) с помощью автономных приложений и/или надстройки Project. Богатый набор приложений — это возможно, в диапазоне от-адресации потребностей пользователей, участвующих в проекте функции поддержки отдела управления Проектами, таких как одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="fd438-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="fd438-105">Упрощенный карточками табельного учета ввода данных для сотрудников</span><span class="sxs-lookup"><span data-stu-id="fd438-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="fd438-106">Утверждение эффективно карточками табельного учета для руководителей</span><span class="sxs-lookup"><span data-stu-id="fd438-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="fd438-107">Надзор за получение разрешений (Закупка и состояние), необходимых для проекта</span><span class="sxs-lookup"><span data-stu-id="fd438-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="fd438-108">Проверка состояния и состояния активных проектов</span><span class="sxs-lookup"><span data-stu-id="fd438-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="fd438-109">Отчет о проблемы</span><span class="sxs-lookup"><span data-stu-id="fd438-109">Issues report</span></span>
- <span data-ttu-id="fd438-110">Изменить отчет о состоянии управления</span><span class="sxs-lookup"><span data-stu-id="fd438-110">Change Management Status report</span></span>
    
<span data-ttu-id="fd438-111">Project Online включает поддержку API для учета в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="fd438-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="fd438-112">Для Project (SharePoint), размещенные надстройки:</span><span class="sxs-lookup"><span data-stu-id="fd438-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="fd438-113">Код (JavaScript, HTML, CSS), которая размещается в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="fd438-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="fd438-114">Средства, которые загружаются в браузере и выполняются в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="fd438-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="fd438-115">Бизнес-логику, которая находится в JavaScript</span><span class="sxs-lookup"><span data-stu-id="fd438-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="fd438-116">Доступ к данным, такие как / сохранены в Project Online и SharePoint (но не ограничиваясь):</span><span class="sxs-lookup"><span data-stu-id="fd438-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="fd438-117">настраиваемые поля;</span><span class="sxs-lookup"><span data-stu-id="fd438-117">Custom fields</span></span>  
  - <span data-ttu-id="fd438-118">Списки</span><span class="sxs-lookup"><span data-stu-id="fd438-118">Lists</span></span>
    
- <span data-ttu-id="fd438-119">Для Project (SharePoint) у поставщика надстройки:</span><span class="sxs-lookup"><span data-stu-id="fd438-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="fd438-120">Код, существующий на сайте, внешними по отношению к сайт Project Online</span><span class="sxs-lookup"><span data-stu-id="fd438-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="fd438-121">Внешний сайт, который может быть (но не ограничиваясь):</span><span class="sxs-lookup"><span data-stu-id="fd438-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="fd438-122">Другой сайт SharePoint</span><span class="sxs-lookup"><span data-stu-id="fd438-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="fd438-123">Веб-приложения и службы основаны на любой платформы</span><span class="sxs-lookup"><span data-stu-id="fd438-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="fd438-124">Внешний узел содержит бизнес-логики</span><span class="sxs-lookup"><span data-stu-id="fd438-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="fd438-125">Веб-обозреватель перенаправляется из Project Online для внешних сайтов с помощью маркеров доступа для Project Online</span><span class="sxs-lookup"><span data-stu-id="fd438-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="fd438-126">Внешних сайтов могут выполнять вызовы SharePoint и Project Online</span><span class="sxs-lookup"><span data-stu-id="fd438-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="fd438-127">Для внешних/автономных надстройке:</span><span class="sxs-lookup"><span data-stu-id="fd438-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="fd438-128">Пользователь выполняет приложение на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="fd438-128">User executes an application on their device</span></span>
  - <span data-ttu-id="fd438-129">Приложение выполняет проверку подлинности и напрямую вызывает Project Online API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="fd438-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="fd438-130">Тип приложения</span><span class="sxs-lookup"><span data-stu-id="fd438-130">Type of application</span></span>|<span data-ttu-id="fd438-131">Реализация интерфейса API</span><span class="sxs-lookup"><span data-stu-id="fd438-131">API implementation</span></span>|<span data-ttu-id="fd438-132">Целевая среда</span><span class="sxs-lookup"><span data-stu-id="fd438-132">Target environment</span></span>|<span data-ttu-id="fd438-133">Примеры приложений</span><span class="sxs-lookup"><span data-stu-id="fd438-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fd438-134">Размещенные проекта</span><span class="sxs-lookup"><span data-stu-id="fd438-134">Project hosted</span></span>  <br/> |<span data-ttu-id="fd438-135">JSOM (объектная модель)</span><span class="sxs-lookup"><span data-stu-id="fd438-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="fd438-136">REST</span><span class="sxs-lookup"><span data-stu-id="fd438-136">REST</span></span>  <br/> |<span data-ttu-id="fd438-137">Веб-браузер</span><span class="sxs-lookup"><span data-stu-id="fd438-137">Browser</span></span>  <br/> |<span data-ttu-id="fd438-138">Запись карточками табельного учета</span><span class="sxs-lookup"><span data-stu-id="fd438-138">Timecard entry</span></span>  <br/> <span data-ttu-id="fd438-139">Утверждение карточками табельного учета</span><span class="sxs-lookup"><span data-stu-id="fd438-139">Timecard approval</span></span>  <br/> <span data-ttu-id="fd438-140">Состояние проекта</span><span class="sxs-lookup"><span data-stu-id="fd438-140">Project Status</span></span>  <br/> <span data-ttu-id="fd438-141">Отчет о проблемы</span><span class="sxs-lookup"><span data-stu-id="fd438-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="fd438-142">Проект размещением у поставщика</span><span class="sxs-lookup"><span data-stu-id="fd438-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="fd438-143">Клиентская библиотека CSOM</span><span class="sxs-lookup"><span data-stu-id="fd438-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="fd438-144">Веб-сайт Azure/приложения</span><span class="sxs-lookup"><span data-stu-id="fd438-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="fd438-145">Среда не Windows (LAMP, и т.д.)</span><span class="sxs-lookup"><span data-stu-id="fd438-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="fd438-146">Средства проверки внешних табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="fd438-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="fd438-147">Средства импорта проектов</span><span class="sxs-lookup"><span data-stu-id="fd438-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="fd438-148">Внешний/автономных</span><span class="sxs-lookup"><span data-stu-id="fd438-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="fd438-149">REST</span><span class="sxs-lookup"><span data-stu-id="fd438-149">REST</span></span>  <br/> <span data-ttu-id="fd438-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="fd438-150">CSOM</span></span>  <br/> |<span data-ttu-id="fd438-151">REST - любой платформы</span><span class="sxs-lookup"><span data-stu-id="fd438-151">REST - any platform</span></span>  <br/> <span data-ttu-id="fd438-152">CSOM - любой платформы .NET поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd438-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="fd438-153">Запись карточками табельного учета</span><span class="sxs-lookup"><span data-stu-id="fd438-153">Timecard entry</span></span>  <br/> <span data-ttu-id="fd438-154">Перенос проектов для нового сайта</span><span class="sxs-lookup"><span data-stu-id="fd438-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="fd438-155">Изменение состояния управления.</span><span class="sxs-lookup"><span data-stu-id="fd438-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="fd438-156">Что требуется быстро приступить к разработке приложений для Project Online?</span><span class="sxs-lookup"><span data-stu-id="fd438-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="fd438-157">Общие элементы, необходимые для разработки проекта веб-приложений являются учетной записи Project Online и тестовых данных--проектов и сведения, связанными с проектом, которые включают в себя назначения, задачи, ресурсы и настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="fd438-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="fd438-158">Также требуются среду разработки, но особенности среды разработки зависят от типа приложения и интерфейс API, необходимый для приложения.</span><span class="sxs-lookup"><span data-stu-id="fd438-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="fd438-159">В следующих разделах описываются потребностей разработки для трех API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="fd438-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="fd438-160">Справочная документация Описание объектной модели, которые являются общими для всех трех интерфейсов, а также сопоставление объектов, показаны отношения между компонентами объектной модели.</span><span class="sxs-lookup"><span data-stu-id="fd438-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="fd438-161">Проект размещенные среды разработки надстройки</span><span class="sxs-lookup"><span data-stu-id="fd438-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="fd438-162">Размещенной надстройки — это надстройка, в которой находится на сервере и загружаются в браузер для выполнения.</span><span class="sxs-lookup"><span data-stu-id="fd438-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="fd438-163">Размещенной надстройки могут использовать интерфейсы JSOM и REST и записывается в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fd438-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="fd438-164">Project Online содержит ссылки на библиотеку JSOM для выполнения.</span><span class="sxs-lookup"><span data-stu-id="fd438-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="fd438-165">Предполагается применение разработки — на платформе Windows, выполните необходимые ресурсы:</span><span class="sxs-lookup"><span data-stu-id="fd438-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="fd438-166">Visual Studio 2015 (рекомендуется) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="fd438-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="fd438-167">Средства разработки Office для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fd438-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="fd438-168">Язык JavaScript</span><span class="sxs-lookup"><span data-stu-id="fd438-168">JavaScript language</span></span>
    
<span data-ttu-id="fd438-169">Посетите https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages для примера приложения.</span><span class="sxs-lookup"><span data-stu-id="fd438-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="fd438-170">Можно загрузить и запустить образец в несколько этапов:</span><span class="sxs-lookup"><span data-stu-id="fd438-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="fd438-171">Загрузите и откройте пример приложения</span><span class="sxs-lookup"><span data-stu-id="fd438-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="fd438-172">Обновите свойство SiteURL в окне свойств</span><span class="sxs-lookup"><span data-stu-id="fd438-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="fd438-173">Project Online проверяет приложения области надстройки и разрешения пользователя для управления доступа к данным на узле Project Online.</span><span class="sxs-lookup"><span data-stu-id="fd438-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="fd438-174">Если явно отказано в доступе в один или оба параметров Project Online не дает доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="fd438-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="fd438-175">В противном случае доступа.</span><span class="sxs-lookup"><span data-stu-id="fd438-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="fd438-176">Включите [sideloading](https://docs.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="fd438-176">Enable [sideloading](https://docs.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="fd438-177">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="fd438-177">Build the project.</span></span>
    
5. <span data-ttu-id="fd438-178">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="fd438-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="fd438-179">Среда размещением у поставщика разработки надстройки Project</span><span class="sxs-lookup"><span data-stu-id="fd438-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="fd438-180">Надстройки размещением у поставщика, приложений и находящихся на любой веб-платформы.</span><span class="sxs-lookup"><span data-stu-id="fd438-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="fd438-181">Они подключения и выполнения операций с данными с помощью REST (или CSOM для платформ Майкрософт, обеспечивающий) API.</span><span class="sxs-lookup"><span data-stu-id="fd438-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="fd438-182">Любой язык и среда, поддерживающая интерфейс REST можно использовать для разработки.</span><span class="sxs-lookup"><span data-stu-id="fd438-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="fd438-183">Пример среды разработки Windows для этого типа приложений включает в себя следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="fd438-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="fd438-184">Visual Studio 2015 (рекомендуется) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="fd438-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="fd438-185">Средства разработки Microsoft Office для Visual Studio (поставляется с помощью Visual Studio 2015 Professional и корпоративные выпуски)</span><span class="sxs-lookup"><span data-stu-id="fd438-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="fd438-186">.NET framework 4.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fd438-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="fd438-187">[Пакет SharePointOnline CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для CSOM звонков)</span><span class="sxs-lookup"><span data-stu-id="fd438-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="fd438-188">Язык программирования, таких как C#</span><span class="sxs-lookup"><span data-stu-id="fd438-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="fd438-189">Посетите https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations для работы примеры сценариев.</span><span class="sxs-lookup"><span data-stu-id="fd438-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="fd438-190">Пример можно запустить в несколько этапов:</span><span class="sxs-lookup"><span data-stu-id="fd438-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="fd438-191">Загрузите и откройте пример приложения</span><span class="sxs-lookup"><span data-stu-id="fd438-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="fd438-192">Обновите свойство SiteURL в окне свойств</span><span class="sxs-lookup"><span data-stu-id="fd438-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="fd438-193">Project Online проверяет приложения области надстройки и разрешения пользователя для управления доступа к данным на узле Project Online.</span><span class="sxs-lookup"><span data-stu-id="fd438-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="fd438-194">Если явно отказано в доступе в один или оба параметров Project Online не дает доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="fd438-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="fd438-195">В противном случае доступа.</span><span class="sxs-lookup"><span data-stu-id="fd438-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="fd438-196">Включите [sideloading](https://docs.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="fd438-196">Enable [sideloading](https://docs.microsoft.com/en-us/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="fd438-197">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="fd438-197">Build the project.</span></span>
    
5. <span data-ttu-id="fd438-198">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="fd438-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="fd438-199">Внешний/автономного приложения среды разработки</span><span class="sxs-lookup"><span data-stu-id="fd438-199">External/standalone application development environment</span></span>

<span data-ttu-id="fd438-200">Автономного приложения можно вызвать Project Online с помощью клиента со стороны объектной модели (CSOM) и REST для взаимодействия с Project Online в создание, получение, обновление и удаление сведений, находящихся на сервере.</span><span class="sxs-lookup"><span data-stu-id="fd438-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="fd438-201">Это изолированная клиентского приложения, которое зависит от уровня доступа пользователя для запуска.</span><span class="sxs-lookup"><span data-stu-id="fd438-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="fd438-202">Пример среды разработки Windows для этого типа приложений включает в себя следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="fd438-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="fd438-203">Visual Studio 2015 (рекомендуется) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="fd438-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="fd438-204">Средства разработки Microsoft Office для Visual Studio (поставляется с помощью Visual Studio 2015 Professional и корпоративные выпуски)</span><span class="sxs-lookup"><span data-stu-id="fd438-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="fd438-205">.NET framework 4.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fd438-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="fd438-206">[Пакет SharePointOnline CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для CSOM звонков)</span><span class="sxs-lookup"><span data-stu-id="fd438-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="fd438-207">Язык программирования, таких как C#</span><span class="sxs-lookup"><span data-stu-id="fd438-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="fd438-208">Посетите https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields для примера приложения.</span><span class="sxs-lookup"><span data-stu-id="fd438-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="fd438-209">Пример можно запустить в несколько этапов:</span><span class="sxs-lookup"><span data-stu-id="fd438-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="fd438-210">Загрузить пример приложения</span><span class="sxs-lookup"><span data-stu-id="fd438-210">Download the sample application</span></span>
    
2. <span data-ttu-id="fd438-211">Внести несколько изменений для доступа к Project Online сайт — имя сайта, учетная запись пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="fd438-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="fd438-212">Убедитесь, что у пользователя есть доступ ко всем проектам.</span><span class="sxs-lookup"><span data-stu-id="fd438-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="fd438-213">Project Online использует разрешения пользователей для контроля доступа к данным в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="fd438-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="fd438-214">Добавьте ссылки, с помощью консоли диспетчер пакетов Nuget из меню "Сервис", введя следующее в командной консоли Nuget сборки SharePoint:</span><span class="sxs-lookup"><span data-stu-id="fd438-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="fd438-215">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="fd438-215">Build the project.</span></span>
    
5. <span data-ttu-id="fd438-216">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="fd438-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="fd438-217">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="fd438-217">Next steps</span></span>

<span data-ttu-id="fd438-218">Каждый учебное приложение имеет статьи для пояснения важные сведения о работе с отдельными API проекта.</span><span class="sxs-lookup"><span data-stu-id="fd438-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="fd438-219">В следующем списке, а также несколько статей, посвященных отношений объектов, сведения о системе запросов и доступ к настраиваемых полей отображаются статьи.</span><span class="sxs-lookup"><span data-stu-id="fd438-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="fd438-220">Разработка Online приложения Project, с помощью клиентской объектной модели</span><span class="sxs-lookup"><span data-stu-id="fd438-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="fd438-221">Разработка Project Online надстройки с помощью модели объектов JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="fd438-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="fd438-222">Доступ к корпоративным настраиваемым полям Project Online</span><span class="sxs-lookup"><span data-stu-id="fd438-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="fd438-223">См. также</span><span class="sxs-lookup"><span data-stu-id="fd438-223">See also</span></span>

<span data-ttu-id="fd438-224">Документация и примеры, связанные с Project Online и разработки приложений с помощью CSOM в разделе [Портал проектов разработки](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="fd438-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

