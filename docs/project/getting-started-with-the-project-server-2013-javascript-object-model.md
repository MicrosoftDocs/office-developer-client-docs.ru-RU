---
title: Начало работы с объектной моделью JavaScript для Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: В Project Server 2013 объектную модель JavaScript можно использовать в Project Online, мобильной и локальной разработке. В этом разделе представлен краткий обзор объектной модели JavaScript, а затем описано, как создать страницу приложения, которая извлекает и итерирует проекты с помощью объектной модели JavaScript.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360475"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a><span data-ttu-id="da66a-104">Начало работы с объектной моделью JavaScript для Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="da66a-104">Getting started with the Project Server 2013 JavaScript object model</span></span>

<span data-ttu-id="da66a-105">В Project Server 2013 объектную модель JavaScript можно использовать в Project Online, мобильных устройствах и локальной разработке.</span><span class="sxs-lookup"><span data-stu-id="da66a-105">In Project Server 2013, the JavaScript object model can be used in Project Online, mobile, and on-premise development.</span></span> <span data-ttu-id="da66a-106">В этом разделе представлен краткий обзор объектной модели JavaScript, а затем описано, как создать страницу приложения, которая извлекает и итерирует проекты с помощью объектной модели JavaScript.</span><span class="sxs-lookup"><span data-stu-id="da66a-106">This topic provides a brief overview of the JavaScript object model and then describes how to create an application page that retrieves and iterates through projects by using the JavaScript object model.</span></span>
  
## <a name="using-the-project-server-javascript-object-model"></a><span data-ttu-id="da66a-107">Использование объектной модели JavaScript для Project Server</span><span class="sxs-lookup"><span data-stu-id="da66a-107">Using the Project Server JavaScript object model</span></span>
<span data-ttu-id="da66a-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="da66a-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span></span>

