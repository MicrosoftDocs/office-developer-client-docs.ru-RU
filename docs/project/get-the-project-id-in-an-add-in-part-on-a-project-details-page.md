---
title: Получение ИД проекта в веб-части надстройки на странице сведений о проекте
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Части надстройки размещены в элементах iframe, полностью изолированных от страницы размещения. Чтобы получить сведения о текущем проекте из части надстройки на странице Project Details Page (PDP), вы можете использовать метод window.postMessage, слушателя событий и обработщика событий, который разберет ИД проекта из сообщения.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322598"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="3999e-104">Получение ИД проекта в веб-части надстройки на странице сведений о проекте</span><span class="sxs-lookup"><span data-stu-id="3999e-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="3999e-105">Части надстройки размещены в **элементах iframe,** полностью изолированных от страницы размещения.</span><span class="sxs-lookup"><span data-stu-id="3999e-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="3999e-106">Чтобы получить сведения о текущем проекте из части надстройки на странице Project Details Page (PDP), вы можете использовать метод **window.postMessage,** прослушиватель событий и обработщик событий, который разберет ID проекта из сообщения.</span><span class="sxs-lookup"><span data-stu-id="3999e-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="3999e-107">Необходимые условия для создания SharePoint надстройки, которая получает ID проекта</span><span class="sxs-lookup"><span data-stu-id="3999e-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="3999e-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="3999e-108"><a name="Prereqs"> </a></span></span>

<span data-ttu-id="3999e-109">Чтобы использовать пример кода в этой статье, вам потребуется один из следующих ниже.</span><span class="sxs-lookup"><span data-stu-id="3999e-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="3999e-110">SharePoint 2013 и Project Server 2013, настроенных для изоляции надстройки.</span><span class="sxs-lookup"><span data-stu-id="3999e-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="3999e-111">Если вы разрабатываете удаленно, сервер должен поддерживать загрузку надстройок, либо необходимо установить надстройку на сайте разработчика.</span><span class="sxs-lookup"><span data-stu-id="3999e-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="3999e-112">SharePoint Онлайн и Project Online</span><span class="sxs-lookup"><span data-stu-id="3999e-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="3999e-113">Visual Studio 2013 2012 Visual Studio с Office средствами разработки для Visual Studio 2013 или Napa</span><span class="sxs-lookup"><span data-stu-id="3999e-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="3999e-114">Достаточные разрешения для пользователя, вошедшего в систему:</span><span class="sxs-lookup"><span data-stu-id="3999e-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="3999e-115">Разрешения локального администратора на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="3999e-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="3999e-116">Ознакомьтесь с доступом по крайней мере к одному проекту.</span><span class="sxs-lookup"><span data-stu-id="3999e-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="3999e-117">Разрешение на редактирование страниц на Project Web App сайте.</span><span class="sxs-lookup"><span data-stu-id="3999e-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="3999e-118">Необходимо войти в систему как кто-то отличную от учетной записи системы.</span><span class="sxs-lookup"><span data-stu-id="3999e-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="3999e-119">Учетная запись системы не имеет разрешения на установку надстройки.</span><span class="sxs-lookup"><span data-stu-id="3999e-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="3999e-120">Дополнительные сведения о надстройки для [Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) см. в Project.</span><span class="sxs-lookup"><span data-stu-id="3999e-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="3999e-121">Настройка [локальной](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) среды разработки для SharePoint надстройок для руководства по локальной настройке (включая отключение проверки циклов при необходимости).</span><span class="sxs-lookup"><span data-stu-id="3999e-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="3999e-122">Если вы разрабатываете удаленно, см. в SharePoint [приложения для удаленной системы.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)</span><span class="sxs-lookup"><span data-stu-id="3999e-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="3999e-123">Создание SharePoint надстройки и клиентской веб-части</span><span class="sxs-lookup"><span data-stu-id="3999e-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="3999e-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="3999e-124"><a name="CreateApp"> </a></span></span>

1. <span data-ttu-id="3999e-125">Откройте Visual Studio и выберите **файл**  >  **Новый**  >  **Project**.</span><span class="sxs-lookup"><span data-stu-id="3999e-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="3999e-126">В раскрывающемся списке в верхней части диалогового окна **Новый проект** выберите пункт **.NET Framework 4.5**.</span><span class="sxs-lookup"><span data-stu-id="3999e-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="3999e-127">В **списке Шаблоны** выберите **Visual C#** Office/SharePoint надстройки для SharePoint  >    >    >  **2013** г.</span><span class="sxs-lookup"><span data-stu-id="3999e-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="3999e-128">Назови надстройку GetProjectIdAddinPart и выберите **кнопку ОК.**</span><span class="sxs-lookup"><span data-stu-id="3999e-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="3999e-129">В **диалоговом окне "Новая** надстройка для SharePoint" введите URL-адрес веб-PWA, который необходимо использовать для отладки (например: _https://contoso.com/sites/pwasite/_ ).</span><span class="sxs-lookup"><span data-stu-id="3999e-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="3999e-130">Выберите вариант **SharePoint,** где будет организована надстройка, а затем выберите кнопку **Готово.**</span><span class="sxs-lookup"><span data-stu-id="3999e-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="3999e-131">В **обозревателе** решений откройте меню ярлыков для проекта GetProjectIdAddinPart и выберите **Добавить**  >  **новый элемент**.</span><span class="sxs-lookup"><span data-stu-id="3999e-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="3999e-132">В **диалоговом** окне Добавить новый элемент выберите клиентскую веб-часть **(Host Web),** назовите веб-часть GetProjectId и выберите кнопку **Добавить.**</span><span class="sxs-lookup"><span data-stu-id="3999e-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="3999e-133">В **диалоговом окне Создание** клиентской веб-части выберите параметр **Создать** новую страницу веб-части клиента, а затем выберите кнопку **Готово.**</span><span class="sxs-lookup"><span data-stu-id="3999e-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="3999e-134">Получить ID проекта в части надстройки</span><span class="sxs-lookup"><span data-stu-id="3999e-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="3999e-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="3999e-135"><a name="GetProjectId"> </a></span></span>

