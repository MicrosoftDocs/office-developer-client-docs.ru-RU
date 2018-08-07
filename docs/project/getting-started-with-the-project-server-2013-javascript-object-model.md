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
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Приступая к работе с объектной моделью Project Server 2013 JavaScript

В Project Server 2013 объектной модели JavaScript можно использовать в Project Online разработке для мобильных устройств и локально. В этом разделе представлен краткий обзор объектной модели JavaScript, а затем описывается, как создать страницу приложения, которая извлекает и итерацию проектов с помощью объектной модели JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>С помощью объектной модели Project Server JavaScript
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

С помощью объектной модели JavaScript — это отличный способ для создания приложений, на котором работает со стороны клиента (в отличие от клиентского управляемого кода, которое необходимо запускать удаленно). Приложения могут использовать объектной модели JavaScript для извлечения или изменения объектов, отправив асинхронных вызовов на сервер. Приложений, использующих объектную модель JavaScript обычно развертываются как настраиваемые надстройки SharePoint, страницы приложений и веб-частей. Для получения дополнительных сведений см. «Типы компонентов SharePoint, которые могут находиться в приложении для SharePoint» в [хост-сайты, добавьте в веб-сайтов и компоненты SharePoint в SharePoint 2013](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).
  
Объектная модель JavaScript реализует основные функциональные возможности Project Server 2013, но объектная модель JavaScript и серверной объектной модели не имеют возможности один к одному. Точка входа в объектной модели JavaScript — это объект **ProjectContext** , который представляет контекст клиента для Project Server 2013 и предоставляет доступ к содержимому сервера и функциональные возможности. Объектная модель JavaScript для Project Server 2013 определяется в файле PS.js, который находится в каталоге путь по умолчанию `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` на сервере приложений. Project Server 2013 также устанавливается PS. Файл Debug.js в одном месте. PS. Debug.js является более unminified версии PS.js, который предоставляет сведения IntelliSense. 
  
