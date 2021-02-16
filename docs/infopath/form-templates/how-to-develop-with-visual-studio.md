---
title: Разработка с помощью Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Вы можете значительно расширить функциональные возможности форм InfoPath, расширив их с помощью управляемого кода, разработанного в Visual Studio 2012. Затем можно опубликовать формы с кодом в библиотеках форм в SharePoint Server 2013.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300289"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="7d6d8-104">Разработка с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7d6d8-104">Develop with Visual Studio</span></span>

<span data-ttu-id="7d6d8-105">Вы можете значительно расширить функциональные возможности форм InfoPath, расширив их с помощью управляемого кода, разработанного в Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-105">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012.</span></span> <span data-ttu-id="7d6d8-106">Затем можно опубликовать формы с кодом в библиотеках форм в SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-106">You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="7d6d8-107">Для начала программирования и развертывания форм InfoPath с управляемым кодом необходимо выполнить три основных действия:</span><span class="sxs-lookup"><span data-stu-id="7d6d8-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="7d6d8-108">Установите Visual Studio 2012 с набор средств Microsoft Visual Studio Tools для работы с приложениями [2012.](https://www.microsoft.com/en-us/download/details.aspx?id=38807)</span><span class="sxs-lookup"><span data-stu-id="7d6d8-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="7d6d8-109">Запишите язык программирования и напишите код в редакторе Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="7d6d8-110">После завершения разработки формы и разработки кода шаблон формы можно опубликовать в SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="7d6d8-111">Вот несколько причин, по которой следует рассмотреть создание форм, совместимых с SharePoint Server 2013:</span><span class="sxs-lookup"><span data-stu-id="7d6d8-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="7d6d8-112">Формы, развернутые в SharePoint Server 2013 с InfoPath Forms Services можно заполнять в браузере.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-112">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser.</span></span> <span data-ttu-id="7d6d8-113">Это позволяет пользователям, у которых не установлен InfoPath, открывать и использовать формы.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-113">This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="7d6d8-114">Вы можете разработать только одну версию формы.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-114">You design only one version of the form.</span></span> <span data-ttu-id="7d6d8-115">Формы, совместимые с Microsoft SharePoint Server, также совместимы с InfoPath Filler, но формы, совместимые только с InfoPath Filler, невозможно открыть в браузере.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-115">Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="7d6d8-116">Существует два способа публикации формы в SharePoint: решения в песочнице SharePoint и решения, развернутые администратором.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-116">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions.</span></span> <span data-ttu-id="7d6d8-117">Дополнительные сведения о каждом методе публикации и предложения о том, какой метод лучше всего для вашего сценария, см. в публикации [форм с кодом.](publishing-forms-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="7d6d8-117">For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span> <span data-ttu-id="7d6d8-118">Примеры решений для решений в песочнице см. в [примере "Sandboxed Solutions".](sample-sandboxed-solutions.md)</span><span class="sxs-lookup"><span data-stu-id="7d6d8-118">For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="7d6d8-119">Разработка с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7d6d8-119">Developing with Visual Studio</span></span>

<span data-ttu-id="7d6d8-120">После Visual Studio 2012 и надстройки набор средств Microsoft Visual Studio Tools для работы с приложениями 2012 можно приступить к разработке решений infoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="7d6d8-121">Выбор языка программирования</span><span class="sxs-lookup"><span data-stu-id="7d6d8-121">Choosing a Programming Language</span></span>

<span data-ttu-id="7d6d8-122">InfoPath предоставляет возможности программирования с помощью четырех версий объектной модели InfoPath на двух языках: Visual Basic и C#.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-122">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#.</span></span> <span data-ttu-id="7d6d8-123">Четыре версии объектной модели обеспечивают совместимость с InfoPath 2013, InfoPath, Office InfoPath 2007 и Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-123">The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="7d6d8-124">Указание языка программирования и объектной модели</span><span class="sxs-lookup"><span data-stu-id="7d6d8-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="7d6d8-125">Открыв проект шаблона формы в конструкторе InfoPath, щелкните **"Язык"** на вкладке **"Разработчик".**</span><span class="sxs-lookup"><span data-stu-id="7d6d8-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="7d6d8-126">В категории **Программирование** диалогового окна **Параметры формы** выберите используемый язык из раскрывающегося списка **Язык кода шаблона формы**.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-126">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list.</span></span> <span data-ttu-id="7d6d8-127">Затем выберите версию объектной модели в выпадаемом списке **целевой** версии.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-127">Then, select the version of the object model from the **Target version** drop-down list.</span></span> <span data-ttu-id="7d6d8-128">Параметр **целевой** версии, совместимый только с InfoPath 2013, не имеет года версии, следующего за **именем InfoPath.**</span><span class="sxs-lookup"><span data-stu-id="7d6d8-128">The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="7d6d8-129">Код поддерживается не всеми типами шаблонов форм.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-129">Not all form template types support code.</span></span> <span data-ttu-id="7d6d8-130">Например, типы шаблона формы **Список SharePoint** и **Блоки шаблона** не поддерживают код формы.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-130">For example, the **SharePoint List** form template type and **Template Parts** do not support form code.</span></span> <span data-ttu-id="7d6d8-131">При разработке типа шаблона, не поддерживающего код, вкладка **Разработчик** не будет доступна.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-131">When designing a form template type that does not support code, the **Developer** tab will not be available.</span></span> <span data-ttu-id="7d6d8-132">Кроме того, только некоторые типы шаблонов форм поддерживают все четыре версии объектной модели.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-132">Also, only some form template types support all four versions of the object model.</span></span> <span data-ttu-id="7d6d8-133">Например, тип шаблона "Пустая форма" **(InfoPath Filler)** поддерживает все четыре версии объектной модели (и создает шаблон формы, совместимый только с InfoPath Filler в этих версиях), но шаблон "Пустая форма" поддерживает только InfoPath 2013 и InfoPath (и создает шаблоны форм, совместимые с InfoPath Filler и браузером). </span><span class="sxs-lookup"><span data-stu-id="7d6d8-133">For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="7d6d8-134">Можно настроить язык программирования по умолчанию, чтобы конструктор форм InfoPath всегда начал с любой версии языка и объектной модели.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="7d6d8-135">Настройка языка программирования по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d6d8-135">To set the default programming language</span></span>

1. <span data-ttu-id="7d6d8-136">Щелкните вкладку **Файл**, а затем щелкните элемент **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="7d6d8-137">В разделе **Общие** диалогового окна **Параметры InfoPath** щелкните элемент **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="7d6d8-138">На вкладке **Разработка** диалогового окна **Параметры** выберите язык программирования по умолчанию в разделе **Параметры программирования по умолчанию**. </span><span class="sxs-lookup"><span data-stu-id="7d6d8-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="7d6d8-139">Написание кода</span><span class="sxs-lookup"><span data-stu-id="7d6d8-139">Writing Code</span></span>

<span data-ttu-id="7d6d8-140">Теперь вы можете начать разработку с infoPath 2013 и Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="7d6d8-141">Запуск редактора Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="7d6d8-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="7d6d8-142">Откройте шаблон формы в конструкторе InfoPath.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="7d6d8-143">Щелкните элемент **Редактор кода** на вкладке **Разработчик**.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="7d6d8-144">Вы также можете запустить редактор кода и автоматически добавить обработчики событий  для событий форм и управления с помощью команд на вкладке "Разработчик", контекстных меню и других методов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7d6d8-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="7d6d8-145">Дополнительные сведения см. в [подстройки "Добавление обработки событий"](how-to-add-an-event-handler.md)</span><span class="sxs-lookup"><span data-stu-id="7d6d8-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

