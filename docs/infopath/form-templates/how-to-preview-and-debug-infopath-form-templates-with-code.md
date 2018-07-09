---
title: Просмотр и отладка шаблонов форм InfoPath с кодом
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- previewing form templates [infopath 2007],debugging form templates [InfoPath 2007],form templates [InfoPath 2007], previewing,debugging [InfoPath 2007], managed-code form templates,form templates [InfoPath 2007], debugging,InfoPath 2007, debugging form templates,InfoPath 2007, previewing form templates
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Приложение Microsoft InfoPath с набором Visual Studio 2012 позволяет выполнять отладку путем запуска кода формы в режиме просмотра. При начале отладки кода формы проект компилируется, и приложение InfoPath отображает форму в окне просмотра InfoPath. Когда встречается строка кода, на которой установлена точка останова, фокус переносится на редактор кода. При продолжении выполнения после точки останова фокус смещается обратно на окно просмотра. При закрытии окна просмотра отладка останавливается.
ms.openlocfilehash: c33a7740d5f5dba1f8443f020007a2942bc0fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807494"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a><span data-ttu-id="d626d-108">Просмотр и отладка шаблонов форм InfoPath с кодом</span><span class="sxs-lookup"><span data-stu-id="d626d-108">Preview and Debug InfoPath Form Templates with Code</span></span>

<span data-ttu-id="d626d-p102">Приложение Microsoft InfoPath с набором Visual Studio 2012 позволяет выполнять отладку путем запуска кода формы в режиме просмотра. При начале отладки кода формы проект компилируется, и приложение InfoPath отображает форму в окне просмотра InfoPath. Когда встречается строка кода, на которой установлена точка останова, фокус переносится на редактор кода. При продолжении выполнения после точки останова фокус смещается обратно на окно просмотра. При закрытии окна просмотра отладка останавливается.</span><span class="sxs-lookup"><span data-stu-id="d626d-p102">Microsoft InfoPath with Visual Studio 2012 enables debugging by running form code in preview mode. When you start debugging form code, your project is compiled and InfoPath displays your form in the InfoPath preview window. When a line of code that has a breakpoint set for it is encountered, the focus moves to the code editor. When you continue past a breakpoint, the focus moves back to the preview window. Debugging stops when you close the preview window.</span></span>
  
<span data-ttu-id="d626d-114">Также можно изменить параметры шаблона формы для просмотра и отладки с помощью указанной роли пользователя, файла образца данных или путем указания домена для публикации формы.</span><span class="sxs-lookup"><span data-stu-id="d626d-114">You can also modify the form options of the form template to preview and debug using a specific user role, a sample data file, or by specifying the domain to which the form will be published.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d626d-115">Отладка шаблонов форм после развертывания во время выполнения из Visual Studio 2012 невозможна.</span><span class="sxs-lookup"><span data-stu-id="d626d-115">It is not possible to debug form templates after they are deployed at run time from Visual Studio 2012.</span></span> <span data-ttu-id="d626d-116">Этот компонент включает шаблонов форм, совместимые только с InfoPath, а также тех, совместимые с InfoPath, так и веб-браузер, с помощью службы InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="d626d-116">This includes form templates that are compatible only with InfoPath, as well as those that are compatible with InfoPath and the Web browser using InfoPath Forms Services.</span></span> <span data-ttu-id="d626d-117">Тем не менее можно запись значений поля из кода во время выполнения при отладке бизнес-логике шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="d626d-117">However, it is possible to log values to a field from code at run time to help with debugging a form template's business logic.</span></span> <span data-ttu-id="d626d-118">Сведения о том, как сделать, просмотра [Журнала значений в поле для отладки](how-to-log-values-to-a-field-for-debugging.md).</span><span class="sxs-lookup"><span data-stu-id="d626d-118">For information about how to do that, see [Log Values to a Field for Debugging](how-to-log-values-to-a-field-for-debugging.md).</span></span> 
  
## <a name="debugging-in-preview-mode"></a><span data-ttu-id="d626d-119">Отладка в режиме просмотра</span><span class="sxs-lookup"><span data-stu-id="d626d-119">Debugging in Preview Mode</span></span>

### <a name="to-debug-an-infopath-project-in-preview-mode"></a><span data-ttu-id="d626d-120">Отладка проекта InfoPath в режиме просмотра</span><span class="sxs-lookup"><span data-stu-id="d626d-120">To debug an InfoPath project in Preview Mode</span></span>

