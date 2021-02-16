---
title: Создание надстройки Project Server с размещением в SharePoint
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Из трех типов приложений, которые можно создать для Project Online (с автоматическим размещением, размещением у поставщика и с размещением в SharePoint), проще всего создать и развернуть приложение с размещением в SharePoint.
ms.openlocfilehash: 9b3b41eda40a8419ad72f11bb474acf7acaf81e9
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773759"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Создание надстройки Project Server с размещением в SharePoint

Из трех типов приложений, которые можно создать для Project Online (с автоматическим размещением, размещением у поставщика и с размещением в SharePoint), проще всего создать и развернуть приложение с размещением в SharePoint. Приложение с хостингом SharePoint не требует проверки подлинности OAuth и не использует Azure или требует обслуживания локального сайта для ресурсов, обслуживаемого поставщиком. Шаблон **приложения для SharePoint 2013** в Visual Studio — это удобная основа для разработки приложений, которые можно публиковать и продавать в Магазине Office или развертывать в частном каталоге приложений в SharePoint. 
  
В Project статус — это процесс, в котором участник группы может использовать страницу задач в Project Web App для отправки состояния назначенной задачи, например количества часов, отработано каждый день недели, потраченных на работу над задачей. Владелец назначения (обычно руководитель проекта) может утвердить или отклонить состояние. После утверждения состояния Project изменяет расписание. Приложение **QuickStatus** отображает назначенные задачи, при этом пользователь может быстро обновить процент завершения и отправить отчет о состоянии выбранных назначений для утверждения. Хотя страница задач в Project Web App имеет гораздо больше функциональных возможностей, приложение **QuickStatus** является примером упрощенного интерфейса. 
  
