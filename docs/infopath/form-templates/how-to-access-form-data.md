---
title: Доступ к данным форм
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- данные формы [infopath 2007] форм [InfoPath 2007], доступ к свойствам, формирующие шаблонов [InfoPath 2007], доступ к свойствам, открытие форм [InfoPath 2007], печать форм [InfoPath 2007] форм [InfoPath 2007], печать, закрытие форм [InfoPath 2007] InfoPath 2007, доступ к данным формы, формы [InfoPath 2007], доступ к источнику данных, форм [InfoPath 2007], закрывающего тега, форм [InfoPath 2007], открывающий, печать [InfoPath 2007], формы, формы [InfoPath 2007], создание
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Флажок расширить функциональность формы InfoPath, часто бывает необходимо программным способом доступа к сведениям о базовом документе XML формы, доступ к данным, который содержит XML-документа или выполнение некоторых действий с документом XML. Объектная модель InfoPath поддерживает доступ к и работа с XML-документом формы посредством использования класса XmlForm в сочетании с классом XmlFormCollection.
ms.openlocfilehash: c39862fd404575fe95bc1986ce7ab7d9689acfb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807526"
---
# <a name="access-form-data"></a>Доступ к данным форм

Флажок расширить функциональность формы InfoPath, часто бывает необходимо программным способом доступа к сведениям о базовом документе XML формы, доступ к данным, который содержит XML-документа или выполнение некоторых действий с документом XML. Объектная модель InfoPath поддерживает доступ к и работа с XML-документом формы посредством использования класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) в сочетании с классом [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) . 
  
Класс [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) — это один из самых полезных типов в объектной модели InfoPath, так как она предоставляет ряд свойств и методов, которые не только взаимодействия с базовым XML формы документов, но также выполнять множество действий, которые доступны в Пользовательский интерфейс приложения InfoPath. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Обзор класса XmlFormCollection

