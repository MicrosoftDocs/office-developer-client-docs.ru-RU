---
title: Разработка с помощью клиентской объектной модели приложения Project Online
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: В этой статье описываются Microsoft Project Online разработки приложений для настольных приложений с помощью .NET Framework 4.0. Приложения, описанного в данной статье извлекает сведения из внешнего размещения сервера.
ms.openlocfilehash: a0a2b4042d4db127c56c5ba873ebe25418344571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812941"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="69c8b-104">Разработка с помощью клиентской объектной модели приложения Project Online</span><span class="sxs-lookup"><span data-stu-id="69c8b-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="69c8b-105">В этой статье описываются Microsoft Project Online разработки приложений для настольных приложений с помощью .NET Framework 4.0.</span><span class="sxs-lookup"><span data-stu-id="69c8b-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="69c8b-106">Приложения, описанного в данной статье извлекает сведения из внешнего размещения сервера.</span><span class="sxs-lookup"><span data-stu-id="69c8b-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="69c8b-107">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="69c8b-107">Background</span></span>

<span data-ttu-id="69c8b-108">Microsoft Project работы в качестве приложения для настольных систем в начале 1990-х годов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="69c8b-109">В настоящее время проекта — гораздо более как подтверждающим ее несколько видов:</span><span class="sxs-lookup"><span data-stu-id="69c8b-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="69c8b-110">Project standard edition — это приложения для настольных систем, на котором выполняется как автономное приложение.</span><span class="sxs-lookup"><span data-stu-id="69c8b-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="69c8b-111">Профессиональный выпуск Project — это настольное приложение, которое может взаимодействовать и общего доступа к данным с сервера на больший размер, а также выполнять функциональные возможности, обнаруженных в Project Стандартный выпуск.</span><span class="sxs-lookup"><span data-stu-id="69c8b-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="69c8b-112">Project Online — служба размещенных на ресурсах Майкрософт, которая предоставляет компании с PMO решения по координации усилий и управление проектов, программ и портфелей.</span><span class="sxs-lookup"><span data-stu-id="69c8b-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="69c8b-113">Различные предложения, чем выпусков для настольных компьютеров, Project Online для обслуживания и отслеживания сведений о проекте в течение всего жизненного цикла проекта.</span><span class="sxs-lookup"><span data-stu-id="69c8b-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="69c8b-114">Project Server — это службы, размещенной в enterprise в котором предприятия управляет и защищает сервер, содержащий проект, программы и сведения о портфеля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="69c8b-115">Project Server, поскольку они защита внутренних, server предлагает проекта, программы и компоненты портфеля ориентированную на внешне размещаемые Project Online в больше возможностей для настройки.</span><span class="sxs-lookup"><span data-stu-id="69c8b-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="69c8b-116">Project Online включает три online наборов API: объектной модели со стороны клиента (CSOM), объектная модель JavaScript (JSOM) и представлений состояния (REST).</span><span class="sxs-lookup"><span data-stu-id="69c8b-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="69c8b-117">Реализация .NET CSOM является предпочтительным интерфейса при разработке приложений Windows, которые взаимодействуют с Project Online клиентов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="69c8b-118">Типичная сред для приложения, ориентированные на пользователя включают настольных компьютеров Windows и Microsoft Surface устройств.</span><span class="sxs-lookup"><span data-stu-id="69c8b-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="69c8b-119">Приложения серверной написан с использованием .NET CSOM могут подключаться к другим серверам для бизнеса логики и источники данных, которые являются внешними по отношению к Project Online.</span><span class="sxs-lookup"><span data-stu-id="69c8b-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="69c8b-120">Запросы на извлечение для Project Online используйте систему LINQ как запрос, который содержит ряд улучшений извлечения основные функции.</span><span class="sxs-lookup"><span data-stu-id="69c8b-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="69c8b-121">Интерфейс объектной модели JavaScript (JSOM) обеспечивает поддержку браузеров для надстройки Project Online. Надстройка — это веб-приложения, которые хранятся в Project Online для клиентов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="69c8b-122">Если требуется запустить надстройку, код для надстройки файлы для загрузки и запущен в браузере на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="69c8b-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="69c8b-123">Этот интерфейс REST/Odata модель предоставляет связи на основе HTTP, рекомендуется для приложений в средах, отличных от Windows.</span><span class="sxs-lookup"><span data-stu-id="69c8b-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="69c8b-124">Конечные точки обмена данными — это объекты на сайте приложения Web Project (PWA).</span><span class="sxs-lookup"><span data-stu-id="69c8b-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="69c8b-125">Результаты предоставляют стандартные коды состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="69c8b-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="69c8b-126">В этой статье основное внимание уделяется приложение, использующее интерфейс .NET CSOM.</span><span class="sxs-lookup"><span data-stu-id="69c8b-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="69c8b-127">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="69c8b-127">Prerequisites</span></span>

