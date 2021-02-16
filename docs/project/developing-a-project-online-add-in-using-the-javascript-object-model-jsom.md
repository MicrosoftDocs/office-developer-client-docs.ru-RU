---
title: Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: В этой статье описывается разработка надстройки Microsoft Project Online для улучшения работы с Project Online. Проект разработки реализован в качестве по walkthrough. Надстройка, используемая для этой статьи, считывает и отображает имена и ИД опубликованных проектов из вашей учетной записи Project Online и позволяет получить дополнительные данные для получения задач, связанных с отдельными проектами.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322694"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)

В этой статье описывается разработка надстройки Microsoft Project Online для улучшения работы с Project Online. Проект разработки реализован в качестве по walkthrough. Надстройка, используемая для этой статьи, считывает и отображает имена и ИД опубликованных проектов из вашей учетной записи Project Online и позволяет получить дополнительные данные для получения задач, связанных с отдельными проектами.
  
Во время запуска описание надстройки выглядит примерно так:
  
![Снимок экрана, на котором показан список проектов и задач JSOM,]на котором показан список(media/766e5914-f048-48f4-9282-291f55e6e90d.png "проектов и задач JSOM")
  
В этом примере основное внимание уделяется взаимодействию с Project Online, запросам и настройке контекста для каждого запроса от службы. Элементы пользовательского интерфейса получают минимальное внимание. Вместо этого исходные листинги предоставляют комментарии относительно пользовательского интерфейса.
  
> [!NOTE]
> Исходные файлы для примера надстройки , Visual Studio проекта, доступны по: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... . При прочтях статьи исходные файлы должны быть под рукой, так как они дополняют друг друга. Файлы в сборке Visual Studio и исполняются с минимальными изменениями— заменяют URL-адрес клиента Project Online на папку PWA. 
  
## <a name="background"></a>Общие сведения

Project Online — это служба Office 365, которая предоставляет компаниям решение по управлению портфелем проектов (PPM) и офису управления проектами (PMO) для координации портфелей, программ и проектов и управления ими. Project Online отличается от классических выпусков Project; Тем не менее, Project Online по-прежнему содержит функции для обслуживания и отслеживания сведений о проекте на протяжении всего жизненного пути проекта. Project Online создан на основе SharePoint Online.
  
Надстройка, в которую находится Project Online, состоит из JavaScript и файлов ресурсов, взаимодействующих с API клиентской объектной модели. Когда пользователь посещает надстройки, JavaScript и ресурсы загружаются и выполняются в браузере. Надстройка совершает асинхронные вызовы Project Online для взаимодействия со службой, будь то создание, искомый, обновляющий или удаляющий данные. 
  
Project Online выполняет еще одно действие для защиты информации, которая принадлежит другим арендаторам, из надстройки; а именно, Project Online создает изолированный сайт для взаимодействия с запросами из надстройки. На хост-сайте Project Online пользовательский код не выполняется. 
  
При настройке разработки надстройки Project Online используется тип Visual Studio надстройки SharePoint. Надстройка написана на JavaScript и использует объектную модель JavaScript (JSOM) Project для взаимодействия со службой Project Online. JSOM наследует большую часть своих функций от JSOM SharePoint.
  
