---
title: Работа с form Windows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007],form windows [InfoPath 2007], Window class [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: При работе с формой InfoPath программным образом можно написать код для доступа к окнам формы, а затем настроить некоторые содержащиеся в них элементы. Объектная модель InfoPath, предоставленная Корпорацией Майкрософт. Office. Пространство имен InfoPath поддерживает доступ к окнам формы с помощью класса Window в связи с классом WindowCollection.
ms.openlocfilehash: 018357519e27629c29b2611bd0a88b8d64f0a1eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431066"
---
# <a name="work-with-form-windows"></a>Работа с form Windows

При работе с формой InfoPath программным образом можно написать код для доступа к окнам формы, а затем настроить некоторые содержащиеся в них элементы. Объектная модель InfoPath, предоставленная [Microsoft.Office. Пространство](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) имен InfoPath поддерживает доступ к окнам формы с помощью класса [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) в связи с [классом WindowCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) 
  
> [!NOTE]
> Классы для работы с окном формы доступны только при работе с **Формой редактора InfoPath**. Если параметр **Совместимость** шаблона формы имеет значение **Форма веб-браузера**, эти классы не будут доступны. 
  
В InfoPath существует два типа окон: 
  
- окно редактирования, которое используется при заполнении формы пользователем;
    
- окно разработки, которое используется при разработке пользователем шаблона формы.
    
При написании кода в шаблоне формы именно окно редактирования предоставляет наиболее полезные функции, так как вы можете использовать объект [Window,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) представляюющий текущее окно, чтобы получить доступ к различным свойствам и методам, которые можно использовать для настройки процесса редактирования формы. 
  
## <a name="overview-of-the-windowscollection-class"></a>Обзор класса "WindowsCollection"

Класс [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) предоставляет следующие свойства, которые разработчики шаблонов форм могут использовать для управления объектами [Window,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) которые в нем содержатся. 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Свойство [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)  <br/> |Получает количество объектов [Window,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) содержащихся в коллекции.  <br/> |
|Свойство [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)  <br/> |Получает ссылку на указанный [объект Window.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx)  <br/> |
   
## <a name="overview-of-the-window-class"></a>Обзор класса "Window"

Класс [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) предоставляет следующие методы и свойства, которые разработчики форм могут использовать для взаимодействия с окном InfoPath. Поддержка этих методов и свойств отличается в зависимости от типа окна [(WindowType),](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) с помощью которых вы работаете. Некоторые методы и свойства работают только с окном редактора (**WindowType.Editor**). Остальные методы и свойства работают как с окном редактора, так и с окном конструктора (**WindowType.Designer**). Кроме того, как и для всех членов объектной модели InfoPath, при вызове из шаблона формы поддержка методов и свойств может изменяться в зависимости от уровня безопасности и метода развертывания формы.
  
|**Имя**|**Описание**|**Поддержка типов окон**|
|:-----|:-----|:-----|
|[Активировать](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx) метод  <br/> |Активирует окно (переключает фокус).  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) property  <br/> |Возвращает логическое (**Boolean**) значение, указывающее, является ли окно активным в данный момент.  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Свойство caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Получает или задает текст подписи для окна, представленного объектом [Window.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx)  <br/> |Только тип **Editor**  <br/> |
|[Метод Close()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Закрывает окно с запросом на сохранение изменений для любой несохраненной формы или формы, изменения которой не были сохранены.  <br/> |Только тип **Editor**  <br/> |
|[Метод Close (Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Закрывает окно и позволяет при необходимости принудительно закрыть без сохранения несохраненную форму или форму с несохраненными изменениями.  <br/> |Только тип **Editor**  <br/> |
|[Свойство CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx)  <br/> |Возвращает ссылку на коллекцию Microsoft Office **CommandBars**, связанную с окном.  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Свойство Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx)  <br/> |Возвращает или задает высоту окна, измеряемую в точках.  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Свойство Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Возвращает или задает горизонтальную позицию окна, измеряемую в точках.  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Свойство MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Получает ссылку на [класс MailEnvelope.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx)  <br/> |Только тип **Editor**  <br/> |
|[Свойство TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx)  <br/> |Получает ссылку на [коллекцию TaskPaneCollection.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx)  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Верхнее](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx) свойство  <br/> |Возвращает или задает вертикальную позицию окна, измеряемую в точках.  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Свойство Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Возвращает или задает ширину окна, измеряемую в точках.  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Свойство WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx)  <br/> |Получает или задает состояние окна как [значение WindowState.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx)  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Свойство WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx)  <br/> |Получает тип окна в виде значения переумерия [WindowType.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx)  <br/> |Типы **Designer** и **Editor**  <br/> |
|[Свойство XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx)  <br/> |Возвращает ссылку на [объект XmlForm,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) связанный с окном.  <br/> |Только тип **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Использование классов "WindowsCollection" и "Window"

К [классу WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) можно получить доступ Windows [свойства](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) класса [Приложения.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) При использовании класса [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) для доступа к окнам формы используется индексатор (для Visual C#) или длинный вход в свойство **Item** (для Visual Basic) для возврата ссылки на экземпляр объекта [Window.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) Например, следующий код задает ссылку на первый объект [Window,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) содержащийся в [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) для текущего сеанса InfoPath. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Вы можете получить доступ к открытому окну [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) в настоящее время непосредственно с помощью свойства [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) класса Application, не проехав [windowCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) как показано в следующей строке кода. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

К [объекту Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) также можно получить доступ с помощью свойства [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) класса [View,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) которое представляет текущее представление, используемое для работы с документом XML формы. Свойство [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) используется для доступа к объекту [View,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) представляюму текущее представление. Например, следующий код задает ссылку на [окно,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) связанное с текущим представлением. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Некоторые свойства и методы класса [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) используются только для типа окна редактирования; если используется с типом окна разработки, они возвращают ошибку. Какие свойства и методы поддерживаются для каждого типа окна, перечислены в таблице ранее в этом разделе. Свойство [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) в коде можно использовать для определения типа окна, с которым вы работаете. 
  

