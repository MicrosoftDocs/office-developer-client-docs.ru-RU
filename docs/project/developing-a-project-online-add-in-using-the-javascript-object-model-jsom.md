---
title: Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: В этой статье описывается Microsoft Project Online надстройки для улучшения работы с Project Online. Проект разработки реализуется в качестве погона. Надстройка, используемая для этой статьи, считывает и отображает имена и ИД опубликованных проектов из вашей учетной записи Project Online и позволяет сверлить для получения задач, связанных с отдельными проектами.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322694"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)

В этой статье Microsoft Project Online разработки надстройки для улучшения работы с Project Online. Проект разработки реализуется в качестве погона. Надстройка, используемая для этой статьи, считывает и отображает имена и ИД опубликованных проектов из вашей учетной записи Project Online и позволяет сверлить для получения задач, связанных с отдельными проектами.
  
При запуске список надстройки выглядит примерно так же, как на следующей иллюстрации:
  
![Снимок экрана, показывающий перечисление проектов и задач JSOM]Screen shot с перечислением(media/766e5914-f048-48f4-9282-291f55e6e90d.png "проектов и задач JSOM")
  
В этом примере основное внимание уделяется взаимодействию с Project Online, запросам и настройке контекста для каждого запроса из службы. Элементы пользовательского интерфейса (пользовательского интерфейса) получают минимальное внимание. Вместо этого исходные списки предоставляют комментарии относительно пользовательского интерфейса.
  
> [!NOTE]
> Исходные файлы для примера надстройки, проекта Visual Studio, доступны по: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... . Держите исходные файлы удобными в качестве ссылки во время чтения статьи, так как каждый из них дополняет другой. Файлы в Visual Studio и исполняются с минимальными изменениями, заменив URL-адрес Project Online клиента в папку PWA. 
  
## <a name="background"></a>Общие сведения

Project Online — это служба Office 365, которая предоставляет компаниям решение для управления портфелями проектов (система УПП) и управления проектами (PMO) для координации и управления портфелями, программами и проектами. Project Online это другое предложение, чем Project настольные выпуски; однако Project Online по-прежнему содержит функции по обслуживанию и отслеживанию сведений о проекте на протяжении всего жизненного пути проекта. Project Online построена на SharePoint Online.
  
Надстройка Project Online состоит из файлов JavaScript и ресурсов, взаимодействующих с API Client-Side-Object-Model. Когда пользователь посещает надстройки, JavaScript и ресурсы загружаются и выполняются в браузере. Надстройка делает асинхронные вызовы для Project Online для взаимодействия со службой, будь то создание, ирисовка, обновление или удаление данных. 
  
Project Online выполняет еще одно действие для защиты от надстройки сведений, принадлежащих другим арендаторам; а именно, Project Online создает изолированный сайт для взаимодействия с запросами из надстройки. Пользовательский код не запускается на Project Online хост. 
  
Настройка разработки для Project Online надстройки использует тип Visual Studio SharePoint надстройки. Надстройка написана в JavaScript и использует объектную модель Project JavaScript (JSOM) для взаимодействия с Project Online службой. JSOM наследует большую часть своих функций от SharePoint JSOM.
  
