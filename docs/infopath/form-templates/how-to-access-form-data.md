---
title: Доступ к данным формы
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form data [infopath 2007],forms [InfoPath 2007], accessing properties,form templates [InfoPath 2007], accessing properties,opening forms [InfoPath 2007],printing forms [InfoPath 2007],forms [InfoPath 2007], printing,closing forms [InfoPath 2007],InfoPath 2007, accessing form data,forms [InfoPath 2007], accessing data source,forms [InfoPath 2007], closing,forms [InfoPath 2007], opening,printing [InfoPath 2007], forms,forms [InfoPath 2007], creating
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Если требуется расширить функциональность формы InfoPath, то зачастую требуется обеспечить программный доступ к сведениям о базовом XML-документе формы или к данным, содержащимся в этом XML-документе, а также выполнить некоторые действия над XML-документом. Объектная модель InfoPath поддерживает доступ к основному XML-документу формы и управление ими с помощью класса XmlForm в связи с классом XmlFormCollection.
ms.openlocfilehash: c8251afcd75391f102215811694515c06b9f3e7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300212"
---
# <a name="access-form-data"></a>Доступ к данным формы

Если требуется расширить функциональность формы InfoPath, то зачастую требуется обеспечить программный доступ к сведениям о базовом XML-документе формы или к данным, содержащимся в этом XML-документе, а также выполнить некоторые действия над XML-документом. Объектная модель InfoPath поддерживает доступ к основному XML-документу формы и управление ими с помощью класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) в связи с классом [XmlFormCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) 
  
Класс [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) является одним из наиболее полезных типов в объектной модели InfoPath, так как он предоставляет различные свойства и методы, которые не только взаимодействуют с XML-документом формы, но и выполняют многие действия, доступные в пользовательском интерфейсе InfoPath. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Обзор класса XmlFormCollection

Класс [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) предоставляет следующие методы и свойства, которые разработчики форм могут использовать для управления объектами [XmlForm,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) которые содержит коллекция. 
  
