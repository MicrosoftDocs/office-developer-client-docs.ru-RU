---
title: 'Пошаговое руководство: Создание шаблона базовой формы с помощью кода'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], creating managed code,managed code form templates [InfoPath 2007], creating,form templates [InfoPath 2007], walkthroughs,InfoPath 2007, walkthroughs
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: Бизнес-логику для приложения Microsoft InfoPath можно написать на языке Visual Basic или C#, открыв шаблон формы в конструкторе InfoPath и воспользовавшись одной из команд интерфейса пользователя для добавления обработчика событий, который откроет набор Visual Studio 2012 для написания необходимого кода.
ms.openlocfilehash: 8c98d71c26f8e56c532b2a4467218c366072b2ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807614"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a><span data-ttu-id="0623d-104">Пошаговое руководство: Создание шаблона базовой формы с помощью кода</span><span class="sxs-lookup"><span data-stu-id="0623d-104">Walkthrough: Create a basic form template with code</span></span>

<span data-ttu-id="0623d-p101">Бизнес-логику для приложения Microsoft InfoPath можно написать на языке Visual Basic или C#, открыв шаблон формы в конструкторе InfoPath и воспользовавшись одной из команд интерфейса пользователя для добавления обработчика событий, который откроет набор Visual Studio 2012 для написания необходимого кода. По умолчанию проекты шаблонов форм создаются с помощью набора средств Visual Studio 2012, использующего новую объектную модель управляемого кода, которая предоставляется пространством имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)</span><span class="sxs-lookup"><span data-stu-id="0623d-p101">In Microsoft InfoPath, you can write business logic in Visual Basic or C# by opening a form template in the InfoPath designer, and then using one of the user interface commands to add an event handler, which will open the Visual Studio 2012 development environment for writing your code. By default, form template projects created using Visual Studio 2012 work against the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
<span data-ttu-id="0623d-p102">В первом пошаговом руководстве демонстрируются методы создания простого приложения "Hello World" с помощью языка C# или Visual Basic в наборе Visual Studio 2012. В заключении руководства приведен пример кода, демонстрирующий принципы использования свойства [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) класса [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) для получения имени текущего пользователя и заполнения элемента управления **Текстовое поле** полученным значением.</span><span class="sxs-lookup"><span data-stu-id="0623d-p102">This walkthrough first shows you how to create a simple Hello World application using C# or Visual Basic in the Visual Studio 2012 development environment. The walkthrough concludes with a code sample that shows you how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the current user's name and populate a **Text Box** control with that value.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="0623d-109">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="0623d-109">Prerequisites</span></span>

<span data-ttu-id="0623d-110">Для выполнения инструкций этого пошагового руководства в наборе Visual Studio 2012 необходимо установить следующее программное обеспечение:</span><span class="sxs-lookup"><span data-stu-id="0623d-110">In order to complete this walkthrough using the Visual Studio 2012 development environment, you will need:</span></span>
  
- <span data-ttu-id="0623d-111">Microsoft InfoPath с набором Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="0623d-111">Microsoft InfoPath with Visual Studio 2012 installed.</span></span>
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a><span data-ttu-id="0623d-112">Создание примера "Hello World" в наборе средств Visual Studio Tools для работы с приложениями</span><span class="sxs-lookup"><span data-stu-id="0623d-112">Hello World in Visual Studio Tools for Applications</span></span>

<span data-ttu-id="0623d-113">В следующем пошаговом руководстве демонстрируется, как написать в наборе Visual Studio 2012 код, отображающий простое диалоговое окно с оповещением путем написания обработчика события [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) класса [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) , связанного с элементом управления **Кнопка**.</span><span class="sxs-lookup"><span data-stu-id="0623d-113">In the following walkthrough, you will learn how to write code in the Visual Studio 2012 development environment to display a simple alert dialog box by writing an event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of the [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) class, which is associated with the **Button** control.</span></span> 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a><span data-ttu-id="0623d-114">Создание нового проекта и выбор языка программирования</span><span class="sxs-lookup"><span data-stu-id="0623d-114">Create a new project and specify the programming language</span></span>

1. <span data-ttu-id="0623d-115">Запустите конструктор InfoPath и дважды щелкните шаблон формы **Пустой (редактор InfoPath)**.</span><span class="sxs-lookup"><span data-stu-id="0623d-115">Start the InfoPath designer, and then double-click the **Blank (InfoPath Editor)** form template.</span></span> 
    
