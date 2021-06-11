---
title: Работа с представлениями
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- просмотр класса [infopath 2007], InfoPath 2007, работа с представлениями,представлениями [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении. Объектная модель InfoPath, предоставленная Корпорацией Майкрософт. Office. Пространство имен InfoPath поддерживает доступ к представлениям формы с помощью членов класса View.
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406299"
---
# <a name="work-with-views"></a>Работа с представлениями

При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении. Объектная модель InfoPath, предоставленная [Microsoft.Office. Пространство](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) имен InfoPath поддерживает доступ к представлениям формы с помощью членов класса [View.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) 
  
## <a name="overview-of-the-view-class"></a>Обзор класса View

Класс [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) предоставляет следующие методы и свойства, которые разработчики форм могут использовать для взаимодействия с представлением InfoPath. 
  
> [!NOTE]
> Методы и свойства класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) недоступны во время события [загрузки.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) 
  
|**Имя**|**Описание**|
|:-----|:-----|
|[Метод DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Отключает автоматическую синхронизацию между XML-документом формы и связанным представлением.  <br/> |
|[Метод EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Включает автоматическую синхронизацию между XML-документом формы и связанным представлением.  <br/> |
|[Метод ExecuteAction (ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Выполняет команду редактирования для связанного XML-документа формы на основе данных, выбранных в представлении.  <br/> |
|[Метод ExecuteAction (ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Выполняет команду редактирования для связанного XML-документа формы на основе указанного поля или группы.  <br/> |
|[Метод экспорта](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Экспортирует представление в файл указанного формата.  <br/> |
|[Метод ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Выполняет принудительную синхронизацию между XML-документом формы и связанным представлением.  <br/> |
|[Метод GetContextNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам, начиная с указанного узла.  <br/> |
|[Метод GetContextNodes (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам в текущей выборке в рамках элемента управления, связанного с указанным полем или группой.  <br/> |
|[Метод GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для прохода по всем XML-узлам в текущей выборке объектов в представлении.  <br/> |
|[Метод SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении на основе указанного начального узла XML.  <br/> |
|[Метод SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении на основе указанного начального и конечного узла XML.  <br/> |
|[Метод SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении на основе указанного начального, конечного узла XML и элемента управления.  <br/> |
|[Метод SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Выбирает текст, содержащийся в изменяемом элементе управления, связанном с узлом, который указан объектом **XPathNavigator**, переданным в этот метод.  <br/> |
|[Метод SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Выбирает текст, содержащийся в изменяемом элементе управления, связанном с узлом, который указан объектом **XPathNavigator**, переданным в этот метод, а также с указанным элементом управления.  <br/> |
|[Метод ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Создает сообщение электронной почты, содержащее текущее представление.  <br/> |
|[Свойство ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)  <br/> |Получает ссылку на [объект ViewInfo,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) связанный с представлением.  <br/> |
|[Свойство Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)  <br/> |Получает ссылку на [объект Window,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) связанный с представлением.  <br/> |
   
> [!NOTE]
> Объектная модель InfoPath также предоставляет классы [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) и [ViewInfo,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) которые можно использовать для получения сведений обо всех представлениях, реализованных в форме. 
  
## <a name="using-the-view-class"></a>Использование класса View

Класс [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) можно получить через свойство [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) класса [XmlForm,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) к которому можно получить доступ с помощью этого **ключевого** слова (C#) или Me **(Visual Basic).** Чтобы получить доступ к имени представления, необходимо получить доступ к [объекту ViewInfo,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) связанному с представлением. В следующем примере демонстрируется отображение окна сообщения с именем активного в данный момент представления. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Все шаблоны форм InfoPath содержат по крайней мере одно представление по умолчанию; Однако InfoPath также поддерживает создание нескольких представлений документа XML формы. При нескольких представлениях [viewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) можно использовать для работы со всеми представлениями, реализованными в шаблоне формы. Чтобы получить доступ [к ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) шаблона формы, используйте свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Вы можете программным образом изменить представление, которое в настоящее время активно с помощью метода [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) [viewInfoCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) как показано в следующем примере кода. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

Предыдущий пример по переключению представления будет работать только после открытия формы. Чтобы установить представление по умолчанию во время [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) события [загрузки,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) используйте начальное свойство [класса ViewInfoCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) как показано в следующем примере. Однако обратите внимание, что это значение применяется только после сохранения и повторного открытия формы. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Выбор элементов управления в представлении

InfoPath предоставляет два метода класса [View,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) оба из которых перегружены, для программного выбора управления в текущем представлении: методы [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) и [SelectNodes().](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) Метод [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) используется для элементов управления входом данных, таких как текстовое **поле,** в то время как метод **SelectNodes** используется для структурных элементов управления, таких как необязательный **раздел**. Для выбора конкретного элемента управления в представлении необходимо предоставить узел и, при желании, идентификатор ViewContext элемента управления. Идентификатор ViewContext необходим, если к одному узлу в источнике данных привязано несколько элементов управления. InfoPath предоставляет сведения об идентификаторе ViewContext при создании формы.
  
ID ViewContext управления отображается на вкладке Расширенный диалоговое окно свойств управления, к которому можно получить доступ правой кнопкой мыши управления, щелкнув свойства _ControlName,_ а затем щелкнув вкладку **Advanced.**  Код ViewContext управления указан в разделе **Код** вкладки **Advanced.** 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Когда используется SelectText и SelectNodes

Вы можете программным образом выбрать следующие элементы управления записью данных с помощью метода [SelectText (XPathNavigator):](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) 
  
- Текстовое поле
    
- Окно форматов RTF
    
- Выбор даты
    
Программным образом можно выбрать следующие структурные элементы управления с помощью метода [SelectNodes (XPathNavigator):](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) 
  
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

В следующем примере для выбора текстового окна, связанного с "my:field1", используется перегрузка **метода SelectText**  [(XPathNavigator),](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) который предоставляет один параметр _xmlNode._ 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Если у вас есть несколько элементов управления, связанных с "my:field1", необходимо использовать перегрузку [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText,** который предоставляет дополнительный параметр  _viewContext_ для выбора определенного управления. В следующем примере предполагается, что к "my:field1" привязано два элемента управления **Текстовое поле**, при этом идентификатор ViewContext первого элемента управления — "CTRL1", а второго — "CTRL8". Выбран второй элемент управления. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

В следующем примере для выбора первой строки в повторяемой таблице, связанной с повторяючей группой "my:employee", используется перегрузка метода [SelectNodes (XPathNavigator) метода SelectNodes( XPathNavigator),](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) который обеспечивает только один параметр _startNode._  
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

В повторяющейся таблице также можно выбирать и несколько строк. В следующем примере первые три строки таблицы повторения, связанной с повторяючей группой "my:employee", выбираются с помощью параметров [SelectNodes (XPathNavigator, XPathNavigator, String),](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) которые предоставляют параметры _startNode_ и _endNode:_  
  
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


