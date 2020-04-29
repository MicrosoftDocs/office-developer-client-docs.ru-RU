---
title: Примеры изолированных решений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: В этом разделе представлено два примера кода, который можно написать в решении InfoPath изолированные решения, и описан способ публикации шаблона форм.
ms.openlocfilehash: 56a9a2a765100ef327790265c7cf734903268bed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439340"
---
# <a name="sample-sandboxed-solutions"></a>Примеры изолированных решений

Формы InfoPath с управляемым кодом можно публиковать в инфраструктуре решения SharePoint изолированные решения из конструктора InfoPath. В этом разделе представлено два примера кода, который можно написать в решении InfoPath изолированные решения, и описан способ публикации шаблона форм.
  
## <a name="example-1-sorting-data-in-an-order-form"></a>Пример 1: Сортировка данных в форме заказа

Полезная задача, которую можно выполнить с помощью кода в шаблоне форм InfoPath, заключается в сортировке данных в повторяющейся таблице. При этом код изменяет порядок узлов в основном документе XML, отображаемом в форме InfoPath. Хотя сценарий, описанный в этом разделе, предполагает публикацию непосредственно из InfoPath как решение изолированные решения, он также может быть развернут и как утвержденный администратором шаблон форм.
  
Прежде чем начать, убедитесь в том, что выполняются следующие требования:
  
- Вы являетесь администратором семейства сайтов на сайте SharePoint Server 2010 или SharePoint Foundation 2010, где планируется опубликовать форму.
    
- Обратитесь к администратору фермы и убедитесь, что на сервере запущена служба изолированного кода Microsoft SharePoint Foundation. Более подробную информацию можно узнать [в статье Публикация форм с помощью кода](publishing-forms-with-code.md).
    
- Выбранный для шаблона форм язык программирования — это **C#** или **Visual Basic** без указания какого-либо номера более ранней версии после названия. Совместимые с InfoPath 2007 версии и объектные модели, совместимые с InfoPath 2003, не поддерживаются для изолированных решений. Дополнительные сведения о том, как указать язык программирования, можно найти в разделе [Разработка с помощью Visual Studio](how-to-develop-with-visual-studio.md).
    
Выполните следующие действия, чтобы создать шаблон форм, сортирующий данные в элементе управления **Повторяющаяся таблица** в форме. 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a>Создание шаблона формы, сортирующего данные a форме программными средствами

1. Создайте новый шаблон форм в конструкторе InfoPath и добавьте в него элемент управления **Повторяющаяся таблица**. Код в этом примере выполняет сортировку строк по первому столбцу, однако его можно изменить, чтобы сортировка выполнялась по любому необходимому столбцу. 
    
2. Добавьте в форму элемент управления **Кнопка**. В обработчик событий для события **Clicked** кнопки будет добавлен код сортировки таблицы; для этих целей также можно использовать любое другое событие. 
    
3. Выберите кнопку, перейдите на вкладку **Свойства** и выберите **Пользовательский код**. Если форма еще не была сохранена, система предложит сохранить ее, а затем откроется окно редактора кода с курсором, установленным в обработчике событий кнопки.
    
4. Вставьте следующий код в обработчик событий кнопки. Код помещает элементы первого столбца в массив, выполняет сортировку массива и изменяет порядок строк в таблице в соответствии с порядком массива. Код рассматривает сортируемые данные в таблице как строковые.
    
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

5. Опубликуйте форму, выполнив следующие действия:
    
    1. Выберите **SharePoint Server** на вкладке **Публикация** в Backstage. 
        
    2. Введите URL-адрес сайта SharePoint для публикации и нажмите кнопку **Далее**. 
        
       > [!IMPORTANT]
       > [!Важно!] Для публикации шаблона форм как решение изолированные решения необходимо быть администратором семейства сайтов. 
    
    3. Выберите элемент **Библиотека форм**, а затем нажмите кнопку **Далее**.
        
    4. Выберите команду **Создать библиотеку форм**, а затем нажмите кнопку **Далее**.
        
    5. Введите имя и описание для библиотеки форм, а затем нажмите кнопку **Далее**.
        
    6. Нажмите кнопку **Опубликовать**.
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a>Пример 2: Управление поставщиками в списке SharePoint

Этот пример предполагает программирование в соответствии с объектной моделью Microsoft SharePoint Foundation 2010. Для этого необходимо создать ссылку на сборку Microsoft.SharePoint.dll, установленную с лицензионной копией SharePoint Server 2010.
  
