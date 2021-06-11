---
title: Создание, извлечение, обновление и удаление проектов с Project JavaScript сервера
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: Получите текущий экземпляр ProjectContext; извлечение и итерации через коллекцию опубликованных проектов на сервере; создание, извлечение, проверка и удаление проекта с помощью объектной Project JavaScript сервера; и изменить свойства проекта.
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322668"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>Создание, извлечение, обновление и удаление проектов с Project JavaScript сервера

Сценарии в этой статье показывают, как получить текущий экземпляр **ProjectContext;** извлечение и итерации через коллекцию опубликованных проектов на сервере; создание, извлечение, проверка и удаление проекта с помощью объектной Project JavaScript сервера; и изменить свойства проекта. 
  
> [!NOTE]
> Эти сценарии определяют настраиваемый код на разметку страницы SharePoint приложения, но не используют файл с кодом, созданный Visual Studio 2012 г. для страницы. 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>Необходимые условия для работы с проектами Project Server 2013 в объектной модели JavaScript

Для выполнения сценариев, описанных в этой статье, необходимо установить и настроить следующие продукты:
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Инструменты разработчика Office для Visual Studio 2012
    
Кроме того, необходимо иметь разрешения на развертывание расширения SharePoint Server 2013 и участие в проектах.
  
> [!NOTE]
> Эти инструкции предполагают, что вы разрабатываете на компьютере, который Project Server 2013. 
  
## <a name="create-the-visual-studio-solution"></a>Создание решения Visual Studio
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

В следующих шагах создается Visual Studio 2012 года, которое содержит SharePoint проекта и страницу приложения. На странице содержится логика работы с проектами.
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Создание проекта SharePoint в Visual Studio

1. На компьютере, который Project Server 2013, запустите Visual Studio 2012 в качестве администратора.
    
2. В строке меню выберите пункты **Файл**, **Создать** и **Проект**.
    
3. В верхней части диалогового окна **Новый проект** выберите **.NET Framework 4.5** в раскрывающемся списке. 
    
4. В категории **Office/SharePoint** выберите **SharePoint Решения,** а затем выберите шаблон SharePoint **2013 Project.** 
    
5. Назови проект ProjectsJSOM и выберите **кнопку ОК.** 
    
6. В диалоговом окне **Мастер настройки SharePoint** выберите **Развернуть как решение фермы** и затем нажмите кнопку **Готово**. 
    
7. Изменение значения свойства **URL-адреса** сайта для проекта **ProjectsJSOM** в соответствие с URL-адресом экземпляра Project Web App (например, `https://ServerName/PWA` ).
    
### <a name="to-create-the-application-page-in-visual-studio"></a>Создание страницы приложения в Visual Studio

1. В **обозревателе** решений откройте меню ярлыков для проекта **ProjectsJSOM** и добавьте папку SharePoint "Layouts". 
    
2. В **папке Макеты** откройте меню ярлыков для папки **ProjectsJSOM,** а затем добавьте новую страницу приложения SharePoint ProjectsList.aspx.
    
3. Откройте меню ярлыка для страницы **ProjectsList.aspx** и выберите **Set as Startup Item**.
    
4. В разметке для страницы **ProjectsList.aspx** определите элементы управления пользовательским интерфейсом внутри тегов **asp:Content** "Main". 
    
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
   > [!Примечание] Эти элементы управления не могут быть использованы в каждом сценарии. Например, в сценарии "Создание проектов" не используются **элементы управления textarea** и **button.** 
  
5. После **тега** закрытия диапазона **добавьте тег SharePoint:ScriptLink,** **тег SharePoint:FormDigest** и  теги скрипта. 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   Тег **SharePoint:ScriptLink** ссылается на PS.js, который определяет объектную модель JavaScript для Project Server 2013. Тег **SharePoint:FormDigest** создает сообщение дайджеста для проверки подлинности при необходимости в операции, обновлять содержимое сервера. 
    