|**Название**|**Описание**|
|:-----|:-----|
|[Метод New(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx)  <br/> |Создает новую форму на основе указанной формы.  <br/> |
|[Метод New(String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (перегрузка 1)  <br/> |Создает новую форму на основе указанной формы с использованием указанного поведения режима открытия.  <br/> |
|[Метод NewFromFormTemplate(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |Создает новую форму на основе указанного шаблона формы.  <br/> |
|[Метод NewFromFormTemplate(String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (перегрузка 1)  <br/> |Создает новую форму на основе указанного шаблона формы и XML-данных.  <br/> |
|[Метод NewFromFormTemplate(String, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (перегрузка 2)  <br/> |Создает новую форму на основе указанного шаблона формы с данными, указанными объектом [XPathNavigator.](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx)  <br/> |
|[Метод NewFromFormTemplate(String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (перегрузка 3)  <br/> |Создает новую форму на основе указанного шаблона формы с данными, указанными объектом **XPathNavigator**, и с использованием указанного поведения режима открытия.  <br/> |
|[Метод Open(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx)  <br/> |Открывает указанную форму.  <br/> |
|[Метод Open(String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (перегрузка 1)  <br/> |Открывает указанную форму с использованием указанного поведения режима открытия.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)  <br/> |Возвращает количество объектов **XmlForm**, содержащихся в семействе.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **XmlForm** из семейства по значению индекса.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Обзор интерфейса XmlForm

Класс [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) предоставляет следующие методы и свойства, которые разработчики форм могут использовать для взаимодействия и выполнения действий над XML-документом формы. 
  
|**Название**|**Описание**|
|:-----|:-----|
|Метод [Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)  <br/> |Закрывает форму.  <br/> |
|[Метод GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx)  <br/> |Возвращает ссылку на коллекцию **Microsoft.Office.Core.WorkflowTasks** для текущей формы.  <br/> |
|[Метод GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx)  <br/> |Возвращает ссылку на коллекцию **Microsoft.Office.Core.WorkflowTemplates** для текущей формы.  <br/> |
|[Метод MergeForm(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |Объединяет текущую форму с формой, указанной с помощью пути или URL-адреса.  <br/> |
|[Метод MergeForm(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (перегрузка 1)  <br/> |Объединяет текущую форму с формой, указанной в узле, возвращаемым переданным в метод объектом **XPathNavigator**.  <br/> |
|[Метод NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx)  <br/> |Предоставляет пользовательское значение для внешнего приложения или ASPX-страницы.  <br/> |
|[Метод Print()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx)  <br/> |Печатает содержимое формы, отображаемое в активном представлении формы.  <br/> |
|[Метод Print(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (перегрузка 1)  <br/> |Печатает содержимое формы при отображке в активном представлении формы, отображая **диалоговое** окно "Печать".  <br/> |
|[Метод Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)  <br/> |Сохраняет форму по указанному URL-адресу, с которым она в настоящий момент связана.  <br/> |
|[Метод SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)  <br/> |Сохраняет форму по указанному URL-адресу.  <br/> |
|[Метод SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx)  <br/> |Устанавливает имя файла по умолчанию для диалогового окна **SaveAs**.  <br/> |
|[Метод SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx)  <br/> |Устанавливает путь по умолчанию для сохранения формы с помощью диалогового окна **SaveAs**.  <br/> |
|[Метод Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx)  <br/> |Отправляет форму с помощью операции отправки, определенной в шаблоне формы.  <br/> |
|[Свойство CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx)  <br/> |Получает объект [View,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) который представляет текущее представление формы.  <br/> |
|[Свойство DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx)  <br/> |Получает объект [DataConnectionCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) связанный с формой.  <br/> |
|[Свойство DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)  <br/> |Получает объект [DataSourceCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) связанный с формой.  <br/> |
|Свойство [Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx)  <br/> |Получает значение, указывающее на то, были ли изменены данные формы с момента последнего сохранения.  <br/> |
|[Свойство Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx)  <br/> |Возвращает ссылку на [FormErrorCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) связанную с формой.  <br/> |
|[Свойство Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx)  <br/> |Получает [system.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) для доступа к функциям и глобальным переменным, содержанымся в основном файле кода формы формы, с помощью [System.Reflection.](https://msdn.microsoft.com/library/system.reflection(v=vs.110).aspx)  <br/> |
|[Свойство FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Возвращает ссылку на контейнер свойств [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) типа, которые могут использовать формы с поддержкой браузера для обработки сведений о состоянии сеансов на сервере.  <br/> |
|[Свойство Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx)  <br/> |Возвращает [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx), который код, запущенный в размещенном экземпляре InfoPath, может использовать для доступа к объектной модели внешнего приложения.  <br/> |
|[Свойство Hosted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx)  <br/> |Определяет, размещен ли InfoPath в качестве элемента управления в другом приложении.  <br/> |
|[Свойство HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx)  <br/> |Возвращение имени приложения,где размещается InfoPath в качестве элемента управления.  <br/> |
|[Свойство MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx)  <br/> |Получает объект [DataSource,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) который представляет основной источник данных формы.  <br/> |
|[Свойство NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx)  <br/> |Возвращает ссылку на [объект XmlNamespaceManager,](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) который можно использовать для разрешения, добавления или удаления пространств имен, используемых в форме.  <br/> |
|[Новое](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) свойство  <br/> |Возвращает значение, которое указывает, является ли форма новой.  <br/> |
|[Свойство Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx)  <br/> |Возвращает ссылку на объект [Permission,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) связанный с формой.  <br/> |
|[Свойство QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx)  <br/> |Получает ссылку на объект [DataConnection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) который представляет подключение к данным, связанное с формой.  <br/> |
|[Свойство ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx)  <br/> |Возвращает значение, которое указывает, имеет ли шаблон доступ только для чтение или заблокирован.  <br/> |
|[Свойство Recovered](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx)  <br/> |Получает значение, указывающее, была ли при предыдущем сохранении формы использована операция сохранения AutoRecover.  <br/> |
|[Свойство Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx)  <br/> |Получает значение, указывающее, была ли форма подписана с использованием цифровой подписи.  <br/> |
|[Свойство SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx)  <br/> |Возвращает ссылку на коллекцию [SignedDataBlockCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) связанную с формой.  <br/> |
|[Свойство TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx)  <br/> |Возвращает ссылку на [TaskPaneCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) связанную с шаблоном формы.  <br/> |
|[Свойство Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx)  <br/> |Возвращает ссылку на [объект FormTemplate,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) который представляет манифест (XSF) шаблона формы, связанного с формой.  <br/> |
|Свойство [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)  <br/> |Получает универсальный код ресурса (URI) формы.  <br/> |
|[Свойство UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx)  <br/> |Возвращает или задает текущего пользователя имени роли формы.  <br/> |
|[Свойство ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx)  <br/> |Возвращает ссылку на [объект ViewInfoCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) связанный с шаблоном формы.  <br/> |
|[Свойство XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Получает значение атрибута **xml:lang** в основном XML-документе формы.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Использование класса XmlFormCollection

Доступ **к классу XmlFormCollection** можно получить с помощью свойства [XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) класса [Application.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) В шаблоне формы с управляемым кодом, созданном с помощью объектной модели, предоставляемой членами пространства имен [Microsoft.Office.InfoPath,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) можно использовать это **ключевое** слово (C#) или **Me** (Visual Basic) в коде формы для доступа к классу **Application** и его членам. 
  
В следующем примере свойство **XmlForms** класса **Application** используется для создания объектной переменной с именем myForms, которая ссылается на объект **XDocumentsCollection** запущенного экземпляра InfoPath. Затем эта переменная используется для отображения количество открытых форм. 
  
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

Затем переменную myForms можно также использовать для создания новых форм (с помощью одного из методов **New** или **NewFromTemplate)** или открытия существующих форм (с помощью одного из методов **Open).** 
  
## <a name="using-the-xmlform-class"></a>Использование класса XmlForm

В шаблоне формы с управляемым кодом, созданном с помощью объектной модели, предоставляемой членами пространства имен [Microsoft.Office.InfoPath,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) можно использовать это ключевое слово  (C#) или **Me** (Visual Basic) в коде формы для прямого доступа к членам класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (без необходимости объектной переменной, которая устанавливает ссылку на класс [XmlForm).](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) 
  
### <a name="accessing-a-forms-property-values"></a>Доступ к значениям свойств формы

В следующем примере  ключевое слово "или я" используется для доступа к свойствам **New,** **ReadOnly,** Signed и  **Uri** класса **XmlForm** и отображения значений, возвращаемого для текущей формы, в окне сообщения.  
  
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

Ключевое свойство класса **XmlForm** в отношении данных формы — это свойство **MainDataSource.** Это свойство возвращает ссылку на объект [DataSource,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) который представляет основные XML-данные текущей формы, который также называется основным или основным источником данных формы. Класс **DataSource** предоставляет метод [CreateNavigator,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) который создает объект [XPathNavigator,](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) который находится в корневом формате XML-документа формы. Затем свойства и методы класса **XPathNavigator** можно использовать для навигации и изменения данных XML формы. 
  
В следующем примере свойство **MainDataSource** класса **XmlForm** используется для создания объекта **XPathNavigator,** расположенного в корне основного источника данных формы. Затем **свойство OuterXml** класса **XPathNavigator** используется для возврата и отображения всего содержимого XML-документа формы. 
  
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
> Так как InfoPath обрабатывает свойство **MainDataSource** как свойство по умолчанию объекта **XmlForm,** доступного при использовании ключевых слов **этого** или me, его можно опустить из строки кода, используемой для создания объекта **XPathNavigator.**  
  
Дополнительные сведения о классе **XPathNavigator** в бизнес-логике шаблона формы InfoPath см. в подзаголовке "Работа с [классами XPathNavigator и XPathNodeIterator".](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Доступ к данным о файле шаблона формы

Доступ к сведениям о шаблоне формы, связанном с формой, включая файл определения формы (XSF) и исходные XML-данные, которые она содержит, также можно получить с помощью класса **XmlForm.** Доступ к этим сведениям можно получить с помощью свойства [Template,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) которое возвращает ссылку на объект [FormTemplate,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) который представляет шаблон формы, связанный с текущей формой. 
  
В следующем примере в первом окне сообщения отображаются некоторые данные, доступные через класс **Template,** например его расположение URI (с использованием свойства [URI),](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) идентификатор кэша (с использованием свойства [CacheId)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) и номер версии (с использованием свойства [Version).](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) В следующем окне сообщения используется свойство [Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) класса **Template** для создания объекта **XPathNavigator,** который используется для отображения XML-кода источника файла определения формы (XSF). 
  
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


