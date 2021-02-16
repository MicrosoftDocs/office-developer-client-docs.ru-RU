---
title: Работа с представлениями
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- класс view [infopath 2007],InfoPath 2007, работа с представлениями,представления [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении. Объектная модель InfoPath, предоставляемая пространством имен Microsoft.Office.InfoPath, поддерживает доступ к представлениям формы с помощью членов класса View.
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406299"
---
# <a name="work-with-views"></a><span data-ttu-id="1c99f-105">Работа с представлениями</span><span class="sxs-lookup"><span data-stu-id="1c99f-105">Work with Views</span></span>

<span data-ttu-id="1c99f-106">При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении.</span><span class="sxs-lookup"><span data-stu-id="1c99f-106">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain.</span></span> <span data-ttu-id="1c99f-107">Объектная модель InfoPath, предоставляемая пространством имен [Microsoft.Office.InfoPath,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) поддерживает доступ к представлениям формы с помощью членов класса [View.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="1c99f-108">Обзор класса View</span><span class="sxs-lookup"><span data-stu-id="1c99f-108">Overview of the View Class</span></span>

<span data-ttu-id="1c99f-109">Класс [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) предоставляет следующие методы и свойства, которые разработчики форм могут использовать для взаимодействия с представлением InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1c99f-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1c99f-110">Методы и свойства класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) недоступны во время события [Loading.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="1c99f-111">**Название**</span><span class="sxs-lookup"><span data-stu-id="1c99f-111">**Name**</span></span>|<span data-ttu-id="1c99f-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c99f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c99f-113">[Метод DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-114">Отключает автоматическую синхронизацию между XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="1c99f-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="1c99f-115">[Метод EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-116">Включает автоматическую синхронизацию между XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="1c99f-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="1c99f-117">[Метод ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-118">Выполняет команду редактирования для связанного XML-документа формы на основе данных, выбранных в представлении.</span><span class="sxs-lookup"><span data-stu-id="1c99f-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="1c99f-119">[Метод ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-120">Выполняет команду редактирования для связанного XML-документа формы на основе указанного поля или группы.</span><span class="sxs-lookup"><span data-stu-id="1c99f-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="1c99f-121">[Метод Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-122">Экспортирует представление в файл указанного формата.</span><span class="sxs-lookup"><span data-stu-id="1c99f-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="1c99f-123">[Метод ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-124">Выполняет принудительную синхронизацию между XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="1c99f-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="1c99f-125">[Метод GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-126">Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам, начиная с указанного узла.</span><span class="sxs-lookup"><span data-stu-id="1c99f-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="1c99f-127">[Метод GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-128">Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам в текущей выборке в рамках элемента управления, связанного с указанным полем или группой.</span><span class="sxs-lookup"><span data-stu-id="1c99f-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="1c99f-129">[Метод GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-130">Возвращает ссылку на объект **XPathNodeIterator** для прохода по всем XML-узлам в текущей выборке объектов в представлении.</span><span class="sxs-lookup"><span data-stu-id="1c99f-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="1c99f-131">[Метод SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-132">Выбирает диапазон узлов в представлении на основе указанного начального узла XML.</span><span class="sxs-lookup"><span data-stu-id="1c99f-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="1c99f-133">[Метод SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-134">Выбирает диапазон узлов в представлении на основе указанного начального и конечного узла XML.</span><span class="sxs-lookup"><span data-stu-id="1c99f-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="1c99f-135">[Метод SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-136">Выбирает диапазон узлов в представлении на основе указанного начального, конечного узла XML и элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1c99f-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="1c99f-137">[Метод SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-138">Выбирает текст, содержащийся в изменяемом элементе управления, связанном с узлом, который указан объектом **XPathNavigator**, переданным в этот метод.</span><span class="sxs-lookup"><span data-stu-id="1c99f-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="1c99f-139">[Метод SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-140">Выбирает текст, содержащийся в изменяемом элементе управления, связанном с узлом, который указан объектом **XPathNavigator**, переданным в этот метод, а также с указанным элементом управления.</span><span class="sxs-lookup"><span data-stu-id="1c99f-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="1c99f-141">[Метод ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="1c99f-142">Создает сообщение электронной почты, содержащее текущее представление.</span><span class="sxs-lookup"><span data-stu-id="1c99f-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="1c99f-143">[Свойство ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="1c99f-144">Возвращает ссылку на объект [ViewInfo,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) связанный с представлением.</span><span class="sxs-lookup"><span data-stu-id="1c99f-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="1c99f-145">[Свойство Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="1c99f-146">Получает ссылку на объект [Window,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) связанный с представлением.</span><span class="sxs-lookup"><span data-stu-id="1c99f-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="1c99f-147">Объектная модель InfoPath также предоставляет классы [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) и [ViewInfo,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) которые можно использовать для получения сведений обо всех представлениях, реализованных в форме.</span><span class="sxs-lookup"><span data-stu-id="1c99f-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="1c99f-148">Использование класса View</span><span class="sxs-lookup"><span data-stu-id="1c99f-148">Using the View Class</span></span>

<span data-ttu-id="1c99f-149">Доступ [к](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) классу View можно получить с помощью свойства [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) класса [XmlForm,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) доступ к которому можно получить с помощью этого **ключевого** слова (C#) или **Me** (Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="1c99f-149">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="1c99f-150">Чтобы получить доступ к имени представления, необходимо получить доступ к [объекту ViewInfo,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) связанному с представлением.</span><span class="sxs-lookup"><span data-stu-id="1c99f-150">To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span> <span data-ttu-id="1c99f-151">В следующем примере демонстрируется отображение окна сообщения с именем активного в данный момент представления.</span><span class="sxs-lookup"><span data-stu-id="1c99f-151">The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="1c99f-152">Все шаблоны форм InfoPath содержат по крайней мере одно представление по умолчанию; Однако InfoPath также поддерживает создание нескольких представлений XML-документа формы.</span><span class="sxs-lookup"><span data-stu-id="1c99f-152">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document.</span></span> <span data-ttu-id="1c99f-153">При работе с несколькими представлениями можно использовать [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) для работы со всеми представлениями, реализованными в шаблоне формы.</span><span class="sxs-lookup"><span data-stu-id="1c99f-153">When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template.</span></span> <span data-ttu-id="1c99f-154">Чтобы получить доступ [к ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) шаблона формы, используйте свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) класса [XmlForm.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-154">To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="1c99f-155">Вы можете программным способом изменить активное представление с помощью метода [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) [viewInfoCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="1c99f-155">You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="1c99f-156">Предыдущий пример по переключению представления будет работать только после открытия формы.</span><span class="sxs-lookup"><span data-stu-id="1c99f-156">The previous example for switching a view will work only after the form is opened.</span></span> <span data-ttu-id="1c99f-157">Чтобы установить представление по умолчанию во время события [Loading,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) используйте свойство [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) класса [ViewInfoCollection,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="1c99f-157">To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example.</span></span> <span data-ttu-id="1c99f-158">Однако обратите внимание, что это значение применяется только после сохранения и повторного открытия формы.</span><span class="sxs-lookup"><span data-stu-id="1c99f-158">Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="1c99f-159">Выбор элементов управления в представлении</span><span class="sxs-lookup"><span data-stu-id="1c99f-159">Selecting Controls in a View</span></span>

<span data-ttu-id="1c99f-160">InfoPath предоставляет два метода класса [View,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) оба из которых перегружены, для программного выбора управления в текущем представлении: методы [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) и [SelectNodes().](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c99f-160">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods.</span></span> <span data-ttu-id="1c99f-161">Метод [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) используется для элементов управления записью данных, таких как текстовое **поле,** а метод **SelectNodes** используется для структурных элементов управления, таких как необязательный **раздел.**</span><span class="sxs-lookup"><span data-stu-id="1c99f-161">The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**.</span></span> <span data-ttu-id="1c99f-162">Для выбора конкретного элемента управления в представлении необходимо предоставить узел и, при желании, идентификатор ViewContext элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1c99f-162">To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID.</span></span> <span data-ttu-id="1c99f-163">Идентификатор ViewContext необходим, если к одному узлу в источнике данных привязано несколько элементов управления.</span><span class="sxs-lookup"><span data-stu-id="1c99f-163">The ViewContext ID is needed when you have multiple controls bound to the same node in the data source.</span></span> <span data-ttu-id="1c99f-164">InfoPath предоставляет сведения об идентификаторе ViewContext при создании формы.</span><span class="sxs-lookup"><span data-stu-id="1c99f-164">InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="1c99f-165">Код ViewContext для управления отображается на  вкладке "Дополнительные" в диалоговом окне свойств этого управления, к которому можно получить доступ, щелкнув  правой кнопкой мыши, щелкнув "Свойства _ControlName"_ и щелкнув вкладку "Дополнительные". Код ViewContext для этого управления указан в разделе **"Код"** на вкладке **"Дополнительные".**</span><span class="sxs-lookup"><span data-stu-id="1c99f-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="1c99f-166">Когда используется SelectText и SelectNodes</span><span class="sxs-lookup"><span data-stu-id="1c99f-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="1c99f-167">С помощью метода [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) можно программным способом выбрать следующие элементы управления записью данных:</span><span class="sxs-lookup"><span data-stu-id="1c99f-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="1c99f-168">Текстовое поле</span><span class="sxs-lookup"><span data-stu-id="1c99f-168">Text Box</span></span>
    
- <span data-ttu-id="1c99f-169">Окно форматов RTF</span><span class="sxs-lookup"><span data-stu-id="1c99f-169">Rich Text Box</span></span>
    
- <span data-ttu-id="1c99f-170">Выбор даты</span><span class="sxs-lookup"><span data-stu-id="1c99f-170">Date Picker</span></span>
    
<span data-ttu-id="1c99f-171">С помощью метода [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) можно программным способом выбрать следующие структурные элементы управления:</span><span class="sxs-lookup"><span data-stu-id="1c99f-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="1c99f-172">Дополнительный раздел</span><span class="sxs-lookup"><span data-stu-id="1c99f-172">Optional Section</span></span>
    
- <span data-ttu-id="1c99f-173">Раздел выбора</span><span class="sxs-lookup"><span data-stu-id="1c99f-173">Choice Section</span></span>
    
- <span data-ttu-id="1c99f-174">Повторяющийся раздел (элементы)</span><span class="sxs-lookup"><span data-stu-id="1c99f-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="1c99f-175">Повторяющаяся таблица (строки)</span><span class="sxs-lookup"><span data-stu-id="1c99f-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="1c99f-176">Повторяющийся рекурсивный раздел (элементы)</span><span class="sxs-lookup"><span data-stu-id="1c99f-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="1c99f-177">Маркированный, нумерованный или простой список</span><span class="sxs-lookup"><span data-stu-id="1c99f-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="1c99f-178">Горизонтальная повторяющаяся таблица</span><span class="sxs-lookup"><span data-stu-id="1c99f-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="1c99f-179">Нельзя выбрать или переместить фокус программными средствами на следующие элементы управления:</span><span class="sxs-lookup"><span data-stu-id="1c99f-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="1c99f-180">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="1c99f-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="1c99f-181">Список</span><span class="sxs-lookup"><span data-stu-id="1c99f-181">List Box</span></span>
    
- <span data-ttu-id="1c99f-182">Флажок</span><span class="sxs-lookup"><span data-stu-id="1c99f-182">Check Box</span></span>
    
- <span data-ttu-id="1c99f-183">Переключатель</span><span class="sxs-lookup"><span data-stu-id="1c99f-183">Option Button</span></span>
    
- <span data-ttu-id="1c99f-184">Кнопка</span><span class="sxs-lookup"><span data-stu-id="1c99f-184">Button</span></span>
    
- <span data-ttu-id="1c99f-185">Изображение (связанное или включенное)</span><span class="sxs-lookup"><span data-stu-id="1c99f-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="1c99f-186">Рисунок от руки</span><span class="sxs-lookup"><span data-stu-id="1c99f-186">Ink Picture</span></span>
    
- <span data-ttu-id="1c99f-187">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="1c99f-187">Hyperlink</span></span>
    
- <span data-ttu-id="1c99f-188">Поле выражения</span><span class="sxs-lookup"><span data-stu-id="1c99f-188">Expression Box</span></span>
    
- <span data-ttu-id="1c99f-189">Вертикальная надпись</span><span class="sxs-lookup"><span data-stu-id="1c99f-189">Vertical Label</span></span>
    
- <span data-ttu-id="1c99f-190">Раздел ActiveX</span><span class="sxs-lookup"><span data-stu-id="1c99f-190">ActiveX Section</span></span>
    
- <span data-ttu-id="1c99f-191">Горизонтальная область.</span><span class="sxs-lookup"><span data-stu-id="1c99f-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="1c99f-192">Использование методов SelectText и SelectNodes</span><span class="sxs-lookup"><span data-stu-id="1c99f-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="1c99f-193">В следующем примере перегрузка [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText,** который предоставляет один параметр _xmlNode,_ используется для выбора текстового поля, привязанного к "my:field1". </span><span class="sxs-lookup"><span data-stu-id="1c99f-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="1c99f-194">Если к "my:field1" привязано несколько элементов управления, необходимо использовать перегрузку [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText,** который предоставляет дополнительный  _параметр viewContext_ для выбора определенного управления.</span><span class="sxs-lookup"><span data-stu-id="1c99f-194">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control.</span></span> <span data-ttu-id="1c99f-195">В следующем примере предполагается, что к "my:field1" привязано два элемента управления **Текстовое поле**, при этом идентификатор ViewContext первого элемента управления — "CTRL1", а второго — "CTRL8".</span><span class="sxs-lookup"><span data-stu-id="1c99f-195">The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8".</span></span> <span data-ttu-id="1c99f-196">Выбран второй элемент управления.</span><span class="sxs-lookup"><span data-stu-id="1c99f-196">The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="1c99f-197">В следующем примере перегрузка [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) метода **SelectNodes,** который предоставляет только один параметр  _startNode,_ используется для выбора первой строки повторяющегося таблицы, привязанного к повторяющегося группе "my:employee".</span><span class="sxs-lookup"><span data-stu-id="1c99f-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="1c99f-198">В повторяющейся таблице также можно выбирать и несколько строк.</span><span class="sxs-lookup"><span data-stu-id="1c99f-198">You can also select multiple rows in a repeating table.</span></span> <span data-ttu-id="1c99f-199">В следующем примере первые три строки повторяющегося таблицы, привязанные к повторяющегося группе "my:employee", выбираются с помощью перегрузки [метода SelectNodes(XPathNavigator, XPathNavigator, String),](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) которая предоставляет _параметры startNode_ и _endNode:_ </span><span class="sxs-lookup"><span data-stu-id="1c99f-199">In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
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


