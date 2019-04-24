---
title: Разработка с помощью Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Вы можете значительно улучшить функциональные возможности форм InfoPath, расширяя их с помощью управляемого кода, разработанного в Visual Studio 2012. После этого вы можете опубликовать формы с помощью кода в библиотеках форм в SharePoint Server 2013.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300289"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="84217-104">Разработка с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="84217-104">Develop with Visual Studio</span></span>

<span data-ttu-id="84217-105">Вы можете значительно улучшить функциональные возможности форм InfoPath, расширяя их с помощью управляемого кода, разработанного в Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="84217-105">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012.</span></span> <span data-ttu-id="84217-106">После этого вы можете опубликовать формы с помощью кода в библиотеках форм в SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="84217-106">You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="84217-107">Для начала программирования и развертывания форм InfoPath с управляемым кодом необходимо выполнить три основных действия:</span><span class="sxs-lookup"><span data-stu-id="84217-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="84217-108">Установите Visual Studio 2012 с надстройкой [Microsoft Visual Studio Tools for applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) .</span><span class="sxs-lookup"><span data-stu-id="84217-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="84217-109">Задайте язык программирования, а затем напишите и отладить код в редакторе кода Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="84217-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="84217-110">Завершив разработку формы и разработку кода, шаблон формы можно опубликовать в SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="84217-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="84217-111">Ниже приведены причины, по которым рекомендуется создавать формы, совместимые с SharePoint Server 2013:</span><span class="sxs-lookup"><span data-stu-id="84217-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="84217-112">Формы, развернутые в SharePoint Server 2013 с помощью InfoPath Forms Services, могут быть заполнены в браузере.</span><span class="sxs-lookup"><span data-stu-id="84217-112">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser.</span></span> <span data-ttu-id="84217-113">Это позволяет пользователям, у которых не установлено приложение InfoPath, открывать и использовать свои формы.</span><span class="sxs-lookup"><span data-stu-id="84217-113">This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="84217-114">Вы разрабатываете только одну версию формы.</span><span class="sxs-lookup"><span data-stu-id="84217-114">You design only one version of the form.</span></span> <span data-ttu-id="84217-115">Формы, совместимые с Microsoft SharePoint Server, также совместимы с InfoPath Filler, но формы, совместимые с InfoPath Filler, не могут быть открыты в браузере.</span><span class="sxs-lookup"><span data-stu-id="84217-115">Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="84217-116">Существует два способа публикации формы в SharePoint: изолированные решения SharePoint и решения, развернутые администратором.</span><span class="sxs-lookup"><span data-stu-id="84217-116">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions.</span></span> <span data-ttu-id="84217-117">Дополнительные сведения о каждом методе публикации и предложениях, наиболее подходящие для вашего сценария, приведены [в статье Публикация форм с помощью кода](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="84217-117">For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span> <span data-ttu-id="84217-118">Примеры решений для изолированных решений вы найдете в статье [примеры изолированНых решений](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="84217-118">For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="84217-119">Разработка с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="84217-119">Developing with Visual Studio</span></span>

<span data-ttu-id="84217-120">С помощью Visual Studio 2012 и надстройки Microsoft Visual Studio Tools for Applications 2012 вы готовы приступить к разработке решений InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="84217-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="84217-121">Выбор языка программирования</span><span class="sxs-lookup"><span data-stu-id="84217-121">Choosing a Programming Language</span></span>

