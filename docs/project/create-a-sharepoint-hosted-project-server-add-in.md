---
title: Создание надстройки Project Server с размещением в SharePoint
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Из трех типов приложений, которые можно создать для Project Online (автоматическим размещением, размещением у поставщика и размещенных в SharePoint) приложения, размещенного в SharePoint — это простейшая для создания и развертывания.
ms.openlocfilehash: 7a74f5b3b848f3fa238051f5b9f9f563c38417b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399587"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>Создание надстройки Project Server с размещением в SharePoint

Из трех типов приложений, которые можно создать для Project Online (автоматическим размещением, размещением у поставщика и размещенных в SharePoint) приложения, размещенного в SharePoint — это простейшая для создания и развертывания. Приложение, размещаемое в SharePoint не требуют проверки подлинности OAuth и не использует Azure и требуют обслуживания локальный сайт для ресурсов, размещаемые у поставщика. Шаблон **приложения для SharePoint 2013** в Visual Studio — это удобный framework для разработки приложений, которые могут публикации и продается в магазин Office или развернут в частном каталоге приложений в SharePoint. 
  
В проекте отчеты о состоянии — это процесс, где участник группы можно использовать странице "задачи" в Project Web App для отправки состояния назначенных задач, такие как количество часов, потраченных каждый день недели, затраченное на работу над задачей. Владелец назначения (как правило, руководитель проекта) может утвердить или отклонить состояние. Если отображается состояние Утверждено, Project пересчитывает расписание. Приложение **QuickStatus** отображает назначенных задач, где пользователь может быстро обновить процент выполнения и отправка состояние выбранного назначений для утверждения. Несмотря на странице "задачи" в Project Web App дополнительные функциональные возможности, приложения **QuickStatus** приведен пример, который предоставляет упрощенный интерфейс. 
  