<span data-ttu-id="69c8b-128">Начать с базовой системы под управлением Windows 10 и добавьте следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="69c8b-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="69c8b-129">.NET framework 4.0 или более поздней версии--используют структуру завершена.</span><span class="sxs-lookup"><span data-stu-id="69c8b-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="69c8b-130">Сайт загрузки — это https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="69c8b-130">The download site is https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="69c8b-131">Visual Studio 2013 или более поздней версии — любой выпуск приемлем.</span><span class="sxs-lookup"><span data-stu-id="69c8b-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="69c8b-132">Сообщество выпуск Visual Studio 2015 использовалась для разработки учебное приложение.</span><span class="sxs-lookup"><span data-stu-id="69c8b-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="69c8b-133">Выпуск сообщества доступном по адресу https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span><span class="sxs-lookup"><span data-stu-id="69c8b-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="69c8b-134">SharePoint Client Components SDK--Project Online и Project Server находятся на основе SharePoint и SharePoint сборки.</span><span class="sxs-lookup"><span data-stu-id="69c8b-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="69c8b-135">Клиентские компоненты SharePoint в Visual Studio Professional и корпоративные выпуски включены.</span><span class="sxs-lookup"><span data-stu-id="69c8b-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="69c8b-136">Если вы используете Visual Studio сообщества edition, последней версии пакета SDK средств разработчика Office доступна на следующем сайте: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span><span class="sxs-lookup"><span data-stu-id="69c8b-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="69c8b-137">Project Online учетной записи — это предоставляет доступ для размещения сайта.</span><span class="sxs-lookup"><span data-stu-id="69c8b-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="69c8b-138">Дополнительные сведения о получении учетной записи Project Online можно https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="69c8b-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="69c8b-139">Проекты на узле размещения, которые заполняются сведения</span><span class="sxs-lookup"><span data-stu-id="69c8b-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="69c8b-140">Стандартный .NET Framework (4.0 или более поздняя версия) — это правильный framework для использования.</span><span class="sxs-lookup"><span data-stu-id="69c8b-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="69c8b-141">Не используйте для клиентского профиля .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="69c8b-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="69c8b-142">Разработка приложения</span><span class="sxs-lookup"><span data-stu-id="69c8b-142">Develop the application</span></span>

<span data-ttu-id="69c8b-143">При разработке приложения для настольных систем для SharePoint, основной интерфейс — это проект клиентской объектной модели (CSOM).</span><span class="sxs-lookup"><span data-stu-id="69c8b-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="69c8b-144">Вы можете загрузить полный пример в https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span><span class="sxs-lookup"><span data-stu-id="69c8b-144">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="69c8b-145">В первых двух разделах рассматриваются основные проблемы: Создание проекта Visual Studio с помощью соответствующего пространства имен и сборки и доступ к серверу размещения.</span><span class="sxs-lookup"><span data-stu-id="69c8b-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="69c8b-146">Остальные разделы работают с извлечением информации о через CSOM, из одной и количество объектов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="69c8b-147">Получение сведений из узла — это процесс два действия из клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="69c8b-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="69c8b-148">Во-первых приложение указывает и отправляет запросы на извлечение одного или нескольких серверов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="69c8b-149">Во-вторых приложение выдает уведомление для выполнения запросов, отправленных на сервер.</span><span class="sxs-lookup"><span data-stu-id="69c8b-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="69c8b-150">Сервер отвечает, отправляя результаты запроса на клиенте.</span><span class="sxs-lookup"><span data-stu-id="69c8b-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="69c8b-151">Настройка проекта Visual Studio</span><span class="sxs-lookup"><span data-stu-id="69c8b-151">Set up the Visual Studio project</span></span>

