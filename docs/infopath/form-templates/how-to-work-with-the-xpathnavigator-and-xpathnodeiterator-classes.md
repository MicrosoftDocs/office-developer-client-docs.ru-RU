---
title: Работа с классами XPathNavigator и XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- класс XPathNodeIterator [infopath 2007], класс XPathNavigator [InfoPath 2007], данные XML формы [InfoPath 2007], доступ к XML DOM [InfoPath 2007], преобразование скрипта MSXML5 [InfoPath 2007], преобразование скрипта MSXML5 [InfoPath 2007]
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Для доступа и работы с данными XML в источники данных шаблона формы, многие члены объектной модели управляемого кода, представленные в пространстве имен Microsoft.Office.InfoPath создать или может быть передан экземпляр класса XPathNavigator System.Xml.XPath пространство имен. После получения доступа к объекту XPathNavigator, возвращенный участником объектной модели InfoPath, можно использовать свойства и методы класса XPathNavigator для работы с данными.
ms.openlocfilehash: f34f2e1a1cbdb8d9e389c864a9b979be20726e6b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393042"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Работа с классами XPathNavigator и XPathNodeIterator

Для доступа и работы с данными XML в источники данных шаблона формы, многие члены объектной модели управляемого кода, представленные в пространстве имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) создать или может быть передан экземпляр класса **XPathNavigator** Пространство имен **System.Xml.XPath** . После получения доступа к объекту **XPathNavigator** , возвращенный участником объектной модели InfoPath, можно использовать свойства и методы класса **XPathNavigator** для работы с данными. 
  
