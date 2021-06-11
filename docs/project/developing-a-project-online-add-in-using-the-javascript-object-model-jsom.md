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
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a><span data-ttu-id="37c31-105">Разработка надстройки Project Online с помощью объектной модели JavaScript (JSOM)</span><span class="sxs-lookup"><span data-stu-id="37c31-105">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>

<span data-ttu-id="37c31-106">В этой статье Microsoft Project Online разработки надстройки для улучшения работы с Project Online.</span><span class="sxs-lookup"><span data-stu-id="37c31-106">This article describes Microsoft Project Online Add-in development to enhance your experience with the Project Online.</span></span> <span data-ttu-id="37c31-107">Проект разработки реализуется в качестве погона.</span><span class="sxs-lookup"><span data-stu-id="37c31-107">The development project is implemented as a walkthrough.</span></span> <span data-ttu-id="37c31-108">Надстройка, используемая для этой статьи, считывает и отображает имена и ИД опубликованных проектов из вашей учетной записи Project Online и позволяет сверлить для получения задач, связанных с отдельными проектами.</span><span class="sxs-lookup"><span data-stu-id="37c31-108">The add-in used for this article reads and displays the project names and IDs of the published projects from your Project Online account and allows you to drill down to retrieve tasks associated with individual projects.</span></span>
  
<span data-ttu-id="37c31-109">При запуске список надстройки выглядит примерно так же, как на следующей иллюстрации:</span><span class="sxs-lookup"><span data-stu-id="37c31-109">At run time, the add-in listing looks similar to the following illustration:</span></span>
  
<span data-ttu-id="37c31-110">![Снимок экрана, показывающий перечисление проектов и задач JSOM]Screen shot с перечислением(media/766e5914-f048-48f4-9282-291f55e6e90d.png "проектов и задач JSOM")</span><span class="sxs-lookup"><span data-stu-id="37c31-110">![Screen shot showing a listing of JSOM projects and tasks](media/766e5914-f048-48f4-9282-291f55e6e90d.png "Screen shot showing a listing of JSOM projects and tasks")</span></span>
  
<span data-ttu-id="37c31-111">В этом примере основное внимание уделяется взаимодействию с Project Online, запросам и настройке контекста для каждого запроса из службы.</span><span class="sxs-lookup"><span data-stu-id="37c31-111">The focus of the example is the interaction with the Project Online, making queries and setting the context for each request from the service.</span></span> <span data-ttu-id="37c31-112">Элементы пользовательского интерфейса (пользовательского интерфейса) получают минимальное внимание.</span><span class="sxs-lookup"><span data-stu-id="37c31-112">User interface (UI) elements receive minimal attention.</span></span> <span data-ttu-id="37c31-113">Вместо этого исходные списки предоставляют комментарии относительно пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="37c31-113">Instead, the source listings provide comments regarding the UI.</span></span>
  
> [!NOTE]
> <span data-ttu-id="37c31-114">Исходные файлы для примера надстройки, проекта Visual Studio, доступны по: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... .</span><span class="sxs-lookup"><span data-stu-id="37c31-114">The source files for the example add-in, a Visual Studio project, are available at: https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.....</span></span> <span data-ttu-id="37c31-115">Держите исходные файлы удобными в качестве ссылки во время чтения статьи, так как каждый из них дополняет другой.</span><span class="sxs-lookup"><span data-stu-id="37c31-115">Keep the source files handy as a reference while you read the article, as each complements the other.</span></span> <span data-ttu-id="37c31-116">Файлы в Visual Studio и исполняются с минимальными изменениями, заменив URL-адрес Project Online клиента в папку PWA.</span><span class="sxs-lookup"><span data-stu-id="37c31-116">The files in the Visual Studio project build and are executable with minimal changes—substituting the URL for your Project Online tenant down to the PWA folder.</span></span> 
  
## <a name="background"></a><span data-ttu-id="37c31-117">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="37c31-117">Background</span></span>

<span data-ttu-id="37c31-118">Project Online — это служба Office 365, которая предоставляет компаниям решение для управления портфелями проектов (система УПП) и управления проектами (PMO) для координации и управления портфелями, программами и проектами.</span><span class="sxs-lookup"><span data-stu-id="37c31-118">Project Online is a Office 365 service that provides companies with a project portfolio management (PPM) and project management office (PMO) solution to coordinate and manage portfolios, programs, and projects.</span></span> <span data-ttu-id="37c31-119">Project Online это другое предложение, чем Project настольные выпуски; однако Project Online по-прежнему содержит функции по обслуживанию и отслеживанию сведений о проекте на протяжении всего жизненного пути проекта.</span><span class="sxs-lookup"><span data-stu-id="37c31-119">Project Online is a different offering than the Project desktop editions; yet, Project Online still contains the functionality to maintain and track project details throughout the life of a project.</span></span> <span data-ttu-id="37c31-120">Project Online построена на SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="37c31-120">Project Online is built on SharePoint Online.</span></span>
  
