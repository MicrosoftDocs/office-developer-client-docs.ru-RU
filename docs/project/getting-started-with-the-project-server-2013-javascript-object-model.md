---
title: Начало работы с объектной Project Server 2013 JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: В Project Server 2013 объектная модель JavaScript может использоваться в Project Online, мобильной и локальной разработке. В этом разделе представлен краткий обзор объектной модели JavaScript, а затем описано, как создать страницу приложения, которая извлекает и итерирует через проекты с помощью объектной модели JavaScript.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360475"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Начало работы с объектной Project Server 2013 JavaScript

В Project Server 2013 объектная модель JavaScript может использоваться в Project Online, мобильной и локальной разработке. В этом разделе представлен краткий обзор объектной модели JavaScript, а затем описано, как создать страницу приложения, которая извлекает и итерирует через проекты с помощью объектной модели JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>Использование объектной модели Project JavaScript сервера
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Использование объектной модели JavaScript — это отличный способ создания приложения с клиентской стороной (в отличие от управляемого клиентского кода, который должен работать удаленно). Приложения могут использовать объектную модель JavaScript для получения или изменения объектов, отправляя асинхронные вызовы на сервер. Приложения, которые используют объектную модель JavaScript, обычно развертываются в качестве настраиваемой SharePoint надстройки, страницы приложений и веб-части. Дополнительные сведения см. в странице "Типы компонентов SharePoint, которые могут быть в приложении для SharePoint" в [веб-сайтах host, веб-сайтах](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx)надстройки и SharePoint компоненты SharePoint 2013 г.
  
Объектная модель JavaScript реализует основные функции Project Server 2013, но объектная модель JavaScript и объектная модель сервера не имеют один к одному паритет. Точкой входа в объектную модель JavaScript является объект **ProjectContext,** который представляет клиентский контекст для Project Server 2013 и предоставляет доступ к содержимому и функциональным возможностям сервера. Объектная модель JavaScript для Project Server 2013 определяется в файле PS.js, который расположен в пути по умолчанию на `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` сервере приложений. Project Сервер 2013 также устанавливает файл PS.Debug.js в том же расположении. PS.Debug.js представляет собой неопределяемую версию PS.js, которая предоставляет IntelliSense информации. 
  
