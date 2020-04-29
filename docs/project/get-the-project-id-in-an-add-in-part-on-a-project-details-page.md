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
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>Получение ИД проекта в веб-части надстройки на странице сведений о проекте

Веб-части надстройки размещаются в элементах **IFRAME** , которые полностью изолированы от страницы размещения. Для получения сведений о текущем проекте из веб-части надстройки на странице сведений о проекте (PDP) можно использовать метод **Window.** i, прослушиватель события и обработчик событий, который анализирует идентификатор проекта из сообщения. 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>Необходимые условия для создания веб компонента надстройки, размещаемой в SharePoint, который получает идентификатор проекта
<a name="Prereqs"> </a>

Чтобы использовать пример кода, описанный в этой статье, вам потребуется один из следующих вариантов:
  
- SharePoint 2013 и Project Server 2013, настроенные для изоляции надстроек. Если вы разрабатываете удаленно, сервер должен поддерживать загрузку надстроек или необходимо установить надстройку на сайте разработчика.
  
- SharePoint Online и Project Online
    
    - Visual Studio 2013, Visual Studio 2012 с инструментами разработчика Office для Visual Studio 2013 или Napa
        
    - Достаточные разрешения для пользователя, вошедшего в систему:
        
        - Разрешения локального администратора на компьютере разработчика.
            
        - Доступ для чтения по крайней мере к одному проекту.
            
        - Разрешение на изменение страниц на сайте Project Web App.
            
        - Необходимо войти в систему как кто-то отличную от учетной записи системы. Системная учетная запись не имеет разрешений на установку надстройки.
    
В этой статье приведены [необходимые условия для создания надстройки для Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) для получения дополнительных сведений о надстройках для Project. Ознакомьтесь с разделом [Настройка локальной среды разработки для надстроек SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) для получения рекомендаций по локальной установке (включая отключение проверки замыкания на себя при необходимости). Если вы разрабатываете удаленно, ознакомьтесь со статьей [Разработка приложений для SharePoint в удаленной системе](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>Создание надстройки, размещаемой в SharePoint, и клиентской веб-части
<a name="CreateApp"> </a>

1. Откройте Visual Studio и выберите **файл** > **создать** > **проект**.
    
2. В раскрывающемся списке в верхней части диалогового окна **Новый проект** выберите пункт **.NET Framework 4.5**. 
    
3. В списке **шаблоны** выберите надстройка **Visual C#** > для**Office и** > **надстройки** > SharePoint**для SharePoint 2013**.
    
4. Назовите надстройку Жетпрожектидаддинпарт, а затем нажмите кнопку **ОК** . 
    
5. В диалоговом окне **Создание надстройки для SharePoint** введите URL-адрес сайта PWA, который вы хотите использовать для отладки (например: _https://contoso.com/sites/pwasite/_).
    
6. Выберите параметр, **размещаемый в SharePoint** , чтобы разместить надстройку, а затем нажмите кнопку **Готово** . 
    
7. В **обозревателе решений**откройте контекстное меню для проекта жетпрожектидаддинпарт и выберите команду **Добавить** > **новый элемент**.
    
8. В диалоговом окне **Добавление нового элемента** выберите **Клиентская веб-часть (хост-сайт)**, назовите веб-часть жетпрожектид, а затем нажмите кнопку **добавить** . 
    
9. В диалоговом окне **Создание клиентской веб-части** выберите параметр **создать новую страницу клиентской веб-части** , а затем нажмите кнопку **Готово** . 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>Получение идентификатора проекта в веб — части надстройки
<a name="GetProjectId"> </a>

Веб-часть надстройки Жетпрожектид определяет свой собственный код на странице Жетпрожектид. aspx клиентской веб-части. Логика, которая получает и обрабатывает сообщение, определяется в элементе **head** страницы, а элементы управления страницы определяются в элементе **Body** страницы. 
  
1. Откройте страницу веб-части Жетпрожектид. aspx (в папке **страницы** ). 
    
2. В элементе **head** страницы замените код между тегами **script** следующим кодом. 
    
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

3. Добавьте следующий код в элемент **Body** страницы. Код определяет элемент управления span, который отображает идентификатор проекта. 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. В файле Elements. XML при необходимости измените имя, название, описание и размер веб-части надстройки по умолчанию. В этом примере используются значения по умолчанию.
    
5. Чтобы протестировать веб-часть надстройки, в строке меню последовательно выберите пункты **Отладка**и **начать отладку**. Если вам будет предложено изменить файл web.config, нажмите кнопку **ОК**. 
    
   Чтобы выполнить отладку веб компонента надстройки, установите соответствующие точки останова в добавленном скрипте.
    
6. Перейдите на страницу PDP и выберите команду **Изменить страницу** в меню Сервис (значок шестеренки). 
    
7. Добавьте часть " **название жетпрожектид** " в веб-часть на странице. ИДЕНТИФИКАТОР проекта отображается в элементе управления **span** на странице веб-частей. 
    
## <a name="next-steps"></a>Дальнейшие действия
<a name="NextSteps"> </a>

В этом примере часть надстройки не получает доступ к данным Project Server или SharePoint. Вы можете использовать идентификатор продукта для получения сведений о текущем проекте с помощью клиентского API, например объектной модели JavaScript или службы REST.
  
В файле AppManifest. xml укажите разрешения, необходимые надстройке для доступа к данным Project Server или SharePoint. 
  
Ознакомьтесь [с разустановочными разделами, чтобы установить](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) надстройку для SharePoint, чтобы узнать, как задать настраиваемые свойства веб компонента надстройки. 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>Пример: извлечение идентификатора проекта в веб-части надстройки на странице PDP
<a name="CodeExample"> </a>

В приведенном ниже примере показан полный код на странице Жетпрожектид. aspx клиентской веб-части. Код регистрирует прослушиватель событий и обработчик событий, который получает и анализирует сообщение, содержащее идентификатор проекта.
  
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
    

