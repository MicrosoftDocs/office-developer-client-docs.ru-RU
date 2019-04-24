---
title: Работать с классами XPathNavigator и XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- XPathNodeIterator Class [InfoPath 2007], класс XPathNavigator [InfoPath 2007], XML-данные формы [InfoPath 2007], доступ, XML DOM [InfoPath 2007], преобразование сценария MSXML5 [InfoPath 2007], скрипт MSXML5 [InfoPath 2007], преобразование
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Для доступа к данным XML и управления ими в источниках данных шаблона формы многие элементы объектной модели управляемого кода, предоставляемые пространством имен Microsoft. Office. InfoPath, создают или могут передавать экземпляр класса XPathNavigator объекта System. XML. XPath пространство имен. После получения доступа к объекту XPathNavigator, возвращенному элементом объектной модели InfoPath, можно использовать свойства и методы класса XPathNavigator для работы с данными.
ms.openlocfilehash: f34f2e1a1cbdb8d9e389c864a9b979be20726e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303551"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="12427-105">Работать с классами XPathNavigator и XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="12427-105">Work with the XPathNavigator and XPathNodeIterator Classes</span></span>

<span data-ttu-id="12427-106">Для доступа к данным XML и управления ими в источниках данных шаблона формы многие элементы объектной модели управляемого кода, предоставляемые пространством имен [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , создают или могут передавать экземпляр класса **XPathNavigator** объекта Пространство имен **System. XML. XPath** .</span><span class="sxs-lookup"><span data-stu-id="12427-106">To access and manipulate the XML data in form template data sources, many members of the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace either create or can be passed an instance of the **XPathNavigator** class of the **System.Xml.XPath** namespace.</span></span> <span data-ttu-id="12427-107">После получения доступа к объекту **XPathNavigator**, возвращенному элементом объектной модели InfoPath, можно использовать свойства и методы класса **XPathNavigator** для работы с данными.</span><span class="sxs-lookup"><span data-stu-id="12427-107">After you have access to an **XPathNavigator** object returned by an InfoPath object model member, you can use the properties and methods of the **XPathNavigator** class to work with the data.</span></span> 
  
<span data-ttu-id="12427-108">Наиболее часто используемым членом пространства имен **Microsoft. Office. InfoPath** , который использует класс **XPathNavigator** , является метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , который позволяет работать с хранимыми данными. представлено объектом **DataSource** .</span><span class="sxs-lookup"><span data-stu-id="12427-108">The most frequently used member of the **Microsoft.Office.InfoPath** namespace that uses the **XPathNavigator** class is the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class, which enables you to work with the stored data represented by a **DataSource** object.</span></span> <span data-ttu-id="12427-109">Метод **CreateNavigator** создает объект **XPathNavigator**, располагающийся в корне источника данных, представленного объектом **DataSource**.</span><span class="sxs-lookup"><span data-stu-id="12427-109">The **CreateNavigator** method creates an **XPathNavigator** object positioned at the root of the data source represented by the **DataSource** object.</span></span> 
  
> [!TIP]
> <span data-ttu-id="12427-110">При наличии опыта использования MSXML5 из скрипта для работы с данными в Microsoft InfoPath 2003 можно рассмотреть вариант применения метода **CreateNavigator** в качестве замены свойства **DOM** для **DataObject**.</span><span class="sxs-lookup"><span data-stu-id="12427-110">If you are familiar with using MSXML5 from script to work with data in Microsoft InfoPath 2003, you can think of the **CreateNavigator** method as the replacement for the **DOM** property of the **DataObject**.</span></span> 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a><span data-ttu-id="12427-111">Использование класса XPathNavigator для доступа к основному источнику данных формы</span><span class="sxs-lookup"><span data-stu-id="12427-111">Using the XPathNavigator Class to Access the Main Data Source of the Form</span></span>

<span data-ttu-id="12427-112">Чтобы получить доступ к основному источнику данных формы, вызовите метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) непосредственно из ключевого слова **this** (C#) или **Me** (Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="12427-112">To access the main data source of the form, call the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="12427-113">В следующем примере создается объект **XPathNavigator**, расположенный в корне основного источника данных, с помощью метода **CreateNavigator**, после чего используется свойство **OuterXml** класса **XPathNavigator** для отображения XML-данных, возвращаемых в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="12427-113">The following example creates an **XPathNavigator** object positioned at the root of the main data source by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> 
  
```cs
XPathNavigator myNavigator = 
   this.CreateNavigator();
MessageBox.Show("Main data source XML: " +
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.CreateNavigator()
MessageBox.Show("Main data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

> [!NOTE]
> <span data-ttu-id="12427-114">Вызов метода [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) непосредственно из ключевого слова **this** или **Me** эквивалентно вызову метода [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) с помощью свойства [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) ( `this.MainDataSource.CreateNavigator()`) или передаче пустой строки в [ ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)Свойство Sources класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ( `this.DataSources[""].CreateNavigator()`).</span><span class="sxs-lookup"><span data-stu-id="12427-114">Calling the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** or **Me** keyword is equivalent to calling [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method by using the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property (  `this.MainDataSource.CreateNavigator()`) or by passing an empty string to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class (  `this.DataSources[""].CreateNavigator()`).</span></span> 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a><span data-ttu-id="12427-115">Выбор и установка XML-узлов для полей в основном источнике данных</span><span class="sxs-lookup"><span data-stu-id="12427-115">Selecting and Setting the XML Nodes for Fields in the Main Data Source</span></span>
<span data-ttu-id="12427-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="12427-116"></span></span>

<span data-ttu-id="12427-117">Чтобы выбрать один узел XML для поля в источнике данных, используйте метод **SelectSingleNode (String, иксмлнамеспацересолвер)** класса **XPathNavigator** .</span><span class="sxs-lookup"><span data-stu-id="12427-117">To select the single XML node for a field in a data source, use the **SelectSingleNode(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="12427-118">Если вы хотите работать с набором повторяющихся полей или повторяющихся групп, используйте метод **SELECT (String, иксмлнамеспацересолвер)** класса **XPathNavigator** .</span><span class="sxs-lookup"><span data-stu-id="12427-118">If you want to work with a set of repeating fields or repeating groups, use the **Select(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="12427-119">Этот метод возвращает объект **XPathNodeIterator** , представляющий коллекцию узлов.</span><span class="sxs-lookup"><span data-stu-id="12427-119">This method returns an **XPathNodeIterator** object that represents a collection of nodes.</span></span> 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a><span data-ttu-id="12427-120">Выбор и установка значения для отдельного узла</span><span class="sxs-lookup"><span data-stu-id="12427-120">Selecting and Setting the Value of a Single Node</span></span>

<span data-ttu-id="12427-121">Перегруженный метод **SelectSingleNode** , который необходимо использовать, имеет параметр _XPath_ , который принимает выражение XPath в виде строки, и параметр распознавателя __ , который принимает объект **XmlNamespaceManager** для разрешения пространства имен префиксы.</span><span class="sxs-lookup"><span data-stu-id="12427-121">The overloaded **SelectSingleNode** method that you must use has an  _xpath_ parameter that takes an XPath expression as a string, and a  _resolver_ parameter that takes an **XmlNamespaceManager** object for resolving namespace prefixes.</span></span> <span data-ttu-id="12427-122">Чтобы выбрать один узел в основном источнике данных формы, передайте выражение XPath, которое указывает поле или группу, которую необходимо выбрать для параметра _XPath_ , вместе с объектом **XmlNamespaceManager** , возвращенным [ Свойство NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) объекта **XmlForm**</span><span class="sxs-lookup"><span data-stu-id="12427-122">To select a single node in the form's main data source, pass in an XPath expression that specifies the field or group that you want to select for the  _xpath_ parameter, together with the **XmlNamespaceManager** object that is returned by the [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) property of the **XmlForm** object.</span></span> <span data-ttu-id="12427-123">Возвращаемый объект **XmlNamespaceManager** инициализируется во время загрузки с использованием всех пространств имен, определенных в файле определения шаблона формы (XSF).</span><span class="sxs-lookup"><span data-stu-id="12427-123">The returned **XmlNamespaceManager** object is initialized at load time with all the namespaces that are defined by the form template's form definition file (.xsf).</span></span> 
  
> [!TIP]
> <span data-ttu-id="12427-p107">Чтобы наиболее быстро создать выражение XPath для выбора узла в источнике данных формы, щелкните правой кнопкой мыши поле или группу в области задач **Поля** и выберите пункт **Копировать XPath**. Чтобы создать и проверить созданные вручную выражения XPath для доступа к узлам в сложной схеме XML или схеме XML с большим числом уровней вложения, добавьте в форму элемент управления **Поле выражения**, укажите в нем выражение XPath и выполните предварительный просмотр формы для отображения результатов.</span><span class="sxs-lookup"><span data-stu-id="12427-p107">The easiest way to create an XPath expression for selecting a node in the form's data source is to right-click the field or group in the **Fields** task pane, and then click **Copy XPath**. To create and test hand-edited XPath expressions for accessing nodes in a complex or heavily nested XML schema, add an **Expression Box** control to the form, specify the XPath expression for the control, and then preview the form to display the results.</span></span> 
  
<span data-ttu-id="12427-126">В следующем примере используется метод **SelectSingleNode** для выбора одного узла для `EmailAlias` поля.</span><span class="sxs-lookup"><span data-stu-id="12427-126">The following example uses the **SelectSingleNode** method to select the single node for the  `EmailAlias` field.</span></span> <span data-ttu-id="12427-127">Затем он использует метод **SetValue** класса **XPathNavigator** и свойство [username](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) класса [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) , чтобы задать значение поля псевдонимом текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="12427-127">Then it uses the **SetValue** method of the **XPathNavigator** class and the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to set the value of the field to the current user's alias.</span></span> 
  
```cs
XPathNavigator emailAlias = 
   this.CreateNavigator().SelectSingleNode(
      "/my:myFields/my:EmailAlias", NamespaceManager);
emailAlias.SetValue(this.Application.User.UserName.ToString());
```

```vb
Dim emailAlias As XPathNavigator = _
   Me.CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:EmailAlias", NamespaceManager)
emailAlias.SetValue(Me.Application.User.UserName.ToString())
```

<span data-ttu-id="12427-128">Сведения о том, как создавать выражения XPath, приведены в справочнике по XPath в MSDN и [рекомендации консорциума по языку путей XML (XPath) версии 1,0 W3C](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="12427-128">For information about how to create XPath expressions, see the XPath Reference on MSDN, and the [XML Path Language (XPath) Version 1.0 W3C Recommendation](https://www.w3.org/TR/xpath).</span></span>
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a><span data-ttu-id="12427-129">Установка значения для узла с атрибутом xsi:nil</span><span class="sxs-lookup"><span data-stu-id="12427-129">Setting the Value of a Node That Has the xsi:nil Attribute</span></span>

<span data-ttu-id="12427-130">Для определенных типов данных при попытке установить значение пустого поля программным способом возникает ошибка "При проверке схемы обнаружены ошибки, не связанные с типами данных".</span><span class="sxs-lookup"><span data-stu-id="12427-130">For certain data types, trying to set the value of a blank field programmatically raises the error "Schema validation found non-data type errors."</span></span> <span data-ttu-id="12427-131">Как правило, причина этой ошибки состоит в том, что для атрибута [xsi: nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="12427-131">Typically the cause of this error is that the element has the [xsi:nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) attribute set to **true**.</span></span> <span data-ttu-id="12427-132">Этот параметр можно обнаружить при проверке базового XML-элемента для пустого поля формы.</span><span class="sxs-lookup"><span data-stu-id="12427-132">If you examine the underlying XML element for the blank field in the form, you can see this setting.</span></span> <span data-ttu-id="12427-133">Например, атрибуту **xsi:nil** XML-фрагмента для следующего пустого поля даты присвоено значение **true**.</span><span class="sxs-lookup"><span data-stu-id="12427-133">For example, the XML fragment for the following blank Date field has the **xsi:nil** attribute set to **true**.</span></span>
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

<span data-ttu-id="12427-134">Если для атрибута **xsi: nil** задано значение **true**, он указывает, что элемент присутствует, но не имеет значения или, другими словами, имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="12427-134">If the **xsi:nil** attribute is set to **true**, it indicates that the element is present but has no value, or in other words, is null .</span></span> <span data-ttu-id="12427-135">При попытке программно задать значение такого узла InfoPath отображает сообщение "Проверка схемы обнаружила ошибки, не связанные с типами данных", так как элемент в данный момент помечен как null.</span><span class="sxs-lookup"><span data-stu-id="12427-135">If you try to programmatically set the value of such a node, InfoPath displays the "Schema validation found non-data type errors" message because the element is currently flagged as being null .</span></span> <span data-ttu-id="12427-136">В InfoPath атрибуту **xsi:nil** присваивается значение **true** для полей null следующих типов данных:</span><span class="sxs-lookup"><span data-stu-id="12427-136">InfoPath sets the **xsi:nil** attribute to **true** for null fields of the following data types:</span></span> 
  
- <span data-ttu-id="12427-137">**Целое число (целое число)**</span><span class="sxs-lookup"><span data-stu-id="12427-137">**Whole Number (integer)**</span></span>
    
- <span data-ttu-id="12427-138">**Decimal (двойной)**</span><span class="sxs-lookup"><span data-stu-id="12427-138">**Decimal (double)**</span></span>
    
- <span data-ttu-id="12427-139">**Date (дата)**</span><span class="sxs-lookup"><span data-stu-id="12427-139">**Date (date)**</span></span>
    
- <span data-ttu-id="12427-140">**Время (время)**</span><span class="sxs-lookup"><span data-stu-id="12427-140">**Time (time)**</span></span>
    
- <span data-ttu-id="12427-141">**Дата и время (dateTime)**</span><span class="sxs-lookup"><span data-stu-id="12427-141">**Date and Time (dateTime)**</span></span>
    
<span data-ttu-id="12427-142">Чтобы избежать этой ошибки, код должен протестировать атрибут **xsi: nil** и, если он присутствует, удалить его перед установкой значения для узла.</span><span class="sxs-lookup"><span data-stu-id="12427-142">To prevent this error, your code must test for the **xsi:nil** attribute, and if it is present, remove it before setting the value of the node.</span></span> <span data-ttu-id="12427-143">Приведенная ниже Подпрограмма получает объект **XPathNavigator** , размещенный в узле, который необходимо задать, проверяет наличие атрибута **nil** и удаляет его, если он существует.</span><span class="sxs-lookup"><span data-stu-id="12427-143">The following subroutine takes an **XpathNavigator** object positioned on the node that you want to set, checks for the **nil** attribute, and then deletes it, if it exists.</span></span> 
  
```cs
public void DeleteNil(XPathNavigator node)
{
   if (node.MoveToAttribute(
      "nil", "https://www.w3.org/2001/XMLSchema-instance"))
      node.DeleteSelf();
}
```

```vb
Public Sub DeleteNil(ByVal node As XPathNavigator)
   If (node.MoveToAttribute( _
      "nil", "https://www.w3.org/2001/XMLSchema-instance")) Then
      node.DeleteSelf()
   End If
End Sub
```

<span data-ttu-id="12427-144">Эту подпрограмму можно вызвать перед попыткой установить поле типа данных, который может содержать атрибут **xsi:nil**, как показано в следующем примере, в котором устанавливается поле даты.</span><span class="sxs-lookup"><span data-stu-id="12427-144">You can call this subroutine before you try to set a field of a data type that might have the **xsi:nil** attribute, as shown in the following example that sets a Date field.</span></span> 
  
```cs
// Access the main data source.
XPathNavigator myForm = this.CreateNavigator();
// Select the field.
XPathNavigator myDate = myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager);
// Check for and remove the "nil" attribute.
DeleteNil(myDate);
// Build the current date in the proper format. (yyyy-mm-dd)
string curDate = DateTime.Today.Year + "-" + DateTime.Today.Month + 
   "-" + DateTime.Today.Day;
