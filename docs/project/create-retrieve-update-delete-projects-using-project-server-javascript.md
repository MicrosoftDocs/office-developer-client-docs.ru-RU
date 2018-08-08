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
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>Создание, получение, обновление и удаление проектов с помощью Project Server JavaScript

Сценарии в этой статье показано, как для получения текущего экземпляра **ProjectContext** ; извлечение и выполнять итерацию по коллекции опубликованных проектов на сервере; Создание, получение, извлечение и удаления проекта с помощью объектной модели Project Server JavaScript; и изменить свойства проекта. 
  
> [!NOTE]
> Эти сценарии определение пользовательского кода в разметке страницы приложения SharePoint, но не используют файл фонового кода, который создает Visual Studio 2012 для страницы. 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>Необходимые условия для работы с Project Server 2013 проектов в объектной модели JavaScript

Для выполнения сценариев, описанных в этой статье, необходимо установить и настроить следующих продуктов:
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Инструменты разработчика Office для Visual Studio 2012
    
Кроме того, необходимо иметь разрешения для развертывания расширения для SharePoint Server 2013 и внесение данных в проектах.
  
> [!NOTE]
> Эти инструкции предполагают, что вы работаете на компьютере, на котором работает Project Server 2013. 
  
## <a name="create-the-visual-studio-solution"></a>Создание решения Visual Studio
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

Следующие шаги создания решения Visual Studio 2012, содержащий проекта SharePoint и страницу приложения. Страница содержит логику для работы с проектами.
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Создание проекта SharePoint в Visual Studio

1. На компьютере, на котором работает Project Server 2013 запустите Visual Studio 2012 с правами администратора.
    
2. В строке меню выберите пункты **Файл**, **Создать** и **Проект**.
    
3. В верхней части диалогового окна **Новый проект** выберите **.NET Framework 4.5** в раскрывающемся списке. 
    
4. В категории шаблонов **Office/SharePoint** щелкните **Решения SharePoint**и затем выберите шаблон **Проекта SharePoint 2013** . 
    
5. Назовите проект ProjectsJSOM и затем нажмите кнопку **ОК** . 
    
6. В диалоговом окне **Мастер настройки SharePoint** выберите **Развернуть как решение фермы** и затем нажмите кнопку **Готово**. 
    
7. Изменить значение свойства **URL-адрес сайта** проекта **ProjectsJSOM** в соответствии с URL-адрес экземпляра Project Web App (например, `http://ServerName/PWA`).
    
### <a name="to-create-the-application-page-in-visual-studio"></a>Создание страницы приложения в Visual Studio

1. В **Обозревателе решений**откройте контекстное меню для проекта **ProjectsJSOM** и добавьте SharePoint «Макеты» сопоставленная папка. 
    
2. В папке **Layouts** откройте контекстное меню для папки **ProjectsJSOM** и добавьте новую страницу приложения SharePoint с именем ProjectsList.aspx.
    
3. Откройте контекстное меню для страницы **ProjectsList.aspx** и выберите команду **назначить элемент**.
    
4. В разметке страницы **ProjectsList.aspx** определите элементы управления пользовательского интерфейса внутри тегов **asp: Content** «Главная», следующим образом. 
    
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
   > Эти элементы управления не могут быть использованы в каждом сценарии. Например сценарий «Создание проектов» не использует элементы управления **textarea** и **кнопка** . 
  
5. После закрывающего тега, **охватывающих** , добавьте тег **SharePoint:ScriptLink** , тег **SharePoint:FormDigest** и **теги,** как показано ниже. 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   Тег **SharePoint:ScriptLink** ссылается на файл PS.js, который определяет объектной модели JavaScript для Project Server 2013. Тег **SharePoint:FormDigest** создает сообщение дайджеста для проверки подлинности при необходимости в операции, обновлять содержимое сервера. 
    
