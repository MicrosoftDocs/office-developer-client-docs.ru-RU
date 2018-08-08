---
title: Разработка с помощью Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Функциональность формы InfoPath можно повысить за счет к ним с управляемым кодом, разработанных в Visual Studio 2012. Затем можно опубликовать форм с кодом в библиотеки форм в SharePoint Server 2013.
ms.openlocfilehash: d6a2cfa1847b4b59b6978b8f4a0775aedf07a72d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807510"
---
# <a name="develop-with-visual-studio"></a><span data-ttu-id="1f2c8-104">Разработка с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1f2c8-104">Develop with Visual Studio</span></span>

<span data-ttu-id="1f2c8-105">Функциональность формы InfoPath можно повысить за счет к ним с управляемым кодом, разработанных в Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-105">You can greatly enhance the functionality of your InfoPath forms by extending them with managed code developed in Visual Studio 2012.</span></span> <span data-ttu-id="1f2c8-106">Затем можно опубликовать форм с кодом в библиотеки форм в SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-106">You can then publish your forms with code to form libraries on SharePoint Server 2013.</span></span>
  
<span data-ttu-id="1f2c8-107">Для начала программирования и развертывания форм InfoPath с управляемым кодом необходимо выполнить три основных действия:</span><span class="sxs-lookup"><span data-stu-id="1f2c8-107">You can start programming and deploying your InfoPath forms with managed code in three high-level steps:</span></span>
  
