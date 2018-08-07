---
title: Приступая к работе с объектной моделью Project Server 2013 JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: В Project Server 2013 объектной модели JavaScript можно использовать в Project Online разработке для мобильных устройств и локально. В этом разделе представлен краткий обзор объектной модели JavaScript, а затем описывается, как создать страницу приложения, которая извлекает и итерацию проектов с помощью объектной модели JavaScript.
ms.openlocfilehash: 94c882249474e22328031d55233cfba654dcff83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812931"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a><span data-ttu-id="84e2b-104">Приступая к работе с объектной моделью Project Server 2013 JavaScript</span><span class="sxs-lookup"><span data-stu-id="84e2b-104">Getting started with the Project Server 2013 JavaScript object model</span></span>

<span data-ttu-id="84e2b-105">В Project Server 2013 объектной модели JavaScript можно использовать в Project Online разработке для мобильных устройств и локально.</span><span class="sxs-lookup"><span data-stu-id="84e2b-105">In Project Server 2013, the JavaScript object model can be used in Project Online, mobile, and on-premise development.</span></span> <span data-ttu-id="84e2b-106">В этом разделе представлен краткий обзор объектной модели JavaScript, а затем описывается, как создать страницу приложения, которая извлекает и итерацию проектов с помощью объектной модели JavaScript.</span><span class="sxs-lookup"><span data-stu-id="84e2b-106">This topic provides a brief overview of the JavaScript object model and then describes how to create an application page that retrieves and iterates through projects by using the JavaScript object model.</span></span>
  
## <a name="using-the-project-server-javascript-object-model"></a><span data-ttu-id="84e2b-107">С помощью объектной модели Project Server JavaScript</span><span class="sxs-lookup"><span data-stu-id="84e2b-107">Using the Project Server JavaScript object model</span></span>
<span data-ttu-id="84e2b-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="84e2b-108"></span></span>

