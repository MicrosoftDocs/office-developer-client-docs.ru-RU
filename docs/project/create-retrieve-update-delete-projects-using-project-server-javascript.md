---
title: Создание, получение, обновление и удаление проектов с помощью Project Server JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Получение текущего экземпляра ProjectContext; извлечение и выполнять итерацию по коллекции опубликованных проектов на сервере; Создание, получение, извлечение и удаления проекта с помощью объектной модели Project Server JavaScript; и изменить свойства проекта.
ms.openlocfilehash: 966c1298d210cb608001e4ce2b390611a75bdb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812922"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a><span data-ttu-id="e0dbe-103">Создание, получение, обновление и удаление проектов с помощью Project Server JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0dbe-103">Create, retrieve, update, and delete projects using Project Server JavaScript</span></span>

<span data-ttu-id="e0dbe-104">Сценарии в этой статье показано, как для получения текущего экземпляра **ProjectContext** ; извлечение и выполнять итерацию по коллекции опубликованных проектов на сервере; Создание, получение, извлечение и удаления проекта с помощью объектной модели Project Server JavaScript; и изменить свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-104">The scenarios in this article show how to get the current **ProjectContext** instance; retrieve and iterate through the collection of published projects on the server; create, retrieve, check out, and delete a project by using the Project Server JavaScript object model; and change a project's properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e0dbe-105">Эти сценарии определение пользовательского кода в разметке страницы приложения SharePoint, но не используют файл фонового кода, который создает Visual Studio 2012 для страницы.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-105">These scenarios define custom code in the markup of a SharePoint application page but do not use the code-behind file that Visual Studio 2012 creates for the page.</span></span> 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a><span data-ttu-id="e0dbe-106">Необходимые условия для работы с Project Server 2013 проектов в объектной модели JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0dbe-106">Prerequisites for working with Project Server 2013 projects in the JavaScript object model</span></span>

<span data-ttu-id="e0dbe-107">Для выполнения сценариев, описанных в этой статье, необходимо установить и настроить следующих продуктов:</span><span class="sxs-lookup"><span data-stu-id="e0dbe-107">To perform the scenarios that are described in this article, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="e0dbe-108">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0dbe-108">SharePoint Server 2013</span></span>
- <span data-ttu-id="e0dbe-109">Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="e0dbe-109">Project Server 2013</span></span>
- <span data-ttu-id="e0dbe-110">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="e0dbe-110">Visual Studio 2012</span></span>
- <span data-ttu-id="e0dbe-111">Инструменты разработчика Office для Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="e0dbe-111">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="e0dbe-112">Кроме того, необходимо иметь разрешения для развертывания расширения для SharePoint Server 2013 и внесение данных в проектах.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-112">You must also have permissions to deploy the extension to SharePoint Server 2013 and to contribute to projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e0dbe-113">Эти инструкции предполагают, что вы работаете на компьютере, на котором работает Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-113">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
## <a name="create-the-visual-studio-solution"></a><span data-ttu-id="e0dbe-114">Создание решения Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0dbe-114">Create the Visual Studio solution</span></span>
<span data-ttu-id="e0dbe-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="e0dbe-115"></span></span>

<span data-ttu-id="e0dbe-116">Следующие шаги создания решения Visual Studio 2012, содержащий проекта SharePoint и страницу приложения.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-116">The following steps create a Visual Studio 2012 solution that contains a SharePoint project and an application page.</span></span> <span data-ttu-id="e0dbe-117">Страница содержит логику для работы с проектами.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-117">The page contains the logic for working with projects.</span></span>
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a><span data-ttu-id="e0dbe-118">Создание проекта SharePoint в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0dbe-118">To create the SharePoint project in Visual Studio</span></span>

1. <span data-ttu-id="e0dbe-119">На компьютере, на котором работает Project Server 2013 запустите Visual Studio 2012 с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-119">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="e0dbe-120">В строке меню выберите пункты **Файл**, **Создать** и **Проект**.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-120">On the menu bar, choose **File**, **New**, **Project**.</span></span>
    
3. <span data-ttu-id="e0dbe-121">В верхней части диалогового окна **Новый проект** выберите **.NET Framework 4.5** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-121">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
4. <span data-ttu-id="e0dbe-122">В категории шаблонов **Office/SharePoint** щелкните **Решения SharePoint**и затем выберите шаблон **Проекта SharePoint 2013** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-122">In the **Office/SharePoint** template category, choose **SharePoint Solutions**, and then choose the **SharePoint 2013 Project** template.</span></span> 
    
5. <span data-ttu-id="e0dbe-123">Назовите проект ProjectsJSOM и затем нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-123">Name the project ProjectsJSOM, and then choose the **OK** button.</span></span> 
    
