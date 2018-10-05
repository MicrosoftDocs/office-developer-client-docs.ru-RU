---
title: Быстрое начало разработки для Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: 'Разработчик приложения можно настроить Project Online сайта (SharePoint hosted) с помощью автономных приложений и/или надстройки Project. Богатый набор приложений — это возможно, в диапазоне от-адресации потребностей пользователей, участвующих в проекте функции поддержки отдела управления Проектами, таких как одно из следующих:'
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392587"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="68b32-103">Быстрое начало разработки для Project Online</span><span class="sxs-lookup"><span data-stu-id="68b32-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="68b32-104">Разработчик приложения можно настроить Project Online сайта (SharePoint hosted) с помощью автономных приложений и/или надстройки Project. Богатый набор приложений — это возможно, в диапазоне от-адресации потребностей пользователей, участвующих в проекте функции поддержки отдела управления Проектами, таких как одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="68b32-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="68b32-105">Упрощенный карточками табельного учета ввода данных для сотрудников</span><span class="sxs-lookup"><span data-stu-id="68b32-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="68b32-106">Утверждение эффективно карточками табельного учета для руководителей</span><span class="sxs-lookup"><span data-stu-id="68b32-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="68b32-107">Надзор за получение разрешений (Закупка и состояние), необходимых для проекта</span><span class="sxs-lookup"><span data-stu-id="68b32-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="68b32-108">Проверка состояния и состояния активных проектов</span><span class="sxs-lookup"><span data-stu-id="68b32-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="68b32-109">Отчет о проблемы</span><span class="sxs-lookup"><span data-stu-id="68b32-109">Issues report</span></span>
- <span data-ttu-id="68b32-110">Изменить отчет о состоянии управления</span><span class="sxs-lookup"><span data-stu-id="68b32-110">Change Management Status report</span></span>
    
<span data-ttu-id="68b32-111">Project Online включает поддержку API для учета в следующих сценариях:</span><span class="sxs-lookup"><span data-stu-id="68b32-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="68b32-112">Для Project (SharePoint), размещенные надстройки:</span><span class="sxs-lookup"><span data-stu-id="68b32-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="68b32-113">Код (JavaScript, HTML, CSS), которая размещается в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="68b32-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="68b32-114">Средства, которые загружаются в браузере и выполняются в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="68b32-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="68b32-115">Бизнес-логику, которая находится в JavaScript</span><span class="sxs-lookup"><span data-stu-id="68b32-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="68b32-116">Доступ к данным, такие как / сохранены в Project Online и SharePoint (но не ограничиваясь):</span><span class="sxs-lookup"><span data-stu-id="68b32-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="68b32-117">настраиваемые поля;</span><span class="sxs-lookup"><span data-stu-id="68b32-117">Custom fields</span></span>  
  - <span data-ttu-id="68b32-118">Списки</span><span class="sxs-lookup"><span data-stu-id="68b32-118">Lists</span></span>
    
