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
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a><span data-ttu-id="3ce52-103">Создание надстройки Project Server с размещением в SharePoint</span><span class="sxs-lookup"><span data-stu-id="3ce52-103">Create a SharePoint-hosted Project Server add-in</span></span>

<span data-ttu-id="3ce52-104">Из трех типов приложений, которые можно создать для Project Online (автоматическим размещением, размещением у поставщика и размещенных в SharePoint) приложения, размещенного в SharePoint — это простейшая для создания и развертывания.</span><span class="sxs-lookup"><span data-stu-id="3ce52-104">Of the three types of apps that you can create for Project Online (autohosted, provider-hosted, and SharePoint-hosted), the SharePoint-hosted app is the simplest to create and deploy.</span></span> <span data-ttu-id="3ce52-105">Приложение, размещаемое в SharePoint не требуют проверки подлинности OAuth и не использует Azure и требуют обслуживания локальный сайт для ресурсов, размещаемые у поставщика.</span><span class="sxs-lookup"><span data-stu-id="3ce52-105">A SharePoint-hosted app does not require OAuth authentication, and does not use Azure or require maintenance of a local site for the provider-hosted resources.</span></span> <span data-ttu-id="3ce52-106">Шаблон **приложения для SharePoint 2013** в Visual Studio — это удобный framework для разработки приложений, которые могут публикации и продается в магазин Office или развернут в частном каталоге приложений в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3ce52-106">The **App for SharePoint 2013** template in Visual Studio is a convenient framework for developing apps that can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> 
  
<span data-ttu-id="3ce52-107">В проекте отчеты о состоянии — это процесс, где участник группы можно использовать странице "задачи" в Project Web App для отправки состояния назначенных задач, такие как количество часов, потраченных каждый день недели, затраченное на работу над задачей.</span><span class="sxs-lookup"><span data-stu-id="3ce52-107">In Project, statusing is a process where a team member can use the Tasks page in Project Web App to submit the status of an assigned task, such as the number of hours worked each day of a week spent working on the task.</span></span> <span data-ttu-id="3ce52-108">Владелец назначения (как правило, руководитель проекта) может утвердить или отклонить состояние.</span><span class="sxs-lookup"><span data-stu-id="3ce52-108">The assignment owner (usually the project manager) can approve or reject the status.</span></span> <span data-ttu-id="3ce52-109">Если отображается состояние Утверждено, Project пересчитывает расписание.</span><span class="sxs-lookup"><span data-stu-id="3ce52-109">When the status is approved, Project recalculates the schedule.</span></span> <span data-ttu-id="3ce52-110">Приложение **QuickStatus** отображает назначенных задач, где пользователь может быстро обновить процент выполнения и отправка состояние выбранного назначений для утверждения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-110">The **QuickStatus** app displays assigned tasks, where the user can quickly update percent complete and submit status of the selected assignments for approval.</span></span> <span data-ttu-id="3ce52-111">Несмотря на странице "задачи" в Project Web App дополнительные функциональные возможности, приложения **QuickStatus** приведен пример, который предоставляет упрощенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3ce52-111">Although the Tasks page in Project Web App has much more functionality, the **QuickStatus** app is an example that provides a simplified interface.</span></span> 
  