Приложение **QuickStatus** — это пример для разработчиков, оно не предназначено для использования в рабочей среде. Основная цель — показать пример разработки приложений для Project Online, а не создать полнофункциональные приложения с состоянием. Более эффективный способ определения состояния см. рекомендациях в разделе [Дальнейшие действия](#pj15_StatusingApp_NextSteps).
  
Общие сведения о состоянии см. в сведениях о [ходе выполнения задачи.](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress) Дополнительные сведения о разработке надстройки для SharePoint и Project Server см. в [надстройки SharePoint.](https://msdn.microsoft.com/library/jj163230.aspx)

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Необходимые компоненты для создания приложения для Project Server 2013

Для разработки относительно простых приложений, которые можно развернуть в Project Online или в локальной установке Project Server 2013, можно использовать Napa, который предоставляет среду разработки в Интернете. Для более сложных приложений, изменения ленты Project Web App и упростить отладку во время разработки, можно использовать Visual Studio 2012 или Visual Studio 2013. Например, в локальной установке можно вручную проверить черновики таблиц данных на наличие изменений в базе данных Project Server. В этой статье показано, как разрабатывать приложения с помощью Visual Studio.
  
Для разработки приложений Project Server с использованием Visual Studio требуются следующие компоненты:
  
- Проверьте, что на локальном компьютере разработчика установлены самые последние пакеты обновления и обновления Windows. Операционной системой может быть Windows 7, Windows 8, Windows Server 2008 или Windows Server 2012.
    
- У вас должен быть компьютер, на котором установлены SharePoint Server 2013 и Project Server 2013, где компьютер настроен для изоляции приложений и загрузки неоконфигурируемых приложений. Загрузка неогрузки Visual Studio временно установить приложение для отладки. Вы можете использовать локальное установку SharePoint и Project Server. Дополнительные сведения см. в настройках локальной среды разработки [приложений для SharePoint.](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx)
    
   > [!NOTE]
   > Для локальной установки настройте изолированный домен  приложений перед созданием корпоративного каталога приложений. 
  
- Компьютером разработки может быть удаленный компьютер с установленными средствами разработчика Office для Visual Studio 2012. Убедитесь, что установлена самая новая версия; см. *раздел "Сервис"* загружаемых приложений для Office и [SharePoint.](https://msdn.microsoft.com/office/apps/fp123627.aspx)
    
- Убедитесь, что Project Web App, который вы будете использовать для разработки и тестирования, доступен в браузере.
    
Сведения об использовании веб-инструментов см. в подстройки среды для разработки приложений [для SharePoint в Office 365.](https://msdn.microsoft.com/library/fp161179.aspx) Поное руководство по построению простого приложения для Project Server, которое использует веб-инструменты, см. в серии блогов EPMSource, в рамках создания первого [приложения Project Server.](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/)

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Создание приложения для Project Server с помощью Visual Studio

Инструменты разработчика Office для Visual Studio 2012 включают шаблон для приложений SharePoint, которые можно использовать с Project Server 2013. При создании решения оно содержит следующие файлы для пользовательского кода:
  
- **AppManifest.xml** с параметрами для названия приложения, области запроса разрешений и другими свойствами. Процедура 1 содержит действия для установки свойств с помощью конструктора манифеста. 
    
- **Default.aspx** в папке "Страницы" — это главная страница приложения. В процедуре 2 показано добавление HTML5-контента для приложения **QuickStatus**. 
    
- **App.js** в папке Scripts является основным файлом для пользовательского кода JavaScript. В процедуре 3 объясняется код JavaScript для приложения **QuickStatus.** 
    
   При добавлении коммерческих элементов управления, таких как сетка на основе jQuery или элемент управления "Выбор даты", можно добавить ссылки на дополнительные файлы JavaScript в файл Default.aspx.
    
- **App.css** в папке "Контент" — это основной файл для настраиваемых стилей CSS3. Процедура 2 и 3 процедуры содержат сведения о каскадных таблицах стилей (CSS) для приложения **QuickStatus**. В файл Default.aspx можно добавить ссылки на дополнительные CSS-файлы. 
    
- **AppIcon.png** в папке "Изображения" — это значок 96 x 96, который приложение отображает в Магазине Office или каталоге приложений. 
    
Чтобы изменить Project Web App ленты, можно добавить настраиваемую ленту. В разделе [Пример кода приложения QuickStatus](#pj15_StatusingApp_Example) представлен полный код измененных файлов Default.aspx, App.js, App.css, Elements.xml и AppManifest.xml. 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Процедура 1. Создание проекта приложения в Visual Studio

1. Запустите Visual Studio 2012 от учетной записи администратора, а затем выберите "Новый **проект"** на странице "Начните". 
    
2. В диалоговом окне **Создание проекта** разверните узлы **Шаблоны**, **Visual C#** и **Office/SharePoint**, а затем выберите пункт **Приложения**. В раскрывающемся списке целевой платформы, расположенном в верхней части центральной панели, выберите **.NET Framework 4.5**, а затем выберите **Приложение для SharePoint 2013** (см. рис. 1). 
    
3. В поле **"Имя"** введите QuickStatus, перейдите к расположению, в котором вы хотите сохранить приложение, а затем выберите **"ОК".**
    
   **Рис. 1. Создание приложения Project Server в Visual Studio**

   ![Создание приложения Project Server в Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Создание приложения Project Server в Visual Studio")
  
4. В диалоговом окне **Создание приложения для SharePoint** заполните следующие три поля: 
    
   - В верхнем текстовом поле введите имя, которое приложение будет отображаться в Project Web App. Например, введите Быстрое обновление состояния.
    
   - Чтобы сайт можно было использовать для отладки, введите URL-адрес Project Web App экземпляра. Например, введите `https://ServerName/ProjectServerName` (заменив _ServerName_ и _ProjectServerName_ собственными значениями), а затем выберите "Проверить".  Если все пройдет успешно, Visual Studio отображает сообщение **Подключение выполнено успешно**. При отображении сообщения об ошибке убедитесь, что url-адрес Project Web App указан правильно и что компьютер Project Server настроен для изоляции приложений и загрузки неоконфигурируемых приложений. Дополнительные сведения см. в разделе ["Необходимые условия для создания приложения для Project Server 2013".](#pj15_StatusingApp_Prerequisites) 
    
   - В раскрывающемся списке **Как разместить приложение для SharePoint?** выберите **Размещение в SharePoint**.
    
   > [!CAUTION]
   > Если вы по ошибке выбрали значение по умолчанию, **С размещением у поставщика**, Visual Studio создает два проекта в решении: **QuickStatus** и **QuickStatusWeb**. Если вы видите два проекта, удалите решение и начните заново. 
  
5. Нажмите кнопку **ОК** для создания решения **QuickStatus**, проекта **QuickStatus** и файлов по умолчанию. 
    
6. Откройте представление конструктора манифеста (например, дважды щелкните файл AppManifest.xml). На вкладке **Общие** в текстовом поле **Название** должно отобразиться имя приложения, введенное на шаге 4. Откройте вкладку **Разрешения**, чтобы добавить следующие запросы разрешений для приложения (см. рис. 2): 
    
   - В первой строке списка **Запросы разрешений** в столбце **Область** выберите **Определение состояния** в раскрывающемся списке. В столбце **Разрешения** выберите **SubmitStatus**.
    
   - Добавьте строку, где **Область** — это **Несколько проектов**, а **Разрешение** — **Чтение**.
    
   **Рис. 2. Установка области разрешений для приложения определения состояния**

   ![Установка области разрешений для приложения определения состояния](media/pj15_CreateStatusingApp_PermissionScope.gif "Установка области разрешений для приложения определения состояния")
  
Приложение **QuickStatus** позволяет пользователю Project Web App читать назначения для этого пользователя из нескольких проектов, изменять процент завершения назначения и отправлять обновление. Другие области запроса разрешений, показанные в выпадаемом списке на рис. 2, не требуются для этого приложения. Области запроса разрешений — это разрешения, которые приложение запрашивает от имени пользователя. Если у пользователя нет этих разрешений в Project Web App, приложение не будет запускаться. Приложение может иметь несколько областей запроса разрешений, в том числе для других разрешений SharePoint, но должно иметь только минимальный необходимый уровень функциональности приложения. Ниже реализации областей запроса разрешений, связанных с Project Server. 

- **Корпоративные** ресурсы : разрешения диспетчера ресурсов для чтения или записи сведений о других Project Web App пользователях.
    
- **Несколько проектов**: чтение или запись в несколько проектов, для которых у пользователя есть запрашиваемые разрешения.
    
- **Project Server**: требует, чтобы у пользователя приложения были разрешения администратора для Project Web App.
    
- **Reporting**: read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App). 
    
- **Один проект**: чтение или запись в проект, для которого у пользователя есть запрашиваемые разрешения.
    
- **Определение состояния**: отправка обновлений состояния назначений, таких как время работы, процент завершения и новых назначений.
    
- **Рабочий процесс**: если у пользователя есть разрешения для запуска рабочих процессов Project Server, приложение выполняется с повышенными привилегиями для рабочего процесса.
    
Дополнительные сведения об области запросов разрешений для Project Server 2013 см. в разделе *"Приложения Project"* статьи "Обновления для разработчиков" в [Project 2013](updates-for-developers-in-project-2013.md) и разрешениях приложений [в SharePoint 2013.](https://msdn.microsoft.com/library/fp142383.aspx)


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Создание HTML-контента для приложения QuickStatus

Прежде чем приступить к написанию кода HTML-содержимого, разработать пользовательский интерфейс и пользовательский интерфейс для приложения QuickStatus (на рисунке 3 показан пример заполненной страницы). Проект также может включать структуру функций JavaScript, взаимодействующих с HTML-кодом. Общие сведения см. в [проектировании дизайна для приложений в SharePoint 2013.](https://msdn.microsoft.com/library/fp179934.aspx)
  
**Рис. 3. Проект страницы приложения QuickStatus**

![Проект страницы приложения QuickStatus](media/pj15_CreateStatusingApp_AfterRefresh.gif "Проект страницы приложения QuickStatus")
  
Приложение отображает имя в верхней части, а именно значение из элемента **Title** файла AppManifest.xml. 
  
По умолчанию страница использует HTML5. Ниже приведены стандартные HTML-элементы для основных объектов пользовательского интерфейса, которые содержатся в тексте страницы приложения **QuickStatus**: 
  
- Элемент **form** содержит все другие элементы пользовательского интерфейса. 
    
- Элемент **fieldset** создает контейнер и границу таблицы назначений, дочерний элемент **legend** предоставляет метку для контейнера. 
    
- Элемент **table** содержит название и заголовок таблицы. Функции JavaScript изменяют заголовок таблицы и добавляют строки для назначений. 
    
   > [!NOTE]
   > Чтобы легко добавить разбиение по страницам и сортировки, рабочее приложение, скорее всего, будет использовать коммерческий элемент управления сетки на основе jQuery вместо таблицы. 
  
   Таблица содержит столбцы имени проекта, имени задачи с флажком, фактических трудозатрат, процента завершения, оставшихся трудозатрат и даты окончания назначения. Функции JavaScript создают этот контрольный список и поле ввода текста для процентного завершения каждой задачи.
    
- Элемент **input** для текстового поля задает процента завершения всех выбранных назначений. 
    
- Элемент **button** отправляет изменения состояния. 
    
- Элемент **button** обновляет страницу. 
    
- Элемент **кнопки** выходит из приложения и возвращается на страницу задач в Project Web App. 
    
Нижние текстовые поля и кнопки находятся в элементах **div**, чтобы таблица CSS могла легко управлять положением и внешним видом объектов пользовательского интерфейса. Функция JavaScript добавляет абзац в нижней части страницы, содержащий результаты для успешного или неудачного обновления состояния. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Процедура 2. Создание HTML-контента

1. В Visual Studio откройте файл Default.aspx.
    
   Файл содержит два **элемента asp:Content:** элемент с атрибутом добавляется в заголовке страницы, а элемент с атрибутом помещается в элемент `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` тела `ContentPlaceHolderID="PlaceHolderMain"`  страницы. 
    
2. В области управления для загона страницы добавьте ссылку на файл PS.js  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` на компьютере Project Server. Для тестирования и отладки можно использовать PS.debug.js. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   Инфраструктура приложений использует `/_layouts/15/` виртуальный каталог для сайта SharePoint в IIS. Физический файл  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js` : .
    
   > [!NOTE]
   > Перед развертыванием приложения для производственного использования удалите ссылки  `.debug` на скрипты, чтобы повысить производительность. 
  
3. В элементе управления для тела страницы удалите созданный элемент div, а затем добавьте HTML-код для `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` объектов пользовательского  интерфейса. Элемент **table** содержит только строку заголовка. Столбец **Имя задачи** содержит элемент управления флажком. Текст для элемента **caption** заменяется обратным вызовом **onGetUserNameSuccess** для функции **getUserInfo** в файле App.js. 
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. В файле App.css добавьте код CSS, определяющий положение и внешний вид элементов пользовательского интерфейса. Полный код CSS приложения **QuickStatus** см. в разделе [Пример кода для приложения QuickStatus](#pj15_StatusingApp_Example). 
    
Процедура 3 добавляет функции JavaScript для чтения назначений и создания строк таблицы, а также для изменения и обновления процента завершения назначения. Фактические действия являются более итеративными при разработке приложения, где вы поочередно создаете часть HTML-кода, добавляете и тестируют связанные стили и функции JavaScript, изменяют или добавляете дополнительный HTML-код, а затем повторяете этот процесс.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Создание функций JavaScript для приложения QuickStatus

Шаблон Visual Studio для приложения SharePoint включает в себя файл App.js, который содержит код инициализации по умолчанию, получающий контекст клиента SharePoint и демонстрирующий базовые операции получения и установки для страницы приложения. Пространство имен JavaScript для клиентской библиотеки SharePoint SP.js **sp.** Так как приложение для Project Server использует библиотеку PS.js, приложение применяет пространство имен **PS** для получения контекста клиента и доступа к JSOM для Project Server. 
  
Функции JavaScript в **приложении QuickStatus** включают следующие: 
  
- Обработчик событий документа **ready** выполняется, когда создается экземпляр объектной модели документов (DOM). Обработчик события **ready** выполняет следующие четыре действия. 
    
    1. Инициализирует глобальную переменную **projContext** с клиентским контекстом для Project Server JSOM и глобальную переменную **pwaWeb**. 
        
    2. Вызывает функцию **getUserInfo** для инициализации глобальной переменной **projUser**. 
        
    3. Вызывает функцию **getAssignments**, которая возвращает указанные данные назначения пользователю. 
        
    4. Привязывает обработчики событий щелчка к флажку заголовка таблицы, а также к флажкам в каждой строке таблицы. Обработчики событий щелчка управляют атрибутом **checked** флажков, когда пользователь устанавливает или снимает флажки в таблице. 
    
- Если функция **getAssignments** выполнена успешно, вызывается функция **onGetAssignmentsSuccess**. Эта функция вставляет строку в таблицу для каждого назначения, инициализирует элементы управления HTML в каждой строке, а затем инициализирует свойства нижней кнопки. 
    
- **Обработник событий onClick** для кнопки **"Обновление"** вызывает **функцию updateAssignments.** Эта функция получает процент полного значения, которое применяется к каждому выбранному назначению; или если текстовое поле в процентах пусто, функция получает процент завершения каждого выбранного назначения в таблице. Затем **функция updateAssignments** сохраняет и передает обновления состояния и записывает сообщение о результатах в нижнюю часть страницы. 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>Процедура 3. Создание функций JavaScript

1. В Visual Studio откройте файл App.js и удалите все его содержимое.
    
2. Добавьте глобальные переменные и обработчик событий **ready**. Доступ к объекту **document** осуществляется с помощью функции jQuery. 
    
   Обработчик события щелчка для флажка заголовка таблицы задает состояние флажков строк. Если все флажки строки установлены или сняты, обработчик события щелчка задает установленное состояние флажка заголовка. Обработчики событий щелчка также задает результирующее сообщение в нижней части страницы как пустую строку.
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. Добавьте функцию **getUserInfo**, которая вызывает **onGetUserNameSuccess** при успешном выполнении запроса. Функция **onGetUserNameSuccess** заменяет содержимое абзаца **caption** на название таблицы, которое содержит имя пользователя. 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. Добавьте **функцию getAssignments,** которая **вызываетgetAssignmentsSuccess** (см. шаг 5) в случае успешного выполнения запроса на назначение. Параметр **Include** ограничивает запрос, возвращая только указанные поля. 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. Добавьте функцию **onGetAssignmentsSuccess**, которая добавляет строку для каждого назначения в таблицу. Переменная **prevProjName** используется для определения того, предназначена ли строка для другого проекта. В этом случае имя проекта отображается полужирным шрифтом, в противном случае имя проекта — это пустая строка. 
    
   > [!NOTE]
   > JSOM не включает свойства **TimeSpan,** которые включает CSOM, например **ActualWorkTimeSpan**. Вместо них JSOM использует свойства, определяющие время в миллисекундах, например [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx). Метод получения этого свойства — **\_ получить actualWorkMilliseconds,** который возвращается в качестве значения. > метод **get_actualWork** возвращает строку, например "3h". В приложении **QuickStatus** можно использовать оба значения, но отображать их по-разному. Запрос назначений содержит оба свойства, благодаря чему можно проверить значение во время отладки. Если удалить переменную **actualWork**, можно также удалить свойство **ActualWork** из запроса назначения. 
  
   Наконец, функция **onGetAssignmentsSuccess** инициализирует кнопки **Update** и **Refresh** с обработчиками события щелчка. Текстовое значение кнопки **Update** кнопки можно задать в HTML-коде. 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. Добавьте обработчик события щелчка **updateAssignments** для кнопки **Update**. Если пользователь изменяет процент завершения задачи или добавляет значение в текстовом поле **percentComplete**, значение можно ввести в различных форматах, например как "60", "60%" или "60 %". Метод **getNumericValue** возвращает введенный текст как числовое значение. 
    
   > [!NOTE]
   > В приложении для рабочей среды следует реализовать проверку вводимого текста и дополнительную проверку на наличие ошибок. 
  
   Пример **updateAssignments** применяет базовую проверку ошибок и отображает информацию в абзаце **message** в нижней части страницы — зеленым цветом, если запрос на обновление выполнен успешно, и красным цветом, если при вводе или выполнении запроса на обновление возникла ошибка. 
    
   Перед использованием метода **submitAllStatusUpdates** приложение должно сохранить обновления на сервере с помощью метода **PS.StatusAssignmentCollection.update**. 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. Добавьте **функцию exitToPwa,** которая использует параметр строки запроса **SPHostUrl** для URL-адреса узла Project Web App сайта. Чтобы вернуться на страницу "Задачи", необходимо перейти  `"/Tasks.aspx"` к URL-адресу. Например, **переменная spHostUrl** будет иметь значение  `https://ServerName/ProjectServerName/Tasks.aspx` .
    
   Функция **getQueryStringParameter** разбивает URL-адрес страницы **QuickStatus** для извлечения и возврата указанного параметра в параметрах URL-адреса. Ниже приведен пример значения **document.URL** для документа **QuickStatus** (все в одной строке): 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   Для предыдущего URL-адреса функция **getQueryStringParameter** возвращает строку **запроса SPHostUrl.** `https://ServerName/pwa` 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

Если опубликовать приложение **QuickStatus** на этом этапе и добавить его в Project Web App, приложение можно запустить на странице "Содержимое сайта", но оно будет труднодоступно для пользователей. Чтобы помочь пользователям, можно добавить кнопку приложения на ленту на странице "Задачи". В процедуре 4 показано, как добавить настраиваемое действие ленты. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Добавление настраиваемого действия на ленте

Вкладки, группы и элементы управления ленты для Project Web App заданы в pwaribbon.xml, который устанавливается в каталоге на компьютере с  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` Project Server. Чтобы помочь в разработке настраиваемых действий для ленты Project Web App, загружаемый SDK Project 2013 включает копию pwaribbon.xml. 
  
Project Web App для страницы задач используются различные определения ленты в зависимости от того, использует ли экземпляр Project Web App режим одной записи, позволяющий пользователям вводить значения как для этого, так и для состояния задачи. Если у вас есть административные разрешения для Project Web App, чтобы определить режим входа, выберите параметры **PWA** в меню параметров в верхнем правом углу страницы. На странице "Параметры PWA" выберите **Параметры и значения по умолчанию для расписания** и посмотрите на флажок **Режим одной операции** в нижней части страницы. 
  
Если режим одной операции отключен, ленту на странице "Задачи" определяет область Моя работа в файле pwaribbon.xml: 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

Если режим одной операции включен, ленту на странице "Задачи" определяет область Связанный режим в файле pwaribbon.xml: 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

Хотя группы и элементы управления в каждой области похожи друг на друга, элемент управления для связанного режима может вызывать функции, отличные от функций того же элемента управления в другом режиме. В процедуре 4 показано, как добавить элемент управления "Кнопка" для приложения **QuickStatus**, если режим одной операции выключен (флажок **Режим одной операции** не установлен). 
  
> [!NOTE]
> Общие сведения о добавлении дополнительных действий на ленту или в меню в приложении SharePoint см. в дополнительных действиях по развертыванию приложений [для SharePoint.](https://msdn.microsoft.com/library/jj163954.aspx) 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Процедура 4. Добавление настраиваемого действия ленты на страницу "Задачи"

1. Проверьте ленту на странице задач в Project Web App. Откройте вкладку **ЗАДАЧИ** на ленте и спланируйте, как ее изменить. Существует семь групп, таких как **Отправить**, **Задачи** и **Период**. Группа **Отправить** содержит два элемента управления: кнопка **Сохранить** и раскрывающееся меню **Отправить состояние**. Вы можете добавить элемент управления в любом месте в группе, добавить группу с новым элементом управления в любое место на вкладке **ЗАДАЧИ** или добавить другую вкладку с настраиваемыми группами и элементами управления. В этом примере мы добавляем третью кнопку для группы **Отправить**, которая вызывает URL-адрес приложения **QuickStatus**. 
    
2. В области **обозревателя** решений в Visual Studio щелкните правой кнопкой мыши проект **QuickStatus** и добавьте новый элемент. В **диалоговом окне** "Добавление нового элемента" выберите **настраиваемые** действия ленты (см. рис. 4). Например, придайте пользовательскому действию имя RibbonQuickStatusAction и выберите **"Добавить".**
    
   **Рис. 4. Добавление настраиваемого действия ленты**

   ![Добавление настраиваемого действия на ленте](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Добавление настраиваемого действия на ленте")
  
3. На первой странице мастера **создания настраиваемого действия ленты** оставьте параметр **Хост-сайт** выбранным, выберите **Нет** в раскрывающемся списке в качестве области настраиваемого действия, а затем нажмите кнопку **Далее** (см. рис. 5). Элементы раскрывающихся списков относятся к SharePoint, а не к Project Server. Мы заменим большую часть созданного XML для настраиваемого действия, чтобы применить XML к Project Server. 
    
   **Рис. 5. Указание свойств для настраиваемого действия ленты**

   ![Указание свойств для настраиваемого действия ленты](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Указание свойств для настраиваемого действия ленты")
  
4. На следующей странице мастера **создания настраиваемого действия ленты** оставьте все значения параметров по умолчанию, а затем нажмите кнопку **Готово** (см. рис. 6). Visual Studio создаст папку **RibbonQuickStatusAction**, которая содержит файл Elements.xml. 
    
   **Рис. 6. Указание параметров для элемента управления "Кнопка"**

   ![Указание параметров для элемента управления "Кнопка"](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Указание параметров для элемента управления "Кнопка"")
  
5. Измените созданный по умолчанию код в файле Elements.xml для настраиваемого действия ленты. Ниже приведен XML-код по умолчанию.
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. В элементе **CustomAction** удалите атрибуты **Sequence** и **Title**. 
    
   2. Чтобы добавить элемент управления в группу **отправки,** найдите первую группу в коллекции в pwaribbon.xml файле, который является элементом,  `Ribbon.ContextualTabs.MyWork.Home.Groups` который  `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"` начинается. Чтобы добавить в группу отправки дополнительный элемент управления, в следующем коде показан правильный атрибут **Location** элемента **CommandUIDefinition** в Elements.xml файла:  
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. Измените значения атрибутов дочернего элемента **Button** следующим образом: 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - Чтобы сделать кнопку третьим элементом управления в группе, атрибут **Sequence** может быть любым числом выше значения существующего элемента управления состоянием отправки (который является элементом `Sequence="20"`  **FlyoutAnchor** в pwaribbon.xml). По соглашению последовательное число групп и элементов управления , что позволяет вставлять элементы  `10, 20, 30, …` в промежуточные позиции.
    
       - Атрибут **Command** указывает команду, которая будет запускаться в **элементе CommandUIHandler** (см. следующий шаг 5.d). Вы можете упростить имя команды, чтобы упростить работу следующего разработчика. Например,  `Command="Invoke_QuickStatus"` это проще для чтения, чем  `Command="Invoke_RibbonQuickStatusActionButtonRequest"` .
    
       - Атрибуты изображения указывают значок размером 16 x 16 пикселей и значок размером 32 x 32 пикселя для кнопки. В файле Elements.xml по умолчанию  `Image32by32="_layouts/15/images/placeholder32x32.png"` указывается оранжевая точка. Вы можете извлечь значки из файлов карты изображений (ps16x16.png и ps32x32.png), установленных в каталоге на компьютере с  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Project Server. Например, значок размером 32 x 32 пикселя находится во втором столбце значков слева и в десятой строке вниз от верхней части карты изображения ps32x32.png (верхняя часть значка находится после конца девятой строки; 9 строк x 32 пикселя/строка = 288 пикселей). 
    
       - Для отображения всплывающей подсказки для элемента управления "Кнопка" добавьте атрибуты **ToolTipTitle** и **ToolTipDescription**. 
    
    4. Измените атрибуты элемента **CommandUIHandler**. Например, убедитесь, что атрибут **Command** соответствует значению атрибута **Command** элемента **Button**. Для **атрибута CommandAction** — это замество для `~appWebUrl` URL-адреса веб-страницы **QuickStatus.** Когда кнопка ленты вызывает приложение **QuickStatus**, маркер **{StandardTokens}** заменяется параметрами URL-адреса, а именно **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber** и **SPAppWebUrl**.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. В **обозревателе решений** откройте конструктор **Feature1.feature** и переместите элемент **RibbonQuickStatusAction** из области **Элементы в решении** в область **Элементы в компоненте**. При открытии конструктора **Package.package** элемент **RibbonQuickStatusAction** будет находиться в области **Элементы в пакете**. 
    
При разработке приложения и добавлении кнопки ленты обычно тестировать приложение и устанавливать точки останова в коде JavaScript для отладки. После нажатия клавиши **F5** Visual Studio компилирует приложение, развертывает его на сайте, который указан в свойстве **URL-адрес сайта** проекта **QuickStatus**, и отображает страницу с вопросом о том, доверяете ли вы приложению. Когда вы переходите и выходите из **приложения QuickStatus,** оно возвращается на страницу задач в Project Web App. 

> [!NOTE]
> На рисунке 7 показано, что кнопка **"Быстрое** состояние" на вкладке **"ЗАДАЧИ"** ленты отключена. После многих развертывание отлаки с Visual Studio настраиваемые элементы управления ленты могут быть заблокированы при продолжении отлаки или развертывания опубликованного приложения на том же тестовом сервере. Чтобы включить кнопку, удалите элемент **RibbonQuickStatusAction** в Visual Studio, а затем создайте новое действие ленты с другим именем и ИД. Если это не решает проблему, попробуйте удалить приложение из Project Web App тестового экземпляра, а затем повторно создать приложение с другим ИД приложения. 
  
**Рис. 7. Просмотр подсказки отключенной кнопки "Quick Status"**

![Просмотр подсказки для отключенной кнопки](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Просмотр подсказки для отключенной кнопки")
  
В процедуре 5 показано, как развернуть и установить приложение **QuickStatus**. В процедуре 6 показаны некоторые дополнительные действия для тестирования приложения после его установки. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Развертывание приложения QuickStatus

Существует несколько способов развертывания приложения в веб-приложении SharePoint, например Project Web App. Выбор используемого развертывания зависит от того, хотите ли вы опубликовать приложение в частном каталоге SharePoint или в общедоступный Магазин Office, а также от того, установлен ли SharePoint локально или в сетевой аренде. В процедуре 5 показано, как развернуть приложение **QuickStatus** для локальной установки в частном каталоге приложений. Дополнительные сведения см. в сведениях [об установке приложений для SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) и публикации приложений [для SharePoint](https://msdn.microsoft.com/library/jj164070.aspx) и управлении ими
  
> [!NOTE]
> Для добавления приложения в каталог SharePoint требуются разрешения администратора SharePoint. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Процедура 5. Развертывание приложения QuickStatus

1. Сохраните все файлы в Visual Studio, а затем щелкните правой кнопкой мыши проект **QuickStatus** в **обозревателе решений** и выберите команду **Опубликовать**.
    
2. Так как **приложение QuickStatus** размещено в SharePoint, существует очень мало вариантов публикации (см. рис. 8). В **диалоговом окне "Публикация приложений** для Office и SharePoint" выберите **"Готово".**
    
   **Рис. 8. Публикация приложения QuickStatus**

   ![Использование мастера публикаций](media/pj15_CreateStatusingApp_PublishWizard.gif "Использование мастера публикаций")
  
3. Скопируйте файл QuickStatus.app из каталога в удобный каталог на локальном компьютере (или на компьютер SharePoint для  `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` локальной установки). 
    
4. В центре администрирования SharePoint выберите **Приложения** на панели быстрого запуска и щелкните **Управление каталогом приложений**.
    
5. Если каталог приложений не существует, создайте для него коллекцию  веб-сайтов, следуя разделу "Настройка сайта каталога приложений для веб-приложения" в разделе "Управление каталогом приложений в [SharePoint 2013".](https://technet.microsoft.com/library/fp161234.aspx)
    
   Если каталог приложений существует, перейдите на URL-адрес сайта на странице "Управление каталогом приложений". Например, на следующих шагах сайт каталога приложений будет  `https://ServerName/sites/TestApps` .
    
6. На странице каталога приложений выберите **Приложения для SharePoint** на панели быстрого запуска. На странице "Приложения для SharePoint" откройте вкладку **ФАЙЛЫ** на ленте и нажмите кнопку **Отправить документ**.
    
7. В диалоговом окне **Добавление документа** найдите файл QuickStatus.app, добавьте комментарии для версии, а затем нажмите **ОК**.
    
8. При добавлении приложения также можно добавить локальные данные, например описание приложения, значок и другие сведения. В диалоговом окне "Приложения для **SharePoint — QuickStatus.app"** добавьте сведения, которые будут показываться для приложения в коллекции веб-сайтов SharePoint. Например, добавьте следующие сведения: 
    
   1. **Поле краткого** описания: введите тестовое приложение "Быстрое состояние".
    
   2. **Поле** описания: введите приложение "Тестирование", чтобы обновить процент выполнения задач в нескольких проектах.
    
   3. **Поля URL-адреса** значка: добавьте изображение размером 96 x 96 пикселей для значка приложения в ресурсы сайта для каталога приложений. Например, перейдите к содержимому сайта в выпадаемом меню "Параметры", выберите "Ресурсы сайта" и добавьте quickStatusApp.png `https://ServerName/sites/TestApps` изображение.    Щелкните правой кнопкой мыши элемент  **quickStatusApp,** выберите "Свойства" и скопируйте значение **адреса (URL-адреса)** в **диалоговом окне** "Свойства". Например, скопируйте и в paste значение в поле веб-адреса `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png` **URL-адреса значка.** Введите описание значка, например (как по рис. 9), введите значок приложения QuickStatus. Проверьте допустимый URL-адрес.
    
      **Рис. 9. Добавление URL-адреса значка для приложения QuickStatus**

      ![Установка свойств в SharePoint для приложения](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Установка свойств в SharePoint для приложения")
  
   4. Поле **Категория**: выберите существующую категорию или укажите свое значение. Например, введите Определение состояния.
    
      > [!NOTE]
      > Категория с именем **Определение состояния** предназначена только для тестирования. Типичная категория для приложения Project Server — **Управление проектами**. 
  
   5. Поле **Имя издателя**: введите имя издателя. В этом примере введите Project SDK.
    
   6. **Поле** "Включено". Чтобы сделать приложение видимым Project Web App администраторам сайтов для установки, выберите **этот** окне. 
    
   7. Дополнительные поля необязательны. Например, можно добавить URL-адрес службы поддержки и несколько изображений для страницы сведений о приложении. На рис. 9 поле **URL-адрес изображения 1** содержит URL-адрес снимка экрана приложения и его описание. 
    
   8. В **диалоговом окне "Приложения для SharePoint — QuickStatus.app"** выберите **"Сохранить".** На рисунке 9 элемент "Быстрое обновление состояния" в библиотеке "Приложения для  SharePoint" был выбран для  редактирования, поэтому на вкладке "ПРАВКА" ленты диалоговых окна можно выбрать "Проверить", чтобы завершить процесс (см. рис. 10).  
    
      **Рис. 10. Приложение QuickStatus добавлено в библиотеку приложений для SharePoint.**

      ![Приложение QuickStatus добавлено в SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Приложение QuickStatus добавлено в SharePoint")
  
9. В Project Web App меню  "Параметры" выберите "Добавить **приложение".** На странице "Ваши приложения" в области быстрого запуска выберите "Из вашей организации" и выберите "Сведения о приложении"  для приложения **"Быстрое обновление состояния".** На рисунке 11 показана страница сведений со значком приложения, снимком экрана и другими сведениями, добавленными на предыдущем шаге. 
    
   **Рис. 11. Использование страницы сведений о приложении "Quick Status Update" в Project Web App**

   ![Добавление приложения QuickStatus в Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Добавление приложения QuickStatus в Project Web App")
  
10. На странице сведений о быстром обновлении состояния выберите **"ДОБАВИТЬ ИТ".** Project Web App отображает диалоговое окно со списком операций, которые может выполнять приложение QuickStatus (см. рис. 12). Список операций является производным от элементов **AppPermissionRequest** в AppManifest.xml файла. 
    
    **Рис. 12. Проверка доверия приложению Quick Status**

    ![Проверка доверия для приложения QuickStatus](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Проверка доверия для приложения QuickStatus")
  
11. В **диалоговом окне "Доверять** ли вы быстрому обновлению состояния" выберите **"Доверять".** Приложение добавляется на страницу содержимого Project Web App сайта (см. рис. 13).
    
    **Рис. 13. Просмотр приложения "Quick Status" на странице "Контент сайта"**

    ![Просмотр приложения QuickStatus в контенте сайта](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Просмотр приложения QuickStatus в контенте сайта")
  
На странице "Контент сайта" щелкните значок **Quick Status Update**, чтобы запустить приложение.

> [!NOTE]
> Для дополнительных команд, которые предоставляют сведения о приложении, на странице  "Содержимое сайта" выберите область, содержаную имя быстрого обновления состояния и многопоковые (...). Вы можете просмотреть страницу "О приложении" для приложения, просмотреть страницу сведений о приложении, содержаную сведения об ошибках приложения, просмотреть страницу разрешений приложения или удалить приложение из Project Web App. 
  
На странице задач в Project Web App (см. рис. 14) кнопка **QuickStatus** должна быть включена на ленте. Если **кнопка "Быстрое** состояние" отключена, попробуйте действия, описанные в примечаительной заметке на рисунке 7. 

**Рис. 14. Запуск приложения QuickStatus на вкладке "ЗАДАЧИ"**

![Запуск приложения QuickStatus из вкладки "ЗАДАЧИ"](media/pj15_CreateStatusingApp_TasksRibbon.gif "Запуск приложения QuickStatus из вкладки "ЗАДАЧИ"")
  
В процедуре 6 показано несколько тестов для проверки приложения QuickStatus.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Тестирование приложения QuickStatus

Каждую операцию, которую пользователь может попробовать в приложении **QuickStatus,** следует протестировать в тестовой установке Project Server перед развертыванием приложения на производственном сервере или в производственном клиенте Project Online. Тестовая установка позволяет изменять и удалять назначения для пользователей, не влияя на фактические проекты. В тестирование также следует включить несколько пользователей с различными наборами разрешений, например администратора, руководителя проекта и участника группы. Тщательное тестирование поможет обнаружить изменения, которые необходимо внести в приложение, которые не были очевидны при тестировании во время разработки. В процедуре 6 показано всего несколько тестов для приложения **QuickStatus**, а полный исчерпывающий ряд проверок. 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>Процедура 6. Тестирование приложения QuickStatus

1. Запустите приложение **QuickStatus**, при этом у пользователя нет назначений. Приложения должно показать сообщение синим цветом в нижней части страницы, например **У имени пользователя нет назначений**.
    
   Нажмите кнопку **Update**, после чего сообщение изменится на зеленое сообщение **Assignments have been updated**.
    
   > [!NOTE]
   > Поведение приложения необходимо изменить, чтобы отключить кнопку **Update**, если назначений не существует. 
  
2. Запустите приложение, в котором у пользователя несколько назначений в различных проектах, при этом некоторые назначения не завершены. Обратите внимание на внешний вид приложения и выполните следующие действия (см. рис. 15).
    
   1. Функция **onGetAssignmentsSuccess** создает строку в таблице для каждого назначения текущего пользователя. Имя проекта показано только один раз полужирным шрифтом для первого назначения в каждом проекте. 
    
   2. Снимите флажок в заголовке столбца **Имя задачи**. Обработчик события щелчка заголовка таблицы снимает все другие флажки в строках задач. 
    
   3. Выберите все задачи. Обработчик события щелчка для каждой строки определяет, выбраны ли все строки, и, если это так, выбирает заголовок столбца **Имя задачи**. 
    
   4. Снимите все флажки еще раз и выберите одно назначение с оставшимися трудозатратами. Например, на рис. 15 показана задача T1 с 20 % оставшихся трудозатрат.
    
   5. В **текстовом поле "Установить процент завершения"** введите 80 и выберите **"Обновить".** Внизу страницы появится зеленое сообщение **Assignments have been updated**.
    
      **Рис. 15. Обновление назначения в приложении QuickStatus**

      ![Обновление назначения в приложении QuickStatus](media/pj15_CreateStatusingApp_Testing1Update.gif "Обновление назначения в приложении QuickStatus")
  
3. Выберите **"Обновить"** (см. рис. 16). Все задачи выбираются снова, а в верхней задаче показано, что 80 % завершено. 
    
      **Рис. 16. Обновление страницы "Quick Status Update"**

      ![Обновление страницы QuickStatus](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Обновление страницы QuickStatus")
  
4. Снимите все флажки и выберите другую задачу. Например, выберите **New task from PWA**. Оставьте поле **Set percent complete** пустым, удалите весь текст в столбце **% complete** для выбранной задачи, а затем нажмите **Update**. Так как оба поля пусты, приложение отображает красное сообщение об ошибке (см. рис. 17).
    
      **Рис. 17. Тестирование сообщения об ошибке**

      ![Проверка сообщения об ошибке](media/pj15_CreateStatusingApp_Testing3Error.gif "Проверка сообщения об ошибке")
  
5. Обновив предыдущую задачу до 80 % завершенной, а затем выберите **"Выход".** Функция **exitToPwa** изменяет расположение окна браузера на страницу "Задачи" в хост-приложении SharePoint (то есть URL-адрес изменяется на https://ServerName/pwa/Tasks.aspx) . На рисунке 18 показано, что задача **T1** и новая задача из **задачи PWA** показывают 80 % выполнения. 
    
      **Рис. 18. Проверка обновления задач в Project Web App**

      ![Проверка обновленных задач в Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Проверка обновленных задач в Project Web App")
  
6. Перед показом обновленного состояния в Project профессиональный 2013 изменения должны быть отправлены на утверждение, а затем утверждены руководителем проекта.
    
Тестирование показывает несколько изменений, которые необходимо внести в приложение **QuickStatus** для повышения удобства использования. Например:

- Следует реализовать дополнительные проверки ошибок и значений текстовых полей. В настоящее время пользователь может ввести нечисловое или отрицательное значение процента завершения, что приводит к сообщению об ошибке. Например, для отрицательного значения отображается сообщение об ошибке **Ошибка обновления назначений: PJClientCallableException: StatusingSetDataValueInvalid**.
    
- В сообщении об ошибке для пустых текстовых полей могут перечисляться проекты и задачи, а также номер строки.
    
- Сообщение об успешном выполнении может включать в себя список обновленных задач или, если функция **updateAssignments** выполнена успешно, она может обновить страниц автоматически и показать обновленные задачи или процентные значения другим цветом и полужирным шрифтом. 
    
- Чтобы избежать получения очень большой таблицы, в таблице назначений следует добавлять только задачи, выполненные не на 100 %. Или можно добавить параметр для отображения всех задач. Эту проблему также можно устранить, используя сетку на основе jQuery вместо таблицы, где вы легко можете реализовать фильтрацию и разбиения таблицы по страницам.
    
- Так как приложение **QuickStatus** не отправляет отчет о состоянии, значок **Quick Status** на вкладке **ЗАДАЧИ** ленты будет логичнее сделать первым значком в группе **ЗАДАЧИ**, а не последним значком в группе **Отправить**. 
    
- Так как функция **onGetAssignmentsSuccess** инициализирует текст кнопки **btnSubmitUpdate**, но другие текстовые значения кнопки инициализируются в HTML, страница остается в частично инициализированном состоянии при выполнении функции **getAssignments**. Кнопки на странице будут более согласованными, если текстовые значения инициализировать в HTML. 
    
Самое главное, подход, используемый приложением **QuickStatus**, где оно изменяет процент завершения для назначений, следует изменить в рабочем приложении. Дополнительные сведения см. в разделе [Дальнейшие действия](#pj15_StatusingApp_NextSteps). 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>Пример кода для приложения QuickStatus

### <a name="defaultaspx-file"></a>Файл Default.aspx.

В файле проекта  `Pages\Default.aspx` **QuickStatus** есть следующий код: 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a>Файл App.js.

В файле проекта  `Scripts\App.js` **QuickStatus** есть следующий код: 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a>Файл App.css

В файле проекта QuickStatus находится следующий код `Content\App.css` CSS:  
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a>Файл Elements.xml для ленты.

Следующее определение XML для кнопки, добавленной на вкладке **TASKS** на ленте, находится в файле проекта `RibbonQuickStatusAction\Elements.xml` **QuickStatus:** 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a>Файл AppManifest.xml

Ниже приведен XML-код для манифеста приложения проекта **QuickStatus**, содержащий две области запроса разрешений, которые необходимы для обновления состояния назначения пользователя в нескольких проектах: 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a>Файл AppIcon.png.

Полное решение Visual Studio для приложения **QuickStatus** содержит настраиваемые файл AppIcon.png. Решение будет включено в загрузку project 2013 SDK. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Дальнейшие действия

Приложение **QuickStatus** — относительно простой пример написания приложений, которые можно установить в Project Server 2013 и Project Online. В разделе [Тестирование приложения QuickStatus](#pj15_StatusingApp_Testing) перечислены несколько улучшений, которые могут сделать приложение более удобным. Приложение **QuickStatus** использует функции JavaScript для обновления состояния назначения для Project Web App. Однако изменение процента завершения назначения — нерекомендуемый метод для управления проектами. Другой подход состоит в обновлении фактической начальной даты и оставшейся длительности назначенных задач. Для обсуждения проблем см. ["Обновление лучше"](https://www.mpug.com/articles/update-better) в бюллетене MPUG. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>См. также

- [Задачи программирования Project Server](project-programming-tasks.md)
- [Надстройки SharePoint](https://msdn.microsoft.com/library/jj163230.aspx)
- [Управление обновлениями задач в Project Web App](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [Создание дополнительных действий для развертывания с надстройками SharePoint](https://msdn.microsoft.com/library/jj163954.aspx)
    

