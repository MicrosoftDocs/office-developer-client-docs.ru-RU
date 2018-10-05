---
title: Предварительные требования для основанных на ASMX примеров кода в Project
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- code samples
- Project Server code samples
- Project Server programming
- PSI code samples
- PSI programming
keywords:
- Примеры кода, project server, Project Server по программированию, PSI, компиляция примеры кода, PSI, программирование
localization_priority: Normal
ms.assetid: df584b25-4460-46c8-89a8-3b2c94d20bba
description: Узнайте, сведения, которые помогут в создании проектов в Visual Studio с помощью образцы кода на основе ASMX, включенные в разделы справочника по интерфейса Project Server (PSI).
ms.openlocfilehash: 26ad2e388b7e7f6f19e028b47c7f6d1a3fbd020c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399328"
---
# <a name="prerequisites-for-asmx-based-code-samples-in-project"></a><span data-ttu-id="2884e-104">Предварительные требования для основанных на ASMX примеров кода в Project</span><span class="sxs-lookup"><span data-stu-id="2884e-104">Prerequisites for ASMX-based code samples in Project</span></span>

<span data-ttu-id="2884e-105">Узнайте, сведения, которые помогут в создании проектов в Visual Studio с помощью образцы кода на основе ASMX, включенные в разделы справочника по интерфейса Project Server (PSI).</span><span class="sxs-lookup"><span data-stu-id="2884e-105">Learn information to help you create projects in Visual Studio by using the ASMX-based code samples that are included in the Project Server Interface (PSI) reference topics.</span></span>
  
<span data-ttu-id="2884e-106">Многие из примеров кода, включенных в [библиотеки и веб-службы Project Server 2013 класс ссылаться](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) изначально были созданы для пакета SDK для Office Project 2007 и использовать стандартный формат для веб-службы ASMX.</span><span class="sxs-lookup"><span data-stu-id="2884e-106">Many of the code samples included in the [Project Server 2013 class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) were originally created for the Office Project 2007 SDK, and use a standard format for ASMX web services.</span></span> <span data-ttu-id="2884e-107">Примеры по-прежнему работают в Project Server 2013 и предназначены для копируются в консольного приложения и запуска в качестве завершения блока.</span><span class="sxs-lookup"><span data-stu-id="2884e-107">The samples still work in Project Server 2013 and are designed to be copied into a console application and run as a complete unit.</span></span> <span data-ttu-id="2884e-108">Имеются следующие исключения в образце.</span><span class="sxs-lookup"><span data-stu-id="2884e-108">Exceptions are noted in the sample.</span></span> 
  