// Set the value of the myDate field.
myDate.SetValue(strCurDate);
```

```vb
' Access the main data source.
Dim myForm As XPathNavigator = Me.CreateNavigator()
' Select the field.
Dim myDate As XPathNavigator = _
   myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager)
' Check for and remove the "nil" attribute.
DeleteNil(myDate)
' Build the current date in the proper format. (yyyy-mm-dd)
Dim curDate As String = DateTime.Today.Year + "-" + _
   DateTime.Today.Month + "-" + DateTime.Today.Day
' Set the value of the myDate field.
myDate.SetValue(strCurDate)
```

> [!NOTE]
> <span data-ttu-id="12427-145">Несмотря на то, что реализация объекта **XPathNavigator** в InfoPath предоставляет метод **сеттипедвалуе** , который используется для задания узла с использованием значения определенного типа, InfoPath не реализует этот метод.</span><span class="sxs-lookup"><span data-stu-id="12427-145">Although the implementation of the **XPathNavigator** object in InfoPath exposes the **SetTypedValue** method—which is used to set a node using a value of a specific type—InfoPath does not implement that method.</span></span> <span data-ttu-id="12427-146">Вместо него необходимо использовать метод **SetValue**, в который передается строковое значение в формате, соответствующем типу данных узла.</span><span class="sxs-lookup"><span data-stu-id="12427-146">You must use the **SetValue** method instead, and pass a string value of the correct format for the data type of the node.</span></span> 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a><span data-ttu-id="12427-147">Выбор и установка набора повторяющихся узлов</span><span class="sxs-lookup"><span data-stu-id="12427-147">Selecting and Setting a Set of Repeating Nodes</span></span>

<span data-ttu-id="12427-148">Чтобы указать набор повторяющихся полей или групп, которые имеют неопределенное число, используйте метод **SELECT** класса **XPathNavigator** .</span><span class="sxs-lookup"><span data-stu-id="12427-148">To specify a set of repeating fields or groups that are of an indeterminate number, use the **Select** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="12427-149">Этот метод возвращает объект XPathNodeIterator, который можно использовать для итерации по заданной коллекции узлов.</span><span class="sxs-lookup"><span data-stu-id="12427-149">This method returns an XPathNodeIterator object that you can use to iterate over the specified collection of nodes.</span></span> 
  
<span data-ttu-id="12427-150">В следующем примере предполагается, что шаблон формы содержит **маркированНый список** или аналогичный повторяющийся элемент управления, привязанный к повторяющемуся `field1`элементу с именем.</span><span class="sxs-lookup"><span data-stu-id="12427-150">The following example assumes that your form template contains a **Bulleted List** or similar repeating control that is bound to a repeating element named  `field1`.</span></span> <span data-ttu-id="12427-151">XPath поля передается в метод **SELECT** , а возвращаемОе значение **XPathNodeIterator** присваивается `nodes` переменной.</span><span class="sxs-lookup"><span data-stu-id="12427-151">The XPath of the field is passed to the **Select** method, and the returned **XPathNodeIterator** is assigned to the  `nodes` variable.</span></span> <span data-ttu-id="12427-152">Метод MoveNext используется для итерации по коллекции узлов, а текущее свойство возвращает объект **XPathNavigator** , размещенный на текущем узле.</span><span class="sxs-lookup"><span data-stu-id="12427-152">You use the MoveNext method to iterate over the collection of nodes, and the Current property to return an **XPathNavigator** object positioned on the current node.</span></span> <span data-ttu-id="12427-153">Наконец, используйте свойство **value** для извлечения и отображения значения каждого повторяющегося поля.</span><span class="sxs-lookup"><span data-stu-id="12427-153">Finally, use the **Value** property to retrieve and display the value of each repeating field.</span></span> 
  
```cs
string message = String.Empty;
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
while (nodes.MoveNext())
{
    message += nodes.Current.Value + System.Environment.NewLine;
}
MessageBox.Show(message);
```

```vb
Dim message As String = String.Empty
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Do While nodes.MoveNext
    message += nodes.Current.Value &amp; System.Environment.NewLine