<span data-ttu-id="69c8b-152">Настройка приложения состоит из создания нового проекта, связывания соответствующие сборки и объявление необходимых пространств имен.</span><span class="sxs-lookup"><span data-stu-id="69c8b-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="69c8b-153">Visual Studio содержит несколько типов проектов разработки.</span><span class="sxs-lookup"><span data-stu-id="69c8b-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="69c8b-154">Выбор проекта Visual Studio</span><span class="sxs-lookup"><span data-stu-id="69c8b-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="69c8b-155">Запустите Visual Studio и выберите команду **Начать новый проект** на начальной странице.</span><span class="sxs-lookup"><span data-stu-id="69c8b-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="69c8b-156">Диалоговое окно Новый проект отображает шаблоны доступных приложений и поля данных для любого выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="69c8b-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="69c8b-157">Для этого приложения укажите следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="69c8b-157">For this application, specify the following items.</span></span> <span data-ttu-id="69c8b-158">Ключевые слова, на экране иметь атрибут полужирного шрифта:</span><span class="sxs-lookup"><span data-stu-id="69c8b-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="69c8b-159">Установленные шаблоны в левой области выберите **C#** => **Windows** => **классического рабочего стола**.</span><span class="sxs-lookup"><span data-stu-id="69c8b-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="69c8b-160">В верхней области центра установите **.NET Framework 4**.</span><span class="sxs-lookup"><span data-stu-id="69c8b-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="69c8b-161">В списке типов приложения в центральной области выберите пункт **Консольное приложение**.</span><span class="sxs-lookup"><span data-stu-id="69c8b-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="69c8b-162">В нижней части укажите имя и расположение проекта и имя решения.</span><span class="sxs-lookup"><span data-stu-id="69c8b-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="69c8b-163">Также в нижней части установите флажок **Создать каталог для решения** .</span><span class="sxs-lookup"><span data-stu-id="69c8b-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="69c8b-164">Нажмите **кнопку ОК** , чтобы создать исходный проект.</span><span class="sxs-lookup"><span data-stu-id="69c8b-164">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="69c8b-165">Добавление сборок</span><span class="sxs-lookup"><span data-stu-id="69c8b-165">Add assemblies</span></span>

