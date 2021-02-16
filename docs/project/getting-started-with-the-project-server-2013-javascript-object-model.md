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
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Начало работы с объектной моделью JavaScript для Project Server 2013

В Project Server 2013 объектную модель JavaScript можно использовать в Project Online, мобильных устройствах и локальной разработке. В этом разделе представлен краткий обзор объектной модели JavaScript, а затем описано, как создать страницу приложения, которая извлекает и итерирует проекты с помощью объектной модели JavaScript.
  
## <a name="using-the-project-server-javascript-object-model"></a>Использование объектной модели JavaScript для Project Server
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Использование объектной модели JavaScript — отличный способ создать приложение, которое работает на стороне клиента (в отличие от управляемого клиентского кода, который должен работать удаленно). Приложения могут использовать объектную модель JavaScript для извлечения или изменения объектов, отправляя асинхронные вызовы на сервер. Приложения, которые используют объектную модель JavaScript, обычно развертываются как пользовательские надстройки SharePoint, страницы приложений и веб-части. Дополнительные сведения см. в подстройки "Типы компонентов SharePoint, которые могут быть в приложении для SharePoint" на хост-сайтах, сайтах надстройки и компонентах SharePoint в [SharePoint 2013.](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx)
  
Объектная модель JavaScript реализует основные функции Project Server 2013, но объектная модель JavaScript и серверная объектная модель не имеют четности "один к одному". Точка входа в объектную модель JavaScript — это объект **ProjectContext,** который представляет контекст клиента для Project Server 2013 и предоставляет доступ к контенту и функциям сервера. Объектная модель JavaScript для Project Server 2013 определена в файле PS.js, который расположен в пути по умолчанию на  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` сервере приложений. Project Server 2013 также устанавливает PS.Debug.js в том же расположении. PS.Debug.js является неустановленной версией PS.js, которая предоставляет IntelliSense сведения. 
  
Объектная модель JavaScript разрешает проверку подлинности на форме, а все запросы аутентификация как текущего пользователя. Дополнительные сведения о безопасности и другие аспекты разработки пользовательских приложений и решений см. в документах "Проверка подлинности,авторизация и безопасность" в [SharePoint 2013,](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx)"Важные аспекты архитектуры и разработки надстройки [SharePoint"](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)и "Сравнение надстройки SharePoint с решениями [SharePoint".](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx)
  
> [!NOTE]
> Для удаленного доступа к данным с сайта SharePoint SharePoint 2013 предоставляет меж доменную библиотеку, которая позволяет делать меж доменные вызовы на стороне клиента. Дополнительные сведения см. в данных [Access SharePoint 2013](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx)из надстройки, использующих меж доменную библиотеку. 
  
Многие концепции и процессы использования объектной модели JavaScript для Project Server 2013 похожи на концепции в связанных клиентских объектных моделях. Дополнительные сведения об управляемой клиентской объектной модели Project Server 2013 см. в примере **Microsoft.ProjectServer.Client.** Дополнительные сведения об объектной модели SharePoint 2013JavaScript и управляемой клиентской объектной модели см. в подразделе "Основные операции с использованием кода библиотеки JavaScript в [SharePoint 2013"](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) и "Завершение базовых операций с использованием кода клиентской библиотеки [SharePoint 2013".](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx)
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Walkthrough: Creating an application page that retrieves and iterates through projects
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

Узнайте, как создать страницу приложения, которая отображает ИД, имя и дату создания каждого опубликованного проекта на сайте.
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>Необходимые условия для создания страницы приложения, которая извлекает и итерирует проекты
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

Для разработки страницы приложения, описанной в этом разделе, необходимо установить и настроить следующие продукты:
  
- SharePoint Server 2013
- Project Server 2013 с хотя бы одним опубликованным проектом
- Visual Studio 2012
- Инструменты разработчика Office для Visual Studio 2012
    
Кроме того, необходимо иметь разрешения на развертывание расширения в SharePoint Server 2013 и извлечение проектов.
  
> [!NOTE]
> В этих инструкциях предполагается, что разработка происходит на компьютере с Project Server 2013. 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Создание страницы приложения в Visual Studio 2012
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

Следующие действия создают проект SharePoint и страницу приложения, которая содержит таблицу и метку. В таблице отображаются сведения о проектах, а метка отображает сообщения об ошибках.
  
1. На компьютере с Project Server 2013 запустите Visual Studio 2012 от учетной записи администратора.
    
2. Создайте пустой проект SharePoint 2013 следующим образом:
    
    1. В раскрывающемся списке в верхней части диалогового окна **Новый проект** выберите пункт **.NET Framework 4.5**. 
        
    2. В списке категорий шаблонов выберите категорию **Office SharePoint,** а затем выберите шаблон **Проекта SharePoint 2013.** 
        
    3. Назовем проект GetProjectsJSOM и  затем нажимаем кнопку "ОК". 
        
    4. В **диалоговом окне** мастера настройки SharePoint выберите "Развернуть как решение фермы" **и** затем кнопку "ОК".  
    
3. В обозревателе решений отредактируем значение свойства **URL-адреса** сайта для проекта **ProjectsJSOM** в соответствие с URL-адресом экземпляра Project Web App (например). `https://ServerName/PWA`
    
