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
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Получение ИД проекта в веб-части надстройки на странице сведений о проекте

Добавьте в части размещаются в **iframe** элементы, которые являются полностью изолирована от внешнего размещения страницы. Для получения сведений о текущем проекте из части надстройки на страницу сведений о Project (PDP), можно использовать метод **window.postMessage** , прослушиватель событий и обработчик событий, который разбор код проекта из сообщения. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Необходимые условия для создания размещенных в SharePoint надстройки часть, которая получает идентификатор проекта
<a name="Prereqs"> </a>

Для использования в примере кода в этой статье, необходимо следующее:
  
- SharePoint 2013 и Project Server 2013, настроенных для изоляции надстройки. При разработке удаленно, сервер должен поддерживать sideloading надстроек или необходимо установить надстройку на сайте разработчика.
  
- SharePoint Online и Project Online
    
    - Средства Visual Studio 2012 с Office для разработчиков Visual Studio 2013 для Visual Studio 2013 или Napa
        
    - Достаточные разрешения для пользователя, вошедшего в систему:
        
        - Разрешения локального администратора на компьютере разработчика.
            
        - Доступ на чтение по крайней мере один проект.
            
        - Разрешение на изменение страниц на сайт Project Web App.
            
        - Необходимо войти в систему как кто-то отличную от учетной записи системы. Системную учетную запись не имеет разрешения, чтобы установить надстройку.
    
[Необходимые условия для создания надстройки уровня приложения для Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) более подробные сведения о надстройках для проекта. В разделе [Настройка локальной среды разработки для SharePoint надстройки](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) рекомендации для локальной установки (включая отключение проверки замыкания на себя при необходимости). При разработке удаленно, видеть [Разработка приложений для SharePoint в удаленной системе](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Создание размещенных в SharePoint и надстройка клиентского веб-части
<a name="CreateApp"> </a>

1. Откройте Visual Studio и выберите **файл** > **New** > **проекта**.
    
2. В диалоговом окне **Новый проект** выберите **.NET Framework 4.5** из раскрывающегося списка в верхней части окна. 
    
3. В списке **шаблонов** выберите **Visual C#** > **Office/SharePoint** > **надстройки** > **Add-in SharePoint 2013**.
    
4. Назовите GetProjectIdAddinPart надстройки и затем нажмите кнопку **ОК** . 
    
5. В диалоговом окне **новой надстройки для SharePoint** введите URL-адрес сайта Project Web Access, который требуется использовать для отладки (например: _https://contoso.com/sites/pwasite/_).
    
6. Выберите вариант **Размещение в SharePoint** для размещения надстройки и затем нажмите кнопку **Готово** . 
    
7. В **Обозревателе решений**откройте контекстное меню для проекта GetProjectIdAddinPart и нажмите кнопку **Добавить** > **Новый элемент**.
    
8. В диалоговом окне **Добавление нового элемента** выберите **клиентская веб-часть (хост-сайта)**, имя веб-части GetProjectId и затем нажмите кнопку **Добавить** . 
    
9. В диалоговом окне **Создание клиентов веб-части** выберите параметр **Создать новый клиент страницу веб-частей** и затем нажмите кнопку **Готово** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Получите код проекта в части "надстройки"
<a name="GetProjectId"> </a>

В GetProjectId часть определяет его пользовательский код на странице GetProjectId.aspx веб-части клиента. Определенные логику, которая получает и обрабатывает сообщение в элемент **head** страницы и элементы управления страницы определены в элемент **body** страницы. 
  
1. Откройте меню GetProjectId.aspx веб-части (в папке **страниц** ). 
    
2. В элемент **head** страницы замените код в тегах **сценария** приведенный ниже код. 
    
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

3. Добавьте следующий код в элемент **body** страницы. Код определяет элемент управления текст, который отображает идентификатор проекта. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. В файле Elements.xml при необходимости измените имя, заголовок, описание и по умолчанию размер части надстройки. В этом примере имеют значения по умолчанию.
    
5. Чтобы протестировать часть надстройка, в строке меню выберите **Отладка**, **Начать отладку**. Если появится запрос на изменение файла web.config, нажмите кнопку **ОК** . 
    
   Отладка части надстройки, установите соответствующие точки останова в скрипте, который вы добавили.
    
6. Перейдите на страницу страница сведений о Проекте и выберите команду **Изменить страницу** из меню "Сервис" (значок шестеренки). 
    
7. Добавьте часть **GetProjectId заголовок** веб-части на странице. КОД проекта отображается в элементе управления **охватывать** на странице веб-частей. 
    
## <a name="next-steps"></a>Дальнейшие действия
<a name="NextSteps"> </a>

Часть надстройка в этом примере не получить доступ к данными Project Server или данных SharePoint. КОД продукта можно использовать для получения сведений о текущем проекте с помощью клиентского интерфейса API, например объектной модели JavaScript или службы REST.
  
В файле AppManifest.xml укажите разрешения, которые надстройка требуется доступ к Project Server данных или данных SharePoint. 
  
В разделе [Создание надстройки частей для установки с помощью надстройки SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) в этой статье описывается установка настраиваемых свойств для части надстройки. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Пример: Начало код проекта в части надстройки на странице страница сведений о Проекте
<a name="CodeExample"> </a>

Следующий пример является полный код на страницу веб-часть клиента GetProjectID.aspx. Этот код регистрирует прослушиватель событий и обработчик событий, который получает и анализирует сообщение, содержащее идентификатор проекта.
  
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
- [Создание веб-частей надстройки для установки совместно с надстройкой SharePoint](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

