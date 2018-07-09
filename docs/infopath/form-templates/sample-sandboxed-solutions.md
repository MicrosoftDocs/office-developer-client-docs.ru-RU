---
title: Примеры изолированных решений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: В этом разделе представлено два примера кода, который можно написать в решении InfoPath изолированные решения, и описан способ публикации шаблона форм.
ms.openlocfilehash: b0874e34d843850df55eee87d689ce0d01112635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807591"
---
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="2bace-103">Примеры изолированных решений</span><span class="sxs-lookup"><span data-stu-id="2bace-103">Sample sandboxed solutions</span></span>

<span data-ttu-id="2bace-p101">Формы InfoPath с управляемым кодом можно публиковать в инфраструктуре решения SharePoint изолированные решения из конструктора InfoPath. В этом разделе представлено два примера кода, который можно написать в решении InfoPath изолированные решения, и описан способ публикации шаблона форм.</span><span class="sxs-lookup"><span data-stu-id="2bace-p101">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer. This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="2bace-106">В примере 1: Сортировка данных в форму заказа</span><span class="sxs-lookup"><span data-stu-id="2bace-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="2bace-p102">Полезная задача, которую можно выполнить с помощью кода в шаблоне форм InfoPath, заключается в сортировке данных в повторяющейся таблице. При этом код изменяет порядок узлов в основном документе XML, отображаемом в форме InfoPath. Хотя сценарий, описанный в этом разделе, предполагает публикацию непосредственно из InfoPath как решение изолированные решения, он также может быть развернут и как утвержденный администратором шаблон форм.</span><span class="sxs-lookup"><span data-stu-id="2bace-p102">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table. To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form. Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="2bace-110">Прежде чем начать, убедитесь в том, что выполняются следующие требования:</span><span class="sxs-lookup"><span data-stu-id="2bace-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="2bace-111">Вы являетесь администратором семейства сайтов на сайте SharePoint Server 2010 или SharePoint Foundation 2010, где планируется опубликовать форму.</span><span class="sxs-lookup"><span data-stu-id="2bace-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="2bace-112">Обратитесь к администратору фермы, убедитесь в том, что запущен на сервере Microsoft SharePoint Foundation службы изолированного кода.</span><span class="sxs-lookup"><span data-stu-id="2bace-112">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server.</span></span> <span data-ttu-id="2bace-113">Для получения дополнительных сведений см [Публикация форм с кодом](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="2bace-113">For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="2bace-114">Язык программирования, выбранного для шаблона формы — **C#** или **Visual Basic** без имени более ранних версий после него.</span><span class="sxs-lookup"><span data-stu-id="2bace-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="2bace-115">Версии языки программирования и объектной модели InfoPath 2003 совместимых и InfoPath 2007 не поддерживается для изолированных решений.</span><span class="sxs-lookup"><span data-stu-id="2bace-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="2bace-116">Дополнительные сведения о том, как выбор языка программирования можно [разработки с использованием Visual Studio](how-to-develop-with-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="2bace-116">For more information about how to specify the programming language, see [Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="2bace-117">Выполните следующие действия, чтобы создать шаблон форм, сортирующий данные в элементе управления **Повторяющаяся таблица** в форме.</span><span class="sxs-lookup"><span data-stu-id="2bace-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="2bace-118">Создание шаблона формы, сортирующего данные a форме программными средствами</span><span class="sxs-lookup"><span data-stu-id="2bace-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="2bace-p105">Создайте новый шаблон форм в конструкторе InfoPath и добавьте в него элемент управления **Повторяющаяся таблица**. Код в этом примере выполняет сортировку строк по первому столбцу, однако его можно изменить, чтобы сортировка выполнялась по любому необходимому столбцу.</span><span class="sxs-lookup"><span data-stu-id="2bace-p105">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form. The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="2bace-p106">Добавьте в форму элемент управления **Кнопка**. В обработчик событий для события **Clicked** кнопки будет добавлен код сортировки таблицы; для этих целей также можно использовать любое другое событие.</span><span class="sxs-lookup"><span data-stu-id="2bace-p106">Add a **Button** control to the form. The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="2bace-p107">Выберите кнопку, перейдите на вкладку **Свойства** и выберите **Пользовательский код**. Если форма еще не была сохранена, система предложит сохранить ее, а затем откроется окно редактора кода с курсором, установленным в обработчике событий кнопки.</span><span class="sxs-lookup"><span data-stu-id="2bace-p107">Select the button, click the **Properties** tab, and then click **Custom Code**. If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="2bace-p108">Вставьте следующий код в обработчик событий кнопки. Код помещает элементы первого столбца в массив, выполняет сортировку массива и изменяет порядок строк в таблице в соответствии с порядком массива. Код рассматривает сортируемые данные в таблице как строковые.</span><span class="sxs-lookup"><span data-stu-id="2bace-p108">Paste the following code into the button's event handler. The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array. This code assumes that the data being sorted is string data.</span></span>
    
   ```cs
    // Put the elements from the first column into an array.
    XPathNavigator root = this.CreateNavigator();
        
    // Create a node iterator which contains only the values that you want to sort.
    // For this form, the entire table is in "group1", each row is a "group2"
    // and the rows are "field1", "field2" and "field3" respectively.
    XPathNodeIterator nodeIterator = root.Select(
        "/my:myFields/my:group1/my:group2/my:field1", this.NamespaceManager);
        
    // Create arrays to use for sorting.
    string[] sortArrayWords = new string[nodeIterator.Count + 1];
    int[] sortArrayKeys = new int[nodeIterator.Count + 1];
    int arrayPosition = 1;
        
    // Populate the arrays for sorting.
    while (nodeIterator.MoveNext()) 
    {
        // Loop until there are no more elements
        sortArrayWords[arrayPosition] = nodeIterator.Current.Value;
        sortArrayKeys[arrayPosition] = arrayPosition;
        arrayPosition += 1;
    }
        
    // Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys);
    arrayPosition = 0;
        
    // Create new XML to update the table.
    string newTableXML = "";
    // Iterate through the sorted array of keys.
    for (int i = 1; i <= sortArrayWords.Length - 1; i++) 
    {
        nodeIterator = root.Select(
            "/my:myFields/my:group1/my:group2", this.NamespaceManager);
            
        // Go to the right position in the table.
        for (int j = 1; j <= sortArrayKeys[i]; j++) 
        {
            nodeIterator.MoveNext();
        }
            
        // Add the row to the XML.
        newTableXML += nodeIterator.Current.OuterXml;
    }
        
    // Set the table to use the new XML.
    root.SelectSingleNode(
        "/my:myFields/my:group1", this.NamespaceManager).InnerXml = newTableXML;
    
   ```

   ```vb
    ' Put the elements from the first column into an array.
    Dim root As XPathNavigator = Me.CreateNavigator
    ' Create a node iterator which contains only the values that you want to sort
    ' For this form, the entire table is in "group1",
    ' each row is a "group2"
    ' and the rows are "field1", "field2" and "field3" respectively.
    Dim nodeIterator As XPathNodeIterator = root.Select( _
        "/my:myFields/my:group1/my:group2/my:field1", Me.NamespaceManager)
    ' Create arrays to use for sorting.
    Dim sortArrayWords(nodeIterator.Count) As String
    Dim sortArrayKeys(nodeIterator.Count) As Integer
    Dim arrayPosition As Integer = 1
    ' Populate the arrays for sorting.
    While nodeIterator.MoveNext() ' Loop until there are no more elements
        sortArrayWords(arrayPosition) = nodeIterator.Current.Value
        sortArrayKeys(arrayPosition) = arrayPosition
        arrayPosition += 1
    End While
    ' Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys)
    arrayPosition = 0
    ' Create new XML to update the table.
    Dim newTableXML As String = ""
    ' Iterate through the sorted array of keys.
    For i As Integer = 1 To sortArrayWords.Length - 1
        nodeIterator = root.Select( _
            "/my:myFields/my:group1/my:group2", Me.NamespaceManager)
        ' Go to the right position in the table.
        For j As Integer = 1 To sortArrayKeys(i)
        nodeIterator.MoveNext()
        Next
    ' Add the row to the XML.
    newTableXML &amp;= nodeIterator.Current.OuterXml
    Next
    ' Set the table to use the new XML.
    root.SelectSingleNode("/my:myFields/my:group1", _
        Me.NamespaceManager).InnerXml = newTableXML
   ```

