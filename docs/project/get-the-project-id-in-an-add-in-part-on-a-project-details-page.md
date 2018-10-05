---
title: Получение ИД проекта в веб-части надстройки на странице сведений о проекте
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Добавьте в части размещаются в iframe элементы, которые являются полностью изолирована от внешнего размещения страницы. Для получения сведений о текущем проекте из части надстройки на страницу сведений о Project (PDP), можно использовать метод window.postMessage, прослушиватель событий и обработчик событий, который разбор код проекта из сообщения.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389885"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="3d58a-104">Получение ИД проекта в веб-части надстройки на странице сведений о проекте</span><span class="sxs-lookup"><span data-stu-id="3d58a-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="3d58a-105">Добавьте в части размещаются в **iframe** элементы, которые являются полностью изолирована от внешнего размещения страницы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="3d58a-106">Для получения сведений о текущем проекте из части надстройки на страницу сведений о Project (PDP), можно использовать метод **window.postMessage** , прослушиватель событий и обработчик событий, который разбор код проекта из сообщения.</span><span class="sxs-lookup"><span data-stu-id="3d58a-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="3d58a-107">Необходимые условия для создания размещенных в SharePoint надстройки часть, которая получает идентификатор проекта</span><span class="sxs-lookup"><span data-stu-id="3d58a-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="3d58a-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="3d58a-108"></span></span>

<span data-ttu-id="3d58a-109">Для использования в примере кода в этой статье, необходимо следующее:</span><span class="sxs-lookup"><span data-stu-id="3d58a-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="3d58a-110">SharePoint 2013 и Project Server 2013, настроенных для изоляции надстройки.</span><span class="sxs-lookup"><span data-stu-id="3d58a-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="3d58a-111">При разработке удаленно, сервер должен поддерживать sideloading надстроек или необходимо установить надстройку на сайте разработчика.</span><span class="sxs-lookup"><span data-stu-id="3d58a-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="3d58a-112">SharePoint Online и Project Online</span><span class="sxs-lookup"><span data-stu-id="3d58a-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="3d58a-113">Средства Visual Studio 2012 с Office для разработчиков Visual Studio 2013 для Visual Studio 2013 или Napa</span><span class="sxs-lookup"><span data-stu-id="3d58a-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="3d58a-114">Достаточные разрешения для пользователя, вошедшего в систему:</span><span class="sxs-lookup"><span data-stu-id="3d58a-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="3d58a-115">Разрешения локального администратора на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="3d58a-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="3d58a-116">Доступ на чтение по крайней мере один проект.</span><span class="sxs-lookup"><span data-stu-id="3d58a-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="3d58a-117">Разрешение на изменение страниц на сайт Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3d58a-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="3d58a-118">Необходимо войти в систему как кто-то отличную от учетной записи системы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="3d58a-119">Системную учетную запись не имеет разрешения, чтобы установить надстройку.</span><span class="sxs-lookup"><span data-stu-id="3d58a-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="3d58a-120">[Необходимые условия для создания надстройки уровня приложения для Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) более подробные сведения о надстройках для проекта.</span><span class="sxs-lookup"><span data-stu-id="3d58a-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="3d58a-121">В разделе [Настройка локальной среды разработки для SharePoint надстройки](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) рекомендации для локальной установки (включая отключение проверки замыкания на себя при необходимости).</span><span class="sxs-lookup"><span data-stu-id="3d58a-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="3d58a-122">При разработке удаленно, видеть [Разработка приложений для SharePoint в удаленной системе](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="3d58a-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="3d58a-123">Создание размещенных в SharePoint и надстройка клиентского веб-части</span><span class="sxs-lookup"><span data-stu-id="3d58a-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="3d58a-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="3d58a-124"></span></span>

1. <span data-ttu-id="3d58a-125">Откройте Visual Studio и выберите **файл** > **New** > **проекта**.</span><span class="sxs-lookup"><span data-stu-id="3d58a-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="3d58a-126">В диалоговом окне **Новый проект** выберите **.NET Framework 4.5** из раскрывающегося списка в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="3d58a-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="3d58a-127">В списке **шаблонов** выберите **Visual C#** > **Office/SharePoint** > **надстройки** > **Add-in SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="3d58a-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="3d58a-128">Назовите GetProjectIdAddinPart надстройки и затем нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="3d58a-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="3d58a-129">В диалоговом окне **новой надстройки для SharePoint** введите URL-адрес сайта Project Web Access, который требуется использовать для отладки (например: _https://contoso.com/sites/pwasite/_).</span><span class="sxs-lookup"><span data-stu-id="3d58a-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="3d58a-130">Выберите вариант **Размещение в SharePoint** для размещения надстройки и затем нажмите кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="3d58a-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="3d58a-131">В **Обозревателе решений**откройте контекстное меню для проекта GetProjectIdAddinPart и нажмите кнопку **Добавить** > **Новый элемент**.</span><span class="sxs-lookup"><span data-stu-id="3d58a-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="3d58a-132">В диалоговом окне **Добавление нового элемента** выберите **клиентская веб-часть (хост-сайта)**, имя веб-части GetProjectId и затем нажмите кнопку **Добавить** .</span><span class="sxs-lookup"><span data-stu-id="3d58a-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="3d58a-133">В диалоговом окне **Создание клиентов веб-части** выберите параметр **Создать новый клиент страницу веб-частей** и затем нажмите кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="3d58a-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="3d58a-134">Получите код проекта в части "надстройки"</span><span class="sxs-lookup"><span data-stu-id="3d58a-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="3d58a-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="3d58a-135"></span></span>