Класс [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) предоставляет следующие методы и свойства, которые можно использовать для управления объектами [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , содержащихся в коллекции. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [New(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx)  <br/> |Создает новую форму на основе указанной формы.  <br/> |
|Метод [New (строка, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (перегрузка 1)  <br/> |Создает новую форму на основе указанной формы с использованием указанного поведения режима открытия.  <br/> |
|Метод [NewFromFormTemplate(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |Создает новую форму на основе указанного шаблона формы.  <br/> |
|Метод [NewFromFormTemplate (строка, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (перегрузка 1)  <br/> |Создает новую форму на основе указанного шаблона формы и XML-данных.  <br/> |
|Метод [NewFromFormTemplate (строка, строка, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (перегрузка 2)  <br/> |Создает новую форму на основе указанного шаблона формы с данными, указанными объектом [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) .  <br/> |
|Метод [NewFromFormTemplate (String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (перегрузка 3)  <br/> |Создает новую форму на основе указанного шаблона формы с данными, указанными объектом **XPathNavigator**, и с использованием указанного поведения режима открытия.  <br/> |
|Метод [Open(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx)  <br/> |Открывает указанную форму.  <br/> |
|Метод [Open (строка, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (перегрузка 1)  <br/> |Открывает указанную форму с использованием указанного поведения режима открытия.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)  <br/> |Возвращает количество объектов **XmlForm**, содержащихся в семействе.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **XmlForm** из семейства по значению индекса.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Обзор интерфейса XmlForm

Класс [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с и выполнения действий над XML-документом формы. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)  <br/> |Закрывает форму.  <br/> |
|Метод [GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx)  <br/> |Возвращает ссылку на семейство **Microsoft.Office.Core.WorkflowTasks** для текущей формы.  <br/> |
|Метод [GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx)  <br/> |Возвращает ссылку на семейство **Microsoft.Office.Core.WorkflowTemplates** для текущей формы.  <br/> |
|Метод [MergeForm(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |Объединяет текущую форму с формой, указанной с помощью пути или URL-адреса.  <br/> |
|Метод [MergeForm(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (перегрузка 1)  <br/> |Объединяет текущую форму с формой, указанной в узле, возвращаемым переданным в метод объектом **XPathNavigator**.  <br/> |
|Метод [NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx)  <br/> |Предоставляет пользовательское значение для внешнего приложения или ASPX-страницы.  <br/> |
|Метод [Print()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx)  <br/> |Распечатывает содержимое формы в соответствии с активным представлением формы.  <br/> |
|Метод [Print(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (перегрузка 1)  <br/> |Распечатывает содержимое формы в соответствии с активным представлением формы путем вывода диалогового окна **Печать**.  <br/> |
|Метод [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)  <br/> |Сохраняет форму по URL-адресу, с которым она в данный момент связана.  <br/> |
|Метод [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)  <br/> |Сохраняет форму по указанному URL-адресу.  <br/> |
|Метод [SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx)  <br/> |Задает имя файла по умолчанию для диалогового окна **Сохранить как**.  <br/> |
|Метод [SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx)  <br/> |Задает путь по умолчанию для сохранения формы с помощью диалогового окна **Сохранить как**.  <br/> |
|Метод [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx)  <br/> |Отправляет форму с помощью операции отправки, указанной в шаблоне формы.  <br/> |
|Свойство [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx)  <br/> |Получает объект [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , представляющий текущее представление формы.  <br/> |
|Свойство [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx)  <br/> |Возвращает объект [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) , связанный с формой.  <br/> |
|Свойство [Источники данных](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)  <br/> |Возвращает объект [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) , связанный с формой.  <br/> |
|Свойство [Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx)  <br/> |Возвращает значение, которое указывает, были ли изменены данные формы с момента ее последнего сохранения.  <br/> |
|Свойство [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx)  <br/> |Возвращает ссылку на [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) , связанного с формой.  <br/> |
|Свойство [Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx)  <br/> |Возвращает [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) для доступа к функциям и глобальным переменным, содержащимся в файле кода формы основной формы, использующего [System.Reflection](https://msdn.microsoft.com/en-us/library/system.reflection(v=vs.110).aspx).  <br/> |
|Свойство [FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Возвращает ссылку на контейнер свойств [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) типа, которые могут использовать формы с поддержкой браузера для обработки сведений о состоянии сеансов на сервере.  <br/> |
|Свойство [узла](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx)  <br/> |Возвращает [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx), который код, запущенный в размещенном экземпляре InfoPath, может использовать для доступа к объектной модели внешнего приложения.  <br/> |
|Свойство [размещенных в узлах](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx)  <br/> |Возвращает факт размещения InfoPath в качестве элемента управления в другом приложении.  <br/> |
|Свойство [HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx)  <br/> |Возвращает имя приложения, размещающего InfoPath в качестве элемента управления.   <br/> |
|Свойство [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx)  <br/> |Получает объект [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , представляющий основной источник данных формы.  <br/> |
|Свойство [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx)  <br/> |Возвращает ссылку на объект [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) , который можно использовать для разрешения, добавления или удаления пространств имен, используемых в форме.  <br/> |
|[Создать](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) свойство  <br/> |Возвращает значение, которое указывает, является ли форма новой.  <br/> |
|Свойство [разрешения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx)  <br/> |Возвращает ссылку на объект [разрешения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) , связанного с формой.  <br/> |
|Свойство [QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx)  <br/> |Возвращает ссылку на объект [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) , который представляет подключение к данным, связанного с формой.  <br/> |
|Свойство [только для чтения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx)  <br/> |Возвращает значение, которое указывает, является ли форма доступной только для чтения или заблокированной.  <br/> |
|Свойство [восстановлен](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx)  <br/> |Возвращает значение, которое указывает, была ли форма сохранена в последний раз с помощью операции сохранения AutoRecover.  <br/> |
|Свойство [выполнен вход](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx)  <br/> |Возвращает значение, которое указывает наличие цифровых подписей для формы.  <br/> |
|Свойство [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx)  <br/> |Возвращает ссылку на коллекцию [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , связанную с формой.  <br/> |
|Свойство [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx)  <br/> |Возвращает ссылку на коллекцию [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) , связанный с шаблоном формы.  <br/> |
|Свойства [шаблона](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx)  <br/> |Возвращает ссылку на объект [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) , представляющий манифеста (XSF) шаблона формы, связанного с формой.  <br/> |
|Свойство [URI](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)  <br/> |Возвращает URI-идентификатор формы.  <br/> |
|Свойство [UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx)  <br/> |Возвращает или задает текущего пользователя для имени роли формы.  <br/> |
|Свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx)  <br/> |Возвращает ссылку на объект [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , связанный с шаблоном формы.  <br/> |
|Свойство [XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Возвращает значение атрибута **xml:lang** в базовом XML-документе формы.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Использование класса XmlFormCollection

Класс **XmlFormCollection** доступен через свойство [XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . В шаблона формы с управляемым кодом, созданных с помощью объектной модели, которая предоставляется элементами пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) можно использовать **Этот** (C#) или ключевое слово **Me** (Visual Basic) в код формы для доступа к **приложения **класс и его элементы. 
  
В следующем примере используется свойство **XmlForms** класса **Application** для создания объектной переменной myForms, которая указывает объект **XDocumentsCollection** запущенного в данный момент экземпляра InfoPath. Эта переменная впоследствии используется для отображения количества открытых форм. 
  
```cs
// Create variable for accessing the XmlFormCollection.
XmlFormCollection myForms = this.Application.XmlForms;
// Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count);
```

```vb
// Create variable for accessing the XmlFormCollection.
Dim myForms As XmlFormCollection = Me.Application.XmlForms
' Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count)
```

Переменную myForms также затем можно использовать для создания новых форм (с помощью одного из методов **New** или **NewFromTemplate**) или открытия существующих форм (с помощью одного из методов **Open**). 
  
## <a name="using-the-xmlform-class"></a>Использование класса XmlForm

В шаблона формы с управляемым кодом, созданных с помощью объектной модели, которая предоставляется элементами пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) можно использовать **Этот** (C#) или ключевое слово **Me** (Visual Basic) в код формы для доступа к элементам [ XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) класс (без необходимости установки объектную переменную, которая устанавливает ссылку на класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ). 
  
### <a name="accessing-a-forms-property-values"></a>Доступ к значениям свойств формы

В следующем примере используется ключевое слово **this** или **Me** для предоставления доступа к свойствам **New**, **ReadOnly**, **Signed** и **Uri** класса **XmlForm** и отображения в окне сообщения значений, возвращенных для текущей формы. 
  
```cs
MessageBox.Show(
   "Is new: " + this.New + System.Environment.NewLine +
   "Is read-only: " + this.ReadOnly + System.Environment.NewLine +
   "Is signed: " + this.Signed + System.Environment.NewLine +
   "Form URI: " + this.Uri);
```

```vb
MessageBox.Show( _
   "Is new: " &amp; Me.New &amp; System.Environment.NewLine &amp; _
   "Is read-only: " &amp; Me.ReadOnly &amp; System.Environment.NewLine + _
   "Is signed: " &amp; Me.Signed &amp; System.Environment.NewLine &amp; _
   "Form URI: " &amp; this.Uri)
```

### <a name="accessing-a-forms-data-source"></a>Доступ к источнику данных формы

Основные свойства класса **XmlForm** по отношению к данным формы является свойство **MainDataSource** . Данное свойство возвращает ссылку на объект [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , представляющий базовый XML-данные из текущей формы, которая также называется источник данных главной или основной формы. Класс **DataSource** предоставляет метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , который создает объект [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) , размещенный в корне базового документа XML формы. Свойства и методы класса **XPathNavigator** затем используется для перемещения и изменение базовых XML-данных формы. 
  
В следующем примере свойство **MainDataSource** класса **XmlForm** для создания объекта **XPathNavigator** , размещенный в корне формы в основном источнике данных. Свойство **OuterXml** класса **XPathNavigator** затем используется для определения и отображения все содержимое XML-документом формы. 
  
```cs
// Get outer XML of the underlying XML document.
string myDoc = this.MainDataSource.CreateNavigator.OuterXml.ToString();
// Display XML.
MessageBox.Show(myDoc);
```

```vb
' Get outer XML of the underlying XML document.
Dim myDoc As String myDoc = _
   Me.MainDataSource.CreateNavigator.OuterXml.ToString()
' Display XML.
MessageBox.Show(myDoc)
```

> [!NOTE]
> Поскольку приложение InfoPath рассматривает свойство **MainDataSource** как свойство по умолчанию объекта **XmlForm**, доступ к которому предоставляется при использовании ключевых слов **this** и **Me**, то можно опустить его в строке кода, используемой для создания объекта **XPathNavigator**. 
  
Чтобы узнать больше о класса **XPathNavigator** в бизнес-логике шаблона формы InfoPath, см [классов XPathNavigator и XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Доступ к сведениям о файле шаблона формы

Сведения о шаблоне формы, связанный с формой, включая файла определения формы (.xsf) и источник XML-данные, он содержит также осуществляется с помощью класса **XmlForm** . Эти сведения осуществляется с помощью свойства [шаблона](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) , который возвращает ссылку на объект [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) , представляющий шаблона формы, связанного с текущей формой. 
  
В следующем примере в первом окне сообщения отображаются некоторые данные, предоставляемые класса **шаблона** , например его местоположение универсальный код ресурса (URI) (с помощью свойства [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) ), идентификатор кэша (с помощью [CacheId ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx)свойство) и номер версии (с использованием свойство [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) ). Далее окно сообщения использует свойство [манифеста](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) класса **шаблон** для создания объекта **XPathNavigator** , который используется для отображения исходного XML файла определения формы (.xsf). 
  
```cs
// Display form template properties.
MessageBox.Show(
   "Cache ID: " + this.Template.CacheId + System.Environment.NewLine +
   "URI: " + this.ReadOnly + System.Environment.NewLine +
   "Version: " + this.Signed, "Form Template Properties");
// Display form definition file XML.
MessageBox.Show(this.Template.Manifest.OuterXml, 
   "Form Definition File XML");
```

```vb
' Display form template properties.
MessageBox.Show( _
   "Cache ID: " &amp; Me.Template.CacheId &amp; System.Environment.NewLine &amp;
   "URI: " &amp; Me.ReadOnly &amp; System.Environment.NewLine &amp;
   "Version: " &amp; Me.Signed, "Form Template Properties")
' Display form definition file XML.
MessageBox.Show(Me.Template.Manifest.OuterXml, _
   "Form Definition File XML")
```