<span data-ttu-id="69c8b-166">Решения VS должен сборки ProjectServerClient из Project 2013 SDK, несколько сборки .NET Framework System.Security и сборки из пакета SDK SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69c8b-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="69c8b-167">В обозревателе решений VS щелкните правой кнопкой мыши элемент ссылки и выберите команду **Добавить ссылку**</span><span class="sxs-lookup"><span data-stu-id="69c8b-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="69c8b-168">в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="69c8b-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="69c8b-169">Установите флажок **Microsoft.ProjectServer.Client.dll**.</span><span class="sxs-lookup"><span data-stu-id="69c8b-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="69c8b-170">При необходимости нажмите кнопку **Обзор...**</span><span class="sxs-lookup"><span data-stu-id="69c8b-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="69c8b-171">кнопки в нижней части диалогового окна и перейдите в каталог установки пакета SDK Project 2013 для обнаружения сборки.</span><span class="sxs-lookup"><span data-stu-id="69c8b-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="69c8b-172">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="69c8b-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="69c8b-173">Добавление пространства имен клиента PrjoctServer CS-файл.</span><span class="sxs-lookup"><span data-stu-id="69c8b-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="69c8b-174">Добавьте пакет SDK для SharePoint 2013 сборки, с помощью консоли диспетчер пакетов NuGet.</span><span class="sxs-lookup"><span data-stu-id="69c8b-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="69c8b-175">Выберите в меню Сервис и выберите следующие меню: **средства =\> диспетчер пакетов NuGet =\> консоли диспетчера пакетов**.</span><span class="sxs-lookup"><span data-stu-id="69c8b-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="69c8b-176">В консоли диспетчера пакетов, введите следующую команду и нажмите клавишу \<ввод\>:</span><span class="sxs-lookup"><span data-stu-id="69c8b-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="69c8b-177">В **Консоли диспетчера пакетов** с описанием результатов команды; и в ссылки проекта в обозревателе решений VS отображаются сборки SharePoint.</span><span class="sxs-lookup"><span data-stu-id="69c8b-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="69c8b-178">Добавьте в файл .cs пространств имен:</span><span class="sxs-lookup"><span data-stu-id="69c8b-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="69c8b-179">System.Security сборка является частью .NET Framework и была установлена с помощью платформы.</span><span class="sxs-lookup"><span data-stu-id="69c8b-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="69c8b-180">Пример приложения должен один дополнительные пространство имен, содержащее зашифрованную строку для размещения системы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="69c8b-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="69c8b-181">После проверки подлинности для доступа проектов для размещения системы.</span><span class="sxs-lookup"><span data-stu-id="69c8b-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="69c8b-182">Добавьте пространство имен System.Security файл .cs таким образом:</span><span class="sxs-lookup"><span data-stu-id="69c8b-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="69c8b-183">В обозревателе решений VS щелкните правой кнопкой мыши элемент ссылки и выберите команду **Добавить ссылку**</span><span class="sxs-lookup"><span data-stu-id="69c8b-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="69c8b-184">в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="69c8b-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="69c8b-185">Выберите **сборки =\> Framework** в левой области диалогового окна Диспетчер справочные материалы, после чего проверьте **System.Security**.</span><span class="sxs-lookup"><span data-stu-id="69c8b-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="69c8b-186">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="69c8b-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="69c8b-187">Добавьте пространство имен System.Security CS-файл:</span><span class="sxs-lookup"><span data-stu-id="69c8b-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="69c8b-188">Начало CS-файл должен содержать следующие пространства имен:</span><span class="sxs-lookup"><span data-stu-id="69c8b-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="69c8b-189">Системный</span><span class="sxs-lookup"><span data-stu-id="69c8b-189">System</span></span>
    
- <span data-ttu-id="69c8b-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="69c8b-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="69c8b-191">System.Linq</span><span class="sxs-lookup"><span data-stu-id="69c8b-191">System.Linq</span></span>
    
- <span data-ttu-id="69c8b-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="69c8b-192">System.Test</span></span>
    
- <span data-ttu-id="69c8b-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="69c8b-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="69c8b-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="69c8b-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="69c8b-195">System.Security</span><span class="sxs-lookup"><span data-stu-id="69c8b-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="69c8b-196">Подключения к системе узла</span><span class="sxs-lookup"><span data-stu-id="69c8b-196">Connect to the host system</span></span>

<span data-ttu-id="69c8b-197">Project Online — это приложение SharePoint, поэтому с использованием проверки подлинности SharePoint — это правильный подход.</span><span class="sxs-lookup"><span data-stu-id="69c8b-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="69c8b-198">В следующем фрагменте кода подготавливает получить доступ к размещенной среде.</span><span class="sxs-lookup"><span data-stu-id="69c8b-198">The following code fragment prepares to access the hosted environment.</span></span>
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