6. <span data-ttu-id="e0dbe-124">В диалоговом окне **Мастер настройки SharePoint** выберите **Развернуть как решение фермы** и затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-124">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="e0dbe-125">Изменить значение свойства **URL-адрес сайта** проекта **ProjectsJSOM** в соответствии с URL-адрес экземпляра Project Web App (например, `http://ServerName/PWA`).</span><span class="sxs-lookup"><span data-stu-id="e0dbe-125">Edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `http://ServerName/PWA`).</span></span>
    
### <a name="to-create-the-application-page-in-visual-studio"></a><span data-ttu-id="e0dbe-126">Создание страницы приложения в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e0dbe-126">To create the application page in Visual Studio</span></span>

1. <span data-ttu-id="e0dbe-127">В **Обозревателе решений**откройте контекстное меню для проекта **ProjectsJSOM** и добавьте SharePoint «Макеты» сопоставленная папка.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-127">In **Solution Explorer**, open the shortcut menu for the **ProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
2. <span data-ttu-id="e0dbe-128">В папке **Layouts** откройте контекстное меню для папки **ProjectsJSOM** и добавьте новую страницу приложения SharePoint с именем ProjectsList.aspx.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-128">In the **Layouts** folder, open the shortcut menu for the **ProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
3. <span data-ttu-id="e0dbe-129">Откройте контекстное меню для страницы **ProjectsList.aspx** и выберите команду **назначить элемент**.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-129">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
4. <span data-ttu-id="e0dbe-130">В разметке страницы **ProjectsList.aspx** определите элементы управления пользовательского интерфейса внутри тегов **asp: Content** «Главная», следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-130">In the markup for the **ProjectsList.aspx** page, define user interface controls inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
   ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Name</th>
            <th width="25%" align="left">Description</th>
            <th width="25%" align="left">Start Date</th>
            <th width="25%" align="left">ID</th>
        </tr>
    </table>
    <textarea id="txtGuid" rows="1" cols="35">Paste the project GUID here.</textarea>
    <button id="btnSend" type="button"></button><br />
    <span id="spanMessage" style="color: #FF0000;"></span>
   ```

   > [!NOTE]
   > <span data-ttu-id="e0dbe-131">Эти элементы управления не могут быть использованы в каждом сценарии.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-131">These controls may not be used in every scenario.</span></span> <span data-ttu-id="e0dbe-132">Например сценарий «Создание проектов» не использует элементы управления **textarea** и **кнопка** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-132">For example, the "Create projects" scenario does not use the **textarea** and **button** controls.</span></span> 
  
5. <span data-ttu-id="e0dbe-133">После закрывающего тега, **охватывающих** , добавьте тег **SharePoint:ScriptLink** , тег **SharePoint:FormDigest** и **теги,** как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-133">After the closing **span** tag, add a **SharePoint:ScriptLink** tag, a **SharePoint:FormDigest** tag, and **script** tags, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   <span data-ttu-id="e0dbe-134">Тег **SharePoint:ScriptLink** ссылается на файл PS.js, который определяет объектной модели JavaScript для Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-134">The **SharePoint:ScriptLink** tag references the PS.js file, which defines the JavaScript object model for Project Server 2013.</span></span> <span data-ttu-id="e0dbe-135">Тег **SharePoint:FormDigest** создает сообщение дайджеста для проверки подлинности при необходимости в операции, обновлять содержимое сервера.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-135">The **SharePoint:FormDigest** tag generates a message digest for security validation when required by operations that update server content.</span></span> 
    
6. <span data-ttu-id="e0dbe-136">Замените комментарий заполнитель на код из одного из следующих процедур:</span><span class="sxs-lookup"><span data-stu-id="e0dbe-136">Replace the placeholder comment with the code from one of the following procedures:</span></span>
    
   - [<span data-ttu-id="e0dbe-137">Создание проектов Project Server 2013 с помощью объектной модели JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0dbe-137">Create Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [<span data-ttu-id="e0dbe-138">Обновление проектов Project Server 2013 с помощью объектной модели JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0dbe-138">Update Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [<span data-ttu-id="e0dbe-139">Удаление проектов Project Server 2013 с помощью объектной модели JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0dbe-139">Delete Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. <span data-ttu-id="e0dbe-140">Тестирование страницы приложения в строке меню выберите **Отладка**, **Начать отладку**.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-140">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="e0dbe-141">Если запрос на изменение файла web.config, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-141">If you are prompted to modify the web.config file, choose **OK**.</span></span>
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="e0dbe-142">Создание проектов Project Server 2013 с помощью объектной модели JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0dbe-142">Create Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="e0dbe-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="e0dbe-143"></span></span>

<span data-ttu-id="e0dbe-144">Процедуры этого раздела создаются проекты с помощью объектной модели JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-144">The procedure in this section creates projects by using the JavaScript object model.</span></span> <span data-ttu-id="e0dbe-145">Процедура включает в себя следующие общие действия:</span><span class="sxs-lookup"><span data-stu-id="e0dbe-145">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="e0dbe-146">Получение текущего экземпляра **ProjectContext** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-146">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="e0dbe-147">Создайте объект **ProjectCreationInformation** для указания начальной свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-147">Create a **ProjectCreationInformation** object to specify initial properties for your project.</span></span> <span data-ttu-id="e0dbe-148">Укажите требуемые **имя** свойства с помощью функции **ProjectCreationInformation.set_name** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-148">Specify the required **name** property by using the **ProjectCreationInformation.set_name** function.</span></span> 
    
3. <span data-ttu-id="e0dbe-149">Получение опубликованных проектов с сервера с помощью функции **ProjectContext.get_projects** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-149">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="e0dbe-150">Функция **get_projects** возвращает объект **ProjectCollection** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-150">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
4. <span data-ttu-id="e0dbe-151">Добавьте новый проект в коллекцию с помощью функции **ProjectCollection.add** , передав объект **ProjectCreationInformation** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-151">Add the new project to the collection by using the **ProjectCollection.add** function and passing in the **ProjectCreationInformation** object.</span></span> 
    
5. <span data-ttu-id="e0dbe-152">Обновление семейства сайтов с помощью функции **ProjectCollection.update** и **ProjectContext.waitForQueueAsync** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-152">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="e0dbe-153">Функция **обновления** возвращает объект **QueueJob** , передаваемых в **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-153">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span> <span data-ttu-id="e0dbe-154">Этот вызов также публикует проект.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-154">This call also publishes the project.</span></span>
    
<span data-ttu-id="e0dbe-155">Вставьте следующий код в тегах **сценария** , которые добавлены в процедуре, **Чтобы создать страницу приложения в Visual Studio** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-155">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare a global variable to store the project collection.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(CreateProject, "PS.js");
    // Add a project the projects collection.
    function CreateProject() {
        
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Initialize a ProjectCreationInformation object and specify properties
        // for the new project.
        // The Name property is required and must be unique.
        var creationInfo = new PS.ProjectCreationInformation();
        creationInfo.set_name("Test Project 1");
        // Specify optional properties for the new project.
        // If not specified, the Start property uses the current date and the
        // EnterpriseProjectTypeId property uses the default EPT.
        creationInfo.set_description("Created through the JSOM.");
        creationInfo.set_start("2013-10-01 09:00:00.000");
        // Get the projects collection.
        projects = projContext.get_projects();
        // Add the new project to the projects collection.
        projects.add(creationInfo);
        // Add a second project to use in the deleting projects procedure.
        creationInfo.set_name("Test Project 2");
        projects.add(creationInfo);
        // Submit the request to update the collection on the server
        var updateJob = projects.update();
        projContext.waitForQueueAsync(updateJob, 10, GetProjects);
    }
    // Get the projects collection.
    function GetProjects(response) {
        // This call demonstrates that you can get the context from the 
        // ProjectCollection object.
        var projContext = projects.get_context();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // This scenario does not use the textarea or button controls.
        $get("txtGuid").disabled = true;
        $get("btnSend").disabled = true;
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="e0dbe-156">Обновление проектов Project Server 2013 с помощью объектной модели JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0dbe-156">Update Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="e0dbe-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="e0dbe-157"></span></span>

<span data-ttu-id="e0dbe-158">Процедуры в данном разделе обновляет свойства **startDate** проекта с помощью объектной модели JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-158">The procedure in this section updates the **startDate** property of a project by using the JavaScript object model.</span></span> <span data-ttu-id="e0dbe-159">Процедура включает в себя следующие общие действия:</span><span class="sxs-lookup"><span data-stu-id="e0dbe-159">The procedure includes the following high-level steps:</span></span> 
  
1. <span data-ttu-id="e0dbe-160">Получение текущего экземпляра **ProjectContext** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-160">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="e0dbe-161">Получение опубликованных проектов с сервера с помощью функции **ProjectContext.get_projects** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-161">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="e0dbe-162">Функция **get_projects** возвращает объект **ProjectCollection** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-162">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="e0dbe-163">Запуск запроса на сервере с помощью функции **ProjectContext.load** и **ProjectContext.executeQueryAsync** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-163">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="e0dbe-164">Извлеките объект **PublishedProject** с помощью функции **ProjectContext.getById** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-164">Retrieve a **PublishedProject** object by using the **ProjectContext.getById** function.</span></span> 
    
5. <span data-ttu-id="e0dbe-165">Извлечение целевого проекта с помощью функции **Project.checkOut** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-165">Check out the target project by using the **Project.checkOut** function.</span></span> <span data-ttu-id="e0dbe-166">Функция **извлечения** Возвращает черновик опубликованного проекта.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-166">The **checkOut** function returns the draft version of the published project.</span></span> 
    
6. <span data-ttu-id="e0dbe-167">Измените дату начала проекта с помощью функции **DraftProject.set_startDate** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-167">Change the project's start date by using the **DraftProject.set_startDate** function.</span></span> 
    
7. <span data-ttu-id="e0dbe-168">Публикация проекта с помощью функции **DraftProject.publish** и **ProjectContext.waitForQueueAsync** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-168">Publish the project by using the **DraftProject.publish** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="e0dbe-169">Функция **публикации** возвращает объект **QueueJob** , передаваемых в **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-169">The **publish** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="e0dbe-170">Вставьте следующий код в тегах **сценария** , которые добавлены в процедуре, **Чтобы создать страницу приложения в Visual Studio** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-170">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { ChangeProject(); };
        $get("btnSend").innerText = "Update";
    }
    // Change the project's start date.
    function ChangeProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then check it out. The checkOut function
        // returns the draft version of the project.
        var project = projects.getById(targetGuid);
        var draftProject = project.checkOut();
        // Set the new property value and then publish the project.
        // Specify "true" to also check the project in.
        draftProject.set_startDate("2013-12-31 09:00:00.000");
        var publishJob = draftProject.publish(true);
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(publishJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="e0dbe-171">Удаление проектов Project Server 2013 с помощью объектной модели JavaScript</span><span class="sxs-lookup"><span data-stu-id="e0dbe-171">Delete Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="e0dbe-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="e0dbe-172"></span></span>

<span data-ttu-id="e0dbe-173">Процедуры этого раздела удаляет проекта с помощью объектной модели JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-173">The procedure in this section deletes a project by using the JavaScript object model.</span></span> <span data-ttu-id="e0dbe-174">Процедура включает в себя следующие общие действия:</span><span class="sxs-lookup"><span data-stu-id="e0dbe-174">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="e0dbe-175">Получение текущего экземпляра **ProjectContext** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-175">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="e0dbe-176">Получение опубликованных проектов с сервера с помощью функции **ProjectContext.get_projects** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-176">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="e0dbe-177">Функция **get_projects** возвращает объект **ProjectCollection** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-177">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="e0dbe-178">Запуск запроса на сервере с помощью функции **ProjectContext.load** и **ProjectContext.executeQueryAsync** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-178">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="e0dbe-179">Извлеките объект **PublishedProject** с помощью функции **ProjectCollection.getById** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-179">Retrieve a **PublishedProject** object by using the **ProjectCollection.getById** function.</span></span> 
    
5. <span data-ttu-id="e0dbe-180">Удаление проекта с передачей их в функцию **ProjectCollection.remove** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-180">Delete the project by passing it to the **ProjectCollection.remove** function.</span></span> 
    
6. <span data-ttu-id="e0dbe-181">Обновление семейства сайтов с помощью функции **ProjectCollection.update** и **ProjectContext.waitForQueueAsync** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-181">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="e0dbe-182">Функция **обновления** возвращает объект **QueueJob** , передаваемых в **waitForQueueAsync**.</span><span class="sxs-lookup"><span data-stu-id="e0dbe-182">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="e0dbe-183">Вставьте следующий код в тегах **сценария** , которые добавлены в процедуре, **Чтобы создать страницу приложения в Visual Studio** .</span><span class="sxs-lookup"><span data-stu-id="e0dbe-183">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { DeleteProject(); };
        $get("btnSend").innerText = "Delete";
    }
    // Delete the project.
    function DeleteProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then remove it from the collection.
        var project = projects.getById(targetGuid);
        projects.remove(project);
        var removeJob = projects.update();
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(removeJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

<span data-ttu-id="e0dbe-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="e0dbe-184"></span></span>

## <a name="see-also"></a><span data-ttu-id="e0dbe-185">См. также</span><span class="sxs-lookup"><span data-stu-id="e0dbe-185">See also</span></span>

- [<span data-ttu-id="e0dbe-186">Задачи программирования Project</span><span class="sxs-lookup"><span data-stu-id="e0dbe-186">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="e0dbe-187">Клиентская объектная модель (CSOM) для Project 2013</span><span class="sxs-lookup"><span data-stu-id="e0dbe-187">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

