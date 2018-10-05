---
title: Разработка Project Online надстройки с помощью модели объектов JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: В этой статье описываются разработки надстройки Microsoft Project сети для улучшения работы с Project Online. Разработка проект реализован в виде Пошаговое руководство. Надстройки, используемые для данной статьи считывает и отображает имена проектов и идентификаторы опубликованные проекты из учетной записи Project Online и позволяет перейти получение задачи, связанные с отдельными проектами.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399307"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Разработка Project Online надстройки с помощью модели объектов JavaScript (JSOM)

В этой статье описываются разработки надстройки Microsoft Project сети для улучшения работы с Project Online. Разработка проект реализован в виде Пошаговое руководство. Надстройки, используемые для данной статьи считывает и отображает имена проектов и идентификаторы опубликованные проекты из учетной записи Project Online и позволяет перейти получение задачи, связанные с отдельными проектами.
  
Во время выполнения добавить в список выглядит примерно на следующем рисунке:
  
![Снимок экрана с отображением список элементов JSOM проектов и задач] (media/766e5914-f048-48f4-9282-291f55e6e90d.png "Снимок экрана с отображением список элементов JSOM проектов и задач")
  
В примере выделена взаимодействия с Project Online, выполнения запросов и установки контекста для каждого запроса в службе. Элементы пользовательского интерфейса (UI) получают минимальной внимания. Перечни источника предоставляют комментарии относительно пользовательского интерфейса.
  
> [!NOTE]
> Исходные файлы для примера надстройки, проекта Visual Studio, доступном по адресу: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks..... Сохранить исходные файлы под рукой справки во время ознакомьтесь со статьей как друг с другом дополняет. Файлы в Visual Studio проекта построения и исполняемый файл с минимальными изменениями, подставляя URL-адрес для клиента Project Online вниз до папки веб-клиента Project. 
  
## <a name="background"></a>Общие сведения

Project Online — это служба Office 365, который предоставляет компании с помощью управления портфелем проектов (PPM) и office (PMO) решение для управления проектами для координации и управления портфелей, программ и проектов. Project Online — это различные предложения, чем выпуски рабочего стола Project; еще Project Online по-прежнему содержит функциональные возможности для обслуживания и отслеживания сведений о проекте в течение всего жизненного цикла проекта. Project Online построена на SharePoint Online.
  
Project Online размещенных надстройки состоит из файлов JavaScript и ресурсов, которые взаимодействуют с использованием интерфейса API клиентской стороне-объектной модели. При посещении надстройки, JavaScript и ресурсы, загружаются и выполнена в браузере. Надстройка вызывает в асинхронном Project Online для взаимодействия со службой, будет ли создание, получение, обновление или удаление данных. 
  
Project Online выполняет одного дополнительные действия для защиты информации, к которой относится к другим клиентам из надстройки; а именно Project Online создает изолированной сайта для взаимодействия с запросов от надстройки. Пользовательский код не выполняется на узле Project Online. 
  
Программа установки разработки для Project Online надстроек использует тип проекта Visual Studio SharePoint надстройки. Надстройки, записывается в JavaScript и для взаимодействия с Project Online службы с помощью объектной модели Project JavaScript (JSOM). JSOM наследует большую часть его функциональные возможности SharePoint JSOM.
  
