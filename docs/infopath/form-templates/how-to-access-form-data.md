---
title: Доступ к данным формы
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- данные форм [InfoPath 2007], формы [InfoPath 2007], доступ к свойствам, шаблонам форм [InfoPath 2007], доступ к свойствам, открытие форм [InfoPath 2007], печать форм [InfoPath 2007], формы [InfoPath 2007], печать, закрытие форм [InfoPath 2007], InfoPath 2007, доступ к данным формы, формы [InfoPath 2007], доступ к источнику данных, формы [InfoPath 2007], закрытие, формы [InfoPath 2007], открытие, печать [InfoPath 2007], формы, формы [InfoPath 2007]
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Если требуется расширить функциональность формы InfoPath, то зачастую требуется обеспечить программный доступ к сведениям о базовом XML-документе формы или к данным, содержащимся в этом XML-документе, а также выполнить некоторые действия над XML-документом. Объектная модель InfoPath поддерживает доступ к базовому XML-документу формы и управление им с помощью класса XmlForm в связи с классом XmlFormCollection.
ms.openlocfilehash: c8251afcd75391f102215811694515c06b9f3e7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300212"
---
# <a name="access-form-data"></a>Доступ к данным формы

Если требуется расширить функциональность формы InfoPath, то зачастую требуется обеспечить программный доступ к сведениям о базовом XML-документе формы или к данным, содержащимся в этом XML-документе, а также выполнить некоторые действия над XML-документом. Объектная модель InfoPath поддерживает доступ к базовому XML-документу формы и управление им с помощью класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) в связи с классом [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) . 
  
Класс [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) является одним из наиболее эффективных типов в объектной модели InfoPath, так как он предоставляет разнообразные свойства и методы, которые не только взаимодействуют с базовым XML-документом формы, но и выполняют многие действия, доступные в пользовательском интерфейсе InfoPath. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Обзор класса XmlFormCollection