5. <span data-ttu-id="2bace-128">Опубликуйте форму, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2bace-128">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="2bace-129">Выберите **SharePoint Server** на вкладке **Публикация** в Backstage.</span><span class="sxs-lookup"><span data-stu-id="2bace-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="2bace-130">Введите URL-адрес сайта SharePoint для публикации и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="2bace-131">Для публикации формы на сайте в качестве решения изолированные решения необходимо иметь привилегии администратора семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="2bace-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="2bace-132">Выберите элемент **Библиотека форм**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="2bace-133">Выберите команду **Создать библиотеку форм**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="2bace-134">Введите имя и описание для библиотеки форм, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="2bace-135">Нажмите кнопку **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="2bace-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="2bace-136">Пример 2: Управление поставщиков в список SharePoint</span><span class="sxs-lookup"><span data-stu-id="2bace-136">Example 2: Managing vendors in a SharePoint list</span></span>

<span data-ttu-id="2bace-p109">Этот пример предполагает программирование в соответствии с объектной моделью Microsoft SharePoint Foundation 2010. Для этого необходимо создать ссылку на сборку Microsoft.SharePoint.dll, установленную с лицензионной копией SharePoint Server 2010.</span><span class="sxs-lookup"><span data-stu-id="2bace-p109">This example involves programming against the Microsoft SharePoint Foundation 2010 object model. To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="2bace-p110">Сборка Microsoft.SharePoint.Server.dll по умолчанию установлена в папке C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI. Этот DLL-файл следует включить в проект, программируемый с использованием объектной модели SharePoint. Чтобы создать ссылку на файл Microsoft.SharePoint.dll в проекте набора Visual Studio 2012, откройте **Редактор кода** и выберите команду **Добавить ссылку** в меню **Сервис**. В диалоговом окне **Добавление ссылки** перейдите на вкладку **Обзор**, укажите местоположение файла Microsoft.SharePoint.dll и нажмите кнопку **ОК**. Файл Microsoft.SharePoint.dll будет скопирован в папку проекта, что позволит использовать члены объектной модели SharePoint Foundation 2010 в решении InfoPath.</span><span class="sxs-lookup"><span data-stu-id="2bace-p110">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default. This DLL must be included in projects where you program against the SharePoint object model. To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu. In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**. This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="2bace-144">Проектирование формы и разработка кода</span><span class="sxs-lookup"><span data-stu-id="2bace-144">Designing the form and developing the code</span></span>

