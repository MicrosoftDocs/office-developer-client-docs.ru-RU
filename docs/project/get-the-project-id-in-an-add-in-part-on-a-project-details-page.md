---
title: Получение ИД проекта в веб-части надстройки на странице сведений о проекте
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: Веб-части надстройки размещаются в элементах IFRAME, которые полностью изолированы от страницы размещения. Для получения сведений о текущем проекте из веб-части надстройки на странице сведений о проекте (PDP) можно использовать метод Window. i, прослушиватель события и обработчик событий, который анализирует идентификатор проекта из сообщения.
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322598"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="d2cfb-104">Получение ИД проекта в веб-части надстройки на странице сведений о проекте</span><span class="sxs-lookup"><span data-stu-id="d2cfb-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="d2cfb-105">Веб-части надстройки размещаются в элементах **IFRAME** , которые полностью изолированы от страницы размещения.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="d2cfb-106">Для получения сведений о текущем проекте из веб-части надстройки на странице сведений о проекте (PDP) можно использовать метод **Window.** i, прослушиватель события и обработчик событий, который анализирует идентификатор проекта из сообщения.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="d2cfb-107">Необходимые условия для создания веб компонента надстройки, размещаемой в SharePoint, который получает идентификатор проекта</span><span class="sxs-lookup"><span data-stu-id="d2cfb-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="d2cfb-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="d2cfb-108"><a name="Prereqs"> </a></span></span>

<span data-ttu-id="d2cfb-109">Чтобы использовать пример кода, описанный в этой статье, вам потребуется один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="d2cfb-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="d2cfb-110">SharePoint 2013 и Project Server 2013, настроенные для изоляции надстроек.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="d2cfb-111">Если вы разрабатываете удаленно, сервер должен поддерживать загрузку надстроек или необходимо установить надстройку на сайте разработчика.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="d2cfb-112">SharePoint Online и Project Online</span><span class="sxs-lookup"><span data-stu-id="d2cfb-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="d2cfb-113">Visual Studio 2013, Visual Studio 2012 с инструментами разработчика Office для Visual Studio 2013 или Napa</span><span class="sxs-lookup"><span data-stu-id="d2cfb-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="d2cfb-114">Достаточные разрешения для пользователя, вошедшего в систему:</span><span class="sxs-lookup"><span data-stu-id="d2cfb-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="d2cfb-115">Разрешения локального администратора на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="d2cfb-116">Доступ для чтения по крайней мере к одному проекту.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="d2cfb-117">Разрешение на изменение страниц на сайте Project Web App.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="d2cfb-118">Необходимо войти в систему как кто-то отличную от учетной записи системы.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="d2cfb-119">Системная учетная запись не имеет разрешений на установку надстройки.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="d2cfb-120">В этой статье приведены [необходимые условия для создания надстройки для Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) для получения дополнительных сведений о надстройках для Project.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="d2cfb-121">Ознакомьтесь с разделом [Настройка локальной среды разработки для надстроек SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) для получения рекомендаций по локальной установке (включая отключение проверки замыкания на себя при необходимости).</span><span class="sxs-lookup"><span data-stu-id="d2cfb-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="d2cfb-122">Если вы разрабатываете удаленно, ознакомьтесь со статьей [Разработка приложений для SharePoint в удаленной системе](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span><span class="sxs-lookup"><span data-stu-id="d2cfb-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="d2cfb-123">Создание надстройки, размещаемой в SharePoint, и клиентской веб-части</span><span class="sxs-lookup"><span data-stu-id="d2cfb-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="d2cfb-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="d2cfb-124"><a name="CreateApp"> </a></span></span>

1. <span data-ttu-id="d2cfb-125">Откройте Visual Studio и выберите **файл** > **создать** > **проект**.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="d2cfb-126">В раскрывающемся списке в верхней части диалогового окна **Новый проект** выберите пункт **.NET Framework 4.5**.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="d2cfb-127">В списке **шаблоны** выберите надстройка **Visual C#** > для**Office и** > **надстройки** > SharePoint**для SharePoint 2013**.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="d2cfb-128">Назовите надстройку Жетпрожектидаддинпарт, а затем нажмите кнопку **ОК** .</span><span class="sxs-lookup"><span data-stu-id="d2cfb-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="d2cfb-129">В диалоговом окне **Создание надстройки для SharePoint** введите URL-адрес сайта PWA, который вы хотите использовать для отладки (например: _https://contoso.com/sites/pwasite/_).</span><span class="sxs-lookup"><span data-stu-id="d2cfb-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="d2cfb-130">Выберите параметр, **размещаемый в SharePoint** , чтобы разместить надстройку, а затем нажмите кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="d2cfb-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="d2cfb-131">В **обозревателе решений**откройте контекстное меню для проекта жетпрожектидаддинпарт и выберите команду **Добавить** > **новый элемент**.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="d2cfb-132">В диалоговом окне **Добавление нового элемента** выберите **Клиентская веб-часть (хост-сайт)**, назовите веб-часть жетпрожектид, а затем нажмите кнопку **добавить** .</span><span class="sxs-lookup"><span data-stu-id="d2cfb-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="d2cfb-133">В диалоговом окне **Создание клиентской веб-части** выберите параметр **создать новую страницу клиентской веб-части** , а затем нажмите кнопку **Готово** .</span><span class="sxs-lookup"><span data-stu-id="d2cfb-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="d2cfb-134">Получение идентификатора проекта в веб — части надстройки</span><span class="sxs-lookup"><span data-stu-id="d2cfb-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="d2cfb-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="d2cfb-135"><a name="GetProjectId"> </a></span></span>