<span data-ttu-id="84e2b-109">С помощью объектной модели JavaScript — это отличный способ для создания приложений, на котором работает со стороны клиента (в отличие от клиентского управляемого кода, которое необходимо запускать удаленно).</span><span class="sxs-lookup"><span data-stu-id="84e2b-109">Using the JavaScript object model is a great way to create an app that runs client-side (as opposed to managed client code which needs to run remotely).</span></span> <span data-ttu-id="84e2b-110">Приложения могут использовать объектной модели JavaScript для извлечения или изменения объектов, отправив асинхронных вызовов на сервер.</span><span class="sxs-lookup"><span data-stu-id="84e2b-110">Apps can use the JavaScript object model to retrieve or change objects by sending asynchronous calls to the server.</span></span> <span data-ttu-id="84e2b-111">Приложений, использующих объектную модель JavaScript обычно развертываются как настраиваемые надстройки SharePoint, страницы приложений и веб-частей.</span><span class="sxs-lookup"><span data-stu-id="84e2b-111">Apps that use the JavaScript object model are typically deployed as custom SharePoint Add-ins, application pages, and Web Parts.</span></span> <span data-ttu-id="84e2b-112">Для получения дополнительных сведений см. «Типы компонентов SharePoint, которые могут находиться в приложении для SharePoint» в [хост-сайты, добавьте в веб-сайтов и компоненты SharePoint в SharePoint 2013](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="84e2b-112">For more information, see "Types of SharePoint components that can be in an app for SharePoint" in [Host webs, add-in webs, and SharePoint components in SharePoint 2013](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="84e2b-113">Объектная модель JavaScript реализует основные функциональные возможности Project Server 2013, но объектная модель JavaScript и серверной объектной модели не имеют возможности один к одному.</span><span class="sxs-lookup"><span data-stu-id="84e2b-113">The JavaScript object model implements the main functionality of Project Server 2013, but the JavaScript object model and the server object model do not have one-to-one parity.</span></span> <span data-ttu-id="84e2b-114">Точка входа в объектной модели JavaScript — это объект **ProjectContext** , который представляет контекст клиента для Project Server 2013 и предоставляет доступ к содержимому сервера и функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="84e2b-114">The entry point to the JavaScript object model is the **ProjectContext** object, which represents the client context for Project Server 2013 and provides access to server content and functionality.</span></span> <span data-ttu-id="84e2b-115">Объектная модель JavaScript для Project Server 2013 определяется в файле PS.js, который находится в каталоге путь по умолчанию `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` на сервере приложений.</span><span class="sxs-lookup"><span data-stu-id="84e2b-115">The JavaScript object model for Project Server 2013 is defined in the PS.js file, which is located in the default path  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` on the application server.</span></span> <span data-ttu-id="84e2b-116">Project Server 2013 также устанавливается PS. Файл Debug.js в одном месте.</span><span class="sxs-lookup"><span data-stu-id="84e2b-116">Project Server 2013 also installs the PS.Debug.js file in the same location.</span></span> <span data-ttu-id="84e2b-117">PS. Debug.js является более unminified версии PS.js, который предоставляет сведения IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="84e2b-117">PS.Debug.js is an unminified version of PS.js that provides IntelliSense information.</span></span> 
  
<span data-ttu-id="84e2b-118">Объектная модель JavaScript позволяет проверка подлинности через формы, а все запросы проходят проверку подлинности имени текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="84e2b-118">The JavaScript object model allows Forms authentication, and all requests are authenticated as the current user.</span></span> <span data-ttu-id="84e2b-119">Дополнительные сведения о безопасности и рекомендации по разработке пользовательских приложений и решений см в разделе [Проверка подлинности, авторизации и безопасности в SharePoint 2013](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx) [важные аспекты архитектуры SharePoint надстройки и разработки Альбомная](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)и [надстройки SharePoint по сравнению с решениями SharePoint](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="84e2b-119">For more information about security and other considerations for designing custom apps and solutions, see [Authentication, authorization, and security in SharePoint 2013](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Important aspects of the SharePoint Add-in architecture and development landscape](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and [SharePoint Add-ins compared with SharePoint solutions](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="84e2b-120">Удаленный доступ к данным на сайте SharePoint, SharePoint 2013 предоставляет междоменной библиотеки, которая позволяет выполнять междоменных вызовов со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="84e2b-120">To access data from a SharePoint site remotely, SharePoint 2013 provides a cross-domain library that enables you to make client-side cross-domain calls.</span></span> <span data-ttu-id="84e2b-121">Для получения дополнительных сведений см [доступа к SharePoint 2013 данные из надстроек с помощью междоменной библиотеки](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="84e2b-121">For more information, see [Access SharePoint 2013 data from add-ins using the cross-domain library](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="84e2b-122">Многие основные понятия и процессы, используемые для использования объектной модели JavaScript для Project Server 2013 похожи в связанных с ними клиентских объектных моделей.</span><span class="sxs-lookup"><span data-stu-id="84e2b-122">Many concepts and processes for using the JavaScript object model for Project Server 2013 resemble those in related client object models.</span></span> <span data-ttu-id="84e2b-123">Дополнительные сведения о Project Server 2013 управляемой клиентской объектной модели можно **Microsoft.ProjectServer.Client**.</span><span class="sxs-lookup"><span data-stu-id="84e2b-123">For more information about the Project Server 2013 managed client object model, see **Microsoft.ProjectServer.Client**.</span></span> <span data-ttu-id="84e2b-124">Дополнительные сведения об объектной модели SharePoint 2013JavaScript и управляемой клиентской объектной модели можно [выполнения основных операций с использованием кода библиотеки JavaScript в SharePoint 2013](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) и [выполнения базовых операций, с помощью клиента SharePoint 2013 код библиотеки](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="84e2b-124">For more information about the SharePoint 2013JavaScript object model and managed client object model, see [Complete basic operations using JavaScript library code in SharePoint 2013](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) and [Complete basic operations using SharePoint 2013 client library code](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span></span>
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="84e2b-125">Пошаговое руководство: Создание страницы приложения, которое получает и выполняется итерация по проектам</span><span class="sxs-lookup"><span data-stu-id="84e2b-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="84e2b-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="84e2b-126"></span></span>

<span data-ttu-id="84e2b-127">Узнайте, как создать страницу приложения, которое отображает идентификатор, имя и даты создания каждого опубликованного проекта на сайте.</span><span class="sxs-lookup"><span data-stu-id="84e2b-127">Learn how to create an application page that displays the ID, name, and created date of each published project in a site.</span></span>
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="84e2b-128">Необходимые условия для создания страницы приложения, которое получает и выполняется итерация по проектам</span><span class="sxs-lookup"><span data-stu-id="84e2b-128">Prerequisites for creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="84e2b-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="84e2b-129"></span></span>

<span data-ttu-id="84e2b-130">Чтобы разработать страницу приложения, описанного в данном разделе, необходимо установить и настроить следующих продуктов:</span><span class="sxs-lookup"><span data-stu-id="84e2b-130">To develop the application page that is described in this topic, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="84e2b-131">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="84e2b-131">SharePoint Server 2013</span></span>
- <span data-ttu-id="84e2b-132">Project Server 2013 с помощью по крайней мере один опубликованного проекта</span><span class="sxs-lookup"><span data-stu-id="84e2b-132">Project Server 2013 with at least one published project</span></span>
- <span data-ttu-id="84e2b-133">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="84e2b-133">Visual Studio 2012</span></span>
- <span data-ttu-id="84e2b-134">Инструменты разработчика Office для Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="84e2b-134">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="84e2b-135">Кроме того, необходимо иметь разрешения для развертывания расширения для SharePoint Server 2013 и для получения проектов.</span><span class="sxs-lookup"><span data-stu-id="84e2b-135">You must also have permissions to deploy the extension to SharePoint Server 2013 and to retrieve projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="84e2b-136">Эти инструкции предполагают, что вы работаете на компьютере, на котором работает Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="84e2b-136">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a><span data-ttu-id="84e2b-137">Создание страницы приложения в Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="84e2b-137">Creating the application page in Visual Studio 2012</span></span>
<span data-ttu-id="84e2b-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span><span class="sxs-lookup"><span data-stu-id="84e2b-138"></span></span>

<span data-ttu-id="84e2b-139">Следующие шаги создания проекта SharePoint и страницу приложения, которая содержит таблицы и метку.</span><span class="sxs-lookup"><span data-stu-id="84e2b-139">The following steps create a SharePoint project and an application page that contains a table and label.</span></span> <span data-ttu-id="84e2b-140">В таблице показаны сведения о проектах, и отображает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="84e2b-140">The table displays information about the projects and the label displays error messages.</span></span>
  
1. <span data-ttu-id="84e2b-141">На компьютере, на котором работает Project Server 2013 запустите Visual Studio 2012 с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="84e2b-141">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="84e2b-142">Создайте пустой проект SharePoint 2013, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="84e2b-142">Create an empty SharePoint 2013 project, as follows:</span></span>
    
    1. <span data-ttu-id="84e2b-143">В диалоговом окне **Новый проект** выберите **.NET Framework 4.5** из раскрывающегося списка в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="84e2b-143">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
        
    2. <span data-ttu-id="84e2b-144">В списке категории шаблонов выберите категорию **Office SharePoint** и затем выберите шаблон **Проекта SharePoint 2013** .</span><span class="sxs-lookup"><span data-stu-id="84e2b-144">In the list of template categories, choose the **Office SharePoint** category, and then choose the **SharePoint 2013 Project** template.</span></span> 
        
    3. <span data-ttu-id="84e2b-145">Назовите проект GetProjectsJSOM и затем нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="84e2b-145">Name the project GetProjectsJSOM, and then choose the **OK** button.</span></span> 
        
    4. <span data-ttu-id="84e2b-146">В диалоговом окне **Мастер настройки SharePoint** выберите **Развернуть как решение фермы**и затем нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="84e2b-146">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="84e2b-147">В окне Обозреватель решений, изменить значение свойства **URL-адрес сайта** проекта **ProjectsJSOM** в соответствии с URL-адрес экземпляра Project Web App (например, `http://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="84e2b-147">In Solution Explorer, edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `http://ServerName/PWA`).</span></span>
    
4. <span data-ttu-id="84e2b-148">Откройте контекстное меню для проекта **GetProjectsJSOM** , а затем добавьте SharePoint «Макеты» сопоставленная папка.</span><span class="sxs-lookup"><span data-stu-id="84e2b-148">Open the shortcut menu for the **GetProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
5. <span data-ttu-id="84e2b-149">В папке **Layouts** откройте контекстное меню для папки **GetProjectsJSOM** и добавьте новую страницу приложения SharePoint с именем ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="84e2b-149">In the **Layouts** folder, open the shortcut menu for the **GetProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="84e2b-150">В этом примере не используется файл фонового кода, который создает Visual Studio 2012 страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="84e2b-150">This example does not use the code-behind file that Visual Studio 2012 creates for the application page.</span></span> 
  
6. <span data-ttu-id="84e2b-151">Откройте контекстное меню для страницы **ProjectsList.aspx** и выберите команду **назначить элемент**.</span><span class="sxs-lookup"><span data-stu-id="84e2b-151">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
7. <span data-ttu-id="84e2b-152">В разметке страницы **ProjectsList.aspx** определите таблицу и заполнитель сообщения внутри тегов **asp: Content** «Главная», как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="84e2b-152">In the markup for the **ProjectsList.aspx** page, define a table and a message placeholder inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
    ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Project name</th>
            <th width="25%" align="left">Created date</th>
            <th width="50%" align="left">Project ID</th>
        </tr>
    </table>
    <div id="divMessage">
        <br/>
        <span id="spanMessage" style="color: #FF0000;"></span>
    </div>
    ```

### <a name="retrieving-the-projects-collection"></a><span data-ttu-id="84e2b-153">Получение коллекции проектов</span><span class="sxs-lookup"><span data-stu-id="84e2b-153">Retrieving the projects collection</span></span>
<span data-ttu-id="84e2b-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="84e2b-154"></span></span>

<span data-ttu-id="84e2b-155">Следующие шаги извлечения и инициализация коллекции проектов.</span><span class="sxs-lookup"><span data-stu-id="84e2b-155">The following steps retrieve and initialize the projects collection.</span></span>
  
1. <span data-ttu-id="84e2b-156">После закрывающего тега **div** , добавьте тег **SharePoint:ScriptLink** , который ссылается на файл PS.js, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="84e2b-156">After the closing **div** tag, add a **SharePoint:ScriptLink** tag that references the PS.js file, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. <span data-ttu-id="84e2b-157">Под тегом **SharePoint:ScriptLink** добавьте теги **сценария** следующим образом.</span><span class="sxs-lookup"><span data-stu-id="84e2b-157">Below the **SharePoint:ScriptLink** tag, add **script** tags, as follows.</span></span> 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. <span data-ttu-id="84e2b-158">Объявите глобальную переменную для хранения коллекции проектов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="84e2b-158">Declare a global variable to store the projects collection, as follows.</span></span>
    
   ```js
   var projects;
   ```

4. <span data-ttu-id="84e2b-159">Вызов **SP. SOD.executeOrDelayUntilScriptLoaded** метод, чтобы гарантировать, что файл PS.js загружается перед выполнением пользовательского кода.</span><span class="sxs-lookup"><span data-stu-id="84e2b-159">Call the **SP.SOD.executeOrDelayUntilScriptLoaded** method to ensure that the PS.js file is loaded before your custom code runs.</span></span> 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. <span data-ttu-id="84e2b-160">Добавление функции, которая подключается к текущий контекст и получает коллекции проектов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="84e2b-160">Add a function that connects to the current context and retrieves the projects collection, as follows.</span></span>
    
   ```js
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
   ```

   <span data-ttu-id="84e2b-161">Некоторые клиентские объекты, которые извлекают в контексте не содержат данных до инициализации; то есть значения свойств объекта недоступны до инициализации объекта.</span><span class="sxs-lookup"><span data-stu-id="84e2b-161">Some client objects that you retrieve through the context contain no data until they are initialized; that is, you cannot access the property values of the object until the object is initialized.</span></span> <span data-ttu-id="84e2b-162">Кроме того для свойства типа **ValueObject**необходимо явно запросить свойства для доступа к его значение.</span><span class="sxs-lookup"><span data-stu-id="84e2b-162">Moreover, for properties of type **ValueObject**, you must explicitly request the property before you can access its value.</span></span> <span data-ttu-id="84e2b-163">(При попытке доступа к свойству до его инициализации, вы получаете исключение **PropertyOrFieldNotInitializedException** .)</span><span class="sxs-lookup"><span data-stu-id="84e2b-163">(If you try to access a property before it is initialized, you receive a **PropertyOrFieldNotInitializedException** exception.)</span></span> 
    
   <span data-ttu-id="84e2b-164">Чтобы инициализировать объект, вызовите метод **load** (или метод **loadQuery** ) и затем метода **executeQueryAsync** .</span><span class="sxs-lookup"><span data-stu-id="84e2b-164">To initialize an object, you call the **load** method (or the **loadQuery** method) and then the **executeQueryAsync** method.</span></span> 
    
   - <span data-ttu-id="84e2b-165">Вызов функции **загрузки** или функция **loadQuery** регистрирует запрос, который требуется запустить на сервере.</span><span class="sxs-lookup"><span data-stu-id="84e2b-165">Calling the **load** function or the **loadQuery** function registers a request that you want to run on the server.</span></span> <span data-ttu-id="84e2b-166">Передайте параметр, представляющий объект, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="84e2b-166">You pass in a parameter that represents the object that you want to retrieve.</span></span> <span data-ttu-id="84e2b-167">При работе со свойством **ValueObject** можно также запрашивать свойства с помощью параметра.</span><span class="sxs-lookup"><span data-stu-id="84e2b-167">If you are working with a **ValueObject** property, then you also request the property in the parameter.</span></span> 
    
   - <span data-ttu-id="84e2b-168">Вызов функции **executeQueryAsync** асинхронно отправляет запрос запросов к серверу.</span><span class="sxs-lookup"><span data-stu-id="84e2b-168">Calling the **executeQueryAsync** function sends the query request to the server asynchronously.</span></span> <span data-ttu-id="84e2b-169">Передать функцию обратного вызова для успеха и функции обратного вызова сбоя для вызова при получении ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="84e2b-169">You pass in a success callback function and a failure callback function to invoke when the server response is received.</span></span> 
    
   <span data-ttu-id="84e2b-170">Чтобы уменьшить сетевой трафик, запросите только свойства, которые вы хотите работать с при вызове функции **загрузки** .</span><span class="sxs-lookup"><span data-stu-id="84e2b-170">To reduce network traffic, request only the properties that you want to work with when you call the **load** function.</span></span> <span data-ttu-id="84e2b-171">Кроме того при работе с несколькими объектами групповой несколько вызовов функции **нагрузки** перед вызовите функцию **executeQueryAsync** , если это возможно.</span><span class="sxs-lookup"><span data-stu-id="84e2b-171">In addition, if you are working with multiple objects, group multiple calls to the **load** function before you call the **executeQueryAsync** function when it is possible.</span></span> 
    
### <a name="iterating-through-the-projects-collection"></a><span data-ttu-id="84e2b-172">Итерации по коллекции проектов</span><span class="sxs-lookup"><span data-stu-id="84e2b-172">Iterating through the projects collection</span></span>
<span data-ttu-id="84e2b-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="84e2b-173"></span></span>

<span data-ttu-id="84e2b-174">Следующие шаги итерации по коллекции проектов (если вызов сервера выполнен успешно) или отображать сообщение об ошибке (если не удается выполнить звонок).</span><span class="sxs-lookup"><span data-stu-id="84e2b-174">The following steps iterate through the projects collection (if the server call is successful) or render an error message (if the call fails).</span></span>
  
1. <span data-ttu-id="84e2b-175">Добавление функции обратного вызова успех, который выполняет итерацию по коллекции проектов, следующим образом.</span><span class="sxs-lookup"><span data-stu-id="84e2b-175">Add a success callback function that iterates through the projects collection, as follows.</span></span>
    
   ```js
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
   ```

2. <span data-ttu-id="84e2b-176">Добавьте функцию обратного вызова ошибка, отображается сообщение об ошибке следующим образом.</span><span class="sxs-lookup"><span data-stu-id="84e2b-176">Add a failure callback function that renders an error message, as follows.</span></span>
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. <span data-ttu-id="84e2b-177">Тестирование страницы приложения в строке меню выберите **Отладка**, **Начать отладку**.</span><span class="sxs-lookup"><span data-stu-id="84e2b-177">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="84e2b-178">Если запрос на изменение файла web.config, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="84e2b-178">If you are prompted to modify the web.config file, choose **OK**.</span></span>

<span data-ttu-id="84e2b-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span><span class="sxs-lookup"><span data-stu-id="84e2b-179"></span></span>

## <a name="complete-code-example"></a><span data-ttu-id="84e2b-180">Полный пример кода</span><span class="sxs-lookup"><span data-stu-id="84e2b-180">Complete code example</span></span>

<span data-ttu-id="84e2b-181">Ниже приведен полный код из файла ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="84e2b-181">Following is the complete code from the ProjectsList.aspx file.</span></span>
  
```js
<%@ Assembly Name="$SharePoint.Project.AssemblyFullName$" %>
<%@ Import Namespace="Microsoft.SharePoint.ApplicationPages" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="asp" Namespace="System.Web.UI" Assembly="System.Web.Extensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" %>
<%@ Import Namespace="Microsoft.SharePoint" %>
<%@ Assembly Name="Microsoft.Web.CommandUI, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ProjectsList.aspx.cs" Inherits="GetProjectsJSOM.Layouts.GetProjectsJSOM.ProjectsList" DynamicMasterPageFile="~masterurl/default.master" %>
<asp:Content ID="PageHead" ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
</asp:Content>
<asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <table width="100%" id="tblProjects">
    <tr id="headerRow">
        <th width="25%" align="left">Project name</th>
        <th width="25%" align="left">Created date</th>
        <th width="50%" align="left">Project ID</th>
    </tr>
</table>
<div id="divMessage">
    <br/>
    <span id="spanMessage" style="color: #FF0000;"></span>
</div>
<SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
<script type="text/javascript">
    // Declare a variable to store the published projects that exist
    // in the current context.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
</script>
</asp:Content>
<asp:Content ID="PageTitle" ContentPlaceHolderID="PlaceHolderPageTitle" runat="server">
Application Page
</asp:Content>
<asp:Content ID="PageTitleInTitleArea" ContentPlaceHolderID="PlaceHolderPageTitleInTitleArea" runat="server" >
My Application Page
</asp:Content>

```

<span data-ttu-id="84e2b-182"><a name="pj15_GetStartedJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="84e2b-182"></span></span>

## <a name="see-also"></a><span data-ttu-id="84e2b-183">См. также</span><span class="sxs-lookup"><span data-stu-id="84e2b-183">See also</span></span>

- [<span data-ttu-id="84e2b-184">Создание, получение, обновление и удаление проектов с помощью объектной модели Project Server JavaScript</span><span class="sxs-lookup"><span data-stu-id="84e2b-184">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [<span data-ttu-id="84e2b-185">Клиентская объектная модель (CSOM) для Project 2013</span><span class="sxs-lookup"><span data-stu-id="84e2b-185">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="84e2b-186">Начало работы с Project Server CSOM и .NET</span><span class="sxs-lookup"><span data-stu-id="84e2b-186">Getting started with the Project Server CSOM and .NET</span></span>](getting-started-with-the-project-server-csom-and-net.md)
    