<span data-ttu-id="3ce52-112">Приложение **QuickStatus** приведен пример для разработчиков; он не предназначен для использования в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="3ce52-112">The **QuickStatus** app is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="3ce52-113">Основным назначением — это пример разработки приложений для Project Online, не для создания приложения с полностью функциональным отчеты о состоянии.</span><span class="sxs-lookup"><span data-stu-id="3ce52-113">The primary purpose is to show an example of app development for Project Online, not to create a fully functional statusing app.</span></span> <span data-ttu-id="3ce52-114">Лучший подход для определения состояния в разделе рекомендуемого [дальнейшие действия](#pj15_StatusingApp_NextSteps).</span><span class="sxs-lookup"><span data-stu-id="3ce52-114">For a better approach to statusing, see the recommendation in [Next steps](#pj15_StatusingApp_NextSteps).</span></span>
  
<span data-ttu-id="3ce52-115">Общие сведения о отчеты о состоянии видеть [Ход выполнения задачи](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span><span class="sxs-lookup"><span data-stu-id="3ce52-115">For general information about statusing, see [Task progress](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress).</span></span> <span data-ttu-id="3ce52-116">Дополнительные сведения о разработке надстроек для SharePoint и Project Server можно [надстройки SharePoint](https://msdn.microsoft.com/library/jj163230.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-116">For more information about developing add-ins for SharePoint and Project Server, see [SharePoint Add-ins](https://msdn.microsoft.com/library/jj163230.aspx).</span></span>

<span data-ttu-id="3ce52-117"><a name="pj15_StatusingApp_Prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-117"></span></span>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a><span data-ttu-id="3ce52-118">Необходимые компоненты для создания приложения для Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ce52-118">Prerequisites for creating an app for Project Server 2013</span></span>

<span data-ttu-id="3ce52-119">Чтобы разработать относительно простого приложения, которые могут быть развернуты в Project Online и локальной установки Project Server 2013, можно использовать Napa, которой обеспечения среды online (en).</span><span class="sxs-lookup"><span data-stu-id="3ce52-119">To develop relatively simple apps that can be deployed to Project Online or to an on-premises installation of Project Server 2013, you can use the Napa, which provide an online development environment.</span></span> <span data-ttu-id="3ce52-120">Для более сложных приложений изменение ленты Project Web App и упрощения отладки во время разработки, можно использовать Visual Studio 2012 или Visual Studio 2013.</span><span class="sxs-lookup"><span data-stu-id="3ce52-120">For more complex apps, modifying the Project Web App ribbon, and easier debugging during development, you can use Visual Studio 2012 or Visual Studio 2013.</span></span> <span data-ttu-id="3ce52-121">Например при локальной установке, вы можете вручную проверить таблиц данных черновиков для изменения в базе данных Project Server.</span><span class="sxs-lookup"><span data-stu-id="3ce52-121">For example, with an on-premises installation, you can manually check the Drafts datatables for changes in the Project Server database.</span></span> <span data-ttu-id="3ce52-122">В этой статье показано, как выполнить разработки приложений с помощью Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3ce52-122">This article shows how to do app development with Visual Studio.</span></span>
  
<span data-ttu-id="3ce52-123">Для разработки приложений Project Server с использованием Visual Studio требуются следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="3ce52-123">Development of Project Server apps with Visual Studio requires the following:</span></span>
  
- <span data-ttu-id="3ce52-p106">Проверьте, что на локальном компьютере разработчика установлены самые последние пакеты обновления и обновления Windows. Операционной системой может быть Windows 7, Windows 8, Windows Server 2008 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p106">Ensure that you have installed the most recent service packs and Windows updates on your local development computer. The operating system can be Windows 7, Windows 8, Windows Server 2008, or Windows Server 2012.</span></span>
    
- <span data-ttu-id="3ce52-126">Необходимо иметь компьютер с SharePoint Server 2013 и Project Server 2013 установлены, где настроен для изоляции приложений и sideloading приложений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-126">You must have a computer that has SharePoint Server 2013 and Project Server 2013 installed, where the computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="3ce52-127">Sideloading позволяет временно установить приложение для отладки Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3ce52-127">Sideloading enables Visual Studio to temporarily install the app for debugging.</span></span> <span data-ttu-id="3ce52-128">Можно использовать для локальной установки SharePoint и Project Server.</span><span class="sxs-lookup"><span data-stu-id="3ce52-128">You can use an on-premises installation of SharePoint and Project Server.</span></span> <span data-ttu-id="3ce52-129">Дополнительные сведения см [в локальной среде разработки приложений для SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-129">For more information, see [Set up an on-premises development environment for apps for SharePoint](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="3ce52-130">Для локальной установки настройки изолированного приложения домена *до* создания корпоративном каталоге приложений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-130">For an on-premises installation, configure an isolated app domain  *before*  you create a corporate app catalog.</span></span> 
  
- <span data-ttu-id="3ce52-131">На компьютере разработчика может быть удаленного компьютера, который имеет инструменты разработчика Office для Visual Studio 2012 установлены.</span><span class="sxs-lookup"><span data-stu-id="3ce52-131">The development computer can be a remote computer that has Office Developer Tools for Visual Studio 2012 installed.</span></span> <span data-ttu-id="3ce52-132">Убедитесь, что вы установили наиболее поздней версии; в разделе *средства* из [файлов для загрузки приложения для Office и SharePoint](https://msdn.microsoft.com/office/apps/fp123627.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-132">Ensure that you have installed the most recent version; see the  *Tools*  section of the [Apps for Office and SharePoint downloads](https://msdn.microsoft.com/office/apps/fp123627.aspx).</span></span>
    
- <span data-ttu-id="3ce52-133">Убедитесь, что экземпляр Project Web App можно будет использовать для разработки и тестирования доступен в браузере.</span><span class="sxs-lookup"><span data-stu-id="3ce52-133">Verify that the Project Web App instance you will be using for development and testing is accessible in the browser.</span></span>
    
<span data-ttu-id="3ce52-134">Для получения сведений об использовании средства online видеть [настроить среду разработки приложений для SharePoint на Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-134">For information about using the online tools, see [Set up an environment for developing apps for SharePoint on Office 365](https://msdn.microsoft.com/library/fp161179.aspx).</span></span> <span data-ttu-id="3ce52-135">Пошаговое руководство по построению простое приложение для Project Server с использованием online средств содержатся в разделе EPMSource серия блогов, [Создание первого приложения Project Server](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).</span><span class="sxs-lookup"><span data-stu-id="3ce52-135">For a walkthrough of building a simple app for Project Server that uses the online tools, see the EPMSource blog series, [Building your first Project Server app](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/).</span></span>

<span data-ttu-id="3ce52-136"><a name="pj15_StatusingApp_UsingVisualStudio"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-136"></span></span>

## <a name="using-visual-studio-to-create-a-project-server-app"></a><span data-ttu-id="3ce52-137">Создание приложения для Project Server с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ce52-137">Using Visual Studio to create a Project Server app</span></span>

<span data-ttu-id="3ce52-138">Office Developer Tools для Visual Studio 2012 включает в себя шаблон для приложений SharePoint, которые могут использоваться с Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3ce52-138">Office Developer Tools for Visual Studio 2012 includes a template for SharePoint apps that can be used with Project Server 2013.</span></span> <span data-ttu-id="3ce52-139">При создании решения приложения решение включает в себя следующие файлы пользовательского кода:</span><span class="sxs-lookup"><span data-stu-id="3ce52-139">When you create an app solution, the solution includes the following files for your custom code:</span></span>
  
- <span data-ttu-id="3ce52-p111">**AppManifest.xml** с параметрами для названия приложения, области запроса разрешений и другими свойствами. Процедура 1 содержит действия для установки свойств с помощью конструктора манифеста.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p111">**AppManifest.xml** includes settings for the app title, permission request scope, and other properties. Procedure 1 includes steps to set the properties by using the Manifest Designer.</span></span> 
    
- <span data-ttu-id="3ce52-p112">**Default.aspx** в папке "Страницы" — это главная страница приложения. В процедуре 2 показано добавление HTML5-контента для приложения **QuickStatus**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p112">**Default.aspx** in the Pages folder is the main page of the app. Procedure 2 shows how to add HTML5 content for the **QuickStatus** app.</span></span> 
    
- <span data-ttu-id="3ce52-144">**App.js** в папке Scripts — это основной файл пользовательского кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3ce52-144">**App.js** in the Scripts folder is the primary file for the custom JavaScript code.</span></span> <span data-ttu-id="3ce52-145">3 описывается код JavaScript для приложения **QuickStatus** .</span><span class="sxs-lookup"><span data-stu-id="3ce52-145">Procedure 3 explains the JavaScript code for the **QuickStatus** app.</span></span> 
    
   <span data-ttu-id="3ce52-146">Если вы добавляете коммерческие элементы управления, такие как jQuery-based сетки или управляющий элемент выбора даты, можно добавить ссылки на дополнительные файлы JavaScript в файл Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="3ce52-146">If you add commercial controls such as a jQuery-based grid or date picker, you can add references to additional JavaScript files in the Default.aspx file.</span></span>
    
- <span data-ttu-id="3ce52-p114">**App.css** в папке "Контент" — это основной файл для настраиваемых стилей CSS3. Процедура 2 и 3 процедуры содержат сведения о каскадных таблицах стилей (CSS) для приложения **QuickStatus**. В файл Default.aspx можно добавить ссылки на дополнительные CSS-файлы.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p114">**App.css** in the Content folder is the primary file for custom CSS3 styles. Procedure 2 and Procedure 3 include information about cascading style sheets (CSS) styles for the **QuickStatus** app. You can add references to additional CSS files in the Default.aspx file.</span></span> 
    
- <span data-ttu-id="3ce52-150">**AppIcon.png** в папке Images — это 96 x 96 значок, который отображает приложения в магазин Office и каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-150">**AppIcon.png** in the Images folder is the 96 x 96 icon that the app displays in the Office Store or the app catalog.</span></span> 
    
<span data-ttu-id="3ce52-151">Изменение ленты Project Web App, можно добавить настраиваемое действие ленты.</span><span class="sxs-lookup"><span data-stu-id="3ce52-151">To modify the Project Web App ribbon, you can add a ribbon custom action.</span></span> <span data-ttu-id="3ce52-152">В разделе [пример кода для приложения QuickStatus](#pj15_StatusingApp_Example) включает в себя полный код для изменения файлов Default.aspx, App.js, App.css, Elements.xml и файл AppManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3ce52-152">The [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section includes the complete code for the modified Default.aspx, App.js, App.css, Elements.xml, and AppManifest.xml files.</span></span> 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a><span data-ttu-id="3ce52-p116">Процедура 1. Создание проекта приложения в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ce52-p116">Procedure 1. To create an app project in Visual Studio</span></span>

1. <span data-ttu-id="3ce52-155">Запустите Visual Studio 2012 с правами администратора и затем выберите **Новый проект** на начальной странице.</span><span class="sxs-lookup"><span data-stu-id="3ce52-155">Run Visual Studio 2012 as an administrator, and then select **New Project** on the Start page.</span></span> 
    
2. <span data-ttu-id="3ce52-p117">В диалоговом окне **Создание проекта** разверните узлы **Шаблоны**, **Visual C#** и **Office/SharePoint**, а затем выберите пункт **Приложения**. В раскрывающемся списке целевой платформы, расположенном в верхней части центральной панели, выберите **.NET Framework 4.5**, а затем выберите **Приложение для SharePoint 2013** (см. рис. 1).</span><span class="sxs-lookup"><span data-stu-id="3ce52-p117">In the **New Project** dialog box, expand the **Templates**, **Visual C#**, and **Office/SharePoint** nodes, and then select **Apps**. Use the default **.NET Framework 4.5** in the target framework drop-down list at the top of the center pane, and then select **App for SharePoint 2013** (see Figure 1).</span></span> 
    
3. <span data-ttu-id="3ce52-158">В поле **имя** введите QuickStatus, перейдите к папке, где требуется сохранить приложение и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-158">In the **Name** field, type QuickStatus, browse to the location where you want to save the app, and then choose **OK**.</span></span>
    
   <span data-ttu-id="3ce52-159">**Рис. 1. Создание приложения Project Server в Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="3ce52-159">**Figure 1. Creating a Project Server app in Visual Studio**</span></span>

   <span data-ttu-id="3ce52-160">![Для создания проекта сервера приложений в Visual Studio] (media/pj15_CreateStatusingApp_NewProject.gif "Для создания проекта сервера приложений в Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="3ce52-160">![Creating a Project Server app in Visual Studio](media/pj15_CreateStatusingApp_NewProject.gif "Creating a Project Server app in Visual Studio")</span></span>
  
4. <span data-ttu-id="3ce52-161">В диалоговом окне **Создание приложения для SharePoint** заполните следующие три поля:</span><span class="sxs-lookup"><span data-stu-id="3ce52-161">In the **New app for SharePoint** dialog box, fill in the following three fields:</span></span> 
    
   - <span data-ttu-id="3ce52-162">В верхнем поле введите имя, которое будет приложения для отображения в Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-162">In the top text box, type the name that you want the app to display in Project Web App.</span></span> <span data-ttu-id="3ce52-163">Например введите быстрого обновления состояния.</span><span class="sxs-lookup"><span data-stu-id="3ce52-163">For example, type Quick Status Update.</span></span>
    
   - <span data-ttu-id="3ce52-164">Для сайта использовать для отладки введите URL-адрес экземпляра Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-164">For the site to use for debugging, type the URL of the Project Web App instance.</span></span> <span data-ttu-id="3ce52-165">Например, введите `https://ServerName/ProjectServerName` (Замените _имя сервера_ и _ProjectServerName_ на собственные значения), а затем нажмите кнопку **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-165">For example, type  `https://ServerName/ProjectServerName` (replacing  _ServerName_ and  _ProjectServerName_ with your own values), and then choose **Validate**.</span></span> <span data-ttu-id="3ce52-166">Если все сделано правильно, Visual Studio отображает **успешное подключение**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-166">If all goes well, Visual Studio shows **Connection successful**.</span></span> <span data-ttu-id="3ce52-167">Если вы получаете сообщение об ошибке, убедитесь, правильность URL-адрес Project Web App и что компьютер Project Server настроен для изоляции приложений и sideloading приложений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-167">If you get an error message, ensure that the Project Web App URL is correct and that the Project Server computer is configured for app isolation and sideloading of apps.</span></span> <span data-ttu-id="3ce52-168">Для получения дополнительных сведений обратитесь к разделу [Необходимые условия для создания приложения для Project Server 2013](#pj15_StatusingApp_Prerequisites) .</span><span class="sxs-lookup"><span data-stu-id="3ce52-168">For more information, see the [Prerequisites for creating an app for Project Server 2013](#pj15_StatusingApp_Prerequisites) section.</span></span> 
    
   - <span data-ttu-id="3ce52-169">В раскрывающемся списке **Как разместить приложение для SharePoint?** выберите **Размещение в SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-169">In the **How do you want to host your app for SharePoint** drop-down list, choose **SharePoint-hosted**.</span></span>
    
   > [!CAUTION]
   > <span data-ttu-id="3ce52-p120">Если вы по ошибке выбрали значение по умолчанию, **С размещением у поставщика**, Visual Studio создает два проекта в решении: **QuickStatus** и **QuickStatusWeb**. Если вы видите два проекта, удалите решение и начните заново.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p120">If you choose the default **Provider-hosted** project type by mistake, Visual Studio creates two projects in the solution: a **QuickStatus** project and a **QuickStatusWeb** project. If you see two projects, delete that solution and start again.</span></span> 
  
5. <span data-ttu-id="3ce52-172">Нажмите кнопку **ОК** для создания решения **QuickStatus**, проекта **QuickStatus** и файлов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ce52-172">Choose **OK** to create the **QuickStatus** solution, **QuickStatus** project, and default files.</span></span> 
    
6. <span data-ttu-id="3ce52-p121">Откройте представление конструктора манифеста (например, дважды щелкните файл AppManifest.xml). На вкладке **Общие** в текстовом поле **Название** должно отобразиться имя приложения, введенное на шаге 4. Откройте вкладку **Разрешения**, чтобы добавить следующие запросы разрешений для приложения (см. рис. 2):</span><span class="sxs-lookup"><span data-stu-id="3ce52-p121">Open the Manifest Designer view (for example, double-click the AppManifest.xml file). On the **General** tab, the **Title** text box should show the app name that you typed in step 4. Choose the **Permissions** tab to add the following permission requests for the app (see Figure 2):</span></span> 
    
   - <span data-ttu-id="3ce52-p122">В первой строке списка **Запросы разрешений** в столбце **Область** выберите **Определение состояния** в раскрывающемся списке. В столбце **Разрешения** выберите **SubmitStatus**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p122">In the first row of the **Permission requests** list, in the **Scope** column, choose **Statusing** in the drop-down list. In the **Permission** column, choose **SubmitStatus**.</span></span>
    
   - <span data-ttu-id="3ce52-178">Добавьте строку, где **Область** — это **Несколько проектов**, а **Разрешение** — **Чтение**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-178">Add a row where the **Scope** is **Multiple Projects** and the **Permission** is **Read**.</span></span>
    
   <span data-ttu-id="3ce52-179">**Рис. 2. Установка области разрешений для приложения определения состояния**</span><span class="sxs-lookup"><span data-stu-id="3ce52-179">**Figure 2. Setting the permission scope for a statusing app**</span></span>

   <span data-ttu-id="3ce52-180">![Установка области разрешений для приложения определения состояния] (media/pj15_CreateStatusingApp_PermissionScope.gif "Установка области разрешений для приложения определения состояния")</span><span class="sxs-lookup"><span data-stu-id="3ce52-180">![Setting the permission scope for a statusing app](media/pj15_CreateStatusingApp_PermissionScope.gif "Setting the permission scope for a statusing app")</span></span>
  
<span data-ttu-id="3ce52-181">Приложение **QuickStatus** позволяет пользователю Project Web App для чтения назначения для этого пользователя из нескольких проектов, изменение назначения процент завершения и отправки обновления.</span><span class="sxs-lookup"><span data-stu-id="3ce52-181">The **QuickStatus** app enables a Project Web App user to read assignments for that user from multiple projects, change the assignment percent complete, and submit the update.</span></span> <span data-ttu-id="3ce52-182">Другие области запросов разрешений в раскрывающемся списке на рисунке 2 показано не являются обязательными для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-182">The other permission request scopes shown in the drop-down list in Figure 2 are not required for this app.</span></span> <span data-ttu-id="3ce52-183">Области запроса разрешений являются разрешения, которые приложение запрашивает от имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ce52-183">The permission request scopes are the permissions that the app requests on behalf of the user.</span></span> <span data-ttu-id="3ce52-184">Если пользователь не имеет разрешения в Project Web App, приложение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ce52-184">If the user does not have those permissions in Project Web App, the app does not run.</span></span> <span data-ttu-id="3ce52-185">Приложение может иметь несколько области запроса разрешений, в том числе для других разрешений SharePoint, но должна быть минимально необходимый для использования функций приложения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-185">An app can have multiple permission request scopes, including those for other SharePoint permissions, but should have only the minimum necessary for the app functionality.</span></span> <span data-ttu-id="3ce52-186">Ниже перечислены области запроса разрешений, которые связаны с Project Server.</span><span class="sxs-lookup"><span data-stu-id="3ce52-186">Following are the permission request scopes that are related to Project Server:</span></span> 

- <span data-ttu-id="3ce52-187">**Корпоративные ресурсы**: разрешения диспетчера ресурсов, для чтения или записи сведений о других пользователях Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-187">**Enterprise Resources**: Resource manager permissions, to read or write information about other Project Web App users.</span></span>
    
- <span data-ttu-id="3ce52-188">**Несколько проектов**: чтение или запись в несколько проектов, для которых у пользователя есть запрашиваемые разрешения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-188">**Multiple Projects**: Read or write to more than one project, where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="3ce52-189">**Project Server**: приложения пользователь должен иметь права администратора для Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-189">**Project Server**: Requires the app user to have administrator permissions for Project Web App.</span></span>
    
- <span data-ttu-id="3ce52-190">**Отчеты**: чтение службы **ProjectData** OData для Project Web App (требуется только для входа разрешений для Project Web App).</span><span class="sxs-lookup"><span data-stu-id="3ce52-190">**Reporting**: Read the **ProjectData** OData service for Project Web App (requires only log on permission for Project Web App).</span></span> 
    
- <span data-ttu-id="3ce52-191">**Один проект**: чтение или запись в проект, для которого у пользователя есть запрашиваемые разрешения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-191">**Single Project**: Read or write to a project where the user has the permissions requested.</span></span>
    
- <span data-ttu-id="3ce52-192">**Определение состояния**: отправка обновлений состояния назначений, таких как время работы, процент завершения и новых назначений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-192">**Statusing**: Submit updates for status of assignments, such as times worked, percent complete, and new assignments.</span></span>
    
- <span data-ttu-id="3ce52-193">**Рабочий процесс**: если у пользователя есть разрешения для запуска рабочих процессов Project Server, приложение выполняется с повышенными привилегиями для рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="3ce52-193">**Workflow**: If the user has permission to run Project Server workflows, the app then runs with elevated permissions for the workflow.</span></span>
    
<span data-ttu-id="3ce52-194">Дополнительные сведения об области запроса разрешений для Project Server 2013 обратитесь к разделу *приложения Project* в [обновления в Project 2013 для разработчиков](updates-for-developers-in-project-2013.md) и [разрешения для приложений в SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-194">For more information about permission request scopes for Project Server 2013, see the  *Project apps*  section in [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md) and [App permissions in SharePoint 2013](https://msdn.microsoft.com/library/fp142383.aspx).</span></span>


<span data-ttu-id="3ce52-195"><a name="pj15_StatusingApp_HTML"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-195"></span></span>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a><span data-ttu-id="3ce52-196">Создание HTML-контента для приложения QuickStatus</span><span class="sxs-lookup"><span data-stu-id="3ce52-196">Creating the HTML content for the QuickStatus app</span></span>

<span data-ttu-id="3ce52-197">Прежде чем начать создание кода HTML-контент, проектирование пользовательского интерфейса и взаимодействие с пользователем для приложения QuickStatus (на рисунке 3 показан пример завершенных страницы).</span><span class="sxs-lookup"><span data-stu-id="3ce52-197">Before you start coding the HTML content, design the user interface and user experience for the QuickStatus app (Figure 3 shows an example of the completed page).</span></span> <span data-ttu-id="3ce52-198">Проект может также включать структуры функций JavaScript, которые взаимодействуют с HTML-код.</span><span class="sxs-lookup"><span data-stu-id="3ce52-198">A design can also include an outline of the JavaScript functions that interact with the HTML code.</span></span> <span data-ttu-id="3ce52-199">Общие сведения см [UX design для приложений в SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-199">For general information, see [UX design for apps in SharePoint 2013](https://msdn.microsoft.com/library/fp179934.aspx).</span></span>
  
<span data-ttu-id="3ce52-200">**Рис. 3. Проект страницы приложения QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="3ce52-200">**Figure 3. Design of the QuickStatus app page**</span></span>

<span data-ttu-id="3ce52-201">![Макет страницы приложения QuickStatus] (media/pj15_CreateStatusingApp_AfterRefresh.gif "Макет страницы приложения QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="3ce52-201">![Design of the QuickStatus app page](media/pj15_CreateStatusingApp_AfterRefresh.gif "Design of the QuickStatus app page")</span></span>
  
<span data-ttu-id="3ce52-202">Приложение отображает имя в верхней части, а именно значение из элемента **Title** файла AppManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3ce52-202">The app shows the display name at the top, which is the value of the **Title** element in AppManifest.xml.</span></span> 
  
<span data-ttu-id="3ce52-p125">По умолчанию страница использует HTML5. Ниже приведены стандартные HTML-элементы для основных объектов пользовательского интерфейса, которые содержатся в тексте страницы приложения **QuickStatus**:</span><span class="sxs-lookup"><span data-stu-id="3ce52-p125">By default, the page uses HTML5. Following are the standard HTML elements for the main UI objects that the **QuickStatus** app contains in the body of the page:</span></span> 
  
- <span data-ttu-id="3ce52-205">Элемент **form** содержит все другие элементы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3ce52-205">A **form** element contains all of the other UI elements.</span></span> 
    
- <span data-ttu-id="3ce52-206">Элемент **fieldset** создает контейнер и границу таблицы назначений, дочерний элемент **legend** предоставляет метку для контейнера.</span><span class="sxs-lookup"><span data-stu-id="3ce52-206">A **fieldset** element creates a container and border for the table of assignments; the child **legend** element provides a label for the container.</span></span> 
    
- <span data-ttu-id="3ce52-207">Элемент **таблицы** содержит заголовок и только заголовок таблицы.</span><span class="sxs-lookup"><span data-stu-id="3ce52-207">A **table** element includes a caption and only a table header.</span></span> <span data-ttu-id="3ce52-208">Функции JavaScript измените заголовок таблицы и добавление строк для назначений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-208">JavaScript functions change the table caption and add rows for the assignments.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="3ce52-209">Чтобы легко добавить разбиение по страницам и сортировки, рабочее приложение, скорее всего, будет использовать коммерческий элемент управления сетки на основе jQuery вместо таблицы.</span><span class="sxs-lookup"><span data-stu-id="3ce52-209">To easily add paging and sorting, a production app would probably use a commercial jQuery-based grid control instead of a table.</span></span> 
  
   <span data-ttu-id="3ce52-210">Таблица содержит имя проекта, имя задачи с флажок, фактические трудозатраты, завершена, оставшихся по трудозатратам и Дата окончания назначения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-210">The table includes columns for the project name, task name with a check box, actual work, percent complete, remaining work, and the assignment finish date.</span></span> <span data-ttu-id="3ce52-211">Функции JavaScript создать флажок и поле ввода текста для процент выполнения каждой задачи.</span><span class="sxs-lookup"><span data-stu-id="3ce52-211">JavaScript functions create the check box and the text input field for the percent complete of each task.</span></span>
    
- <span data-ttu-id="3ce52-212">Элемент **input** для текстового поля задает процента завершения всех выбранных назначений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-212">An **input** element for a text box sets percent complete for all selected assignments.</span></span> 
    
- <span data-ttu-id="3ce52-213">Элемент **button** отправляет изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="3ce52-213">A **button** element submits the status changes.</span></span> 
    
- <span data-ttu-id="3ce52-214">Элемент **button** обновляет страницу.</span><span class="sxs-lookup"><span data-stu-id="3ce52-214">A **button** element refreshes the page.</span></span> 
    
- <span data-ttu-id="3ce52-215">Элемент **button** выполняет выход из приложения и возвращает к странице "задачи" в Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-215">A **button** element exits the app and returns to the Tasks page in Project Web App.</span></span> 
    
<span data-ttu-id="3ce52-216">Текстовые поля и кнопка элементы нижней находятся в пределах элементов **div** , чтобы CSS можно легко управлять положение и внешний вид объектов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3ce52-216">The bottom text box and button elements are within **div** elements, so that CSS can easily manage the position and appearance of the UI objects.</span></span> <span data-ttu-id="3ce52-217">Функция JavaScript добавляется абзац в нижней части страницы, содержащий результаты для успех или сбой обновления состояния.</span><span class="sxs-lookup"><span data-stu-id="3ce52-217">A JavaScript function adds a paragraph at the bottom of the page that contains results for success or failure of the status update.</span></span> 
  
### <a name="procedure-2-to-create-the-html-content"></a><span data-ttu-id="3ce52-p129">Процедура 2. Создание HTML-контента</span><span class="sxs-lookup"><span data-stu-id="3ce52-p129">Procedure 2. To create the HTML content</span></span>

1. <span data-ttu-id="3ce52-220">В Visual Studio откройте файл Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="3ce52-220">In Visual Studio, open the Default.aspx file.</span></span>
    
   <span data-ttu-id="3ce52-221">Файл содержит два элемента **asp: Content** : элемент с `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` атрибут добавляется в заголовке страницы и элемент с `ContentPlaceHolderID="PlaceHolderMain"` атрибут размещается внутри элемента **body** страницы.</span><span class="sxs-lookup"><span data-stu-id="3ce52-221">The file includes two **asp:Content** elements: The element with the  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` attribute is added within the page header, and the element with the  `ContentPlaceHolderID="PlaceHolderMain"` attribute is placed within the page **body** element.</span></span> 
    
2. <span data-ttu-id="3ce52-222">В `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` управления для заголовка страницы, добавьте ссылку на файл PS.js на сервере Project Server.</span><span class="sxs-lookup"><span data-stu-id="3ce52-222">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` control for the page header, add a reference to the PS.js file on the Project Server computer.</span></span> <span data-ttu-id="3ce52-223">Для тестирования и отладки, можно использовать PS.debug.js.</span><span class="sxs-lookup"><span data-stu-id="3ce52-223">For testing and debugging, you can use PS.debug.js.</span></span> 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   <span data-ttu-id="3ce52-224">Инфраструктура приложение использует `/_layouts/15/` виртуальный каталог для сайта SharePoint в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="3ce52-224">The app infrastructure uses the `/_layouts/15/` virtual directory for the SharePoint site in IIS.</span></span> <span data-ttu-id="3ce52-225">— Это физического файла `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.</span><span class="sxs-lookup"><span data-stu-id="3ce52-225">The physical file is  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="3ce52-226">Перед развертыванием приложения для рабочей среды, удалить `.debug` из ссылок на сценарии для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="3ce52-226">Before you deploy the app for production use, remove  `.debug` from the script references to improve performance.</span></span> 
  
3. <span data-ttu-id="3ce52-227">В `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` управления для основной части страницы, удалите элемент созданный **div** и добавьте HTML-код для объектов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3ce52-227">In the  `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` control for the page body, delete the generated **div** element, and then add the HTML code for the UI objects.</span></span> <span data-ttu-id="3ce52-228">В **таблице** элемент содержит только строку заголовка.</span><span class="sxs-lookup"><span data-stu-id="3ce52-228">The **table** element contains only a header row.</span></span> <span data-ttu-id="3ce52-229">В столбце **Название задачи** включает в себя ввода управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="3ce52-229">The **Task name** column includes a check box input control.</span></span> <span data-ttu-id="3ce52-230">Текст для элемента **заголовка** заменяется **onGetUserNameSuccess** обратного вызова для функции **getUserInfo** в файле App.js.</span><span class="sxs-lookup"><span data-stu-id="3ce52-230">Text for the **caption** element is replaced by the **onGetUserNameSuccess** callback for the **getUserInfo** function in the App.js file.</span></span> 
    
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

4. <span data-ttu-id="3ce52-p133">В файле App.css добавьте код CSS, определяющий положение и внешний вид элементов пользовательского интерфейса. Полный код CSS приложения **QuickStatus** см. в разделе [Пример кода для приложения QuickStatus](#pj15_StatusingApp_Example).</span><span class="sxs-lookup"><span data-stu-id="3ce52-p133">In the App.css file, add CSS code for the position and appearance of the UI elements. For the complete CSS code of the **QuickStatus** app, see the [Example code for the QuickStatus app](#pj15_StatusingApp_Example) section.</span></span> 
    
<span data-ttu-id="3ce52-233">В процедуре 3 добавляет функции JavaScript назначения читать и создавать строк таблицы, а также изменение и обновление назначения процент завершения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-233">Procedure 3 adds the JavaScript functions to read the assignments and create the table rows, and to change and update the assignment percent complete.</span></span> <span data-ttu-id="3ce52-234">Фактические действия более последовательной при разработке приложения, которых можно также создать некоторые из HTML-код, добавление и функции JavaScript и связанных с ними стили проверить изменить или добавить дополнительный код HTML и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="3ce52-234">The actual steps are more iterative in developing an app, where you alternately create some of the HTML code, add and test related styles and JavaScript functions, modify or add more HTML code, and then repeat the process.</span></span>

<span data-ttu-id="3ce52-235"><a name="pj15_StatusingApp_JavaScript"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-235"></span></span>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a><span data-ttu-id="3ce52-236">Создание функций JavaScript для приложения QuickStatus</span><span class="sxs-lookup"><span data-stu-id="3ce52-236">Creating the JavaScript functions for the QuickStatus app</span></span>

<span data-ttu-id="3ce52-237">Шаблон Visual Studio для приложений SharePoint включает в себя App.js файл, который содержит код инициализации по умолчанию, который возвращает контекст клиента SharePoint и демонстрируются основные получить и задать действия для страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-237">The Visual Studio template for a SharePoint app includes the App.js file, which contains default initialization code that gets the SharePoint client context and demonstrates basic get and set actions for the app page.</span></span> <span data-ttu-id="3ce52-238">Пространство имен JavaScript для библиотеки SP.js со стороны клиента SharePoint — **пакет обновления**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-238">The JavaScript namespace for the SharePoint client-side SP.js library is **SP**.</span></span> <span data-ttu-id="3ce52-239">Так как приложения Project Server с помощью библиотеки PS.js, приложение использует пространство имен **PS** для получения клиентского контекста и получить доступ к JSOM для Project Server.</span><span class="sxs-lookup"><span data-stu-id="3ce52-239">Because a Project Server app uses the PS.js library, the app uses the **PS** namespace to get the client context and access the JSOM for Project Server.</span></span> 
  
<span data-ttu-id="3ce52-240">Функции JavaScript в приложении **QuickStatus** относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="3ce52-240">JavaScript functions in the **QuickStatus** app include the following:</span></span> 
  
- <span data-ttu-id="3ce52-p136">Обработчик событий документа **ready** выполняется, когда создается экземпляр объектной модели документов (DOM). Обработчик события **ready** выполняет следующие четыре действия.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p136">The document **ready** event handler runs when the document object model (DOM) is instantiated. The **ready** event handler does the following four steps:</span></span> 
    
    1. <span data-ttu-id="3ce52-243">Инициализирует глобальную переменную **projContext** с клиентским контекстом для Project Server JSOM и глобальную переменную **pwaWeb**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-243">Initializes the **projContext** global variable with the client context for the Project Server JSOM and the **pwaWeb** global variable.</span></span> 
        
    2. <span data-ttu-id="3ce52-244">Вызывает функцию **getUserInfo** для инициализации глобальной переменной **projUser**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-244">Calls the **getUserInfo** function to initialize the **projUser** global variable.</span></span> 
        
    3. <span data-ttu-id="3ce52-245">Вызывает функцию **getAssignments**, которая возвращает указанные данные назначения пользователю.</span><span class="sxs-lookup"><span data-stu-id="3ce52-245">Calls the **getAssignments** function, which gets specified assignment data for the user.</span></span> 
        
    4. <span data-ttu-id="3ce52-p137">Привязывает обработчики событий щелчка к флажку заголовка таблицы, а также к флажкам в каждой строке таблицы. Обработчики событий щелчка управляют атрибутом **checked** флажков, когда пользователь устанавливает или снимает флажки в таблице.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p137">Binds click event handlers to the table header check box, and to the check boxes in each row of the table. The click event handlers manage the **checked** attribute of the check boxes when the user selects or clears any check box in the table.</span></span> 
    
- <span data-ttu-id="3ce52-p138">Если функция **getAssignments** выполнена успешно, вызывается функция **onGetAssignmentsSuccess**. Эта функция вставляет строку в таблицу для каждого назначения, инициализирует элементы управления HTML в каждой строке, а затем инициализирует свойства нижней кнопки.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p138">If the **getAssignments** function is successful, it calls the **onGetAssignmentsSuccess** function. That function inserts a row in the table for each assignment, initializes the HTML controls in each row, and then initializes the bottom button properties.</span></span> 
    
- <span data-ttu-id="3ce52-p139">Обработчик события **onClick** для кнопки **Update** вызывает функцию **updateAssignments**. Она получает процент завершения, который применяется для каждого выбранного назначения. Если поле процента завершения пусто, функция возвращает процент завершения каждого выбранного назначения в таблице. Функция **updateAssignments** сохраняет и отправляет обновления состояния и записывает сообщение о результатах в нижнюю часть страницы.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p139">The **onClick** event handler for the **Update** button calls the **updateAssignments** function. That function gets the percent complete value that is applied to each selected assignment; or if the percent complete text box is empty, the function gets the percent complete of each selected assignment in the table. The **updateAssignments** function then saves and submits the status updates and writes a message about the results to the bottom of the page.</span></span> 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a><span data-ttu-id="3ce52-p140">Процедура 3. Создание функций JavaScript</span><span class="sxs-lookup"><span data-stu-id="3ce52-p140">Procedure 3. To create the JavaScript functions</span></span>

1. <span data-ttu-id="3ce52-255">В Visual Studio откройте файл App.js и удалите все его содержимое.</span><span class="sxs-lookup"><span data-stu-id="3ce52-255">In Visual Studio, open the App.js file, and then delete all the content in the file.</span></span>
    
2. <span data-ttu-id="3ce52-p141">Добавьте глобальные переменные и обработчик событий **ready**. Доступ к объекту **document** осуществляется с помощью функции jQuery.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p141">Add the global variables and the document **ready** event handler. The **document** object is accessed by using a jQuery function.</span></span> 
    
   <span data-ttu-id="3ce52-p142">Обработчик события щелчка для флажка заголовка таблицы задает состояние флажков строк. Если все флажки строки установлены или сняты, обработчик события щелчка задает установленное состояние флажка заголовка. Обработчики событий щелчка также задает результирующее сообщение в нижней части страницы как пустую строку.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p142">The click event handler for the table header check box sets the checked state of the row check boxes. If all of the row check boxes are selected or all are clear, the click event handler for the row check boxes sets the checked state of the header check box. The click event handlers also set the results message at the bottom of the page to an empty string.</span></span>
    
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

3. <span data-ttu-id="3ce52-p143">Добавьте функцию **getUserInfo**, которая вызывает **onGetUserNameSuccess** при успешном выполнении запроса. Функция **onGetUserNameSuccess** заменяет содержимое абзаца**caption** на название таблицы, которое содержит имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p143">Add the **getUserInfo** function, which calls **onGetUserNameSuccess** if the query is successful. The **onGetUserNameSuccess** function replaces the contents of the **caption** paragraph with a table caption that includes the user name.</span></span> 
    
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

4. <span data-ttu-id="3ce52-p144">Добавьте функцию **getAssignments**, которая вызывает **onGetAssignmentsSuccess** (см. шаг 5) при успешном выполнении запроса назначения. Параметр **Include** ограничивает запрос для возврата только указанных полей.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p144">Add the **getAssignments** function, which calls **onGetAssignmentsSuccess** (see step 5) if the assignment query is successful. The **Include** option limits the query to return only the fields specified.</span></span> 
    
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

5. <span data-ttu-id="3ce52-p145">Добавьте функцию **onGetAssignmentsSuccess**, которая добавляет строку для каждого назначения в таблицу. Переменная **prevProjName** используется для определения того, предназначена ли строка для другого проекта. В этом случае имя проекта отображается полужирным шрифтом, в противном случае имя проекта — это пустая строка.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p145">Add the **onGetAssignmentsSuccess** function, which adds a row for each assignment to the table. The **prevProjName** variable is used to determine whether a row is for a different project. If so, the project name is shown in a bold font; if not, the project name is set to an empty string.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="3ce52-268">JSOM не включает свойства **TimeSpan** , включает CSOM, такие как **ActualWorkTimeSpan**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-268">The JSOM does not include **TimeSpan** properties that the CSOM includes, such as **ActualWorkTimeSpan**.</span></span> <span data-ttu-id="3ce52-269">Вместо этого JSOM с помощью свойства в миллисекундах, такие как [PS. StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) свойство.</span><span class="sxs-lookup"><span data-stu-id="3ce52-269">Instead, the JSOM uses properties for the number of milliseconds, such as the [PS.StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) property.</span></span> <span data-ttu-id="3ce52-270">Метод для получения этого свойства — **получить\_actualWorkMilliseconds**, который возвращает значение типа integer.</span><span class="sxs-lookup"><span data-stu-id="3ce52-270">The method to get that property is **get\_actualWorkMilliseconds**, which returns an integer value.</span></span> <span data-ttu-id="3ce52-271">> **Get_actualWork** метод возвращает строку, например «3 h».</span><span class="sxs-lookup"><span data-stu-id="3ce52-271">> The **get_actualWork** method returns a string such as "3h".</span></span> <span data-ttu-id="3ce52-272">Может использовать либо значение приложения **QuickStatus** , но по-разному их отображения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-272">You could use either value in the **QuickStatus** app, but display it differently.</span></span> <span data-ttu-id="3ce52-273">Запрос назначений включает оба свойства для проверки значения при отладке кода.</span><span class="sxs-lookup"><span data-stu-id="3ce52-273">The assignments query includes both properties, so you can test the value during debugging.</span></span> <span data-ttu-id="3ce52-274">При удалении переменной **actualWork** , можно также удалить свойство **ActualWork** в запрос назначений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-274">If you remove the **actualWork** variable, you can also remove the **ActualWork** property in the assignments query.</span></span> 
  
   <span data-ttu-id="3ce52-p147">Наконец, функция **onGetAssignmentsSuccess** инициализирует кнопки **Update** и **Refresh** с обработчиками события щелчка. Текстовое значение кнопки **Update** кнопки можно задать в HTML-коде.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p147">Finally, the **onGetAssignmentsSuccess** function initializes the **Update** button and the **Refresh** button with click event handlers. The text value of the **Update** button could also be set in the HTML code.</span></span> 
    
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

6. <span data-ttu-id="3ce52-p148">Добавьте обработчик события щелчка **updateAssignments** для кнопки **Update**. Если пользователь изменяет процент завершения задачи или добавляет значение в текстовом поле **percentComplete**, значение можно ввести в различных форматах, например как "60", "60%" или "60 %". Метод **getNumericValue** возвращает введенный текст как числовое значение.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p148">Add the **updateAssignments** click event handler for the **Update** button. When the user changes a value for percent complete of a task, or adds a value in the **percentComplete** text box, the value could be entered in several formats such as "60", "60%", or "60 %". The **getNumericValue** method returns the numeric value of the input text.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="3ce52-280">В приложении для рабочей среды следует реализовать проверку вводимого текста и дополнительную проверку на наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="3ce52-280">In an app that is designed for production use, input values for numeric information should include field validation and additional error checking.</span></span> 
  
   <span data-ttu-id="3ce52-281">Пример **updateAssignments** применяет базовую проверку ошибок и отображает информацию в абзаце **message** в нижней части страницы — зеленым цветом, если запрос на обновление выполнен успешно, и красным цветом, если при вводе или выполнении запроса на обновление возникла ошибка.</span><span class="sxs-lookup"><span data-stu-id="3ce52-281">The **updateAssignments** example includes some basic error checking, and displays information in the **message** paragraph at the bottom of the page—green if the update query is successful and red if there is an input error or the update query is unsuccessful.</span></span> 
    
   <span data-ttu-id="3ce52-282">Перед использованием метода **submitAllStatusUpdates** приложение должно сохранить обновления на сервере с помощью метода **PS.StatusAssignmentCollection.update**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-282">Before using the **submitAllStatusUpdates** method, the app must save the updates to the server by using the **PS.StatusAssignmentCollection.update** method.</span></span> 
    
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

7. <span data-ttu-id="3ce52-283">Добавьте функцию **exitToPwa** , которая использует параметр строки запроса **SPHostUrl** для URL-адрес сайта Project Web App узла.</span><span class="sxs-lookup"><span data-stu-id="3ce52-283">Add the **exitToPwa** function, which uses the **SPHostUrl** query string parameter for the URL of the host Project Web App site.</span></span> <span data-ttu-id="3ce52-284">Чтобы перейти к странице "задачи", добавьте `"/Tasks.aspx"` URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="3ce52-284">To navigate back to the Tasks page, append  `"/Tasks.aspx"` to the URL.</span></span> <span data-ttu-id="3ce52-285">Например, значение переменной **spHostUrl** `https://ServerName/ProjectServerName/Tasks.aspx`.</span><span class="sxs-lookup"><span data-stu-id="3ce52-285">For example, the **spHostUrl** variable would be set to  `https://ServerName/ProjectServerName/Tasks.aspx`.</span></span>
    
   <span data-ttu-id="3ce52-p150">Функция **getQueryStringParameter** разбивает URL-адрес страницы **QuickStatus** для извлечения и возврата указанного параметра в параметрах URL-адреса. Ниже приведен пример значения **document.URL** для документа **QuickStatus** (все в одной строке):</span><span class="sxs-lookup"><span data-stu-id="3ce52-p150">The **getQueryStringParameter** function splits the URL of the **QuickStatus** page to extract and return the specified parameter in the URL options. Following is an example of the **document.URL** value for the **QuickStatus** document (all on one line):</span></span> 
    
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

   <span data-ttu-id="3ce52-288">Для предыдущего URL-адреса, функция **getQueryStringParameter** возвращает строковое значение запроса **SPHostUrl** `https://ServerName/pwa`.</span><span class="sxs-lookup"><span data-stu-id="3ce52-288">For the previous URL, the **getQueryStringParameter** function returns the **SPHostUrl** query string value,  `https://ServerName/pwa`.</span></span> 
    
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

<span data-ttu-id="3ce52-289">Если на этом этапе публикация приложения **QuickStatus** и добавление его в Project Web App, приложение может выполняться на странице контент сайта, но не легко доступным для пользователей.</span><span class="sxs-lookup"><span data-stu-id="3ce52-289">If you publish the **QuickStatus** app at this point and add it to Project Web App, the app can be run from the Site Contents page, but it is not easily available to users.</span></span> <span data-ttu-id="3ce52-290">Чтобы помочь пользователям находить и запустите приложение, можно добавить кнопку для его на ленту на странице "задачи".</span><span class="sxs-lookup"><span data-stu-id="3ce52-290">To help users find and run the app, you can add a button for it to the ribbon on the Tasks page.</span></span> <span data-ttu-id="3ce52-291">4 показано, как добавить настраиваемое действие ленты.</span><span class="sxs-lookup"><span data-stu-id="3ce52-291">Procedure 4 shows how to add a ribbon custom action.</span></span> 

<span data-ttu-id="3ce52-292"><a name="pj15_StatusingApp_ribbon"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-292"></span></span>

### <a name="adding-a-ribbon-custom-action"></a><span data-ttu-id="3ce52-293">Добавление настраиваемого действия на ленте</span><span class="sxs-lookup"><span data-stu-id="3ce52-293">Adding a ribbon custom action</span></span>

<span data-ttu-id="3ce52-294">Ленты вкладок, групп и элементов управления для Project Web App заданы в файле pwaribbon.xml, который устанавливается в `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` каталог на компьютере, где запущен Project Server.</span><span class="sxs-lookup"><span data-stu-id="3ce52-294">Ribbon tabs, groups, and controls for Project Web App are specified in the pwaribbon.xml file, which is installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` directory on the computer running Project Server.</span></span> <span data-ttu-id="3ce52-295">Для разработки настраиваемых действий для ленты Project Web App, загружаемого пакета Project 2013 SDK включает в себя копию pwaribbon.xml.</span><span class="sxs-lookup"><span data-stu-id="3ce52-295">To help design custom actions for the Project Web App ribbon, the Project 2013 SDK download includes a copy of pwaribbon.xml.</span></span> 
  
<span data-ttu-id="3ce52-296">Project Web App использует определения различных ленты на странице задач в зависимости от того, является ли экземпляр Project Web App использует режим одной операции, которая позволяет пользователям вводить значения для состояния расписания и задачи.</span><span class="sxs-lookup"><span data-stu-id="3ce52-296">Project Web App uses different ribbon definitions for the Tasks page, depending on whether the Project Web App instance uses single entry mode that enables users to enter values for both the timesheet and task status.</span></span> <span data-ttu-id="3ce52-297">При наличии разрешения администратора для Project Web App для определения режима операции, выберите в меню Параметры раскрывающийся список в правом верхнем углу страницы **Параметров веб-клиента Project** .</span><span class="sxs-lookup"><span data-stu-id="3ce52-297">If you have administrative permissions for Project Web App, to determine the entry mode, choose **PWA Settings** in the drop-down settings menu at the top-right corner of the page.</span></span> <span data-ttu-id="3ce52-298">На странице "Параметры веб-клиента Project" Выбор **параметров расписания и значения по умолчанию**и посмотрите на флажок **Режим одной операции** в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="3ce52-298">On the PWA Settings page, choose **Timesheet Settings and Defaults**, and then look at the **Single Entry Mode** check box at the bottom of the page.</span></span> 
  
<span data-ttu-id="3ce52-299">Если режим одной операции отключен, ленту на странице "Задачи" определяет область Моя работа в файле pwaribbon.xml:</span><span class="sxs-lookup"><span data-stu-id="3ce52-299">When single entry mode is off, the ribbon on the Tasks page is defined by the My Work region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

<span data-ttu-id="3ce52-300">Если режим одной операции включен, ленту на странице "Задачи" определяет область Связанный режим в файле pwaribbon.xml:</span><span class="sxs-lookup"><span data-stu-id="3ce52-300">When single entry mode is on, the Tasks page ribbon is defined by the Tied Mode region in pwaribbon.xml:</span></span> 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

<span data-ttu-id="3ce52-p154">Хотя группы и элементы управления в каждой области похожи друг на друга, элемент управления для связанного режима может вызывать функции, отличные от функций того же элемента управления в другом режиме. В процедуре 4 показано, как добавить элемент управления "Кнопка" для приложения **QuickStatus**, если режим одной операции выключен (флажок **Режим одной операции** не установлен).</span><span class="sxs-lookup"><span data-stu-id="3ce52-p154">Although the groups and controls in each region look similar, a control for the tied mode can call a different function than the same control for the non-tied mode. Procedure 4 shows how to add a button control for the **QuickStatus** app when single entry mode is off (the **Single Entry Mode** check box is clear).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3ce52-303">Общие сведения о добавлении дополнительных действий на ленту или в меню в приложении SharePoint видеть [создать настраиваемые действия для развертывания с помощью приложения для SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-303">For general information about adding custom actions to a ribbon or to a menu in a SharePoint application, see [Create custom actions to deploy with apps for SharePoint](https://msdn.microsoft.com/library/jj163954.aspx).</span></span> 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a><span data-ttu-id="3ce52-p155">Процедура 4. Добавление настраиваемого действия ленты на страницу "Задачи"</span><span class="sxs-lookup"><span data-stu-id="3ce52-p155">Procedure 4. To add a ribbon custom action to the Tasks page</span></span>

1. <span data-ttu-id="3ce52-306">Проверка на ленте на странице "задачи" в Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-306">Examine the ribbon on the Tasks page in Project Web App.</span></span> <span data-ttu-id="3ce52-307">Перейдите на вкладку **ЗАДАЧИ** на ленте и планированию и изменить его.</span><span class="sxs-lookup"><span data-stu-id="3ce52-307">Select the **TASKS** tab on the ribbon and plan how to modify it.</span></span> <span data-ttu-id="3ce52-308">Существует семь групп, таких как **Submit**, **задачи**и **периода**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-308">There are seven groups, such as **Submit**, **Tasks**, and **Period**.</span></span> <span data-ttu-id="3ce52-309">Группа **Submit** имеет два элемента управления, кнопки **Сохранить** и **Отправить состояние** раскрывающееся меню.</span><span class="sxs-lookup"><span data-stu-id="3ce52-309">The **Submit** group has two controls, a **Save** button and a **Send Status** drop-down menu.</span></span> <span data-ttu-id="3ce52-310">Можно добавить элемент управления в любом месте в группу, добавление группы с помощью нового элемента управления в любом месте на вкладке **ЗАДАЧИ** или добавьте другой вкладки ленты с пользовательских групп и элементов управления.</span><span class="sxs-lookup"><span data-stu-id="3ce52-310">You can add a control at any location in a group, add a group with a new control at any location in the **TASKS** tab, or add another ribbon tab that has custom groups and controls.</span></span> <span data-ttu-id="3ce52-311">В этом примере мы добавьте третья кнопка группе **Отправить** , где кнопки вызывает URL-адрес приложения **QuickStatus** .</span><span class="sxs-lookup"><span data-stu-id="3ce52-311">In this example, we add a third button to the **Submit** group, where the button invokes the URL of the **QuickStatus** app.</span></span> 
    
2. <span data-ttu-id="3ce52-312">В области **Обозреватель решений** в Visual Studio щелкните правой кнопкой мыши проект **QuickStatus** и затем добавить новый элемент.</span><span class="sxs-lookup"><span data-stu-id="3ce52-312">In the **Solution Explorer** pane in Visual Studio, right-click the **QuickStatus** project, and then add a new item.</span></span> <span data-ttu-id="3ce52-313">В диалоговом окне **Добавление нового элемента** выберите **Настраиваемое действие ленты** (см).</span><span class="sxs-lookup"><span data-stu-id="3ce52-313">In the **Add New Item** dialog box, choose **Ribbon Custom Action** (see Figure 4).</span></span> <span data-ttu-id="3ce52-314">Например имя дополнительного действия RibbonQuickStatusAction и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-314">For example, name the custom action RibbonQuickStatusAction, and then choose **Add**.</span></span>
    
   <span data-ttu-id="3ce52-315">**Рис. 4. Добавление настраиваемого действия ленты**</span><span class="sxs-lookup"><span data-stu-id="3ce52-315">**Figure 4. Adding a ribbon custom action**</span></span>

   <span data-ttu-id="3ce52-316">![Добавление настраиваемого действия ленты] (media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Добавление настраиваемого действия ленты")</span><span class="sxs-lookup"><span data-stu-id="3ce52-316">![Adding a ribbon custom action](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "Adding a ribbon custom action")</span></span>
  
3. <span data-ttu-id="3ce52-p158">На первой странице мастера **создания настраиваемого действия ленты** оставьте параметр **Хост-сайт** выбранным, выберите **Нет** в раскрывающемся списке в качестве области настраиваемого действия, а затем нажмите кнопку **Далее** (см. рис. 5). Элементы раскрывающихся списков относятся к SharePoint, а не к Project Server. Мы заменим большую часть созданного XML для настраиваемого действия, чтобы применить XML к Project Server.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p158">On the first page of the **Create Custom Action for Ribbon** wizard, leave the **Host Web** option selected, choose **None** in the drop-down list for the custom action scope, and then choose **Next** (see Figure 5). The items in the drop-down lists are relevant to SharePoint, not to Project Server. We will replace most of the generated XML for the custom action so that it applies to Project Server.</span></span> 
    
   <span data-ttu-id="3ce52-320">**Рис. 5. Указание свойств для настраиваемого действия ленты**</span><span class="sxs-lookup"><span data-stu-id="3ce52-320">**Figure 5. Specifying properties for the ribbon custom action**</span></span>

   <span data-ttu-id="3ce52-321">![Указание свойств для дополнительного действия ленты] (media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Указание свойств для дополнительного действия ленты")</span><span class="sxs-lookup"><span data-stu-id="3ce52-321">![Specifying properties for the ribbon custom action](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "Specifying properties for the ribbon custom action")</span></span>
  
4. <span data-ttu-id="3ce52-p159">На следующей странице мастера **создания настраиваемого действия ленты** оставьте все значения параметров по умолчанию, а затем нажмите кнопку **Готово** (см. рис. 6). Visual Studio создаст папку **RibbonQuickStatusAction**, которая содержит файл Elements.xml.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p159">On the next page of the **Create Custom Action for Ribbon** wizard, leave all the default values for the settings, and then choose **Finish** (see Figure 6). Visual Studio creates the **RibbonQuickStatusAction** folder, which contains an Elements.xml file.</span></span> 
    
   <span data-ttu-id="3ce52-324">**Рис. 6. Указание параметров для элемента управления "Кнопка"**</span><span class="sxs-lookup"><span data-stu-id="3ce52-324">**Figure 6. Specifying the settings for a button control**</span></span>

   <span data-ttu-id="3ce52-325">![Указание параметров для элемента управления button] (media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Указание параметров для элемента управления button")</span><span class="sxs-lookup"><span data-stu-id="3ce52-325">![Specifying the settings for a button control](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "Specifying the settings for a button control")</span></span>
  
5. <span data-ttu-id="3ce52-p160">Измените созданный по умолчанию код в файле Elements.xml для настраиваемого действия ленты. Ниже приведен XML-код по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p160">Modify the default generated code in the Elements.xml file for the ribbon custom action. Following is the default XML code:</span></span>
    
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

   1. <span data-ttu-id="3ce52-328">В элементе **CustomAction** удалите атрибуты **Sequence** и **Title**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-328">In the **CustomAction** element, delete the **Sequence** attribute and the **Title** attribute.</span></span> 
    
   2. <span data-ttu-id="3ce52-329">Чтобы добавить элемент управления в группе **Отправить** , найдите первой группы в `Ribbon.ContextualTabs.MyWork.Home.Groups` семейства сайтов в файле pwaribbon.xml, который представляет собой элемент, который начинается, `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`.</span><span class="sxs-lookup"><span data-stu-id="3ce52-329">To add a control to the **Submit** group, find the first group in the  `Ribbon.ContextualTabs.MyWork.Home.Groups` collection in the pwaribbon.xml file, which is the element that begins,  `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`.</span></span> <span data-ttu-id="3ce52-330">Чтобы добавить дочерний элемент управления в группе **Отправить** , в следующем коде показан правильный атрибут **Location** элемента **CommandUIDefinition** в файле Elements.xml:</span><span class="sxs-lookup"><span data-stu-id="3ce52-330">To add a child control to the **Submit** group, the following code shows the correct **Location** attribute of the **CommandUIDefinition** element in the Elements.xml file:</span></span> 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. <span data-ttu-id="3ce52-331">Измените значения атрибутов дочернего элемента **Button** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3ce52-331">Change the attribute values of the child **Button** element as follows:</span></span> 
    
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

       - <span data-ttu-id="3ce52-332">Чтобы сделать кнопку третьего элемента управления в группе, **последовательности** атрибут может принимать значения выше, чем `Sequence="20"` значение существующего **Отправить состояние** управления (элемент **FlyoutAnchor** в pwaribbon.xml).</span><span class="sxs-lookup"><span data-stu-id="3ce52-332">To make the button the third control in the group, the **Sequence** attribute can be any number higher than the  `Sequence="20"` value of the existing **Send Status** control (which is a **FlyoutAnchor** element in pwaribbon.xml).</span></span> <span data-ttu-id="3ce52-333">В соответствии с соглашением телефонов последовательность, групп и элементов управления, `10, 20, 30, …`, что позволяет элементов для вставки в промежуточные позиции.</span><span class="sxs-lookup"><span data-stu-id="3ce52-333">By convention, the sequence numbers of groups and controls are  `10, 20, 30, …`, which enables elements to be inserted in intermediate positions.</span></span>
    
       - <span data-ttu-id="3ce52-334">Атрибут **команда** задает команду для запуска в элемент **CommandUIHandler** (содержатся в следующих разделах шаг 5.d).</span><span class="sxs-lookup"><span data-stu-id="3ce52-334">The **Command** attribute specifies the command to run in the **CommandUIHandler** element (see the following step 5.d).</span></span> <span data-ttu-id="3ce52-335">Можно упростить имя команды для упрощения Далее разработчика.</span><span class="sxs-lookup"><span data-stu-id="3ce52-335">You can simplify the command name to make it easier for the next developer.</span></span> <span data-ttu-id="3ce52-336">Например `Command="Invoke_QuickStatus"` проще, чем читать `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.</span><span class="sxs-lookup"><span data-stu-id="3ce52-336">For example  `Command="Invoke_QuickStatus"` is easier to read than  `Command="Invoke_RibbonQuickStatusActionButtonRequest"`.</span></span>
    
       - <span data-ttu-id="3ce52-337">Атрибуты изображения укажите значок 16 x 16 пикселей и значок размером 32 x 32 пикселя для элемента управления кнопка.</span><span class="sxs-lookup"><span data-stu-id="3ce52-337">The image attributes specify the 16 x 16-pixel icon and the 32 x 32-pixel icon for the button control.</span></span> <span data-ttu-id="3ce52-338">В файле Elements.xml по умолчанию `Image32by32="_layouts/15/images/placeholder32x32.png"` указывает оранжевый dot.</span><span class="sxs-lookup"><span data-stu-id="3ce52-338">In the default Elements.xml file,  `Image32by32="_layouts/15/images/placeholder32x32.png"` specifies an orange dot.</span></span> <span data-ttu-id="3ce52-339">Значки можно извлечь из карты файлы изображений (ps16x16.png и ps32x32.png), которые устанавливаются в `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` каталог на компьютере, где запущен Project Server.</span><span class="sxs-lookup"><span data-stu-id="3ce52-339">You can extract icons from the image map files (ps16x16.png and ps32x32.png) that are installed in the  `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` directory on the computer running Project Server.</span></span> <span data-ttu-id="3ce52-340">Например значок размером 32 x 32 пикселя на недоступность во втором столбце значки слева, а 10 строке из верхней части гиперкарты ps32x32.png (значок находится в конце девятая строки; 9 строк x 32 строка пикселей = 288 пикселей).</span><span class="sxs-lookup"><span data-stu-id="3ce52-340">For example, the 32 x 32-pixel icon is in the second column of icons from the left and the tenth row down from the top of the ps32x32.png image map (the top of the icon is after the end of the ninth row; 9 rows x 32 pixels/row = 288 pixels).</span></span> 
    
       - <span data-ttu-id="3ce52-341">Для отображения всплывающей подсказки для элемента управления "Кнопка" добавьте атрибуты **ToolTipTitle** и **ToolTipDescription**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-341">To show a tool tip for the button control, add the **ToolTipTitle** attribute and the **ToolTipDescription** attribute.</span></span> 
    
    4. <span data-ttu-id="3ce52-342">Измените атрибуты элемента **CommandUIHandler** .</span><span class="sxs-lookup"><span data-stu-id="3ce52-342">Change the attributes of the **CommandUIHandler** element.</span></span> <span data-ttu-id="3ce52-343">Например убедитесь, что атрибут **команду** совпадает значение атрибута **команды** для элемента **Button** .</span><span class="sxs-lookup"><span data-stu-id="3ce52-343">For example, ensure that the **Command** attribute matches the **Command** attribute value for the **Button** element.</span></span> <span data-ttu-id="3ce52-344">В атрибуте **CommandAction** `~appWebUrl` — это URL-адрес веб-страницы **QuickStatus** .</span><span class="sxs-lookup"><span data-stu-id="3ce52-344">For the **CommandAction** attribute,  `~appWebUrl` is a placeholder for the URL of the **QuickStatus** webpage.</span></span> <span data-ttu-id="3ce52-345">Когда кнопки ленты вызывает приложения **QuickStatus** , маркер **{StandardTokens}** заменяется параметры URL-адреса, которые включают в себя **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**и \*\*SPAppWebUrl \*\*.</span><span class="sxs-lookup"><span data-stu-id="3ce52-345">When the ribbon button invokes the **QuickStatus** app, the **{StandardTokens}** token is replaced by URL options that include **SPHostUrl**, **SPLanguage**, **SPClientTag**, **SPProductNumber**, and **SPAppWebUrl**.</span></span>
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. <span data-ttu-id="3ce52-p166">В **обозревателе решений**откройте конструктор **Feature1.feature** и переместите элемент **RibbonQuickStatusAction** из области **Элементы в решении** в область **Элементы в компоненте**. При открытии конструктора **Package.package** элемент **RibbonQuickStatusAction** будет находиться в области **Элементы в пакете**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p166">In **Solution Explorer**, open the **Feature1.feature** designer, and move the **RibbonQuickStatusAction** item from the **Items in the Solution** pane to the **Items in the Feature** pane. If you then open the **Package.package** designer, the **RibbonQuickStatusAction** item will be in the **Items in the Package** pane.</span></span> 
    
<span data-ttu-id="3ce52-348">При разработке приложения и добавление кнопки ленты, обычно тестирование приложения и задайте точки останова в код JavaScript для отладки.</span><span class="sxs-lookup"><span data-stu-id="3ce52-348">As you develop the app and add a ribbon button, you normally test the app and set breakpoints in the JavaScript code for debugging.</span></span> <span data-ttu-id="3ce52-349">Когда вы нажимаете клавишу **F5** , чтобы начать отладку, Visual Studio компилирует приложение, развертывает его на сайт, указанный в свойстве **URL-адрес сайта** проекта **QuickStatus** и отображает страницу с вопросом, будет ли вы доверяете приложению.</span><span class="sxs-lookup"><span data-stu-id="3ce52-349">When you press **F5** to start debugging, Visual Studio compiles the app, deploys it to the site that is specified in the **Site URL** property of the **QuickStatus** project, and displays a page that asks whether you trust the app.</span></span> <span data-ttu-id="3ce52-350">Если продолжить работу и выйдите из приложения **QuickStatus** возвращает на странице "задачи" в Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-350">When you proceed and then exit the **QuickStatus** app, it returns to the Tasks page in Project Web App.</span></span> 

> [!NOTE]
> <span data-ttu-id="3ce52-351">На рисунке 7 показано, что отключена кнопка **Быстрого состояния** на вкладке **ЗАДАЧИ** на ленте.</span><span class="sxs-lookup"><span data-stu-id="3ce52-351">Figure 7 shows that the **Quick Status** button on the **TASKS** tab of the ribbon is disabled.</span></span> <span data-ttu-id="3ce52-352">После многие отладки развертываний с помощью Visual Studio, элементов управления настраиваемой ленты, можно заблокировать при возобновлении отладки или развертывания опубликованного приложения на том же сервере тестирования.</span><span class="sxs-lookup"><span data-stu-id="3ce52-352">After many debug deployments with Visual Studio, custom ribbon controls can be blocked when you continue to debug or deploy the published app on the same test server.</span></span> <span data-ttu-id="3ce52-353">Чтобы активировать кнопку Удалить элемент **RibbonQuickStatusAction** в Visual Studio и создайте новое действие ленты, который имеет другое имя и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3ce52-353">To enable the button, delete the **RibbonQuickStatusAction** item in Visual Studio, and then create a new ribbon action that has a different name and ID.</span></span> <span data-ttu-id="3ce52-354">Если, не помогает, попробуйте удалить приложения из экземпляра Project Web App тестирования и создайте приложение с идентификатором различных приложений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-354">If that doesn't solve the problem, try removing the app from the Project Web App test instance, and then recreate the app with a different app ID.</span></span> 
  
<span data-ttu-id="3ce52-355">**Рис. 7. Просмотр подсказки отключенной кнопки "Quick Status"**</span><span class="sxs-lookup"><span data-stu-id="3ce52-355">**Figure 7. Viewing the tooltip of the disabled Quick Status button**</span></span>

<span data-ttu-id="3ce52-356">![Просмотр подсказки отключенной кнопки] (media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Просмотр подсказки отключенной кнопки")</span><span class="sxs-lookup"><span data-stu-id="3ce52-356">![Viewing the tooltip of the disabled button](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "Viewing the tooltip of the disabled button")</span></span>
  
<span data-ttu-id="3ce52-p169">В процедуре 5 показано, как развернуть и установить приложение **QuickStatus**. В процедуре 6 показаны некоторые дополнительные действия для тестирования приложения после его установки.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p169">Procedure 5 shows how to deploy and install the **QuickStatus** app. Procedure 6 shows some additional steps in testing the app after you have installed it.</span></span> 

<span data-ttu-id="3ce52-359"><a name="pj15_StatusingApp_Deploying"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-359"></span></span>

## <a name="deploying-the-quickstatus-app"></a><span data-ttu-id="3ce52-360">Развертывание приложения QuickStatus</span><span class="sxs-lookup"><span data-stu-id="3ce52-360">Deploying the QuickStatus app</span></span>

<span data-ttu-id="3ce52-361">Существует несколько способов развертывания приложения в веб-приложение SharePoint, такие как Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-361">There are several ways to deploy an app to a SharePoint web application such as Project Web App.</span></span> <span data-ttu-id="3ce52-362">Какие развертывания используется зависит от того, требуется ли опубликовать приложение частном каталоге SharePoint или на общедоступном магазине Office и SharePoint установлен в локальной или является online аренды.</span><span class="sxs-lookup"><span data-stu-id="3ce52-362">Which deployment you use will depend on whether you want to publish the app to a private SharePoint catalog or to the public Office Store, and whether SharePoint is installed on-premises or is an online tenancy.</span></span> <span data-ttu-id="3ce52-363">5 показано, как развернуть приложения **QuickStatus** локальная установка в в частном каталоге приложений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-363">Procedure 5 shows how to deploy the **QuickStatus** app to an on-premises installation in a private app catalog.</span></span> <span data-ttu-id="3ce52-364">Дополнительные сведения можно [Установка приложений для SharePoint 2013 и управление ими](https://technet.microsoft.com/library/fp161232.aspx) и [Публикация приложений для SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ce52-364">For more information, see [Install and manage apps for SharePoint 2013](https://technet.microsoft.com/library/fp161232.aspx) and [Publish apps for SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)</span></span>
  
> [!NOTE]
> <span data-ttu-id="3ce52-365">Для добавления приложения в каталог SharePoint требуются разрешения администратора SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3ce52-365">Adding an app to a SharePoint catalog requires SharePoint administrator permissions.</span></span> 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a><span data-ttu-id="3ce52-p171">Процедура 5. Развертывание приложения QuickStatus</span><span class="sxs-lookup"><span data-stu-id="3ce52-p171">Procedure 5. To deploy the QuickStatus app</span></span>

1. <span data-ttu-id="3ce52-368">Сохраните все файлы в Visual Studio, а затем щелкните правой кнопкой мыши проект **QuickStatus** в **обозревателе решений** и выберите команду **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-368">In Visual Studio, save all of the files, and then right-click the **QuickStatus** project in the **Solution Explorer** and choose **Publish**.</span></span>
    
2. <span data-ttu-id="3ce52-p172">Так как приложение **QuickStatus** размещается в SharePoint, существует всего несколько вариантов публикации (см. рис. 8). В диалоговом окне **Публикация приложений для Office и SharePoint** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p172">Because the **QuickStatus** app is SharePoint-hosted, there are very few options for publishing (see Figure 8). In the **Publish apps for Office and SharePoint** dialog box, choose **Finish**.</span></span>
    
   <span data-ttu-id="3ce52-371">**Рис. 8. Публикация приложения QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="3ce52-371">**Figure 8. Publishing the QuickStatus app**</span></span>

   <span data-ttu-id="3ce52-372">![С помощью мастера публикации] (media/pj15_CreateStatusingApp_PublishWizard.gif "С помощью мастера публикации")</span><span class="sxs-lookup"><span data-stu-id="3ce52-372">![Using the Publish Wizard](media/pj15_CreateStatusingApp_PublishWizard.gif "Using the Publish Wizard")</span></span>
  
3. <span data-ttu-id="3ce52-373">Скопируйте файл QuickStatus.app из `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` каталога удобное каталог на локальном компьютере (или на компьютер SharePoint для локальной установки).</span><span class="sxs-lookup"><span data-stu-id="3ce52-373">Copy the QuickStatus.app file from the  `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` directory to a convenient directory on the local computer (or to the SharePoint computer for an on-premises installation).</span></span> 
    
4. <span data-ttu-id="3ce52-374">В центре администрирования SharePoint выберите **Приложения** на панели быстрого запуска и щелкните **Управление каталогом приложений**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-374">In SharePoint Central Administration, choose **Apps** in the Quick Launch, and then choose **Manage App Catalog**.</span></span>
    
5. <span data-ttu-id="3ce52-375">Если каталог приложений не существует, создайте семейство сайтов для каталога приложений, выполнив в разделе *Настройка сайта каталога приложений для веб-приложения* в [управление каталогом приложений в SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-375">If an app catalog does not exist, create a site collection for the app catalog, by following the  *Configure the App Catalog site for a web application*  section in [Manage the App Catalog in SharePoint 2013](https://technet.microsoft.com/library/fp161234.aspx).</span></span>
    
   <span data-ttu-id="3ce52-376">Если каталог приложений, перейдите в URL-адрес сайта на странице Управление каталогом приложений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-376">If an app catalog exists, navigate to the site URL on the Manage App Catalog page.</span></span> <span data-ttu-id="3ce52-377">Например, на следующем этапе будет сайт каталога приложений `https://ServerName/sites/TestApps`.</span><span class="sxs-lookup"><span data-stu-id="3ce52-377">For example, in the following steps, the app catalog site is  `https://ServerName/sites/TestApps`.</span></span>
    
6. <span data-ttu-id="3ce52-p174">На странице каталога приложений выберите **Приложения для SharePoint** на панели быстрого запуска. На странице "Приложения для SharePoint" откройте вкладку **ФАЙЛЫ** на ленте и нажмите кнопку **Отправить документ**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p174">On the app catalog page, choose **Apps for SharePoint** in the Quick Launch. On the Apps for SharePoint page, on the **FILES** tab of the ribbon, choose **Upload Document**.</span></span>
    
7. <span data-ttu-id="3ce52-380">В диалоговом окне **Добавление документа** найдите файл QuickStatus.app, добавьте комментарии для версии, а затем нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-380">In the **Add a document** dialog box, browse for the QuickStatus.app file, add comments for the version, and then choose **OK**.</span></span>
    
8. <span data-ttu-id="3ce52-381">При добавлении приложения также можно добавить локальный сведения для описания приложения, значок и другие сведения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-381">When you add an app, you can also add local information for the app description, icon, and other information.</span></span> <span data-ttu-id="3ce52-382">В диалоговом окне **приложения для SharePoint — QuickStatus.app** добавьте информацию, которая требуется для отображения приложения в коллекции веб-сайтов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3ce52-382">In the **Apps for SharePoint - QuickStatus.app** dialog box, add the information that you want to show for the app in the SharePoint site collection.</span></span> <span data-ttu-id="3ce52-383">Например добавьте следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="3ce52-383">For example, add the following information:</span></span> 
    
   1. <span data-ttu-id="3ce52-384">В поле **Краткое описание** : тип быстрого состояние тестовое приложение.</span><span class="sxs-lookup"><span data-stu-id="3ce52-384">**Short Description** field: Type Quick Status test app.</span></span>
    
   2. <span data-ttu-id="3ce52-385">В поле **Описание** : тип тестовое приложение для обновления процент выполнения задачи в нескольких проектов.</span><span class="sxs-lookup"><span data-stu-id="3ce52-385">**Description** field: Type Test app to update percent complete for tasks in multiple projects.</span></span>
    
   3. <span data-ttu-id="3ce52-386">**URL-адрес значка** поля: добавить изображения 96 x 96 пикселей для значок приложения в ресурсах сайта для каталога приложений.</span><span class="sxs-lookup"><span data-stu-id="3ce52-386">**Icon URL** fields: Add a 96 x 96-pixel image for the app icon to the site assets for the app catalog.</span></span> <span data-ttu-id="3ce52-387">Например, перейдите к `https://ServerName/sites/TestApps` **контент сайта** выберите в раскрывающемся меню **параметров** , нажмите **Ресурсах сайта**, а затем добавьте изображение quickStatusApp.png.</span><span class="sxs-lookup"><span data-stu-id="3ce52-387">For example, navigate to  `https://ServerName/sites/TestApps`, choose **Site contents** in the **Settings** drop-down menu, choose **Site Assets**, and then add the quickStatusApp.png image.</span></span> <span data-ttu-id="3ce52-388">Щелкните правой кнопкой мыши элемент **quickStatusApp** , выберите **Свойства**и затем скопируйте значение **(URL-адреса)** в диалоговом окне **Свойства** .</span><span class="sxs-lookup"><span data-stu-id="3ce52-388">Right-click the **quickStatusApp** item, choose **Properties**, and then copy the **Address (URL)** value in the **Properties** dialog box.</span></span> <span data-ttu-id="3ce52-389">Например, скопируйте `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`и затем вставьте значение в поле адреса **URL-адрес значка** web.</span><span class="sxs-lookup"><span data-stu-id="3ce52-389">For example, copy  `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`, and then paste the value in the **Icon URL** web address field.</span></span> <span data-ttu-id="3ce52-390">Введите описание для значка, например (как показано на рисунке 9), введите значок приложения QuickStatus.</span><span class="sxs-lookup"><span data-stu-id="3ce52-390">Type a description for the icon, for example (as in Figure 9), type QuickStatus app icon.</span></span> <span data-ttu-id="3ce52-391">Проверьте, что URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="3ce52-391">Test that the URL is valid.</span></span>
    
      <span data-ttu-id="3ce52-392">**Рис. 9. Добавление URL-адреса значка для приложения QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="3ce52-392">**Figure 9. Adding an icon URL for the QuickStatus app**</span></span>

      <span data-ttu-id="3ce52-393">![Установка свойств в SharePoint для приложения] (media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Установка свойств в SharePoint для приложения")</span><span class="sxs-lookup"><span data-stu-id="3ce52-393">![Setting properties in SharePoint for the app](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "Setting properties in SharePoint for the app")</span></span>
  
   4. <span data-ttu-id="3ce52-394">Поле " **Категория** ": нажмите кнопку существующей категории или указать собственное значение.</span><span class="sxs-lookup"><span data-stu-id="3ce52-394">**Category** field: Choose an existing category, or specify your own value.</span></span> <span data-ttu-id="3ce52-395">Например введите отчеты о состоянии.</span><span class="sxs-lookup"><span data-stu-id="3ce52-395">For example, type Statusing.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="3ce52-p178">Категория с именем **Определение состояния** предназначена только для тестирования. Типичная категория для приложения Project Server — **Управление проектами**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p178">A category named **Statusing** is just for testing purposes. A typical category for Project Server apps is **Project Management**.</span></span> 
  
   5. <span data-ttu-id="3ce52-398">Поле **Имя издателя** : Введите имя издателя.</span><span class="sxs-lookup"><span data-stu-id="3ce52-398">**Publisher name** field: Type the name of the publisher.</span></span> <span data-ttu-id="3ce52-399">В этом примере введите пакет SDK для Project.</span><span class="sxs-lookup"><span data-stu-id="3ce52-399">In this example, type Project SDK.</span></span>
    
   6. <span data-ttu-id="3ce52-400">**Enabled** field: чтобы сделать видимой администраторам сайтов Project Web App для установки приложения, установите флажок **включено** .</span><span class="sxs-lookup"><span data-stu-id="3ce52-400">**Enabled** field: To make the app visible to Project Web App site administrators for installation, select the **Enabled** check box.</span></span> 
    
   7. <span data-ttu-id="3ce52-p180">Дополнительные поля необязательны. Например, можно добавить URL-адрес службы поддержки и несколько изображений для страницы сведений о приложении. На рис. 9 поле **URL-адрес изображения 1** содержит URL-адрес снимка экрана приложения и его описание.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p180">Additional fields are optional. For example, you can add a support URL and multiple help images for the app details page. In Figure 9, the **Image URL 1** fields include the URL for a screenshot of the app and a description of the screenshot.</span></span> 
    
   8. <span data-ttu-id="3ce52-404">В диалоговом окне **приложения для SharePoint — QuickStatus.app** выберите команду **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-404">In the **Apps for SharePoint - QuickStatus.app** dialog box, choose **Save**.</span></span> <span data-ttu-id="3ce52-405">На рисунке 9 **Быстрого обновление состояния** элемента в приложениях для библиотеки SharePoint извлечен для редактирования, так далее вкладку **Правка** ленты поле диалоговое окно, выберите **Вернуть** для завершения процесса (см).</span><span class="sxs-lookup"><span data-stu-id="3ce52-405">In Figure 9, the **Quick Status Update** item in the Apps for SharePoint library is checked out for editing, so on the **EDIT** tab of the dialog box ribbon, you would choose **Check In** to complete the process (see Figure 10).</span></span> 
    
      <span data-ttu-id="3ce52-406">**Рис. 10. Приложение QuickStatus добавлено в библиотеку приложений для SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="3ce52-406">**Figure 10. The QuickStatus app is added to the Apps for SharePoint library.**</span></span>

      <span data-ttu-id="3ce52-407">![Приложение QuickStatus добавляется в SharePoint] (media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "Приложение QuickStatus добавляется в SharePoint")</span><span class="sxs-lookup"><span data-stu-id="3ce52-407">![The QuickStatus app is added to SharePoint](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "The QuickStatus app is added to SharePoint")</span></span>
  
9. <span data-ttu-id="3ce52-408">В Project Web App в раскрывающемся меню **Параметры** выберите команду **Добавить приложение**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-408">In Project Web App, in the **Settings** drop-down menu, choose **Add an app**.</span></span> <span data-ttu-id="3ce52-409">На странице "ваши приложения" в панели быстрого запуска выберите **Из вашей организации**и выберите **Сведения о приложениях** для **Быстрого обновления состояния** приложения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-409">On the Your Apps page, in the Quick Launch, choose **From Your Organization**, and then choose **App Details** for the **Quick Status Update** app.</span></span> <span data-ttu-id="3ce52-410">На рисунке 11 показаны страница сведений о значок приложения, снимок экрана и другие сведения, которые вы добавили в предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="3ce52-410">Figure 11 shows the details page with the app icon, screenshot, and other information that you added in the previous step.</span></span> 
    
   <span data-ttu-id="3ce52-411">**Рис. 11. Использование страницы сведений о приложении "Quick Status Update" в Project Web App**</span><span class="sxs-lookup"><span data-stu-id="3ce52-411">**Figure 11. Using the Quick Status Update details page in Project Web App**</span></span>

   <span data-ttu-id="3ce52-412">![Добавление приложения QuickStatus в Project Web App] (media/pj15_CreateStatusingApp_AddAppToPWA.gif "Добавление приложения QuickStatus в Project Web App")</span><span class="sxs-lookup"><span data-stu-id="3ce52-412">![Adding the QuickStatus app to Project Web App](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Adding the QuickStatus app to Project Web App")</span></span>
  
10. <span data-ttu-id="3ce52-413">На странице сведений о быстрого обновления состояния выберите **ADD IT**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-413">On the Quick Status Update details page, choose **ADD IT**.</span></span> <span data-ttu-id="3ce52-414">Project Web App отображает диалоговое окно, в котором приведены операции, которые приложения QuickStatus может выполнять (см).</span><span class="sxs-lookup"><span data-stu-id="3ce52-414">Project Web App displays a dialog box that lists the operations that the QuickStatus app can perform (see Figure 12).</span></span> <span data-ttu-id="3ce52-415">Список операций является производным от **AppPermissionRequest** элементы в файле AppManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3ce52-415">The list of operations is derived from the **AppPermissionRequest** elements in the AppManifest.xml file.</span></span> 
    
    <span data-ttu-id="3ce52-416">**Рис. 12. Проверка доверия приложению Quick Status**</span><span class="sxs-lookup"><span data-stu-id="3ce52-416">**Figure 12. Verifying that you trust the Quick Status app**</span></span>

    <span data-ttu-id="3ce52-417">![Проверка доверия для приложения QuickStatus] (media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Проверка доверия для приложения QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="3ce52-417">![Verifying trust for the QuickStatus app](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "Verifying trust for the QuickStatus app")</span></span>
  
11. <span data-ttu-id="3ce52-418">В диалоговом окне **Доверять быстрого обновления состояния** выберите **Доверия**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-418">In the **Do you trust Quick Status Update** dialog box, choose **Trust It**.</span></span> <span data-ttu-id="3ce52-419">Приложение добавляется на страницу контент сайта Project Web App (см).</span><span class="sxs-lookup"><span data-stu-id="3ce52-419">The app is added to the Project Web App Site Contents page (see Figure 13).</span></span>
    
    <span data-ttu-id="3ce52-420">**Рис. 13. Просмотр приложения "Quick Status" на странице "Контент сайта"**</span><span class="sxs-lookup"><span data-stu-id="3ce52-420">**Figure 13. Viewing the Quick Status app on the Site Contents page**</span></span>

    <span data-ttu-id="3ce52-421">![Просмотр приложения QuickStatus в контенте сайта] (media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Просмотр приложения QuickStatus в контенте сайта")</span><span class="sxs-lookup"><span data-stu-id="3ce52-421">![Viewing the QuickStatus app in Site Contents](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "Viewing the QuickStatus app in Site Contents")</span></span>
  
<span data-ttu-id="3ce52-422">На странице "Контент сайта" щелкните значок **Quick Status Update**, чтобы запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="3ce52-422">On the Site Contents page, you can select the **Quick Status Update** icon to run the app.</span></span>

> [!NOTE]
> <span data-ttu-id="3ce52-423">Дополнительные команды, содержащие сведения об этом приложении, на странице контент сайта выберите области, которая содержит имя **Быстрого обновления состояния** и кнопку с многоточием (...). Можно просмотреть страницу о программе для приложения, просмотр страницы сведения о приложении, которое содержит сведения об ошибках приложения, просмотрите страницу разрешений приложения и удалить приложения из Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-423">For additional commands that provide information about the app, on the Site Contents page, choose the region that contains the **Quick Status Update** name and the ellipsis (...). You can review the About page for the app, view the App Details page that contains information about app errors, review the app permissions page, or remove the app from Project Web App.</span></span> 
  
<span data-ttu-id="3ce52-424">На странице "задачи" в Project Web App (см), кнопка **QuickStatus** должна быть включена на ленте.</span><span class="sxs-lookup"><span data-stu-id="3ce52-424">On the Tasks page in Project Web App (see Figure 14), the **QuickStatus** button should be enabled on the ribbon.</span></span> <span data-ttu-id="3ce52-425">Если кнопка **Быстрого состояния** отключена, то действий, описанных в заметки на рисунке 7.</span><span class="sxs-lookup"><span data-stu-id="3ce52-425">If the **Quick Status** button is disabled, try the actions described in the note for Figure 7.</span></span> 

<span data-ttu-id="3ce52-426">**Рис. 14. Запуск приложения QuickStatus на вкладке "ЗАДАЧИ"**</span><span class="sxs-lookup"><span data-stu-id="3ce52-426">**Figure 14. Starting the QuickStatus app from the TASKS tab**</span></span>

<span data-ttu-id="3ce52-427">![Запуск приложения QuickStatus из вкладки "ЗАДАЧИ"] (media/pj15_CreateStatusingApp_TasksRibbon.gif "Запуск приложения QuickStatus из вкладки \"ЗАДАЧИ\"")</span><span class="sxs-lookup"><span data-stu-id="3ce52-427">![Starting the QuickStatus app from the TASKS tab](media/pj15_CreateStatusingApp_TasksRibbon.gif "Starting the QuickStatus app from the TASKS tab")</span></span>
  
<span data-ttu-id="3ce52-428">В процедуре 6 показано несколько тестов для проверки приложения QuickStatus.</span><span class="sxs-lookup"><span data-stu-id="3ce52-428">Procedure 6 shows some tests to make with the QuickStatus app.</span></span>

<span data-ttu-id="3ce52-429"><a name="pj15_StatusingApp_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-429"></span></span>

## <a name="testing-the-quickstatus-app"></a><span data-ttu-id="3ce52-430">Тестирование приложения QuickStatus</span><span class="sxs-lookup"><span data-stu-id="3ce52-430">Testing the QuickStatus app</span></span>

<span data-ttu-id="3ce52-431">Каждой операции, пользователь мог попытаться в приложении **QuickStatus** должно тестироваться на тестовой версии Project Server перед развертыванием приложения на рабочем сервере или на рабочий клиент из Project Online.</span><span class="sxs-lookup"><span data-stu-id="3ce52-431">Every operation that a user might try in the **QuickStatus** app should be tested on a test installation of Project Server before deploying the app to a production server or to a production tenant of Project Online.</span></span> <span data-ttu-id="3ce52-432">Установка тестовой позволяет изменить и удалить назначения для пользователей без воздействия на фактический проектов.</span><span class="sxs-lookup"><span data-stu-id="3ce52-432">A test installation enables you to change and delete assignments for users without affecting actual projects.</span></span> <span data-ttu-id="3ce52-433">Тестирование следует также включает несколько пользователей, имеющих различных наборов разрешений, таких как администратор, руководитель проекта и член рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="3ce52-433">Testing should also involve several users who have different sets of permissions, such as administrator, project manager, and team member.</span></span> <span data-ttu-id="3ce52-434">Тщательное тестирование может помочь обнаружить изменения, должна создаваться в приложении, которые не были видимый в тестирование во время разработки.</span><span class="sxs-lookup"><span data-stu-id="3ce52-434">Thorough testing can uncover changes that should be made in the app, which were not apparent in testing during development.</span></span> <span data-ttu-id="3ce52-435">Процедура 6 приведены несколько тестов для приложения **QuickStatus** , но не включает исчерпывающий набор тестов.</span><span class="sxs-lookup"><span data-stu-id="3ce52-435">Procedure 6 lists several tests for the **QuickStatus** app, but does not include an exhaustive series of tests.</span></span> 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a><span data-ttu-id="3ce52-p187">Процедура 6. Тестирование приложения QuickStatus</span><span class="sxs-lookup"><span data-stu-id="3ce52-p187">Procedure 6. To test the QuickStatus app</span></span>

1. <span data-ttu-id="3ce52-p188">Запустите приложение **QuickStatus**, при этом у пользователя нет назначений. Приложения должно показать сообщение синим цветом в нижней части страницы, например **У имени пользователя нет назначений**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p188">Run the **QuickStatus** app where the user has no assignments. The app should show a blue message at the bottom of the page, for example, **User Name has no assignments**.</span></span>
    
   <span data-ttu-id="3ce52-440">Нажмите кнопку **Update**, после чего сообщение изменится на зеленое сообщение **Assignments have been updated**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-440">Choose **Update**, and the message changes to a green **Assignments have been updated**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="3ce52-441">Поведение приложения необходимо изменить, чтобы отключить кнопку **Update**, если назначений не существует.</span><span class="sxs-lookup"><span data-stu-id="3ce52-441">The app behavior should be changed so that the **Update** button is disabled when there are no assignments.</span></span> 
  
2. <span data-ttu-id="3ce52-p189">Запустите приложение, в котором у пользователя несколько назначений в различных проектах, при этом некоторые назначения не завершены. Обратите внимание на внешний вид приложения и выполните следующие действия (см. рис. 15).</span><span class="sxs-lookup"><span data-stu-id="3ce52-p189">Run the app where the user has multiple assignments in several different projects and some assignments are not complete. Notice the appearance of the app and perform actions as follows (see Figure 15):</span></span>
    
   1. <span data-ttu-id="3ce52-p190">Функция **onGetAssignmentsSuccess** создает строку в таблице для каждого назначения текущего пользователя. Имя проекта показано только один раз полужирным шрифтом для первого назначения в каждом проекте.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p190">The **onGetAssignmentsSuccess** function creates a row in the table for each assignment for the current user. The project name shows only once, in a bold font, for the first assignment in each project.</span></span> 
    
   2. <span data-ttu-id="3ce52-p191">Снимите флажок в заголовке столбца **Имя задачи**. Обработчик события щелчка заголовка таблицы снимает все другие флажки в строках задач.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p191">Clear the check box in the **Task name** column header. The table header click event handler clears all of the other check boxes in the task rows.</span></span> 
    
   3. <span data-ttu-id="3ce52-p192">Выберите все задачи. Обработчик события щелчка для каждой строки определяет, выбраны ли все строки, и, если это так, выбирает заголовок столбца **Имя задачи**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p192">Select all of the tasks. The click event handler for each row determines whether all rows are selected, and if so, selects the **Task name** column header.</span></span> 
    
   4. <span data-ttu-id="3ce52-p193">Снимите все флажки еще раз и выберите одно назначение с оставшимися трудозатратами. Например, на рис. 15 показана задача T1 с 20 % оставшихся трудозатрат.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p193">Clear all of the check boxes again, and then select one assignment that has some remaining work. For example, Figure 15 shows the top task T1 has 20% remaining work to complete.</span></span>
    
   5. <span data-ttu-id="3ce52-452">В текстовом поле **Задайте процент выполнения** введите 80 и нажмите кнопку **обновления**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-452">In the **Set percent complete** text box, type 80, and then choose **Update**.</span></span> <span data-ttu-id="3ce52-453">Внизу страницы следует показывать зеленой сообщение, **назначения обновлены**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-453">The bottom of the page should show a green message, **Assignments have been updated**.</span></span>
    
      <span data-ttu-id="3ce52-454">**Рис. 15. Обновление назначения в приложении QuickStatus**</span><span class="sxs-lookup"><span data-stu-id="3ce52-454">**Figure 15. Updating an assignment in the QuickStatus app**</span></span>

      <span data-ttu-id="3ce52-455">![Обновление назначения в приложении QuickStatus] (media/pj15_CreateStatusingApp_Testing1Update.gif "Обновление назначения в приложении QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="3ce52-455">![Updating an assignment in the QuickStatus app](media/pj15_CreateStatusingApp_Testing1Update.gif "Updating an assignment in the QuickStatus app")</span></span>
  
3. <span data-ttu-id="3ce52-p195">Щелкните **Refresh** (см. рис. 16). Все задачи будут выбраны еще раз, а в верхней части будет показано, что задача завершена на 80 %.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p195">Choose **Refresh** (see Figure 16). All of the tasks are selected again, and the top task shows 80% complete.</span></span> 
    
      <span data-ttu-id="3ce52-458">**Рис. 16. Обновление страницы "Quick Status Update"**</span><span class="sxs-lookup"><span data-stu-id="3ce52-458">**Figure 16. Refreshing the Quick Status Update page**</span></span>

      <span data-ttu-id="3ce52-459">![Обновление страницы QuickStatus] (media/pj15_CreateStatusingApp_Testing2Refresh.gif "Обновление страницы QuickStatus")</span><span class="sxs-lookup"><span data-stu-id="3ce52-459">![Refreshing the QuickStatus page](media/pj15_CreateStatusingApp_Testing2Refresh.gif "Refreshing the QuickStatus page")</span></span>
  
4. <span data-ttu-id="3ce52-p196">Снимите все флажки и выберите другую задачу. Например, выберите **New task from PWA**. Оставьте поле **Set percent complete** пустым, удалите весь текст в столбце **% complete** для выбранной задачи, а затем нажмите **Update**. Так как оба поля пусты, приложение отображает красное сообщение об ошибке (см. рис. 17).</span><span class="sxs-lookup"><span data-stu-id="3ce52-p196">Clear all of the check boxes, and then select another task. For example, select **New task from PWA**. Leave the **Set percent complete** text box empty, delete all text in the **% complete** column for the selected task, and then choose **Update**. Because both text boxes are empty, the app shows a red error message (see Figure 17).</span></span>
    
      <span data-ttu-id="3ce52-464">**Рис. 17. Тестирование сообщения об ошибке**</span><span class="sxs-lookup"><span data-stu-id="3ce52-464">**Figure 17. Testing the error message**</span></span>

      <span data-ttu-id="3ce52-465">![Тестирование сообщения об ошибке] (media/pj15_CreateStatusingApp_Testing3Error.gif "Тестирование сообщения об ошибке")</span><span class="sxs-lookup"><span data-stu-id="3ce52-465">![Testing the error message](media/pj15_CreateStatusingApp_Testing3Error.gif "Testing the error message")</span></span>
  
5. <span data-ttu-id="3ce52-466">Обновление предыдущей задаче 80% завершения и затем выберите команду **Выход**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-466">Update the previous task to 80% complete, and then choose **Exit**.</span></span> <span data-ttu-id="3ce52-467">Функция **exitToPwa** изменяется расположение окна браузера на странице "задачи" в ведущем приложении SharePoint (то есть, URL-адрес изменяется на https://ServerName/pwa/Tasks.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ce52-467">The **exitToPwa** function changes the browser window location to the Tasks page in the SharePoint host application (that is, the URL changes to https://ServerName/pwa/Tasks.aspx).</span></span> <span data-ttu-id="3ce52-468">На рисунке 18 показано, что задачи **T1** и задач **новую задачу из веб-клиента Project** Показать 80% завершения.</span><span class="sxs-lookup"><span data-stu-id="3ce52-468">Figure 18 shows that the **T1** task and the **New task from PWA** task each show 80% complete.</span></span> 
    
      <span data-ttu-id="3ce52-469">**Рис. 18. Проверка обновления задач в Project Web App**</span><span class="sxs-lookup"><span data-stu-id="3ce52-469">**Figure 18. Verifying the tasks are updated in Project Web App**</span></span>

      <span data-ttu-id="3ce52-470">![Проверка обновленных задач в Project Web App] (media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Проверка обновленных задач в Project Web App")</span><span class="sxs-lookup"><span data-stu-id="3ce52-470">![Verifying the updated tasks in Project Web App](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Verifying the updated tasks in Project Web App")</span></span>
  
6. <span data-ttu-id="3ce52-471">Перед в Project Professional 2013 отображается обновленный состояние, изменения необходимо быть отправить для утверждения и затем утвержденных руководителем проекта.</span><span class="sxs-lookup"><span data-stu-id="3ce52-471">Before the updated status shows in Project Professional 2013, the changes must be submitted for approval, and then approved by the project manager.</span></span>
    
<span data-ttu-id="3ce52-p198">Тестирование показывает несколько изменений, которые необходимо внести в приложение **QuickStatus** для повышения удобства использования. Например:</span><span class="sxs-lookup"><span data-stu-id="3ce52-p198">Testing reveals several other changes that should be made in the **QuickStatus** app for improved usability. For example:</span></span>

- <span data-ttu-id="3ce52-p199">Следует реализовать дополнительные проверки ошибок и значений текстовых полей. В настоящее время пользователь может ввести нечисловое или отрицательное значение процента завершения, что приводит к сообщению об ошибке. Например, для отрицательного значения отображается сообщение об ошибке **Ошибка обновления назначений: PJClientCallableException: StatusingSetDataValueInvalid**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p199">There should be additional error checks and validation of text box values. Currently, a user can enter a non-numeric value or a negative value for percent complete, which results in an unfriendly error message. For example, with a negative value, the error message is **Error updating assignments: PJClientCallableException: StatusingSetDataValueInvalid**.</span></span>
    
- <span data-ttu-id="3ce52-477">В сообщении об ошибке для пустых текстовых полей могут перечисляться проекты и задачи, а также номер строки.</span><span class="sxs-lookup"><span data-stu-id="3ce52-477">The error message for blank text boxes could list the project and task, in addition to the row number.</span></span>
    
- <span data-ttu-id="3ce52-478">Сообщение об успешном выполнении может включать в себя список обновленных задач или, если функция **updateAssignments** выполнена успешно, она может обновить страниц автоматически и показать обновленные задачи или процентные значения другим цветом и полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="3ce52-478">The success message could include a list of the tasks updated; or if the **updateAssignments** function is successful, it could perform an automatic page refresh and show updated tasks or percentages in a different color and bold font.</span></span> 
    
- <span data-ttu-id="3ce52-p200">Чтобы избежать получения очень большой таблицы, в таблице назначений следует добавлять только задачи, выполненные не на 100 %. Или можно добавить параметр для отображения всех задач. Эту проблему также можно устранить, используя сетку на основе jQuery вместо таблицы, где вы легко можете реализовать фильтрацию и разбиения таблицы по страницам.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p200">To avoid a very large table, the table of assignments should be limited to tasks that are less than 100% complete. Or, add an option to show all tasks. This problem could also be solved by using a jQuery-based grid instead of a table, where you can easily implement filtering and grid paging.</span></span>
    
- <span data-ttu-id="3ce52-482">Так как приложение **QuickStatus** не отправляет отчет о состоянии, значок **Quick Status** на вкладке **ЗАДАЧИ** ленты будет логичнее сделать первым значком в группе **ЗАДАЧИ**, а не последним значком в группе **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="3ce52-482">Because the **QuickStatus** app does not submit status, the **Quick Status** icon on the **TASKS** tab of the ribbon would more logically be the first icon in the **Tasks** group, rather than the last icon in the **Submit** group.</span></span> 
    
- <span data-ttu-id="3ce52-p201">Так как функция **onGetAssignmentsSuccess** инициализирует текст кнопки **btnSubmitUpdate**, но другие текстовые значения кнопки инициализируются в HTML, страница остается в частично инициализированном состоянии при выполнении функции **getAssignments**. Кнопки на странице будут более согласованными, если текстовые значения инициализировать в HTML.</span><span class="sxs-lookup"><span data-stu-id="3ce52-p201">Because the **onGetAssignmentsSuccess** function initializes the **btnSubmitUpdate** button text, but the other button text values are initialized in HTML, the page is left in a partially initialized state while the **getAssignments** function runs. Buttons on the page would appear more consistent if the text values were all initialized in HTML.</span></span> 
    
<span data-ttu-id="3ce52-p202">Самое главное, подход, используемый приложением **QuickStatus**, где оно изменяет процент завершения для назначений, следует изменить в рабочем приложении. Дополнительные сведения см. в разделе [Дальнейшие действия](#pj15_StatusingApp_NextSteps).</span><span class="sxs-lookup"><span data-stu-id="3ce52-p202">Most importantly, the approach that the **QuickStatus** app uses, where it changes percent complete for assignments, should be revised in a production app. For more information, see the [Next steps](#pj15_StatusingApp_NextSteps) section.</span></span> 

<span data-ttu-id="3ce52-487"><a name="pj15_StatusingApp_Example"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-487"></span></span>

## <a name="example-code-for-the-quickstatus-app"></a><span data-ttu-id="3ce52-488">Пример кода для приложения QuickStatus</span><span class="sxs-lookup"><span data-stu-id="3ce52-488">Example code for the QuickStatus app</span></span>

### <a name="defaultaspx-file"></a><span data-ttu-id="3ce52-489">Файл Default.aspx</span><span class="sxs-lookup"><span data-stu-id="3ce52-489">Default.aspx file</span></span>

<span data-ttu-id="3ce52-490">Следующий код находится в `Pages\Default.aspx` файл **QuickStatus** проекта:</span><span class="sxs-lookup"><span data-stu-id="3ce52-490">The following code is in the  `Pages\Default.aspx` file of the **QuickStatus** project:</span></span> 
  
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

### <a name="appjs-file"></a><span data-ttu-id="3ce52-491">Файл app.js</span><span class="sxs-lookup"><span data-stu-id="3ce52-491">App.js file</span></span>

<span data-ttu-id="3ce52-492">Следующий код находится в `Scripts\App.js` файл **QuickStatus** проекта:</span><span class="sxs-lookup"><span data-stu-id="3ce52-492">The following code is in the  `Scripts\App.js` file of the **QuickStatus** project:</span></span> 
  
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

### <a name="appcss-file"></a><span data-ttu-id="3ce52-493">Файл App.css</span><span class="sxs-lookup"><span data-stu-id="3ce52-493">App.css file</span></span>

<span data-ttu-id="3ce52-494">Приведенный ниже код CSS находится в `Content\App.css` файл **QuickStatus** проекта:</span><span class="sxs-lookup"><span data-stu-id="3ce52-494">The following CSS code is in the  `Content\App.css` file of the **QuickStatus** project:</span></span> 
  
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

### <a name="elementsxml-file-for-the-ribbon"></a><span data-ttu-id="3ce52-495">Файл Elements.XML для ленты</span><span class="sxs-lookup"><span data-stu-id="3ce52-495">Elements.xml file for the ribbon</span></span>

<span data-ttu-id="3ce52-496">— Это следующее определение XML, добавлены кнопки на вкладке **ЗАДАЧИ** на ленте в `RibbonQuickStatusAction\Elements.xml` файл **QuickStatus** проекта:</span><span class="sxs-lookup"><span data-stu-id="3ce52-496">The following XML definition, for the added button on the **TASKS** tab on the ribbon, is in the  `RibbonQuickStatusAction\Elements.xml` file of the **QuickStatus** project:</span></span> 
  
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

### <a name="appmanifestxml-file"></a><span data-ttu-id="3ce52-497">Файл AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="3ce52-497">AppManifest.xml file</span></span>

<span data-ttu-id="3ce52-498">Ниже приведен XML-код для манифеста приложения **QuickStatus** проекта, который включает два области запроса разрешений, которые необходимы для обновления состояния назначения пользователя приложения в нескольких проектов.</span><span class="sxs-lookup"><span data-stu-id="3ce52-498">Following is the XML for the app manifest of the **QuickStatus** project, which includes the two permission request scopes that are necessary for updating the app user's assignment status in multiple projects:</span></span> 
  
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

### <a name="appiconpng-file"></a><span data-ttu-id="3ce52-499">Файл AppIcon.png</span><span class="sxs-lookup"><span data-stu-id="3ce52-499">AppIcon.png file</span></span>

<span data-ttu-id="3ce52-500">Законченное решение Visual Studio для приложения **QuickStatus** включает в себя пользовательский файл AppIcon.png.</span><span class="sxs-lookup"><span data-stu-id="3ce52-500">The complete Visual Studio solution for the **QuickStatus** app includes a custom AppIcon.png file.</span></span> <span data-ttu-id="3ce52-501">Решение будет включен в пакет SDK для Project 2013 для загрузки.</span><span class="sxs-lookup"><span data-stu-id="3ce52-501">The solution will be included in the Project 2013 SDK download.</span></span> 

<span data-ttu-id="3ce52-502"><a name="pj15_StatusingApp_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-502"></span></span>

## <a name="next-steps"></a><span data-ttu-id="3ce52-503">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="3ce52-503">Next steps</span></span>

<span data-ttu-id="3ce52-504">Приложение **QuickStatus** является относительно простой пример того, как создавать приложения, которые можно установить на Project Server 2013 и Project Online.</span><span class="sxs-lookup"><span data-stu-id="3ce52-504">The **QuickStatus** app is a relatively simple example of how to write apps that can be installed on Project Server 2013 and Project Online.</span></span> <span data-ttu-id="3ce52-505">В разделе [Тестирование приложения QuickStatus](#pj15_StatusingApp_Testing) приведены несколько улучшений, которые могут быть выполнены для более удобной.</span><span class="sxs-lookup"><span data-stu-id="3ce52-505">The [Testing the QuickStatus app](#pj15_StatusingApp_Testing) section lists several improvements that can be made for better usability.</span></span> <span data-ttu-id="3ce52-506">Приложение **QuickStatus** использует функции JavaScript для обновления состояния назначения для Project Web App.</span><span class="sxs-lookup"><span data-stu-id="3ce52-506">The **QuickStatus** app uses JavaScript functions to update assignment status for Project Web App.</span></span> <span data-ttu-id="3ce52-507">Однако изменение назначения процент завершения не методика управления рекомендуемые проекта.</span><span class="sxs-lookup"><span data-stu-id="3ce52-507">But, changing the assignment percent complete is not a recommended project management practice.</span></span> <span data-ttu-id="3ce52-508">Другим подходом будет обновлять фактическая дата начала и оставшаяся продолжительность свою задачу.</span><span class="sxs-lookup"><span data-stu-id="3ce52-508">Another approach would be to update the actual start date and remaining duration of assigned tasks.</span></span> <span data-ttu-id="3ce52-509">Описание проблем см раздел [Обновление лучше](https://www.mpug.com/articles/update-better) информационный бюллетень MPUG.</span><span class="sxs-lookup"><span data-stu-id="3ce52-509">For a discussion of the issues, see [Update Better](https://www.mpug.com/articles/update-better) in the MPUG newsletter.</span></span> 

<span data-ttu-id="3ce52-510"><a name="pj15_StatusingApp_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="3ce52-510"></span></span>

## <a name="see-also"></a><span data-ttu-id="3ce52-511">См. также</span><span class="sxs-lookup"><span data-stu-id="3ce52-511">See also</span></span>

- [<span data-ttu-id="3ce52-512">Задачи программирования Project Server</span><span class="sxs-lookup"><span data-stu-id="3ce52-512">Project Server programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="3ce52-513">Надстройки SharePoint</span><span class="sxs-lookup"><span data-stu-id="3ce52-513">SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163230.aspx)
- [<span data-ttu-id="3ce52-514">Управление обновлениями задач в Project Web App</span><span class="sxs-lookup"><span data-stu-id="3ce52-514">Managing task updates in Project Web App</span></span>](https://technet.microsoft.com/en-us/library/hh767481%28v=office.14%29.aspx)
- [<span data-ttu-id="3ce52-515">Создание дополнительных действий для развертывания с надстройками SharePoint</span><span class="sxs-lookup"><span data-stu-id="3ce52-515">Create custom actions to deploy with SharePoint Add-ins</span></span>](https://msdn.microsoft.com/library/jj163954.aspx)
    