Приложение **QuickStatus** приведен пример для разработчиков; он не предназначен для использования в рабочей среде. Основным назначением — это пример разработки приложений для Project Online, не для создания приложения с полностью функциональным отчеты о состоянии. Лучший подход для определения состояния в разделе рекомендуемого [дальнейшие действия](#pj15_StatusingApp_NextSteps).
  
Общие сведения о отчеты о состоянии видеть [Ход выполнения задачи](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress). Дополнительные сведения о разработке надстроек для SharePoint и Project Server можно [надстройки SharePoint](https://msdn.microsoft.com/library/jj163230.aspx).

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Необходимые компоненты для создания приложения для Project Server 2013

Чтобы разработать относительно простого приложения, которые могут быть развернуты в Project Online и локальной установки Project Server 2013, можно использовать Napa, которой обеспечения среды online (en). Для более сложных приложений изменение ленты Project Web App и упрощения отладки во время разработки, можно использовать Visual Studio 2012 или Visual Studio 2013. Например при локальной установке, вы можете вручную проверить таблиц данных черновиков для изменения в базе данных Project Server. В этой статье показано, как выполнить разработки приложений с помощью Visual Studio.
  
Для разработки приложений Project Server с использованием Visual Studio требуются следующие компоненты:
  
- Проверьте, что на локальном компьютере разработчика установлены самые последние пакеты обновления и обновления Windows. Операционной системой может быть Windows 7, Windows 8, Windows Server 2008 или Windows Server 2012.
    
- Необходимо иметь компьютер с SharePoint Server 2013 и Project Server 2013 установлены, где настроен для изоляции приложений и sideloading приложений. Sideloading позволяет временно установить приложение для отладки Visual Studio. Можно использовать для локальной установки SharePoint и Project Server. Дополнительные сведения см [в локальной среде разработки приложений для SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).
    
   > [!NOTE]
   > Для локальной установки настройки изолированного приложения домена *до* создания корпоративном каталоге приложений. 
  
- На компьютере разработчика может быть удаленного компьютера, который имеет инструменты разработчика Office для Visual Studio 2012 установлены. Убедитесь, что вы установили наиболее поздней версии; в разделе *средства* из [файлов для загрузки приложения для Office и SharePoint](https://msdn.microsoft.com/office/apps/fp123627.aspx).
    
- Убедитесь, что экземпляр Project Web App можно будет использовать для разработки и тестирования доступен в браузере.
    
Для получения сведений об использовании средства online видеть [настроить среду разработки приложений для SharePoint на Office 365](https://msdn.microsoft.com/library/fp161179.aspx). Пошаговое руководство по построению простое приложение для Project Server с использованием online средств содержатся в разделе EPMSource серия блогов, [Создание первого приложения Project Server](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Создание приложения для Project Server с помощью Visual Studio

Office Developer Tools для Visual Studio 2012 включает в себя шаблон для приложений SharePoint, которые могут использоваться с Project Server 2013. При создании решения приложения решение включает в себя следующие файлы пользовательского кода:
  
- **AppManifest.xml** с параметрами для названия приложения, области запроса разрешений и другими свойствами. Процедура 1 содержит действия для установки свойств с помощью конструктора манифеста. 
    
- **Default.aspx** в папке "Страницы" — это главная страница приложения. В процедуре 2 показано добавление HTML5-контента для приложения **QuickStatus**. 
    
- **App.js** в папке Scripts — это основной файл пользовательского кода JavaScript. 3 описывается код JavaScript для приложения **QuickStatus** . 
    
   Если вы добавляете коммерческие элементы управления, такие как jQuery-based сетки или управляющий элемент выбора даты, можно добавить ссылки на дополнительные файлы JavaScript в файл Default.aspx.
    
- **App.css** в папке "Контент" — это основной файл для настраиваемых стилей CSS3. Процедура 2 и 3 процедуры содержат сведения о каскадных таблицах стилей (CSS) для приложения **QuickStatus**. В файл Default.aspx можно добавить ссылки на дополнительные CSS-файлы. 
    
- **AppIcon.png** в папке Images — это 96 x 96 значок, который отображает приложения в магазин Office и каталога приложений. 
    
Изменение ленты Project Web App, можно добавить настраиваемое действие ленты. В разделе [пример кода для приложения QuickStatus](#pj15_StatusingApp_Example) включает в себя полный код для изменения файлов Default.aspx, App.js, App.css, Elements.xml и файл AppManifest.xml. 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>Процедура 1. Создание проекта приложения в Visual Studio

1. Запустите Visual Studio 2012 с правами администратора и затем выберите **Новый проект** на начальной странице. 
    
2. В диалоговом окне **Создание проекта** разверните узлы **Шаблоны**, **Visual C#** и **Office/SharePoint**, а затем выберите пункт **Приложения**. В раскрывающемся списке целевой платформы, расположенном в верхней части центральной панели, выберите **.NET Framework 4.5**, а затем выберите **Приложение для SharePoint 2013** (см. рис. 1). 
    
3. В поле **имя** введите QuickStatus, перейдите к папке, где требуется сохранить приложение и нажмите кнопку **ОК**.
    
   **Рис. 1. Создание приложения Project Server в Visual Studio**

   ![Для создания проекта сервера приложений в Visual Studio] (media/pj15_CreateStatusingApp_NewProject.gif "Для создания проекта сервера приложений в Visual Studio")
  
4. В диалоговом окне **Создание приложения для SharePoint** заполните следующие три поля: 
    
   - В верхнем поле введите имя, которое будет приложения для отображения в Project Web App. Например введите быстрого обновления состояния.
    
   - Для сайта использовать для отладки введите URL-адрес экземпляра Project Web App. Например, введите `https://ServerName/ProjectServerName` (Замените _имя сервера_ и _ProjectServerName_ на собственные значения), а затем нажмите кнопку **Проверить**. Если все сделано правильно, Visual Studio отображает **успешное подключение**. Если вы получаете сообщение об ошибке, убедитесь, правильность URL-адрес Project Web App и что компьютер Project Server настроен для изоляции приложений и sideloading приложений. Для получения дополнительных сведений обратитесь к разделу [Необходимые условия для создания приложения для Project Server 2013](#pj15_StatusingApp_Prerequisites) . 
    
   - В раскрывающемся списке **Как разместить приложение для SharePoint?** выберите **Размещение в SharePoint**.
    
   > [!CAUTION]
   > Если вы по ошибке выбрали значение по умолчанию, **С размещением у поставщика**, Visual Studio создает два проекта в решении: **QuickStatus** и **QuickStatusWeb**. Если вы видите два проекта, удалите решение и начните заново. 
  
5. Нажмите кнопку **ОК** для создания решения **QuickStatus**, проекта **QuickStatus** и файлов по умолчанию. 
    
6. Откройте представление конструктора манифеста (например, дважды щелкните файл AppManifest.xml). На вкладке **Общие** в текстовом поле **Название** должно отобразиться имя приложения, введенное на шаге 4. Откройте вкладку **Разрешения**, чтобы добавить следующие запросы разрешений для приложения (см. рис. 2): 
    
   - В первой строке списка **Запросы разрешений** в столбце **Область** выберите **Определение состояния** в раскрывающемся списке. В столбце **Разрешения** выберите **SubmitStatus**.
    
   - Добавьте строку, где **Область** — это **Несколько проектов**, а **Разрешение** — **Чтение**.
    
   **Рис. 2. Установка области разрешений для приложения определения состояния**

   ![Установка области разрешений для приложения определения состояния] (media/pj15_CreateStatusingApp_PermissionScope.gif "Установка области разрешений для приложения определения состояния")
  
Приложение **QuickStatus** позволяет пользователю Project Web App для чтения назначения для этого пользователя из нескольких проектов, изменение назначения процент завершения и отправки обновления. Другие области запросов разрешений в раскрывающемся списке на рисунке 2 показано не являются обязательными для этого приложения. Области запроса разрешений являются разрешения, которые приложение запрашивает от имени пользователя. Если пользователь не имеет разрешения в Project Web App, приложение не выполняется. Приложение может иметь несколько области запроса разрешений, в том числе для других разрешений SharePoint, но должна быть минимально необходимый для использования функций приложения. Ниже перечислены области запроса разрешений, которые связаны с Project Server. 

- **Корпоративные ресурсы**: разрешения диспетчера ресурсов, для чтения или записи сведений о других пользователях Project Web App.
    
- **Несколько проектов**: чтение или запись в несколько проектов, для которых у пользователя есть запрашиваемые разрешения.
    
- **Project Server**: приложения пользователь должен иметь права администратора для Project Web App.
    
- **Отчеты**: чтение службы **ProjectData** OData для Project Web App (требуется только для входа разрешений для Project Web App). 
    
- **Один проект**: чтение или запись в проект, для которого у пользователя есть запрашиваемые разрешения.
    
- **Определение состояния**: отправка обновлений состояния назначений, таких как время работы, процент завершения и новых назначений.
    
- **Рабочий процесс**: если у пользователя есть разрешения для запуска рабочих процессов Project Server, приложение выполняется с повышенными привилегиями для рабочего процесса.
    
Дополнительные сведения об области запроса разрешений для Project Server 2013 обратитесь к разделу *приложения Project* в [обновления в Project 2013 для разработчиков](updates-for-developers-in-project-2013.md) и [разрешения для приложений в SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>Создание HTML-контента для приложения QuickStatus

Прежде чем начать создание кода HTML-контент, проектирование пользовательского интерфейса и взаимодействие с пользователем для приложения QuickStatus (на рисунке 3 показан пример завершенных страницы). Проект может также включать структуры функций JavaScript, которые взаимодействуют с HTML-код. Общие сведения см [UX design для приложений в SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).
  
**Рис. 3. Проект страницы приложения QuickStatus**

![Макет страницы приложения QuickStatus] (media/pj15_CreateStatusingApp_AfterRefresh.gif "Макет страницы приложения QuickStatus")
  
Приложение отображает имя в верхней части, а именно значение из элемента **Title** файла AppManifest.xml. 
  
По умолчанию страница использует HTML5. Ниже приведены стандартные HTML-элементы для основных объектов пользовательского интерфейса, которые содержатся в тексте страницы приложения **QuickStatus**: 
  
- Элемент **form** содержит все другие элементы пользовательского интерфейса. 
    
- Элемент **fieldset** создает контейнер и границу таблицы назначений, дочерний элемент **legend** предоставляет метку для контейнера. 
    
- Элемент **таблицы** содержит заголовок и только заголовок таблицы. Функции JavaScript измените заголовок таблицы и добавление строк для назначений. 
    
   > [!NOTE]
   > Чтобы легко добавить разбиение по страницам и сортировки, рабочее приложение, скорее всего, будет использовать коммерческий элемент управления сетки на основе jQuery вместо таблицы. 
  
   Таблица содержит имя проекта, имя задачи с флажок, фактические трудозатраты, завершена, оставшихся по трудозатратам и Дата окончания назначения. Функции JavaScript создать флажок и поле ввода текста для процент выполнения каждой задачи.
    
- Элемент **input** для текстового поля задает процента завершения всех выбранных назначений. 
    
- Элемент **button** отправляет изменения состояния. 
    
- Элемент **button** обновляет страницу. 
    
- Элемент **button** выполняет выход из приложения и возвращает к странице "задачи" в Project Web App. 
    
Текстовые поля и кнопка элементы нижней находятся в пределах элементов **div** , чтобы CSS можно легко управлять положение и внешний вид объектов пользовательского интерфейса. Функция JavaScript добавляется абзац в нижней части страницы, содержащий результаты для успех или сбой обновления состояния. 
  
### <a name="procedure-2-to-create-the-html-content"></a>Процедура 2. Создание HTML-контента

1. В Visual Studio откройте файл Default.aspx.
    
   Файл содержит два элемента **asp: Content** : элемент с `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` атрибут добавляется в заголовке страницы и элемент с `ContentPlaceHolderID="PlaceHolderMain"` атрибут размещается внутри элемента **body** страницы. 
    
2. В `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` управления для заголовка страницы, добавьте ссылку на файл PS.js на сервере Project Server. Для тестирования и отладки, можно использовать PS.debug.js. 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   Инфраструктура приложение использует `/_layouts/15/` виртуальный каталог для сайта SharePoint в службах IIS. — Это физического файла `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.
    
   > [!NOTE]
   > Перед развертыванием приложения для рабочей среды, удалить `.debug` из ссылок на сценарии для повышения производительности. 
  
3. В `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` управления для основной части страницы, удалите элемент созданный **div** и добавьте HTML-код для объектов пользовательского интерфейса. В **таблице** элемент содержит только строку заголовка. В столбце **Название задачи** включает в себя ввода управления "флажок". Текст для элемента **заголовка** заменяется **onGetUserNameSuccess** обратного вызова для функции **getUserInfo** в файле App.js. 
    
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
    
В процедуре 3 добавляет функции JavaScript назначения читать и создавать строк таблицы, а также изменение и обновление назначения процент завершения. Фактические действия более последовательной при разработке приложения, которых можно также создать некоторые из HTML-код, добавление и функции JavaScript и связанных с ними стили проверить изменить или добавить дополнительный код HTML и повторите попытку.

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>Создание функций JavaScript для приложения QuickStatus

Шаблон Visual Studio для приложений SharePoint включает в себя App.js файл, который содержит код инициализации по умолчанию, который возвращает контекст клиента SharePoint и демонстрируются основные получить и задать действия для страницы приложения. Пространство имен JavaScript для библиотеки SP.js со стороны клиента SharePoint — **пакет обновления**. Так как приложения Project Server с помощью библиотеки PS.js, приложение использует пространство имен **PS** для получения клиентского контекста и получить доступ к JSOM для Project Server. 
  
Функции JavaScript в приложении **QuickStatus** относятся следующие: 
  
- Обработчик событий документа **ready** выполняется, когда создается экземпляр объектной модели документов (DOM). Обработчик события **ready** выполняет следующие четыре действия. 
    
    1. Инициализирует глобальную переменную **projContext** с клиентским контекстом для Project Server JSOM и глобальную переменную **pwaWeb**. 
        
    2. Вызывает функцию **getUserInfo** для инициализации глобальной переменной **projUser**. 
        
    3. Вызывает функцию **getAssignments**, которая возвращает указанные данные назначения пользователю. 
        
    4. Привязывает обработчики событий щелчка к флажку заголовка таблицы, а также к флажкам в каждой строке таблицы. Обработчики событий щелчка управляют атрибутом **checked** флажков, когда пользователь устанавливает или снимает флажки в таблице. 
    
- Если функция **getAssignments** выполнена успешно, вызывается функция **onGetAssignmentsSuccess**. Эта функция вставляет строку в таблицу для каждого назначения, инициализирует элементы управления HTML в каждой строке, а затем инициализирует свойства нижней кнопки. 
    
- Обработчик события **onClick** для кнопки **Update** вызывает функцию **updateAssignments**. Она получает процент завершения, который применяется для каждого выбранного назначения. Если поле процента завершения пусто, функция возвращает процент завершения каждого выбранного назначения в таблице. Функция **updateAssignments** сохраняет и отправляет обновления состояния и записывает сообщение о результатах в нижнюю часть страницы. 
    
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

3. Добавьте функцию **getUserInfo**, которая вызывает **onGetUserNameSuccess** при успешном выполнении запроса. Функция **onGetUserNameSuccess** заменяет содержимое абзаца**caption** на название таблицы, которое содержит имя пользователя. 
    
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

4. Добавьте функцию **getAssignments**, которая вызывает **onGetAssignmentsSuccess** (см. шаг 5) при успешном выполнении запроса назначения. Параметр **Include** ограничивает запрос для возврата только указанных полей. 
    
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
   > JSOM не включает свойства **TimeSpan** , включает CSOM, такие как **ActualWorkTimeSpan**. Вместо этого JSOM с помощью свойства в миллисекундах, такие как [PS. StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) свойство. Метод для получения этого свойства — **получить\_actualWorkMilliseconds**, который возвращает значение типа integer. > **Get_actualWork** метод возвращает строку, например «3 h». Может использовать либо значение приложения **QuickStatus** , но по-разному их отображения. Запрос назначений включает оба свойства для проверки значения при отладке кода. При удалении переменной **actualWork** , можно также удалить свойство **ActualWork** в запрос назначений. 
  
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

7. Добавьте функцию **exitToPwa** , которая использует параметр строки запроса **SPHostUrl** для URL-адрес сайта Project Web App узла. Чтобы перейти к странице "задачи", добавьте `"/Tasks.aspx"` URL-адрес. Например, значение переменной **spHostUrl** `https://ServerName/ProjectServerName/Tasks.aspx`.
    
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

   Для предыдущего URL-адреса, функция **getQueryStringParameter** возвращает строковое значение запроса **SPHostUrl** `https://ServerName/pwa`. 
    
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

Если на этом этапе публикация приложения **QuickStatus** и добавление его в Project Web App, приложение может выполняться на странице контент сайта, но не легко доступным для пользователей. Чтобы помочь пользователям находить и запустите приложение, можно добавить кнопку для его на ленту на странице "задачи". 4 показано, как добавить настраиваемое действие ленты. 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>Добавление настраиваемого действия на ленте

Ленты вкладок, групп и элементов управления для Project Web App заданы в файле pwaribbon.xml, который устанавливается в `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` каталог на компьютере, где запущен Project Server. Для разработки настраиваемых действий для ленты Project Web App, загружаемого пакета Project 2013 SDK включает в себя копию pwaribbon.xml. 
  
Project Web App использует определения различных ленты на странице задач в зависимости от того, является ли экземпляр Project Web App использует режим одной операции, которая позволяет пользователям вводить значения для состояния расписания и задачи. При наличии разрешения администратора для Project Web App для определения режима операции, выберите в меню Параметры раскрывающийся список в правом верхнем углу страницы **Параметров веб-клиента Project** . На странице "Параметры веб-клиента Project" Выбор **параметров расписания и значения по умолчанию**и посмотрите на флажок **Режим одной операции** в нижней части страницы. 
  
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
> Общие сведения о добавлении дополнительных действий на ленту или в меню в приложении SharePoint видеть [создать настраиваемые действия для развертывания с помощью приложения для SharePoint](https://msdn.microsoft.com/library/jj163954.aspx). 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>Процедура 4. Добавление настраиваемого действия ленты на страницу "Задачи"

1. Проверка на ленте на странице "задачи" в Project Web App. Перейдите на вкладку **ЗАДАЧИ** на ленте и планированию и изменить его. Существует семь групп, таких как **Submit**, **задачи**и **периода**. Группа **Submit** имеет два элемента управления, кнопки **Сохранить** и **Отправить состояние** раскрывающееся меню. Можно добавить элемент управления в любом месте в группу, добавление группы с помощью нового элемента управления в любом месте на вкладке **ЗАДАЧИ** или добавьте другой вкладки ленты с пользовательских групп и элементов управления. В этом примере мы добавьте третья кнопка группе **Отправить** , где кнопки вызывает URL-адрес приложения **QuickStatus** . 
    
2. В области **Обозреватель решений** в Visual Studio щелкните правой кнопкой мыши проект **QuickStatus** и затем добавить новый элемент. В диалоговом окне **Добавление нового элемента** выберите **Настраиваемое действие ленты** (см). Например имя дополнительного действия RibbonQuickStatusAction и нажмите кнопку **Добавить**.
    
   **Рис. 4. Добавление настраиваемого действия ленты**

   ![Добавление настраиваемого действия ленты] (media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Добавление настраиваемого действия ленты")
  
3. На первой странице мастера **создания настраиваемого действия ленты** оставьте параметр **Хост-сайт** выбранным, выберите **Нет** в раскрывающемся списке в качестве области настраиваемого действия, а затем нажмите кнопку **Далее** (см. рис. 5). Элементы раскрывающихся списков относятся к SharePoint, а не к Project Server. Мы заменим большую часть созданного XML для настраиваемого действия, чтобы применить XML к Project Server. 
    
   **Рис. 5. Указание свойств для настраиваемого действия ленты**

   ![Указание свойств для дополнительного действия ленты] (media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Указание свойств для дополнительного действия ленты")
  
4. На следующей странице мастера **создания настраиваемого действия ленты** оставьте все значения параметров по умолчанию, а затем нажмите кнопку **Готово** (см. рис. 6). Visual Studio создаст папку **RibbonQuickStatusAction**, которая содержит файл Elements.xml. 
    
   **Рис. 6. Указание параметров для элемента управления "Кнопка"**

   ![Указание параметров для элемента управления button] (media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Указание параметров для элемента управления button")
  
5. Измените созданный по умолчанию код в файле Elements.xml для настраиваемого действия ленты. Ниже приведен XML-код по умолчанию.
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="https://schemas.microsoft.com/sharepoint/">
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
    
   2. Чтобы добавить элемент управления в группе **Отправить** , найдите первой группы в `Ribbon.ContextualTabs.MyWork.Home.Groups` семейства сайтов в файле pwaribbon.xml, который представляет собой элемент, который начинается, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`. Чтобы добавить дочерний элемент управления в группе **Отправить** , в следующем коде показан правильный атрибут **Location** элемента **CommandUIDefinition** в файле Elements.xml: 
    
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

       - Чтобы сделать кнопку третьего элемента управления в группе, **последовательности** атрибут может принимать значения выше, чем `Sequence="20"` значение существующего **Отправить состояние** управления (элемент **FlyoutAnchor** в pwaribbon.xml). В соответствии с соглашением телефонов последовательность, групп и элементов управления, `10, 20, 30, …`, что позволяет элементов для вставки в промежуточные позиции.
    
       - Атрибут **команда** задает команду для запуска в элемент **CommandUIHandler** (содержатся в следующих разделах шаг 5.d). Можно упростить имя команды для упрощения Далее разработчика. Например `Command="Invoke_QuickStatus"` проще, чем читать `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.
    
       - Атрибуты изображения укажите значок 16 x 16 пикселей и значок размером 32 x 32 пикселя для элемента управления кнопка. В файле Elements.xml по умолчанию `Image32by32="_layouts/15/images/placeholder32x32.png"` указывает оранжевый dot. Значки можно извлечь из карты файлы изображений (ps16x16.png и ps32x32.png), которые устанавливаются в `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` каталог на компьютере, где запущен Project Server. Например значок размером 32 x 32 пикселя на недоступность во втором столбце значки слева, а 10 строке из верхней части гиперкарты ps32x32.png (значок находится в конце девятая строки; 9 строк x 32 строка пикселей = 288 пикселей). 
    
       - Для отображения всплывающей подсказки для элемента управления "Кнопка" добавьте атрибуты **ToolTipTitle** и **ToolTipDescription**. 
    
    4. Измените атрибуты элемента **CommandUIHandler** . Например убедитесь, что атрибут **команду** совпадает значение атрибута **команды** для элемента **Button** . В атрибуте **CommandAction** `~appWebUrl` — это URL-адрес веб-страницы **QuickStatus** . Когда кнопки ленты вызывает приложения **QuickStatus** , маркер **{StandardTokens}** заменяется параметры URL-адреса, которые включают в себя **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**и **SPAppWebUrl **.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. В **обозревателе решений**откройте конструктор **Feature1.feature** и переместите элемент **RibbonQuickStatusAction** из области **Элементы в решении** в область **Элементы в компоненте**. При открытии конструктора **Package.package** элемент **RibbonQuickStatusAction** будет находиться в области **Элементы в пакете**. 
    
При разработке приложения и добавление кнопки ленты, обычно тестирование приложения и задайте точки останова в код JavaScript для отладки. Когда вы нажимаете клавишу **F5** , чтобы начать отладку, Visual Studio компилирует приложение, развертывает его на сайт, указанный в свойстве **URL-адрес сайта** проекта **QuickStatus** и отображает страницу с вопросом, будет ли вы доверяете приложению. Если продолжить работу и выйдите из приложения **QuickStatus** возвращает на странице "задачи" в Project Web App. 

> [!NOTE]
> На рисунке 7 показано, что отключена кнопка **Быстрого состояния** на вкладке **ЗАДАЧИ** на ленте. После многие отладки развертываний с помощью Visual Studio, элементов управления настраиваемой ленты, можно заблокировать при возобновлении отладки или развертывания опубликованного приложения на том же сервере тестирования. Чтобы активировать кнопку Удалить элемент **RibbonQuickStatusAction** в Visual Studio и создайте новое действие ленты, который имеет другое имя и идентификатор. Если, не помогает, попробуйте удалить приложения из экземпляра Project Web App тестирования и создайте приложение с идентификатором различных приложений. 
  
**Рис. 7. Просмотр подсказки отключенной кнопки "Quick Status"**

![Просмотр подсказки отключенной кнопки] (media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Просмотр подсказки отключенной кнопки")
  
В процедуре 5 показано, как развернуть и установить приложение **QuickStatus**. В процедуре 6 показаны некоторые дополнительные действия для тестирования приложения после его установки. 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>Развертывание приложения QuickStatus

Существует несколько способов развертывания приложения в веб-приложение SharePoint, такие как Project Web App. Какие развертывания используется зависит от того, требуется ли опубликовать приложение частном каталоге SharePoint или на общедоступном магазине Office и SharePoint установлен в локальной или является online аренды. 5 показано, как развернуть приложения **QuickStatus** локальная установка в в частном каталоге приложений. Дополнительные сведения можно [Установка приложений для SharePoint 2013 и управление ими](https://technet.microsoft.com/library/fp161232.aspx) и [Публикация приложений для SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> Для добавления приложения в каталог SharePoint требуются разрешения администратора SharePoint. 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>Процедура 5. Развертывание приложения QuickStatus

1. Сохраните все файлы в Visual Studio, а затем щелкните правой кнопкой мыши проект **QuickStatus** в **обозревателе решений** и выберите команду **Опубликовать**.
    
2. Так как приложение **QuickStatus** размещается в SharePoint, существует всего несколько вариантов публикации (см. рис. 8). В диалоговом окне **Публикация приложений для Office и SharePoint** нажмите кнопку **Готово**.
    
   **Рис. 8. Публикация приложения QuickStatus**

   ![С помощью мастера публикации] (media/pj15_CreateStatusingApp_PublishWizard.gif "С помощью мастера публикации")
  
3. Скопируйте файл QuickStatus.app из `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` каталога удобное каталог на локальном компьютере (или на компьютер SharePoint для локальной установки). 
    
4. В центре администрирования SharePoint выберите **Приложения** на панели быстрого запуска и щелкните **Управление каталогом приложений**.
    
5. Если каталог приложений не существует, создайте семейство сайтов для каталога приложений, выполнив в разделе *Настройка сайта каталога приложений для веб-приложения* в [управление каталогом приложений в SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).
    
   Если каталог приложений, перейдите в URL-адрес сайта на странице Управление каталогом приложений. Например, на следующем этапе будет сайт каталога приложений `https://ServerName/sites/TestApps`.
    
6. На странице каталога приложений выберите **Приложения для SharePoint** на панели быстрого запуска. На странице "Приложения для SharePoint" откройте вкладку **ФАЙЛЫ** на ленте и нажмите кнопку **Отправить документ**.
    
7. В диалоговом окне **Добавление документа** найдите файл QuickStatus.app, добавьте комментарии для версии, а затем нажмите **ОК**.
    
8. При добавлении приложения также можно добавить локальный сведения для описания приложения, значок и другие сведения. В диалоговом окне **приложения для SharePoint — QuickStatus.app** добавьте информацию, которая требуется для отображения приложения в коллекции веб-сайтов SharePoint. Например добавьте следующие сведения: 
    
   1. В поле **Краткое описание** : тип быстрого состояние тестовое приложение.
    
   2. В поле **Описание** : тип тестовое приложение для обновления процент выполнения задачи в нескольких проектов.
    
   3. **URL-адрес значка** поля: добавить изображения 96 x 96 пикселей для значок приложения в ресурсах сайта для каталога приложений. Например, перейдите к `https://ServerName/sites/TestApps` **контент сайта** выберите в раскрывающемся меню **параметров** , нажмите **Ресурсах сайта**, а затем добавьте изображение quickStatusApp.png. Щелкните правой кнопкой мыши элемент **quickStatusApp** , выберите **Свойства**и затем скопируйте значение **(URL-адреса)** в диалоговом окне **Свойства** . Например, скопируйте `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`и затем вставьте значение в поле адреса **URL-адрес значка** web. Введите описание для значка, например (как показано на рисунке 9), введите значок приложения QuickStatus. Проверьте, что URL-адрес.
    
      **Рис. 9. Добавление URL-адреса значка для приложения QuickStatus**

      ![Установка свойств в SharePoint для приложения] (media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Установка свойств в SharePoint для приложения")
  
   4. Поле " **Категория** ": нажмите кнопку существующей категории или указать собственное значение. Например введите отчеты о состоянии.
    
      > [!NOTE]
      > Категория с именем **Определение состояния** предназначена только для тестирования. Типичная категория для приложения Project Server — **Управление проектами**. 
  
   5. Поле **Имя издателя** : Введите имя издателя. В этом примере введите пакет SDK для Project.
    
   6. **Enabled** field: чтобы сделать видимой администраторам сайтов Project Web App для установки приложения, установите флажок **включено** . 
    
   7. Дополнительные поля необязательны. Например, можно добавить URL-адрес службы поддержки и несколько изображений для страницы сведений о приложении. На рис. 9 поле **URL-адрес изображения 1** содержит URL-адрес снимка экрана приложения и его описание. 
    
   8. В диалоговом окне **приложения для SharePoint — QuickStatus.app** выберите команду **Сохранить**. На рисунке 9 **Быстрого обновление состояния** элемента в приложениях для библиотеки SharePoint извлечен для редактирования, так далее вкладку **Правка** ленты поле диалоговое окно, выберите **Вернуть** для завершения процесса (см). 
    
      **Рис. 10. Приложение QuickStatus добавлено в библиотеку приложений для SharePoint.**

      ![Приложение QuickStatus добавляется в SharePoint] (media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Приложение QuickStatus добавляется в SharePoint")
  
9. В Project Web App в раскрывающемся меню **Параметры** выберите команду **Добавить приложение**. На странице "ваши приложения" в панели быстрого запуска выберите **Из вашей организации**и выберите **Сведения о приложениях** для **Быстрого обновления состояния** приложения. На рисунке 11 показаны страница сведений о значок приложения, снимок экрана и другие сведения, которые вы добавили в предыдущем шаге. 
    
   **Рис. 11. Использование страницы сведений о приложении "Quick Status Update" в Project Web App**

   ![Добавление приложения QuickStatus в Project Web App] (media/pj15_CreateStatusingApp_AddAppToPWA.gif "Добавление приложения QuickStatus в Project Web App")
  
10. На странице сведений о быстрого обновления состояния выберите **ADD IT**. Project Web App отображает диалоговое окно, в котором приведены операции, которые приложения QuickStatus может выполнять (см). Список операций является производным от **AppPermissionRequest** элементы в файле AppManifest.xml. 
    
    **Рис. 12. Проверка доверия приложению Quick Status**

    ![Проверка доверия для приложения QuickStatus] (media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Проверка доверия для приложения QuickStatus")
  
11. В диалоговом окне **Доверять быстрого обновления состояния** выберите **Доверия**. Приложение добавляется на страницу контент сайта Project Web App (см).
    
    **Рис. 13. Просмотр приложения "Quick Status" на странице "Контент сайта"**

    ![Просмотр приложения QuickStatus в контенте сайта] (media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Просмотр приложения QuickStatus в контенте сайта")
  
На странице "Контент сайта" щелкните значок **Quick Status Update**, чтобы запустить приложение.

> [!NOTE]
> Дополнительные команды, содержащие сведения об этом приложении, на странице контент сайта выберите области, которая содержит имя **Быстрого обновления состояния** и кнопку с многоточием (...). Можно просмотреть страницу о программе для приложения, просмотр страницы сведения о приложении, которое содержит сведения об ошибках приложения, просмотрите страницу разрешений приложения и удалить приложения из Project Web App. 
  
На странице "задачи" в Project Web App (см), кнопка **QuickStatus** должна быть включена на ленте. Если кнопка **Быстрого состояния** отключена, то действий, описанных в заметки на рисунке 7. 

**Рис. 14. Запуск приложения QuickStatus на вкладке "ЗАДАЧИ"**

![Запуск приложения QuickStatus из вкладки "ЗАДАЧИ"] (media/pj15_CreateStatusingApp_TasksRibbon.gif "Запуск приложения QuickStatus из вкладки \"ЗАДАЧИ\"")
  
В процедуре 6 показано несколько тестов для проверки приложения QuickStatus.

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>Тестирование приложения QuickStatus

Каждой операции, пользователь мог попытаться в приложении **QuickStatus** должно тестироваться на тестовой версии Project Server перед развертыванием приложения на рабочем сервере или на рабочий клиент из Project Online. Установка тестовой позволяет изменить и удалить назначения для пользователей без воздействия на фактический проектов. Тестирование следует также включает несколько пользователей, имеющих различных наборов разрешений, таких как администратор, руководитель проекта и член рабочей группы. Тщательное тестирование может помочь обнаружить изменения, должна создаваться в приложении, которые не были видимый в тестирование во время разработки. Процедура 6 приведены несколько тестов для приложения **QuickStatus** , но не включает исчерпывающий набор тестов. 
  
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
    
   5. В текстовом поле **Задайте процент выполнения** введите 80 и нажмите кнопку **обновления**. Внизу страницы следует показывать зеленой сообщение, **назначения обновлены**.
    
      **Рис. 15. Обновление назначения в приложении QuickStatus**

      ![Обновление назначения в приложении QuickStatus] (media/pj15_CreateStatusingApp_Testing1Update.gif "Обновление назначения в приложении QuickStatus")
  
3. Щелкните **Refresh** (см. рис. 16). Все задачи будут выбраны еще раз, а в верхней части будет показано, что задача завершена на 80 %. 
    
      **Рис. 16. Обновление страницы "Quick Status Update"**

      ![Обновление страницы QuickStatus] (media/pj15_CreateStatusingApp_Testing2Refresh.gif "Обновление страницы QuickStatus")
  
4. Снимите все флажки и выберите другую задачу. Например, выберите **New task from PWA**. Оставьте поле **Set percent complete** пустым, удалите весь текст в столбце **% complete** для выбранной задачи, а затем нажмите **Update**. Так как оба поля пусты, приложение отображает красное сообщение об ошибке (см. рис. 17).
    
      **Рис. 17. Тестирование сообщения об ошибке**

      ![Тестирование сообщения об ошибке] (media/pj15_CreateStatusingApp_Testing3Error.gif "Тестирование сообщения об ошибке")
  
5. Обновление предыдущей задаче 80% завершения и затем выберите команду **Выход**. Функция **exitToPwa** изменяется расположение окна браузера на странице "задачи" в ведущем приложении SharePoint (то есть, URL-адрес изменяется на https://ServerName/pwa/Tasks.aspx). На рисунке 18 показано, что задачи **T1** и задач **новую задачу из веб-клиента Project** Показать 80% завершения. 
    
      **Рис. 18. Проверка обновления задач в Project Web App**

      ![Проверка обновленных задач в Project Web App] (media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Проверка обновленных задач в Project Web App")
  
6. Перед в Project Professional 2013 отображается обновленный состояние, изменения необходимо быть отправить для утверждения и затем утвержденных руководителем проекта.
    
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

### <a name="defaultaspx-file"></a>Файл Default.aspx

Следующий код находится в `Pages\Default.aspx` файл **QuickStatus** проекта: 
  
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

### <a name="appjs-file"></a>Файл app.js

Следующий код находится в `Scripts\App.js` файл **QuickStatus** проекта: 
  
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

Приведенный ниже код CSS находится в `Content\App.css` файл **QuickStatus** проекта: 
  
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

### <a name="elementsxml-file-for-the-ribbon"></a>Файл Elements.XML для ленты

— Это следующее определение XML, добавлены кнопки на вкладке **ЗАДАЧИ** на ленте в `RibbonQuickStatusAction\Elements.xml` файл **QuickStatus** проекта: 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="https://schemas.microsoft.com/sharepoint/">
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

Ниже приведен XML-код для манифеста приложения **QuickStatus** проекта, который включает два области запроса разрешений, которые необходимы для обновления состояния назначения пользователя приложения в нескольких проектов. 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="https://schemas.microsoft.com/sharepoint/2012/app/manifest"
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

### <a name="appiconpng-file"></a>Файл AppIcon.png

Законченное решение Visual Studio для приложения **QuickStatus** включает в себя пользовательский файл AppIcon.png. Решение будет включен в пакет SDK для Project 2013 для загрузки. 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>Дальнейшие действия

Приложение **QuickStatus** является относительно простой пример того, как создавать приложения, которые можно установить на Project Server 2013 и Project Online. В разделе [Тестирование приложения QuickStatus](#pj15_StatusingApp_Testing) приведены несколько улучшений, которые могут быть выполнены для более удобной. Приложение **QuickStatus** использует функции JavaScript для обновления состояния назначения для Project Web App. Однако изменение назначения процент завершения не методика управления рекомендуемые проекта. Другим подходом будет обновлять фактическая дата начала и оставшаяся продолжительность свою задачу. Описание проблем см раздел [Обновление лучше](https://www.mpug.com/articles/update-better) информационный бюллетень MPUG. 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>См. также

- [Задачи программирования Project Server](project-programming-tasks.md)
- [Надстройки SharePoint](https://msdn.microsoft.com/library/jj163230.aspx)
- [Управление обновлениями задач в Project Web App](https://technet.microsoft.com/en-us/library/hh767481%28v=office.14%29.aspx)
- [Создание дополнительных действий для развертывания с надстройками SharePoint](https://msdn.microsoft.com/library/jj163954.aspx)
    