> [!NOTE]
> Надстройки можно публиковать и продавать в Магазине Office или развертывать в частном каталоге приложений в SharePoint. Дополнительные сведения [см. в теме "Развертывание и публикация надстройки Office".](https://docs.microsoft.com/office/dev/add-ins/publish/publish)
> 
> Надстройка, используемая в этой статье, является образцом для разработчиков; Он не предназначен для использования в производственной среде. Основная цель — показать пример разработки приложений для Project Online. 
  
## <a name="prerequisites"></a>Необходимые компоненты

Добавьте следующие элементы в поддерживаемую среду Windows:
  
- **.NET Framework 4.0 или** более поздней версии: полные версии структуры из версии 4.0 совместимы. Сайт загрузки файлов — https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 или более поздней:**  
    
   - Профессиональный выпуск Visual Studio 2015 готов к выпуску и доступен по https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx
    
   - Выпуск сообщества Visual Studio 2015 доступен https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx по В этом выпуске требуется ручная установка Microsoft Office средств разработчика для Visual Studio.
    
   Инструменты Microsoft Office для разработчиков Visual Studio доступны по https://www.visualstudio.com/en-us/features/office-tools-vs.aspx
    
- **Учетная запись Project Online:** предоставляет доступ к службе размещения. Дополнительные сведения о получении учетной записи Project Online см. здесь: https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Убедитесь, что у пользователя надстройки достаточно авторизации для доступа к некоторым проектам в клиенте Project Online. 
    
- **Проекты на сайте размещения,** которые заполнены информацией.
    
> [!NOTE]
> Стандартная .NET Framework является правильной используемой структурой. Не используйте "Профиль клиента .NET Framework 4". 
  
### <a name="set-up-the-visual-studio-project"></a>Настройка проекта Visual Studio

Настройка приложения состоит из создания нового проекта, связывания соответствующих библиотек и объявления необходимых пространств имен. Visual Studio поддерживает нескольких типов проектов разработки. Раздел краткий и очень простой. Значение состоит в том, что сведения совмескуются в одном месте.
  
#### <a name="select-a-visual-studio-project"></a>Выберите проект Visual Studio

Чтобы создать проект соответствующего типа для надстройки, необходимо сделать следующее. Ключевые слова, которые встречаются на экране, имеют **полужирный** атрибут: 
  
1. В меню "Файл" выберите **"Файл**  >  **новый**  >  **проект".** 
    
2. В левой области установленных шаблонов выберите веб-надстройки **C#** Для Office и  >  **SharePoint.**  >   
    
3. В верхней части центральной области выберите **.NET Framework 4** или более поздней; текущая версия — 4.6. 
    
4. Из типов приложений на центральной области выберите надстройку **SharePoint.** 
    
5. В нижней части укажите имя и расположение проекта, а также имя решения. 
    
6. Кроме того, в нижней части установите флажок **Создать каталог для решения**. 
    
7. Нажмите кнопку **ОК**, чтобы создать начальный проект. 
    
Мастер Visual Studio задает несколько последующих вопросов о сайте параметров Project Online (называемых настройками SharePoint в диалоговом окнах) в нескольких последующих диалогов. Ниже 2 000 000 000 0
  
1. Какой сайт SharePoint вы хотите использовать для отладки надстройки? Укажите URL-адрес сайта PWA, например https://contoso.sharepoint.com/sites/pwa .
    
2. Как вы хотите провести надстройки SharePoint? Choose [X] **SharePoint-hosted**.
    
   Дополнительные сведения о надстройки SharePoint, включая параметры размещения, см. в [надстройках SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)
    
3. Нажмите **Далее**. 
    
Во втором дополнительном диалоговом ок можно указать версию SharePoint Online для надстройки: 
  
1. Какая версия SharePoint является более ранней, на которую будет ориентирована надстройка? Выберите [X] S **harePoint-Online.** 
    
2. Нажмите кнопку **Готово**. 
    
Visual Studio создает проект и имеет доступ к сайту Project Online. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Включить загрузку неогрузки на сайте Project Online

Загрузка нео боков — это механизм тестирования и отладки надстроек Project Online. Для загрузки неогрузки требуется два сценария: один для загрузки неогрузки на сайте Project Online, а другой — для отключения загрузки неогрузки после завершения тестирования и отладки надстройки.
  
Дополнительные сведения о настройке загрузки неоконтружаемого приложения см. в подзагрузке неоконтружаемого приложения в вашем [неоконтружаемом наборе веб-сайтов.](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)
  
> [!NOTE]
> Загрузка нео боковых приложений — это функция разработчика и тестирования. Он не **предназначен для производственного использования.** Не выгружайте нео том же приложения регулярно или о том, что загрузка неогруженных приложений включена дольше, чем вы активно используете эту функцию. 
  
## <a name="add-content-to-the-add-in-project"></a>Добавление содержимого в проект надстройки

После создания проекта и настройки механизма отладки добавление содержимого в приложение включает следующие задачи:
  
- Настройка области приложения
    
- Связывание библиотеки JSOM
    
- Добавление элементов пользовательского интерфейса в надстройку
    
- Инициализация и подключение к службе Project Online
    
- Ирисовка проектов, сведений и свойств
    
- Отображение проектов
    
- Отображение задач для проекта
    
Проект надстройки состоит из множества файлов. В этом примере необходимо изменить следующие файлы: 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.css — необязательный; содержит определения стилей, разработанные для надстройки
    
При изменениях клиента Project Online, например при переходе с пробной версии на сайт подписки, можно обновить свойства проекта, включая подключение к серверу и URL-адрес сайта, с помощью окна свойств, доступного в окне "Просмотр  >   свойств". 
  
Вы также можете добавлять файлы в проект. В этом случае необходимо обновить файл Elements.xml, расположенный в той же группе (контент, изображения, страницы или сценарии), чтобы включить новые файлы. Дополнительные сведения о файлах проекта см. в сведениях о структуре манифеста приложения и [пакете надстройки SharePoint.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)
  
### <a name="set-application-scope"></a>Настройка области приложения

Для надстройки требуется область действия или уровни разрешений, определенные перед тем, как служба возвращает сведения в результатах запроса. Для этой надстройки используйте следующую область для Visual Studio проекта. Это изменение внося в файл AppManifest.xml на вкладке "Разрешения":

|Область|Разрешение|
|:-----|:-----|
|Несколько проектов (Project Server)  <br/> |Чтение  <br/> |
   
Сохраните файл после настройки области приложения. В противном случае данные из службы не возвращаются. 
  
### <a name="link-the-jsom-library"></a>Связывать библиотеку JSOM

Библиотеки времени работы Project Online, PS.js и PS.debug.js, предоставляются в Project Online и всегда являются самой последней версией. Надстройки JavaScript, которые используют JSOM, должны связываться с одной из этих библиотек. Определения ссылок добавляются в файл Default.aspx. Команды для использования PS.js или PS.debug.js являются частью кода, расположенного в App.js файла.
  
Добавьте следующую команду для PS.js или PS.debug.js в элемент после  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` "SharePoint:ScriptLink" для sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Атрибут **OnDemand** для PS.js или PS.debug.js установлен в **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Добавление элементов пользовательского интерфейса в надстройку

Пример надстройки состоит из нескольких компонентов. Статические описания элементов находятся в файле Default.aspx. Описания динамических элементов и код для всех компонентов находятся в App.js файла. Комментарии к компонентам можно найти в списках исходных кодов. Вот список компонентов пользовательского интерфейса в надстройки:
  
- Название
    
- Вводная пошаговая фраза
    
- Кнопка для удаления задач из таблицы
    
- Таблица, в которую перечислены ИД и имя проекта, а также сведения о задаче.
    
- Кнопка задач (клонированная один раз для каждого проекта), которая импортирует данные задачи в таблицу.
    
Подробные сведения об пользовательском интерфейсе, например заголовок и часть заголовка таблицы проекта, см. в файле проекта Default.aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Инициализация и подключение к хост-системе

Файл App.js содержит код JavaScript. Надстройка загружает PS.js браузере, а затем вызывает функцию initializePage. InitializePage извлекает контекст конечной точки Project Online и запускает функцию loadProjects.
  
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

Функция loadProjects запрашивает у службы имена проектов и их ИД. 
  
Приложение извлекает имя проекта и его ИД. Доступны и другие сведения о проекте, к ним можно получить доступ, изменяя метод загрузки для явного определения извлекаемого свойства. Пример представлен в коде в качестве комментария. 
  
В случае успешного выполнения запроса надстройка продолжает вызывать displayProjects. 
  
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

Функция displayProjects создает таблицу по одной строке для каждого проекта и кнопку для отображения задач для конкретного проекта. 
  
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
> Цикл while имеет доступ к свойствам ID и name. Это немного отличается от проекта с исходным кодом, который вызывает функцию, которая, в свою очередь, имеет доступ к тем же свойствам. 
  
### <a name="display-the-tasks-for-a-project"></a>Отображение задач для проекта

Задачи, хотя и являются частью надстройки, не являются частью начальной загрузки. Если пользователь заинтересован в задачах, связанных с проектом, нажатие кнопки "Показать задачи" приводит к отображжение задач в списке с помощью обработера событий btnLoadTasks. 
  
Обработец событий btnLoadTasks с соответствующим ИД проекта запрашивает задачи для указанного проекта с сервера. После получения btnLoadTasks передает список задач для отображения задач для отображения задач на экране.
  
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
> Цикл while имеет доступ к свойствам ИД задачи и имени. Это немного отличается от проекта с исходным кодом, который вызывает функцию, которая, в свою очередь, имеет доступ к тем же свойствам. 
  
Пример выходных данных для задач одного проекта:
  
![Снимок экрана, на котором показаны выходные данные]для задачи(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "проекта")
  
## <a name="see-also"></a>Дополнительные ресурсы

Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/en-us/project).
    


