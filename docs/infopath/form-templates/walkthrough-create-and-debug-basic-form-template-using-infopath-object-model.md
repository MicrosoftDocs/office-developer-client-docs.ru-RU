---
title: 'Погон: создание и отлаживка базового шаблона формы с помощью объектной модели InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- шаблоны форм [infopath 2007], walkthroughs,form templates [InfoPath 2007], создание infoPath 2003-compatible,InfoPath 2003-compatible form templates, walkthroughs
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: В этом разделе содержится руководство по созданию базового шаблона формы управляемых форм кода InfoPath, который работает с объектной моделью, совместимой с InfoPath 2003, предоставляемой Корпорацией Майкрософт. Office.Interop.InfoPath.SemiTrust пространство имен.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414342"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="bf852-104">Погон: создание и отлаживка базового шаблона формы с помощью объектной модели InfoPath</span><span class="sxs-lookup"><span data-stu-id="bf852-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="bf852-105">В этом разделе содержится руководство по созданию базового шаблона формы управляемых форм кода InfoPath, который работает с объектной моделью InfoPath 2003, предоставляемой пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)</span><span class="sxs-lookup"><span data-stu-id="bf852-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="bf852-106">Hello World</span><span class="sxs-lookup"><span data-stu-id="bf852-106">Hello World</span></span>

<span data-ttu-id="bf852-107">В следующем примере вы узнаете, как отобразить [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) простой диалоговое окно оповещения с помощью метода Оповещения объектной модели InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="bf852-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="bf852-108">Создание нового шаблона формы InfoPath, работающего с объектной моделью, совместимой с InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="bf852-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="bf852-109">Создайте новый шаблон формы, который работает с объектной моделью InfoPath 2003, как описано в "Создание шаблона формы с помощью объектной модели [InfoPath 2003".](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)</span><span class="sxs-lookup"><span data-stu-id="bf852-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="bf852-110">Введите имя проекта шаблона формы HelloWorld и сохраните проект.</span><span class="sxs-lookup"><span data-stu-id="bf852-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="bf852-p101">Проектная система создаст файлы кода и проекта, а затем откроет пустой шаблон формы в режиме конструктора InfoPath. Теперь можно добавлять обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="bf852-p101">The project system creates code and project files, and then opens a blank form template in InfoPath design mode. You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="bf852-113">Добавление кнопки с обработчиком событий OnClick</span><span class="sxs-lookup"><span data-stu-id="bf852-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="bf852-114">В разделе **Элементы управления** вкладки **Главная** щелкните элемент управления **Кнопка**, чтобы вставить его в представление.</span><span class="sxs-lookup"><span data-stu-id="bf852-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="bf852-115">Щелкните правой кнопкой мыши элемент управления и выберите **Свойства кнопки**.</span><span class="sxs-lookup"><span data-stu-id="bf852-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="bf852-116">Измените **метку на** Alert.</span><span class="sxs-lookup"><span data-stu-id="bf852-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="bf852-117">Измените **ID на** AlertID.</span><span class="sxs-lookup"><span data-stu-id="bf852-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="bf852-118">Щелкните **Редактировать код формы**.</span><span class="sxs-lookup"><span data-stu-id="bf852-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="bf852-119">Создается скелет обработника событий для события [OnClick,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) и фокус перемещается в редактор кода Visual Studio 2012 г.</span><span class="sxs-lookup"><span data-stu-id="bf852-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="bf852-120">Дополнительные сведения о работе с обработчиками событий см. в добавлении обработчик событий [с помощью объектной модели InfoPath 2003.](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)</span><span class="sxs-lookup"><span data-stu-id="bf852-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="bf852-121">Теперь можно добавить код формы для обработчика событий кнопки.</span><span class="sxs-lookup"><span data-stu-id="bf852-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="bf852-122">Добавление кода формы для обработчика событий</span><span class="sxs-lookup"><span data-stu-id="bf852-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="bf852-123">Введите в обработчике событий **OnClick** следующий код:</span><span class="sxs-lookup"><span data-stu-id="bf852-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="bf852-p103">Обратите внимание, что после ввода каждой точки в строке кода отображается раскрывающийся список Microsoft IntelliSense. Целиком обработчик событий должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bf852-p103">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code. The entire event handler should look like the following:</span></span>
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > <span data-ttu-id="bf852-126">В качестве альтернативы использованию метода **Alert** можно воспользоваться методом **MessageBox.Show** пространства имен **System.Windows.Forms** для отображения окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="bf852-126">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box.</span></span> <span data-ttu-id="bf852-127">Для этого необходимо добавить ссылку на систему. Windows. Формирует сборку, добавляет или добавляет директивы в начале кода, а затем введите строку кода, например `using System.Windows.Forms;` `Imports System.Windows.Forms` следующие:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="bf852-127">To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="bf852-128">Переключитесь в окно режима конструктора InfoPath и нажмите кнопку **Просмотр** на вкладке **Главная**.</span><span class="sxs-lookup"><span data-stu-id="bf852-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="bf852-129">В окне **Просмотр** нажмите кнопку **Оповещение**.</span><span class="sxs-lookup"><span data-stu-id="bf852-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="bf852-130">Отобразится окно с текстовым сообщением "Hello World!"</span><span class="sxs-lookup"><span data-stu-id="bf852-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="bf852-131">В следующей процедуре показано, как добавить отладочные точки останова в код формы.</span><span class="sxs-lookup"><span data-stu-id="bf852-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="bf852-132">Отладка кода формы</span><span class="sxs-lookup"><span data-stu-id="bf852-132">Debug form code</span></span>