<span data-ttu-id="69c8b-199">Действия по подготовке получить доступ к размещенной среде включают следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="69c8b-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="69c8b-200">Создать объект context для проектов — это содержится в следующем коде выше.</span><span class="sxs-lookup"><span data-stu-id="69c8b-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="69c8b-201">Контекст наследуется от других компонентов, позволяя системы для управления контекста объектной модели проектов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="69c8b-202">Определение сайта узла — это делается в следующем коде с выше.</span><span class="sxs-lookup"><span data-stu-id="69c8b-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="69c8b-203">При создании экземпляра контекста проекты, приложению для предоставления корневого семейства веб-сайтов проектов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="69c8b-204">Приложение использует подстроки URL-адрес корня проектов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="69c8b-205">Моментальный снимок вложенным папкам будет выделена с красный прямоугольник на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="69c8b-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="69c8b-206">Проверка подлинности должна строку с его начала через подстроки «веб-клиента Project».</span><span class="sxs-lookup"><span data-stu-id="69c8b-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="69c8b-207">В пример кода, приложение использует строку "https://XXXXXXXX.sharepoint.com/sites/pwa«.</span><span class="sxs-lookup"><span data-stu-id="69c8b-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="69c8b-208">![Изображение URL-адрес семейства сайтов проектов в рамках красной границей.] (media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Снимок экрана URL-адрес проектов веб-сайтов семейства сайтов в пределах красной границы")</span><span class="sxs-lookup"><span data-stu-id="69c8b-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="69c8b-209">Поместите пароль в защищенной строки — это делается в следующем коде с выше.</span><span class="sxs-lookup"><span data-stu-id="69c8b-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="69c8b-210">Учетная запись пользователя и пароль — учетные данные для доступа к сайту узла.</span><span class="sxs-lookup"><span data-stu-id="69c8b-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="69c8b-211">Добавьте учетную запись пользователя и пароль в область учетные данные объекта контекста — это делается в следующем коде с выше.</span><span class="sxs-lookup"><span data-stu-id="69c8b-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="69c8b-212">Контекст инициализированный проекта готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="69c8b-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="69c8b-213">Список всех опубликованных проектов</span><span class="sxs-lookup"><span data-stu-id="69c8b-213">List all published projects</span></span>

<span data-ttu-id="69c8b-214">Project Online и ProjectServer использовать прокси-серверы для связи с сервером для создания, отчет, обновления и удаления (CRUD) операции.</span><span class="sxs-lookup"><span data-stu-id="69c8b-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="69c8b-215">Сервер обрабатывает запросы эффективно и имеет клиента выполните следующие действия в связи с сервером:</span><span class="sxs-lookup"><span data-stu-id="69c8b-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="69c8b-216">Установите контекст для обмена данными.</span><span class="sxs-lookup"><span data-stu-id="69c8b-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="69c8b-217">Контекст используется коллекции проектов, а также другие объекты и коллекции через наследование, включая коллекции задачи, семейства назначений, объект рабочей области и настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="69c8b-218">Использование объектной модели для указания объекта, семейства сайтов или данные требуется получить.</span><span class="sxs-lookup"><span data-stu-id="69c8b-218">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="69c8b-219">Этот шаг использует LINQ, как запрос или метод.</span><span class="sxs-lookup"><span data-stu-id="69c8b-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="69c8b-220">Спецификации определяет, вы получаете.</span><span class="sxs-lookup"><span data-stu-id="69c8b-220">The specification controls what you receive.</span></span> <span data-ttu-id="69c8b-221">Часто это действие встраивается в теле метода Load (шаг 3).</span><span class="sxs-lookup"><span data-stu-id="69c8b-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="69c8b-222">Загрузка спецификации извлечения на предыдущем шаге, с помощью метода Load() или LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="69c8b-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="69c8b-223">Для загрузки коллекций и объектов, используйте Load().</span><span class="sxs-lookup"><span data-stu-id="69c8b-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="69c8b-224">Для запросов с помощью предложения, такие как «места» и «группировать», используйте LoadQuery().</span><span class="sxs-lookup"><span data-stu-id="69c8b-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="69c8b-225">Выполнение запроса с помощью метода ExecuteQuery().</span><span class="sxs-lookup"><span data-stu-id="69c8b-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="69c8b-226">Метод ExecuteQuery() уведомляет узел, все готово для выполнения запросов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="69c8b-227">Когда узел получает уведомление, выполняет запросы и отправляет результаты клиенту.</span><span class="sxs-lookup"><span data-stu-id="69c8b-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="69c8b-228">Данные на клиенте приложение может использовать его.</span><span class="sxs-lookup"><span data-stu-id="69c8b-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="69c8b-229">В следующем фрагменте кода циклический перебор опубликованных проектов и печатает Id и Name для каждого опубликованного проекта на узле.</span><span class="sxs-lookup"><span data-stu-id="69c8b-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