<span data-ttu-id="37c31-121">Надстройка Project Online состоит из файлов JavaScript и ресурсов, взаимодействующих с API Client-Side-Object-Model.</span><span class="sxs-lookup"><span data-stu-id="37c31-121">A Project Online hosted add-in consists of JavaScript and resource files that interact with the Client-Side-Object-Model API.</span></span> <span data-ttu-id="37c31-122">Когда пользователь посещает надстройки, JavaScript и ресурсы загружаются и выполняются в браузере.</span><span class="sxs-lookup"><span data-stu-id="37c31-122">When the user visits the add-in, the JavaScript and resources are downloaded and executed within the browser.</span></span> <span data-ttu-id="37c31-123">Надстройка делает асинхронные вызовы для Project Online для взаимодействия со службой, будь то создание, ирисовка, обновление или удаление данных.</span><span class="sxs-lookup"><span data-stu-id="37c31-123">The add-In makes asynchronous calls to Project Online to interact with the service, whether creating, retrieving, updating, or deleting data.</span></span> 
  
<span data-ttu-id="37c31-124">Project Online выполняет еще одно действие для защиты от надстройки сведений, принадлежащих другим арендаторам; а именно, Project Online создает изолированный сайт для взаимодействия с запросами из надстройки.</span><span class="sxs-lookup"><span data-stu-id="37c31-124">Project Online performs one more action to protect information that belongs to other tenants from the add-in; namely, Project Online creates an isolated site to interact with the requests from the add-in.</span></span> <span data-ttu-id="37c31-125">Пользовательский код не запускается на Project Online хост.</span><span class="sxs-lookup"><span data-stu-id="37c31-125">No custom code runs on the Project Online host.</span></span> 
  
<span data-ttu-id="37c31-126">Настройка разработки для Project Online надстройки использует тип Visual Studio SharePoint надстройки.</span><span class="sxs-lookup"><span data-stu-id="37c31-126">The development setup for Project Online add-ins uses the Visual Studio SharePoint Add-in project type.</span></span> <span data-ttu-id="37c31-127">Надстройка написана в JavaScript и использует объектную модель Project JavaScript (JSOM) для взаимодействия с Project Online службой.</span><span class="sxs-lookup"><span data-stu-id="37c31-127">The add-in is written in JavaScript, and uses the Project JavaScript object model (JSOM) to interact with the Project Online service.</span></span> <span data-ttu-id="37c31-128">JSOM наследует большую часть своих функций от SharePoint JSOM.</span><span class="sxs-lookup"><span data-stu-id="37c31-128">The JSOM inherits much of its functionality from the SharePoint JSOM.</span></span>
  