1. <span data-ttu-id="1f2c8-108">Установка Visual Studio 2012 с использованием надстройки [Набор средств Microsoft Visual Studio 2012 приложений](http://www.microsoft.com/en-us/download/details.aspx?id=38807) .</span><span class="sxs-lookup"><span data-stu-id="1f2c8-108">Install Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on.</span></span> 
    
2. <span data-ttu-id="1f2c8-109">Определить язык программирования и написание и отладка кода в редакторе кода Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-109">Set your programming language, and then write and debug code in the Visual Studio 2012 code editor.</span></span>
    
3. <span data-ttu-id="1f2c8-110">После завершения создания формы и кода шаблон формы можно опубликовать в SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-110">When you have finished designing the form and developing your code, the form template can be published to SharePoint Server 2013.</span></span>
    
<span data-ttu-id="1f2c8-111">Ниже приведены некоторые причины использовать Создание форм, совместимых с SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-111">Here are some reasons to consider creating forms that are compatible with SharePoint Server 2013:</span></span>
  
- <span data-ttu-id="1f2c8-112">В браузере можно заполнение форм, развернуть в SharePoint Server 2013 с помощью службы InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-112">Forms deployed to SharePoint Server 2013 with InfoPath Forms Services can be filled out in a browser.</span></span> <span data-ttu-id="1f2c8-113">Это позволяет пользователям, у которых не установлен InfoPath, открытие и использование форм.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-113">This enables users who do not have InfoPath installed to open and use your forms.</span></span>
    
- <span data-ttu-id="1f2c8-114">Разработка только одной версии формы.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-114">You design only one version of the form.</span></span> <span data-ttu-id="1f2c8-115">Формы, совместимые с Microsoft SharePoint Server совместимы с InfoPath Filler, но формы, совместимые с InfoPath Filler только не открываются в браузере.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-115">Forms that are compatible with Microsoft SharePoint Server are also compatible with the InfoPath Filler, but forms that are compatible only with the InfoPath Filler cannot be opened in the browser.</span></span>
    
<span data-ttu-id="1f2c8-116">Существует два способа для публикации формы в SharePoint: SharePoint изолированных решений и решений, рассматриваемых администратором.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-116">There are two ways to publish your form to SharePoint: SharePoint sandboxed solutions, and administrator-deployed solutions.</span></span> <span data-ttu-id="1f2c8-117">Дополнительные сведения о каждом метод публикации и предложений о том, какие метод лучше всего подходит для вашей ситуации можно [Публикация форм с кодом](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="1f2c8-117">For more information about each publication method and suggestions about which method is best for your scenario, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span> <span data-ttu-id="1f2c8-118">Для примера решения для изолированных решений просмотрите [Примеры изолированных решений](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="1f2c8-118">For example solutions for sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
## <a name="developing-with-visual-studio"></a><span data-ttu-id="1f2c8-119">Разработка с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1f2c8-119">Developing with Visual Studio</span></span>

<span data-ttu-id="1f2c8-120">С помощью Visual Studio 2012 и Microsoft Visual Studio Tools для установки надстройки приложений 2012 г. вы готовы приступить к разработке решений InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-120">With Visual Studio 2012 and the Microsoft Visual Studio Tools for Applications 2012 add-on installed, you are ready to start to develop InfoPath managed code solutions.</span></span>
  
### <a name="choosing-a-programming-language"></a><span data-ttu-id="1f2c8-121">Выбор языка программирования</span><span class="sxs-lookup"><span data-stu-id="1f2c8-121">Choosing a Programming Language</span></span>

<span data-ttu-id="1f2c8-122">InfoPath предоставляет возможности программирования с использованием объектной модели InfoPath четыре версии на двух языках: Visual Basic и C#.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-122">InfoPath provides the options to program by using four versions of the InfoPath object model in two languages: Visual Basic and C#.</span></span> <span data-ttu-id="1f2c8-123">Четыре версии объектной модели обеспечивают совместимость с InfoPath 2013, InfoPath, Office InfoPath 2007 и Microsoft InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-123">The four versions of the object model provide compatibility with InfoPath 2013, InfoPath, Office InfoPath 2007, and Microsoft InfoPath 2003.</span></span>
  
### <a name="to-specify-the-programming-language-and-object-model"></a><span data-ttu-id="1f2c8-124">Указание языка программирования и объектной модели</span><span class="sxs-lookup"><span data-stu-id="1f2c8-124">To specify the programming language and object model</span></span>

1. <span data-ttu-id="1f2c8-125">С помощью откройте проект шаблона формы в InfoPath designer выберите **язык** на вкладке **Разработчик** .</span><span class="sxs-lookup"><span data-stu-id="1f2c8-125">With a form template project open in the InfoPath designer, click **Language** on the **Developer** tab.</span></span> 
    
2. <span data-ttu-id="1f2c8-126">В разделе **программирование** Категория диалогового окна **Параметры формы** выберите язык, для работы с из раскрывающегося списка **язык кода шаблона формы** .</span><span class="sxs-lookup"><span data-stu-id="1f2c8-126">In the **Programming** category of the **Form Options** dialog box, select the language that you want to work with from the **Form template code language** drop-down list.</span></span> <span data-ttu-id="1f2c8-127">Выберите версию объектной модели из раскрывающегося списка **требуемой версии** .</span><span class="sxs-lookup"><span data-stu-id="1f2c8-127">Then, select the version of the object model from the **Target version** drop-down list.</span></span> <span data-ttu-id="1f2c8-128">Параметр **целевую версию** , совместимую с InfoPath 2013 только нет версии года после имени **InfoPath** .</span><span class="sxs-lookup"><span data-stu-id="1f2c8-128">The **Target version** option that is compatible only with InfoPath 2013 does not have a version year following the **InfoPath** name.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="1f2c8-129">Не все типы шаблона формы поддерживают кода.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-129">Not all form template types support code.</span></span> <span data-ttu-id="1f2c8-130">Например тип шаблона формы **Списка SharePoint** и **Блоков шаблона** не поддерживают кода формы.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-130">For example, the **SharePoint List** form template type and **Template Parts** do not support form code.</span></span> <span data-ttu-id="1f2c8-131">При разработке тип шаблона формы, который не поддерживает код, вкладки " **Разработчик** " не будет доступен.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-131">When designing a form template type that does not support code, the **Developer** tab will not be available.</span></span> <span data-ttu-id="1f2c8-132">Кроме того только некоторые типы шаблона формы поддерживает все четыре версии объектной модели.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-132">Also, only some form template types support all four versions of the object model.</span></span> <span data-ttu-id="1f2c8-133">Например тип шаблона **Пустая форма (InfoPath Filler)** поддерживает все четыре версии объектной модели (и создает шаблон формы, совместимые с InfoPath Filler этих версий только), но шаблон **Пустой формы** поддерживает только InfoPath 2013 и InfoPath (и создает шаблонов форм, совместимых с InfoPath Filler и браузера).</span><span class="sxs-lookup"><span data-stu-id="1f2c8-133">For example, the **Blank Form (InfoPath Filler)** template type supports all four versions of the object model (and creates form template that are compatible only with the InfoPath Filler in those versions), but the **Blank Form** template supports only InfoPath 2013 and InfoPath (and creates form templates that are compatible with both the InfoPath Filler and the browser).</span></span> 
  
    <span data-ttu-id="1f2c8-134">Можно задать язык программирования, поэтому конструктор форм InfoPath всегда начинается с версии языка и объектной модели собственное по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-134">You can set a default programming language so that the InfoPath form designer will always start with the language and object model version of your choice.</span></span>
    
### <a name="to-set-the-default-programming-language"></a><span data-ttu-id="1f2c8-135">Настройка языка программирования по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1f2c8-135">To set the default programming language</span></span>

1. <span data-ttu-id="1f2c8-136">Щелкните вкладку **Файл**, а затем щелкните элемент **Параметры**.
</span><span class="sxs-lookup"><span data-stu-id="1f2c8-136">Click the **File** tab, and then click **Options**.</span></span>
    
2. <span data-ttu-id="1f2c8-137">В разделе **Общие** диалогового окна **Параметры InfoPath** щелкните элемент **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-137">In the **General** section of the **InfoPath Options** dialog box, click **More Options**.</span></span>
    
3. <span data-ttu-id="1f2c8-138">На вкладке **Разработка** диалогового окна **Параметры** выберите язык программирования по умолчанию в разделе **Параметры программирования по умолчанию**. </span><span class="sxs-lookup"><span data-stu-id="1f2c8-138">On the **Design** tab of the **Options** dialog box, select the default programming language in the **Programming Defaults** section.</span></span> 
    
### <a name="writing-code"></a><span data-ttu-id="1f2c8-139">Написание кода</span><span class="sxs-lookup"><span data-stu-id="1f2c8-139">Writing Code</span></span>

<span data-ttu-id="1f2c8-140">Теперь можно приступить к разработке с помощью InfoPath 2013 и Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-140">You can now start to develop with InfoPath 2013 and Visual Studio 2012.</span></span> 
  
### <a name="to-start-the-visual-studio-code-editor"></a><span data-ttu-id="1f2c8-141">Чтобы запустить редактор кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1f2c8-141">To start the Visual Studio Code Editor</span></span>

1. <span data-ttu-id="1f2c8-142">Откройте шаблон формы в InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-142">Open a form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="1f2c8-143">Щелкните элемент **Редактор кода** на вкладке **Разработчик**.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-143">Click **Code Editor** on the **Developer** tab.</span></span> 
    
> [!TIP]
> <span data-ttu-id="1f2c8-144">Можно также запустить редактор кода и автоматическое добавление обработчиков событий для события формы и элемента управления с помощью команды на вкладке **Разработчик** , контекстных меню и другие методы интерфейса пользователя.</span><span class="sxs-lookup"><span data-stu-id="1f2c8-144">You can also start the code editor and automatically add event handlers for form and control events using commands on the **Developer** tab, context menus, and other user interface methods.</span></span> <span data-ttu-id="1f2c8-145">Дополнительные сведения можно [Добавить обработчик событий](how-to-add-an-event-handler.md)</span><span class="sxs-lookup"><span data-stu-id="1f2c8-145">For more information, see [Add an Event Handler](how-to-add-an-event-handler.md)</span></span>
  