<span data-ttu-id="69c8b-230">Выходные данные:</span><span class="sxs-lookup"><span data-stu-id="69c8b-230">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="69c8b-231">Для выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="69c8b-231">Make a request</span></span>

<span data-ttu-id="69c8b-232">Использование действий в этом фрагменте кода, приложение получает список проектов в указанную учетную запись на узле размещения.</span><span class="sxs-lookup"><span data-stu-id="69c8b-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="69c8b-233">Для проектов, которые перечислены указан ProjectContext.</span><span class="sxs-lookup"><span data-stu-id="69c8b-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="69c8b-234">Укажите элемента для извлечения.</span><span class="sxs-lookup"><span data-stu-id="69c8b-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="69c8b-235">С помощью только о том, коллекцию, сервер получает коллекции проектов, заполнение каждого проекта со значениями по умолчанию набор свойств.</span><span class="sxs-lookup"><span data-stu-id="69c8b-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="69c8b-236">Доступ к свойствам, которые входят в состав набора свойств по умолчанию предоставляет успешные результаты.</span><span class="sxs-lookup"><span data-stu-id="69c8b-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="69c8b-237">Доступ к свойствам, которые не являются частью по умолчанию задайте результаты исключение «Не инициализирован».</span><span class="sxs-lookup"><span data-stu-id="69c8b-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="69c8b-238">Загрузите запрос (projContext.Load).</span><span class="sxs-lookup"><span data-stu-id="69c8b-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="69c8b-239">Это входит в предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="69c8b-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="69c8b-240">Выполнение запроса (ExecuteQuery).</span><span class="sxs-lookup"><span data-stu-id="69c8b-240">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="69c8b-241">Получение сведений высокого уровня проекта</span><span class="sxs-lookup"><span data-stu-id="69c8b-241">Retrieve high-level project information</span></span>

<span data-ttu-id="69c8b-242">Свойства, которые не являются свойства по умолчанию должно быть указано в запросе на сервер.</span><span class="sxs-lookup"><span data-stu-id="69c8b-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="69c8b-243">В следующем фрагменте кода загружает контекста семейства проекты как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="69c8b-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="69c8b-244">Затем спецификации запрашивает дополнительные свойства не по умолчанию, необходимо включить в результат.</span><span class="sxs-lookup"><span data-stu-id="69c8b-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="69c8b-245">Инструкция load определяет контекст коллекции проектов и добавляет StartDate, фазы и стадии в результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="69c8b-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="69c8b-246">Дополнительные свойства могут быть скалярные, объектов и коллекций.</span><span class="sxs-lookup"><span data-stu-id="69c8b-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="69c8b-247">Скалярные элементов возможен непосредственно.</span><span class="sxs-lookup"><span data-stu-id="69c8b-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="69c8b-248">Объекты и коллекции требуют дополнительной обработки, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="69c8b-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