<span data-ttu-id="d2cfb-136">Веб-часть надстройки Жетпрожектид определяет свой собственный код на странице Жетпрожектид. aspx клиентской веб-части.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="d2cfb-137">Логика, которая получает и обрабатывает сообщение, определяется в элементе **head** страницы, а элементы управления страницы определяются в элементе **Body** страницы.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="d2cfb-138">Откройте страницу веб-части Жетпрожектид. aspx (в папке **страницы** ).</span><span class="sxs-lookup"><span data-stu-id="d2cfb-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="d2cfb-139">В элементе **head** страницы замените код между тегами **script** следующим кодом.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="d2cfb-140">Добавьте следующий код в элемент **Body** страницы.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="d2cfb-141">Код определяет элемент управления span, который отображает идентификатор проекта.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="d2cfb-142">В файле Elements. XML при необходимости измените имя, название, описание и размер веб-части надстройки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="d2cfb-143">В этом примере используются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="d2cfb-144">Чтобы протестировать веб-часть надстройки, в строке меню последовательно выберите пункты **Отладка**и **начать отладку**.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="d2cfb-145">Если вам будет предложено изменить файл web.config, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="d2cfb-146">Чтобы выполнить отладку веб компонента надстройки, установите соответствующие точки останова в добавленном скрипте.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="d2cfb-147">Перейдите на страницу PDP и выберите команду **Изменить страницу** в меню Сервис (значок шестеренки).</span><span class="sxs-lookup"><span data-stu-id="d2cfb-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="d2cfb-148">Добавьте часть " **название жетпрожектид** " в веб-часть на странице.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="d2cfb-149">ИДЕНТИФИКАТОР проекта отображается в элементе управления **span** на странице веб-частей.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="d2cfb-150">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="d2cfb-150">Next steps</span></span>
<span data-ttu-id="d2cfb-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="d2cfb-151"><a name="NextSteps"> </a></span></span>

<span data-ttu-id="d2cfb-152">В этом примере часть надстройки не получает доступ к данным Project Server или SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="d2cfb-153">Вы можете использовать идентификатор продукта для получения сведений о текущем проекте с помощью клиентского API, например объектной модели JavaScript или службы REST.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="d2cfb-154">В файле AppManifest. xml укажите разрешения, необходимые надстройке для доступа к данным Project Server или SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="d2cfb-155">Ознакомьтесь [с разустановочными разделами, чтобы установить](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) надстройку для SharePoint, чтобы узнать, как задать настраиваемые свойства веб компонента надстройки.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="d2cfb-156">Пример: извлечение идентификатора проекта в веб-части надстройки на странице PDP</span><span class="sxs-lookup"><span data-stu-id="d2cfb-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="d2cfb-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="d2cfb-157"><a name="CodeExample"> </a></span></span>

<span data-ttu-id="d2cfb-158">В приведенном ниже примере показан полный код на странице Жетпрожектид. aspx клиентской веб-части.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="d2cfb-159">Код регистрирует прослушиватель событий и обработчик событий, который получает и анализирует сообщение, содержащее идентификатор проекта.</span><span class="sxs-lookup"><span data-stu-id="d2cfb-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="d2cfb-160">См. также</span><span class="sxs-lookup"><span data-stu-id="d2cfb-160">See also</span></span>

- [<span data-ttu-id="d2cfb-161">Задачи программирования Project</span><span class="sxs-lookup"><span data-stu-id="d2cfb-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="d2cfb-162">Создание надстройки Project Server с размещением в SharePoint</span><span class="sxs-lookup"><span data-stu-id="d2cfb-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="d2cfb-163">Создание веб-частей надстроек для установки вместе с надстройкой SharePoint</span><span class="sxs-lookup"><span data-stu-id="d2cfb-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