<span data-ttu-id="84217-122">InfoPath предоставляет возможности для программирования с помощью четырех версий объектной модели InfoPath на двух языках: Visual Basic и C#.</span><span class="sxs-lookup"><span data-stu-id="84217-122">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#.</span></span> <span data-ttu-id="84217-123">Четыре версии объектной модели обеспечивают совместимость с InfoPath 2013, InfoPath, Office InfoPath 2007 и Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="84217-123">The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="84217-124">Указание языка программирования и объектной модели</span><span class="sxs-lookup"><span data-stu-id="84217-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="84217-125">Откройте проект шаблона формы в конструкторе InfoPath и выберите **язык** на вкладке **разработчик** .</span><span class="sxs-lookup"><span data-stu-id="84217-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="84217-126">В категории **Программирование** диалогового окна **Параметры формы** выберите используемый язык из раскрывающегося списка **Язык кода шаблона формы**.</span><span class="sxs-lookup"><span data-stu-id="84217-126">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list.</span></span> <span data-ttu-id="84217-127">Затем выберите версию объектной модели из раскрывающегося списка **конечная версия** .</span><span class="sxs-lookup"><span data-stu-id="84217-127">Then, select the version of the object model from the **Target version** drop-down list.</span></span> <span data-ttu-id="84217-128">В параметре **целевой версии** , совместимом только с InfoPath 2013, не указан год, который следует за именем **InfoPath** .</span><span class="sxs-lookup"><span data-stu-id="84217-128">The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="84217-129">Код поддерживается не всеми типами шаблонов форм.</span><span class="sxs-lookup"><span data-stu-id="84217-129">Not all form template types support code.</span></span> <span data-ttu-id="84217-130">Например, типы шаблона формы **Список SharePoint** и **Блоки шаблона** не поддерживают код формы.</span><span class="sxs-lookup"><span data-stu-id="84217-130">For example, the **SharePoint List** form template type and **Template Parts** do not support form code.</span></span> <span data-ttu-id="84217-131">При разработке типа шаблона, не поддерживающего код, вкладка **Разработчик** не будет доступна.</span><span class="sxs-lookup"><span data-stu-id="84217-131">When designing a form template type that does not support code, the **Developer** tab will not be available.</span></span> <span data-ttu-id="84217-132">Кроме того, только некоторые типы шаблонов форм поддерживают все четыре версии объектной модели.</span><span class="sxs-lookup"><span data-stu-id="84217-132">Also, only some form template types support all four versions of the object model.</span></span> <span data-ttu-id="84217-133">Например, тип шаблона " **пустАя форма" (InfoPath Filler)** поддерживает все четыре версии объектной модели (и создает шаблон формы, совместимый только с InfoPath Filler в этих версиях), но **пустой шаблон формы** поддерживает только InfoPath 2013 и InfoPath (и создает шаблоны форм, совместимые с InfoPath Filler и браузером).</span><span class="sxs-lookup"><span data-stu-id="84217-133">For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="84217-134">Вы можете задать язык программирования по умолчанию, чтобы конструктор форм InfoPath всегда начинался с выбранной вами версией языка и объектной модели.</span><span class="sxs-lookup"><span data-stu-id="84217-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="84217-135">Настройка языка программирования по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84217-135">To set the default programming language</span></span>

1. <span data-ttu-id="84217-136">Щелкните вкладку **Файл**, а затем щелкните элемент **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="84217-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="84217-137">В разделе **Общие** диалогового окна **Параметры InfoPath** щелкните элемент **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="84217-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="84217-138">На вкладке **Разработка** диалогового окна **Параметры** выберите язык программирования по умолчанию в разделе **Параметры программирования по умолчанию**. </span><span class="sxs-lookup"><span data-stu-id="84217-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="84217-139">Написание кода</span><span class="sxs-lookup"><span data-stu-id="84217-139">Writing Code</span></span>

<span data-ttu-id="84217-140">Теперь вы можете начать разработку с помощью InfoPath 2013 и Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="84217-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="84217-141">Запуск редактора кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="84217-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="84217-142">Откройте шаблон формы в конструкторе InfoPath.</span><span class="sxs-lookup"><span data-stu-id="84217-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="84217-143">Щелкните элемент **Редактор кода** на вкладке **Разработчик**.</span><span class="sxs-lookup"><span data-stu-id="84217-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="84217-144">Кроме того, можно запустить редактор кода и автоматически добавлять обработчики событий для событий форм и элементов управления с помощью команд на вкладке **разработчик** , контекстные меню и другие методы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="84217-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="84217-145">Дополнительные сведения см. [в статье Добавление обработчика событий](how-to-add-an-event-handler.md)</span><span class="sxs-lookup"><span data-stu-id="84217-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