Объектная модель JavaScript позволяет проверка подлинности через формы, а все запросы проходят проверку подлинности имени текущего пользователя. Дополнительные сведения о безопасности и рекомендации по разработке пользовательских приложений и решений см в разделе [Проверка подлинности, авторизации и безопасности в SharePoint 2013](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx) [важные аспекты архитектуры SharePoint надстройки и разработки Альбомная](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)и [надстройки SharePoint по сравнению с решениями SharePoint](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Удаленный доступ к данным на сайте SharePoint, SharePoint 2013 предоставляет междоменной библиотеки, которая позволяет выполнять междоменных вызовов со стороны клиента. Для получения дополнительных сведений см [доступа к SharePoint 2013 данные из надстроек с помощью междоменной библиотеки](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx). 
  
Многие основные понятия и процессы, используемые для использования объектной модели JavaScript для Project Server 2013 похожи в связанных с ними клиентских объектных моделей. Дополнительные сведения о Project Server 2013 управляемой клиентской объектной модели можно **Microsoft.ProjectServer.Client**. Дополнительные сведения об объектной модели SharePoint 2013JavaScript и управляемой клиентской объектной модели можно [выполнения основных операций с использованием кода библиотеки JavaScript в SharePoint 2013](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) и [выполнения базовых операций, с помощью клиента SharePoint 2013 код библиотеки](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Пошаговое руководство: Создание страницы приложения, которое получает и выполняется итерация по проектам
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Узнайте, как создать страницу приложения, которое отображает идентификатор, имя и даты создания каждого опубликованного проекта на сайте.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Необходимые условия для создания страницы приложения, которое получает и выполняется итерация по проектам
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Чтобы разработать страницу приложения, описанного в данном разделе, необходимо установить и настроить следующих продуктов:
  
- SharePoint Server 2013
- Project Server 2013 с помощью по крайней мере один опубликованного проекта
- Visual Studio 2012
- Инструменты разработчика Office для Visual Studio 2012
    
Кроме того, необходимо иметь разрешения для развертывания расширения для SharePoint Server 2013 и для получения проектов.
  
> [!NOTE]
> Эти инструкции предполагают, что вы работаете на компьютере, на котором работает Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Создание страницы приложения в Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

Следующие шаги создания проекта SharePoint и страницу приложения, которая содержит таблицы и метку. В таблице показаны сведения о проектах, и отображает сообщения об ошибках.
  
1. На компьютере, на котором работает Project Server 2013 запустите Visual Studio 2012 с правами администратора.
    
2. Создайте пустой проект SharePoint 2013, как показано ниже:
    
    1. В диалоговом окне **Новый проект** выберите **.NET Framework 4.5** из раскрывающегося списка в верхней части окна. 
        
    2. В списке категории шаблонов выберите категорию **Office SharePoint** и затем выберите шаблон **Проекта SharePoint 2013** . 
        
    3. Назовите проект GetProjectsJSOM и затем нажмите кнопку **ОК** . 
        
    4. В диалоговом окне **Мастер настройки SharePoint** выберите **Развернуть как решение фермы**и затем нажмите кнопку **ОК** . 
    
3. В окне Обозреватель решений, изменить значение свойства **URL-адрес сайта** проекта **ProjectsJSOM** в соответствии с URL-адрес экземпляра Project Web App (например, `http://ServerName/PWA`).
    
4. Откройте контекстное меню для проекта **GetProjectsJSOM** , а затем добавьте SharePoint «Макеты» сопоставленная папка. 
    
5. В папке **Layouts** откройте контекстное меню для папки **GetProjectsJSOM** и добавьте новую страницу приложения SharePoint с именем ProjectsList.aspx.
    
   > [!NOTE]
   > В этом примере не используется файл фонового кода, который создает Visual Studio 2012 страницы приложения. 
  
6. Откройте контекстное меню для страницы **ProjectsList.aspx** и выберите команду **назначить элемент**.
    
7. В разметке страницы **ProjectsList.aspx** определите таблицу и заполнитель сообщения внутри тегов **asp: Content** «Главная», как показано ниже. 
    
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

### <a name="retrieving-the-projects-collection"></a>Получение коллекции проектов
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

Следующие шаги извлечения и инициализация коллекции проектов.
  
1. После закрывающего тега **div** , добавьте тег **SharePoint:ScriptLink** , который ссылается на файл PS.js, как показано ниже. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Под тегом **SharePoint:ScriptLink** добавьте теги **сценария** следующим образом. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Объявите глобальную переменную для хранения коллекции проектов, как показано ниже.
    
   ```js
   var projects;
   ```

4. Вызов **SP. SOD.executeOrDelayUntilScriptLoaded** метод, чтобы гарантировать, что файл PS.js загружается перед выполнением пользовательского кода. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Добавление функции, которая подключается к текущий контекст и получает коллекции проектов, как показано ниже.
    
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

   Некоторые клиентские объекты, которые извлекают в контексте не содержат данных до инициализации; то есть значения свойств объекта недоступны до инициализации объекта. Кроме того для свойства типа **ValueObject**необходимо явно запросить свойства для доступа к его значение. (При попытке доступа к свойству до его инициализации, вы получаете исключение **PropertyOrFieldNotInitializedException** .) 
    
   Чтобы инициализировать объект, вызовите метод **load** (или метод **loadQuery** ) и затем метода **executeQueryAsync** . 
    
   - Вызов функции **загрузки** или функция **loadQuery** регистрирует запрос, который требуется запустить на сервере. Передайте параметр, представляющий объект, который требуется получить. При работе со свойством **ValueObject** можно также запрашивать свойства с помощью параметра. 
    
   - Вызов функции **executeQueryAsync** асинхронно отправляет запрос запросов к серверу. Передать функцию обратного вызова для успеха и функции обратного вызова сбоя для вызова при получении ответа сервера. 
    
   Чтобы уменьшить сетевой трафик, запросите только свойства, которые вы хотите работать с при вызове функции **загрузки** . Кроме того при работе с несколькими объектами групповой несколько вызовов функции **нагрузки** перед вызовите функцию **executeQueryAsync** , если это возможно. 
    
### <a name="iterating-through-the-projects-collection"></a>Итерации по коллекции проектов
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

Следующие шаги итерации по коллекции проектов (если вызов сервера выполнен успешно) или отображать сообщение об ошибке (если не удается выполнить звонок).
  
1. Добавление функции обратного вызова успех, который выполняет итерацию по коллекции проектов, следующим образом.
    
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

2. Добавьте функцию обратного вызова ошибка, отображается сообщение об ошибке следующим образом.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Тестирование страницы приложения в строке меню выберите **Отладка**, **Начать отладку**. Если запрос на изменение файла web.config, нажмите кнопку **ОК**.

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>Полный пример кода

Ниже приведен полный код из файла ProjectsList.aspx.
  
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

<a name="pj15_GetStartedJSOM_AR"> </a>

## <a name="see-also"></a>См. также

- [Создание, получение, обновление и удаление проектов с помощью объектной модели Project Server JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Начало работы с Project Server CSOM и .NET](getting-started-with-the-project-server-csom-and-net.md)
    

