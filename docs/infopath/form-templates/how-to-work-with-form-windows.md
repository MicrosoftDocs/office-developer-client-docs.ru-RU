---
title: Работа с окнами форм
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007] окна формы [InfoPath 2007], класс "Window" [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: При работе программным путем с помощью формы InfoPath, можно написать код для доступа к форме windows и затем настроить некоторые элементы, которые они содержат. Объектная модель InfoPath, предоставляемой поддерживает доступ пространства имен Microsoft.Office.InfoPath к windows формы посредством использования класса Window в сочетании с классом WindowCollection.
ms.openlocfilehash: 5b24798e92849a2d79bf836e12dd91845ee58942
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807518"
---
# <a name="work-with-form-windows"></a>Работа с окнами форм

При работе программным путем с помощью формы InfoPath, можно написать код для доступа к форме windows и затем настроить некоторые элементы, которые они содержат. Объектная модель InfoPath, предоставляемой поддерживает доступ пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) к windows формы посредством использования класса [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) в сочетании с классом [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) . 
  
> [!NOTE]
> Классы для работы с окном формы доступны только при работе с **Формой редактора InfoPath**. Если параметр **Совместимость** шаблона формы имеет значение **Форма веб-браузера**, эти классы не будут доступны. 
  
В InfoPath существует два типа окон:  
  
- окно редактирования, которое используется при заполнении формы пользователем;
    
- окно разработки, которое используется при разработке пользователем шаблона формы.
    
При написании кода в шаблоне формы, это окно редактирования, которое предоставляет возможности наиболее полезным, так как можно использовать объект [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , представляющий текущее окно для доступа к Выбор свойств и методов, которые можно использовать для настройки Форма редактирования качества. 
  
## <a name="overview-of-the-windowscollection-class"></a>Обзор класса "WindowsCollection"

Класс [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) предоставляет следующие свойства, которые разработчики форм могут использоваться для управления объектами [окна](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , которые он содержит. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)  <br/> |Возвращает количество объектов [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , содержащихся в коллекции.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)  <br/> |Возвращает ссылку на указанный объект [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) .  <br/> |
   
## <a name="overview-of-the-window-class"></a>Обзор класса "Window"

Класс [окна](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с окнами Microsoft InfoPath. Поддержка для этих методов и свойств отличаются в зависимости от типа окна ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ), с которыми выполняется. Некоторые методы и свойства работать только с типом окна Редактор (**WindowType.Editor**). Оставшиеся методы и свойства, работать с типом окна Редактор и тип окно конструктора (**WindowType.Designer**). Кроме того как все InfoPath элементы объектной модели при вызове из шаблона формы поддержка методы и свойства могут различаться в зависимости от уровня безопасности и способ развертывания формы.
  
|**Имя**|**Описание**|**Поддержка типов окон**|
|:-----|:-----|:-----|
|Метод [Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx)  <br/> |Активирует окно (переключает фокус).   <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [активности](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx)  <br/> |Возвращает логическое (**Boolean**) значение, указывающее, является ли окно активным в данный момент.  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Получает или задает текст заголовка для окна, представленного объектом [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) .  <br/> |Только тип **Editor**  <br/> |
|Метод [Close()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Закрывает окно с запросом на сохранение изменений для любой несохраненной формы или формы, изменения которой не были сохранены.  <br/> |Только тип **Editor**  <br/> |
|Метод [Close(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Закрывает окно и позволяет при необходимости принудительно закрыть без сохранения несохраненную форму или форму с несохраненными изменениями.   <br/> |Только тип **Editor**  <br/> |
|Свойство [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx)  <br/> |Возвращает ссылку на коллекцию Microsoft Office **CommandBars**, связанную с окном.  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx)  <br/> |Возвращает или задает высоту окна, измеряемую в точках.  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [слева](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Возвращает или задает горизонтальную позицию окна, измеряемую в точках.  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Возвращает ссылку на класс [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) .  <br/> |Только тип **Editor**  <br/> |
|Свойство [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx)  <br/> |Возвращает ссылку на коллекцию [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) .  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx)  <br/> |Возвращает или задает вертикальную позицию окна, измеряемую в точках.  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Возвращает или задает ширину окна, измеряемую в точках.  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx)  <br/> |Получает или задает состояние окна как значение [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) .  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx)  <br/> |Возвращает тип окна как значение перечисления [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) .  <br/> |Типы **Designer** и **Editor**  <br/> |
|Свойство [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx)  <br/> |Возвращает ссылку на объект [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , связанный с окном.  <br/> |Только тип **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Использование классов "WindowsCollection" и "Window"

Класс [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) доступен через свойство [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . При использовании класса [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) для доступа к формы windows, можно использовать индексатор (для Visual C#) или передать длинное целое свойство **Item** (в Visual Basic) возвращает ссылку на экземпляр объекта [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) . Например следующий пример кода задает ссылку на первый объект [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , содержащихся в [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) для текущего сеанса InfoPath. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Можно получить доступ к открытая в настоящий момент окно, непосредственно с использованием свойство [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) без прохода через [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) , как показано в следующей строке кода. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Объект [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) также может осуществляться с помощью свойство [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , который представляет текущего представления, которое используется для работы с XML-документом формы. Свойство [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) используется для доступа к [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) объект, представляющий текущее представление. Например следующий пример кода задает ссылку на [окно](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , связанное с текущим представлением. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Некоторые свойства и методы класса [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) — только для типа окна редактирования; Если разработка тип окна, они возвращают ошибку. В таблице ранее в этом разделе перечислены свойства и методы, поддерживаемые для каждого типа окна. Свойство [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) можно использовать в коде для определения, какой тип окна, с которыми выполняется. 
  