> [!NOTE]
> Надстройки можно публиковать и продавать в Office Store или развертывать в частном каталоге приложений в SharePoint. Дополнительные сведения см. в [публикации Развертывания и публикации Office надстройки.](https://docs.microsoft.com/office/dev/add-ins/publish/publish)
> 
> Надстройка, используемая в этой статье, является образцом для разработчиков; она не предназначена для использования в производственной среде. Основная цель — показать пример разработки приложений для Project Online. 
  
## <a name="prerequisites"></a>Предварительные требования

Добавление следующих элементов в поддерживаемую Windows среду:
  
- **платформа .NET Framework 4.0 или** более поздней версии: совместимы полные версии фреймворка из версии 4.0. Сайт загрузки файлов — https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 или позже:**  
    
   - Профессиональное издание Visual Studio 2015 г. готово к выходу из окна и доступно на https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx сайте .
    
   - В сообществе выпуск Visual Studio 2015 доступен по https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx номеру . В этом выпуске требуется ручная установка Microsoft Office средств разработки для Visual Studio.
    
   Средства Microsoft Office для Visual Studio доступны по https://www.visualstudio.com/en-us/features/office-tools-vs.aspx .
    
- **Учетная Project Online.** Это обеспечивает доступ к службе размещения. Дополнительные сведения о получении учетной записи Project Online см. здесь: https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Убедитесь, что пользователь надстройки имеет достаточное разрешение для доступа к некоторым проектам Project Online клиента. 
    
- **Проекты на сайте размещения,** которые заполнены информацией.
    
> [!NOTE]
> Стандартным платформа .NET Framework является правильная используемая структура. Не используйте "профиль платформа .NET Framework 4". 
  
### <a name="set-up-the-visual-studio-project"></a>Настройка проекта Visual Studio

Настройка приложения состоит из создания нового проекта, связывания соответствующих библиотек и объявления необходимых пространств имен. Visual Studio поддерживает нескольких типов проектов разработки. Раздел краткий и очень простой. Значение состоит в том, что сведения совмеся в одном месте.
  
#### <a name="select-a-visual-studio-project"></a>Выберите проект Visual Studio

Чтобы создать проект соответствующего типа для надстройки, необходимо сделать следующие действия. Ключевые слова, которые встречаются на экране, имеют **смелый атрибут:** 
  
1. В меню File выберите **файл**  >  **Project.**  >   
    
2. Из установленных шаблонов в левой области выберите C#  >  **Office/SharePoint**  >  **веб-надстройки**. 
    
3. В верхней части центральной области выберите платформа .NET Framework **4** или более поздней части; текущая версия 4.6. 
    
4. Из типов приложений на центральной области выберите SharePoint **надстройку.** 
    
5. В нижней части укажите имя и расположение проекта, а также имя решения. 
    
6. Кроме того, в нижней части установите флажок **Создать каталог для решения**. 
    
7. Нажмите кнопку **ОК**, чтобы создать начальный проект. 
    
Мастер Visual Studio задает несколько последующих вопросов о сайте параметров Project Online (называемый SharePoint параметров в диалоговом окрашиваемом диалоге) в нескольких последующих диалогов. Вот вопросы:
  
1. Какие SharePoint вы хотите использовать для отладки надстройки? Укажите URL-адрес PWA сайта, например https://contoso.sharepoint.com/sites/pwa .
    
2. Как вы хотите провести SharePoint надстройки? Выберите [X] **SharePoint-хостинга**.
    
   Дополнительные сведения о SharePoint надстройки, включая варианты размещения, см. в SharePoint [надстройки.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)
    
3. Нажмите **Далее**. 
    
Во втором дополнительном диалоговом окрашиваемом диалоговом окрашиваемой версии SharePoint Online для надстройки: 
  
1. Что является ранней версией SharePoint, которую необходимо нацелить на надстройки? Выберите [X] S **harePoint-Online**. 
    
2. Нажмите кнопку **Готово**. 
    
Visual Studio создает проект и имеет доступ к Project Online сайту. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Включить побную загрузку на Project Online сайте

Sideloading — это механизм тестирования и отладки Project Online надстроек. Для боковой загрузки требуется два сценария: один для обеспечения боковой загрузки Project Online сайта, а другой для отключения боковой загрузки после завершения тестирования и отладки надстройки.
  
Дополнительные сведения о настройке боковой загрузки см. в приложении [Enable SideLoading в коллекции сайтов,](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)не относяющихся к разработчику.
  
> [!NOTE]
> Sideloading apps is a developer/test feature. Он не **предназначен для использования в производстве.** Не перегружайте приложения регулярно или не делайте загрузку приложения включенной дольше, чем вы активно используете эту функцию. 
  
## <a name="add-content-to-the-add-in-project"></a>Добавление контента в проект надстройки

После создания проекта и настройки механизма отладки добавление контента в приложение включает следующие задачи:
  
- Настройка области приложения
    
- Связь библиотеки JSOM
    
- Добавление элементов пользовательского интерфейса в надстройку
    
- Инициализация и подключение к Project Online службе
    
- Ирисовка проектов и сведений/свойств
    
- Отображение проектов
    
- Отображение задач для Project
    
Проект надстройки состоит из множества файлов. В этом примере необходимо изменить следующие файлы: 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.css — необязательный; содержит определения стилей, разработанные для надстройки
    
Если клиент Project Online, например переход с пробной версии на сайт подписки, можно обновить свойства проекта, включая подключение к серверу и URL-адрес сайта, используя окно свойств, доступное через команду **Окно** свойств  >   просмотра. 
  
Вы также можете добавить файлы в проект. Если это так, вам потребуется обновить файл Elements.xml, расположенный в одной группе (контент, изображения, страницы или скрипты), чтобы включить новые файлы. Дополнительные сведения о файлах проекта см. в дополнительных сведениях о структуре манифеста приложения и пакете [SharePoint надстройки.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)
  
### <a name="set-application-scope"></a>Настройка области приложения

Область потребностей надстройки или уровни разрешений, определенные перед возвращением службой сведений в результатах запроса. Для этой надстройки используйте следующую область для Visual Studio проекта. Это изменение в файле AppManifest.xml на вкладке Permissions:

|Область|Разрешение|
|:-----|:-----|
|Несколько проектов (Project Server)  <br/> |Чтение  <br/> |
   
Сохраните файл после настройки области приложения. В противном случае данные из службы не возвращаются. 
  
### <a name="link-the-jsom-library"></a>Ссылка библиотеки JSOM

Библиотеки Project Online, PS.js и PS.debug.js, предоставлены Project Online и всегда являются последней версией. Надстройки JavaScript, которые используют JSOM, должны связываться с одной из этих библиотек. Определения ссылок добавляются в файл Default.aspx. Команды по использованию PS.js или PS.debug.js являются частью кода, расположенного в App.js файле.
  
Добавьте следующую команду для определения PS.js или PS.debug.js в элементе, следующего за `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` "SharePoint:ScriptLink" для sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Атрибут **OnDemand** для PS.js или PS.debug.js для false **.** 
  
### <a name="add-ui-elements-to-the-add-in"></a>Добавление элементов пользовательского интерфейса в надстройку

Пример надстройки состоит из нескольких компонентов. Статические описания элементов находятся в файле Default.aspx. Динамические описания элементов и код для всех компонентов находятся в App.js файле. Для комментариев по компонентам обратитесь к спискам исходных кодов. Вот список компонентов пользовательского интерфейса в надстройки:
  
- Название
    
- Вводная глагольная фраза
    
- Кнопка для удаления задач из таблицы
    
- Таблица, в которую перечислены ИД проекта и имя, а также сведения о задачах.
    
- Кнопка Tasks (клонированная один раз для каждого проекта), которая импортирует данные задач в таблицу.
    
Подробные сведения об пользовательском интерфейсе, например заголовок и заголовок таблицы проектов, см. в файле проекта Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Инициализация и подключение к хост-системе

Файл App.js содержит код JavaScript. Надстройка загружается PS.js браузере, а затем вызывает функцию initializePage. InitializePage извлекает контекст в конечную точку Project Online и запускает функцию loadProjects.
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a>Извлечение проектов

Функция loadProjects запрашивает службу для имен и ИД проекта. 
  
Приложение извлекает имя проекта и id проекта. Другие сведения о проекте доступны, к ним можно получить доступ, изменяя метод нагрузки, чтобы точно определить свойства, которые нужно получить. В коде в качестве комментария представлен пример. 
  
Если запрос удался, надстройка продолжит вызывать displayProjects. 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a>Отображение проектов

Функция displayProjects создает таблицу, одну строку для каждого проекта и кнопку для отображения задач для конкретного проекта. 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> В то время как цикл имеет доступ к свойствам ID и имен. Это немного отличается от проекта исходных кодов, который вызывает функцию, которая, в свою очередь, имеет доступ к тем же свойствам. 
  
### <a name="display-the-tasks-for-a-project"></a>Отображение задач для проекта

Задачи, хотя и являются частью надстройки, не являются частью начальной загрузки. Если пользователь заинтересован в задачах, связанных с проектом, нажатие кнопки "Показать задачи" вызывает отображение задач в списке с помощью обработанта событий btnLoadTasks. 
  
Обработник событий btnLoadTasks с соответствующим ИД проекта запрашивает задачи для указанного проекта с сервера. После получения btnLoadTasks передает список задач для отображенияTasks, чтобы представить задачи на экране.
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

Функция displayTasks отображает задачи, связанные с указанным проектом, непосредственно под записью проекта.
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> В то время как цикл имеет доступ к ID задачи и свойствам имен. Это немного отличается от проекта исходных кодов, который вызывает функцию, которая, в свою очередь, имеет доступ к тем же свойствам. 
  
Пример вывода для задач одного проекта следует.
  
![Снимок экрана, показывающий выход для снимка]экрана задачи проекта,(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "показывающий выход для задачи проекта")
  
## <a name="see-also"></a>Дополнительные ресурсы

Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/en-us/project).
    


