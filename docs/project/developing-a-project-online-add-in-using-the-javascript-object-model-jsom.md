---
title: Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: В этой статье описывается разработка надстроек Microsoft Project Online для повышения качества работы с Project Online. Проект разработки реализован как пошаговое руководство. Надстройка, используемая для этой статьи, считывает и отображает имена проектов и идентификаторов опубликованных проектов из учетной записи Project Online, а также позволяет получить подробные сведения о задачах, связанных с отдельными проектами.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322694"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="783db-105">Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="783db-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="783db-106">В этой статье описывается разработка надстроек Microsoft Project Online, позволяющая улучшить работу с Project Online.</span><span class="sxs-lookup"><span data-stu-id="783db-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="783db-107">Проект разработки реализован как пошаговое руководство.</span><span class="sxs-lookup"><span data-stu-id="783db-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="783db-108">Надстройка, используемая для этой статьи, считывает и отображает имена проектов и идентификаторов опубликованных проектов из учетной записи Project Online, а также позволяет получить подробные сведения о задачах, связанных с отдельными проектами.</span><span class="sxs-lookup"><span data-stu-id="783db-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="783db-109">Во время выполнения список надстроек выглядит примерно так, как показано на следующем рисунке:</span><span class="sxs-lookup"><span data-stu-id="783db-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="783db-110">![Снимок экрана, на котором показан список проектов и задач JSOM] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Снимок экрана, на котором показан список проектов и задач JSOM")</span><span class="sxs-lookup"><span data-stu-id="783db-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="783db-111">В этом примере основное внимание уделяется взаимодействию с Project Online, что делает запросы и настраивает контекст для каждого запроса от службы.</span><span class="sxs-lookup"><span data-stu-id="783db-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="783db-112">Элементы ПОЛЬЗОВАТЕЛЬСКОГО интерфейса получают минимальное внимание.</span><span class="sxs-lookup"><span data-stu-id="783db-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="783db-113">Вместо этого списки источников содержат комментарии к ПОЛЬЗОВАТЕЛЬСКОМу ИНТЕРФЕЙСу.</span><span class="sxs-lookup"><span data-stu-id="783db-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="783db-114">Исходные файлы для примера надстройки, проект Visual Studio, доступны по адресу: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span><span class="sxs-lookup"><span data-stu-id="783db-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="783db-115">Во время чтения статьи Храните исходные файлы как справочные материалы, когда все дополняют ее.</span><span class="sxs-lookup"><span data-stu-id="783db-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="783db-116">Файлы в построении проекта Visual Studio и исполняемые файлы с минимальными изменениями — замена URL-адреса для клиента Project Online на папку PWA.</span><span class="sxs-lookup"><span data-stu-id="783db-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="783db-117">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="783db-117">Background</span></span>

