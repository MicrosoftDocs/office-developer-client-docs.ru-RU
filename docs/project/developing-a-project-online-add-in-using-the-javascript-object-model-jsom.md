---
title: Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: В этой статье описывается разработка надстроек Microsoft Project Online для повышения качества работы с Project Online. Проект разработки реализован как пошаговое руководство. Надстройка, используемая для этой статьи, считывает и отображает имена проектов и идентификаторов опубликованных проектов из учетной записи Project Online, а также позволяет получить подробные сведения о задачах, связанных с отдельными проектами.
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322694"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)

В этой статье описывается разработка надстроек Microsoft Project Online, позволяющая улучшить работу с Project Online. Проект разработки реализован как пошаговое руководство. Надстройка, используемая для этой статьи, считывает и отображает имена проектов и идентификаторов опубликованных проектов из учетной записи Project Online, а также позволяет получить подробные сведения о задачах, связанных с отдельными проектами.
  
Во время выполнения список надстроек выглядит примерно так, как показано на следующем рисунке:
  
![Снимок экрана, на котором показан список проектов и задач JSOM,](media/766e5914-f048-48f4-9282-291f55e6e90d.png "иллюстрирующий список проектов и задач JSOM")
  
В этом примере основное внимание уделяется взаимодействию с Project Online, что делает запросы и настраивает контекст для каждого запроса от службы. Элементы ПОЛЬЗОВАТЕЛЬСКОГО интерфейса получают минимальное внимание. Вместо этого списки источников содержат комментарии к пользовательскому интерфейсу.
  
> [!NOTE]
> Исходные файлы для примера надстройки, проект Visual Studio, доступны по адресу: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks..... Во время чтения статьи Храните исходные файлы как справочные материалы, когда все дополняют ее. Файлы в построении проекта Visual Studio и исполняемые файлы с минимальными изменениями — замена URL-адреса для клиента Project Online на папку PWA. 
  
## <a name="background"></a>Общие сведения

Project Online — это служба Office 365, которая предоставляет организациям решение для координации и управления портфелями, программами и проектами, используя решение для управления портфелем проектов (PPM) и управления проектами Office (PMO). Project Online — это другое предложение, чем выпуски Project для настольных ПК; Однако Project Online по-прежнему содержит функциональные возможности для обслуживания и отслеживания сведений о проекте в течение всего времени существования проекта. Project Online основан на SharePoint Online.
  
Размещенная Надстройка Project Online состоит из JavaScript и файлов ресурсов, взаимодействующих с API клиент-объектной модели. Когда пользователь посещает надстройку, JavaScript и ресурсы загружаются и выполняются в браузере. Надстройка выполняет асинхронные вызовы Project Online, чтобы взаимодействовать со службой, будь то создание, извлечение, обновление или удаление данных. 
  
Project Online выполняет еще одно действие для защиты информации, которая относится к другим клиентам, из надстройки; Project Online создает изолированный сайт для взаимодействия с запросами из надстройки. На узле Project Online не выполняется настраиваемый код. 
  
Настройка разработки для надстроек Project Online использует тип проекта надстройки SharePoint для Visual Studio. Надстройка написана на JavaScript и использует объектную модель JavaScript для Project (JSOM) для взаимодействия с веб-службой Project Online. JSOM наследует множество функций из SharePoint JSOM.
  
