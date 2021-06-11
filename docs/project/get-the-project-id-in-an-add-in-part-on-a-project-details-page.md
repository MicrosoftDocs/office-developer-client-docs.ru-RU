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
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Получение ИД проекта в веб-части надстройки на странице сведений о проекте

Части надстройки размещены в **элементах iframe,** полностью изолированных от страницы размещения. Чтобы получить сведения о текущем проекте из части надстройки на странице Project Details Page (PDP), вы можете использовать метод **window.postMessage,** прослушиватель событий и обработщик событий, который разберет ID проекта из сообщения. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Необходимые условия для создания SharePoint надстройки, которая получает ID проекта
<a name="Prereqs"> </a>

Чтобы использовать пример кода в этой статье, вам потребуется один из следующих ниже.
  
- SharePoint 2013 и Project Server 2013, настроенных для изоляции надстройки. Если вы разрабатываете удаленно, сервер должен поддерживать загрузку надстройок, либо необходимо установить надстройку на сайте разработчика.
  
- SharePoint Онлайн и Project Online
    
    - Visual Studio 2013 2012 Visual Studio с Office средствами разработки для Visual Studio 2013 или Napa
        
    - Достаточные разрешения для пользователя, вошедшего в систему:
        
        - Разрешения локального администратора на компьютере разработчика.
            
        - Ознакомьтесь с доступом по крайней мере к одному проекту.
            
        - Разрешение на редактирование страниц на Project Web App сайте.
            
        - Необходимо войти в систему как кто-то отличную от учетной записи системы. Учетная запись системы не имеет разрешения на установку надстройки.
    
Дополнительные сведения о надстройки для [Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) см. в Project. Настройка [локальной](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) среды разработки для SharePoint надстройок для руководства по локальной настройке (включая отключение проверки циклов при необходимости). Если вы разрабатываете удаленно, см. в SharePoint [приложения для удаленной системы.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Создание SharePoint надстройки и клиентской веб-части
<a name="CreateApp"> </a>

1. Откройте Visual Studio и выберите **файл**  >  **Новый**  >  **Project**.
    
2. В раскрывающемся списке в верхней части диалогового окна **Новый проект** выберите пункт **.NET Framework 4.5**. 
    
3. В **списке Шаблоны** выберите **Visual C#** Office/SharePoint надстройки для SharePoint  >    >    >  **2013** г.
    
4. Назови надстройку GetProjectIdAddinPart и выберите **кнопку ОК.** 
    
5. В **диалоговом окне "Новая** надстройка для SharePoint" введите URL-адрес веб-PWA, который необходимо использовать для отладки (например: _https://contoso.com/sites/pwasite/_ ).
    
6. Выберите вариант **SharePoint,** где будет организована надстройка, а затем выберите кнопку **Готово.** 
    
7. В **обозревателе** решений откройте меню ярлыков для проекта GetProjectIdAddinPart и выберите **Добавить**  >  **новый элемент**.
    
8. В **диалоговом** окне Добавить новый элемент выберите клиентскую веб-часть **(Host Web),** назовите веб-часть GetProjectId и выберите кнопку **Добавить.** 
    
9. В **диалоговом окне Создание** клиентской веб-части выберите параметр **Создать** новую страницу веб-части клиента, а затем выберите кнопку **Готово.** 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Получить ID проекта в части надстройки
<a name="GetProjectId"> </a>

Часть надстройки GetProjectId определяет свой пользовательский код на странице GetProjectId.aspx клиентской веб-части. Логика получения и обработки сообщения определяется  в головном элементе страницы, а элементы  управления страницей определяются в элементе тела страницы. 
  
1. Откройте страницу веб-части GetProjectId.aspx (в **папке Pages).** 
    
2. В **головном** элементе страницы замените код между **тегами** скрипта следующим кодом. 
    
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

3. Добавьте следующий код в **элемент тела** страницы. Код определяет контроль пролета, отображает код проекта. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. В Elements.xml дополнительно измените имя, название, описание и размер надстройки по умолчанию. В этом примере используются значения по умолчанию.
    
5. Чтобы проверить часть надстройки, в панели меню выберите **Отладку**, **Начните отладку.** Если вам будет предложено изменить файл web.config, нажмите кнопку **ОК**. 
    
   Чтобы отлавить часть надстройки, установите соответствующие точки перерывов в добавленных скриптах.
    
6. Просмотрите страницу PDP и выберите **страницу Изменить** из меню Tools (значок передач). 
    
7. Добавьте часть **GetProjectId Title** в веб-часть на странице. ID проекта отображает в области управления **диапазоном** на странице веб-части. 
    
## <a name="next-steps"></a>Дальнейшие действия
<a name="NextSteps"> </a>

Часть надстройки в этом примере не имеет доступа к Project серверу или SharePoint данным. Вы можете использовать ID продукта для получения сведений о текущем проекте с помощью клиентского API, например объектной модели JavaScript или службы REST.
  
В файле AppManifest.xml укажите разрешения, необходимые вашей надстройки для доступа Project или SharePoint данных. 
  
См. [статью](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) Создание частей надстройки для установки SharePoint надстройки, чтобы узнать, как настроить настраиваемые свойства для надстройки. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Пример. Получение ID проекта в части надстройки на странице PDP
<a name="CodeExample"> </a>

Ниже приводится полный код на странице GetProjectID.aspx клиентской веб-части. Код регистрирует слушателя событий и обработщика событий, который получает и обрабатывает сообщение, содержаное код проекта.
  
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

## <a name="see-also"></a>См. также

- [Задачи программирования Project](project-programming-tasks.md)
- [Создание надстройки Project Server с размещением в SharePoint](create-a-sharepoint-hosted-project-server-add-in.md)
- [Создание веб-частей надстроек для установки вместе с надстройкой SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

