---
title: Работа с классами XPathNavigator и XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- класс xpathnodeiterator [infopath 2007], класс XPathNavigator [InfoPath 2007], форма XML-данных [InfoPath 2007], доступ, XML DOM [InfoPath 2007], преобразование скрипта MSXML5 [InfoPath 2007],MSXML5 скрипт [InfoPath 2007], преобразование
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Чтобы получить доступ к XML-данным в источниках данных шаблона форм, многие члены объектной модели управляемого кода, предоставляемой Корпорацией Майкрософт. Office. Пространство имен InfoPath создается или может быть передано экземпляру класса XPathNavigator System.Xml. Пространство имен XPath. После получения доступа к объекту XPathNavigator, возвращенному элементом объектной модели InfoPath, можно использовать свойства и методы класса XPathNavigator для работы с данными.
ms.openlocfilehash: f34f2e1a1cbdb8d9e389c864a9b979be20726e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303551"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Работа с классами XPathNavigator и XPathNodeIterator

Для доступа и управления данными XML в источниках данных шаблона форм многие члены объектной модели управляемого кода, [предоставляемой Корпорацией Майкрософт.Office. Пространство](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) имен InfoPath создается или может быть передано экземпляру **класса XPathNavigator** **System.Xml. Пространство имен XPath.** После получения доступа к объекту **XPathNavigator**, возвращенному элементом объектной модели InfoPath, можно использовать свойства и методы класса **XPathNavigator** для работы с данными. 
  
Наиболее часто используемый член **Microsoft.Office. Пространство имен InfoPath,** использующее **класс XPathNavigator,** — это метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) класса [DataSource,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) который позволяет работать с сохраненными данными, представленными объектом **DataSource.** Метод **CreateNavigator** создает объект **XPathNavigator**, располагающийся в корне источника данных, представленного объектом **DataSource**. 
  
> [!TIP]
> При наличии опыта использования MSXML5 из скрипта для работы с данными в Microsoft InfoPath 2003 можно рассмотреть вариант применения метода **CreateNavigator** в качестве замены свойства **DOM** для **DataObject**. 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>Использование класса XPathNavigator для доступа к основному источнику данных формы