Наиболее часто используемых элементов пространства имен **Microsoft.Office.InfoPath** , с помощью класса **XPathNavigator** — это метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) класса [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , которое позволяет работать с помощью сохраненных данных представлены объектом **источника данных** . Метод **CreateNavigator** создает объект **XPathNavigator** , размещенный в корне источника данных, представленного объектом **источника данных** . 
  
> [!TIP]
> При наличии опыта использования MSXML5 из скрипта для работы с данными в Microsoft InfoPath 2003 можно рассмотреть вариант применения метода **CreateNavigator** в качестве замены свойства **DOM** для **DataObject**. 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>Использование класса XPathNavigator для доступа к основному источнику данных формы

Для доступа к основной источник данных формы, вызовите метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) непосредственно из **этой** (C#) или ключевое слово **Me** (Visual Basic). В следующем примере создается объект **XPathNavigator** , размещенный в корне основного источника данных с помощью метода **CreateNavigator** и затем использует свойство **OuterXml** класса **XPathNavigator** для отображения XML-кода возвращаются в окне сообщения. 
  
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
> Вызов метода [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) непосредственно из **этого** или ключевое слово **Me** эквивалентен вызову метода [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) с помощью свойства [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) ( `this.MainDataSource.CreateNavigator()`) или передаче пустой строке [ Источники данных](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) свойства класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ( `this.DataSources[""].CreateNavigator()`). 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>Выбор и установка XML-узлов для полей в основном источнике данных
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Чтобы выбрать отдельного узла XML для поля в источнике данных, используйте метод **SelectSingleNode(String,IXmlNamespaceResolver)** класса **XPathNavigator** . Если вы хотите работать с набором повторяющиеся поля или повторяющейся группы, используйте метод **Select(String,IXmlNamespaceResolver)** класса **XPathNavigator** . Этот метод возвращает объект **XPathNodeIterator** , представляющий коллекцию узлов. 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>Выбор и установка значения для отдельного узла

Имеет перегруженный метод **SelectSingleNode** , который необходимо использовать параметр _xpath_ , который принимает выражение XPath в виде строки, а также параметр _сопоставления имен_ , который принимает объект **XmlNamespaceManager** для разрешения имен префиксы. Чтобы выбрать отдельного узла в виде основного источника данных, передайте выражение XPath, указывающее поля или группы, необходимо выбрать параметр _xpath_ вместе с объект **XmlNamespaceManager** , возвращаемый [ NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) свойства объекта **XmlForm** . Возвращаемый объект **XmlNamespaceManager** инициализируется во время загрузки со всеми пространствами имен, которые определены в шаблоне формы файла определения формы (.xsf). 
  
> [!TIP]
> Чтобы наиболее быстро создать выражение XPath для выбора узла в источнике данных формы, щелкните правой кнопкой мыши поле или группу в области задач **Поля** и выберите пункт **Копировать XPath**. Чтобы создать и проверить созданные вручную выражения XPath для доступа к узлам в сложной схеме XML или схеме XML с большим числом уровней вложения, добавьте в форму элемент управления **Поле выражения**, укажите в нем выражение XPath и выполните предварительный просмотр формы для отображения результатов. 
  
В следующем примере используется метод **SelectSingleNode** для выбора отдельного узла для `EmailAlias` поля. Затем присвоено значение поля текущего пользователя псевдоним использует метод **SetValue** класса **XPathNavigator** и свойство [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) класса [пользователя](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) . 
  
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

Сведения о создании выражения XPath видеть ссылку XPath на MSDN и [рекомендации W3C язык адресации XML (XPath) версии 1.0](https://www.w3.org/TR/xpath).
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>Установка значения для узла с атрибутом xsi:nil

Для определенных типов данных при попытке задать значение пустое поле программными средствами вызывает ошибку «проверку на соответствие схеме обнаружены ошибки не данных типа». Обычно причиной этой ошибки — это, что элемент имеет атрибут [xsi: nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) присвоено **значение true**. Если посмотреть на базовый XML-элемента для пустого поля в форме, можно видеть этот параметр. Например фрагмент XML-кода для следующих пустые поля даты имеет атрибут **xsi: nil** присвоено **значение true**.
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

Если атрибут **xsi: nil** имеет значение **true**, это означает, что элемент присутствует, но не имеет значения или другими словами, имеет значение null. При попытке программно задавать значение такой узел InfoPath отображает сообщение «проверку на соответствие схеме обнаружены ошибки не данных типа» так как в текущий момент элемент помечается как значение null. Приложение InfoPath устанавливает атрибут **xsi: nil** значение **true,** значение null, полей следующие типы данных: 
  
- **Целого числа (integer)**
    
- **Тип decimal (double)**
    
- **Date (дата)**
    
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
> Хотя для реализации объекта **XPathNavigator** в InfoPath предоставляет метод **SetTypedValue** — которая используется для задания узла, используя значение определенного типа — InfoPath не реализует этот метод. Вместо этого используйте метод **SetValue** и передать значение string правильный формат для типа данных узла. 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>Выбор и установка набора повторяющихся узлов

Для определения набора повторяющихся поля или группы, которые могут представлять неопределенное число, используйте метод **Select** класса **XPathNavigator** . Этот метод возвращает объект XPathNodeIterator, которые можно использовать для итерации по указанного семейства узлов. 
  
В следующем примере предполагается, что шаблон формы содержит **Маркированного списка** или аналогичную повторяющегося элемента управления, привязанном к повторяющегося элемента с именем `field1`. Выражение XPath поля передается методу **выберите** и назначается возвращенного **XPathNodeIterator** `nodes` переменной. Используйте метод MoveNext для итерации по коллекции узлов и текущее свойство возвращает объект **XPathNavigator** , размещенный на текущем узле. И, наконец используйте свойство **Value** для извлечения и отображения значения каждого повторяющееся поле. 
  
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

Для доступа к внешнему источнику данных связанного с формой, передайте имя источника данных в свойство [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Для создания подключения к источника внешних данных, или чтобы просмотреть список имен существующих подключений к внешним данным источника щелкните **Подключения к данным** на вкладке **данные** на ленте. 
  
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
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |Метод [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |Метод [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Свойство [Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Свойство [context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)  <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |Метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |
||Метод [GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |
||Метод [SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)  <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |Свойства [сайта](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |Методы [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)  <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |Свойства [манифест](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Свойство [XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)  <br/> |
|[Подпись](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Свойства [SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Свойство [SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)  <br/> |
|[Просмотр](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |Методы [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||Методы [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |
||Методы [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |Метод [EXECUTE](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)  <br/> |
||Метод [GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Свойство [OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)  <br/> |
||Свойства [сайта](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |Свойство [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) , которое возвращает объект **DataSource** , который в свою очередь, предоставляет метод **CreateNavigator** для создания объект **XPathNavigator** , размещенный в корне XML-документом формы (основных данных источник).  <br/> |
||Метод [MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |Метод [NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Методы [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)  <br/> |
   
В дополнение к элементам объектной модели InfoPath, возвращающим или принимающим объект **XPathNavigator**, следующие методы возвращают экземпляр класса **XPathNodeIterator** пространства имен **System.Xml.XPath** для прохода по XML-узлам элементов, указанных или выбранных в представлении. 
  
|**Родительский класс**|**Элемент**|
|:-----|:-----|
|[Просмотр](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |Методы [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||Метод [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>Использование классов XPathNavigator и XPathNodeIterator для работы с данными, выбранными в представлении
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

В следующем примере используются элементы обоих классов **XPathNavigator** и **XPathNodeIterator** для работы с данными форм в следующей последовательности: 
  
1. Метод **CreateNavigator** класса **DataSource** используется для создания переменной объекта **XPathNavigator** с именем repeatingTableRow1, который по умолчанию, размещенный в корне базового документа XML формы (основных данных источник).
    
2. Метод **SelectSingleNode** класса **XPathNavigator** используется для смещения позиции объекта **XPathNavigator** в первую строку элемента управления **Повторяющаяся таблица**, связанного с группой group2 в источнике данных. 
    
3. Объектная переменная repeatingTableRow1 передается методу **SelectNodes** класса **View** для выбора узлов в этой строке. 
    
4. Объявляется объектная переменная **XPathNodeIterator** с именем selectedNodes и используется метод **GetSelectedNodes** класса **View** для заполнения объекта **XPathNodeIterator** выбранными узлами.  
    
5. Свойство **Count** класса **XPathNodeIterator** используется для отображения количества узлов, содержащихся в объектной переменной selectedNodes. 
    
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

Дополнительные сведения о работе с данными XML из шаблонов форм InfoPath в разделе Работа с XML-данных с помощью класса XPathNavigator в шаблонах форм InfoPath 2007.
  