<span data-ttu-id="783db-118">Project Online — это служба Office 365, которая предоставляет организациям решение для координации и управления портфелями, программами и проектами, используя решение для управления портфелем проектов (PPM) и управления проектами Office (PMO).</span><span class="sxs-lookup"><span data-stu-id="783db-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="783db-119">Project Online — это другое предложение, чем выпуски Project для настольных ПК; Однако Project Online по-прежнему содержит функциональные возможности для обслуживания и отслеживания сведений о проекте в течение всего времени существования проекта.</span><span class="sxs-lookup"><span data-stu-id="783db-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="783db-120">Project Online основан на SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="783db-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="783db-121">Размещенная Надстройка Project Online состоит из JavaScript и файлов ресурсов, взаимодействующих с API клиент-объектной модели.</span><span class="sxs-lookup"><span data-stu-id="783db-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="783db-122">Когда пользователь посещает надстройку, JavaScript и ресурсы загружаются и выполняются в браузере.</span><span class="sxs-lookup"><span data-stu-id="783db-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="783db-123">Надстройка выполняет асинхронные вызовы Project Online, чтобы взаимодействовать со службой, будь то создание, извлечение, обновление или удаление данных.</span><span class="sxs-lookup"><span data-stu-id="783db-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="783db-124">Project Online выполняет еще одно действие для защиты информации, которая относится к другим клиентам, из надстройки; Project Online создает изолированный сайт для взаимодействия с запросами из надстройки.</span><span class="sxs-lookup"><span data-stu-id="783db-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="783db-125">На узле Project Online не выполняется настраиваемый код.</span><span class="sxs-lookup"><span data-stu-id="783db-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="783db-126">Настройка разработки для надстроек Project Online использует тип проекта надстройки SharePoint для Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="783db-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="783db-127">Надстройка написана на JavaScript и использует объектную модель JavaScript для Project (JSOM) для взаимодействия с веб-службой Project Online.</span><span class="sxs-lookup"><span data-stu-id="783db-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="783db-128">JSOM наследует множество функций из SharePoint JSOM.</span><span class="sxs-lookup"><span data-stu-id="783db-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="783db-129">Надстройки могут быть опубликованы и проданы в магазине Office или развернуты в частном каталоге приложений в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="783db-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="783db-130">Дополнительные сведения можно найти [в статье Развертывание и публикация надстройки Office](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span><span class="sxs-lookup"><span data-stu-id="783db-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="783db-131">Надстройка, используемая в этой статье, является примером для разработчиков; Он не предназначен для использования в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="783db-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="783db-132">Основная цель — показать пример разработки приложений для Project Online.</span><span class="sxs-lookup"><span data-stu-id="783db-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="783db-133">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="783db-133">Prerequisites</span></span>

<span data-ttu-id="783db-134">Добавьте следующие элементы в поддерживаемую среду Windows:</span><span class="sxs-lookup"><span data-stu-id="783db-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="783db-135">**.NET framework 4,0 или более поздней**версии: совместимые версии .NET Framework от версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="783db-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="783db-136">Сайт загрузки файлов — https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="783db-136">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="783db-137">**Visual Studio 2013 или более поздней версии**:</span><span class="sxs-lookup"><span data-stu-id="783db-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="783db-138">Профессиональный выпуск Visual Studio 2015 готов к использованию и доступен по адресу https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="783db-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="783db-139">Выпуск Visual Studio 2015 для сообщества пользователей доступен по адресу https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="783db-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="783db-140">Для этого выпуска требуется ручная установка инструментов разработчика Microsoft Office для Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="783db-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="783db-141">Инструменты разработчика Microsoft Office для Visual Studio доступны по адресу https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="783db-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="783db-142">**Учетная запись Project Online**: обеспечивает доступ к службе хостинга.</span><span class="sxs-lookup"><span data-stu-id="783db-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="783db-143">Дополнительные сведения о получении учетной записи Project Online см. здесь: https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="783db-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="783db-144">Убедитесь, что у пользователя надстройки есть достаточные права на доступ к некоторым проектам в клиенте Project Online.</span><span class="sxs-lookup"><span data-stu-id="783db-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="783db-145">**Проекты на сайте сайта** с данными.</span><span class="sxs-lookup"><span data-stu-id="783db-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="783db-146">Стандартная платформа .NET Framework — правильная используемая платформа.</span><span class="sxs-lookup"><span data-stu-id="783db-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="783db-147">Не используйте "клиентский профиль .NET Framework 4".</span><span class="sxs-lookup"><span data-stu-id="783db-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="783db-148">Настройка проекта Visual Studio</span><span class="sxs-lookup"><span data-stu-id="783db-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="783db-149">Настройка приложения состоит из создания нового проекта, связывания соответствующих библиотек и объявления необходимых пространств имен.</span><span class="sxs-lookup"><span data-stu-id="783db-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="783db-150">Visual Studio поддерживает нескольких типов проектов разработки.</span><span class="sxs-lookup"><span data-stu-id="783db-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="783db-151">Раздел является кратким и очень базовым.</span><span class="sxs-lookup"><span data-stu-id="783db-151">The section is brief and very basic.</span></span> <span data-ttu-id="783db-152">Значение заключается в том, что сведения объединены в одном месте.</span><span class="sxs-lookup"><span data-stu-id="783db-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="783db-153">Выберите проект Visual Studio</span><span class="sxs-lookup"><span data-stu-id="783db-153">Select a Visual Studio project</span></span>

<span data-ttu-id="783db-154">Чтобы создать проект соответствующего типа надстройки, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="783db-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="783db-155">Ключевые слова на экране имеют атрибут **Bold** :</span><span class="sxs-lookup"><span data-stu-id="783db-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="783db-156">В меню Файл выберите **файл** > **создать** > **проект**.</span><span class="sxs-lookup"><span data-stu-id="783db-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="783db-157">На левой панели в разделе Установленные шаблоны выберите пункт **C#** > **Office и** > **веб-** надстройки SharePoint.</span><span class="sxs-lookup"><span data-stu-id="783db-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="783db-158">В верхней части центральной панели выберите **.NET Framework 4** или более поздней версии. Текущая версия — 4,6.</span><span class="sxs-lookup"><span data-stu-id="783db-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="783db-159">В центральной области в разделе Типы приложений выберите надстройка **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="783db-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="783db-160">В нижней части укажите имя и расположение проекта, а также имя решения.</span><span class="sxs-lookup"><span data-stu-id="783db-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="783db-161">Кроме того, в нижней части установите флажок **Создать каталог для решения**.</span><span class="sxs-lookup"><span data-stu-id="783db-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="783db-162">Нажмите кнопку **ОК**, чтобы создать начальный проект.</span><span class="sxs-lookup"><span data-stu-id="783db-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="783db-163">Мастер Visual Studio запрашивает несколько дальнейших вопросов о сайте параметров Project Online (называемых параметрами SharePoint в диалоговых окнах) в нескольких следующих диалоговых окнах.</span><span class="sxs-lookup"><span data-stu-id="783db-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="783db-164">Вот вопросы:</span><span class="sxs-lookup"><span data-stu-id="783db-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="783db-165">Какой сайт SharePoint вы хотите использовать для отладки надстройки?</span><span class="sxs-lookup"><span data-stu-id="783db-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="783db-166">Укажите URL-адрес сайта PWA, например https://contoso.sharepoint.com/sites/pwa.</span><span class="sxs-lookup"><span data-stu-id="783db-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="783db-167">Как вы хотите разместить надстройку SharePoint?</span><span class="sxs-lookup"><span data-stu-id="783db-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="783db-168">Выберите [X] **размещаемую в SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="783db-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="783db-169">Для получения дополнительных сведений о надстройках SharePoint, в том числе о вариантах их хранения, обратитесь к разделу надстройки [SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="783db-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="783db-170">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="783db-170">Click **Next**.</span></span> 
    
<span data-ttu-id="783db-171">Во втором дополнительном диалоговом окне предлагается указать версию SharePoint Online для надстройки.</span><span class="sxs-lookup"><span data-stu-id="783db-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="783db-172">Какова самая ранняя версия SharePoint, которую вы хотите назначить надстройке?</span><span class="sxs-lookup"><span data-stu-id="783db-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="783db-173">Выберите [X] S **харепоинт-Online**.</span><span class="sxs-lookup"><span data-stu-id="783db-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="783db-174">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="783db-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="783db-175">Visual Studio создает проект и получает доступ к сайту Project Online.</span><span class="sxs-lookup"><span data-stu-id="783db-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="783db-176">Включение загрузки неопубликованных приложений на сайте Project Online</span><span class="sxs-lookup"><span data-stu-id="783db-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="783db-177">НеОпубликованный сервер — это механизм тестирования и отладки надстроек Project Online. Для загрузки неопубликованных приложений требуется два сценария: один — для включения неопубликованных приложений на сайте Project Online, а другой — для отключения загрузки неопубликованных приложений после тестирования и отладки надстройки.</span><span class="sxs-lookup"><span data-stu-id="783db-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="783db-178">Дополнительные сведения о настройке корпоративных приложений можно найти в статье Включение неОпубликованной копии [приложений в семействе веб-сайтов, не являющихся разработчиками](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span><span class="sxs-lookup"><span data-stu-id="783db-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="783db-179">Приложения для загрузки неОпубликованных приложений — это функция разработки и тестирования.</span><span class="sxs-lookup"><span data-stu-id="783db-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="783db-180">Он **не предназначен для производственного использования**.</span><span class="sxs-lookup"><span data-stu-id="783db-180">It is **not intended for production use**.</span></span> <span data-ttu-id="783db-181">Не Загрузка неопубликованных приложения регулярно или храните загрузку неопубликованных приложений дольше, чем вы активно используете эту функцию.</span><span class="sxs-lookup"><span data-stu-id="783db-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="783db-182">Добавление контента в проект надстройки</span><span class="sxs-lookup"><span data-stu-id="783db-182">Add content to the add-in project</span></span>

<span data-ttu-id="783db-183">После создания проекта и настройки механизма отладки Добавление контента в приложение включает в себя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="783db-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="783db-184">Настройка области применения приложения</span><span class="sxs-lookup"><span data-stu-id="783db-184">Setting the application scope</span></span>
    
- <span data-ttu-id="783db-185">Связывание библиотеки JSOM</span><span class="sxs-lookup"><span data-stu-id="783db-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="783db-186">Добавление элементов ПОЛЬЗОВАТЕЛЬСКОГО интерфейса в надстройку</span><span class="sxs-lookup"><span data-stu-id="783db-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="783db-187">Инициализация и подключение к службе Project Online</span><span class="sxs-lookup"><span data-stu-id="783db-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="783db-188">Получение проектов и сведений и свойств</span><span class="sxs-lookup"><span data-stu-id="783db-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="783db-189">Отображение проектов</span><span class="sxs-lookup"><span data-stu-id="783db-189">Displaying projects</span></span>
    
- <span data-ttu-id="783db-190">Отображение задач для проекта</span><span class="sxs-lookup"><span data-stu-id="783db-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="783db-191">Проект надстройки состоит из нескольких файлов.</span><span class="sxs-lookup"><span data-stu-id="783db-191">The add-in project consists of many files.</span></span> <span data-ttu-id="783db-192">В этом примере необходимо изменить следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="783db-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="783db-193">AppManifest. XML</span><span class="sxs-lookup"><span data-stu-id="783db-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="783db-194">Default. aspx</span><span class="sxs-lookup"><span data-stu-id="783db-194">Default.aspx</span></span>
    
- <span data-ttu-id="783db-195">App. js</span><span class="sxs-lookup"><span data-stu-id="783db-195">App.js</span></span>
    
- <span data-ttu-id="783db-196">App. CSS — необязательный; содержит определения стилей, разработанные для надстройки</span><span class="sxs-lookup"><span data-stu-id="783db-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="783db-197">Если клиент Project Online изменился (например, переход с пробной версии на сайт подписки), можно обновить свойства проекта, включая подключение сервера и URL-адрес сайта, используя окно свойств, доступное через \*\*\*\* > \*\*Свойства представления. \*\*Команда "окно".</span><span class="sxs-lookup"><span data-stu-id="783db-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="783db-198">Вы также можете добавлять файлы в проект.</span><span class="sxs-lookup"><span data-stu-id="783db-198">You can also add files to the project.</span></span> <span data-ttu-id="783db-199">В этом случае необходимо обновить файл Elements. XML, расположенный в той же группе (содержимое, изображения, страницы или скрипты), чтобы добавить новые файлы.</span><span class="sxs-lookup"><span data-stu-id="783db-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="783db-200">Дополнительные сведения о файлах проекта приведены в статье [изучение структуры манифеста приложения и пакета надстройки SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span><span class="sxs-lookup"><span data-stu-id="783db-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="783db-201">Задать область применения приложения</span><span class="sxs-lookup"><span data-stu-id="783db-201">Set application scope</span></span>

<span data-ttu-id="783db-202">Надстройке требуются уровни или уровни разрешений, определенные до того, как служба возвращает сведения в результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="783db-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="783db-203">Для этой надстройки используйте следующую область в проекте Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="783db-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="783db-204">Это изменение вносятся в файл AppManifest. XML на вкладке разрешения:</span><span class="sxs-lookup"><span data-stu-id="783db-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="783db-205">Scope</span><span class="sxs-lookup"><span data-stu-id="783db-205">Scope</span></span>|<span data-ttu-id="783db-206">Разрешение</span><span class="sxs-lookup"><span data-stu-id="783db-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="783db-207">Несколько проектов (Project Server)</span><span class="sxs-lookup"><span data-stu-id="783db-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="783db-208">Чтение</span><span class="sxs-lookup"><span data-stu-id="783db-208">Read</span></span>  <br/> |
   
<span data-ttu-id="783db-209">Сохраните файл после задания области применения приложения.</span><span class="sxs-lookup"><span data-stu-id="783db-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="783db-210">В противном случае данные из службы не будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="783db-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="783db-211">Связывание библиотеки JSOM</span><span class="sxs-lookup"><span data-stu-id="783db-211">Link the JSOM library</span></span>

<span data-ttu-id="783db-212">Библиотеки среды выполнения Project Online, PS. js и PS. Debug. js предоставляются в Project Online и всегда являются самыми последними версиями.</span><span class="sxs-lookup"><span data-stu-id="783db-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="783db-213">Надстройки JavaScript, использующие JSOM, должны ссылаться на одну из этих библиотек.</span><span class="sxs-lookup"><span data-stu-id="783db-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="783db-214">Определения ссылок добавляются в файл Default. aspx.</span><span class="sxs-lookup"><span data-stu-id="783db-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="783db-215">Команды для использования файла PS. js и/или PS. Debug. js являются частью кода, расположенного в файле App. js.</span><span class="sxs-lookup"><span data-stu-id="783db-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="783db-216">Добавьте указанную ниже команду для определения PS. js или PS. Debug. js в `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` элементе, подразделе "SharePoint: ScriptLink" для SP. js.</span><span class="sxs-lookup"><span data-stu-id="783db-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="783db-217">Атрибут **OnDemand** для PS. js или PS. Debug. js имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="783db-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="783db-218">Добавление элементов ПОЛЬЗОВАТЕЛЬСКОГО интерфейса в надстройку</span><span class="sxs-lookup"><span data-stu-id="783db-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="783db-219">Пример надстройки состоит из нескольких компонентов.</span><span class="sxs-lookup"><span data-stu-id="783db-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="783db-220">Описания статических элементов находятся в файле Default. aspx.</span><span class="sxs-lookup"><span data-stu-id="783db-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="783db-221">Описания динамических элементов и код для всех компонентов находятся в файле App. js.</span><span class="sxs-lookup"><span data-stu-id="783db-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="783db-222">Комментарии, касающиеся компонентов, можно найти в листингах исходного кода.</span><span class="sxs-lookup"><span data-stu-id="783db-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="783db-223">Ниже приведен список компонентов ПОЛЬЗОВАТЕЛЬСКОГО интерфейса в надстройке.</span><span class="sxs-lookup"><span data-stu-id="783db-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="783db-224">Заголовок</span><span class="sxs-lookup"><span data-stu-id="783db-224">Title</span></span>
    
- <span data-ttu-id="783db-225">Вводный многословные</span><span class="sxs-lookup"><span data-stu-id="783db-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="783db-226">Кнопка для удаления задач из таблицы</span><span class="sxs-lookup"><span data-stu-id="783db-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="783db-227">Таблица, в которой перечислены идентификатор проекта и его имя, а также сведения о задаче.</span><span class="sxs-lookup"><span data-stu-id="783db-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="783db-228">Кнопка "задачи" (копируется один раз для каждого проекта), который импортирует данные задачи в таблицу.</span><span class="sxs-lookup"><span data-stu-id="783db-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="783db-229">Подробные сведения о пользовательском интерфейсе, такие как заголовок и область заголовка таблицы Project, представлены в файле проекта Default. aspx.</span><span class="sxs-lookup"><span data-stu-id="783db-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="783db-230">Инициализация и подключение к обслуживающей системе</span><span class="sxs-lookup"><span data-stu-id="783db-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="783db-231">Файл App. js содержит код JavaScript.</span><span class="sxs-lookup"><span data-stu-id="783db-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="783db-232">Надстройка загружает в браузере PS. js, а затем вызывает функцию Инитиализепаже.</span><span class="sxs-lookup"><span data-stu-id="783db-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="783db-233">Инитиализепаже получает контекст конечной точки Project Online и запускает функцию Лоадпрожектс.</span><span class="sxs-lookup"><span data-stu-id="783db-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a><span data-ttu-id="783db-234">Получение проектов</span><span class="sxs-lookup"><span data-stu-id="783db-234">Retrieve the projects</span></span>

<span data-ttu-id="783db-235">Функция Лоадпрожектс запрашивает у службы имена и идентификаторы проектов.</span><span class="sxs-lookup"><span data-stu-id="783db-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="783db-236">Приложение извлекает имя проекта и идентификатор проекта. Другие сведения о проекте доступны, и доступ к ним можно получить, изменив метод Load, чтобы явным образом определить свойства для извлечения.</span><span class="sxs-lookup"><span data-stu-id="783db-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="783db-237">Пример представлен в коде в виде комментария.</span><span class="sxs-lookup"><span data-stu-id="783db-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="783db-238">Если запрос выполнен успешно, надстройка продолжается вызовом Дисплайпрожектс.</span><span class="sxs-lookup"><span data-stu-id="783db-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a><span data-ttu-id="783db-239">Отображение проектов</span><span class="sxs-lookup"><span data-stu-id="783db-239">Display the projects</span></span>

<span data-ttu-id="783db-240">Функция Дисплайпрожектс создает таблицу, одну строку для каждого проекта и кнопку для отображения задач для конкретного проекта.</span><span class="sxs-lookup"><span data-stu-id="783db-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="783db-241">Цикл while получает доступ к свойствам ID и Name.</span><span class="sxs-lookup"><span data-stu-id="783db-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="783db-242">Это немного отличается от проекта исходного кода, который вызывает функцию, которая, в свою очередь, обращается к тем же свойствам.</span><span class="sxs-lookup"><span data-stu-id="783db-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="783db-243">Отображение задач для проекта</span><span class="sxs-lookup"><span data-stu-id="783db-243">Display the tasks for a project</span></span>

<span data-ttu-id="783db-244">Задачи, в то время как часть надстройки, не являются частью начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="783db-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="783db-245">Если пользователь заинтересован в задачах, связанных с проектом, при нажатии кнопки "Show Tasks" задачи отображаются в списке с помощью обработчика событий Бтнлоадтаскс.</span><span class="sxs-lookup"><span data-stu-id="783db-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="783db-246">Обработчик событий Бтнлоадтаскс с соответствующим ИДЕНТИФИКАТОРом проекта запрашивает задачи для указанного проекта с сервера.</span><span class="sxs-lookup"><span data-stu-id="783db-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="783db-247">После извлечения Бтнлоадтаскс передает список задач в displayTasks для показа задач на экране.</span><span class="sxs-lookup"><span data-stu-id="783db-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

<span data-ttu-id="783db-248">Функция displayTasks отображает задачи, связанные с указанным проектом, непосредственно под записью проекта.</span><span class="sxs-lookup"><span data-stu-id="783db-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> <span data-ttu-id="783db-249">Цикл while получает доступ к свойствам идентификатора и имени задачи.</span><span class="sxs-lookup"><span data-stu-id="783db-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="783db-250">Это немного отличается от проекта исходного кода, который вызывает функцию, которая, в свою очередь, обращается к тем же свойствам.</span><span class="sxs-lookup"><span data-stu-id="783db-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="783db-251">Ниже приведены примеры выходных данных для задач одного проекта.</span><span class="sxs-lookup"><span data-stu-id="783db-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="783db-252">![Снимок экрана, на котором показаны выходные данные для задачи проекта] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Снимок экрана, на котором показаны выходные данные для задачи проекта")</span><span class="sxs-lookup"><span data-stu-id="783db-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="783db-253">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="783db-253">See also</span></span>

<span data-ttu-id="783db-254">Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="783db-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