- <span data-ttu-id="68b32-119">Для Project (SharePoint) у поставщика надстройки:</span><span class="sxs-lookup"><span data-stu-id="68b32-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="68b32-120">Код, существующий на сайте, внешними по отношению к сайт Project Online</span><span class="sxs-lookup"><span data-stu-id="68b32-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="68b32-121">Внешний сайт, который может быть (но не ограничиваясь):</span><span class="sxs-lookup"><span data-stu-id="68b32-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="68b32-122">Другой сайт SharePoint</span><span class="sxs-lookup"><span data-stu-id="68b32-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="68b32-123">Веб-приложения и службы основаны на любой платформы</span><span class="sxs-lookup"><span data-stu-id="68b32-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="68b32-124">Внешний узел содержит бизнес-логики</span><span class="sxs-lookup"><span data-stu-id="68b32-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="68b32-125">Веб-обозреватель перенаправляется из Project Online для внешних сайтов с помощью маркеров доступа для Project Online</span><span class="sxs-lookup"><span data-stu-id="68b32-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="68b32-126">Внешних сайтов могут выполнять вызовы SharePoint и Project Online</span><span class="sxs-lookup"><span data-stu-id="68b32-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="68b32-127">Для внешних/автономных надстройке:</span><span class="sxs-lookup"><span data-stu-id="68b32-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="68b32-128">Пользователь выполняет приложение на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="68b32-128">User executes an application on their device</span></span>
  - <span data-ttu-id="68b32-129">Приложение выполняет проверку подлинности и напрямую вызывает Project Online API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="68b32-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="68b32-130">Тип приложения</span><span class="sxs-lookup"><span data-stu-id="68b32-130">Type of application</span></span>|<span data-ttu-id="68b32-131">Реализация интерфейса API</span><span class="sxs-lookup"><span data-stu-id="68b32-131">API implementation</span></span>|<span data-ttu-id="68b32-132">Целевая среда</span><span class="sxs-lookup"><span data-stu-id="68b32-132">Target environment</span></span>|<span data-ttu-id="68b32-133">Примеры приложений</span><span class="sxs-lookup"><span data-stu-id="68b32-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68b32-134">Размещенные проекта</span><span class="sxs-lookup"><span data-stu-id="68b32-134">Project hosted</span></span>  <br/> |<span data-ttu-id="68b32-135">JSOM (объектная модель)</span><span class="sxs-lookup"><span data-stu-id="68b32-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="68b32-136">REST</span><span class="sxs-lookup"><span data-stu-id="68b32-136">REST</span></span>  <br/> |<span data-ttu-id="68b32-137">Веб-браузер</span><span class="sxs-lookup"><span data-stu-id="68b32-137">Browser</span></span>  <br/> |<span data-ttu-id="68b32-138">Запись карточками табельного учета</span><span class="sxs-lookup"><span data-stu-id="68b32-138">Timecard entry</span></span>  <br/> <span data-ttu-id="68b32-139">Утверждение карточками табельного учета</span><span class="sxs-lookup"><span data-stu-id="68b32-139">Timecard approval</span></span>  <br/> <span data-ttu-id="68b32-140">Состояние проекта</span><span class="sxs-lookup"><span data-stu-id="68b32-140">Project Status</span></span>  <br/> <span data-ttu-id="68b32-141">Отчет о проблемы</span><span class="sxs-lookup"><span data-stu-id="68b32-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="68b32-142">Проект размещением у поставщика</span><span class="sxs-lookup"><span data-stu-id="68b32-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="68b32-143">Клиентская библиотека CSOM</span><span class="sxs-lookup"><span data-stu-id="68b32-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="68b32-144">Веб-сайт Azure/приложения</span><span class="sxs-lookup"><span data-stu-id="68b32-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="68b32-145">Среда не Windows (LAMP, и т.д.)</span><span class="sxs-lookup"><span data-stu-id="68b32-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="68b32-146">Средства проверки внешних табеля учета рабочего времени</span><span class="sxs-lookup"><span data-stu-id="68b32-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="68b32-147">Средства импорта проектов</span><span class="sxs-lookup"><span data-stu-id="68b32-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="68b32-148">Внешний/автономных</span><span class="sxs-lookup"><span data-stu-id="68b32-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="68b32-149">REST</span><span class="sxs-lookup"><span data-stu-id="68b32-149">REST</span></span>  <br/> <span data-ttu-id="68b32-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="68b32-150">CSOM</span></span>  <br/> |<span data-ttu-id="68b32-151">REST - любой платформы</span><span class="sxs-lookup"><span data-stu-id="68b32-151">REST - any platform</span></span>  <br/> <span data-ttu-id="68b32-152">CSOM - любой платформы .NET поддерживается</span><span class="sxs-lookup"><span data-stu-id="68b32-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="68b32-153">Запись карточками табельного учета</span><span class="sxs-lookup"><span data-stu-id="68b32-153">Timecard entry</span></span>  <br/> <span data-ttu-id="68b32-154">Перенос проектов для нового сайта</span><span class="sxs-lookup"><span data-stu-id="68b32-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="68b32-155">Изменение состояния управления.</span><span class="sxs-lookup"><span data-stu-id="68b32-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="68b32-156">Что требуется быстро приступить к разработке приложений для Project Online?</span><span class="sxs-lookup"><span data-stu-id="68b32-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="68b32-157">Общие элементы, необходимые для разработки проекта веб-приложений являются учетной записи Project Online и тестовых данных--проектов и сведения, связанными с проектом, которые включают в себя назначения, задачи, ресурсы и настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="68b32-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="68b32-158">Также требуются среду разработки, но особенности среды разработки зависят от типа приложения и интерфейс API, необходимый для приложения.</span><span class="sxs-lookup"><span data-stu-id="68b32-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="68b32-159">В следующих разделах описываются потребностей разработки для трех API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="68b32-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="68b32-160">Справочная документация Описание объектной модели, которые являются общими для всех трех интерфейсов, а также сопоставление объектов, показаны отношения между компонентами объектной модели.</span><span class="sxs-lookup"><span data-stu-id="68b32-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="68b32-161">Проект размещенные среды разработки надстройки</span><span class="sxs-lookup"><span data-stu-id="68b32-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="68b32-162">Размещенной надстройки — это надстройка, в которой находится на сервере и загружаются в браузер для выполнения.</span><span class="sxs-lookup"><span data-stu-id="68b32-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="68b32-163">Размещенной надстройки могут использовать интерфейсы JSOM и REST и записывается в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="68b32-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="68b32-164">Project Online содержит ссылки на библиотеку JSOM для выполнения.</span><span class="sxs-lookup"><span data-stu-id="68b32-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="68b32-165">Предполагается применение разработки — на платформе Windows, выполните необходимые ресурсы:</span><span class="sxs-lookup"><span data-stu-id="68b32-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="68b32-166">Visual Studio 2015 (рекомендуется) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="68b32-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="68b32-167">Средства разработки Office для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="68b32-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="68b32-168">Язык JavaScript</span><span class="sxs-lookup"><span data-stu-id="68b32-168">JavaScript language</span></span>
    
