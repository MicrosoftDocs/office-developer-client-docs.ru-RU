---
title: Работа с представлениями
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Класс View [infopath 2007] InfoPath 2007, работа с представлениями, служит для просмотра [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: При работе с шаблона формы InfoPath можно написать код для доступа к представлениям формы и выполните ряд действий на данные, которые содержат представления. InfoPath объектной модели, предоставляемые с Microsoft.Office.InfoPath пространство имен поддерживает доступ к представлений формы посредством использования членов класса View.
ms.openlocfilehash: 84c32244454e388e50433922c007d556fbef806a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807522"
---
# <a name="work-with-views"></a>Работа с представлениями

При работе с шаблона формы InfoPath можно написать код для доступа к представлениям формы и выполните ряд действий на данные, которые содержат представления. Объектная модель InfoPath, предоставленные поддерживает доступ пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) для представления формы посредством использования членов класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) . 
  
## <a name="overview-of-the-view-class"></a>Обзор класса View

Класс [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с представлением InfoPath. 
  
> [!NOTE]
> Методы и свойства класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) недоступны во время события [загрузки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) . 
  
|**Имя**|**Описание**|
|:-----|:-----|
|Метод [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Отключает автоматическую синхронизацию между базовым XML-документом формы и связанным представлением.  <br/> |
|Метод [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Включает автоматическую синхронизацию между базовым XML-документом формы и связанным представлением.  <br/> |
|Метод [ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Выполняет команду редактирования для базового XML-документа формы, основываясь на выбранных в данный момент данных в представлении.  <br/> |
|Метод [ExecuteAction (тип действия, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Выполняет команду редактирования для базового XML-документа формы, основываясь на указанном поле или группе.  <br/> |
|Метод [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Экспортирует представление в файл определенного формата.  <br/> |
|Метод [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Выполняет синхронизацию между базовым XML-документом формы и связанным представлением.  <br/> |
|Метод [GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам, начиная с указанного узла.  <br/> |
|Метод [GetContextNodes (XPathNavigator, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для выполнения итерации в возвращенных узлах XML в текущем выборе в элементе управления, привязанном к указанного поля или группы.  <br/> |
|Метод [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Возвращает ссылку на объект **XPathNodeIterator** для прохода по всем XML-узлам в текущем выборе элементов в представлении.  <br/> |
|Метод [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении, основываясь на указанном начальном XML-узле.   <br/> |
|Метод [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении, основываясь на указанных начальном и конечном XML-узлах.  <br/> |
|Метод [SelectNodes (XPathNavigator, XPathNavigator, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Выбирает диапазон узлов в представлении, основываясь на указанных начальном и конечном XML-узлах, а также на указанном элементе управления.   <br/> |
|Метод [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Выделяет текст, содержащийся в редактируемом элементе управления, привязанном к узлу, указанному объектом **XPathNavigator** , переданным в этот метод.  <br/> |
|Метод [SelectText (XPathNavigator, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Выделяет текст, содержащийся в редактируемом элементе управления, привязанном к узлу, указанному объектом **XPathNavigator** , переданным в этот метод и указанного элемента управления.  <br/> |
|Метод [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Создает сообщение электронной почты, содержащее текущее представление.  <br/> |
|Свойство [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)  <br/> |Возвращает ссылку на объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , связанный с представлением.  <br/> |
|Свойство [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)  <br/> |Возвращает ссылку на объект [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , связанный с представлением.  <br/> |
   
> [!NOTE]
> Объектная модель InfoPath также предоставляет классы [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) и [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , которые можно использовать для получения сведений обо всех представлениях, реализованных в форме. 
  
## <a name="using-the-view-class"></a>Использование класса View

Класс [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) доступен через свойство [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , к которому можно получить с помощью **этой** (C#) или ключевое слово **Me** (Visual Basic). Для доступа к имени представления, необходимо получить доступ к объекту [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , связанный с представлением. Следующий пример демонстрирует для отображения окна сообщения с именем активного представления. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Все шаблоны форм InfoPath содержит по крайней мере один представление по умолчанию; Тем не менее InfoPath поддерживает создание нескольких представлений формы XML-документом. При наличии нескольких представлений [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) можно использовать для работы со всех представлениях, реализованных в шаблоне формы. Для доступа к коллекции [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) шаблона формы, используйте свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Программными средствами можно изменить представление, в настоящее время active, используя метод [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , как показано в следующем примере кода. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

Для предыдущего примера для переключения представления будут работать только после открыта форма. Чтобы задать представление по умолчанию во время события [загрузки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , воспользуйтесь свойством [начальной](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) класса [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , как показано в следующем примере. Обратите внимание, что это значение только вступят в силу после сохранения и повторного открытия формы. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Выбор элементов управления в представлении

InfoPath предоставляет два метода класса [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , которые являются перегруженными, чтобы программно выбрать элемент управления в текущем представлении: методы [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) и [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . Метод [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) используется для данных элементов управления, например **Текстовое поле**, а метод **SelectNodes** для структурные элементы управления, такие как **Дополнительный раздел**. Чтобы выбрать определенный элемент управления в представлении, необходимо указать узел и, возможно, идентификатором ViewContext элемента управления. Идентификатор ViewContext необходим, когда у вас есть несколько элементов управления, привязанных на том же узле в источнике данных. InfoPath предоставляет сведения идентификатор ViewContext, при создании формы.
  
Идентификатор ViewContext элемента управления отображается на вкладке **Дополнительно** диалоговое окно "Свойства" для элемента управления, к которому можно получить, щелкнув правой кнопкой мыши элемент управления, нажав кнопку _ИмяЭлементаУправления_ **Свойства**и перейдите на вкладку **Дополнительно** . Идентификатор ViewContext элемента управления отображается в разделе **код** на вкладку **Дополнительно** . 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Когда используется SelectText и SelectNodes

Следующие элементы управления запись данных можно выбрать программными средствами с помощью метода [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) : 
  
- Текстовое поле
    
- Окно форматов RTF
    
- Выбор даты
    
Следующие структурные элементы управления можно выбрать программными средствами с помощью метода [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) : 
  
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
    
- Гиперссылка
    
- Поле выражения
    
- Вертикальная надпись
    
- Раздел ActiveX
    
- Горизонтальная область.
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>Использование методов SelectText и SelectNodes

В следующем примере перегрузка [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText** , предоставляющего один параметр _xmlNode_ , используется в **Текстовое поле** , связанное с «my: field1». 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Если у вас есть несколько элементов управления, привязанных к «my: field1», необходимо использовать перегруженный метод [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText** , который предоставляется параметр Дополнительные _viewContext_ для выбора конкретного элемента управления. В следующем примере предполагается, что существует два элемента управления **Текстового поля** , привязанных к «my: field1», с помощью первый элемент управления с Идентификатором ViewContext «CTRL1» и второй элемент управления с Идентификатором ViewContext «CTRL8». Второй элемент управления установлен. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

В следующем примере перегрузка [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) методу **SelectNodes** , который содержит только один параметр _Начальный_узел_ используется для выберите первую строку в повторяющейся таблицы, привязанных к повторяющейся группе «my: Сотрудник». 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Также можно выбрать несколько строк в повторяющейся таблицы. В следующем примере первые три строки повторяющейся таблицы, привязанных к повторяющейся группе «my: сотрудников» выбраны с помощью метода **SelectNodes** , который предоставляет перегрузки [SelectNodes (XPathNavigator, XPathNavigator, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  Параметры _Начальный_узел_ и _endNode_ : 
  
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