<span data-ttu-id="3999e-136">Часть надстройки GetProjectId определяет свой пользовательский код на странице GetProjectId.aspx клиентской веб-части.</span><span class="sxs-lookup"><span data-stu-id="3999e-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="3999e-137">Логика получения и обработки сообщения определяется  в головном элементе страницы, а элементы  управления страницей определяются в элементе тела страницы.</span><span class="sxs-lookup"><span data-stu-id="3999e-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="3999e-138">Откройте страницу веб-части GetProjectId.aspx (в **папке Pages).**</span><span class="sxs-lookup"><span data-stu-id="3999e-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="3999e-139">В **головном** элементе страницы замените код между **тегами** скрипта следующим кодом.</span><span class="sxs-lookup"><span data-stu-id="3999e-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="3999e-140">Добавьте следующий код в **элемент тела** страницы.</span><span class="sxs-lookup"><span data-stu-id="3999e-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="3999e-141">Код определяет контроль пролета, отображает код проекта.</span><span class="sxs-lookup"><span data-stu-id="3999e-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="3999e-142">В Elements.xml дополнительно измените имя, название, описание и размер надстройки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3999e-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="3999e-143">В этом примере используются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3999e-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="3999e-144">Чтобы проверить часть надстройки, в панели меню выберите **Отладку**, **Начните отладку.**</span><span class="sxs-lookup"><span data-stu-id="3999e-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="3999e-145">Если вам будет предложено изменить файл web.config, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3999e-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="3999e-146">Чтобы отлавить часть надстройки, установите соответствующие точки перерывов в добавленных скриптах.</span><span class="sxs-lookup"><span data-stu-id="3999e-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="3999e-147">Просмотрите страницу PDP и выберите **страницу Изменить** из меню Tools (значок передач).</span><span class="sxs-lookup"><span data-stu-id="3999e-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="3999e-148">Добавьте часть **GetProjectId Title** в веб-часть на странице.</span><span class="sxs-lookup"><span data-stu-id="3999e-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="3999e-149">ID проекта отображает в области управления **диапазоном** на странице веб-части.</span><span class="sxs-lookup"><span data-stu-id="3999e-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="3999e-150">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="3999e-150">Next steps</span></span>
<span data-ttu-id="3999e-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="3999e-151"><a name="NextSteps"> </a></span></span>

<span data-ttu-id="3999e-152">Часть надстройки в этом примере не имеет доступа к Project серверу или SharePoint данным.</span><span class="sxs-lookup"><span data-stu-id="3999e-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="3999e-153">Вы можете использовать ID продукта для получения сведений о текущем проекте с помощью клиентского API, например объектной модели JavaScript или службы REST.</span><span class="sxs-lookup"><span data-stu-id="3999e-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="3999e-154">В файле AppManifest.xml укажите разрешения, необходимые вашей надстройки для доступа Project или SharePoint данных.</span><span class="sxs-lookup"><span data-stu-id="3999e-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="3999e-155">См. [статью](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) Создание частей надстройки для установки SharePoint надстройки, чтобы узнать, как настроить настраиваемые свойства для надстройки.</span><span class="sxs-lookup"><span data-stu-id="3999e-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="3999e-156">Пример. Получение ID проекта в части надстройки на странице PDP</span><span class="sxs-lookup"><span data-stu-id="3999e-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="3999e-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="3999e-157"><a name="CodeExample"> </a></span></span>

<span data-ttu-id="3999e-158">Ниже приводится полный код на странице GetProjectID.aspx клиентской веб-части.</span><span class="sxs-lookup"><span data-stu-id="3999e-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="3999e-159">Код регистрирует слушателя событий и обработщика событий, который получает и обрабатывает сообщение, содержаное код проекта.</span><span class="sxs-lookup"><span data-stu-id="3999e-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="3999e-160">См. также</span><span class="sxs-lookup"><span data-stu-id="3999e-160">See also</span></span>

- [<span data-ttu-id="3999e-161">Задачи программирования Project</span><span class="sxs-lookup"><span data-stu-id="3999e-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="3999e-162">Создание надстройки Project Server с размещением в SharePoint</span><span class="sxs-lookup"><span data-stu-id="3999e-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="3999e-163">Создание веб-частей надстроек для установки вместе с надстройкой SharePoint</span><span class="sxs-lookup"><span data-stu-id="3999e-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