1. <span data-ttu-id="d626d-121">Создайте или откройте шаблон формы InfoPath с управляемым кодом в наборе Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="d626d-121">Create or open an InfoPath managed code form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="d626d-122">Задайте одну или несколько точек останова в коде формы с помощью редактора кода, щелкнув серую полоску слева от строки кода, где требуется вставить точку останова.</span><span class="sxs-lookup"><span data-stu-id="d626d-122">Set one or more breakpoints in your form code in the code editor by clicking the grey bar to the left of the line of code where you want to insert a breakpoint.</span></span>
    
    <span data-ttu-id="d626d-123">Отобразится красный кружок, а строка кода будет выделена, указывая, что при запуске кода формы возникнет пауза в этой точке останова.</span><span class="sxs-lookup"><span data-stu-id="d626d-123">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="d626d-124">В меню **Отладка** выберите пункт **Начать отладку** или нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="d626d-124">On the **Debug** menu, click **Start Debugging**; or press F5.</span></span>
    
    <span data-ttu-id="d626d-125">Проект скомпилируется, и в окне просмотра отобразится форма.</span><span class="sxs-lookup"><span data-stu-id="d626d-125">The project will be compiled and the form is displayed in the preview window.</span></span>
    
4. <span data-ttu-id="d626d-126">Выполняйте форму до тех пор, пока не встретится строка кода, содержащая точку останова.</span><span class="sxs-lookup"><span data-stu-id="d626d-126">Interact with the form until a line of code containing a breakpoint is encountered.</span></span>
    
    <span data-ttu-id="d626d-127">Фокус сместится на редактор кода.</span><span class="sxs-lookup"><span data-stu-id="d626d-127">The focus returns to the code editor.</span></span>
    
5. <span data-ttu-id="d626d-128">В меню **Отладка** выберите пункт **Продолжить** или нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="d626d-128">On the **Debug** menu, click **Continue**; or press F5.</span></span>
    
6. <span data-ttu-id="d626d-129">По завершении отладки закройте окно просмотра или выберите пункт **Остановить отладку** в меню **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="d626d-129">When you are finished debugging, close the preview window; or on the **Debug** menu, click **Stop Debugging**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d626d-130">Чтобы выполнить отладку шаблона формы InfoPath управляемого кода при использовании элемента объектной модели, требующего полного доверия, необходимо настроить шаблон формы, как описано в [Предварительный просмотр и отладка шаблонов форм, требующих полного доверия](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="d626d-130">To debug an InfoPath managed code form template when using an object model member that requires full trust, you must configure your form template as described in [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  
## <a name="using-a-sample-data-file"></a><span data-ttu-id="d626d-131">Использование файла образца данных</span><span class="sxs-lookup"><span data-stu-id="d626d-131">Using a Sample Data File</span></span>

<span data-ttu-id="d626d-p104">По умолчанию при отладке и просмотре используется файл template.xml, который создается при создании шаблона формы. Можно создать собственный файл данных и указать его использование при просмотре и отладке, воспользовавшись одной из следующих процедур.</span><span class="sxs-lookup"><span data-stu-id="d626d-p104">By default, debugging and previewing uses the template.xml file that is created when a form template is created. You can create your own data file and specify to use it when previewing or debugging by using one of the following procedures.</span></span> 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a><span data-ttu-id="d626d-134">Указание файла образца данных для использования при отладке и просмотре в наборе средств Visual Studio Tools для работы с приложениями</span><span class="sxs-lookup"><span data-stu-id="d626d-134">To specify a sample data file to use while debugging or previewing in Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="d626d-135">Чтобы просмотреть файл template.xml, откройте шаблон формы в режиме конструктора InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d626d-135">To view template.xml, open the form template in InfoPath design mode.</span></span>
    
2. <span data-ttu-id="d626d-136">Перейдите на вкладку **Файл**, выберите **Сохранение**, щелкните **Сохранить шаблон формы как**и выберите **Исходные файлы**.</span><span class="sxs-lookup"><span data-stu-id="d626d-136">Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click **Source Files**.</span></span>
    
3. <span data-ttu-id="d626d-137">Сохраните файлы шаблона формы в папку, а затем откройте файл template.xml в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="d626d-137">Save the form template files to a folder, and then open the template.xml file in a text editor.</span></span>
    
4. <span data-ttu-id="d626d-138">Создайте и сохраните файл с той же структурой, что и template.xml, и с образцом данных, который требуется использовать.</span><span class="sxs-lookup"><span data-stu-id="d626d-138">Create and save a file with the same structure as template.xml with the sample data you want to use.</span></span>
    