2. <span data-ttu-id="0623d-116">Чтобы выбрать язык программирования, нажмите кнопку **Microsoft Office**, выберите **Параметры форм**, в списке **Категории** выберите **Программирование**, а затем выберите либо **Visual Basic**, либо **C#** в раскрывающемся списке **Язык кода шаблона формы**.</span><span class="sxs-lookup"><span data-stu-id="0623d-116">To specify which programming language to use, click the **Office Button**, click **Form Options**, click **Programming** in the **Category** list, and then select either **Visual Basic** or **C#** from the **Form template code language** drop-down list.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="0623d-p103">[!Примечание] При выборе других вариантов языков программирования в списке **Язык кода шаблона формы** обеспечивается совместимость с более ранними версиями InfoPath. Варианты **C# (совместимый с InfoPath 2007)** и **Visual Basic (совместимый с InfoPath 2007)** работают с соблюдением описанных здесь процедур. Однако дополнительные сведения об использовании **C# (совместимый с InfoPath 2003)** и **Visual Basic (совместимый с InfoPath 2003)** см. в разделе [Пошаговое руководство. Создание и отладка начального шаблона формы с помощью объектной модели InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="0623d-p103">The other programming language options in the **Form template code language** drop-down list provide compatibility with previous versions of InfoPath. The **C# (InfoPath 2007 Compatible)** and **Visual Basic (InfoPath 2007 Compatible)** options will work with the procedures in this topic. However, to use the **C# (InfoPath 2003 Compatible)** and **Visual Basic (InfoPath 2003 Compatible)** options, see [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span></span> 
  
    <span data-ttu-id="0623d-120">Теперь можно добавить элемент управления **Кнопка** и создать для него обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="0623d-120">You are now ready to add a **Button** control and create its event handler.</span></span> 
    
### <a name="add-a-button-control-and-event-handler"></a><span data-ttu-id="0623d-121">Добавление элемента управления "Кнопка" и обработчика событий</span><span class="sxs-lookup"><span data-stu-id="0623d-121">Add a Button control and event handler</span></span>

1. <span data-ttu-id="0623d-122">В группе **Элементы управления** нажмите элемент управления **Кнопка**, чтобы добавить его в форму.</span><span class="sxs-lookup"><span data-stu-id="0623d-122">In the **Controls** group, click the **Button** control to add it the form.</span></span> 
    
2. <span data-ttu-id="0623d-p104">Дважды щелкните элемент управления **Кнопка**, введите значение Hello для свойства **Надпись** на вкладке **Свойства** ленты и щелкните **Пользовательский код**. При получении запроса сохраните форму и назовите ее HelloWorld.</span><span class="sxs-lookup"><span data-stu-id="0623d-p104">Double-click the **Button** control, type Hello for the **Label** property on the **Properties** tab of the ribbon, and then click **Custom Code**. When prompted, save the form and name it HelloWorld.</span></span>
    
   <span data-ttu-id="0623d-125">После этого откроется среда **Набор средств Microsoft Visual Studio для работы с приложениями** с курсором на обработчике событий [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) для элемента управления **Кнопка**.</span><span class="sxs-lookup"><span data-stu-id="0623d-125">This will open the **Visual Studio Tools for Applications** environment with the cursor in the event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of **Button** control.</span></span> 
    
   <span data-ttu-id="0623d-126">Теперь можно добавить код формы для обработчика событий кнопки.</span><span class="sxs-lookup"><span data-stu-id="0623d-126">You are now ready to add form code to the event handler for the button.</span></span> 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a><span data-ttu-id="0623d-127">Добавьте в обработчик событий код "Hello World" и просмотрите форму</span><span class="sxs-lookup"><span data-stu-id="0623d-127">Add "Hello World" code to the event handler and preview the form</span></span>

1. <span data-ttu-id="0623d-128">В структуре обработчика событий введите:</span><span class="sxs-lookup"><span data-stu-id="0623d-128">In the event handler skeleton, type:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="0623d-129">Код в шаблоне формы должен выглядеть примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0623d-129">The code for your form template should look similar to the following:</span></span>
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. <span data-ttu-id="0623d-130">Переключитесь в окно режима конструктора InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0623d-130">Switch to the InfoPath designer window.</span></span>
    
3. <span data-ttu-id="0623d-131">Нажмите кнопку **Просмотр** на панели инструментов **Главная**.</span><span class="sxs-lookup"><span data-stu-id="0623d-131">Click the **Preview** button on the **Home** tab.</span></span> 
    
