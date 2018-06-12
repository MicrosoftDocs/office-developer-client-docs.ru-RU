---
title: Работа с окнами форм, использующих объектную модель InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- шаблоны форм, совместимых 2003 InfoPath, форм windows form windows [InfoPath 2007], совместимых с InfoPath 2003 шаблонов форм
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: При работе программным путем с помощью формы InfoPath, можно написать код для доступа к форме windows и затем настроить некоторые элементы, которые они содержат. Объектная модель совместимых с InfoPath 2003 поддерживает доступ к windows формы посредством использования интерфейса WindowObject в сочетании с помощью интерфейса WindowsCollection.
ms.openlocfilehash: 4ca0fb53fd8502773d3e770814a5a24c40b2d79f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807516"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Работа с окнами форм, использующих объектную модель InfoPath 2003

При работе программным путем с помощью формы InfoPath, можно написать код для доступа к форме windows и затем настроить некоторые элементы, которые они содержат. Объектная модель совместимых с InfoPath 2003 поддерживает доступ к windows формы посредством использования интерфейса [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) в сочетании с помощью интерфейса [WindowsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) . 
  
В InfoPath существует два типа окон:
  
- Окно редактирования, которое используется при заполнении формы пользователем.
    
- Окно разработки, которое используется при разработке пользователем шаблона формы.
    
При написании кода в шаблоне формы, это окно редактирования, которое предоставляет возможности наиболее полезным, так как можно использовать экземпляр **WindowObject** , которая обращается к ним для доступа к различных свойств и методов, которые можно использовать для настройки формы процесс изменения. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Обзор интерфейса WindowsCollection

Интерфейс **WindowsCollection** предоставляет указанные ниже свойства, которыми разработчики форм могут пользоваться для управления экземплярами **WindowObject** , которые он содержит. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)  <br/> |Возвращает количество объектов **Window** , содержащихся в коллекции.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)  <br/> |Возвращает ссылку на указанный объект **Window** .  <br/> **Примечание**: Visual C# осуществляет доступ к коллекции с помощью индексатора вместо вызова свойство **Item** . Пример: `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Обзор объекта Window

Интерфейс **WindowObject** предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с окнами Microsoft InfoPath. Поддержка для этих методов и свойств отличаются в зависимости от типа окна ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ), с которыми выполняется. Некоторые методы и свойства работать только с типом окна Редактор (**XdWindowType.xdEditorWindow**). Оставшиеся методы и свойства, работать с типом окна Редактор и тип окно конструктора (**XdWindowType.xdDesignerWindow**). Кроме того как все InfoPath элементы объектной модели при вызове из шаблона формы поддержка методы и свойства могут различаться в зависимости от уровня безопасности и способ развертывания формы.
  
|**Имя**|**Описание**|**Поддержка типов окон**|
|:-----|:-----|:-----|
|Метод [Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx)  <br/> |Обозначает окно как активное в данный момент окно.   <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [активности](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx)  <br/> |Возвращает **логическое** значение, указывающее, является ли окно текущего активного окна.  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx)  <br/> |Свойство чтения и записи, которое возвращает или задает текст заголовка для окна, представленного объектом **Window** .  <br/> |Только тип **xdEditorWindow**  <br/> |
|Метод [Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)  <br/> |Закрывает окно.  <br/> |Только тип **xdEditorWindow**  <br/> |
|Свойство [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx)  <br/> |Возвращает ссылку на объект Microsoft Office **CommandBars** .  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [Height](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx)  <br/> |Свойство чтения и записи тип длинное целое, задающее высоту окна, представленную объектом **Window** и измеряемую в точках.  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [слева](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx)  <br/> |Свойство чтения и записи тип длинное целое, которое указывает горизонтальную позицию окна, представленного объектом **Window** и измеряемую в точках.  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx)  <br/> |Возвращает ссылку на объект [MailEnvelopeObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) .  <br/> |Только тип **xdEditorWindow**  <br/> |
|Свойство [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx)  <br/> |Возвращает ссылку на коллекцию [TaskPanesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) .  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [Top](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx)  <br/> |Свойство чтения и записи тип длинное целое, которое указывает вертикальную позицию окна, представленную объектом **Window** и измеряемую в точках.  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx)  <br/> |Возвращает номер, указывающий тип окна, основанный на перечисление [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) .  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [Width](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx)  <br/> |Свойство чтения и записи тип длинное целое, задающее ширину окна, представленную объектом **Window** и измеряемую в точках.  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx)  <br/> |Свойство чтения и записи типа [XdWindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) , которое возвращает или задает состояние окна, представленного объектом **Window** .  <br/> |**Типы xdDesignWindow** и **xdEditorWindow** типов  <br/> |
|Свойство [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx)  <br/> |Возвращает ссылку на объект [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) , связанный с окном.  <br/> |Только тип **xdEditorWindow**  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Использование интерфейсов WindowsCollection и Window

Интерфейс **WindowsCollection** может осуществляться через свойство [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . При использовании интерфейса **WindowsCollection** для доступа к формы windows, можно использовать индексатор (для Visual C#) или передать длинное целое свойство **Item** (в Visual Basic) возвращает ссылку на экземпляр интерфейса **WindowObject** . Например следующий пример кода задает ссылку на первый **WindowObject** , содержащихся в **WindowsCollection**.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

Тем не менее, можно получить доступ к открытая в настоящий момент окно непосредственно, используя свойство [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) интерфейса **приложения** без прохода через ** WindowsCollection **, как показано в следующем коде.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> При отладке проекта InfoPath управляемым кодом свойство **ActiveWindow** всегда возвращает **значение null,** поскольку окно отладки активно. 
  
Доступ к **WindowObject** можно получить с помощью свойства [окна](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) интерфейса [представления](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) , который связан с XML-документом формы. Свойство **представления** интерфейса **XDocument** используется для доступа к объекту **представления** . Например следующий пример кода задает ссылку на **WindowObject** , связанный с представлением XML-документом формы. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> Некоторые свойства и методы объекта **Window** — только для типа окна редактирования; Если разработка тип окна, они возвращают ошибку. В таблице показано ранее в этом разделе перечислены свойства и методы, которые поддерживаются для каждого типа окна. Чтобы определить, какой тип окна, с которыми выполняется можно использовать свойство **WindowType** в коде. 
  