1. <span data-ttu-id="bf852-133">В редакторе кода щелкните серую полоску слева от строки:</span><span class="sxs-lookup"><span data-stu-id="bf852-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="bf852-134">Отобразится красный кружок, а строка кода будет выделена, указывая, что при запуске кода формы возникнет пауза в этой точке останова.</span><span class="sxs-lookup"><span data-stu-id="bf852-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="bf852-135">В меню **Отладка** выберите пункт **Начать отладку** (или нажмите клавишу F5).</span><span class="sxs-lookup"><span data-stu-id="bf852-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="bf852-136">В окне InfoPath **Просмотр** нажмите кнопку **Оповещение**.</span><span class="sxs-lookup"><span data-stu-id="bf852-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="bf852-137">Фокус перемещается на редактор кода, и выделяется строка точки останова.</span><span class="sxs-lookup"><span data-stu-id="bf852-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="bf852-138">В меню **Отладка** выберите пункт **Шаг с обходом** (или нажмите сочетание клавиш SHIFT+F8), чтобы продолжить обход кода.</span><span class="sxs-lookup"><span data-stu-id="bf852-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="bf852-p105">Выполнится код метода **Alert** и в окне InfoPath **Просмотр** отобразится оповещение "Hello World!".</span><span class="sxs-lookup"><span data-stu-id="bf852-p105">The **Alert** method code is executed, and the "Hello World!" alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="bf852-141">Получение имени текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="bf852-141">Getting the Current User's Name</span></span>

<span data-ttu-id="bf852-p106">С помощью классов .NET Framework можно получить доступ к возможностям, которые сложно реализовать в скрипте. В этом примере предоставляется обучение использованию классов .NET Framework для получения имени текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf852-p106">By using the .NET Framework classes, you can get access to functionality that was not easily available in script. In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="bf852-144">Добавление обработчика событий OnLoad</span><span class="sxs-lookup"><span data-stu-id="bf852-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="bf852-145">Откройте проект InfoPath "HelloWorld", созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="bf852-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="bf852-146">На вкладке **Вид** выберите пункт **Отобразить поля**.</span><span class="sxs-lookup"><span data-stu-id="bf852-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="bf852-147">Щелкните правой кнопкой мыши узел **myFields**, а затем щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="bf852-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="bf852-148">В поле **Имя** введите **employee** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bf852-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="bf852-149">Перетащите узел **employee** в представление.</span><span class="sxs-lookup"><span data-stu-id="bf852-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="bf852-150">На вкладке **Разработчик** щелкните **Событие OnLoad**.</span><span class="sxs-lookup"><span data-stu-id="bf852-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="bf852-151">Это создаст обработник событий для события [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) и фокус перемещается в редактор кода.</span><span class="sxs-lookup"><span data-stu-id="bf852-151">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor.</span></span> <span data-ttu-id="bf852-152">Код этого обработчика событий будет вызываться при каждой загрузке формы.</span><span class="sxs-lookup"><span data-stu-id="bf852-152">The code in this event handler will be called each time the form is loaded.</span></span> <span data-ttu-id="bf852-153">В следующей процедуре демонстрируется добавление кода формы, получающего имя пользователя для обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="bf852-153">The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="bf852-154">Добавление кода формы </span><span class="sxs-lookup"><span data-stu-id="bf852-154">Add form code</span></span>

1. <span data-ttu-id="bf852-155">Введите в обработчике событий **OnLoad** следующий код:</span><span class="sxs-lookup"><span data-stu-id="bf852-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. <span data-ttu-id="bf852-156">Скомпилируйте и просмотрите форму.</span><span class="sxs-lookup"><span data-stu-id="bf852-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="bf852-157">Теперь в текстовом поле employee должно быть выведено текущее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf852-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="bf852-158">Сведения о развертывании шаблона формы управляемого кода см. в ссылке [Развертывание шаблонов форм InfoPath с кодом.](how-to-deploy-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="bf852-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="bf852-159">Сведения об объектной модели InfoPath и общих задачах программирования в шаблонах управляемых форм кода, которые работают с объектной моделью InfoPath 2003, см. в примере [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="bf852-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf852-160">См. также</span><span class="sxs-lookup"><span data-stu-id="bf852-160">See also</span></span>

- [<span data-ttu-id="bf852-161">Инициализация и очистка кода с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="bf852-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="bf852-162">Объектные модели, совместимые с InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="bf852-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="bf852-163">Добавление обработера событий с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="bf852-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