Класс [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для управления объектами [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , содержащимися в коллекции. 
  
|**Название**|**Описание**|
|:-----|:-----|
|Метод [New (String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx)  <br/> |Создает новую форму на основе указанной формы.  <br/> |
|Метод [New (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (перегрузка 1)  <br/> |Создает новую форму на основе указанной формы с использованием указанного поведения режима открытия.  <br/> |
|Метод [Метод NewFromFormTemplate (String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |Создает новую форму на основе указанного шаблона формы.  <br/> |
|Метод [Метод NewFromFormTemplate (String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (Overload 1)  <br/> |Создает новую форму на основе указанного шаблона формы и XML-данных.  <br/> |
|Метод [Метод NewFromFormTemplate (String, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (перегрузка 2)  <br/> |Создает новую форму на основе указанного шаблона формы с данными, указанными в объекте [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) .  <br/> |
|Метод [Метод NewFromFormTemplate (String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (перегрузка 3)  <br/> |Создает новую форму на основе указанного шаблона формы с данными, указанными объектом **XPathNavigator**, и с использованием указанного поведения режима открытия.  <br/> |
|Метод [Open (String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx)  <br/> |Открывает указанную форму.  <br/> |
|Метод [Open (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (перегрузка 1)  <br/> |Открывает указанную форму с использованием указанного поведения режима открытия.  <br/> |
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)  <br/> |Возвращает количество объектов **XmlForm**, содержащихся в семействе.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **XmlForm** из семейства по значению индекса.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Обзор интерфейса XmlForm

Класс [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с базовым XML-документом формы и выполнения действий над ним. 
  
|**Название**|**Описание**|
|:-----|:-----|
|Метод [Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)  <br/> |Закрывает форму.  <br/> |
|Метод [жетворкфловтаскс](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx)  <br/> |Возвращает ссылку на коллекцию **Microsoft.Office.Core.WorkflowTasks** для текущей формы.  <br/> |
|Метод [жетворкфловтемплатес](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx)  <br/> |Возвращает ссылку на коллекцию **Microsoft.Office.Core.WorkflowTemplates** для текущей формы.  <br/> |
|Метод [MergeForm (String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |Объединяет текущую форму с формой, указанной с помощью пути или URL-адреса.  <br/> |
|Метод [MergeForm (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (перегрузка 1)  <br/> |Объединяет текущую форму с формой, указанной в узле, возвращаемым переданным в метод объектом **XPathNavigator**.  <br/> |
|Метод [NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx)  <br/> |Предоставляет пользовательское значение для внешнего приложения или ASPX-страницы.  <br/> |
|Метод [Print ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx)  <br/> |Печатает содержимое формы, отображаемое в активном представлении формы.  <br/> |
|Метод [Print (Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (перегрузка 1)  <br/> |Печатает содержимое формы, отображаемое в активном представлении формы, отображая диалоговое окно " **Печать** ".  <br/> |
|Метод [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)  <br/> |Сохраняет форму по указанному URL-адресу, с которым она в настоящий момент связана.  <br/> |
|Метод [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)  <br/> |Сохраняет форму по указанному URL-адресу.  <br/> |
|Метод [SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx)  <br/> |Устанавливает имя файла по умолчанию для диалогового окна **SaveAs**.  <br/> |
|Метод [SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx)  <br/> |Устанавливает путь по умолчанию для сохранения формы с помощью диалогового окна **SaveAs**.  <br/> |
|Метод [Reоправить](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx)  <br/> |Отправляет форму с помощью операции отправки, определенной в шаблоне формы.  <br/> |
|Свойство [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx)  <br/> |Возвращает объект [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , представляющий текущее представление формы.  <br/> |
|Свойство [Connections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx)  <br/> |Получает объект [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) , связанный с формой.  <br/> |
|Свойство [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)  <br/> |Получает объект [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) , связанный с формой.  <br/> |
|Свойство [Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx)  <br/> |Получает значение, указывающее на то, были ли изменены данные формы с момента последнего сохранения.  <br/> |
|Свойство [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx)  <br/> |Возвращает ссылку на [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) , связанную с формой.  <br/> |
|Свойство [Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx)  <br/> |Получает объект [System. Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) для доступа к функциям и глобальным переменным, которые хранятся в основном файле кода формы с помощью [System. Reflection](https://msdn.microsoft.com/library/system.reflection(v=vs.110).aspx).  <br/> |
|Свойство [контейнере FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Возвращает ссылку на контейнер свойств [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) типа, которые могут использовать формы с поддержкой браузера для обработки сведений о состоянии сеансов на сервере.  <br/> |
|Свойство [Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx)  <br/> |Возвращает [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx), который код, запущенный в размещенном экземпляре InfoPath, может использовать для доступа к объектной модели внешнего приложения.  <br/> |
|[Размещаемое](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) свойство  <br/> |Определяет, размещен ли InfoPath в качестве элемента управления в другом приложении.  <br/> |
|Свойство [HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx)  <br/> |Возвращение имени приложения,где размещается InfoPath в качестве элемента управления.  <br/> |
|Свойство [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx)  <br/> |Получает объект [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , представляющий основной источник данных формы.  <br/> |
|Свойство [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx)  <br/> |Возвращает ссылку на объект [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) , который можно использовать для разрешения, добавления или удаления пространств имен, используемых в форме.  <br/> |
|[Новое](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) свойство  <br/> |Возвращает значение, которое указывает, является ли форма новой.  <br/> |
|Свойство [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx)  <br/> |Возвращает ссылку на объект [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) , связанный с формой.  <br/> |
|Свойство [куеридатаконнектион](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx)  <br/> |Возвращает ссылку на объект [подключения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) к данным, который представляет подключение к данным, связанное с формой.  <br/> |
|Свойство [ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx)  <br/> |Возвращает значение, которое указывает, имеет ли шаблон доступ только для чтение или заблокирован.  <br/> |
|[Восстановленное](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) свойство  <br/> |Получает значение, указывающее, была ли при предыдущем сохранении формы использована операция сохранения AutoRecover.  <br/> |
|Свойство [signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx)  <br/> |Получает значение, указывающее, была ли форма подписана с использованием цифровой подписи.  <br/> |
|Свойство [сигнеддатаблоккс](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx)  <br/> |Возвращает ссылку на коллекцию [сигнеддатаблоккколлектион](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) , связанную с формой.  <br/> |
|Свойство [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx)  <br/> |Возвращает ссылку на [коллекции TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) , связанную с шаблоном формы.  <br/> |
|Свойство [template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx)  <br/> |Возвращает ссылку на объект [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) , представляющий манифест (XSF) шаблона формы, связанного с формой.  <br/> |
|Свойство [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)  <br/> |Получает универсальный код ресурса (URI) формы.  <br/> |
|Свойство [UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx)  <br/> |Возвращает или задает текущего пользователя имени роли формы.  <br/> |
|Свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx)  <br/> |Возвращает ссылку на объект [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , связанный с шаблоном формы.  <br/> |
|Свойство [ксмлланг](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Получает значение атрибута **XML: lang** в БАЗОВОМ XML-документе формы.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Использование класса XmlFormCollection

Доступ к классу **XmlFormCollection** осуществляется с помощью свойства [ксмлформс](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . В шаблоне формы с управляемым кодом, созданном с помощью объектной модели, предоставляемой элементами пространства имен [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , вы можете использовать ключевое слово **this** (C#) или **Me** (Visual Basic) в коде формы для доступа к классу **Application** и его членам. 
  
В следующем примере используется свойство **ксмлформс** класса **Application** для создания объектной переменной с именем миформс, которая ссылается на объект **XDocumentsCollection** в запущенном в данный момент экземпляре InfoPath. Эта переменная затем используется для отображения количества открытых форм. 
  
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

Кроме того, переменную Миформс можно использовать для создания новых форм (с помощью одного из методов **New** или **невфромтемплате** ) или открыть существующие формы (с помощью одного из методов **Open** ). 
  
## <a name="using-the-xmlform-class"></a>Использование класса XmlForm

В шаблоне формы с управляемым кодом, созданном с помощью объектной модели, предоставляемой элементами пространства имен [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , можно использовать ключевое слово **this** (C#) или **Me** (Visual Basic) в коде формы для прямого доступа к членам класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (без необходимости использовать объектную переменную, которая устанавливает ссылку на класс [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ). 
  
### <a name="accessing-a-forms-property-values"></a>Доступ к значениям свойств формы

В следующем примере используется ключевое слово **this** или **Me** для доступа к свойствам **New**, **ReadOnly**, **signed**и **URI** класса **XmlForm** и отображаются значения, возвращенные для текущей формы в окне сообщения. 
  
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

Ключевым свойством класса **XmlForm** , в отношении которого являются данные формы, является свойство **MainDataSource** . Это свойство возвращает ссылку на объект [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , представляющий базовые XML-данные текущей формы, которые также называют основным или основным источником данных формы. Класс **DataSource** предоставляет метод [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , который создает объект [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) , РАЗМЕЩЕННЫЙ в корне базового XML-документа формы. Затем свойства и методы класса **XPathNavigator** можно использовать для навигации и редактирования базовых XML-данных формы. 
  
В следующем примере используется свойство **MainDataSource** класса **XmlForm** для создания объекта **XPathNavigator** , расположенного в корне основного источника данных формы. Затем свойство **OuterXml** класса **XPathNavigator** используется для возврата и отображения всего содержимого базового XML-документа формы. 
  
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
> Так как InfoPath обрабатывает свойство **MainDataSource** как свойство по умолчанию объекта **XmlForm** , доступного при использовании **этих** ключевых **слов** или ключевых слов, можно опустить его из строки кода, использованной для создания объекта **XPathNavigator** . 
  
Чтобы узнать больше о классе **XPathNavigator** в бизнес-логике шаблона формы InfoPath, ознакомьтесь со статьей [Работа с классами XPathNavigator и XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Доступ к данным о файле шаблона формы формы

Также можно получить **доступ к** сведениям о шаблоне формы, связанном с формой, включая файл определения формы (XSF) и исходные данные XML, которые он содержит. Доступ к этой информации осуществляется с помощью свойства [template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) , которое возвращает ссылку на объект [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) , представляющий шаблон формы, связанный с текущей формой. 
  
В следующем примере в первом окне сообщения отображаются некоторые данные, доступные через класс **template** , такие как расположение URI (с помощью свойства [URI](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) ), идентификатор кэша (с использованием свойства [cacheID](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) ) и его номер версии (с помощью свойства [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) ). В следующем окне сообщения для создания объекта **XPathNavigator** , используемого для отображения исходного XML-кода файла определения формы (XSF), используется свойство [manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) класса **template** . 
  
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