<span data-ttu-id="69c8b-249">Выходные данные первых трех проектов:</span><span class="sxs-lookup"><span data-stu-id="69c8b-249">Output of the first three projects:</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="69c8b-250">Извлечение всех задач в проекте</span><span class="sxs-lookup"><span data-stu-id="69c8b-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="69c8b-251">Каждый проект имеет многих задач.</span><span class="sxs-lookup"><span data-stu-id="69c8b-251">Each project has many tasks.</span></span> <span data-ttu-id="69c8b-252">Таким образом помещение задачи для отдельного проекта состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="69c8b-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="69c8b-253">Установите контекст коллекции проектов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="69c8b-254">Получение сведений о проекте, включая свойства задачи.</span><span class="sxs-lookup"><span data-stu-id="69c8b-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="69c8b-255">Обратите внимание, что приложение является адресации опубликованных проектов.</span><span class="sxs-lookup"><span data-stu-id="69c8b-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="69c8b-256">Контекст для текущего опубликованного проекта — pubProj.</span><span class="sxs-lookup"><span data-stu-id="69c8b-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="69c8b-257">Установите контекст для коллекции задачи.</span><span class="sxs-lookup"><span data-stu-id="69c8b-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="69c8b-258">`pubProj.Tasks` Свойство ссылается на задачи текущего опубликованного проекта.</span><span class="sxs-lookup"><span data-stu-id="69c8b-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="69c8b-259">Загрузите спецификацию, чтобы получить коллекцию задач, в том числе соответствующие свойства не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69c8b-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="69c8b-260">Выполнение запроса для извлечения коллекций задач с помощью соответствующих свойств.</span><span class="sxs-lookup"><span data-stu-id="69c8b-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="69c8b-261">Информация теперь является локальной.</span><span class="sxs-lookup"><span data-stu-id="69c8b-261">The information is now local.</span></span> <span data-ttu-id="69c8b-262">В следующем фрагменте кода обрабатывает семейства сайтов опубликованных задачи, написав сведения на консоль.</span><span class="sxs-lookup"><span data-stu-id="69c8b-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

<span data-ttu-id="69c8b-263">Выходные данные задачи для одного проекта:</span><span class="sxs-lookup"><span data-stu-id="69c8b-263">Output of tasks for one project:</span></span>
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="69c8b-264">Сведения о доступе на нескольких уровнях</span><span class="sxs-lookup"><span data-stu-id="69c8b-264">Access information at multiple levels</span></span>