<span data-ttu-id="3d58a-136">В GetProjectId часть определяет его пользовательский код на странице GetProjectId.aspx веб-части клиента.</span><span class="sxs-lookup"><span data-stu-id="3d58a-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="3d58a-137">Определенные логику, которая получает и обрабатывает сообщение в элемент **head** страницы и элементы управления страницы определены в элемент **body** страницы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="3d58a-138">Откройте меню GetProjectId.aspx веб-части (в папке **страниц** ).</span><span class="sxs-lookup"><span data-stu-id="3d58a-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="3d58a-139">В элемент **head** страницы замените код в тегах **сценария** приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="3d58a-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
   ```js
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
                (function () {
                    var hostUrl = '';
                    var link = document.createElement('link');
                    link.setAttribute('rel', 'stylesheet');
                    if (document.URL.indexOf('?') != -1) {
                        var params = document.URL.split('?')[1].split('&');
                        for (var i = 0; i < params.length; i++) {
                            var p = decodeURIComponent(params[i]);
                            if (/^SPHostUrl=/i.test(p)) {
                                hostUrl = p.split('=')[1];
                                link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                                break;
                            }
                        }
                    }
                    if (hostUrl == '') {
                        link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
                    }
                    document.head.appendChild(link);
                })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
   ```

3. <span data-ttu-id="3d58a-140">Добавьте следующий код в элемент **body** страницы.</span><span class="sxs-lookup"><span data-stu-id="3d58a-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="3d58a-141">Код определяет элемент управления текст, который отображает идентификатор проекта.</span><span class="sxs-lookup"><span data-stu-id="3d58a-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="3d58a-142">В файле Elements.xml при необходимости измените имя, заголовок, описание и по умолчанию размер части надстройки.</span><span class="sxs-lookup"><span data-stu-id="3d58a-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="3d58a-143">В этом примере имеют значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d58a-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="3d58a-144">Чтобы протестировать часть надстройка, в строке меню выберите **Отладка**, **Начать отладку**.</span><span class="sxs-lookup"><span data-stu-id="3d58a-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="3d58a-145">Если появится запрос на изменение файла web.config, нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="3d58a-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="3d58a-146">Отладка части надстройки, установите соответствующие точки останова в скрипте, который вы добавили.</span><span class="sxs-lookup"><span data-stu-id="3d58a-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="3d58a-147">Перейдите на страницу страница сведений о Проекте и выберите команду **Изменить страницу** из меню "Сервис" (значок шестеренки).</span><span class="sxs-lookup"><span data-stu-id="3d58a-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="3d58a-148">Добавьте часть **GetProjectId заголовок** веб-части на странице.</span><span class="sxs-lookup"><span data-stu-id="3d58a-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="3d58a-149">КОД проекта отображается в элементе управления **охватывать** на странице веб-частей.</span><span class="sxs-lookup"><span data-stu-id="3d58a-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="3d58a-150">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="3d58a-150">Next steps</span></span>
<span data-ttu-id="3d58a-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="3d58a-151"></span></span>

<span data-ttu-id="3d58a-152">Часть надстройка в этом примере не получить доступ к данными Project Server или данных SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3d58a-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="3d58a-153">КОД продукта можно использовать для получения сведений о текущем проекте с помощью клиентского интерфейса API, например объектной модели JavaScript или службы REST.</span><span class="sxs-lookup"><span data-stu-id="3d58a-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="3d58a-154">В файле AppManifest.xml укажите разрешения, которые надстройка требуется доступ к Project Server данных или данных SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3d58a-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="3d58a-155">В разделе [Создание надстройки частей для установки с помощью надстройки SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) в этой статье описывается установка настраиваемых свойств для части надстройки.</span><span class="sxs-lookup"><span data-stu-id="3d58a-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="3d58a-156">Пример: Начало код проекта в части надстройки на странице страница сведений о Проекте</span><span class="sxs-lookup"><span data-stu-id="3d58a-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="3d58a-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="3d58a-157"></span></span>

<span data-ttu-id="3d58a-158">Следующий пример является полный код на страницу веб-часть клиента GetProjectID.aspx.</span><span class="sxs-lookup"><span data-stu-id="3d58a-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="3d58a-159">Этот код регистрирует прослушиватель событий и обработчик событий, который получает и анализирует сообщение, содержащее идентификатор проекта.</span><span class="sxs-lookup"><span data-stu-id="3d58a-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
```HTML
<%@ Page language="C#" Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<WebPartPages:AllowFraming ID="AllowFraming" runat="server" />
<html>
<head>
    <title></title>
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/MicrosoftAjax.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.js"></script>
    <script type="text/javascript">
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
        (function () {
            var hostUrl = '';
            var link = document.createElement('link');
            link.setAttribute('rel', 'stylesheet');
            if (document.URL.indexOf('?') != -1) {
                var params = document.URL.split('?')[1].split('&');
                for (var i = 0; i < params.length; i++) {
                    var p = decodeURIComponent(params[i]);
                    if (/^SPHostUrl=/i.test(p)) {
                        hostUrl = p.split('=')[1];
                        link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                        break;
                    }
                }
            }
            if (hostUrl == '') {
                link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
            }
            document.head.appendChild(link);
        })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
    </script>
</head>
<body>
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
</body>
</html>

```

## <a name="see-also"></a><span data-ttu-id="3d58a-160">См. также</span><span class="sxs-lookup"><span data-stu-id="3d58a-160">See also</span></span>

- [<span data-ttu-id="3d58a-161">Задачи программирования Project</span><span class="sxs-lookup"><span data-stu-id="3d58a-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="3d58a-162">Создание надстройки Project Server с размещением в SharePoint</span><span class="sxs-lookup"><span data-stu-id="3d58a-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="3d58a-163">Создание веб-частей надстройки для установки совместно с надстройкой SharePoint</span><span class="sxs-lookup"><span data-stu-id="3d58a-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

