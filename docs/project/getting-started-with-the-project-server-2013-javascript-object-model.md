---
title: Начало работы с объектной моделью JavaScript Project Server 2013
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: В Project Server 2013 объектная модель JavaScript может использоваться в Project Online, мобильных и локальных разработках. В этом разделе представлен краткий обзор объектной модели JavaScript, а затем показано, как создать страницу приложения, которая получает и просматривает проекты с помощью объектной модели JavaScript.
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360475"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Начало работы с объектной моделью JavaScript Project Server 2013

В Project Server 2013 объектная модель JavaScript может использоваться в Project Online, мобильных и локальных разработках. В этом разделе представлен краткий обзор объектной модели JavaScript, а затем показано, как создать страницу приложения, которая получает и просматривает проекты с помощью объектной модели JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>Использование объектной модели JavaScript Project Server
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

С помощью объектной модели JavaScript можно создать приложение, которое работает на стороне клиента (а не в управляемом клиентском коде, который необходимо запускать удаленно). Приложения могут использовать объектную модель JavaScript для извлечения или изменения объектов путем отправки асинхронных вызовов на сервер. Приложения, использующие объектную модель JavaScript, обычно развертываются как пользовательские надстройки SharePoint, страницы приложений и веб-части. Дополнительные сведения см. в разделе "типы компонентов SharePoint, которые могут находиться в приложении для SharePoint" на [хост-сайтах, веб-сайтах надстроек и компонентах SharePoint в sharepoint 2013](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).
  
Объектная модель JavaScript реализует основные функциональные возможности Project Server 2013, но объектная модель JavaScript и Серверная объектная модель не имеют проверки четности "один к одному". Точкой входа для объектной модели JavaScript является объект **ProjectContext** , который представляет собой клиентский контекст для Project Server 2013 и предоставляет доступ к содержимому и функциям сервера. Объектная модель JavaScript для Project Server 2013 определена в файле PS. js, расположенном по пути `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` по умолчанию на сервере приложений. Project Server 2013 также устанавливает PS. Файл debug. js в том же расположении. PCL. Debug. js — это унминифиед версия файла PS. js, которая предоставляет информацию IntelliSense. 
  