<span data-ttu-id="da66a-109">Использование объектной модели JavaScript — отличный способ создать приложение, которое работает на стороне клиента (в отличие от управляемого клиентского кода, который должен работать удаленно).</span><span class="sxs-lookup"><span data-stu-id="da66a-109">Using the JavaScript object model is a great way to create an app that runs client-side (as opposed to managed client code which needs to run remotely).</span></span> <span data-ttu-id="da66a-110">Приложения могут использовать объектную модель JavaScript для извлечения или изменения объектов, отправляя асинхронные вызовы на сервер.</span><span class="sxs-lookup"><span data-stu-id="da66a-110">Apps can use the JavaScript object model to retrieve or change objects by sending asynchronous calls to the server.</span></span> <span data-ttu-id="da66a-111">Приложения, которые используют объектную модель JavaScript, обычно развертываются как пользовательские надстройки SharePoint, страницы приложений и веб-части.</span><span class="sxs-lookup"><span data-stu-id="da66a-111">Apps that use the JavaScript object model are typically deployed as custom SharePoint Add-ins, application pages, and Web Parts.</span></span> <span data-ttu-id="da66a-112">Дополнительные сведения см. в подстройки "Типы компонентов SharePoint, которые могут быть в приложении для SharePoint" на хост-сайтах, сайтах надстройки и компонентах SharePoint в [SharePoint 2013.](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da66a-112">For more information, see "Types of SharePoint components that can be in an app for SharePoint" in [Host webs, add-in webs, and SharePoint components in SharePoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="da66a-113">Объектная модель JavaScript реализует основные функции Project Server 2013, но объектная модель JavaScript и серверная объектная модель не имеют четности "один к одному".</span><span class="sxs-lookup"><span data-stu-id="da66a-113">The JavaScript object model implements the main functionality of Project Server 2013, but the JavaScript object model and the server object model do not have one-to-one parity.</span></span> <span data-ttu-id="da66a-114">Точка входа в объектную модель JavaScript — это объект **ProjectContext,** который представляет контекст клиента для Project Server 2013 и предоставляет доступ к контенту и функциям сервера.</span><span class="sxs-lookup"><span data-stu-id="da66a-114">The entry point to the JavaScript object model is the **ProjectContext** object, which represents the client context for Project Server 2013 and provides access to server content and functionality.</span></span> <span data-ttu-id="da66a-115">Объектная модель JavaScript для Project Server 2013 определена в файле PS.js, который расположен в пути по умолчанию на  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` сервере приложений.</span><span class="sxs-lookup"><span data-stu-id="da66a-115">The JavaScript object model for Project Server 2013 is defined in the PS.js file, which is located in the default path  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` on the application server.</span></span> <span data-ttu-id="da66a-116">Project Server 2013 также устанавливает PS.Debug.js в том же расположении.</span><span class="sxs-lookup"><span data-stu-id="da66a-116">Project Server 2013 also installs the PS.Debug.js file in the same location.</span></span> <span data-ttu-id="da66a-117">PS.Debug.js является неустановленной версией PS.js, которая предоставляет IntelliSense сведения.</span><span class="sxs-lookup"><span data-stu-id="da66a-117">PS.Debug.js is an unminified version of PS.js that provides IntelliSense information.</span></span> 
  
<span data-ttu-id="da66a-118">Объектная модель JavaScript разрешает проверку подлинности на форме, а все запросы аутентификация как текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="da66a-118">The JavaScript object model allows Forms authentication, and all requests are authenticated as the current user.</span></span> <span data-ttu-id="da66a-119">Дополнительные сведения о безопасности и другие аспекты разработки пользовательских приложений и решений см. в документах "Проверка подлинности,авторизация и безопасность" в [SharePoint 2013,](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx)"Важные аспекты архитектуры и разработки надстройки [SharePoint"](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)и "Сравнение надстройки SharePoint с решениями [SharePoint".](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da66a-119">For more information about security and other considerations for designing custom apps and solutions, see [Authentication, authorization, and security in SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Important aspects of the SharePoint Add-in architecture and development landscape](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and [SharePoint Add-ins compared with SharePoint solutions](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="da66a-120">Для удаленного доступа к данным с сайта SharePoint SharePoint 2013 предоставляет меж доменную библиотеку, которая позволяет делать меж доменные вызовы на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="da66a-120">To access data from a SharePoint site remotely, SharePoint 2013 provides a cross-domain library that enables you to make client-side cross-domain calls.</span></span> <span data-ttu-id="da66a-121">Дополнительные сведения см. в данных [Access SharePoint 2013](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx)из надстройки, использующих меж доменную библиотеку.</span><span class="sxs-lookup"><span data-stu-id="da66a-121">For more information, see [Access SharePoint 2013 data from add-ins using the cross-domain library](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="da66a-122">Многие концепции и процессы использования объектной модели JavaScript для Project Server 2013 похожи на концепции в связанных клиентских объектных моделях.</span><span class="sxs-lookup"><span data-stu-id="da66a-122">Many concepts and processes for using the JavaScript object model for Project Server 2013 resemble those in related client object models.</span></span> <span data-ttu-id="da66a-123">Дополнительные сведения об управляемой клиентской объектной модели Project Server 2013 см. в примере **Microsoft.ProjectServer.Client.**</span><span class="sxs-lookup"><span data-stu-id="da66a-123">For more information about the Project Server 2013 managed client object model, see **Microsoft.ProjectServer.Client**.</span></span> <span data-ttu-id="da66a-124">Дополнительные сведения об объектной модели SharePoint 2013JavaScript и управляемой клиентской объектной модели см. в подразделе "Основные операции с использованием кода библиотеки JavaScript в [SharePoint 2013"](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) и "Завершение базовых операций с использованием кода клиентской библиотеки [SharePoint 2013".](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da66a-124">For more information about the SharePoint 2013JavaScript object model and managed client object model, see [Complete basic operations using JavaScript library code in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) and [Complete basic operations using SharePoint 2013 client library code](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span></span>
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="da66a-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span><span class="sxs-lookup"><span data-stu-id="da66a-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="da66a-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="da66a-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span></span>

<span data-ttu-id="da66a-127">Узнайте, как создать страницу приложения, которая отображает ИД, имя и дату создания каждого опубликованного проекта на сайте.</span><span class="sxs-lookup"><span data-stu-id="da66a-127">Learn how to create an application page that displays the ID, name, and created date of each published project in a site.</span></span>
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="da66a-128">Необходимые условия для создания страницы приложения, которая извлекает и итерирует проекты</span><span class="sxs-lookup"><span data-stu-id="da66a-128">Prerequisites for creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="da66a-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="da66a-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span></span>

<span data-ttu-id="da66a-130">Для разработки страницы приложения, описанной в этом разделе, необходимо установить и настроить следующие продукты:</span><span class="sxs-lookup"><span data-stu-id="da66a-130">To develop the application page that is described in this topic, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="da66a-131">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="da66a-131">SharePoint Server 2013</span></span>
- <span data-ttu-id="da66a-132">Project Server 2013 с хотя бы одним опубликованным проектом</span><span class="sxs-lookup"><span data-stu-id="da66a-132">Project Server 2013 with at least one published project</span></span>
- <span data-ttu-id="da66a-133">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="da66a-133">Visual Studio 2012</span></span>
- <span data-ttu-id="da66a-134">Инструменты разработчика Office для Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="da66a-134">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="da66a-135">Кроме того, необходимо иметь разрешения на развертывание расширения в SharePoint Server 2013 и извлечение проектов.</span><span class="sxs-lookup"><span data-stu-id="da66a-135">You must also have permissions to deploy the extension to SharePoint Server 2013 and to retrieve projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="da66a-136">В этих инструкциях предполагается, что разработка происходит на компьютере с Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="da66a-136">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a><span data-ttu-id="da66a-137">Создание страницы приложения в Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="da66a-137">Creating the application page in Visual Studio 2012</span></span>
<span data-ttu-id="da66a-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span><span class="sxs-lookup"><span data-stu-id="da66a-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span></span>

<span data-ttu-id="da66a-139">Следующие действия создают проект SharePoint и страницу приложения, которая содержит таблицу и метку.</span><span class="sxs-lookup"><span data-stu-id="da66a-139">The following steps create a SharePoint project and an application page that contains a table and label.</span></span> <span data-ttu-id="da66a-140">В таблице отображаются сведения о проектах, а метка отображает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="da66a-140">The table displays information about the projects and the label displays error messages.</span></span>
  
1. <span data-ttu-id="da66a-141">На компьютере с Project Server 2013 запустите Visual Studio 2012 от учетной записи администратора.</span><span class="sxs-lookup"><span data-stu-id="da66a-141">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="da66a-142">Создайте пустой проект SharePoint 2013 следующим образом:</span><span class="sxs-lookup"><span data-stu-id="da66a-142">Create an empty SharePoint 2013 project, as follows:</span></span>
    
    1. <span data-ttu-id="da66a-143">В раскрывающемся списке в верхней части диалогового окна **Новый проект** выберите пункт **.NET Framework 4.5**.</span><span class="sxs-lookup"><span data-stu-id="da66a-143">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
        
    2. <span data-ttu-id="da66a-144">В списке категорий шаблонов выберите категорию **Office SharePoint,** а затем выберите шаблон **Проекта SharePoint 2013.**</span><span class="sxs-lookup"><span data-stu-id="da66a-144">In the list of template categories, choose the **Office SharePoint** category, and then choose the **SharePoint 2013 Project** template.</span></span> 
        
    3. <span data-ttu-id="da66a-145">Назовем проект GetProjectsJSOM и  затем нажимаем кнопку "ОК".</span><span class="sxs-lookup"><span data-stu-id="da66a-145">Name the project GetProjectsJSOM, and then choose the **OK** button.</span></span> 
        
    4. <span data-ttu-id="da66a-146">В **диалоговом окне** мастера настройки SharePoint выберите "Развернуть как решение фермы" **и** затем кнопку "ОК". </span><span class="sxs-lookup"><span data-stu-id="da66a-146">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="da66a-147">В обозревателе решений отредактируем значение свойства **URL-адреса** сайта для проекта **ProjectsJSOM** в соответствие с URL-адресом экземпляра Project Web App (например). `https://ServerName/PWA`</span><span class="sxs-lookup"><span data-stu-id="da66a-147">In Solution Explorer, edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
4. <span data-ttu-id="da66a-148">Откройте меню ярлыка для проекта **GetProjectsJSOM,** а затем добавьте папку SharePoint "Layouts".</span><span class="sxs-lookup"><span data-stu-id="da66a-148">Open the shortcut menu for the **GetProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
5. <span data-ttu-id="da66a-149">В **папке Layouts** откройте меню ярлыка для папки **GetProjectsJSOM** и добавьте новую страницу приложения SharePoint с именем ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="da66a-149">In the **Layouts** folder, open the shortcut menu for the **GetProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="da66a-150">В этом примере не используется файл кода,который Visual Studio 2012 для страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="da66a-150">This example does not use the code-behind file that Visual Studio 2012 creates for the application page.</span></span> 
  
6. <span data-ttu-id="da66a-151">Откройте меню ярлыка для страницы **ProjectsList.aspx** и выберите **"Установить как элемент запуска".**</span><span class="sxs-lookup"><span data-stu-id="da66a-151">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
7. <span data-ttu-id="da66a-152">В разметке для страницы **ProjectsList.aspx** определите таблицу и замещение сообщений в тегах **Asp:Content,** как поется ниже.</span><span class="sxs-lookup"><span data-stu-id="da66a-152">In the markup for the **ProjectsList.aspx** page, define a table and a message placeholder inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
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

### <a name="retrieving-the-projects-collection"></a><span data-ttu-id="da66a-153">Ирисовка коллекции проектов</span><span class="sxs-lookup"><span data-stu-id="da66a-153">Retrieving the projects collection</span></span>
<span data-ttu-id="da66a-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="da66a-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span></span>

<span data-ttu-id="da66a-155">Следующие действия по извлечению и инициализации коллекции проектов.</span><span class="sxs-lookup"><span data-stu-id="da66a-155">The following steps retrieve and initialize the projects collection.</span></span>
  
1. <span data-ttu-id="da66a-156">После закрытия **тега div** добавьте тег **SharePoint:ScriptLink,** который ссылается на PS.js файла, как пошагово.</span><span class="sxs-lookup"><span data-stu-id="da66a-156">After the closing **div** tag, add a **SharePoint:ScriptLink** tag that references the PS.js file, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. <span data-ttu-id="da66a-157">Под **тегом SharePoint:ScriptLink** добавьте **теги** скрипта следующим образом.</span><span class="sxs-lookup"><span data-stu-id="da66a-157">Below the **SharePoint:ScriptLink** tag, add **script** tags, as follows.</span></span> 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. <span data-ttu-id="da66a-158">Объявите глобальную переменную для хранения коллекции проектов следующим образом.</span><span class="sxs-lookup"><span data-stu-id="da66a-158">Declare a global variable to store the projects collection, as follows.</span></span>
    
   ```js
   var projects;
   ```

4. <span data-ttu-id="da66a-159">Вызовите **методSP.SOD.exeOrDelayUntilScriptLoaded,** чтобы убедиться, что PS.js загружается перед запуском пользовательского кода.</span><span class="sxs-lookup"><span data-stu-id="da66a-159">Call the **SP.SOD.executeOrDelayUntilScriptLoaded** method to ensure that the PS.js file is loaded before your custom code runs.</span></span> 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. <span data-ttu-id="da66a-160">Добавьте функцию, которая подключается к текущему контексту и извлекает коллекцию проектов следующим образом.</span><span class="sxs-lookup"><span data-stu-id="da66a-160">Add a function that connects to the current context and retrieves the projects collection, as follows.</span></span>
    
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

   <span data-ttu-id="da66a-161">Некоторые клиентские объекты, которые вы извлекаете через контекст, не содержат данных до их инициализации; то есть вы не сможете получить доступ к значениям свойств объекта, пока объект не будет инициализирован.</span><span class="sxs-lookup"><span data-stu-id="da66a-161">Some client objects that you retrieve through the context contain no data until they are initialized; that is, you cannot access the property values of the object until the object is initialized.</span></span> <span data-ttu-id="da66a-162">Кроме того, для свойств типа **ValueObject** необходимо явно запросить свойство, прежде чем получить доступ к его значению.</span><span class="sxs-lookup"><span data-stu-id="da66a-162">Moreover, for properties of type **ValueObject**, you must explicitly request the property before you can access its value.</span></span> <span data-ttu-id="da66a-163">(При попытке получить доступ к свойству до его инициализации вы получите исключение **PropertyOrFieldNotInitializedException.)**</span><span class="sxs-lookup"><span data-stu-id="da66a-163">(If you try to access a property before it is initialized, you receive a **PropertyOrFieldNotInitializedException** exception.)</span></span> 
    
   <span data-ttu-id="da66a-164">Чтобы инициализировать объект, вызовите метод **load** (или **метод loadQuery),** а затем **метод executeQueryAsync.**</span><span class="sxs-lookup"><span data-stu-id="da66a-164">To initialize an object, you call the **load** method (or the **loadQuery** method) and then the **executeQueryAsync** method.</span></span> 
    
   - <span data-ttu-id="da66a-165">Вызов **функции загрузки** или **loadQuery** регистрирует запрос, который необходимо выполнить на сервере.</span><span class="sxs-lookup"><span data-stu-id="da66a-165">Calling the **load** function or the **loadQuery** function registers a request that you want to run on the server.</span></span> <span data-ttu-id="da66a-166">Передав параметр, который представляет объект, который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="da66a-166">You pass in a parameter that represents the object that you want to retrieve.</span></span> <span data-ttu-id="da66a-167">Если вы работаете со **свойством ValueObject,** вы также запрашиваете свойство в параметре.</span><span class="sxs-lookup"><span data-stu-id="da66a-167">If you are working with a **ValueObject** property, then you also request the property in the parameter.</span></span> 
    
   - <span data-ttu-id="da66a-168">Вызов **функции executeQueryAsync** асинхронно отправляет запрос на сервер.</span><span class="sxs-lookup"><span data-stu-id="da66a-168">Calling the **executeQueryAsync** function sends the query request to the server asynchronously.</span></span> <span data-ttu-id="da66a-169">Вы передаете функцию успешного вызова и функцию ответного вызова сбоя для вызова при получении ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="da66a-169">You pass in a success callback function and a failure callback function to invoke when the server response is received.</span></span> 
    
   <span data-ttu-id="da66a-170">Чтобы уменьшить сетевой трафик, запрашивать только свойства, с которые необходимо работать при вызове **функции загрузки.**</span><span class="sxs-lookup"><span data-stu-id="da66a-170">To reduce network traffic, request only the properties that you want to work with when you call the **load** function.</span></span> <span data-ttu-id="da66a-171">Кроме того, если вы работаете с несколькими  объектами, группу нескольких вызовов функции загрузки, прежде чем вызывать **функцию executeQueryAsync,** когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="da66a-171">In addition, if you are working with multiple objects, group multiple calls to the **load** function before you call the **executeQueryAsync** function when it is possible.</span></span> 
    
### <a name="iterating-through-the-projects-collection"></a><span data-ttu-id="da66a-172">Итерации по коллекции проектов</span><span class="sxs-lookup"><span data-stu-id="da66a-172">Iterating through the projects collection</span></span>
<span data-ttu-id="da66a-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="da66a-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span></span>

<span data-ttu-id="da66a-174">Следующие действия проходят по коллекции проектов (при успешном вызове сервера) или отрисовке сообщения об ошибке (если вызов не удается).</span><span class="sxs-lookup"><span data-stu-id="da66a-174">The following steps iterate through the projects collection (if the server call is successful) or render an error message (if the call fails).</span></span>
  
1. <span data-ttu-id="da66a-175">Добавьте функцию успешного вызова, которая проходит по коллекции проектов следующим образом.</span><span class="sxs-lookup"><span data-stu-id="da66a-175">Add a success callback function that iterates through the projects collection, as follows.</span></span>
    
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

2. <span data-ttu-id="da66a-176">Добавьте функцию вызова сбоя, которая отрисовка сообщения об ошибке следующим образом.</span><span class="sxs-lookup"><span data-stu-id="da66a-176">Add a failure callback function that renders an error message, as follows.</span></span>
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. <span data-ttu-id="da66a-177">Чтобы протестировать страницу приложения, в панели меню выберите команды **Отладка**, **Начать отладку**.</span><span class="sxs-lookup"><span data-stu-id="da66a-177">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="da66a-178">Если вам будет предложено изменить файл web.config, выберите **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="da66a-178">If you are prompted to modify the web.config file, choose **OK**.</span></span>

<span data-ttu-id="da66a-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span><span class="sxs-lookup"><span data-stu-id="da66a-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span></span>

## <a name="complete-code-example"></a><span data-ttu-id="da66a-180">Полный пример кода</span><span class="sxs-lookup"><span data-stu-id="da66a-180">Complete code example</span></span>

<span data-ttu-id="da66a-181">Ниже приводится полный код из файла ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="da66a-181">Following is the complete code from the ProjectsList.aspx file.</span></span>
  
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

<span data-ttu-id="da66a-182"><a name="pj15_GetStartedJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="da66a-182"><a name="pj15_GetStartedJSOM_AR"> </a></span></span>

## <a name="see-also"></a><span data-ttu-id="da66a-183">См. также</span><span class="sxs-lookup"><span data-stu-id="da66a-183">See also</span></span>

- [<span data-ttu-id="da66a-184">Создание, извлечение, обновление и удаление проектов с помощью объектной модели JavaScript для Project Server</span><span class="sxs-lookup"><span data-stu-id="da66a-184">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [<span data-ttu-id="da66a-185">Клиентская объектная модель (CSOM) для Project 2013</span><span class="sxs-lookup"><span data-stu-id="da66a-185">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="da66a-186">Начало работы с Project Server CSOM и .NET</span><span class="sxs-lookup"><span data-stu-id="da66a-186">Getting started with the Project Server CSOM and .NET</span></span>](getting-started-with-the-project-server-csom-and-net.md)
    