6. Замените комментарий заполнитель на код из одного из следующих процедур:
    
   - [Создание проектов Project Server 2013 с помощью объектной модели JavaScript](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [Обновление проектов Project Server 2013 с помощью объектной модели JavaScript](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [Удаление проектов Project Server 2013 с помощью объектной модели JavaScript](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. Тестирование страницы приложения в строке меню выберите **Отладка**, **Начать отладку**. Если запрос на изменение файла web.config, нажмите кнопку **ОК**.
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>Создание проектов Project Server 2013 с помощью объектной модели JavaScript
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

Процедуры этого раздела создаются проекты с помощью объектной модели JavaScript. Процедура включает в себя следующие общие действия:
  
1. Получение текущего экземпляра **ProjectContext** . 
    
2. Создайте объект **ProjectCreationInformation** для указания начальной свойства проекта. Укажите требуемые **имя** свойства с помощью функции **ProjectCreationInformation.set_name** . 
    
3. Получение опубликованных проектов с сервера с помощью функции **ProjectContext.get_projects** . Функция **get_projects** возвращает объект **ProjectCollection** . 
    
4. Добавьте новый проект в коллекцию с помощью функции **ProjectCollection.add** , передав объект **ProjectCreationInformation** . 
    
5. Обновление семейства сайтов с помощью функции **ProjectCollection.update** и **ProjectContext.waitForQueueAsync** . Функция **обновления** возвращает объект **QueueJob** , передаваемых в **waitForQueueAsync**. Этот вызов также публикует проект.
    
Вставьте следующий код в тегах **сценария** , которые добавлены в процедуре, **Чтобы создать страницу приложения в Visual Studio** . 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>Обновление проектов Project Server 2013 с помощью объектной модели JavaScript
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

Процедуры в данном разделе обновляет свойства **startDate** проекта с помощью объектной модели JavaScript. Процедура включает в себя следующие общие действия: 
  
1. Получение текущего экземпляра **ProjectContext** . 
    
2. Получение опубликованных проектов с сервера с помощью функции **ProjectContext.get_projects** . Функция **get_projects** возвращает объект **ProjectCollection** . 
    
3. Запуск запроса на сервере с помощью функции **ProjectContext.load** и **ProjectContext.executeQueryAsync** . 
    
4. Извлеките объект **PublishedProject** с помощью функции **ProjectContext.getById** . 
    
5. Извлечение целевого проекта с помощью функции **Project.checkOut** . Функция **извлечения** Возвращает черновик опубликованного проекта. 
    
6. Измените дату начала проекта с помощью функции **DraftProject.set_startDate** . 
    
7. Публикация проекта с помощью функции **DraftProject.publish** и **ProjectContext.waitForQueueAsync** . Функция **публикации** возвращает объект **QueueJob** , передаваемых в **waitForQueueAsync**.
    
Вставьте следующий код в тегах **сценария** , которые добавлены в процедуре, **Чтобы создать страницу приложения в Visual Studio** . 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>Удаление проектов Project Server 2013 с помощью объектной модели JavaScript
<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

Процедуры этого раздела удаляет проекта с помощью объектной модели JavaScript. Процедура включает в себя следующие общие действия:
  
1. Получение текущего экземпляра **ProjectContext** . 
    
2. Получение опубликованных проектов с сервера с помощью функции **ProjectContext.get_projects** . Функция **get_projects** возвращает объект **ProjectCollection** . 
    
3. Запуск запроса на сервере с помощью функции **ProjectContext.load** и **ProjectContext.executeQueryAsync** . 
    
4. Извлеките объект **PublishedProject** с помощью функции **ProjectCollection.getById** . 
    
5. Удаление проекта с передачей их в функцию **ProjectCollection.remove** . 
    
6. Обновление семейства сайтов с помощью функции **ProjectCollection.update** и **ProjectContext.waitForQueueAsync** . Функция **обновления** возвращает объект **QueueJob** , передаваемых в **waitForQueueAsync**.
    
Вставьте следующий код в тегах **сценария** , которые добавлены в процедуре, **Чтобы создать страницу приложения в Visual Studio** . 
  
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
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
    