Объектная модель JavaScript позволяет использовать проверку подлинности на основе форм, а все запросы проходят проверку подлинности текущего пользователя. Для получения дополнительных сведений о безопасности и других рекомендациях по проектированию пользовательских приложений и решений, ознакомьтесь с разделом [Проверка подлинности, авторизация и безопасность в SharePoint 2013](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [важные аспекты архитектуры и разработки надстройки SharePoint](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), а также [надстройки SharePoint в сравнении с решениями SharePoint](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).
  
> [!NOTE]
> Для удаленного доступа к данным с сайта SharePoint SharePoint 2013 предоставляет междоменную библиотеку, позволяющую выполнять междоменные вызовы на стороне клиента. Для получения дополнительных сведений ознакомьтесь [со статьей доступ к данным в SharePoint 2013 из надстроек с помощью междоменной библиотеки](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx). 
  
Многие концепции и процессы для использования объектной модели JavaScript для Project Server 2013 похожи на те, которые относятся к связанным клиентским объектным моделям. Дополнительные сведения об управляемой клиентской объектной модели Project Server 2013 можно найти в **статье Microsoft. Project. Client**. Дополнительные сведения об объектной модели 2013JavaScript и управляемой клиентской объектной модели приведены [в статье выполнение базовых операций с использованием кода библиотеки JavaScript в sharepoint 2013](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) и [Выполнение базовых операций с использованием кода клиентской библиотеки SharePoint 2013](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Пошаговое руководство: Создание страницы приложения, которая получает и просматривает проекты
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Узнайте, как создать страницу приложения, которая отображает идентификатор, имя и дату создания каждого опубликованного проекта на сайте.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Необходимые условия для создания страницы приложения, которая извлекает и просматривает проекты
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Для разработки страницы приложения, описанной в этом разделе, необходимо установить и настроить следующие продукты:
  
- SharePoint Server 2013
- Project Server 2013 с по крайней мере одним опубликованным проектом
- Visual Studio 2012
- Инструменты разработчика Office для Visual Studio 2012
    
Кроме того, необходимо иметь разрешения на развертывание расширения в SharePoint Server 2013 и получение проектов.
  
> [!NOTE]
> В этих инструкциях предполагается, что вы разрабатываете на компьютере, на котором работает Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Создание страницы приложения в Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

Выполните следующие действия, чтобы создать проект SharePoint и страницу приложения, содержащие таблицу и метку. В таблице отображаются сведения о проектах, а в метке отображаются сообщения об ошибках.
  
1. На компьютере, на котором работает Project Server 2013, запустите Visual Studio 2012 от имени администратора.
    
2. Создайте пустой проект SharePoint 2013, как показано ниже:
    
    1. В раскрывающемся списке в верхней части диалогового окна **Новый проект** выберите пункт **.NET Framework 4.5**. 
        
    2. В списке категорий шаблонов выберите категорию **Office SharePoint** , а затем выберите шаблон **проекта SharePoint 2013** . 
        
    3. Назовите проект Жетпрожектсжсом, а затем нажмите кнопку **ОК** . 
        
    4. В диалоговом окне **Мастер настройки SharePoint** выберите **Развернуть как решение фермы**, а затем нажмите кнопку **ОК** . 
    
3. В обозревателе решений измените значение свойства **URL-адрес сайта** для проекта **прожектсжсом** , чтобы оно было соответствующим URL-адресу экземпляра Project Web App (например, `https://ServerName/PWA`).
    
4. Откройте контекстное меню для проекта **жетпрожектсжсом** и добавьте сопоставленную папку "макеты SharePoint". 
    
5. В папке **Layouts** откройте контекстное меню для папки **жетпрожектсжсом** и добавьте новую страницу приложения SharePoint с именем прожектслист. aspx.
    
   > [!NOTE]
   > В этом примере не используется файл кода программной части, который Visual Studio 2012 создает для страницы приложения. 
  
6. Откройте контекстное меню для страницы **прожектслист. aspx** и выберите пункт **Назначить запускаемым элементом**.
    
7. В разметке для страницы **прожектслист. aspx** определите таблицу и заполнитель сообщения внутри "Main" **ASP: Content** Tags, как показано ниже. 
    
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

Следующие шаги извлекают и инициализируют коллекцию Projects.
  
1. После закрывающего тега **div** добавьте тег **SharePoint: ScriptLink** , ссылающийся на файл PS. js, как показано ниже. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Под тегом **SharePoint: ScriptLink** добавьте теги **скрипта** , как показано ниже. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Объявите глобальную переменную для хранения коллекции Projects, как показано ниже.
    
   ```js
   var projects;
   ```

4. Вызовите **пакет SP. Метод СОД. Ексекутеорделайунтилскриптлоадед** , чтобы убедиться, что файл PS. js загружен перед запуском пользовательского кода. 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. Добавьте функцию, которая подключается к текущему контексту и получает коллекцию проектов, как показано ниже.
    
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

   Некоторые клиентские объекты, получаемые через контекст, не содержат данных, пока не будут инициализированы; то есть невозможно получить доступ к значениям свойства объекта до инициализации объекта. Кроме того, для свойств типа **валуеобжект**необходимо явным образом запросить свойство, чтобы получить доступ к его значению. (Если вы попытаетесь получить доступ к свойству до его инициализации, вы получите исключение **пропертйорфиелднотинитиализедексцептион** .) 
    
   Для инициализации объекта вызывается метод **Load** (или метод **LoadQuery** ), а затем метод **executeQueryAsync** . 
    
   - При вызове функции **Load** или **LoadQuery** регистрируется запрос, который необходимо запустить на сервере. Вы передаете параметр, представляющий объект, который требуется получить. Если вы работаете со свойством **валуеобжект** , вы также запрашиваете свойство в параметре. 
    
   - При вызове функции **executeQueryAsync** запрос отправляется на сервер асинхронно. Вы передаете функцию обратного вызова для успешного выполнения и функцию обратного вызова при сбое, которая вызывается при получении ответа сервера. 
    
   Чтобы уменьшить сетевой трафик, запросите только те свойства, с которыми вы хотите работать при вызове функции **Load** . Кроме того, если вы работаете с несколькими объектами, сгруппируйте несколько вызовов функции **Load** перед вызовом функции **executeQueryAsync** , когда это возможно. 
    
### <a name="iterating-through-the-projects-collection"></a>Итерация коллекции проектов
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

Выполните следующие действия, чтобы выполнить итерацию коллекции проектов (при успешном вызове сервера) или отобразить сообщение об ошибке (если вызов завершается с ошибкой).
  
1. Добавьте функцию обратного вызова для успешного выполнения, которая выполняет итерацию коллекции Projects, как показано ниже.
    
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

2. Добавьте функцию обратного вызова при сбое, которая отображает сообщение об ошибке, как показано ниже.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Чтобы протестировать страницу приложения, в панели меню выберите команды **Отладка**, **Начать отладку**. Если вам будет предложено изменить файл Web. config, нажмите кнопку **ОК**.

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>Полный пример кода

Ниже приведен полный код из файла Прожектслист. aspx.
  
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

- [Создание, получение, обновление и удаление проектов с помощью объектной модели JavaScript Project Server](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Начало работы с Project Server CSOM и .NET](getting-started-with-the-project-server-csom-and-net.md)
    