<span data-ttu-id="68b32-169">Посетите https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages для примера приложения.</span><span class="sxs-lookup"><span data-stu-id="68b32-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="68b32-170">Можно загрузить и запустить образец в несколько этапов:</span><span class="sxs-lookup"><span data-stu-id="68b32-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="68b32-171">Загрузите и откройте пример приложения</span><span class="sxs-lookup"><span data-stu-id="68b32-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="68b32-172">Обновите свойство SiteURL в окне свойств</span><span class="sxs-lookup"><span data-stu-id="68b32-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="68b32-173">Project Online проверяет приложения области надстройки и разрешения пользователя для управления доступа к данным на узле Project Online.</span><span class="sxs-lookup"><span data-stu-id="68b32-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="68b32-174">Если явно отказано в доступе в один или оба параметров Project Online не дает доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="68b32-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="68b32-175">В противном случае доступа.</span><span class="sxs-lookup"><span data-stu-id="68b32-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="68b32-176">Включите [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="68b32-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="68b32-177">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="68b32-177">Build the project.</span></span>
    
5. <span data-ttu-id="68b32-178">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="68b32-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="68b32-179">Среда размещением у поставщика разработки надстройки Project</span><span class="sxs-lookup"><span data-stu-id="68b32-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="68b32-180">Надстройки размещением у поставщика, приложений и находящихся на любой веб-платформы.</span><span class="sxs-lookup"><span data-stu-id="68b32-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="68b32-181">Они подключения и выполнения операций с данными с помощью REST (или CSOM для платформ Майкрософт, обеспечивающий) API.</span><span class="sxs-lookup"><span data-stu-id="68b32-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="68b32-182">Любой язык и среда, поддерживающая интерфейс REST можно использовать для разработки.</span><span class="sxs-lookup"><span data-stu-id="68b32-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="68b32-183">Пример среды разработки Windows для этого типа приложений включает в себя следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="68b32-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="68b32-184">Visual Studio 2015 (рекомендуется) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="68b32-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="68b32-185">Средства разработки Microsoft Office для Visual Studio (поставляется с помощью Visual Studio 2015 Professional и корпоративные выпуски)</span><span class="sxs-lookup"><span data-stu-id="68b32-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="68b32-186">.NET framework 4.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="68b32-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="68b32-187">[Пакет SharePointOnline CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для CSOM звонков)</span><span class="sxs-lookup"><span data-stu-id="68b32-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="68b32-188">Язык программирования, таких как C#</span><span class="sxs-lookup"><span data-stu-id="68b32-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="68b32-189">Посетите https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations для работы примеры сценариев.</span><span class="sxs-lookup"><span data-stu-id="68b32-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="68b32-190">Пример можно запустить в несколько этапов:</span><span class="sxs-lookup"><span data-stu-id="68b32-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="68b32-191">Загрузите и откройте пример приложения</span><span class="sxs-lookup"><span data-stu-id="68b32-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="68b32-192">Обновите свойство SiteURL в окне свойств</span><span class="sxs-lookup"><span data-stu-id="68b32-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="68b32-193">Project Online проверяет приложения области надстройки и разрешения пользователя для управления доступа к данным на узле Project Online.</span><span class="sxs-lookup"><span data-stu-id="68b32-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="68b32-194">Если явно отказано в доступе в один или оба параметров Project Online не дает доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="68b32-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="68b32-195">В противном случае доступа.</span><span class="sxs-lookup"><span data-stu-id="68b32-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="68b32-196">Включите [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="68b32-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="68b32-197">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="68b32-197">Build the project.</span></span>
    