> [!NOTE]
> <span data-ttu-id="37c31-129">Надстройки можно публиковать и продавать в Office Store или развертывать в частном каталоге приложений в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="37c31-129">Add-ins can be published and sold in the Office Store or deployed to a private app catalog on SharePoint.</span></span> <span data-ttu-id="37c31-130">Дополнительные сведения см. в [публикации Развертывания и публикации Office надстройки.](https://docs.microsoft.com/office/dev/add-ins/publish/publish)</span><span class="sxs-lookup"><span data-stu-id="37c31-130">For more information, see [Deploy and publish your Office Add-in](https://docs.microsoft.com/office/dev/add-ins/publish/publish).</span></span>
> 
> <span data-ttu-id="37c31-131">Надстройка, используемая в этой статье, является образцом для разработчиков; она не предназначена для использования в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="37c31-131">The add-in used in this article is a sample for developers; it is not intended for use in a production environment.</span></span> <span data-ttu-id="37c31-132">Основная цель — показать пример разработки приложений для Project Online.</span><span class="sxs-lookup"><span data-stu-id="37c31-132">The primary purpose is to show an example of app development for Project Online.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="37c31-133">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="37c31-133">Prerequisites</span></span>

<span data-ttu-id="37c31-134">Добавление следующих элементов в поддерживаемую Windows среду:</span><span class="sxs-lookup"><span data-stu-id="37c31-134">Add the following items to a supported Windows environment:</span></span>
  
- <span data-ttu-id="37c31-135">**платформа .NET Framework 4.0 или** более поздней версии: совместимы полные версии фреймворка из версии 4.0.</span><span class="sxs-lookup"><span data-stu-id="37c31-135">**.NET Framework 4.0 or later**: Complete versions of the framework from version 4.0 are compatible.</span></span> <span data-ttu-id="37c31-136">Сайт загрузки файлов — https://msdn.microsoft.com/vstudio/aa496123.aspx.</span><span class="sxs-lookup"><span data-stu-id="37c31-136">The download site is https://msdn.microsoft.com/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="37c31-137">**Visual Studio 2013 или позже:**</span><span class="sxs-lookup"><span data-stu-id="37c31-137">**Visual Studio 2013 or later**:</span></span>  
    
   - <span data-ttu-id="37c31-138">Профессиональное издание Visual Studio 2015 г. готово к выходу из окна и доступно на https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx сайте .</span><span class="sxs-lookup"><span data-stu-id="37c31-138">The professional edition of Visual Studio 2015 is ready to go out-of-the box and is available at https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx.</span></span>
    
   - <span data-ttu-id="37c31-139">В сообществе выпуск Visual Studio 2015 доступен по https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx номеру .</span><span class="sxs-lookup"><span data-stu-id="37c31-139">The community edition of Visual Studio 2015 is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span> <span data-ttu-id="37c31-140">В этом выпуске требуется ручная установка Microsoft Office средств разработки для Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="37c31-140">This edition requires manual installation of the Microsoft Office Developer Tools for Visual Studio.</span></span>
    
   <span data-ttu-id="37c31-141">Средства Microsoft Office для Visual Studio доступны по https://www.visualstudio.com/en-us/features/office-tools-vs.aspx .</span><span class="sxs-lookup"><span data-stu-id="37c31-141">The Microsoft Office Developer Tools for Visual Studio are available at https://www.visualstudio.com/en-us/features/office-tools-vs.aspx.</span></span>
    
- <span data-ttu-id="37c31-142">**Учетная Project Online.** Это обеспечивает доступ к службе размещения.</span><span class="sxs-lookup"><span data-stu-id="37c31-142">**A Project Online account**: This provides access to the hosting service.</span></span> <span data-ttu-id="37c31-143">Дополнительные сведения о получении учетной записи Project Online см. здесь: https://products.office.com/en-us/Project/project-online-portfolio-management.</span><span class="sxs-lookup"><span data-stu-id="37c31-143">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
   <span data-ttu-id="37c31-144">Убедитесь, что пользователь надстройки имеет достаточное разрешение для доступа к некоторым проектам Project Online клиента.</span><span class="sxs-lookup"><span data-stu-id="37c31-144">Ensure that the add-in user has sufficient authorization to access some projects in the Project Online tenant.</span></span> 
    
- <span data-ttu-id="37c31-145">**Проекты на сайте размещения,** которые заполнены информацией.</span><span class="sxs-lookup"><span data-stu-id="37c31-145">**Projects on the hosting site** that are populated with information.</span></span>
    
> [!NOTE]
> <span data-ttu-id="37c31-146">Стандартным платформа .NET Framework является правильная используемая структура.</span><span class="sxs-lookup"><span data-stu-id="37c31-146">The standard .NET Framework is the correct framework to use.</span></span> <span data-ttu-id="37c31-147">Не используйте "профиль платформа .NET Framework 4".</span><span class="sxs-lookup"><span data-stu-id="37c31-147">Do not use the ".NET Framework 4 Client Profile".</span></span> 
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="37c31-148">Настройка проекта Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37c31-148">Set up the Visual Studio project</span></span>

<span data-ttu-id="37c31-149">Настройка приложения состоит из создания нового проекта, связывания соответствующих библиотек и объявления необходимых пространств имен.</span><span class="sxs-lookup"><span data-stu-id="37c31-149">The application setup consists of creating a new project, linking the appropriate libraries and declaring the needed namespaces.</span></span> <span data-ttu-id="37c31-150">Visual Studio поддерживает нескольких типов проектов разработки.</span><span class="sxs-lookup"><span data-stu-id="37c31-150">Visual Studio presents several types of development projects.</span></span> <span data-ttu-id="37c31-151">Раздел краткий и очень простой.</span><span class="sxs-lookup"><span data-stu-id="37c31-151">The section is brief and very basic.</span></span> <span data-ttu-id="37c31-152">Значение состоит в том, что сведения совмеся в одном месте.</span><span class="sxs-lookup"><span data-stu-id="37c31-152">The value is having the information is coalesced in one place.</span></span>
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="37c31-153">Выберите проект Visual Studio</span><span class="sxs-lookup"><span data-stu-id="37c31-153">Select a Visual Studio project</span></span>

<span data-ttu-id="37c31-154">Чтобы создать проект соответствующего типа для надстройки, необходимо сделать следующие действия.</span><span class="sxs-lookup"><span data-stu-id="37c31-154">To create a project of the appropriate type for the add-in, you must do the following steps.</span></span> <span data-ttu-id="37c31-155">Ключевые слова, которые встречаются на экране, имеют **смелый атрибут:**</span><span class="sxs-lookup"><span data-stu-id="37c31-155">Keywords encountered on the screen have a **bold** attribute:</span></span> 
  
1. <span data-ttu-id="37c31-156">В меню File выберите **файл**  >  **Project.**  >  </span><span class="sxs-lookup"><span data-stu-id="37c31-156">From the File menu, choose **File** > **New** > **Project**.</span></span> 
    
2. <span data-ttu-id="37c31-157">Из установленных шаблонов в левой области выберите C#  >  **Office/SharePoint**  >  **веб-надстройки**.</span><span class="sxs-lookup"><span data-stu-id="37c31-157">From the Installed templates in the left pane, select **C#** > **Office/SharePoint** > **Web Add-ins**.</span></span> 
    
3. <span data-ttu-id="37c31-158">В верхней части центральной области выберите платформа .NET Framework **4** или более поздней части; текущая версия 4.6.</span><span class="sxs-lookup"><span data-stu-id="37c31-158">At the top of the central pane, select **.NET Framework 4** or later; the current version is 4.6.</span></span> 
    
4. <span data-ttu-id="37c31-159">Из типов приложений на центральной области выберите SharePoint **надстройку.**</span><span class="sxs-lookup"><span data-stu-id="37c31-159">From the application types in the central pane, choose **SharePoint Add-in**.</span></span> 
    
5. <span data-ttu-id="37c31-160">В нижней части укажите имя и расположение проекта, а также имя решения.</span><span class="sxs-lookup"><span data-stu-id="37c31-160">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
6. <span data-ttu-id="37c31-161">Кроме того, в нижней части установите флажок **Создать каталог для решения**.</span><span class="sxs-lookup"><span data-stu-id="37c31-161">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
7. <span data-ttu-id="37c31-162">Нажмите кнопку **ОК**, чтобы создать начальный проект.</span><span class="sxs-lookup"><span data-stu-id="37c31-162">Click **OK** to create the initial project.</span></span> 
    
<span data-ttu-id="37c31-163">Мастер Visual Studio задает несколько последующих вопросов о сайте параметров Project Online (называемый SharePoint параметров в диалоговом окрашиваемом диалоге) в нескольких последующих диалогов.</span><span class="sxs-lookup"><span data-stu-id="37c31-163">The Visual Studio Wizard asks a few follow-up questions about the Project Online settings site (called SharePoint settings in the dialogs) in a couple of dialogs that follow.</span></span> <span data-ttu-id="37c31-164">Вот вопросы:</span><span class="sxs-lookup"><span data-stu-id="37c31-164">Here are the questions:</span></span>
  
1. <span data-ttu-id="37c31-165">Какие SharePoint вы хотите использовать для отладки надстройки?</span><span class="sxs-lookup"><span data-stu-id="37c31-165">What SharePoint site do you want to use for debugging your add-in?</span></span> <span data-ttu-id="37c31-166">Укажите URL-адрес PWA сайта, например https://contoso.sharepoint.com/sites/pwa .</span><span class="sxs-lookup"><span data-stu-id="37c31-166">Specify the URL to your PWA site, such as https://contoso.sharepoint.com/sites/pwa.</span></span>
    
2. <span data-ttu-id="37c31-167">Как вы хотите провести SharePoint надстройки?</span><span class="sxs-lookup"><span data-stu-id="37c31-167">How do you want to host your SharePoint Add-in?</span></span> <span data-ttu-id="37c31-168">Выберите [X] **SharePoint-хостинга**.</span><span class="sxs-lookup"><span data-stu-id="37c31-168">Choose [X] **SharePoint-hosted**.</span></span>
    
   <span data-ttu-id="37c31-169">Дополнительные сведения о SharePoint надстройки, включая варианты размещения, см. в SharePoint [надстройки.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)</span><span class="sxs-lookup"><span data-stu-id="37c31-169">For more information about SharePoint Add-ins, including hosting options, see [SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins).</span></span>
    
3. <span data-ttu-id="37c31-170">Нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="37c31-170">Click **Next**.</span></span> 
    
<span data-ttu-id="37c31-171">Во втором дополнительном диалоговом окрашиваемом диалоговом окрашиваемой версии SharePoint Online для надстройки:</span><span class="sxs-lookup"><span data-stu-id="37c31-171">The second additional dialog asks you to specify the SharePoint Online version for the add-in:</span></span> 
  
1. <span data-ttu-id="37c31-172">Что является ранней версией SharePoint, которую необходимо нацелить на надстройки?</span><span class="sxs-lookup"><span data-stu-id="37c31-172">What's the earliest version of SharePoint that you want your add-in to target?</span></span> <span data-ttu-id="37c31-173">Выберите [X] S **harePoint-Online**.</span><span class="sxs-lookup"><span data-stu-id="37c31-173">Choose [X] S **harePoint-Online**.</span></span> 
    
2. <span data-ttu-id="37c31-174">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="37c31-174">Click **Finish**.</span></span> 
    
<span data-ttu-id="37c31-175">Visual Studio создает проект и имеет доступ к Project Online сайту.</span><span class="sxs-lookup"><span data-stu-id="37c31-175">Visual Studio creates the project and accesses the Project Online site.</span></span> 
  
### <a name="enable-sideloading-on-the-project-online-site"></a><span data-ttu-id="37c31-176">Включить побную загрузку на Project Online сайте</span><span class="sxs-lookup"><span data-stu-id="37c31-176">Enable sideloading on the Project Online site</span></span>

<span data-ttu-id="37c31-177">Sideloading — это механизм тестирования и отладки Project Online надстроек. Для боковой загрузки требуется два сценария: один для обеспечения боковой загрузки Project Online сайта, а другой для отключения боковой загрузки после завершения тестирования и отладки надстройки.</span><span class="sxs-lookup"><span data-stu-id="37c31-177">Sideloading is the mechanism for testing and debugging Project Online add-ins. You need two scripts for sideloading: one to enable sideloading on your Project Online site and another to disable sideloading once you finish testing and debugging the add-in.</span></span>
  
<span data-ttu-id="37c31-178">Дополнительные сведения о настройке боковой загрузки см. в приложении [Enable SideLoading в коллекции сайтов,](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)не относяющихся к разработчику.</span><span class="sxs-lookup"><span data-stu-id="37c31-178">For more information about setting up sideloading, see [Enable app SideLoading in your non-developer site collection](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/).</span></span>
  
> [!NOTE]
> <span data-ttu-id="37c31-179">Sideloading apps is a developer/test feature.</span><span class="sxs-lookup"><span data-stu-id="37c31-179">Sideloading apps is a developer/test feature.</span></span> <span data-ttu-id="37c31-180">Он не **предназначен для использования в производстве.**</span><span class="sxs-lookup"><span data-stu-id="37c31-180">It is **not intended for production use**.</span></span> <span data-ttu-id="37c31-181">Не перегружайте приложения регулярно или не делайте загрузку приложения включенной дольше, чем вы активно используете эту функцию.</span><span class="sxs-lookup"><span data-stu-id="37c31-181">Do not sideload apps regularly, or keep app sideloading enabled for longer than you are actively using the feature.</span></span> 
  
## <a name="add-content-to-the-add-in-project"></a><span data-ttu-id="37c31-182">Добавление контента в проект надстройки</span><span class="sxs-lookup"><span data-stu-id="37c31-182">Add content to the add-in project</span></span>

<span data-ttu-id="37c31-183">После создания проекта и настройки механизма отладки добавление контента в приложение включает следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="37c31-183">After creating a project and setting up the debugging mechanism, adding content to the app includes the following tasks:</span></span>
  
- <span data-ttu-id="37c31-184">Настройка области приложения</span><span class="sxs-lookup"><span data-stu-id="37c31-184">Setting the application scope</span></span>
    
- <span data-ttu-id="37c31-185">Связь библиотеки JSOM</span><span class="sxs-lookup"><span data-stu-id="37c31-185">Linking the JSOM library</span></span>
    
- <span data-ttu-id="37c31-186">Добавление элементов пользовательского интерфейса в надстройку</span><span class="sxs-lookup"><span data-stu-id="37c31-186">Adding UI Elements to the add-in</span></span>
    
- <span data-ttu-id="37c31-187">Инициализация и подключение к Project Online службе</span><span class="sxs-lookup"><span data-stu-id="37c31-187">Initializing and connecting to the Project Online service</span></span>
    
- <span data-ttu-id="37c31-188">Ирисовка проектов и сведений/свойств</span><span class="sxs-lookup"><span data-stu-id="37c31-188">Retrieving projects and details/properties</span></span>
    
- <span data-ttu-id="37c31-189">Отображение проектов</span><span class="sxs-lookup"><span data-stu-id="37c31-189">Displaying projects</span></span>
    
- <span data-ttu-id="37c31-190">Отображение задач для Project</span><span class="sxs-lookup"><span data-stu-id="37c31-190">Displaying tasks for a Project</span></span>
    
<span data-ttu-id="37c31-191">Проект надстройки состоит из множества файлов.</span><span class="sxs-lookup"><span data-stu-id="37c31-191">The add-in project consists of many files.</span></span> <span data-ttu-id="37c31-192">В этом примере необходимо изменить следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="37c31-192">In this example, you'll need to edit the following files:</span></span> 
  
- <span data-ttu-id="37c31-193">AppManifest.xml</span><span class="sxs-lookup"><span data-stu-id="37c31-193">AppManifest.xml</span></span>
    
- <span data-ttu-id="37c31-194">Default.aspx</span><span class="sxs-lookup"><span data-stu-id="37c31-194">Default.aspx</span></span>
    
- <span data-ttu-id="37c31-195">App.js</span><span class="sxs-lookup"><span data-stu-id="37c31-195">App.js</span></span>
    
- <span data-ttu-id="37c31-196">App.css — необязательный; содержит определения стилей, разработанные для надстройки</span><span class="sxs-lookup"><span data-stu-id="37c31-196">App.css - optional; contains style definitions developed for the add-in</span></span>
    
<span data-ttu-id="37c31-197">Если клиент Project Online, например переход с пробной версии на сайт подписки, можно обновить свойства проекта, включая подключение к серверу и URL-адрес сайта, используя окно свойств, доступное через команду **Окно** свойств  >   просмотра.</span><span class="sxs-lookup"><span data-stu-id="37c31-197">If the Project Online tenant changes, such as moving from a trial to a subscription site, you can update the project properties, including the Server Connection and Site URL, using the Properties Window available through the **View** > **Properties Window** command.</span></span> 
  
<span data-ttu-id="37c31-198">Вы также можете добавить файлы в проект.</span><span class="sxs-lookup"><span data-stu-id="37c31-198">You can also add files to the project.</span></span> <span data-ttu-id="37c31-199">Если это так, вам потребуется обновить файл Elements.xml, расположенный в одной группе (контент, изображения, страницы или скрипты), чтобы включить новые файлы.</span><span class="sxs-lookup"><span data-stu-id="37c31-199">If so, you'll need to update the Elements.xml file located in the same group (Content, Images, Pages, or Scripts) to include the new files.</span></span> <span data-ttu-id="37c31-200">Дополнительные сведения о файлах проекта см. в дополнительных сведениях о структуре манифеста приложения и пакете [SharePoint надстройки.](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)</span><span class="sxs-lookup"><span data-stu-id="37c31-200">For more information about the project files, see [Explore the app manifest structure and the package of a SharePoint Add-in](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in).</span></span>
  
### <a name="set-application-scope"></a><span data-ttu-id="37c31-201">Настройка области приложения</span><span class="sxs-lookup"><span data-stu-id="37c31-201">Set application scope</span></span>

<span data-ttu-id="37c31-202">Область потребностей надстройки или уровни разрешений, определенные перед возвращением службой сведений в результатах запроса.</span><span class="sxs-lookup"><span data-stu-id="37c31-202">The add-in needs scope or permission levels defined before the service returns information in query results.</span></span> <span data-ttu-id="37c31-203">Для этой надстройки используйте следующую область для Visual Studio проекта.</span><span class="sxs-lookup"><span data-stu-id="37c31-203">For this add-in, use the following scope to the Visual Studio project.</span></span> <span data-ttu-id="37c31-204">Это изменение в файле AppManifest.xml на вкладке Permissions:</span><span class="sxs-lookup"><span data-stu-id="37c31-204">This change is made to the AppManifest.xml file in the Permissions tab:</span></span>

|<span data-ttu-id="37c31-205">Область</span><span class="sxs-lookup"><span data-stu-id="37c31-205">Scope</span></span>|<span data-ttu-id="37c31-206">Разрешение</span><span class="sxs-lookup"><span data-stu-id="37c31-206">Permission</span></span>|
|:-----|:-----|
|<span data-ttu-id="37c31-207">Несколько проектов (Project Server)</span><span class="sxs-lookup"><span data-stu-id="37c31-207">Multiple Projects (Project Server)</span></span>  <br/> |<span data-ttu-id="37c31-208">Чтение</span><span class="sxs-lookup"><span data-stu-id="37c31-208">Read</span></span>  <br/> |
   
<span data-ttu-id="37c31-209">Сохраните файл после настройки области приложения.</span><span class="sxs-lookup"><span data-stu-id="37c31-209">Save the file after setting the application scope.</span></span> <span data-ttu-id="37c31-210">В противном случае данные из службы не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="37c31-210">Otherwise, no data will be returned from the service.</span></span> 
  
### <a name="link-the-jsom-library"></a><span data-ttu-id="37c31-211">Ссылка библиотеки JSOM</span><span class="sxs-lookup"><span data-stu-id="37c31-211">Link the JSOM library</span></span>

<span data-ttu-id="37c31-212">Библиотеки Project Online, PS.js и PS.debug.js, предоставлены Project Online и всегда являются последней версией.</span><span class="sxs-lookup"><span data-stu-id="37c31-212">The runtime Project Online libraries, PS.js and PS.debug.js, are provided by Project Online and are always the most recent version.</span></span> <span data-ttu-id="37c31-213">Надстройки JavaScript, которые используют JSOM, должны связываться с одной из этих библиотек.</span><span class="sxs-lookup"><span data-stu-id="37c31-213">JavaScript add-ins that use JSOM must link with one of these libraries.</span></span> <span data-ttu-id="37c31-214">Определения ссылок добавляются в файл Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="37c31-214">The linking definitions are added in the Default.aspx file.</span></span> <span data-ttu-id="37c31-215">Команды по использованию PS.js или PS.debug.js являются частью кода, расположенного в App.js файле.</span><span class="sxs-lookup"><span data-stu-id="37c31-215">The commands to use the PS.js and/or PS.debug.js are part of the code located in the App.js file.</span></span>
  
<span data-ttu-id="37c31-216">Добавьте следующую команду для определения PS.js или PS.debug.js в элементе, следующего за `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` "SharePoint:ScriptLink" для sp.js.</span><span class="sxs-lookup"><span data-stu-id="37c31-216">Add the following command for PS.js or PS.debug.js definition in the  `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` element following the "SharePoint:ScriptLink" for sp.js.</span></span> 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> <span data-ttu-id="37c31-217">Атрибут **OnDemand** для PS.js или PS.debug.js для false **.**</span><span class="sxs-lookup"><span data-stu-id="37c31-217">The **OnDemand** attribute for PS.js or PS.debug.js set to **false**.</span></span> 
  
### <a name="add-ui-elements-to-the-add-in"></a><span data-ttu-id="37c31-218">Добавление элементов пользовательского интерфейса в надстройку</span><span class="sxs-lookup"><span data-stu-id="37c31-218">Add UI elements to the add-in</span></span>

<span data-ttu-id="37c31-219">Пример надстройки состоит из нескольких компонентов.</span><span class="sxs-lookup"><span data-stu-id="37c31-219">The example add-in consists of a few components.</span></span> <span data-ttu-id="37c31-220">Статические описания элементов находятся в файле Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="37c31-220">Static element descriptions are located in the Default.aspx file.</span></span> <span data-ttu-id="37c31-221">Динамические описания элементов и код для всех компонентов находятся в App.js файле.</span><span class="sxs-lookup"><span data-stu-id="37c31-221">Dynamic element descriptions and code for all components are located in the App.js file.</span></span> <span data-ttu-id="37c31-222">Для комментариев по компонентам обратитесь к спискам исходных кодов.</span><span class="sxs-lookup"><span data-stu-id="37c31-222">For comments regarding the components, refer to the source code listings.</span></span> <span data-ttu-id="37c31-223">Вот список компонентов пользовательского интерфейса в надстройки:</span><span class="sxs-lookup"><span data-stu-id="37c31-223">Here is a list of the UI components in the add-in:</span></span>
  
- <span data-ttu-id="37c31-224">Название</span><span class="sxs-lookup"><span data-stu-id="37c31-224">Title</span></span>
    
- <span data-ttu-id="37c31-225">Вводная глагольная фраза</span><span class="sxs-lookup"><span data-stu-id="37c31-225">Introductory verbiage</span></span>
    
- <span data-ttu-id="37c31-226">Кнопка для удаления задач из таблицы</span><span class="sxs-lookup"><span data-stu-id="37c31-226">Button to remove tasks from the table</span></span>
    
- <span data-ttu-id="37c31-227">Таблица, в которую перечислены ИД проекта и имя, а также сведения о задачах.</span><span class="sxs-lookup"><span data-stu-id="37c31-227">Table that lists the project ID and name, and the task information.</span></span>
    
- <span data-ttu-id="37c31-228">Кнопка Tasks (клонированная один раз для каждого проекта), которая импортирует данные задач в таблицу.</span><span class="sxs-lookup"><span data-stu-id="37c31-228">Tasks Button (cloned once for each project) that imports task data into the table.</span></span>
    
<span data-ttu-id="37c31-229">Подробные сведения об пользовательском интерфейсе, например заголовок и заголовок таблицы проектов, см. в файле проекта Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="37c31-229">For details of the user interface, such as the title and the header portion of the project table, see the Default.aspx project file.</span></span>
  
### <a name="initialize-and-connect-to-the-host-system"></a><span data-ttu-id="37c31-230">Инициализация и подключение к хост-системе</span><span class="sxs-lookup"><span data-stu-id="37c31-230">Initialize and connect to the host system</span></span>

<span data-ttu-id="37c31-231">Файл App.js содержит код JavaScript.</span><span class="sxs-lookup"><span data-stu-id="37c31-231">The App.js file contains the JavaScript code.</span></span> <span data-ttu-id="37c31-232">Надстройка загружается PS.js браузере, а затем вызывает функцию initializePage.</span><span class="sxs-lookup"><span data-stu-id="37c31-232">The add-in loads PS.js in the browser, and then calls the initializePage function.</span></span> <span data-ttu-id="37c31-233">InitializePage извлекает контекст в конечную точку Project Online и запускает функцию loadProjects.</span><span class="sxs-lookup"><span data-stu-id="37c31-233">InitializePage retrieves a context to the Project Online endpoint and starts the loadProjects function.</span></span>
  
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

### <a name="retrieve-the-projects"></a><span data-ttu-id="37c31-234">Извлечение проектов</span><span class="sxs-lookup"><span data-stu-id="37c31-234">Retrieve the projects</span></span>

<span data-ttu-id="37c31-235">Функция loadProjects запрашивает службу для имен и ИД проекта.</span><span class="sxs-lookup"><span data-stu-id="37c31-235">The loadProjects function queries the service for the project names and IDs.</span></span> 
  
<span data-ttu-id="37c31-236">Приложение извлекает имя проекта и id проекта. Другие сведения о проекте доступны, к ним можно получить доступ, изменяя метод нагрузки, чтобы точно определить свойства, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="37c31-236">The application retrieves the project name and project Id. Other information about the project is available and can be accessed by modifying the load method to identify explicitly the properties to retrieve.</span></span> <span data-ttu-id="37c31-237">В коде в качестве комментария представлен пример.</span><span class="sxs-lookup"><span data-stu-id="37c31-237">An example is provided in the code as a comment.</span></span> 
  
<span data-ttu-id="37c31-238">Если запрос удался, надстройка продолжит вызывать displayProjects.</span><span class="sxs-lookup"><span data-stu-id="37c31-238">If the query succeeds, the add-in continues by calling displayProjects.</span></span> 
  
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

### <a name="display-the-projects"></a><span data-ttu-id="37c31-239">Отображение проектов</span><span class="sxs-lookup"><span data-stu-id="37c31-239">Display the projects</span></span>

<span data-ttu-id="37c31-240">Функция displayProjects создает таблицу, одну строку для каждого проекта и кнопку для отображения задач для конкретного проекта.</span><span class="sxs-lookup"><span data-stu-id="37c31-240">The displayProjects function creates a table, one row per project, and a button to show the tasks for the specific project.</span></span> 
  
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
> <span data-ttu-id="37c31-241">В то время как цикл имеет доступ к свойствам ID и имен.</span><span class="sxs-lookup"><span data-stu-id="37c31-241">The while loop accesses the ID and name properties.</span></span> <span data-ttu-id="37c31-242">Это немного отличается от проекта исходных кодов, который вызывает функцию, которая, в свою очередь, имеет доступ к тем же свойствам.</span><span class="sxs-lookup"><span data-stu-id="37c31-242">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
### <a name="display-the-tasks-for-a-project"></a><span data-ttu-id="37c31-243">Отображение задач для проекта</span><span class="sxs-lookup"><span data-stu-id="37c31-243">Display the tasks for a project</span></span>

<span data-ttu-id="37c31-244">Задачи, хотя и являются частью надстройки, не являются частью начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="37c31-244">The tasks, while part of the add-in, are not part of the initial loading.</span></span> <span data-ttu-id="37c31-245">Если пользователь заинтересован в задачах, связанных с проектом, нажатие кнопки "Показать задачи" вызывает отображение задач в списке с помощью обработанта событий btnLoadTasks.</span><span class="sxs-lookup"><span data-stu-id="37c31-245">If the user is interested in the tasks associated with a project, clicking the "Show Tasks" button causes the tasks to display in the list using the btnLoadTasks event handler.</span></span> 
  
<span data-ttu-id="37c31-246">Обработник событий btnLoadTasks с соответствующим ИД проекта запрашивает задачи для указанного проекта с сервера.</span><span class="sxs-lookup"><span data-stu-id="37c31-246">The btnLoadTasks event handler, with the appropriate project ID, requests the tasks for the specified project from the server.</span></span> <span data-ttu-id="37c31-247">После получения btnLoadTasks передает список задач для отображенияTasks, чтобы представить задачи на экране.</span><span class="sxs-lookup"><span data-stu-id="37c31-247">Once retrieved, btnLoadTasks passes the task list to displayTasks to present the tasks onscreen.</span></span>
  
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

<span data-ttu-id="37c31-248">Функция displayTasks отображает задачи, связанные с указанным проектом, непосредственно под записью проекта.</span><span class="sxs-lookup"><span data-stu-id="37c31-248">The displayTasks function displays the tasks associated with a specified project immediately beneath the project entry.</span></span>
  
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
> <span data-ttu-id="37c31-249">В то время как цикл имеет доступ к ID задачи и свойствам имен.</span><span class="sxs-lookup"><span data-stu-id="37c31-249">The while loop accesses the task ID and name properties.</span></span> <span data-ttu-id="37c31-250">Это немного отличается от проекта исходных кодов, который вызывает функцию, которая, в свою очередь, имеет доступ к тем же свойствам.</span><span class="sxs-lookup"><span data-stu-id="37c31-250">This is slightly different than the source code project that calls a function that, in turn, accesses the same properties.</span></span> 
  
<span data-ttu-id="37c31-251">Пример вывода для задач одного проекта следует.</span><span class="sxs-lookup"><span data-stu-id="37c31-251">Sample output for the tasks of a single project follows.</span></span>
  
<span data-ttu-id="37c31-252">![Снимок экрана, показывающий выход для снимка]экрана задачи проекта,(media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "показывающий выход для задачи проекта")</span><span class="sxs-lookup"><span data-stu-id="37c31-252">![Screen shot showing the output for a project task](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "Screen shot showing the output for a project task")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37c31-253">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="37c31-253">See also</span></span>

<span data-ttu-id="37c31-254">Документы и примеры, относящиеся к Project Online и разработке приложений с помощью CSOM, находятся на [портале разработчиков Project](https://developer.microsoft.com/en-us/project).</span><span class="sxs-lookup"><span data-stu-id="37c31-254">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    