<span data-ttu-id="69c8b-265">Каждой задачи может иметь один или несколько лиц (известной как</span><span class="sxs-lookup"><span data-stu-id="69c8b-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="69c8b-266">ресурс), что обеспечивает до его завершения.</span><span class="sxs-lookup"><span data-stu-id="69c8b-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="69c8b-267">Коллекции назначений и ресурсы содержат эти сведения для каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="69c8b-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="69c8b-268">Обработка состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="69c8b-268">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="69c8b-269">Получение контекста для задачи проекта.</span><span class="sxs-lookup"><span data-stu-id="69c8b-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="69c8b-270">Создание запроса и загружать запроса для назначений, которые привязаны к задаче.</span><span class="sxs-lookup"><span data-stu-id="69c8b-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="69c8b-271">Выполнение запроса для назначений.</span><span class="sxs-lookup"><span data-stu-id="69c8b-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="69c8b-272">Создание запроса и загрузки запрос на ресурс, связанный с индивидуального назначения.</span><span class="sxs-lookup"><span data-stu-id="69c8b-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="69c8b-273">Выполнение запроса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="69c8b-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="69c8b-274">Семейства назначений явно запрошено данные с сервера, так как он не является свойством по умолчанию коллекции задачи.</span><span class="sxs-lookup"><span data-stu-id="69c8b-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="69c8b-275">Как семейство последующие запрос выполняется для семейства сайтов с сервера по запросу.</span><span class="sxs-lookup"><span data-stu-id="69c8b-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="69c8b-276">Ресурс — это объект.</span><span class="sxs-lookup"><span data-stu-id="69c8b-276">The Resource is an object.</span></span> <span data-ttu-id="69c8b-277">Запрос для назначения включает в себя имя ресурса, связанного с назначением.</span><span class="sxs-lookup"><span data-stu-id="69c8b-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

<span data-ttu-id="69c8b-278">Выходные данные для задач, 52, 75 и 76 проекта:</span><span class="sxs-lookup"><span data-stu-id="69c8b-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="69c8b-279">Настраиваемые корпоративные поля доступа</span><span class="sxs-lookup"><span data-stu-id="69c8b-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="69c8b-280">Настраиваемые поля существует для Project Online.</span><span class="sxs-lookup"><span data-stu-id="69c8b-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="69c8b-281">Это корпоративные поля, которые могут быть связаны с отдельными проекта.</span><span class="sxs-lookup"><span data-stu-id="69c8b-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="69c8b-282">В этом разделе описывается, как получить доступ к эти поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="69c8b-283">Настраиваемые поля не включаются в набор по умолчанию свойства, связанные с проектом.</span><span class="sxs-lookup"><span data-stu-id="69c8b-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="69c8b-284">Таким образом они должны явные идентификации в спецификации извлечения.</span><span class="sxs-lookup"><span data-stu-id="69c8b-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="69c8b-285">Высокоуровневое представление процесса состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="69c8b-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="69c8b-286">Переход с помощью его общее имя настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="69c8b-287">Получение внутреннее имя настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="69c8b-288">Вернуться к глобального контекста и серверов запросов системы, с помощью внутреннее имя настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="69c8b-289">Переход в настраиваемых полей, извлечение внутреннего имени и используется для запроса системы</span><span class="sxs-lookup"><span data-stu-id="69c8b-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="69c8b-290">Эта задача указывает извлечения, использующего свойство не по умолчанию с помощью одного добавлены подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="69c8b-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="69c8b-291">Начните с помощью контекста проектов, как описано в начале этой статьи.</span><span class="sxs-lookup"><span data-stu-id="69c8b-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="69c8b-292">Добавьте два элемента для получения запроса по извлечения коллекции проектов в дополнение к другим свойствам не по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="69c8b-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="69c8b-293">`p => p.IncludeCustomFields` Предложение определяет необходимость использования объекта проекта, который поддерживает настраиваемые поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="69c8b-294">`p => p.IncludeCustomFields.CustomFields` Предложение запрашивает включения настраиваемых полей базы данных в результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="69c8b-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="69c8b-295">Эти сведения используются после получения внутреннее имя настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="69c8b-296">Загрузите запрос.</span><span class="sxs-lookup"><span data-stu-id="69c8b-296">Load the request.</span></span>
    
   <span data-ttu-id="69c8b-297">Это входит в предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="69c8b-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="69c8b-298">Выполнение запроса.</span><span class="sxs-lookup"><span data-stu-id="69c8b-298">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="69c8b-299">Эти сведения на стороне клиента создавайте запрос на извлечение настраиваемых полей, сопоставленных с текущим проектом.</span><span class="sxs-lookup"><span data-stu-id="69c8b-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="69c8b-300">Перейдите в соответствующий настраиваемого поля и получить внутреннее имя поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="69c8b-301">Получить внутреннее имя настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="69c8b-302">Высокоуровневая элементы 1 и 2 завершены.</span><span class="sxs-lookup"><span data-stu-id="69c8b-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="69c8b-303">Вернитесь в контексте проекта и извлечения значения настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="69c8b-304">Значения настраиваемого поля извлекаются с помощью внутреннее имя в качестве индекса.</span><span class="sxs-lookup"><span data-stu-id="69c8b-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="69c8b-305">Выходные данные из трех проектов, состоящий из кода проекта, имя проекта, имя настраиваемого поля, внутреннее имя настраиваемого поля и значения настраиваемого поля.</span><span class="sxs-lookup"><span data-stu-id="69c8b-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a><span data-ttu-id="69c8b-306">См. также</span><span class="sxs-lookup"><span data-stu-id="69c8b-306">See also</span></span>

<span data-ttu-id="69c8b-307">Документация и примеры, связанные с Project Online и разработки приложений с помощью CSOM в разделе [Портал проектов разработки](http://dev.office.com/project.aspx).</span><span class="sxs-lookup"><span data-stu-id="69c8b-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](http://dev.office.com/project.aspx).</span></span>
    