Объектная модель JavaScript позволяет проверку подлинности Forms, и все запросы проверки подлинности в качестве текущего пользователя. Дополнительные сведения о безопасности и других соображениях для разработки настраиваемого приложения и решений см. в нем: [Authentication, authorization and security in SharePoint 2013,](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx)Important [aspects of the SharePoint Add-in architecture and development landscape](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and SharePoint [add-ins compared with SharePoint solutions](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Для удаленного доступа SharePoint сайта SharePoint 2013 г. предоставляется меж доменная библиотека, которая позволяет делать клиентские меж доменные вызовы. Дополнительные сведения см. в SharePoint access [SharePoint 2013](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx)г. из надстройки с помощью меж доменной библиотеки. 
  
Многие концепции и процессы использования объектной модели JavaScript для Project Server 2013 напоминают концепции в связанных клиентских объектах. Дополнительные сведения о управляемой клиентской объектной модели Project Server 2013 см. в **примере Microsoft.ProjectServer.Client.** Дополнительные сведения о объектной модели 2013 SharePoint JavaScript и управляемой клиентской объектной модели см. в рублях Complete [basic operations using JavaScript library code in SharePoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) и [Complete basic operations using SharePoint 2013 client library code](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Погон: создание страницы приложения, которая извлекает и итерирует с помощью проектов
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Узнайте, как создать страницу приложения, которая отображает ID, имя и созданную дату каждого опубликованного проекта на сайте.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Необходимые условия для создания страницы приложения, которая извлекает и итерирует с помощью проектов
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Чтобы разработать страницу приложения, описанную в этом разделе, необходимо установить и настроить следующие продукты:
  
- SharePoint Server 2013
- Project Server 2013 с по крайней мере одним опубликованным проектом
- Visual Studio 2012
- Инструменты разработчика Office для Visual Studio 2012
    
Также необходимо иметь разрешения на развертывание расширения SharePoint Server 2013 и извлечение проектов.
  
> [!NOTE]
> Эти инструкции предполагают, что вы разрабатываете на компьютере, который Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Создание страницы приложения в Visual Studio 2012 г.
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

В следующих действиях создается SharePoint и страница приложения, содержаная таблицу и метку. В таблице отображаются сведения о проектах, а на этикетке отображаются сообщения об ошибках.
  
1. На компьютере, который Project Server 2013, запустите Visual Studio 2012 в качестве администратора.
    
2. Создайте пустой SharePoint 2013 г., следующим образом:
    
    1. В раскрывающемся списке в верхней части диалогового окна **Новый проект** выберите пункт **.NET Framework 4.5**. 
        
    2. В списке категорий шаблонов  выберите категорию Office SharePoint, а затем выберите SharePoint **2013 Project.** 
        
    3. Назови проект GetProjectsJSOM и выберите **кнопку ОК.** 
        
    4. В **диалоговом окне мастер** SharePoint настройки выберите **Развертывание** в качестве решения фермы, а затем выберите кнопку **ОК.** 
    
3. В Обозревателе решений изменить  значение свойства URL-адреса сайта для проекта **ProjectsJSOM** в соответствие с URL-адресом экземпляра Project Web App (например, `https://ServerName/PWA` ).
    
4. Откройте меню ярлыка для **проекта GetProjectsJSOM,** а затем добавьте SharePoint папку "Макеты". 
    
5. В **папке Макеты** откройте меню ярлыков для папки **GetProjectsJSOM,** а затем добавьте новую страницу приложения SharePoint ProjectsList.aspx.
    
   > [!NOTE]
   > В этом примере не используется файл с кодом, который Visual Studio 2012 для страницы приложения. 
  
6. Откройте меню ярлыка для страницы **ProjectsList.aspx** и выберите **Set as Startup Item**.
    
7. В разметке для страницы **ProjectsList.aspx** определите таблицу и местообнамерщик сообщений в тегах **asp:Content** "Main". 
    
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

### <a name="retrieving-the-projects-collection"></a>Сбор коллекции проектов
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

Следующие действия: извлечение и инициализация коллекции проектов.
  
1. После закрытия **тега div** **добавьте тег SharePoint:ScriptLink,** который ссылается на PS.js файл, как следует. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Ниже **тега SharePoint:ScriptLink** **добавьте** теги скрипта. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Объявите глобальную переменную для хранения коллекции проектов следующим образом.
    
   ```js
   var projects;
   ```

4. Позвоните **SP.SOD.executeOrDelayUntilScriptLoaded,** чтобы убедиться, что файл PS.js загружается перед запуском настраиваемого кода. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Добавьте функцию, которая подключается к текущему контексту и извлекает коллекцию проектов следующим образом.
    
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

   Некоторые клиентские объекты, полученные в контексте, не содержат данных до инициализации; то есть вы не можете получить доступ к значениям свойств объекта до инициализации объекта. Кроме того, для свойств типа **ValueObject** необходимо явно запросить свойство, прежде чем получить доступ к его значению. (Если вы пытаетесь получить доступ к свойству до инициализации, вы получите исключение **PropertyOrFieldNotInitializedException.)** 
    
   Чтобы инициализировать объект, необходимо вызвать метод нагрузки (или **метод loadQuery),** а затем **метод executeQueryAsync.**  
    
   - Вызов **функции нагрузки** или **функции loadQuery** регистрирует запрос, который необходимо выполнить на сервере. Вы передаете параметр, представляю который представляет объект, который необходимо получить. Если вы работаете с **свойством ValueObject,** вы также запрашиваете свойство в параметре. 
    
   - Вызов **функции executeQueryAsync** отправляет запрос на сервер асинхронно. При получении ответа на сервер вы передаете функцию успешного вызова и функцию вызова вызова с ошибкой. 
    
   Чтобы уменьшить сетевой трафик, запрашивать только свойства, с которые необходимо работать при вызове **функции нагрузки.** Кроме того, если вы работаете с несколькими  объектами, группу нескольких вызовов в функцию нагрузки перед вызовом функции **executeQueryAsync,** когда это возможно. 
    
### <a name="iterating-through-the-projects-collection"></a>Итерирование через коллекцию проектов
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

Следующие действия итерируют в коллекции проектов (если вызов сервера успешно) или отрисовка сообщения об ошибке (если вызов не удается).
  
1. Добавьте функцию вызова успешного вызова, которая итерируется в коллекции проектов, следующим образом.
    
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

2. Добавьте функцию вызова сбоя, которая передает сообщение об ошибке следующим образом.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Чтобы протестировать страницу приложения, в панели меню выберите команды **Отладка**, **Начать отладку**. Если вам предложено изменить файл web.config, выберите **ОК**.

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>Полный пример кода

Ниже приводится полный код из файла ProjectsList.aspx.
  
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

- [Создание, извлечение, обновление и удаление проектов с помощью объектной модели Project Server JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Начало работы с Project Server CSOM и .NET](getting-started-with-the-project-server-csom-and-net.md)
    