> [!NOTE]
> Надстройки могут быть опубликованы и проданы в магазине Office или развернуты в частном каталоге приложений в SharePoint. Дополнительные сведения можно найти [в статье Развертывание и публикация надстройки Office](https://docs.microsoft.com/office/dev/add-ins/publish/publish).
> 
> Надстройка, используемая в этой статье, является примером для разработчиков; Он не предназначен для использования в рабочей среде. Основная цель — показать пример разработки приложений для Project Online. 
  
## <a name="prerequisites"></a>Необходимые компоненты

Добавьте следующие элементы в поддерживаемую среду Windows:
  
- **.NET framework 4,0 или более поздней**версии: совместимые версии .NET Framework от версии 4,0. Сайт загрузки файлов — https://msdn.microsoft.com/vstudio/aa496123.aspx.
    
- **Visual Studio 2013 или более поздней версии**:  
    
   - Профессиональный выпуск Visual Studio 2015 готов к использованию и доступен по адресу https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.
    
   - Выпуск Visual Studio 2015 для сообщества пользователей доступен по адресу https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx. Для этого выпуска требуется ручная установка инструментов разработчика Microsoft Office для Visual Studio.
    
   Инструменты разработчика Microsoft Office для Visual Studio доступны по адресу https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.
    
- **Учетная запись Project Online**: обеспечивает доступ к службе хостинга. Дополнительные сведения о получении учетной записи Project Online см. здесь: https://products.office.com/en-us/Project/project-online-portfolio-management.
    
   Убедитесь, что у пользователя надстройки есть достаточные права на доступ к некоторым проектам в клиенте Project Online. 
    
- **Проекты на сайте сайта** с данными.
    
> [!NOTE]
> Стандартная платформа .NET Framework — правильная используемая платформа. Не используйте "клиентский профиль .NET Framework 4". 
  
### <a name="set-up-the-visual-studio-project"></a>Настройка проекта Visual Studio

Настройка приложения состоит из создания нового проекта, связывания соответствующих библиотек и объявления необходимых пространств имен. Visual Studio поддерживает нескольких типов проектов разработки. Раздел является кратким и очень базовым. Значение заключается в том, что сведения объединены в одном месте.
  
#### <a name="select-a-visual-studio-project"></a>Выберите проект Visual Studio

Чтобы создать проект соответствующего типа надстройки, необходимо выполнить следующие действия. Ключевые слова на экране имеют атрибут **Bold** : 
  
1. В меню Файл выберите **файл** > **создать** > **проект**. 
    
2. На левой панели в разделе Установленные шаблоны выберите пункт **C#** > **Office и** > **веб-** надстройки SharePoint. 
    
3. В верхней части центральной панели выберите **.NET Framework 4** или более поздней версии. Текущая версия — 4,6. 
    
4. В центральной области в разделе Типы приложений выберите **надстройка SharePoint**. 
    
5. В нижней части укажите имя и расположение проекта, а также имя решения. 
    
6. Кроме того, в нижней части установите флажок **Создать каталог для решения**. 
    
7. Нажмите кнопку **ОК**, чтобы создать начальный проект. 
    
Мастер Visual Studio запрашивает несколько дальнейших вопросов о сайте параметров Project Online (называемых параметрами SharePoint в диалоговых окнах) в нескольких следующих диалоговых окнах. Вот вопросы:
  
1. Какой сайт SharePoint вы хотите использовать для отладки надстройки? Укажите URL-адрес сайта PWA, например https://contoso.sharepoint.com/sites/pwa.
    
2. Как вы хотите разместить надстройку SharePoint? Выберите [X] **размещаемую в SharePoint**.
    
   Для получения дополнительных сведений о надстройках SharePoint, в том числе о вариантах их хранения, обратитесь к разделу надстройки [SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).
    
3. Нажмите кнопку **Далее**. 
    
Во втором дополнительном диалоговом окне предлагается указать версию SharePoint Online для надстройки. 
  
1. Какова самая ранняя версия SharePoint, которую вы хотите назначить надстройке? Выберите [X] S **харепоинт-Online**. 
    
2. Нажмите кнопку **Готово**. 
    
Visual Studio создает проект и получает доступ к сайту Project Online. 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Включение загрузки неопубликованных приложений на сайте Project Online

Неопубликованный сервер — это механизм тестирования и отладки надстроек Project Online. Для загрузки неопубликованных приложений требуется два сценария: один — для включения неопубликованных приложений на сайте Project Online, а другой — для отключения загрузки неопубликованных приложений после тестирования и отладки надстройки.
  
Дополнительные сведения о настройке корпоративных приложений можно найти [в статье Включение неопубликованной копии приложений в семействе веб-сайтов, не являющихся разработчиками](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).
  
> [!NOTE]
> Приложения для загрузки неопубликованных приложений — это функция разработки и тестирования. Он **не предназначен для производственного использования**. Не Загрузка неопубликованных приложения регулярно или храните загрузку неопубликованных приложений дольше, чем вы активно используете эту функцию. 
  
## <a name="add-content-to-the-add-in-project"></a>Добавление контента в проект надстройки

После создания проекта и настройки механизма отладки Добавление контента в приложение включает в себя следующие задачи:
  
- Настройка области применения приложения
    
- Связывание библиотеки JSOM
    
- Добавление элементов пользовательского интерфейса в надстройку
    
- Инициализация и подключение к службе Project Online
    
- Получение проектов и сведений и свойств
    
- Отображение проектов
    
- Отображение задач для проекта
    
Проект надстройки состоит из нескольких файлов. В этом примере необходимо изменить следующие файлы: 
  
- AppManifest. XML
    
- Default. aspx
    
- App. js
    
- App. CSS — необязательный; содержит определения стилей, разработанные для надстройки
    
Если клиент Project Online изменился (например, переход с пробной версии на сайт подписки), можно обновить свойства проекта, включая подключение сервера и URL-адрес сайта, используя окно Свойства, доступное через команду **View** > **Properties Window** . 
  
Вы также можете добавлять файлы в проект. В этом случае необходимо обновить файл Elements. XML, расположенный в той же группе (содержимое, изображения, страницы или скрипты), чтобы добавить новые файлы. Дополнительные сведения о файлах проекта приведены в статье [изучение структуры манифеста приложения и пакета надстройки SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).
  
### <a name="set-application-scope"></a>Задать область применения приложения

Надстройке требуются уровни или уровни разрешений, определенные до того, как служба возвращает сведения в результатах запроса. Для этой надстройки используйте следующую область в проекте Visual Studio. Это изменение вносятся в файл AppManifest. XML на вкладке разрешения:

|Scope|Разрешение|
|:-----|:-----|
|Несколько проектов (Project Server)  <br/> |Чтение  <br/> |
   
Сохраните файл после задания области применения приложения. В противном случае данные из службы не будут возвращены. 
  
### <a name="link-the-jsom-library"></a>Связывание библиотеки JSOM

Библиотеки среды выполнения Project Online, PS. js и PS. Debug. js предоставляются в Project Online и всегда являются самыми последними версиями. Надстройки JavaScript, использующие JSOM, должны ссылаться на одну из этих библиотек. Определения ссылок добавляются в файл Default. aspx. Команды для использования файла PS. js и/или PS. Debug. js являются частью кода, расположенного в файле App. js.
  
Добавьте указанную ниже команду для определения PS. js или PS. Debug. js в `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` элементе, подразделе "SharePoint: ScriptLink" для SP. js. 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> Атрибут **OnDemand** для PS. js или PS. Debug. js имеет значение **false**. 
  
### <a name="add-ui-elements-to-the-add-in"></a>Добавление элементов пользовательского интерфейса в надстройку

Пример надстройки состоит из нескольких компонентов. Описания статических элементов находятся в файле Default. aspx. Описания динамических элементов и код для всех компонентов находятся в файле App. js. Комментарии, касающиеся компонентов, можно найти в листингах исходного кода. Ниже приведен список компонентов пользовательского интерфейса в надстройке.
  
- Название
    
- Вводный многословные
    
- Кнопка для удаления задач из таблицы
    
- Таблица, в которой перечислены идентификатор проекта и его имя, а также сведения о задаче.
    
- Кнопка "задачи" (копируется один раз для каждого проекта), который импортирует данные задачи в таблицу.
    
Подробные сведения о пользовательском интерфейсе, такие как заголовок и область заголовка таблицы Project, представлены в файле проекта Default. aspx.
  
### <a name="initialize-and-connect-to-the-host-system"></a>Инициализация и подключение к обслуживающей системе

Файл App. js содержит код JavaScript. Надстройка загружает в браузере PS. js, а затем вызывает функцию Инитиализепаже. Инитиализепаже получает контекст конечной точки Project Online и запускает функцию Лоадпрожектс.
  
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

Функция Лоадпрожектс запрашивает у службы имена и идентификаторы проектов. 
  
Приложение извлекает имя проекта и идентификатор проекта. Другие сведения о проекте доступны, и доступ к ним можно получить, изменив метод Load, чтобы явным образом определить свойства для извлечения. Пример представлен в коде в виде комментария. 
  
Если запрос выполнен успешно, надстройка продолжается вызовом Дисплайпрожектс. 
  
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

Функция Дисплайпрожектс создает таблицу, одну строку для каждого проекта и кнопку для отображения задач для конкретного проекта. 
  
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
> Цикл while получает доступ к свойствам ID и Name. Это немного отличается от проекта исходного кода, который вызывает функцию, которая, в свою очередь, обращается к тем же свойствам. 
  
### <a name="display-the-tasks-for-a-project"></a>Отображение задач для проекта

Задачи, в то время как часть надстройки, не являются частью начальной загрузки. Если пользователь заинтересован в задачах, связанных с проектом, при нажатии кнопки "Show Tasks" задачи отображаются в списке с помощью обработчика событий Бтнлоадтаскс. 
  
Обработчик событий Бтнлоадтаскс с соответствующим ИДЕНТИФИКАТОРом проекта запрашивает задачи для указанного проекта с сервера. После извлечения Бтнлоадтаскс передает список задач в displayTasks для показа задач на экране.
  
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
> Цикл while получает доступ к свойствам идентификатора и имени задачи. Это немного отличается от проекта исходного кода, который вызывает функцию, которая, в свою очередь, обращается к тем же свойствам. 
  
Ниже приведены примеры выходных данных для задач одного проекта.
  
![Снимок экрана]с изображением(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "снимка экрана на странице задач проекта, в котором показаны выходные данные для задачи проекта")
  
## <a name="see-also"></a>Дополнительные ресурсы

Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/en-us/project).
    