4. Откройте меню ярлыка для проекта **GetProjectsJSOM,** а затем добавьте папку SharePoint "Layouts". 
    
5. В **папке Layouts** откройте меню ярлыка для папки **GetProjectsJSOM** и добавьте новую страницу приложения SharePoint с именем ProjectsList.aspx.
    
   > [!NOTE]
   > В этом примере не используется файл кода,который Visual Studio 2012 для страницы приложения. 
  
6. Откройте меню ярлыка для страницы **ProjectsList.aspx** и выберите **"Установить как элемент запуска".**
    
7. В разметке для страницы **ProjectsList.aspx** определите таблицу и замещение сообщений в тегах **Asp:Content,** как поется ниже. 
    
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

### <a name="retrieving-the-projects-collection"></a>Ирисовка коллекции проектов
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

Следующие действия по извлечению и инициализации коллекции проектов.
  
1. После закрытия **тега div** добавьте тег **SharePoint:ScriptLink,** который ссылается на PS.js файла, как пошагово. 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. Под **тегом SharePoint:ScriptLink** добавьте **теги** скрипта следующим образом. 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. Объявите глобальную переменную для хранения коллекции проектов следующим образом.
    
   ```js
   var projects;
   ```

4. Вызовите **методSP.SOD.exeOrDelayUntilScriptLoaded,** чтобы убедиться, что PS.js загружается перед запуском пользовательского кода. 
    
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

   Некоторые клиентские объекты, которые вы извлекаете через контекст, не содержат данных до их инициализации; то есть вы не сможете получить доступ к значениям свойств объекта, пока объект не будет инициализирован. Кроме того, для свойств типа **ValueObject** необходимо явно запросить свойство, прежде чем получить доступ к его значению. (При попытке получить доступ к свойству до его инициализации вы получите исключение **PropertyOrFieldNotInitializedException.)** 
    
   Чтобы инициализировать объект, вызовите метод **load** (или **метод loadQuery),** а затем **метод executeQueryAsync.** 
    
   - Вызов **функции загрузки** или **loadQuery** регистрирует запрос, который необходимо выполнить на сервере. Передав параметр, который представляет объект, который необходимо получить. Если вы работаете со **свойством ValueObject,** вы также запрашиваете свойство в параметре. 
    
   - Вызов **функции executeQueryAsync** асинхронно отправляет запрос на сервер. Вы передаете функцию успешного вызова и функцию ответного вызова сбоя для вызова при получении ответа сервера. 
    
   Чтобы уменьшить сетевой трафик, запрашивать только свойства, с которые необходимо работать при вызове **функции загрузки.** Кроме того, если вы работаете с несколькими  объектами, группу нескольких вызовов функции загрузки, прежде чем вызывать **функцию executeQueryAsync,** когда это возможно. 
    
### <a name="iterating-through-the-projects-collection"></a>Итерации по коллекции проектов
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

Следующие действия проходят по коллекции проектов (при успешном вызове сервера) или отрисовке сообщения об ошибке (если вызов не удается).
  
1. Добавьте функцию успешного вызова, которая проходит по коллекции проектов следующим образом.
    
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

2. Добавьте функцию вызова сбоя, которая отрисовка сообщения об ошибке следующим образом.
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. Чтобы протестировать страницу приложения, в панели меню выберите команды **Отладка**, **Начать отладку**. Если вам будет предложено изменить файл web.config, выберите **"ОК".**

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

- [Создание, извлечение, обновление и удаление проектов с помощью объектной модели JavaScript для Project Server](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Клиентская объектная модель (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md)
- [Начало работы с Project Server CSOM и .NET](getting-started-with-the-project-server-csom-and-net.md)
    