4. <span data-ttu-id="0623d-132">Нажмите на форме кнопку Hello.</span><span class="sxs-lookup"><span data-stu-id="0623d-132">Click the Hello button on the form.</span></span> 
    
   <span data-ttu-id="0623d-133">Отобразится окно с текстовым сообщением "Hello World!"</span><span class="sxs-lookup"><span data-stu-id="0623d-133">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="0623d-134">В следующей процедуре показано, как добавить отладочные точки останова в код формы.</span><span class="sxs-lookup"><span data-stu-id="0623d-134">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="0623d-135">Отладка кода формы</span><span class="sxs-lookup"><span data-stu-id="0623d-135">Debug form code</span></span>

1. <span data-ttu-id="0623d-136">Переключитесь обратно в окно набора Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="0623d-136">Switch back to the Visual Studio 2012 window.</span></span>
    
2. <span data-ttu-id="0623d-137">Щелкните серую полосу слева от строки:</span><span class="sxs-lookup"><span data-stu-id="0623d-137">Click the grey bar to the left of the line:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="0623d-138">Отобразится красный кружок, а строка кода будет выделена, указывая, что при запуске кода формы возникнет пауза в этой точке останова.</span><span class="sxs-lookup"><span data-stu-id="0623d-138">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="0623d-139">В меню **Отладка** выберите пункт **Начать отладку** (или нажмите клавишу F5).</span><span class="sxs-lookup"><span data-stu-id="0623d-139">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
4. <span data-ttu-id="0623d-140">В окне InfoPath **Просмотр** нажмите кнопку Hello на форме.</span><span class="sxs-lookup"><span data-stu-id="0623d-140">In the InfoPath **Preview** window, click the Hello button on the form.</span></span> 
    
5. <span data-ttu-id="0623d-141">Фокус переместится на редактор кода набора Visual Studio 2012 и выделится строка точки останова.</span><span class="sxs-lookup"><span data-stu-id="0623d-141">The Visual Studio 2012 code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
6. <span data-ttu-id="0623d-142">Чтобы продолжить выполнение кода, в меню **Отладка** выберите пункт **Шаг с обходом** (или нажмите сочетание клавиш SHIFT+F8).</span><span class="sxs-lookup"><span data-stu-id="0623d-142">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
7. <span data-ttu-id="0623d-p105">Выполнится код обработчика событий, и отобразится сообщение "Hello World!".</span><span class="sxs-lookup"><span data-stu-id="0623d-p105">The event handler code is executed, and the "Hello World!" message is displayed.</span></span> 
    
8. <span data-ttu-id="0623d-145">Нажмите кнопку **ОК**, чтобы вернуться в редактор кода набора Visual Studio 2012, а затем щелкните **Остановить отладку** в меню **Отладка** (или нажмите сочетание клавиш CTRL+ALT+BREAK).</span><span class="sxs-lookup"><span data-stu-id="0623d-145">Click **OK** to return to the Visual Studio 2012 code editor, and then click **Stop Debugging** on the **Debug** menu (or press Ctrl+Alt+Break).</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="0623d-146">Получение имени текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="0623d-146">Getting the current user's name</span></span>