> [!NOTE]
> Надстройки могут публикации и продается в магазин Office или развернут в частном каталоге приложений на сайте SharePoint. Дополнительные сведения можно [Развернуть и публикация надстройки Office](https://docs.microsoft.com/office/dev/add-ins/publish/publish).
> 
> Надстройки, используемые в этой статье приведен пример для разработчиков; он не предназначен для использования в рабочей среде. Основной целью является Показать пример разработки приложений для Project Online. 
  
## <a name="prerequisites"></a>Необходимые разрешения

Поддерживаемые среды Windows добавьте следующие элементы:
  
- **.NET framework 4.0 или более поздней версии**: совместимы полной версии framework версии 4.0. Сайт загрузки — это https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 или более поздней версии**:  
    
   - Профессиональный выпуск Visual Studio 2015 готова к работе out-встроенным и доступны в https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - Сообщество выпуск Visual Studio 2015 доступном по адресу https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx. В этом выпуске требуется ручная установка инструментов разработчика Microsoft Office для Visual Studio.
    
   Инструменты разработчика Microsoft Office для Visual Studio доступны на https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.
    
- **Учетная запись A Project Online**: Это обеспечивает доступ к службе размещения. Дополнительные сведения о получении учетной записи Project Online можно https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Убедитесь, что пользователь надстройки имеет недостаточно прав на доступ к некоторых проектов в Project Online для клиентов. 
    
- **Проекты на узле размещения** , заполненный сведения.
    
> [!NOTE]
> Стандартный .NET Framework — это правильный framework для использования. Не используйте «Профиль .NET Framework 4 клиента». 
  
### <a name="set-up-the-visual-studio-project"></a>Настройка проекта Visual Studio

Настройка приложения состоит из создания нового проекта, связывание соответствующие библиотеки и объявление необходимых пространств имен. Visual Studio содержит несколько типов проектов разработки. Раздел представляет краткий и основные. Значение является наличие совместно в одном месте.
  
#### <a name="select-a-visual-studio-project"></a>Выбор проекта Visual Studio

Создание проекта соответствующего типа для надстройки, необходимо выполнить следующие действия. Ключевые слова, на экране иметь атрибут **полужирного шрифта** : 
  
1. В меню Файл выберите команду **файл** > **New** > **проекта**. 
    
2. Установленные шаблоны в левой области выберите **C#** > **Office/SharePoint** > **Web - надстройки**. 
    
3. В верхней области центра, установите **.NET Framework 4** или более поздняя версия; Текущая версия — 4.6. 
    
4. Типы приложений в центральной области выберите **Добавить в SharePoint**. 
    
5. В нижней части укажите имя и расположение проекта и имя решения. 
    
6. Также в нижней части установите флажок **Создать каталог для решения** . 
    
7. Нажмите **кнопку ОК** , чтобы создать исходный проект. 
    
Мастер Visual Studio указываются Project Online параметров сайта (называемое параметры SharePoint в диалоговых окнах) ряда звонящему вопросов в нескольких диалоговых окон, следуйте. Ниже приведены вопросы.
  
1. Какой сайт SharePoint вы хотите использовать для отладки надстройки? Укажите URL-адрес для веб-узла веб-клиента Project, таких как https://contoso.sharepoint.com/sites/pwa.
    
2. Как требуется размещать надстройки SharePoint? Выберите [X] **Размещение в SharePoint**.
    
   Дополнительные сведения о SharePoint надстройках включая варианты размещения, можно [надстройки SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Нажмите кнопку **Далее**. 
    
Второй диалоговое окно дополнительных запрашивает можно использовать для определения версии SharePoint Online для надстройки: 
  
1. Что такое самая ранняя версия SharePoint, которое надстройки к целевому? Выберите [X] S **harePoint Online**. 
    
2. Нажмите кнопку **Готово**. 
    
Visual Studio создает проект и получает доступ к Project Online сайта. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Включить sideloading на сайт Project Online

Sideloading — это механизм для тестирования и отладки Project Online надстроек. Необходимо два сценария для sideloading: один для включения sideloading на сайте Project Online, а другой для отключения sideloading после завершения тестирования и отладки надстройки.
  
Дополнительные сведения о настройке sideloading [приложения SideLoading в семействе веб-сайтов не разработчика](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)см.
  
> [!NOTE]
> Sideloading приложения — это функция разработчика/test. Это **не предназначенный для использования в рабочей среде**. Регулярно выполните не sideload приложения или оставьте включена поддержка больше, чем вы активно использующих функцию sideloading приложения. 
  
## <a name="add-content-to-the-add-in-project"></a>Добавление контента в проект надстройки

После создания проекта и настройка механизм отладки, добавление контента в приложение включает в себя следующие задачи:
  
- Задание области приложения
    
- Связывание библиотекой JSOM
    
- Добавление элементов пользовательского интерфейса для надстройки
    
- Инициализация и подключение к службе Project Online
    
- Получение проектов и сведений и свойства
    
- Отображение проектов
    
- Отображение задачи для проекта
    
Проект надстройки состоит из нескольких файлов. В этом примере вам потребуется изменить следующие файлы: 
  
- Файл AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.CSS - необязательный; содержит определения стилей, разработанных для надстройки
    
При изменении проекта интерактивного клиента, такие как перемещение из пробную версию подписки на сайт, можно обновить свойства проекта, включая подключение к серверу и URL-адрес сайта с помощью окно свойств, доступных в **представлении** > **Свойства Окно** команды. 
  
Также можно добавить файлы в проект. Если это так, то необходимо обновить файл Elements.xml, расположенный в той же группе (контент, изображения, страницы или сценарии) для включения новых файлов. Дополнительные сведения о файлах проекта [Изучите Структура манифеста приложения и пакет из SharePoint надстройки](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)см.
  
### <a name="set-application-scope"></a>Область приложения Set

Надстройка должна области или разрешение уровней определенных перед служба возвращает сведения в результатах запроса. Для этой надстройки используйте следующие области действия в проект Visual Studio. Это изменение внесено для файла AppManifest.xml на вкладке разрешения:

|Область|Permission|
|:-----|:-----|
|Несколько проектов (Project Server)  <br/> |Read  <br/> |
   
Сохраните файл после настройки области приложения. В противном случае данные не будут возвращены из службы. 
  
### <a name="link-the-jsom-library"></a>Связать с библиотекой JSOM

Библиотеки времени выполнения Project Online, PS.js и PS.debug.js, с Project Online и всегда являются наиболее поздней версии. Надстройки JavaScript, использующие JSOM необходимо связать с одним из этих библиотек. Связи определения добавляются в файл Default.aspx. Команды, чтобы использовать PS.js и/или PS.debug.js являются частью кода, находится в файле App.js.
  
Добавьте следующую команду для определения PS.js или PS.debug.js в `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` элемент после «SharePoint:ScriptLink» для sp.js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Атрибут **OnDemand** для PS.js или PS.debug.js значение **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Добавление элементов пользовательского интерфейса для надстройки

Пример добавления в состоит из нескольких компонентов. Описания статических элементов, находятся в файл Default.aspx. Описание динамических элементов и код для всех компонентов, находятся в файле App.js. Комментарии относительно компонентов можно найти исходного кода. Далее представлен список компонентов пользовательского интерфейса в надстройку:
  
- Title
    
- Ознакомительные формулировки
    
- Нажмите кнопку, чтобы удалить задачи из таблицы
    
- Таблица, перечисляющая код проекта и имя и сведения о задаче.
    
- Обзор задач кнопки (клонировании один раз для каждого проекта), импортирует данные задачи в таблице.
    
Для получения дополнительных сведений о пользовательском интерфейсе, такие как название и область заголовка в таблице проекта просмотрите файл Default.aspx проекта.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Инициализация и подключения к системе узла

Файл App.js содержит код JavaScript. Надстройка загружается PS.js в браузере и затем вызывает функцию initializePage. InitializePage получает контекст к конечной точке Project Online и запускает функцию loadProjects.
  
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

### <a name="retrieve-the-projects"></a>Получение проектов

Функция loadProjects запрашивает службу для проекта имена и идентификаторы. 
  
Приложение получает имя проекта и проекта код. Другие сведения о проекте доступен и осуществляется путем изменения метод load для идентификации явно свойства для извлечения. Пример предоставляется в коде комментария. 
  
Если запрос пройдет успешно, надстройка продолжает путем вызова displayProjects. 
  
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

Функция displayProjects создает таблицы, одной строке для каждого проекта и кнопка для отображения задач для конкретного проекта. 
  
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
> Цикл while обращается к идентификатор и имя свойства. Это отличается от проект исходного кода, которая вызывает функцию, в свою очередь, обращается к те же свойства. 
  
### <a name="display-the-tasks-for-a-project"></a>Отображение задачи для проекта

Задачи, при частью надстройки, не являющихся частью начальной загрузки. Если пользователь заинтересована в задачи, связанные с проектом, нажав кнопку «Показать задачи» вызывает задачи для отображения в списке с помощью обработчика событий btnLoadTasks. 
  
Обработчик событий btnLoadTasks с Идентификатором соответствующий проект запрашивает задачи для указанного проекта с сервера. После извлечения, btnLoadTasks передает список задач displayTasks до настоящего времени задачи на экране.
  
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

Функция displayTasks отображает задачи, связанные с указанной проекта непосредственно под записью проекта.
  
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
> Цикл while обращается к идентификатор задачи и имя свойства. Это отличается от проект исходного кода, которая вызывает функцию, в свою очередь, обращается к те же свойства. 
  
Следует пример выходных данных для задач одного проекта.
  
![Снимок экрана: выходных данных для задачи проекта] (media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Снимок экрана: выходных данных для задачи проекта")
  
## <a name="see-also"></a>См. также

Документация и примеры, связанные с Project Online и разработки приложений с помощью CSOM в разделе [Портал проектов разработки](https://developer.microsoft.com/en-us/project).
    