Чтобы получить доступ к основному источнику данных формы, позвоните  по методу [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) непосредственно из этого (C#) или ключевых слов **Me** (Visual Basic). В следующем примере создается объект **XPathNavigator**, расположенный в корне основного источника данных, с помощью метода **CreateNavigator**, после чего используется свойство **OuterXml** класса **XPathNavigator** для отображения XML-данных, возвращаемых в окне сообщения. 
  
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
> Вызов метода [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) непосредственно  из  этого или ключевого слова Me эквивалентен вызову [метода CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) с помощью свойства [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) () или путем передачи пустой строки свойству `this.MainDataSource.CreateNavigator()` [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ( `this.DataSources[""].CreateNavigator()` ). 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>Выбор и установка XML-узлов для полей в основном источнике данных
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Чтобы выбрать один узел XML для поля в источнике данных, используйте метод **SelectSingleNode (String, IXmlNamespaceResolver)** класса **XPathNavigator.** Если вы хотите работать с набором повторяюющихся полей или повторяюющихся групп, используйте метод **Select(String,IXmlNamespaceResolver)** класса **XPathNavigator.** Этот метод возвращает **объект XPathNodeIterator,** который представляет коллекцию узлов. 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>Выбор и установка значения для отдельного узла

Перегруженный метод **SelectSingleNode,** который необходимо использовать, имеет параметр _xpath,_ который принимает  выражение XPath в качестве строки, и параметр разрешения, который принимает объект **XmlNamespaceManager** для решения префиксов пространства имен. Чтобы выбрать один узел в основном источнике данных формы, передай выражение XPath, которое указывает поле или группу для параметра _xpath,_ вместе с объектом **XmlNamespaceManager,** возвращаемым свойством [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) объекта **XmlForm.** Возвращаемый объект **XmlNamespaceManager** инициализируется во время загрузки с использованием всех пространств имен, определенных в файле определения шаблона формы (XSF). 
  
> [!TIP]
> Чтобы наиболее быстро создать выражение XPath для выбора узла в источнике данных формы, щелкните правой кнопкой мыши поле или группу в области задач **Поля** и выберите пункт **Копировать XPath**. Чтобы создать и проверить созданные вручную выражения XPath для доступа к узлам в сложной схеме XML или схеме XML с большим числом уровней вложения, добавьте в форму элемент управления **Поле выражения**, укажите в нем выражение XPath и выполните предварительный просмотр формы для отображения результатов. 
  
В следующем примере **метод SelectSingleNode** используется для выбора единого узла  `EmailAlias` для поля. Затем он использует метод **SetValue** класса **XPathNavigator** и свойство [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) класса [User,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) чтобы задать значение поля псевдониму текущего пользователя. 
  
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

Сведения о создании выражений XPath см. в справке XPath на MSDN и [xML Path Language (XPath) Версии 1.0 W3C.](https://www.w3.org/TR/xpath)
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>Установка значения для узла с атрибутом xsi:nil

Для определенных типов данных при попытке установить значение пустого поля программным способом возникает ошибка "При проверке схемы обнаружены ошибки, не связанные с типами данных". Как правило, причина этой ошибки в том, что элемент имеет [атрибут xsi:nil,](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) задаваемый **true.** Этот параметр можно обнаружить при проверке базового XML-элемента для пустого поля формы. Например, атрибуту **xsi:nil** XML-фрагмента для следующего пустого поля даты присвоено значение **true**.
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

Если **атрибут xsi:nil** настроен на значение **true,** он указывает на то, что элемент присутствует, но не имеет значения, или, другими словами, является null . Если вы пытаетесь программным образом установить значение такого узла, InfoPath отображает сообщение "Проверка схемы, обнаруженная без ошибок типа данных", так как элемент в настоящее время помечен как null . В InfoPath атрибуту **xsi:nil** присваивается значение **true** для полей null следующих типов данных: 
  
- **Целое число (целое число)**
    
- **Десятичной (двойной)**
    
- **Дата (дата)**
    
- **Время (время)**
    
- **Дата и время (dateTime)**
    
Чтобы предотвратить возникновение этой ошибки, в коде необходимо реализовать проверку наличия атрибута **xsi:nil**. Если этот атрибут присутствует, следует удалить его перед установкой значения узла. В следующей подпрограмме принимается объект **XpathNavigator**, расположенный в узле, который требуется установить, выполняется проверка наличия атрибута **nil**, после чего, в случае обнаружения этого атрибута, он удаляется. 
  
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

Эту подпрограмму можно вызвать перед попыткой установить поле типа данных, который может содержать атрибут **xsi:nil**, как показано в следующем примере, в котором устанавливается поле даты. 
  
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
> Хотя реализация объекта **XPathNavigator** в InfoPath предоставляет метод **SetTypedValue,** который используется для набора узла с использованием значения определенного типа, InfoPath не реализует этот метод. Вместо него необходимо использовать метод **SetValue**, в который передается строковое значение в формате, соответствующем типу данных узла. 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>Выбор и установка набора повторяющихся узлов

Чтобы указать набор повторяюющихся полей или групп с неопределяемым числом, используйте метод **Select** класса **XPathNavigator.** Этот метод возвращает объект XPathNodeIterator, который можно использовать для итерации над указанной коллекцией узлов. 
  
В следующем примере предполагается, что шаблон формы содержит список **с** пулями или аналогичный элемент управления повтором, который привязан к элементу с именем повторяемой  `field1` формы. XPath поля передается методу **Select,** а возвращенный **XPathNodeIterator** назначен  `nodes` переменной. Метод MoveNext используется для итерации коллекции узлов и свойства Current для возврата объекта **XPathNavigator,** расположенного на текущем узле. Наконец, используйте свойство **Value** для получения и отображения значения каждого повторяют поле. 
  
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

В предыдущем примере обрабатываются строковые значения в заданном повторяющемся поле. Однако если поле содержит числовые значения, можно использовать аналогичный код для итерации по значениям поля и выполнения арифметических операций, таких как вычисление суммы или средней величины всех значений.
  
Также вместо использования свойства **Value** для извлечения значения каждого экземпляра повторяющегося поля можно использовать метод **SetValue** для итерации по полям и установки их значений, как показано в следующем примере. 
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a>Использование класса XPathNavigator для доступа к внешнему источнику данных
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Чтобы получить доступ к внешнему источнику данных, связанному с формой, передайте имя источника данных свойству [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Чтобы создать подключение к новому внешнему источнику данных или просмотреть имена существующих подключений к внешнему источнику данных, выберите элемент **Подключения к данным** на вкладке **Данные** ленты. 
  
В следующем примере кода описывается создание объекта **XPathNavigator**, расположенного в корне внешнего источника данных "CityList", с помощью метода **CreateNavigator** с последующим использованием свойства **OuterXml** класса **XPathNavigator** для отображения XML-данных, возвращаемых в окне сообщения. В этом примере кода предполагается, что создано подключение к данным списка городов, который хранится во внешнем источнике данных, например, в XML-документе или списке SharePoint, и этому подключению присвоено имя "CityList". 
  
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

После получения доступа к объекту **XPathNavigator**, расположенному в корне внешнего источника данных, можно использовать члены класса **XPathNavigator**, такие как методы **SelectSingleNode** и **SetValue**, для работы с содержащимися в нем данными. 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Элементы объектной модели InfoPath, использующие классы XPathNavigator и XPathNodeIterator
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

В следующей таблице приведены обобщенные сведения обо всех элементах пространства имен **Microsoft.Office.InfoPath**, использующих класс **XPathNavigator** для доступа к XML-данным, управления ими и их отправки. 
  
|**Родительский класс**|**Элемент**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[Метод BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |[Метод BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[Свойство Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[Свойство Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)  <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[Метод CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |
||[Метод GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |
||[Метод SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[Метод выполнения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Метод выполнения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Метод выполнения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)  <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[Свойство site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Добавление](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) методов  <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Свойство Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[Свойство Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Метод выполнения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)  <br/> |
|[Подпись](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[Свойство SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[Свойство SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[Методы GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||[Методы SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |
||[Методы SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Метод выполнения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)  <br/> |
||[Метод GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[Свойство OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)  <br/> |
||[Свойство site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[Свойство MainDataSource,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) которое возвращает объект **DataSource,** который, в свою очередь, предоставляет метод **CreateNavigator** для создания объекта **XPathNavigator,** расположенного в корне основного XML-документа формы (основного источника данных).  <br/> |
||[Метод MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[Метод NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[Методы ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)  <br/> |
   
В дополнение к элементам объектной модели InfoPath, возвращающим или принимающим объект **XPathNavigator**, следующие методы возвращают экземпляр класса **XPathNodeIterator** пространства имен **System.Xml.XPath** для прохода по XML-узлам элементов, указанных или выбранных в представлении. 
  
|**Родительский класс**|**Элемент**|
|:-----|:-----|
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[Методы GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||[Метод GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>Использование классов XPathNavigator и XPathNodeIterator для работы с данными, выбранными в представлении
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

В следующем примере используются элементы обоих классов **XPathNavigator** и **XPathNodeIterator** для работы с данными форм в следующей последовательности: 
  
1. Метод **CreateNavigator** класса **DataSource** используется для создания переменной объекта **XPathNavigator** с именем repeatingTableRow1, которая по умолчанию находится в корне основного XML-документа формы (основного источника данных).
    
2. Метод **SelectSingleNode** класса **XPathNavigator** используется для перемещения положения объекта **XPathNavigator** в первую строку управления повторяемой таблицой, связанной с group2 в источнике данных.  
    
3. Объектная переменная repeatingTableRow1 передается методу **SelectNodes** класса **View** для выбора узлов в этой строке. 
    
4. Объявлена переменная объекта **XPathNodeIterator** с именем **selectedNodes, а метод GetSelectedNodes** класса **View** используется для заполнения объекта **XPathNodeIterator** выбранными узлами. 
    
5. Свойство **Count** класса **XPathNodeIterator** используется для отображения количества узлов, содержащихся в переменной объекта selectedNodes. 
    
6. Цикл For/Each используется для прохода по узлам объектной переменной selectedNodes и отображения сведений о каждом узле с помощью свойств **Name**, **InnerXml** и **Value** класса **XPathNavigator**. 
    
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

Дополнительные сведения о работе с XML-данными из шаблонов форм InfoPath см. в рублях Работа с XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.
  

