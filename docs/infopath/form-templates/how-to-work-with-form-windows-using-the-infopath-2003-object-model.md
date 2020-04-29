---
title: Работать с окнами форм с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- шаблоны форм, совместимые с InfoPath 2003, окна форм, окна форм [InfoPath 2007], InfoPath 2003 совместимые шаблоны форм
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: При работе с формой InfoPath программным образом можно написать код для доступа к окнам формы, а затем настроить некоторые содержащиеся в них элементы. Объектная модель, совместимая с InfoPath 2003, поддерживает доступ к окнам формы с помощью интерфейса WindowObject в связи с интерфейсом WindowsCollection.
ms.openlocfilehash: f8939fc562cf16c1bce0f6f88bba659e895254f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427579"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Работать с окнами форм с помощью объектной модели InfoPath 2003

При работе с формой InfoPath программным образом можно написать код для доступа к окнам формы, а затем настроить некоторые содержащиеся в них элементы. Объектная модель, совместимая с InfoPath 2003, поддерживает доступ к окнам формы с помощью интерфейса [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) в связи с интерфейсом [WindowsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) . 
  
В InfoPath существует два типа окон:
  
- Окно редактирования, которое используется при заполнении формы пользователем.
    
- Окно разработки, которое используется при разработке пользователем шаблона формы.
    
При написании кода в шаблоне формы наиболее удобные функциональные возможности обеспечивает окно редактирования, поскольку оно позволяет использовать экземпляр **WindowObject**, который указывает на него для доступа к целому ряду свойств и методов, которые можно использовать для настройки процесса редактирования формы. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Обзор интерфейса WindowsCollection

Интерфейс **WindowsCollection** предоставляет указанные ниже свойства, которыми разработчики форм могут пользоваться для управления экземплярами **WindowObject**, содержащимися в интерфейсе. 
  
|**Название**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)  <br/> |Возвращает количество объектов  **Window** в семействе.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **Window**.  <br/> **Note**: Visual C# обращается к коллекциям с помощью индексатора вместо вызова свойства **Item** . Пример: `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Обзор объекта Window

Интерфейс **WindowObject** предоставляет указанные ниже методы и свойства, которыми разработчики форм могут пользоваться для взаимодействия с окном InfoPath. Поддержка этих методов и свойств зависит от типа окна ( [ксдвиндовтипе](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ), с которым ведется работа. Некоторые методы и свойства работают только с окном редактора (**XdWindowType.xdEditorWindow**). Остальные методы и свойства работают как с окном редактора, так и с окном конструктора (**XdWindowType.xdDesignerWindow**). Кроме того, как и для всех членов объектной модели InfoPath, при вызове из шаблона формы поддержка методов и свойств может изменяться в зависимости от уровня безопасности и метода развертывания формы.
  
|**Название**|**Описание**|**Поддержка типов окон**|
|:-----|:-----|:-----|
|Метод [Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx)  <br/> |Обозначает окно как активное в данный момент окно.  <br/> |Типы **xdDesignWindow** и **xdEditorWindow**  <br/> |
|Свойство [Active](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx)  <br/> |Возвращает логическое (**Boolean**) значение, указывающее, является ли окно активным в данный момент.  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx)  <br/> |Свойство чтения и записи, которое возвращает или задает текст заголовка окна, представленного объектом **Window**.  <br/> |Только тип **xdEditorWindow**  <br/> |
|Метод [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)  <br/> |Закрывает окно.  <br/> |Только тип **xdEditorWindow**  <br/> |
|Свойство [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx)  <br/> |Возвращает ссылку на объект Microsoft Office **CommandBars**.  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [Height](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx)  <br/> |Свойство чтения и записи с типом "длинное целое", которое указывает высоту окна, представленную объектом **Window** и измеряемую в точках.  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [Left](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx)  <br/> |Свойство чтения и записи с типом "длинное целое", которое указывает горизонтальную позицию окна, представленную объектом **Window** и измеряемую в точках.  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx)  <br/> |Возвращает ссылку на объект [MailEnvelopeObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) .  <br/> |Только тип **xdEditorWindow**  <br/> |
|Свойство [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx)  <br/> |Возвращает ссылку на коллекцию [таскпанесколлектион](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) .  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [Top](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx)  <br/> |Свойство чтения и записи с типом "длинное целое", которое указывает вертикальную позицию окна, представленную объектом **Window** и измеряемую в точках.  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [виндовтипе](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx)  <br/> |Возвращает число, обозначающее тип окна, на основе перечисления [ксдвиндовтипе](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) .  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [Width](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx)  <br/> |Свойство чтения и записи с типом "длинное целое", которое указывает ширину окна, представленную объектом **Window** и измеряемую в точках.  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx)  <br/> |Свойство чтения и записи типа [ксдвиндовстате](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) , которое возвращает или задает состояние окна, представленное объектом **Window** .  <br/> |Типы **типы xddesignwindow** и **xdEditorWindow**  <br/> |
|Свойство [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx)  <br/> |Возвращает ссылку на объект [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) , связанный с окном.  <br/> |Только тип **xdEditorWindow**  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Использование интерфейсов WindowsCollection и Window

Доступ к интерфейсу **WindowsCollection** можно получить с помощью свойства [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . При использовании интерфейса **WindowsCollection** для доступа к окнам форм используется индексатор (в Visual C#) или передача длинного целого для свойства **Item** (в Visual Basic), чтобы вернуть ссылку на экземпляр интерфейса **WindowObject**. Например, следующий код задает ссылку на первый объект **WindowObject**, содержащийся в **WindowsCollection**.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

Тем не менее, вы можете получить доступ к открытому в данный момент окну напрямую с помощью свойства [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) интерфейса **приложения** , не проходящих через * * WindowsCollection * *, как показано в следующем коде.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> При отладке проекта InfoPath с управляемым кодом свойство **ActiveWindow** всегда будет возвращать **null**, поскольку окно отладки активно. 
  
Доступ к **WindowObject** можно также получить с помощью свойства [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) интерфейса [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) , связанного с базовым XML-документом формы. Свойство **View** интерфейса **XDocument** используется для доступа к объекту **View**. Например, следующий код задает ссылку на объект **WindowObject**, который связан с представлением базового XML-документа формы. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> Некоторые свойства и методы объекта **Window** относятся только к типу окна редактирования; При использовании с типом окна "Разработка" они возвращают ошибку. Свойства и методы, поддерживаемые для каждого типа окна, перечислены в таблице, показанной ранее в этой статье. Вы можете использовать свойство **виндовтипе** в своем коде, чтобы определить тип окна, с которым вы работаете. 
  