Loop
MessageBox.Show(message)
```

<span data-ttu-id="12427-p115">В предыдущем примере обрабатываются строковые значения в заданном повторяющемся поле. Однако если поле содержит числовые значения, можно использовать аналогичный код для итерации по значениям поля и выполнения арифметических операций, таких как вычисление суммы или средней величины всех значений.</span><span class="sxs-lookup"><span data-stu-id="12427-p115">The previous example works with string values in the specified repeating field. However, if the field contains numeric values, you can use similar code to iterate over the values in the field to perform arithmetic, such as calculating the total or average of the values.</span></span>
  
<span data-ttu-id="12427-156">Также вместо использования свойства **Value** для извлечения значения каждого экземпляра повторяющегося поля можно использовать метод **SetValue** для итерации по полям и установки их значений, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="12427-156">Similarly, instead of using the **Value** property to retrieve the value of each instance of the repeating field, you can use the **SetValue** method to iterate over the fields and set their values, as shown in the following example.</span></span> 
  
```cs
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
int myInt = 1;
while (nodes.MoveNext())
{
   nodes.Current.SetValue(myInt.ToString());
   myInt = myInt + 1;
}
```

```vb
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Dim myInt As Integer = 1
Do While nodes.MoveNext
   nodes.Current.SetValue(myInt.ToString())
   myInt = myInt + 1