6. Замените комментарий держателя кодом из одной из следующих процедур:
    
   - [Создание проектов Project Server 2013 с помощью объектной модели JavaScript](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [Обновление Project Server 2013 с помощью объектной модели JavaScript](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [Удаление Project Server 2013 с помощью объектной модели JavaScript](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. Чтобы протестировать страницу приложения, в панели меню выберите команды **Отладка**, **Начать отладку**. Если вам предложено изменить файл web.config, выберите **ОК**.
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>Создание проектов Project Server 2013 с помощью объектной модели JavaScript
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

Процедура в этом разделе создает проекты с помощью объектной модели JavaScript. Процедура включает следующие действия высокого уровня:
  
1. Получите текущий **экземпляр ProjectContext.** 
    
2. Создайте **объект ProjectCreationInformation,** чтобы указать начальные свойства для проекта. Укажите необходимое **свойство имени** с помощью **функции ProjectCreationInformation.set_name.** 
    
3. Извлечение опубликованных проектов с сервера с помощью **ProjectContext.get_projects** функции. Функция **get_projects** возвращает **объект ProjectCollection.** 
    
4. Добавьте новый проект в коллекцию с помощью **функции ProjectCollection.add** и передав объект **ProjectCreationInformation.** 
    
5. Обновите коллекцию с помощью **функции ProjectCollection.update** и **функции ProjectContext.waitForQueueAsync.** Функция **обновления** возвращает объект **QueueJob,** который передается для **ожиданияForQueueAsync.** Этот вызов также публикует проект.
    
Вклейте следующий код между тегами **скрипта,** добавленными в приложении **To create the application page in Visual Studio** процедуре. 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>Обновление Project Server 2013 с помощью объектной модели JavaScript
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

Процедура в этом разделе обновляет **свойство startDate** проекта с помощью объектной модели JavaScript. Процедура включает следующие действия высокого уровня: 
  
1. Получите текущий **экземпляр ProjectContext.** 
    
2. Извлечение опубликованных проектов с сервера с помощью **ProjectContext.get_projects** функции. Функция **get_projects** возвращает **объект ProjectCollection.** 
    
3. Запустите запрос на сервере с помощью **функции ProjectContext.load** и **функцииProjectContext.exeCuteQueryAsync.** 
    
4. **Извлечение объекта PublishedProject** с помощью **функции ProjectContext.getById.** 
    
5. Ознакомьтесь с целевым проектом с помощью **функции Project.checkOut.** Функция **checkOut** возвращает проектную версию опубликованного проекта. 
    
6. Измените дату начала проекта с помощью **функции DraftProject.set_startDate.** 
    
7. Публикация проекта с помощью **функции DraftProject.publish** и **функции ProjectContext.waitForQueueAsync.** Функция **публикации** возвращает объект **QueueJob,** который передается для **ожиданияForQueueAsync.**
    
Вклейте следующий код между тегами **скрипта,** добавленными в приложении **To create the application page in Visual Studio** процедуре. 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>Удаление Project Server 2013 с помощью объектной модели JavaScript
<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

Процедура в этом разделе удаляет проект с помощью объектной модели JavaScript. Процедура включает следующие действия высокого уровня:
  
1. Получите текущий **экземпляр ProjectContext.** 
    
2. Извлечение опубликованных проектов с сервера с помощью **ProjectContext.get_projects** функции. Функция **get_projects** возвращает **объект ProjectCollection.** 
    
3. Запустите запрос на сервере с помощью **функции ProjectContext.load** и **функцииProjectContext.exeCuteQueryAsync.** 
    
4. **Извлечение объекта PublishedProject** с помощью **функции ProjectCollection.getById.** 
    
5. Удалите проект, передав его функции **ProjectCollection.remove.** 
    
6. Обновите коллекцию с помощью **функции ProjectCollection.update** и **функции ProjectContext.waitForQueueAsync.** Функция **обновления** возвращает объект **QueueJob,** который передается для **ожиданияForQueueAsync.**
    
Вклейте следующий код между тегами **скрипта,** добавленными в приложении **To create the application page in Visual Studio** процедуре. 
  
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

<a name="pj15_CRUDProjectsJSOM_AR"> </a>

## <a name="see-also"></a>См. также

- [Задачи программирования Project](project-programming-tasks.md)
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
    