<span data-ttu-id="2bace-p111">Объектную модель SharePoint из кода формы InfoPath можно использовать для создания элементов списков поиска. Это удобно при необходимости заполнения раскрывающихся списков из списков SharePoint, когда необходимо добавлять новые значения, не создавая отдельные формы. В этом примере используется раскрывающийся список, в котором отображаются все присутствующие в данный момент в списке значения, а также создается программная логика для добавления значения в список, если его в нем еще нет.</span><span class="sxs-lookup"><span data-stu-id="2bace-p111">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists. This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form. This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="2bace-148">Создание шаблона форм, способного добавлять новые элементы в раскрывающийся список на основе списка SharePoint</span><span class="sxs-lookup"><span data-stu-id="2bace-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="2bace-149">Создание простого настраиваемого списка на сервере SharePoint Server 2010 и присвойте ему имя MyList.</span><span class="sxs-lookup"><span data-stu-id="2bace-149">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList.</span></span> <span data-ttu-id="2bace-150">В следующем примере используется **Поле со списком** , привязанных к поля **заголовка** этого списка.</span><span class="sxs-lookup"><span data-stu-id="2bace-150">The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="2bace-151">Создание новой **Пустой формы** в InfoPath Designer, вставьте **элемент управления в форме** и измените в поле со списком на Мой_список.</span><span class="sxs-lookup"><span data-stu-id="2bace-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="2bace-152">Создание подключения к данным в список, который будет использоваться для заполнения раскрывающего списка, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2bace-152">Create the data connection to the list that will be used to populate the combo box by using the following steps:</span></span>
    
    1. <span data-ttu-id="2bace-153">На вкладке **Данные** в группе **Получить внешние данные** нажмите кнопку **Из списка SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="2bace-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="2bace-154">Введите URL-адрес сайта, содержащего список, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="2bace-155">Выделите список и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="2bace-p113">Выберите поля, которые необходимо включить, например, выделите поля Заголовок и ID. Поле Заголовок содержит значения для поиска. Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-p113">Select the fields that you want to include, for this example, select Title and ID. Title contains the values for lookup. Click **Next**.</span></span>
        
    5. <span data-ttu-id="2bace-159">Нажмите кнопку **Далее** на следующем экране.</span><span class="sxs-lookup"><span data-stu-id="2bace-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="2bace-160">Задайте подключению к данным имя Список_поиска и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="2bace-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="2bace-161">Укажите значения в поле со списком в списке, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2bace-161">Populate the values in the combo box from the list by using the following steps:</span></span>
    
    1. <span data-ttu-id="2bace-162">Выберите раскрывающийся список, созданный в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="2bace-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="2bace-163">Щелкните **Изменить варианты** на вкладке **Свойства средств управления** ленты.</span><span class="sxs-lookup"><span data-stu-id="2bace-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="2bace-164">Выберите **Получить варианты из внешнего источника данных**.</span><span class="sxs-lookup"><span data-stu-id="2bace-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="2bace-165">Убедитесь, что в поле **Источник данных** задано подключение, созданное в шаге 2.</span><span class="sxs-lookup"><span data-stu-id="2bace-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="2bace-166">Задайте значение и измените отображаемое имя на Заголовок.</span><span class="sxs-lookup"><span data-stu-id="2bace-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="2bace-167">На вкладке **браузерных форм** выберите **всегда** в разделе **Параметры обратной передачи**и нажмите кнопку **ОК** , чтобы закрыть диалоговое окно "Свойства".</span><span class="sxs-lookup"><span data-stu-id="2bace-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="2bace-168">Убедитесь, что поле со списком по-прежнему выбрана и нажмите кнопку **Событие изменения** на вкладке " **Разработчик** " на ленте.</span><span class="sxs-lookup"><span data-stu-id="2bace-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="2bace-169">Если форма еще не была сохранена, система предложит сохранить ее.</span><span class="sxs-lookup"><span data-stu-id="2bace-169">If your form is not saved yet, you are prompted to save it.</span></span> <span data-ttu-id="2bace-170">И затем, открывается окно Редактор кода с текущей позиции в `myCombo_Changed` обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="2bace-170">And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="2bace-171">Добавьте ссылку на сборку Microsoft.SharePoint.dll, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="2bace-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="2bace-172">Дополнительные сведения о ссылки на сборку Microsoft.SharePoint увидеть [Элементы объектной модели использования SharePoint](how-to-use-sharepoint-object-model-members.md).</span><span class="sxs-lookup"><span data-stu-id="2bace-172">For more information about referencing the Microsoft.SharePoint assembly, see [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="2bace-173">Вставьте следующий код в `myCombo_Changed` обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="2bace-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
   ```cs
    // Use InfoPath OM's ServerInfo.SharePointSiteUrl property to programmatically
    // specify the site where the form is published.
    using (SPSite FormSite = new SPSite(ServerInfo.SharePointSiteUrl.ToString()))
    {
        using (SPWeb FormWeb = FormSite.OpenWeb())
        {
            // Get the SharePoint list.
            SPList LookupList = FormWeb.Lists["MyList"];
            // Query for the item.
            SPQuery MyQuery = new SPQuery();
            // "Title" is the field (column) to search in the SharePoint list.
            // /my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" + 
                GetDomValue("/my:myFields/my:myCombo") + "</Value></Eq></Where>";
            SPListItemCollection ReturnedItems = LookupList.GetItems(MyQuery);
            // Add the item to the SharePoint list if no items were returned in the query.
            if (ReturnedItems.Count == 0)
            {
                SPListItem NewItem = LookupList.Items.Add();
                // Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem["Title"] = GetDomValue("/my:myFields/my:myCombo");
                // Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = true;
                NewItem.Update();
                // Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = false;
            }
        }
    }
   ```

   ```vb
    ' Use InfoPath OM's ServerInfo.SharePointSiteUrl property to specify the site where the form is published.
    Using FormSite As New SPSite(ServerInfo.SharePointSiteUrl.ToString())
        Using FormWeb As SPWeb = FormSite.OpenWeb()
            ' Get the SharePoint list.
            Dim LookupList As SPList = FormWeb.Lists("MyList")
            ' Query for the item.
            Dim MyQuery As New SPQuery()
            ' "Title" is the field (column) to search in the SharePoint list.
            ' my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" &amp; _
                GetDomValue("/my:myFields/my:myCombo") &amp; "</Value></Eq></Where>"
            Dim ReturnedItems As SPListItemCollection = LookupList.GetItems(MyQuery)
            ' Add the item to the lookup list if no items were returned in the query.
            If ReturnedItems.Count = 0 Then
                Dim NewItem As SPListItem = LookupList.Items.Add()
                ' Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem("Title") = GetDomValue("/my:myFields/my:myCombo")
                ' Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = True
                NewItem.Update()
                ' Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = False
            End If
        End Using
    End Using
   ```

8. <span data-ttu-id="2bace-174">В предыдущем примере кода зависит от `GetDomValue` вспомогательной функции.</span><span class="sxs-lookup"><span data-stu-id="2bace-174">The preceding code example depends on the  `GetDomValue` helper function.</span></span> <span data-ttu-id="2bace-175">Вставьте следующий код для `GetDomValue` вспомогательная функция ниже `myCombo_Changed` функции обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="2bace-175">Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
   ```cs
    private string GetDomValue(string XpathToGet)
    {
        return this.CreateNavigator().SelectSingleNode(XpathToGet, this.NamespaceManager).Value;
    }
   ```

   ```vb
    Private Function GetDomValue(XpathToGet As String) As String
        Return Me.CreateNavigator().SelectSingleNode(XpathToGet, Me.NamespaceManager).Value
    End Function
   ```

9. <span data-ttu-id="2bace-176">Опубликуйте форму, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2bace-176">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="2bace-177">Выберите **SharePoint Server** на вкладке **Публикация** в Backstage.</span><span class="sxs-lookup"><span data-stu-id="2bace-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="2bace-178">Введите URL-адрес сайта SharePoint для публикации и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="2bace-179">Для публикации формы на сайте в качестве решения изолированные решения необходимо иметь привилегии администратора семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="2bace-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="2bace-180">Выберите элемент **Библиотека форм**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="2bace-181">Выберите команду **Создать библиотеку форм**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="2bace-182">Введите имя и описание для библиотеки форм и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="2bace-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="2bace-183">Нажмите кнопку **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="2bace-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="2bace-184">После успешной публикации формы открытия формы из библиотеки форм и добавить новое значение в поле со списком для тестирования кода.</span><span class="sxs-lookup"><span data-stu-id="2bace-184">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code.</span></span> <span data-ttu-id="2bace-185">После выхода из поля Мой_список новое значение будет записан в список SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2bace-185">When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