Loop
```

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a><span data-ttu-id="12427-157">Использование класса XPathNavigator для доступа к внешнему источнику данных</span><span class="sxs-lookup"><span data-stu-id="12427-157">Using the XPathNavigator Class to Access an External Data Source</span></span>
<span data-ttu-id="12427-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="12427-158"></span></span>

<span data-ttu-id="12427-159">Чтобы получить доступ к внешнему источнику данных, связанному с формой, передайте имя источника данных [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) в свойство Sources класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .</span><span class="sxs-lookup"><span data-stu-id="12427-159">To access an external data source associated with the form, pass the name of the data source to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="12427-160">Чтобы создать подключение к новому внешнему источнику данных или просмотреть имена существующих подключений к внешнему источнику данных, выберите элемент **Подключения к данным** на вкладке **Данные** ленты.</span><span class="sxs-lookup"><span data-stu-id="12427-160">To create a connection to a new external data source, or to view a list of the names of existing external data source connections, click **Data Connections** on the **Data** tab of the ribbon.</span></span> 
  
<span data-ttu-id="12427-161">В следующем примере кода описывается создание объекта **XPathNavigator**, расположенного в корне внешнего источника данных "CityList", с помощью метода **CreateNavigator** с последующим использованием свойства **OuterXml** класса **XPathNavigator** для отображения XML-данных, возвращаемых в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="12427-161">The following code sample shows how to create an **XPathNavigator** object positioned at the root of an external data source named "CityList" by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> <span data-ttu-id="12427-162">В этом примере кода предполагается, что создано подключение к данным списка городов, который хранится во внешнем источнике данных, например, в XML-документе или списке SharePoint, и этому подключению присвоено имя "CityList".</span><span class="sxs-lookup"><span data-stu-id="12427-162">This code sample assumes that you created a data connection to a list of city names that are stored in an external data source, such as an XML document or a SharePoint list, and named that data connection "CityList."</span></span> 
  
```cs
XPathNavigator myNavigator = 
   this.DataSources["CityList"].CreateNavigator();