Сборка Microsoft.SharePoint.Server.dll по умолчанию установлена в папке C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI. Этот DLL-файл следует включить в проект, программируемый с использованием объектной модели SharePoint. Чтобы создать ссылку на файл Microsoft.SharePoint.dll в проекте набора Visual Studio 2012, откройте **Редактор кода** и выберите команду **Добавить ссылку** в меню **Сервис**. В диалоговом окне **Добавление ссылки** перейдите на вкладку **Обзор**, укажите местоположение файла Microsoft.SharePoint.dll и нажмите кнопку **ОК**. Файл Microsoft.SharePoint.dll будет скопирован в папку проекта, что позволит использовать члены объектной модели SharePoint Foundation 2010 в решении InfoPath.
  
### <a name="designing-the-form-and-developing-the-code"></a>Разработка формы и разработка кода

Объектную модель SharePoint из кода формы InfoPath можно использовать для создания элементов списков поиска. Это удобно при необходимости заполнения раскрывающихся списков из списков SharePoint, когда необходимо добавлять новые значения, не создавая отдельные формы. В этом примере используется раскрывающийся список, в котором отображаются все присутствующие в данный момент в списке значения, а также создается программная логика для добавления значения в список, если его в нем еще нет.
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a>Создание шаблона форм, способного добавлять новые элементы в раскрывающийся список на основе списка SharePoint

1. Создайте простой настраиваемый список на сервере SharePoint Server 2010 и назовите его Милист. В приведенном ниже примере используется **поле со списком** , связанное с полем **заголовка** этого списка. 
    
2. Создайте новую **пустую форму** в конструкторе InfoPath, вставьте в форму элемент управления **"поле со списком"** и переименуйте поле, привязанное к полю со списком, в микомбо.
    
3. Создайте подключение к списку, который будет использоваться для заполнения поля со списком, выполнив следующие действия:
    
    1. На вкладке **Данные** в группе **Получить внешние данные** нажмите кнопку **Из списка SharePoint**. 
        
    2. Введите URL-адрес сайта, содержащего список, и нажмите кнопку **Далее**.
        
    3. Выделите список и нажмите кнопку **Далее**.
        
    4. Выберите поля, которые необходимо включить, например, выделите поля Заголовок и ID. Поле Заголовок содержит значения для поиска. Нажмите кнопку **Далее**.
        
    5. Нажмите кнопку **Далее** на следующем экране. 
        
    6. Задайте подключению к данным имя Список_поиска и нажмите кнопку **Готово**.
    
4. Заполните поля со списком из списка, выполнив следующие действия:
    
    1. Выберите раскрывающийся список, созданный в шаге 1.
        
    2. Щелкните **Изменить варианты** на вкладке **Свойства средств управления** ленты. 
        
    3. Выберите **Получить варианты из внешнего источника данных**.
        
    4. Убедитесь, что в поле **Источник данных** задано подключение, созданное в шаге 2. 
        
    5. Задайте значение и измените отображаемое имя на Заголовок.
        
    6. На вкладке **формы браузера** выберите **всегда** в разделе **параметры обратной передачи**, а затем нажмите кнопку **ОК** , чтобы закрыть диалоговое окно Свойства. 
    
5. Убедитесь, что поле со списком все еще выбрано, а затем выберите **событие изменено** на вкладке **разработчик** ленты. 
    
    Если форма еще не была сохранена, система предложит сохранить ее. После этого откроется окно Редактор кода с курсором в обработчике `myCombo_Changed` событий. 
    
6. Добавьте ссылку на сборку Microsoft.SharePoint.dll, как описано выше. Дополнительные сведения о ссылках на сборку Microsoft. SharePoint см в разделе [Использование элементов объектной модели SharePoint](how-to-use-sharepoint-object-model-members.md).
    
7. Вставьте следующий код в обработчик `myCombo_Changed` событий. 
    
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

8. Приведенный выше пример кода зависит от `GetDomValue` вспомогательной функции. Вставьте следующий код для `GetDomValue` вспомогательной функции под функцией обработчика `myCombo_Changed` событий. 
    
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

9. Опубликуйте форму, выполнив следующие действия:
    
    1. Выберите **SharePoint Server** на вкладке **Публикация** в Backstage. 
        
    2. Введите URL-адрес сайта SharePoint для публикации и нажмите кнопку **Далее**. 
        
       > [!IMPORTANT]
       > [!Важно!] Для публикации шаблона форм как решение изолированные решения необходимо быть администратором семейства сайтов. 
    
    3. Выберите элемент **Библиотека форм**, а затем нажмите кнопку **Далее**.
        
    4. Выберите команду **Создать библиотеку форм**, а затем нажмите кнопку **Далее**.
        
    5. Введите имя и описание библиотеки форм, а затем нажмите кнопку **Далее**.
        
    6. Нажмите кнопку **Опубликовать**.
        
    7. После успешной публикации формы откройте форму из библиотеки форм и добавьте в поле со списком новое значение, чтобы протестировать код. При выходе из поля Микомбо новое значение будет записано в список SharePoint. 
    