<span data-ttu-id="2884e-109">Новые образцы PSI в пакет SDK для Project 2013 соответствует формат, который использует службы Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="2884e-109">New PSI samples in the Project 2013 SDK conform to a format that uses Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="2884e-110">Примеры на основе ASMX также можно адаптировать для использования службы WCF.</span><span class="sxs-lookup"><span data-stu-id="2884e-110">The ASMX-based samples can also be adapted to use WCF services.</span></span> <span data-ttu-id="2884e-111">В этой статье показано, как использовать образцы с веб-службы ASMX.</span><span class="sxs-lookup"><span data-stu-id="2884e-111">This article shows how to use the samples with ASMX web services.</span></span> <span data-ttu-id="2884e-112">Для получения сведений об использовании примеров со службами WCF видеть [Необходимые условия для образцов кода на основе WCF в проекте](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="2884e-112">For information about using the samples with WCF services, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="2884e-113">Интерфейс веб-службы ASMX из PSI рекомендуется использовать в Project Server 2013, но по-прежнему поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2884e-113">The ASMX web service interface of the PSI is deprecated in Project Server 2013, but is still supported.</span></span> <span data-ttu-id="2884e-114">Если клиентской объектной модели (CSOM) содержит методы, которые требуются приложению, необходимо разработать новые приложения с помощью CSOM.</span><span class="sxs-lookup"><span data-stu-id="2884e-114">If the client-side object model (CSOM) includes the methods that your application requires, new applications should be developed with the CSOM.</span></span> <span data-ttu-id="2884e-115">CSOM позволяет приложениям для работы с Project Online и локальной установки Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2884e-115">The CSOM enables applications to work with Project Online or an on-premises installation of Project Server 2013.</span></span> <span data-ttu-id="2884e-116">В противном случае — если приложение использует PSI, следует использовать интерфейс WCF, который является технологии, рекомендуется использовать сетевые подключения.</span><span class="sxs-lookup"><span data-stu-id="2884e-116">Otherwise, if your application uses the PSI, it should use the WCF interface, which is the technology that we recommend for network communications.</span></span> <span data-ttu-id="2884e-117">Приложения, использующие интерфейс ASMX или WCF интерфейс может работать только для локальных установок Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2884e-117">Applications that use the ASMX interface or the WCF interface can work only for on-premises installations of Project Server 2013.</span></span> <span data-ttu-id="2884e-118">Дополнительные сведения о CSOM можно [Архитектура Project Server 2013](project-server-2013-architecture.md) и [объектной модели со стороны клиента (CSOM) для Project 2013](client-side-object-model-csom-for-project-2013.md).</span><span class="sxs-lookup"><span data-stu-id="2884e-118">For more information about the CSOM, see [Project Server 2013 architecture](project-server-2013-architecture.md) and [Client-side object model (CSOM) for Project 2013](client-side-object-model-csom-for-project-2013.md).</span></span> 
  
<span data-ttu-id="2884e-119">Перед выполнением примеров кода вам следует настроить среду разработки и само приложение, а также изменить значения общих констант в соответствии с вашей средой.</span><span class="sxs-lookup"><span data-stu-id="2884e-119">Before running the code samples, you must set up the development environment, configure the application, and change generic constant values to match your environment.</span></span>
  
## <a name="setting-up-the-development-environment"></a><span data-ttu-id="2884e-120">Настройка среды разработки</span><span class="sxs-lookup"><span data-stu-id="2884e-120">Setting up the development environment</span></span>
<span data-ttu-id="2884e-121"><a name="pj15_PrerequisitesASMX_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-121"></span></span>

1. <span data-ttu-id="2884e-122">**Настройте тестовую систему Project Server**.</span><span class="sxs-lookup"><span data-stu-id="2884e-122">**Set up a test Project Server system**.</span></span>
    
   <span data-ttu-id="2884e-p104">Во время разработки или тестирования всегда используйте тестовую систему Project Server. Даже если ваш код работает идеально, зависимости между проектами, ведение отчетов или другие зависящие от среды факторы могут привести к непредусмотренным последствиям.</span><span class="sxs-lookup"><span data-stu-id="2884e-p104">Use a test Project Server system whenever you are developing or testing. Even when your code works perfectly, interproject dependencies, reporting, or other environmental factors can cause unintended consequences.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="2884e-125">Убедитесь, что действительный пользователь на сервере и проверьте наличие достаточных разрешений для вызовов PSI, используемые приложением.</span><span class="sxs-lookup"><span data-stu-id="2884e-125">Ensure that you are a valid user on the server, and check that you have sufficient permissions for the PSI calls that your application uses.</span></span> <span data-ttu-id="2884e-126">В разделах, для каждого метода PSI включает в себя таблице разрешения Project Server.</span><span class="sxs-lookup"><span data-stu-id="2884e-126">The reference topic for each PSI method includes a Project Server Permissions table.</span></span> <span data-ttu-id="2884e-127">Например метод [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) требуется глобальное разрешение **NewProject** и разрешение **SaveProjectTemplate** .</span><span class="sxs-lookup"><span data-stu-id="2884e-127">For example, the [Project.QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) method requires the global **NewProject** permission and the **SaveProjectTemplate** permission.</span></span> 
  
   <span data-ttu-id="2884e-128">В некоторых случаях может потребоваться удаленной отладки на сервере.</span><span class="sxs-lookup"><span data-stu-id="2884e-128">In some cases, you may have to do remote debugging on the server.</span></span> <span data-ttu-id="2884e-129">Кроме того, необходимо настроить обработчик событий, установка сборки обработчика событий на каждом компьютере Project Server в ферме SharePoint, а затем настройки обработчика событий для экземпляра Project Web App с помощью страницы параметров Project Server в целом Параметры приложений центра администрирования SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2884e-129">You may also have to set up an event handler by installing an event handler assembly on each Project Server computer in the SharePoint farm, and then configuring the event handler for the Project Web App instance by using the Project Server Settings page in the General Application Settings of SharePoint Central Administration.</span></span>
    
2. <span data-ttu-id="2884e-130">**Настройте компьютер разработчика.**</span><span class="sxs-lookup"><span data-stu-id="2884e-130">**Set up a development computer.**</span></span>
    
   <span data-ttu-id="2884e-p107">Обычно вы осуществляете доступ к PSI по сети. Примеры кода предназначены для выполнения на клиенте, который, кроме особо оговоренных случаев, находится отдельно от сервера.</span><span class="sxs-lookup"><span data-stu-id="2884e-p107">You usually access the PSI through a network. The code samples are designed to be run on a client that is separate from the server, except where noted.</span></span>
    
   1. <span data-ttu-id="2884e-133">**Установите правильную версию Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="2884e-133">**Install the correct version of Visual Studio.**</span></span> <span data-ttu-id="2884e-134">За исключением того, если не указано иное, примеры кода написаны в Visual C#.</span><span class="sxs-lookup"><span data-stu-id="2884e-134">Except where noted, the code samples are written in Visual C#.</span></span> <span data-ttu-id="2884e-135">Они могут использоваться с Visual Studio 2010 или Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="2884e-135">They can be used with Visual Studio 2010 or Visual Studio 2012.</span></span> <span data-ttu-id="2884e-136">Убедитесь, что самым последним пакетом установки.</span><span class="sxs-lookup"><span data-stu-id="2884e-136">Ensure that you have the most recent service pack installed.</span></span> 
        
   2. <span data-ttu-id="2884e-137">**Скопируйте DLL-библиотеки Project Server на компьютере разработчика.**</span><span class="sxs-lookup"><span data-stu-id="2884e-137">**Copy Project Server DLLs to the development computer.**</span></span> <span data-ttu-id="2884e-138">Скопируйте следующие сборки из `[Program Files]\Microsoft Office Servers\15.0\Bin` на сервере Project Server на компьютере разработчика:</span><span class="sxs-lookup"><span data-stu-id="2884e-138">Copy the following assemblies from  `[Program Files]\Microsoft Office Servers\15.0\Bin` on the Project Server computer to the development computer:</span></span> 
        
      - <span data-ttu-id="2884e-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span><span class="sxs-lookup"><span data-stu-id="2884e-139">Microsoft.Office.Project.Server.Events.Receivers.dll</span></span>
      - <span data-ttu-id="2884e-140">Microsoft.Office.Project.Server.Library.dll</span><span class="sxs-lookup"><span data-stu-id="2884e-140">Microsoft.Office.Project.Server.Library.dll</span></span>
        
   3. <span data-ttu-id="2884e-141">Дополнительные сведения о том, как компилировать и использовать сборку прокси-сервера ProjectServerServices.dll для веб-служб ASMX в PSI, см. в статье [Использование сборки прокси-сервера PSI и описаний IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="2884e-141">For information about how to compile and use the ProjectServerServices.dll proxy assembly for the ASMX web services in the PSI, see [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
3. <span data-ttu-id="2884e-142">**Установите файлы IntelliSense.**</span><span class="sxs-lookup"><span data-stu-id="2884e-142">**Install the IntelliSense files.**</span></span>
    
    <span data-ttu-id="2884e-143">Использование описания IntelliSense для классов и членов в Project Server сборки, копия обновленные IntelliSense XML-файлы из пакета SDK Project 2013 Загрузите в ту же папку, где расположены сборки Project Server.</span><span class="sxs-lookup"><span data-stu-id="2884e-143">To use IntelliSense descriptions for classes and members in Project Server assemblies, copy the updated IntelliSense XML files from the Project 2013 SDK download to the same directory where the Project Server assemblies are located.</span></span> <span data-ttu-id="2884e-144">Например скопируйте файл Microsoft.Office.Project.Server.Library.xml в каталог, где приложение будет задать ссылку на сборку Microsoft.Office.Project.Server.Library.dll.</span><span class="sxs-lookup"><span data-stu-id="2884e-144">For example, copy the Microsoft.Office.Project.Server.Library.xml file to the directory where your application will set a reference to the Microsoft.Office.Project.Server.Library.dll assembly.</span></span>
    
    <span data-ttu-id="2884e-145">Описания IntelliSense для веб-службы PSI требуют создания сборкой PSI прокси-сервера с помощью сценария CompileASMXProxyAssembly.cmd в `Documentation\IntelliSense\WSDL` подкаталог в пакет SDK для Project 2013 для загрузки.</span><span class="sxs-lookup"><span data-stu-id="2884e-145">IntelliSense descriptions for the PSI web services require that you create a PSI proxy assembly by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` subdirectory in the Project 2013 SDK download.</span></span> <span data-ttu-id="2884e-146">Сценарий создает сборки на основе ASMX ProjectServerServices.dll прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2884e-146">The script creates the ASMX-based ProjectServerServices.dll proxy assembly.</span></span> <span data-ttu-id="2884e-147">Дополнительные сведения содержатся в файле [ReadMe_IntelliSense] в пакет SDK для загрузки.</span><span class="sxs-lookup"><span data-stu-id="2884e-147">For more information, see the [ReadMe_IntelliSense] file in the SDK download.</span></span> 
    
## <a name="creating-the-application-and-adding-a-web-service-reference"></a><span data-ttu-id="2884e-148">Создание приложения и добавление ссылки на веб-службу</span><span class="sxs-lookup"><span data-stu-id="2884e-148">Creating the application and adding a web service reference</span></span>
<span data-ttu-id="2884e-149"><a name="pj15_PrerequisitesASMX_Configure"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-149"></span></span>

1. <span data-ttu-id="2884e-150">**Создайте консольное приложение**.</span><span class="sxs-lookup"><span data-stu-id="2884e-150">**Create a console application**.</span></span>
    
   <span data-ttu-id="2884e-p112">Когда вы создаете консольное приложение, выберите в раскрывающемся списке диалогового окна **Новый проект** значение **.NET Framework 4**. Вы можете скопировать пример кода PSI в это новое приложение.</span><span class="sxs-lookup"><span data-stu-id="2884e-p112">When you create a console application, in the drop-down list of the **New Project** dialog box, select **.NET Framework 4**. You can copy the PSI example code into the new application.</span></span>
    
2. <span data-ttu-id="2884e-153">**Добавьте необходимую для ASMX ссылку.**</span><span class="sxs-lookup"><span data-stu-id="2884e-153">**Add the reference required for ASMX.**</span></span>
    
   <span data-ttu-id="2884e-154">В обозревателе решений добавьте ссылку на **System.Web.Services** (см. рисунок 1).</span><span class="sxs-lookup"><span data-stu-id="2884e-154">In Solution Explorer, add a reference to **System.Web.Services** (see Figure 1).</span></span> 
    
   <span data-ttu-id="2884e-155">**Рис. 1. Добавление ссылки в Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="2884e-155">**Figure 1. Adding a reference in Visual Studio**</span></span>

   <span data-ttu-id="2884e-156">![Добавление ссылки в Visual Studio] (media/pj15_PrerequisitesASMX_AddReference.gif "Добавление ссылки в Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="2884e-156">![Adding a reference in Visual Studio](media/pj15_PrerequisitesASMX_AddReference.gif "Adding a reference in Visual Studio")</span></span>
  
3. <span data-ttu-id="2884e-157">**Скопируйте код**.</span><span class="sxs-lookup"><span data-stu-id="2884e-157">**Copy the code**.</span></span>
    
   <span data-ttu-id="2884e-158">Скопируйте полный пример кода в файл Program.cs консольного приложения.</span><span class="sxs-lookup"><span data-stu-id="2884e-158">Copy the complete code example into the Program.cs file of the console application.</span></span>
    
4. <span data-ttu-id="2884e-159">**Задайте пространство имен для примера приложения**.</span><span class="sxs-lookup"><span data-stu-id="2884e-159">**Set the namespace for the sample application**.</span></span>
    
   <span data-ttu-id="2884e-p113">Вы можете либо изменить пространство имен, указанное в верхней части примера, на используемое по умолчанию пространство имен приложения, либо изменить используемое по умолчанию пространство имен приложения в соответствии с данным примером. Для изменения используемого по умолчанию пространства имен приложения вы можете изменить свойства приложения.</span><span class="sxs-lookup"><span data-stu-id="2884e-p113">You can either change the namespace listed at the top of the sample to the application default namespace, or change the default application namespace to match the sample. You can change the default application namespace by changing the application properties.</span></span>
    
   <span data-ttu-id="2884e-162">Например образец кода для [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) имеет пространство имен **Microsoft.SDK.Project.Samples.RenameProject**.</span><span class="sxs-lookup"><span data-stu-id="2884e-162">For example, the code sample for [QueueRenameProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueRenameProject.aspx) has the namespace **Microsoft.SDK.Project.Samples.RenameProject**.</span></span> <span data-ttu-id="2884e-163">Если имя проекта Visual Studio **RenameProject**, копирование файла Program.cs пространства имен, а затем откройте панель **свойств** проекта (в меню **проект** выберите пункт **Свойства RenameProject**).</span><span class="sxs-lookup"><span data-stu-id="2884e-163">If the name of the Visual Studio project is **RenameProject**, copy the namespace from the Program.cs file, and then open the project **Properties** pane (on the **Project** menu, choose **RenameProject Properties**).</span></span> <span data-ttu-id="2884e-164">На вкладке **приложение** скопируйте пространства имен в текстовом поле **пространство имен по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="2884e-164">On the **Application** tab, copy the namespace into the **Default namespace** text box.</span></span> 
    
5. <span data-ttu-id="2884e-165">**Задайте веб-ссылки**.</span><span class="sxs-lookup"><span data-stu-id="2884e-165">**Set the web references**.</span></span>
    
   <span data-ttu-id="2884e-p115">Для большинства примеров требуется ссылка на одну или несколько веб-служб PSI. Они указаны в самом примере или в комментариях перед ним. Чтобы получить правильное пространство имен для веб-ссылок, сначала следует задать пространство имен приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2884e-p115">Most examples require a reference to one or more of the PSI web services. These are listed in the sample itself or in comments that precede the sample. To get the correct namespace of the web references, ensure that you first set the default application namespace.</span></span>
    
   <span data-ttu-id="2884e-169">Существует три способа добавить ссылку на веб-службу ASMX для PSI:</span><span class="sxs-lookup"><span data-stu-id="2884e-169">There are three ways to add an ASMX web service reference for the PSI:</span></span>
    
   - <span data-ttu-id="2884e-170">Построения PSI сборки прокси-сервера с именем ProjectServerServices.dll, а затем установите ссылку на сборку.</span><span class="sxs-lookup"><span data-stu-id="2884e-170">Build a PSI proxy assembly named ProjectServerServices.dll, and then set a reference to the assembly.</span></span> <span data-ttu-id="2884e-171">Чтобы получить IntelliSense, это рекомендуемый способ добавить ссылку на интерфейс PSI.</span><span class="sxs-lookup"><span data-stu-id="2884e-171">To get IntelliSense, this is the recommended way to add a PSI reference.</span></span> <span data-ttu-id="2884e-172">В разделе [использование сборки прокси-сервера PSI и описания IntelliSense](#pj15_PrerequisitesASMX_BuildingProxy).</span><span class="sxs-lookup"><span data-stu-id="2884e-172">See [Using a PSI proxy assembly and IntelliSense descriptions](#pj15_PrerequisitesASMX_BuildingProxy).</span></span>
    
   - <span data-ttu-id="2884e-p117">Добавьте файл прокси из выходных данных wsdl.exe в решение Visual Studio. См. статью [Добавление файла прокси PSI](#pj15_PrerequisitesASMX_AddingProxyFile).</span><span class="sxs-lookup"><span data-stu-id="2884e-p117">Add a proxy file from the wsdl.exe output to the Visual Studio solution. See [Adding a PSI proxy file](#pj15_PrerequisitesASMX_AddingProxyFile).</span></span>
    
   - <span data-ttu-id="2884e-p118">Добавьте ссылку на веб-службу с помощью Visual Studio. См. статью [Добавление ссылки на веб-службу](#pj15_PrerequisitesASMX_AddingServiceReference).</span><span class="sxs-lookup"><span data-stu-id="2884e-p118">Add a web service reference by using Visual Studio. See [Adding a web service reference](#pj15_PrerequisitesASMX_AddingServiceReference).</span></span>

<span data-ttu-id="2884e-177"><a name="pj15_PrerequisitesASMX_BuildingProxy"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-177"></span></span>

### <a name="using-a-psi-proxy-assembly-and-intellisense-descriptions"></a><span data-ttu-id="2884e-178">Использование сборки прокси-сервера PSI и описаний IntelliSense</span><span class="sxs-lookup"><span data-stu-id="2884e-178">Using a PSI proxy assembly and IntelliSense descriptions</span></span>

<span data-ttu-id="2884e-179">Можно создавать и использовать сборку ProjectServerServices.dll прокси-сервера для всех на основе ASMX веб-служб в PSI, с помощью сценария CompileASMXProxyAssembly.cmd в `Documentation\IntelliSense\WSDL` папки загружаемого пакета Project 2013 SDK.</span><span class="sxs-lookup"><span data-stu-id="2884e-179">You can build and use the ProjectServerServices.dll proxy assembly for all ASMX-based web services in the PSI, by using the CompileASMXProxyAssembly.cmd script in the  `Documentation\IntelliSense\WSDL` folder of the Project 2013 SDK download.</span></span> <span data-ttu-id="2884e-180">Ссылка на страницу загрузки [Документация для разработчиков Project 2013](project-2013-developer-documentation.md)см.</span><span class="sxs-lookup"><span data-stu-id="2884e-180">For a link to the download, see [Project 2013 developer documentation](project-2013-developer-documentation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="2884e-181">При извлечении исходных файлов прокси-сервера из файл Source.zip файл, файлы в `Documentation\IntelliSense\WSDL\Source` папки текущей даты публикации из загружаемого пакета Project 2013 SDK.</span><span class="sxs-lookup"><span data-stu-id="2884e-181">When you extract the proxy source files from the Source.zip file, the files in the  `Documentation\IntelliSense\WSDL\Source` folder are current as of the publication date of the Project 2013 SDK download.</span></span> <span data-ttu-id="2884e-182">Для создания обновлено PSI прокси-сервер исходные файлы, запустите сценарий GenASMXProxyAssembly.cmd на сервере Project Server.</span><span class="sxs-lookup"><span data-stu-id="2884e-182">To generate updated PSI proxy source files, run the GenASMXProxyAssembly.cmd script on the Project Server computer.</span></span> <span data-ttu-id="2884e-183">Скрипты в `Documentation\IntelliSense\WCF` папки не работают для приложений на основе ASMX.</span><span class="sxs-lookup"><span data-stu-id="2884e-183">The scripts in the  `Documentation\IntelliSense\WCF` folder do not work for ASMX-based applications.</span></span> <span data-ttu-id="2884e-184">Сценарий GenWCFProxyAssembly.cmd вызывает SvcUtil.exe, который создает исходные файлы кода для служб WCF.</span><span class="sxs-lookup"><span data-stu-id="2884e-184">The GenWCFProxyAssembly.cmd script calls SvcUtil.exe, which generates source code files for the WCF services.</span></span> <span data-ttu-id="2884e-185">Файлы прокси-сервера WCF включают различные атрибуты, интерфейс канала и класс клиента для каждой службы PSI.</span><span class="sxs-lookup"><span data-stu-id="2884e-185">The WCF proxy files include different attributes, the channel interface, and a client class for each PSI service.</span></span> <span data-ttu-id="2884e-186">Например службу ресурсов на основе WCF включает в себя интерфейс **ResourceChannel** , интерфейс **ресурсов** и класс **ResourceClient** .</span><span class="sxs-lookup"><span data-stu-id="2884e-186">For example, the WCF-based Resource service includes the **ResourceChannel** interface, the **Resource** interface, and the **ResourceClient** class.</span></span> <span data-ttu-id="2884e-187">В Интернете на основе ASMX ресурсов включает в себя класс **ресурсов** с некоторыми другими свойствами.</span><span class="sxs-lookup"><span data-stu-id="2884e-187">The ASMX-based Resource web includes the **Resource** class with some different properties.</span></span> 
  
<span data-ttu-id="2884e-188">Ниже приведен скрипт GenASMXProxyAssembly.cmd, который создает выходные WSDL-файлы для веб-служб PSI, а затем компилирует сборку.</span><span class="sxs-lookup"><span data-stu-id="2884e-188">Following is the GenASMXProxyAssembly.cmd script that generates WSDL output files for the PSI web services, and then compiles the assembly.</span></span>
  
```MS-DOS
@echo off
@ECHO ---------------------------------------------------
@ECHO Creating C# files for the ASMX-based proxy assembly
@ECHO ---------------------------------------------------
REM Replace ServerName with the name of the server and 
REM the instance name of Project Web App. Do not use localhost.
(set VDIR=https://ServerName/pwa/_vti_bin/psi)
(set OUTDIR=.\Source)
REM ** Wsdl.exe is the same version in the v6.0A and v7.0A subdirectories. 
(set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe")
if not exist %OUTDIR% (
md %OUTDIR%
)
for /F %%i in (Classlist_asmx.txt) do %WSDL% /nologo /l:CS /namespace:Svc%%i /out:%OUTDIR%\wsdl.%%i.cs %VDIR%/%%i.asmx?wsdl 
@ECHO ----------------------------
@ECHO Compiling the proxy assembly
@ECHO ----------------------------
(set SOURCE=%OUTDIR%\wsdl)
(set CSC=%WINDIR%\Microsoft.NET\Framework64\v4.0.30319\csc.exe)
(set ASSEMBLY_NAME=ProjectServerServices.dll)
%CSC% /t:library /out:%ASSEMBLY_NAME% %SOURCE%*.cs
```

<span data-ttu-id="2884e-189">Этот скрипт использует файл ClassList_asmx.txt, который содержит список веб-служб, доступных для сторонних разработчиков.</span><span class="sxs-lookup"><span data-stu-id="2884e-189">The script uses the ClassList_asmx.txt file, which contains the list of web services that are available for third-party developers.</span></span>
  
```text
Admin
Archive
Calendar
CubeAdmin
CustomFields
Driver
Events
LoginForms
LoginWindows
LookupTable
Notifications
ObjectLinkProvider
PortfolioAnalyses
Project
QueueSystem
ResourcePlan
Resource
Security
Statusing
TimeSheet
Workflow
WssInterop
```

<span data-ttu-id="2884e-p121">Скрипты создают сборку с именем ProjectServerServices.dll. Не путайте ее с ProjectServerServices.dll для основанной на WCF сборки. Имена сборок не отличаются, чтобы любую из сборок можно было использовать с файлом IntelliSense ProjectServerServices.xml.</span><span class="sxs-lookup"><span data-stu-id="2884e-p121">The scripts create an assembly named ProjectServerServices.dll. Avoid confusing it with ProjectServerServices.dll for the WCF-based assembly. The assembly names are the same, to enable using either assembly with the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="2884e-p122">Скрипты создают одинаковое произвольное пространство имен как для веб-служб ASMX, так и для служб WCF, поэтому файл IntelliSense ProjectServerServices.xml работает с любой из сборок. Например, пространством имен службы Resource в основанной на WCF сборке прокси-сервера и в основанной на ASMX сборке прокси-сервера является **SvcResource**. Вы, конечно же, можете изменять имена пространств имен, однако при этом нужно следить за тем, чтобы они совпадали в сборке прокси-сервера и в файле IntelliSense ProjectServerServices.xml.</span><span class="sxs-lookup"><span data-stu-id="2884e-p122">The arbitrary namespace created by the scripts for both the ASMX web services and the WCF services is the same, so that the ProjectServerServices.xml IntelliSense file works with either assembly. For example, the namespace of the Resource service in the WCF-based proxy assembly and in the ASMX-based proxy assembly is **SvcResource**. You can, of course, change the namespace names—if you ensure that they match in the proxy assembly and in the ProjectServerServices.xml IntelliSense file.</span></span>
  
<span data-ttu-id="2884e-196">Если пример кода использует для пространства имен веб-службы PSI другое имя, например **ProjectWebSvc**, для работы IntelliSense вам следует изменить данный пример таким образом, чтобы он использовал **SvcProject** и в результате пространство имен соответствовало сборке прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2884e-196">If a code sample uses a different name for a PSI web service namespace, for example **ProjectWebSvc**, for IntelliSense to work you must change the sample to use **SvcProject** so that the namespace matches the proxy assembly.</span></span> 
  
<span data-ttu-id="2884e-197">— Это преимущество сборки прокси-сервера на основе ASMX, что она включает в себя все PSI веб-службы пространства имен; Создание нескольких веб-ссылки не нужно.</span><span class="sxs-lookup"><span data-stu-id="2884e-197">An advantage to using the ASMX-based proxy assembly is that it includes all PSI web service namespaces; you do not have to create multiple web references.</span></span> <span data-ttu-id="2884e-198">Другое преимущество —, что при добавлении в файл ProjectServerServices.xml в тот же каталог, где нужно задать ссылку на сборку ProjectServerServices.dll прокси-сервера, вы можете получить описания IntelliSense для PSI классы и члены.</span><span class="sxs-lookup"><span data-stu-id="2884e-198">Another advantage is that, if you add the ProjectServerServices.xml file to the same directory where you set a reference to the ProjectServerServices.dll proxy assembly, you can get IntelliSense descriptions for the PSI classes and members.</span></span> <span data-ttu-id="2884e-199">На рисунке 2 показано текст IntelliSense для метода **Project.QueueCreateProject** .</span><span class="sxs-lookup"><span data-stu-id="2884e-199">Figure 2 shows the IntelliSense text for the **Project.QueueCreateProject** method.</span></span> <span data-ttu-id="2884e-200">Дополнительные сведения содержатся в файле [ReadMe_IntelliSense] в папке IntelliSense загружаемого пакета Project 2013 SDK.</span><span class="sxs-lookup"><span data-stu-id="2884e-200">For more information, see the [ReadMe_IntelliSense] file in the IntelliSense folder of the Project 2013 SDK download.</span></span> 
  
<span data-ttu-id="2884e-201">**Рис. 2. Использование IntelliSense для метода в веб-службе Project**</span><span class="sxs-lookup"><span data-stu-id="2884e-201">**Figure 2. Using IntelliSense for a method in the Project web service**</span></span>

<span data-ttu-id="2884e-202">![Использование Intellisense для метода в службе PSI] (media/pj15_PrerequisitesASMX_Intellisense.gif "Использование Intellisense для метода в службе PSI")</span><span class="sxs-lookup"><span data-stu-id="2884e-202">![Using Intellisense for a method in a PSI service](media/pj15_PrerequisitesASMX_Intellisense.gif "Using Intellisense for a method in a PSI service")</span></span>
  
<span data-ttu-id="2884e-p124">Недостатки использования этой сборки прокси-сервера заключаются в том, что такое решение больше по размеру, кроме того, вам требуется распространять и устанавливать вместе с ним сборку прокси-сервера. Вам также приходится использовать те же пространства имен, которые указаны в сборке прокси-сервера и файлах IntelliSense, если только вы не измените скрипт и файл IntelliSense ProjectServerServices.xml для использования других пространств имен.</span><span class="sxs-lookup"><span data-stu-id="2884e-p124">Disadvantages to using the proxy assembly are that the solution is larger and you must distribute and install the proxy assembly with the solution. You must also use the same namespaces that are in the proxy assembly and IntelliSense files, unless you change the script and ProjectServerServices.xml IntelliSense file to use different namespaces.</span></span>
  
### <a name="adding-a-psi-proxy-file"></a><span data-ttu-id="2884e-205">Добавление файла прокси PSI</span><span class="sxs-lookup"><span data-stu-id="2884e-205">Adding a PSI proxy file</span></span>
<span data-ttu-id="2884e-206"><a name="pj15_PrerequisitesASMX_AddingProxyFile"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-206"></span></span>

<span data-ttu-id="2884e-207">Загрузить пакет SDK Project 2013 включает в себя исходные файлы, созданные с помощью команды Wsdl.exe для сборки прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="2884e-207">The Project 2013 SDK download includes the source files generated by the Wsdl.exe command for the proxy assembly.</span></span> <span data-ttu-id="2884e-208">Исходные файлы находятся в файл Source.zip в `Documentation\IntelliSense\ASMX` подкаталог.</span><span class="sxs-lookup"><span data-stu-id="2884e-208">The source files are in Source.zip in the  `Documentation\IntelliSense\ASMX` subdirectory.</span></span> <span data-ttu-id="2884e-209">Вместо установки ссылки на сборку прокси-сервера, можно добавить одну или несколько исходных файлов решение Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2884e-209">Instead of setting a reference to the proxy assembly, you can add one or more of the source files to a Visual Studio solution.</span></span> <span data-ttu-id="2884e-210">Например после выполнения сценария GenASMXProxyAssembly.cmd, добавьте wsdl. Файл Project.cs в решение.</span><span class="sxs-lookup"><span data-stu-id="2884e-210">For example, after running the GenASMXProxyAssembly.cmd script, add the wsdl.Project.cs file to the solution.</span></span> <span data-ttu-id="2884e-211">Вместо выполнение скрипта, можно выполните следующие команды для создания одного исходного файла, например:</span><span class="sxs-lookup"><span data-stu-id="2884e-211">Instead of running the script, you can run the following commands to generate a single source file, for example:</span></span> 
  
```MS-DOS
set VDIR=https://ServerName/ProjectServerName/_vti_bin/psi
set WSDL="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin\x64\wsdl.exe"
%WSDL% /nologo /l:cs /namespace:SvcProject /out:wsdl.Project.cs %VDIR%/Project.asmx?wsdl
```

<span data-ttu-id="2884e-p126">Чтобы определить объект **Project** как переменную класса с именем **project**, используйте следующий код. Метод **AddContextInfo** добавляет сведения о контексте в объект **project** для проверки подлинности Windows и проверки подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="2884e-p126">To define a **Project** object as a class variable named **project**, use the following code. The **AddContextInfo** method adds the context information to the **project** object for Windows authentication and Forms-based authentication.</span></span> 
  
```cs
private static SvcProject.Project project;
private static SvcLoginForms.LoginForms loginForms =
            new SvcLoginForms.LoginForms();
. . .
public void AddContextInfo()
{
    // Add the Url property.
    project.Url = "https://ServerName /ProjectServerName /_vti_bin/psi/project.asmx";
    // Add Windows credentials.
    project.Credentials = CredentialCache.DefaultCredentials;
    // If Forms authentication is used, add the Project Server cookie.
    project.CookieContainer = loginForms.CookieContainer;
}
```

> [!NOTE]
> <span data-ttu-id="2884e-214">Используете ли вы сборку прокси-сервера PSI или добавляете файл прокси для ссылки на службу Project с именем **SvcProject**, для создания объекта **project** вы воспользуетесь одним и тем же кодом.</span><span class="sxs-lookup"><span data-stu-id="2884e-214">Whether you use a PSI proxy assembly or add a proxy file for a Project service reference named **SvcProject**, you would use the same code to create a **project** object.</span></span> 
  
### <a name="adding-a-web-service-reference"></a><span data-ttu-id="2884e-215">Добавление ссылки на веб-службу</span><span class="sxs-lookup"><span data-stu-id="2884e-215">Adding a web service reference</span></span>
<span data-ttu-id="2884e-216"><a name="pj15_PrerequisitesASMX_AddingServiceReference"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-216"></span></span>

<span data-ttu-id="2884e-217">Если не использовать прокси-сервер на основе ASMX сборки или добавить WSDL-файла вывода, можно задать один или несколько отдельных веб-ссылки.</span><span class="sxs-lookup"><span data-stu-id="2884e-217">If you do not use the ASMX-based proxy assembly or add a WSDL output file, you can set one or more individual web references.</span></span> <span data-ttu-id="2884e-218">Далее показано, как настроить веб-ссылку с помощью Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="2884e-218">The following steps show how to set a web reference by using Visual Studio 2012.</span></span>
  
1. <span data-ttu-id="2884e-219">В **обозревателе решений** щелкните правой кнопкой мыши папку **Ссылки**, а затем выберите **Добавить ссылку на службу**.</span><span class="sxs-lookup"><span data-stu-id="2884e-219">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Service Reference**.</span></span> 
    
2. <span data-ttu-id="2884e-220">В диалоговом окне **Добавить ссылку на службу** выберите **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="2884e-220">In the **Add Service Reference** dialog box, choose **Advanced**.</span></span>
    
3. <span data-ttu-id="2884e-221">В диалоговом окне **Настройки ссылок на службы** выберите **Добавить веб-ссылку**.</span><span class="sxs-lookup"><span data-stu-id="2884e-221">In the **Service Reference Settings** dialog box, choose **Add Web Reference**.</span></span>
    
4. <span data-ttu-id="2884e-222">В текстовом поле **URL-адрес** введите `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, а затем нажмите клавишу **Ввод** или выберите значок **Переход** .</span><span class="sxs-lookup"><span data-stu-id="2884e-222">In the **URL** text box, type `https:// _ServerName_/ _ProjectServerName_/_vti_bin/psi/ _ServiceName_.asmx?wsdl`, and then press **Enter** or choose the **Go** icon.</span></span> <span data-ttu-id="2884e-223">Если у вас есть Secure Sockets Layer (SSL) установлен, следует использовать протокол HTTPS вместо протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="2884e-223">If you have Secure Sockets Layer (SSL) installed, you should use the HTTPS protocol instead of the HTTP protocol.</span></span> 

   <span data-ttu-id="2884e-224">Например, используйте следующий URL-адрес для службы Project на `https://MyServer/pwa` сайт Project Web App:`https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span><span class="sxs-lookup"><span data-stu-id="2884e-224">For example, use the following URL for the Project service on the  `https://MyServer/pwa` site for Project Web App: `https://MyServer/pwa/_vti_bin/psi/project.asmx?wsdl`</span></span>
    
   <span data-ttu-id="2884e-225">Или, откройте веб-браузер и перейдите к `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span><span class="sxs-lookup"><span data-stu-id="2884e-225">Or, open your web browser, and navigate to `https://ServerName/ProjectServerName/_vti_bin/psi/ServiceName.asmx?wsdl`.</span></span> <span data-ttu-id="2884e-226">Сохраните файл в локальный каталог, таких как `C:\Project\WebServices\ServiceName.wsdl`.</span><span class="sxs-lookup"><span data-stu-id="2884e-226">Save the file to a local directory, such as `C:\Project\WebServices\ServiceName.wsdl`.</span></span> <span data-ttu-id="2884e-227">В диалоговом окне **Добавление веб-ссылки** для **URL-адреса**, введите протокол файла и путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="2884e-227">In the **Add Web Reference** dialog box, for **URL**, type the file protocol and the path to the file.</span></span> <span data-ttu-id="2884e-228">Например, введите `file://C:\Project\WebServices\Project.wsdl`.</span><span class="sxs-lookup"><span data-stu-id="2884e-228">For example, type `file://C:\Project\WebServices\Project.wsdl`.</span></span> 
    
5. <span data-ttu-id="2884e-229">После ссылки разрешаются, введите имя ссылки в текстовом поле **имя веб-ссылки** .</span><span class="sxs-lookup"><span data-stu-id="2884e-229">After the reference resolves, type the reference name in the **Web reference name** text box.</span></span> <span data-ttu-id="2884e-230">Примеры кода в документации для разработчиков по Project 2013 используйте имя произвольных стандартную ссылку **Svc _имя_службы_**.</span><span class="sxs-lookup"><span data-stu-id="2884e-230">Code examples in the Project 2013 developer documentation use the arbitrary standard reference name **Svc _ServiceName_**.</span></span> <span data-ttu-id="2884e-231">Например, проект веб-службы с именем **SvcProject** (см).</span><span class="sxs-lookup"><span data-stu-id="2884e-231">For example, the Project web service is named **SvcProject** (see Figure 3).</span></span> 
    
   <span data-ttu-id="2884e-232">**Рис. 3. Добавление ссылки на веб-службу ASMX**</span><span class="sxs-lookup"><span data-stu-id="2884e-232">**Figure 3. Adding an ASMX web service reference**</span></span>

   <span data-ttu-id="2884e-233">![Добавление службы веб-ASMX] (media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Добавление службы веб-ASMX")</span><span class="sxs-lookup"><span data-stu-id="2884e-233">![Adding an ASMX web service reference](media/pj15_PrerequisitesASMX_AddWebSvcReference.gif "Adding an ASMX web service reference")</span></span>
  
<span data-ttu-id="2884e-234">Для компонентов приложения, которые необходимо выполнить на сервере Project Server применяющих олицетворение, или более высокого разрешения, вместо веб-ASMX использовать ссылки на службу WCF.</span><span class="sxs-lookup"><span data-stu-id="2884e-234">For application components that must run on the Project Server computer, use impersonation, or have elevated permissions, use a WCF service reference instead of an ASMX web reference.</span></span> <span data-ttu-id="2884e-235">Для получения дополнительных сведений см [Необходимые условия для образцов кода на основе WCF в проекте](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="2884e-235">For more information, see [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="setting-other-references"></a><span data-ttu-id="2884e-236">Настройка других ссылок</span><span class="sxs-lookup"><span data-stu-id="2884e-236">Setting other references</span></span>
<span data-ttu-id="2884e-237"><a name="pj15_PrerequisitesASMX_OtherReferences"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-237"></span></span>

<span data-ttu-id="2884e-238">Приложения Project Server часто используют другие службы, такие как веб-служб SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2884e-238">Project Server applications often use other services, such as SharePoint Server 2013 web services.</span></span> <span data-ttu-id="2884e-239">Если требуются другие службы, они указаны в примере.</span><span class="sxs-lookup"><span data-stu-id="2884e-239">If other services are required, they are noted in the example.</span></span>
  
<span data-ttu-id="2884e-240">Локальные ссылки для примера кода указаны в операторах **using** в верхней части примера:</span><span class="sxs-lookup"><span data-stu-id="2884e-240">Local references for the code sample are listed in **using** statements at the top of the sample:</span></span> 
  
1. <span data-ttu-id="2884e-241">В **обозревателе решений** щелкните правой кнопкой мыши папку **Ссылки**, а затем выберите **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="2884e-241">In **Solution Explorer**, right-click the **References** folder, and then choose **Add Reference**.</span></span>
    
2. <span data-ttu-id="2884e-p133">Нажмите кнопку **Обзор** и перейдите в расположение, где вы сохранили скопированные ранее библиотеки DLL Project Server. Выберите требуемые библиотеки DLL и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2884e-p133">Choose **Browse**, and then browse to the location where you stored the Project Server DLLs that you copied previously. Choose the DLLs you need, and then choose **OK**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="2884e-244">Убедитесь, что версии сборки на компьютере разработки точно соответствуют версиям сборки на конечном компьютере Project Server.</span><span class="sxs-lookup"><span data-stu-id="2884e-244">Ensure that the assembly versions on your development computer exactly match those on the target Project Server computer.</span></span> 
  
## <a name="using-multiple-authentication"></a><span data-ttu-id="2884e-245">Использование нескольких методов проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="2884e-245">Using multiple authentication</span></span>
<span data-ttu-id="2884e-246"><a name="pj15_PrerequisitesASMX_ClaimsMultiAuth"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-246"></span></span>

<span data-ttu-id="2884e-247">Проверка подлинности пользователей локального сервера Project Server, проверка подлинности Windows или проверки подлинности форм по осуществляется с помощью утверждений обработки в SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2884e-247">Authentication of on-premises Project Server users, whether by Windows authentication or Forms authentication, is done through claims processing in SharePoint Server 2013.</span></span> <span data-ttu-id="2884e-248">Несколько проверка подлинности означает, что веб-приложения, где был подготовлен Project Web App поддерживает проверку подлинности Windows и проверка подлинности на основе форм.</span><span class="sxs-lookup"><span data-stu-id="2884e-248">Multiple authentication means that the web application on which Project Web App is provisioned supports both Windows authentication and Forms-based authentication.</span></span> <span data-ttu-id="2884e-249">Если это так, вызов веб-службы ASMX, использующего проверку подлинности Windows завершится с ошибкой из-за ошибки, так как процесс утверждения не может определить, какой тип пользователя для проверки подлинности:</span><span class="sxs-lookup"><span data-stu-id="2884e-249">If that is the case, a call to an ASMX web service that uses Windows authentication will fail with the following error, because the claims process cannot determine which type of user to authenticate:</span></span>
  
`The server was unable to process the request due to an internal error. . . .`

<span data-ttu-id="2884e-p135">Чтобы устранить эту проблему с ASMX, все вызовы в методы PSI должны направляться в производный класс, который определен для каждой веб-службы PSI. Этот производный класс также должен использовать класс **SvcLoginWindows.LoginWindows**, чтобы получить файл cookie для производного класса служб PSI. В следующем примере класс **ProjectDerived** является производным от класса **SvcProject.Project**. Этот производный класс добавляет свойство **EnforceWindowsAuth** и переопределяет заголовок веб-запроса для каждого вызова в метод в классе **Project**. Если свойство **EnforceWindowsAuth** имеет значение **true**, метод **GetWebRequest** добавляет заголовок, отключающий проверку подлинности на основе форм. Если **EnforceWindowsAuth** имеет значение **false**, выполнение проверки подлинности на основе форм разрешается.</span><span class="sxs-lookup"><span data-stu-id="2884e-p135">To fix the problem for ASMX, all calls to PSI methods should be to a derived class that is defined for each PSI web service. The derived class must also use the **SvcLoginWindows.LoginWindows** class to get a cookie for the derived PSI service class. In the following example, the **ProjectDerived** class derives from the **SvcProject.Project** class. The derived class adds the **EnforceWindowsAuth** property and overrides the web request header for every call to a method in the **Project** class. If the **EnforceWindowsAuth** property is **true**, the **GetWebRequest** method adds a header that disables Forms authentication. If **EnforceWindowsAuth** is **false**, Forms authentication can proceed.</span></span>
  
<span data-ttu-id="2884e-p136">Чтобы использовать следующий пример **ASMXLogon_MultiAuth**, создайте консольное приложение, выполните действия из раздела [Создание приложения и добавление ссылки на веб-службу](#pj15_PrerequisitesASMX_Configure), а затем добавьте файл прокси wsdl.LoginWindows.cs и файл прокси wsdl.Project.cs. Метод **Main** создает экземпляр **project** класса **ProjectDerived**. Этот пример должен использовать производный класс **LoginWindowsDerived** для получения объекта **CookieContainer** для свойства **project.CookieContainer**, которое позволяет отличить проверку подлинности на основе форм от проверки подлинности Windows. После этого объект **project** можно использовать для выполнения вызовов в любой метод в классе **SvcProject.Project**.</span><span class="sxs-lookup"><span data-stu-id="2884e-p136">To use the following **ASMXLogon_MultiAuth** sample, create a console application, follow the steps in [Creating the application and adding a web service reference](#pj15_PrerequisitesASMX_Configure), and then add the wsdl.LoginWindows.cs proxy file and the wsdl.Project.cs proxy file. The **Main** method creates the **project** instance of the **ProjectDerived** class. The sample must use the derived **LoginWindowsDerived** class to get a **CookieContainer** object for the **project.CookieContainer** property, which distinguishes Forms authentication from Windows authentication. The **project** object can then be used to make calls to any method in the **SvcProject.Project** class.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2884e-p137">Служба **LoginWindows** необходима только для приложений ASMX в среде с несколькими методами проверки подлинности. В примере **ASMXLogon_MultiAuth** метод **GetLogonCookie** получает файл cookie для объекта **loginWindows**. Для свойства **project.CookieContainer** устанавливается значение **loginWindows.CookieContainer**.</span><span class="sxs-lookup"><span data-stu-id="2884e-p137">The **LoginWindows** service is required only for ASMX applications in a multiple authentication environment. In the **ASMXLogon_MultiAuth** sample, the **GetLogonCookie** method gets a cookie for the **loginWindows** object. The **project.CookieContainer** property is set to the **loginWindows.CookieContainer** value.</span></span> 
  
```cs
using System;
using System.Net;
using PSLibrary = Microsoft.Office.Project.Server.Library;
namespace ASMXLogon_MultiAuth
{
    class Program
    {
        private const string PROJECT_SERVER_URL = 
            "https://ServerName/ProjectServerName/_vti_bin/psi/";
        static void Main(string[] args)
        {
            bool isWindowsUser = true;
            // Create an instance of the project object.
            ProjectDerived project = new ProjectDerived();
            project.Url = PROJECT_SERVER_URL + "Project.asmx";
            project.Credentials = CredentialCache.DefaultCredentials;
            try
            {
                // The program works on a Windows-auth-only computer if you comment-out the
                // following line. The line is required for multiple authentication.
                project.CookieContainer = GetLogonCookie();
                project.EnforceWindowsAuth = isWindowsUser;
                // Get a list of all published projects. 
                // Use ReadProjectStatus instead of ReadProjectList,
                // because the permission requirements are lower.
                SvcProject.ProjectDataSet projectDs =
                    project.ReadProjectStatus(Guid.Empty,
                        SvcProject.DataStoreEnum.PublishedStore,
                        string.Empty,
                        (int)PSLibrary.Project.ProjectType.Project);
                Console.WriteLine(string.Format(
                    "There are {0} published projects.", 
                    projectDs.Project.Rows.Count));
            }
            catch (UnauthorizedAccessException ex)
            {
                Console.WriteLine(ex.Message);
            }
            catch (WebException ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                Console.Write("Press any key to continue...");
                Console.ReadKey(false);
            }
        }
        private static CookieContainer GetLogonCookie()
        {
            // Create an instance of the loginWindows object.
            LoginWindowsDerived loginWindows = new LoginWindowsDerived();
            loginWindows.EnforceWindowsAuth = true;
            loginWindows.Url = PROJECT_SERVER_URL + "LoginWindows.asmx";
            loginWindows.Credentials = CredentialCache.DefaultCredentials;
            loginWindows.CookieContainer = new CookieContainer();
            if (!loginWindows.Login())
            {
                // Login failed; throw an exception.
                throw new UnauthorizedAccessException("Login failed.");
            }
            return loginWindows.CookieContainer;
        }
    }
    // Derive from LoginWindows class; include additional property and 
    // override the web request header.
    class LoginWindowsDerived : SvcLoginWindows.LoginWindows
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
    // Derive from Project class; include additional property and 
    // override the web request header.
    class ProjectDerived : SvcProject.Project
    {
        public bool EnforceWindowsAuth { get; set; }
        protected override WebRequest GetWebRequest(Uri uri)
        {
            WebRequest request = base.GetWebRequest(uri);
            if (this.EnforceWindowsAuth)
            {
                request.Headers.Add("X-FORMS_BASED_AUTH_ACCEPTED", "f");
            }
            return request;
        }
    }
}
```

<span data-ttu-id="2884e-p138">Использование производного класса **LoginWindows** и выполнение вызовов PSI с заголовком веб-запроса, отключающим проверку подлинности на основе форм необходимы для приложений, которые выполняются в среде с несколькими методами проверки подлинности. Если Project Server использует только проверку подлинности на основе утверждений, производный класс, добавляющий заголовок веб-запроса, не требуется. Предыдущий пример подходит для использования в обеих средах.</span><span class="sxs-lookup"><span data-stu-id="2884e-p138">Using the derived **LoginWindows** class, and making PSI calls with a web request header that disables Forms authentication, is required for applications that run in a multiple authentication environment. If Project Server uses only claims authentication, it is not necessary to derive a class that adds a web request header. The previous example runs in both environments.</span></span> 
  
<span data-ttu-id="2884e-266">Исправление для приложения на основе WCF отличается.</span><span class="sxs-lookup"><span data-stu-id="2884e-266">The fix for a WCF-based application is different.</span></span> <span data-ttu-id="2884e-267">Для получения дополнительных сведений обратитесь к разделу *с использованием нескольких проверки подлинности* в [Необходимые условия для образцов кода на основе WCF в проекте](prerequisites-for-wcf-based-code-samples-in-project.md).</span><span class="sxs-lookup"><span data-stu-id="2884e-267">For more information, see the  *Using multiple authentication*  section in [Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md).</span></span>
  
## <a name="changing-the-values-of-generic-constants"></a><span data-ttu-id="2884e-268">Изменение значений общих констант</span><span class="sxs-lookup"><span data-stu-id="2884e-268">Changing the values of generic constants</span></span>
<span data-ttu-id="2884e-269"><a name="pj15_PrerequisitesASMX_ChangeValues"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-269"></span></span>

<span data-ttu-id="2884e-270">Большинство образцов имеет один или несколько переменных, которые необходимо обновить образец работал надлежащим образом в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="2884e-270">Most samples have one or more variables that you must update for the sample to work properly in your environment.</span></span> <span data-ttu-id="2884e-271">В следующем примере Если протокол SSL, используйте протокол HTTPS вместо протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="2884e-271">In the following example, if you have SSL installed, use the HTTPS protocol instead of the HTTP protocol.</span></span> <span data-ttu-id="2884e-272">Замените _имя сервера_ имя сервера, на котором вы используете.</span><span class="sxs-lookup"><span data-stu-id="2884e-272">Replace  _ServerName_ with the name of the server that you are using.</span></span> <span data-ttu-id="2884e-273">Замените _ProjectServerName_ имя виртуального каталога веб-узла Project Server, например веб-клиента Project.</span><span class="sxs-lookup"><span data-stu-id="2884e-273">Replace  _ProjectServerName_ with the virtual directory name of your Project Server site, such as PWA.</span></span> 
  
```cs
const string PROJECT_SERVER_URI = "https://ServerName/ProjectServerName/";
```

<span data-ttu-id="2884e-274">Все остальные переменные, которые вам следует изменить, или иные предварительные требования указаны в верхней части примера кода.</span><span class="sxs-lookup"><span data-stu-id="2884e-274">Any other variables that you must change or other prerequisites are noted at the top of the code example.</span></span>
  
## <a name="verifying-the-results"></a><span data-ttu-id="2884e-275">Проверка результатов</span><span class="sxs-lookup"><span data-stu-id="2884e-275">Verifying the results</span></span>
<span data-ttu-id="2884e-276"><a name="pj15_PrerequisitesASMX_Verify"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-276"></span></span>

<span data-ttu-id="2884e-277">Получение и интерпретации результатов из примера кода не всегда просто.</span><span class="sxs-lookup"><span data-stu-id="2884e-277">Getting and interpreting results from a code sample is not always straightforward.</span></span> <span data-ttu-id="2884e-278">Например при создании проекта, необходимо опубликовать проект, чтобы оно может отображаться на странице центра проектов в Project Web App.</span><span class="sxs-lookup"><span data-stu-id="2884e-278">For example, if you create a project, you must publish the project before it can appear on the Project Center page in Project Web App.</span></span>
  
<span data-ttu-id="2884e-279">Вы можете проверить результаты примера кода несколькими различными способами, например:</span><span class="sxs-lookup"><span data-stu-id="2884e-279">You can verify code sample results in several ways, for example:</span></span>
  
- <span data-ttu-id="2884e-280">Просмотр элементов, которые будут использовать клиента Project Professional 2013 для откройте проект на сервере Project Server</span><span class="sxs-lookup"><span data-stu-id="2884e-280">Use the Project Professional 2013 client to open the project from the Project Server computer, and view the items that you want.</span></span>
    
- <span data-ttu-id="2884e-281">Просмотр опубликованных проектов на странице центра проектов Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).</span><span class="sxs-lookup"><span data-stu-id="2884e-281">View published projects on the Project Center page of Project Web App ( `https://ServerName/ProjectServerName/projects.aspx`).</span></span>
    
- <span data-ttu-id="2884e-282">Просмотр журнала очереди в Project Web App.</span><span class="sxs-lookup"><span data-stu-id="2884e-282">View the Queue log in Project Web App.</span></span> <span data-ttu-id="2884e-283">Открыть страницу "Параметры сервера" (в верхнем правом углу щелкните значок **Параметры** ), а затем выберите **Мои задания в очереди** в разделе **Личные параметры** ( `https://ServerName/ProjectServerName/MyJobs.aspx`).</span><span class="sxs-lookup"><span data-stu-id="2884e-283">Open the Server Settings page (choose the **Settings** icon in the top-right corner), and then choose **My Queued Jobs** under the **Personal Settings** section (  `https://ServerName/ProjectServerName/MyJobs.aspx`).</span></span> <span data-ttu-id="2884e-284">В раскрывающемся списке **представление** можно сортировать по состояние задания.</span><span class="sxs-lookup"><span data-stu-id="2884e-284">In the **View** drop-down list, you can sort by the job status.</span></span> <span data-ttu-id="2884e-285">Состояние по умолчанию — **в ходе выполнения и произошел сбой задания за прошлую неделю**.</span><span class="sxs-lookup"><span data-stu-id="2884e-285">The default status is **In Progress and Failed Jobs in the Past Week**.</span></span> 
    
- <span data-ttu-id="2884e-286">Используйте страницу параметров сервера в Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) для управления заданиями в очереди и удаления или принудительный возврат корпоративных объектов.</span><span class="sxs-lookup"><span data-stu-id="2884e-286">Use the Server Settings page in Project Web App ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`) to manage all queue jobs and delete or force check-in enterprise objects.</span></span> <span data-ttu-id="2884e-287">Необходимо иметь разрешения администратора для доступа к этих ссылок на странице "Параметры сервера".</span><span class="sxs-lookup"><span data-stu-id="2884e-287">You must have administrative permissions to access those links on the Server Settings page.</span></span>
    
- <span data-ttu-id="2884e-p144">Используйте **Microsoft SQL Server Management Studio**, чтобы выполнить запрос для таблицы в базе данных Project. Например, используйте следующий запрос, чтобы выбрать 200 верхних строк таблицы pub.MSP_WORKFLOW_STAGE_PDPS для отображения информации о страницах сведений о проектах (PDP) в этапах рабочего проекта.</span><span class="sxs-lookup"><span data-stu-id="2884e-p144">Use **Microsoft SQL Server Management Studio** to run a query on a table in the Project database. For example, use the following query to select the top 200 rows of the pub.MSP_WORKFLOW_STAGE_PDPS table to show information about the project detail pages (PDPs) in workflow stages.</span></span> 
    
   ```sql
    SELECT TOP 200 [STAGE_UID]
            ,[PDP_UID]
            ,[PDP_NAME]
            ,[PDP_POSITION]
            ,[PDP_ID]
            ,[PDP_STAGE_DESCRIPTION]
            ,[PDP_REQUIRES_ATTENTION]
        FROM [ProjectService].[pub].[MSP_WORKFLOW_STAGE_PDPS]
   ```

## <a name="cleaning-up"></a><span data-ttu-id="2884e-290">Очистка</span><span class="sxs-lookup"><span data-stu-id="2884e-290">Cleaning up</span></span>
<span data-ttu-id="2884e-291"><a name="pj15_PrerequisitesASMX_Cleanup"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-291"></span></span>

<span data-ttu-id="2884e-292">После тестирования некоторые примеры кода существует корпоративных объектов и параметров, которые следует удалить или сбросить.</span><span class="sxs-lookup"><span data-stu-id="2884e-292">After you test some code samples, there are enterprise objects and settings that should be deleted or reset.</span></span> <span data-ttu-id="2884e-293">На странице "Параметры сервера" в Project Web App можно использовать для управления корпоративными данными ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span><span class="sxs-lookup"><span data-stu-id="2884e-293">You can use the Server Settings page in Project Web App to manage enterprise data ( `https://ServerName/ProjectServerName/_layouts/15/pwa/admin/admin.aspx`).</span></span> <span data-ttu-id="2884e-294">Ссылки на странице "Параметры сервера" позволяет удалять старые элементы, принудительный возврат проектов, управлять очередь заданий для всех пользователей и выполнять другие задачи администрирования.</span><span class="sxs-lookup"><span data-stu-id="2884e-294">Links on the Server Settings page enable you to delete old items, force check-in projects, manage the job queue for all users, and perform other administrative tasks.</span></span>
  
<span data-ttu-id="2884e-295">Ниже приведено несколько ссылок на страницу параметров сервера, которые вы можете использовать для выполнения стандартных операций очистки после запуска примеров кода:</span><span class="sxs-lookup"><span data-stu-id="2884e-295">Following are some of the links on the Server Settings page that you can use for typical cleanup activities after running code samples:</span></span>
  
- <span data-ttu-id="2884e-296">**Корпоративные настраиваемые поля и таблицы подстановки**</span><span class="sxs-lookup"><span data-stu-id="2884e-296">**Enterprise Custom Fields and Lookup Tables**</span></span>
    
- <span data-ttu-id="2884e-297">**Управление заданиями в очереди**</span><span class="sxs-lookup"><span data-stu-id="2884e-297">**Manage Queue Jobs**</span></span>
    
- <span data-ttu-id="2884e-298">**Удаление корпоративных объектов**</span><span class="sxs-lookup"><span data-stu-id="2884e-298">**Delete Enterprise Objects**</span></span>
    
- <span data-ttu-id="2884e-299">**Принудительное возвращение корпоративных объектов**</span><span class="sxs-lookup"><span data-stu-id="2884e-299">**Force Check-in Enterprise Objects**</span></span>
    
- <span data-ttu-id="2884e-300">**Типы корпоративных проектов**</span><span class="sxs-lookup"><span data-stu-id="2884e-300">**Enterprise Project Types**</span></span>
    
- <span data-ttu-id="2884e-301">**Этапы рабочего процесса**</span><span class="sxs-lookup"><span data-stu-id="2884e-301">**Workflow Phases**</span></span>
    
- <span data-ttu-id="2884e-302">**Этапы рабочего процесса**</span><span class="sxs-lookup"><span data-stu-id="2884e-302">**Workflow Stages**</span></span>
    
- <span data-ttu-id="2884e-303">**Страницы сведений о проекте**</span><span class="sxs-lookup"><span data-stu-id="2884e-303">**Project Detail Pages**</span></span>
    
- <span data-ttu-id="2884e-304">**Отчетные периоды времени**</span><span class="sxs-lookup"><span data-stu-id="2884e-304">**Time Reporting Periods**</span></span>
    
- <span data-ttu-id="2884e-305">**Параметры и значения по умолчанию для расписания**</span><span class="sxs-lookup"><span data-stu-id="2884e-305">**Timesheet Settings and Defaults**</span></span>
    
- <span data-ttu-id="2884e-306">**Классификация строк**</span><span class="sxs-lookup"><span data-stu-id="2884e-306">**Line Classifications**</span></span>
    
<span data-ttu-id="2884e-307">Дополнительные параметры управляются с SharePoint Server 2013 для каждого экземпляра Project Web App, а не с определенной странице Параметры сервера Project Web App.</span><span class="sxs-lookup"><span data-stu-id="2884e-307">Additional settings are managed by SharePoint Server 2013 for each Project Web App instance, rather than by a specific Project Web App Server Settings page.</span></span> <span data-ttu-id="2884e-308">В приложения центра администрирования SharePoint выберите **Общие параметры приложения**, выберите **Управление** в разделе **Параметры Project Server**и затем в раскрывающемся списке на странице "Параметры сервера" нажмите кнопку экземпляр Project Web App .</span><span class="sxs-lookup"><span data-stu-id="2884e-308">In the SharePoint Central Administration application, choose **General Application Settings**, choose **Manage** under **Project Server Settings**, and then choose the Project Web App instance in the drop-down list on the Server Settings page.</span></span> <span data-ttu-id="2884e-309">Например выберите **Обработчики событий на стороне сервера** , чтобы добавить или удалить обработчики событий для выбранного экземпляра Project Web App.</span><span class="sxs-lookup"><span data-stu-id="2884e-309">For example, choose **Server Side Event Handlers** to add or delete event handlers for the selected Project Web App instance.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2884e-310">См. также</span><span class="sxs-lookup"><span data-stu-id="2884e-310">See also</span></span>
<span data-ttu-id="2884e-311"><a name="pj15_PrerequisitesASMX_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="2884e-311"></span></span>

- [<span data-ttu-id="2884e-312">Необходимые условия для примеров кода на основе WCF в Project</span><span class="sxs-lookup"><span data-stu-id="2884e-312">Prerequisites for WCF-based code samples in Project</span></span>](prerequisites-for-wcf-based-code-samples-in-project.md)
- [<span data-ttu-id="2884e-313">Использование олицетворения с WCF</span><span class="sxs-lookup"><span data-stu-id="2884e-313">Use Impersonation with WCF</span></span>](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
- [<span data-ttu-id="2884e-314">Справочный обзор PSI Project</span><span class="sxs-lookup"><span data-stu-id="2884e-314">Project PSI reference overview</span></span>](project-psi-reference-overview.md)
- [<span data-ttu-id="2884e-315">Центр по разработке для SharePoint</span><span class="sxs-lookup"><span data-stu-id="2884e-315">SharePoint Developer Center</span></span>](https://msdn.microsoft.com/sharepoint/default.aspx)
    