MessageBox.Show("External data source XML: " + 
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.DataSources("CityList").CreateNavigator()
MessageBox.Show("External data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

<span data-ttu-id="12427-163">После получения доступа к объекту **XPathNavigator**, расположенному в корне внешнего источника данных, можно использовать члены класса **XPathNavigator**, такие как методы **SelectSingleNode** и **SetValue**, для работы с содержащимися в нем данными.</span><span class="sxs-lookup"><span data-stu-id="12427-163">After you have access to an **XPathNavigator** object positioned at the root of an external data source, you can use members of the **XPathNavigator** class such as the **SelectSingleNode** and **SetValue** methods to work with the data it contains.</span></span> 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="12427-164">Элементы объектной модели InfoPath, использующие классы XPathNavigator и XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="12427-164">InfoPath Object Model Members That Use the XPathNavigator and XPathNodeIterator Classes</span></span>
<span data-ttu-id="12427-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="12427-165"></span></span>

<span data-ttu-id="12427-166">В следующей таблице приведены обобщенные сведения обо всех элементах пространства имен **Microsoft.Office.InfoPath**, использующих класс **XPathNavigator** для доступа к XML-данным, управления ими и их отправки.</span><span class="sxs-lookup"><span data-stu-id="12427-166">The following table provides a summary of all of the members of the **Microsoft.Office.InfoPath** namespace that use the **XPathNavigator** class to access, manipulate, or submit XML data.</span></span> 
  
|<span data-ttu-id="12427-167">**Родительский класс**</span><span class="sxs-lookup"><span data-stu-id="12427-167">**Parent Class**</span></span>|<span data-ttu-id="12427-168">**Member**</span><span class="sxs-lookup"><span data-stu-id="12427-168">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12427-169">AdoQueryConnection</span><span class="sxs-lookup"><span data-stu-id="12427-169">AdoQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |<span data-ttu-id="12427-170">Метод [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-171">AdoSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="12427-171">AdoSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |<span data-ttu-id="12427-172">Метод [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-173">Кликкедевентаргс</span><span class="sxs-lookup"><span data-stu-id="12427-173">ClickedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |<span data-ttu-id="12427-174">Свойство [Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12427-175">Контекстчанжедевентаргс</span><span class="sxs-lookup"><span data-stu-id="12427-175">ContextChangedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |<span data-ttu-id="12427-176">Свойство [context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12427-177">DataSource</span><span class="sxs-lookup"><span data-stu-id="12427-177">DataSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |<span data-ttu-id="12427-178">Метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method</span></span>  <br/> |
||<span data-ttu-id="12427-179">Метод [жетнамеднодепроперти](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) method</span></span>  <br/> |
||<span data-ttu-id="12427-180">Метод [сетнамеднодепроперти](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-181">EmailSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="12427-181">EmailSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |<span data-ttu-id="12427-182">Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-183">FileQueryConnection</span><span class="sxs-lookup"><span data-stu-id="12427-183">FileQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |<span data-ttu-id="12427-184">Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-185">FileSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="12427-185">FileSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |<span data-ttu-id="12427-186">Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-187">FormError</span><span class="sxs-lookup"><span data-stu-id="12427-187">FormError</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |<span data-ttu-id="12427-188">Свойство [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12427-189">FormErrorCollection</span><span class="sxs-lookup"><span data-stu-id="12427-189">FormErrorCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |<span data-ttu-id="12427-190">Методы [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="12427-191">FormTemplate</span><span class="sxs-lookup"><span data-stu-id="12427-191">FormTemplate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |<span data-ttu-id="12427-192">Свойство [manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12427-193">Мержеевентаргс</span><span class="sxs-lookup"><span data-stu-id="12427-193">MergeEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |<span data-ttu-id="12427-194">Свойство [XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12427-195">SharepointListQueryConnection</span><span class="sxs-lookup"><span data-stu-id="12427-195">SharepointListQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |<span data-ttu-id="12427-196">Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-197">Подпись</span><span class="sxs-lookup"><span data-stu-id="12427-197">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="12427-198">Свойство [сигнатуреблоккксмлноде](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12427-199">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="12427-199">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="12427-200">Свойство [сигнатуреконтаинер](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12427-201">View</span><span class="sxs-lookup"><span data-stu-id="12427-201">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="12427-202">Методы [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="12427-203">Методы [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="12427-204">Методы [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="12427-205">WebServiceConnection</span><span class="sxs-lookup"><span data-stu-id="12427-205">WebServiceConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |<span data-ttu-id="12427-206">Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) method</span></span>  <br/> |
||<span data-ttu-id="12427-207">Метод [GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-208">XmlEventArgs</span><span class="sxs-lookup"><span data-stu-id="12427-208">XmlEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |<span data-ttu-id="12427-209">Свойство [олдпарент](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) property</span></span>  <br/> |
||<span data-ttu-id="12427-210">Свойство [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12427-211">XmlForm</span><span class="sxs-lookup"><span data-stu-id="12427-211">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |<span data-ttu-id="12427-212">Свойство [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) , которое возвращает объект **DataSource** , который, в свою очередь, предоставляет метод **CreateNavigator** для создания объекта **XPathNavigator** , расположенного в корне базового XML-документа формы (основные данные Источник).</span><span class="sxs-lookup"><span data-stu-id="12427-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property, which returns a **DataSource** object that in turn provides the **CreateNavigator** method for creating an **XPathNavigator** object positioned at the root of the form's underlying XML document (main data source).</span></span>  <br/> |
||<span data-ttu-id="12427-213">Метод [MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-214">XmlFormCollection</span><span class="sxs-lookup"><span data-stu-id="12427-214">XmlFormCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |<span data-ttu-id="12427-215">Метод [Метод NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12427-216">XmlValidatingEventArgs</span><span class="sxs-lookup"><span data-stu-id="12427-216">XmlValidatingEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |<span data-ttu-id="12427-217">Методы [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) methods</span></span>  <br/> |
   
<span data-ttu-id="12427-218">В дополнение к элементам объектной модели InfoPath, возвращающим или принимающим объект **XPathNavigator**, следующие методы возвращают экземпляр класса **XPathNodeIterator** пространства имен **System.Xml.XPath** для прохода по XML-узлам элементов, указанных или выбранных в представлении.</span><span class="sxs-lookup"><span data-stu-id="12427-218">In addition to the InfoPath object model members that return or accept an **XPathNavigator** object, the following methods return an instance of the **XPathNodeIterator** class of the **System.Xml.XPath** namespace for iterating over the XML nodes of items that are specified or selected in a view.</span></span> 
  
|<span data-ttu-id="12427-219">**Родительский класс**</span><span class="sxs-lookup"><span data-stu-id="12427-219">**Parent Class**</span></span>|<span data-ttu-id="12427-220">**Member**</span><span class="sxs-lookup"><span data-stu-id="12427-220">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12427-221">View</span><span class="sxs-lookup"><span data-stu-id="12427-221">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="12427-222">Методы [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="12427-223">Метод [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="12427-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a><span data-ttu-id="12427-224">Использование классов XPathNavigator и XPathNodeIterator для работы с данными, выбранными в представлении</span><span class="sxs-lookup"><span data-stu-id="12427-224">Using the XPathNavigator and XPathNodeIterator Classes to Work with Data Selected in a View</span></span>
<span data-ttu-id="12427-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="12427-225"></span></span>

<span data-ttu-id="12427-226">В следующем примере используются элементы обоих классов **XPathNavigator** и **XPathNodeIterator** для работы с данными форм в следующей последовательности:</span><span class="sxs-lookup"><span data-stu-id="12427-226">The following example uses members of both the **XPathNavigator** and **XPathNodeIterator** classes to work with form data in the following sequence:</span></span> 
  
1. <span data-ttu-id="12427-227">Метод **CreateNavigator** класса **DataSource** используется для создания объектной переменной **XPathNavigator** с именем repeatingTableRow1, которая по умолчанию размещается в корне базового XML-документа формы (основные данные Источник).</span><span class="sxs-lookup"><span data-stu-id="12427-227">The **CreateNavigator** method of the **DataSource** class is used to create an **XPathNavigator** object variable named repeatingTableRow1, which by default is positioned at the root of the underlying XML document of the form (the main data source).</span></span>
    
2. <span data-ttu-id="12427-228">Метод **SelectSingleNode** класса **XPathNavigator** используется для перемещения позиции объекта **XPathNavigator** в первую строку элемента управления **Повторяющаяся таблица** , привязанного к group2 в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="12427-228">The **SelectSingleNode** method of the **XPathNavigator** class is used to move the position of the **XPathNavigator** object to the first row of a **Repeating Table** control bound to group2 in the data source.</span></span> 
    
3. <span data-ttu-id="12427-229">Объектная переменная repeatingTableRow1 передается методу **SelectNodes** класса **View** для выбора узлов в этой строке.</span><span class="sxs-lookup"><span data-stu-id="12427-229">The repeatingTableRow1 object variable is passed to the **SelectNodes** method of the **View** class to select the nodes in that row.</span></span> 
    
4. <span data-ttu-id="12427-230">Переменная объекта **XPathNodeIterator** с именем объектной selectednodes объявляется, а метод **GetSelectedNodes** класса **View** используется для заполнения объекта **XPathNodeIterator** выбранными узлами.</span><span class="sxs-lookup"><span data-stu-id="12427-230">An **XPathNodeIterator** object variable named selectedNodes is declared and the **GetSelectedNodes** method of the **View** class is used populate the **XPathNodeIterator** object with the selected nodes.</span></span> 
    
5. <span data-ttu-id="12427-231">Свойство **Count** класса **XPathNodeIterator** используется для отображения числа узлов, которые хранятся в переменной объекта объектной selectednodes.</span><span class="sxs-lookup"><span data-stu-id="12427-231">The **Count** property of the **XPathNodeIterator** class is used to display the number of nodes contained in the selectedNodes object variable.</span></span> 
    
6. <span data-ttu-id="12427-232">Цикл For/Each используется для прохода по узлам объектной переменной selectedNodes и отображения сведений о каждом узле с помощью свойств **Name**, **InnerXml** и **Value** класса **XPathNavigator**.</span><span class="sxs-lookup"><span data-stu-id="12427-232">A For/Each loop is used to iterate over the nodes in the selectedNodes object variable and display information about each node using the **Name**, **InnerXml**, and **Value** properties of the **XPathNavigator** class.</span></span> 
    
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   this.CreateNavigator().SelectSingleNode(
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
// Get selected nodes.
XPathNodeIterator selectedNodes = 
   CurrentView.GetSelectedNodes();
// Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString());
// Loop through collection and display information.
foreach (XPathNavigator selectedNode in selectedNodes)
{
   MessageBox.Show(selectedNode.Name);
   MessageBox.Show(selectedNode.InnerXml);
   MessageBox.Show(selectedNode.Value);
}
```

```vb
' Create XPathNavigator and specify XPath for nodes.
Dim repeatingTableRow1 As XPathNavigator  = _
   Me.CreateNavigator().SelectSingleNode( _
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager)
' Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1)
' Get selected nodes.
Dim selectedNodes As XPathNodeIterator = _
   CurrentView.GetSelectedNodes()
' Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString())
' Loop through collection and display information.
Dim selectedNode As XPathNavigator
For Each selectedNode In selectedNodes
   MessageBox.Show(selectedNode.Name)
   MessageBox.Show(selectedNode.InnerXml)
   MessageBox.Show(selectedNode.Value)
Next
```

<span data-ttu-id="12427-233">Дополнительные сведения о том, как работать с данными XML из шаблонов форм InfoPath, приведены в статье работа с XML-данными с помощью класса XPathNavigator в шаблонах форм InfoPath 2007.</span><span class="sxs-lookup"><span data-stu-id="12427-233">For more information about how to work with XML data from InfoPath form templates, see Working with XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.</span></span>
  