5. <span data-ttu-id="68b32-198">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="68b32-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="68b32-199">Внешний/автономного приложения среды разработки</span><span class="sxs-lookup"><span data-stu-id="68b32-199">External/standalone application development environment</span></span>

<span data-ttu-id="68b32-200">Автономного приложения можно вызвать Project Online с помощью клиента со стороны объектной модели (CSOM) и REST для взаимодействия с Project Online в создание, получение, обновление и удаление сведений, находящихся на сервере.</span><span class="sxs-lookup"><span data-stu-id="68b32-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="68b32-201">Это изолированная клиентского приложения, которое зависит от уровня доступа пользователя для запуска.</span><span class="sxs-lookup"><span data-stu-id="68b32-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="68b32-202">Пример среды разработки Windows для этого типа приложений включает в себя следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="68b32-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="68b32-203">Visual Studio 2015 (рекомендуется) или Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="68b32-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="68b32-204">Средства разработки Microsoft Office для Visual Studio (поставляется с помощью Visual Studio 2015 Professional и корпоративные выпуски)</span><span class="sxs-lookup"><span data-stu-id="68b32-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="68b32-205">.NET framework 4.0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="68b32-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="68b32-206">[Пакет SharePointOnline CSOM](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (для CSOM звонков)</span><span class="sxs-lookup"><span data-stu-id="68b32-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="68b32-207">Язык программирования, таких как C#</span><span class="sxs-lookup"><span data-stu-id="68b32-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="68b32-208">Посетите https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields для примера приложения.</span><span class="sxs-lookup"><span data-stu-id="68b32-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="68b32-209">Пример можно запустить в несколько этапов:</span><span class="sxs-lookup"><span data-stu-id="68b32-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="68b32-210">Загрузить пример приложения</span><span class="sxs-lookup"><span data-stu-id="68b32-210">Download the sample application</span></span>
    
2. <span data-ttu-id="68b32-211">Внести несколько изменений для доступа к Project Online сайт — имя сайта, учетная запись пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="68b32-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="68b32-212">Убедитесь, что у пользователя есть доступ ко всем проектам.</span><span class="sxs-lookup"><span data-stu-id="68b32-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="68b32-213">Project Online использует разрешения пользователей для контроля доступа к данным в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="68b32-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="68b32-214">Добавьте ссылки, с помощью консоли диспетчер пакетов Nuget из меню "Сервис", введя следующее в командной консоли Nuget сборки SharePoint:</span><span class="sxs-lookup"><span data-stu-id="68b32-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="68b32-215">Выполните построение проекта.</span><span class="sxs-lookup"><span data-stu-id="68b32-215">Build the project.</span></span>
    
5. <span data-ttu-id="68b32-216">Запустите проект.</span><span class="sxs-lookup"><span data-stu-id="68b32-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="68b32-217">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="68b32-217">Next steps</span></span>

<span data-ttu-id="68b32-218">Каждый учебное приложение имеет статьи для пояснения важные сведения о работе с отдельными API проекта.</span><span class="sxs-lookup"><span data-stu-id="68b32-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="68b32-219">В следующем списке, а также несколько статей, посвященных отношений объектов, сведения о системе запросов и доступ к настраиваемых полей отображаются статьи.</span><span class="sxs-lookup"><span data-stu-id="68b32-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="68b32-220">Разработка Online приложения Project, с помощью клиентской объектной модели</span><span class="sxs-lookup"><span data-stu-id="68b32-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="68b32-221">Разработка Project Online надстройки с помощью модели объектов JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="68b32-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="68b32-222">Доступ к корпоративным настраиваемым полям Project Online</span><span class="sxs-lookup"><span data-stu-id="68b32-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="68b32-223">См. также</span><span class="sxs-lookup"><span data-stu-id="68b32-223">See also</span></span>

<span data-ttu-id="68b32-224">Документация и примеры, связанные с Project Online и разработки приложений с помощью CSOM в разделе [Портал проектов разработки](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="68b32-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