5. <span data-ttu-id="d626d-139">Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="d626d-139">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
6. <span data-ttu-id="d626d-140">Выберите категорию **Просмотр** в диалоговом окне **Параметры формы**, а затем в разделе **Образец данных** укажите файл образца данных, созданный в поле **Расположение файла**.</span><span class="sxs-lookup"><span data-stu-id="d626d-140">Click the **Preview** category of the **Form Options** dialog box, and then under **Sample data** specify the sample data file you created in the **File location** box.</span></span> 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="d626d-141">Указание роли пользователя для использования при отладке и просмотре</span><span class="sxs-lookup"><span data-stu-id="d626d-141">Specifying a User Role to Use While Debugging or Previewing</span></span>

<span data-ttu-id="d626d-p105">Если для формы, с которой осуществляется работа, определены роли пользователей, то можно указать роль пользователя для использования при отладке и просмотре формы. Сведения об определении ролей пользователей см. в справке InfoPath по строке поиска "роль пользователя".</span><span class="sxs-lookup"><span data-stu-id="d626d-p105">If the form you are working with has user roles defined for it, you can specify a user role to use while debugging or previewing your form. For information on how to define user roles, search InfoPath help for "user role".</span></span>
  
> [!NOTE]
> <span data-ttu-id="d626d-p106">Параметр, указывающий роль пользователя, недоступен, если для шаблона форм задана совместимость **Форма веб-браузера**. Роли пользователей не поддерживаются шаблонами форм, открытыми в браузерах из служб форм InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d626d-p106">The option to specify a user role is not available if the compatibility setting for your form template is set to **Web Browser Form**. User roles are not supported in form templates opened in the browser from InfoPath Forms Services.</span></span> 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="d626d-146">Указание роли, используемой при отладке и просмотре</span><span class="sxs-lookup"><span data-stu-id="d626d-146">To specify a role to use while debugging or previewing</span></span>

1. <span data-ttu-id="d626d-147">Если работа осуществляется в наборе Visual Studio 2012 переключитесь на InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d626d-147">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="d626d-148">Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="d626d-148">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="d626d-149">Выберите категорию **Просмотр** в диалоговом окне **Параметры формы**, а затем укажите роль пользователя для использования в раскрывающемся списке **Роль для предварительного просмотра**.</span><span class="sxs-lookup"><span data-stu-id="d626d-149">Click the **Preview** category of the **Form Options** dialog box, and then specify the user role to use in the **Preview as** drop-down box.</span></span> 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="d626d-150">Указание домена для использования при отладке и просмотре</span><span class="sxs-lookup"><span data-stu-id="d626d-150">Specifying a Domain to Use While Debugging or Previewing</span></span>

<span data-ttu-id="d626d-p107">Существует возможность просмотреть форму, как если бы она была опубликована на конкретном домене. Этот параметр применяется только в том случае, если уровень безопасности для шаблона формы явно установлен на значение **Домен**.</span><span class="sxs-lookup"><span data-stu-id="d626d-p107">You can preview a form as if it was published to a specific domain. This setting will only apply if the security level of the form template is explicitly set to **Domain**.</span></span>
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="d626d-153">Указание домена, используемого при отладке и просмотре</span><span class="sxs-lookup"><span data-stu-id="d626d-153">To specify a domain to use while debugging or previewing</span></span>

1. <span data-ttu-id="d626d-154">Если работа осуществляется в наборе Visual Studio 2012 переключитесь на InfoPath.</span><span class="sxs-lookup"><span data-stu-id="d626d-154">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="d626d-155">Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="d626d-155">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="d626d-156">Выберите категорию **Просмотр** в диалоговом окне **Параметры формы**, а затем в поле **Домен** укажите домен для использования при просмотре и отладке.</span><span class="sxs-lookup"><span data-stu-id="d626d-156">Click the **Preview** category of the **Form Options** dialog box, and then specify the domain to use while previewing and debugging in the **Domain** box.</span></span> 
    
4. <span data-ttu-id="d626d-157">Выберите в диалоговом окне **Параметры формы** категорию **Безопасность и доверие**, снимите флажок **Автоматически определять уровень безопасности**, а затем щелкните **Домен**.</span><span class="sxs-lookup"><span data-stu-id="d626d-157">Click the **Security and Trust** category of the **Forms Options** dialog box, clear the **Automatically determine security level** check box, and then click **Domain**.</span></span>
    

