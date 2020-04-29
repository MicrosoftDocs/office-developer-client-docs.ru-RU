---
title: Работать с представлениями
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Класс View [InfoPath 2007], InfoPath 2007, работа с представлениями, представления [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении. Объектная модель InfoPath, предоставляемая пространством имен Microsoft. Office. InfoPath, поддерживает доступ к представлениям формы с помощью членов класса View.
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406299"
---
# <a name="work-with-views"></a>Работать с представлениями

При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении. Объектная модель InfoPath, предоставляемая пространством имен [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , поддерживает доступ к представлениям формы с помощью членов класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) . 
  
## <a name="overview-of-the-view-class"></a>Обзор класса View

Класс [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с представлением InfoPath. 
  
> [!NOTE]
> Методы и свойства класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) недоступны во время события [загрузки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
|**Название**|**Описание**|
|:-----|:-----|
|Метод [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Отключает автоматическую синхронизацию между XML-документом формы и связанным представлением.  <br/> |
|Метод [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Включает автоматическую синхронизацию между XML-документом формы и связанным представлением.  <br/> |
|Метод [ExecuteAction (метод)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Выполняет команду редактирования для связанного XML-документа формы на основе данных, выбранных в представлении.  <br/> |
|Метод [ExecuteAction (себя, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Выполняет команду редактирования для связанного XML-документа формы на основе указанного поля или группы.  <br/> |
|Метод [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Экспортирует представление в файл указанного формата.  <br/> |
|Метод [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Выполняет принудительную синхронизацию между XML-документом формы и связанным представлением.  <br/> |
|Метод [GetContextNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам, начиная с указанного узла.  <br/> |
|Метод [GetContextNodes (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам в текущей выборке в рамках элемента управления, связанного с указанным полем или группой.  <br/> |
|Метод [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для прохода по всем XML-узлам в текущей выборке объектов в представлении.  <br/> |
|Метод [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении на основе указанного начального узла XML.  <br/> |
|Метод [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении на основе указанного начального и конечного узла XML.  <br/> |
|Метод [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении на основе указанного начального, конечного узла XML и элемента управления.  <br/> |
|Метод [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Выбирает текст, содержащийся в изменяемом элементе управления, связанном с узлом, который указан объектом **XPathNavigator**, переданным в этот метод.  <br/> |
|[SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метод  <br/> |Выбирает текст, содержащийся в изменяемом элементе управления, связанном с узлом, который указан объектом **XPathNavigator**, переданным в этот метод, а также с указанным элементом управления.  <br/> |
|Метод [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Создает сообщение электронной почты, содержащее текущее представление.  <br/> |
|Свойство [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)  <br/> |Возвращает ссылку на объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , связанный с представлением.  <br/> |
|Свойство [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)  <br/> |Возвращает ссылку на объект [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , связанный с представлением.  <br/> |
   
> [!NOTE]
> Объектная модель InfoPath также предоставляет классы [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) и [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , которые можно использовать для получения сведений обо всех представлениях, реализованных в форме. 
  
## <a name="using-the-view-class"></a>Использование класса View

Доступ к классу [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) осуществляется с помощью свойства [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , доступ к которому осуществляется с помощью ключевого слова **this** (C#) или **Me** (Visual Basic). Чтобы получить доступ к имени представления, необходимо получить доступ к объекту [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , связанному с представлением. В следующем примере демонстрируется отображение окна сообщения с именем активного в данный момент представления. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Все шаблоны форм InfoPath содержат по крайней мере одно представление по умолчанию; Однако InfoPath также поддерживает создание нескольких представлений базового XML-документа формы. При наличии нескольких представлений [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) можно использовать для работы со всеми представлениями, реализованными в шаблоне формы. Чтобы получить доступ к [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) шаблона формы, используйте свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Можно программно изменить текущее активное представление с помощью метода [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) объекта [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , как показано в следующем примере кода. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

Предыдущий пример по переключению представления будет работать только после открытия формы. Чтобы задать представление по умолчанию во время события [Load](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , используйте свойство [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) класса [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , как показано в следующем примере. Однако обратите внимание, что это значение применяется только после сохранения и повторного открытия формы. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Выбор элементов управления в представлении

InfoPath предоставляет два метода класса [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , которые перегружаются для программного выбора элемента управления в текущем представлении: методы [SelectText ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) и [SelectNodes ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . Метод [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) используется для элементов управления вводом данных, например **текстового поля**, а метод **SelectNodes** используется для структурных элементов управления, таких как **необязательный раздел**. Для выбора конкретного элемента управления в представлении необходимо предоставить узел и, при желании, идентификатор ViewContext элемента управления. Идентификатор ViewContext необходим, если к одному узлу в источнике данных привязано несколько элементов управления. InfoPath предоставляет сведения об идентификаторе ViewContext при создании формы.
  
Идентификатор ViewContext элемента управления отображается на вкладке **Дополнительно** диалогового окна Свойства элемента управления, к которому можно получить доступ, щелкнув элемент управления правой кнопкой мыши, выбрав _контролнаме_ **Свойства**и выбрав вкладку **Дополнительно** . Идентификатор ViewContext элемента управления указан в разделе **код** вкладки **Дополнительно** . 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Когда используется SelectText и SelectNodes

Вы можете программным способом выбрать следующие элементы управления вводом данных с помощью метода [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) : 
  
- Текстовое поле
    
- Окно форматов RTF
    
- Выбор даты
    
С помощью метода [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) можно программно выбрать следующие структурные элементы управления: 
  
- Дополнительный раздел
    
- Раздел выбора
    
- Повторяющийся раздел (элементы)
    
- Повторяющаяся таблица (строки)
    
- Повторяющийся рекурсивный раздел (элементы)
    
- Маркированный, нумерованный или простой список
    
- Горизонтальная повторяющаяся таблица
    
Нельзя выбрать или переместить фокус программными средствами на следующие элементы управления:
  
- Раскрывающийся список
    
- Список
    
- Флажок
    
- Переключатель
    
- Кнопка
    
- Изображение (связанное или включенное)
    
- Рисунок от руки
    
- Hyperlink
    
- Поле выражения
    
- Вертикальная надпись
    
- Раздел ActiveX
    
- Горизонтальная область.
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>Использование методов SelectText и SelectNodes

В следующем примере перегрузка [(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText** , который предоставляет один параметр _XmlNode_ , используется для выбора **текстового поля** , которое привязано к "My: поле1". 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

При наличии нескольких элементов управления, привязанных к "My: Field1", необходимо использовать перегрузку метода SelectText [(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText** , который предоставляет дополнительный параметр _ViewContext_ для выбора определенного элемента управления. В следующем примере предполагается, что к "my:field1" привязано два элемента управления **Текстовое поле**, при этом идентификатор ViewContext первого элемента управления — "CTRL1", а второго — "CTRL8". Выбран второй элемент управления. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

В следующем примере перегрузка [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) метода **SelectNodes** , который предоставляет только один параметр _StartNode_ , используется для выбора первой строки в повторяющейся таблице, привязанной к повторяющейся группе "My: Employee". 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

В повторяющейся таблице также можно выбирать и несколько строк. В следующем примере первые три строки повторяющейся таблицы, привязанные к повторяющейся группе "My: Employee", выбираются с помощью перегрузки метода SelectNodes [(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) метода **SelectNodes** , предоставляющего параметры _StartNode_ и _ендноде_ : 
  
```cs
// Create XPathNavigators to specify range of nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
XPathNavigator repeatingTableRow3 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:myemployee[3]", NamespaceManager);
// Select range of nodes in specified XPathNavigators.
CurrentView.SelectNodes(repeatingTableRow1, repeatingTableRow3);
```