<span data-ttu-id="0623d-147">В следующем примере демонстрируется, как использовать свойство [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) класса [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) для получения имени текущего пользователя и заполнения значения элемента управления **Текстовое поле** с помощью обработчика событий [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0623d-147">In the following example, you will learn how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the name of the current user and populate the value of a **Text Box** control by using an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
<span data-ttu-id="0623d-148">Заполнение элемента управления **Текстовое поле** выполняется с помощью экземпляра класса [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) для написания имени текущего пользователя в узле XML, к которому привязан элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0623d-148">Populating the **Text Box** control is accomplished by using an instance of the [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) class to write the current user's name to the XML node that the control is bound to.</span></span> 
  
<span data-ttu-id="0623d-p106">Сначала свойство [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) вызывается для получения экземпляра класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , представляющего базовый XML-документ формы. Затем объект [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) вызывает метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , создающий объект **XPathNavigator** и размещающий его в корневом узле основного источника данных формы.</span><span class="sxs-lookup"><span data-stu-id="0623d-p106">First, the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class is called to retrieve an instance of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class that represents the underlying XML document of the form. The [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) object then calls the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method, which creates the **XPathNavigator** object and positions it at the root node of the form's main data source.</span></span> 
  
<span data-ttu-id="0623d-p107">Метод [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) класса **XPathNavigator** вызывается для выбора поля employee в источнике данных формы. В заключение вызывается метод [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) для установки значения поля с использованием свойства [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0623d-p107">The [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) method of the **XPathNavigator** class is called to select the employee field in the form's data source. Finally, the [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) method is called to set the value of the field with the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property.</span></span> 
  
<span data-ttu-id="0623d-153">Дополнительные сведения о работе с **System.Xml** в шаблонах форм с управляемым кодом [могли работать с классов XPathNavigator и XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)см.</span><span class="sxs-lookup"><span data-stu-id="0623d-153">For more information on working with **System.Xml** in managed code form templates, see [Work with the XPathNavigator and XPathNodeIterator Classes](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span></span>
  
### <a name="add-a-loading-event-handler"></a><span data-ttu-id="0623d-154">Добавление обработчика событий загрузки</span><span class="sxs-lookup"><span data-stu-id="0623d-154">Add a Loading event handler</span></span>

1. <span data-ttu-id="0623d-155">Откройте шаблон формы "HelloWorld", созданный в предыдущем пошаговом руководстве.</span><span class="sxs-lookup"><span data-stu-id="0623d-155">Open the HelloWorld form template that you created in the previous walkthrough in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="0623d-156">На вкладке **Просмотр** выберите **Отобразить поля**.</span><span class="sxs-lookup"><span data-stu-id="0623d-156">On the **View** tab, select **Show Fields**.</span></span>
    
3. <span data-ttu-id="0623d-157">Щелкните правой кнопкой мыши папку **myFields**, а затем выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="0623d-157">Right click the **myFields** folder, and then click **Add**.</span></span>
    
4. <span data-ttu-id="0623d-158">В поле **Имя** введите значение employee и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0623d-158">In **Name**, type employee, and then click **OK**.</span></span>
    
5. <span data-ttu-id="0623d-159">Перетащите поле employee в текущее представление.</span><span class="sxs-lookup"><span data-stu-id="0623d-159">Drag the employee field onto the view.</span></span> 
    
6. <span data-ttu-id="0623d-160">На вкладке **Разработчик** щелкните **Событие "Загрузка"**.</span><span class="sxs-lookup"><span data-stu-id="0623d-160">On the **Developer** tab, click **Loading Event**.</span></span>
    
   <span data-ttu-id="0623d-161">При этом будет создан обработчик событий [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , а фокус переключится на этот обработчик событий в редакторе кода.</span><span class="sxs-lookup"><span data-stu-id="0623d-161">This will create an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, and move the focus to that event handler in the code editor.</span></span> 
    
7. <span data-ttu-id="0623d-162">В редакторе кода введите следующее:</span><span class="sxs-lookup"><span data-stu-id="0623d-162">In the code editor, type the following:</span></span>
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. <span data-ttu-id="0623d-163">Переключитесь в окно конструктора форм InfoPath и нажмите кнопку **Просмотр** на вкладке **Главная**, чтобы просмотреть форму.</span><span class="sxs-lookup"><span data-stu-id="0623d-163">Switch to the InfoPath form design window, and then click the **Preview** button on the **Home** tab to preview the form.</span></span> 
    
   <span data-ttu-id="0623d-164">В поле employee должно быть автоматически введено имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="0623d-164">The employee field should automatically fill in with your user name.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="0623d-165">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="0623d-165">Next steps</span></span>

- <span data-ttu-id="0623d-166">Сведения о работе с обработчики событий для других элементов управления и события можно [Добавить обработчик событий](how-to-add-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="0623d-166">For information about working with event handlers for other controls and events, see [Add an Event Handler](how-to-add-an-event-handler.md).</span></span>
    
- <span data-ttu-id="0623d-167">Дополнительные сведения о просмотре и отладке кода в шаблонах форм можно [Предварительный просмотр и отладка шаблонов форм InfoPath с кодом](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="0623d-167">For more information about previewing and debugging code in form templates, see [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="0623d-168">Сведения о развертывании шаблонов форм с управляемым кодом содержатся в разделе [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="0623d-168">For information about how to deploy a managed-code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="0623d-169">Сведения об объектной модели InfoPath и распространенных задачах программирования для шаблонов форм с управляемым кодом см. в разделе [Ознакомление с объектной моделью InfoPath и распространенными задачами разработчиков](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span><span class="sxs-lookup"><span data-stu-id="0623d-169">For information about the InfoPath object model and common programming tasks in managed-code form templates, see [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0623d-170">См. также</span><span class="sxs-lookup"><span data-stu-id="0623d-170">See also</span></span>

- [<span data-ttu-id="0623d-171">XmlForm</span><span class="sxs-lookup"><span data-stu-id="0623d-171">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

