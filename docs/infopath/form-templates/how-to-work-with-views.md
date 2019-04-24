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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303544"
---
# <a name="work-with-views"></a><span data-ttu-id="b25c0-105">Работать с представлениями</span><span class="sxs-lookup"><span data-stu-id="b25c0-105">Work with Views</span></span>

<span data-ttu-id="b25c0-106">При работе с шаблоном формы InfoPath можно написать код для доступа к представлениям формы, а затем выполнить различные действия с данными, содержащимися в представлении.</span><span class="sxs-lookup"><span data-stu-id="b25c0-106">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain.</span></span> <span data-ttu-id="b25c0-107">Объектная модель InfoPath, предоставляемая пространством имен [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , поддерживает доступ к представлениям формы с помощью членов класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b25c0-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="b25c0-108">Обзор класса View</span><span class="sxs-lookup"><span data-stu-id="b25c0-108">Overview of the View Class</span></span>

<span data-ttu-id="b25c0-109">Класс [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с представлением InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b25c0-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b25c0-110">Методы и свойства класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) недоступны во время события [загрузки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b25c0-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="b25c0-111">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b25c0-111">**Name**</span></span>|<span data-ttu-id="b25c0-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b25c0-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b25c0-113">Метод [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-114">Отключает автоматическую синхронизацию между XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="b25c0-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="b25c0-115">Метод [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-116">Включает автоматическую синхронизацию между XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="b25c0-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="b25c0-117">Метод [ExecuteAction (метод)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-118">Выполняет команду редактирования для связанного XML-документа формы на основе данных, выбранных в представлении.</span><span class="sxs-lookup"><span data-stu-id="b25c0-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="b25c0-119">Метод [ExecuteAction (себя, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-120">Выполняет команду редактирования для связанного XML-документа формы на основе указанного поля или группы.</span><span class="sxs-lookup"><span data-stu-id="b25c0-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="b25c0-121">Метод [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-122">Экспортирует представление в файл указанного формата.</span><span class="sxs-lookup"><span data-stu-id="b25c0-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="b25c0-123">Метод [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-124">Выполняет принудительную синхронизацию между XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="b25c0-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="b25c0-125">Метод [GetContextNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-126">Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам, начиная с указанного узла.</span><span class="sxs-lookup"><span data-stu-id="b25c0-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="b25c0-127">Метод [GetContextNodes (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-128">Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам в текущей выборке в рамках элемента управления, связанного с указанным полем или группой.</span><span class="sxs-lookup"><span data-stu-id="b25c0-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="b25c0-129">Метод [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-130">Возвращает ссылку на объект **XPathNodeIterator** для прохода по всем XML-узлам в текущей выборке объектов в представлении.</span><span class="sxs-lookup"><span data-stu-id="b25c0-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="b25c0-131">Метод [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-132">Выбирает диапазон узлов в представлении на основе указанного начального узла XML.</span><span class="sxs-lookup"><span data-stu-id="b25c0-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="b25c0-133">Метод [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-134">Выбирает диапазон узлов в представлении на основе указанного начального и конечного узла XML.</span><span class="sxs-lookup"><span data-stu-id="b25c0-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="b25c0-135">Метод [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-136">Выбирает диапазон узлов в представлении на основе указанного начального, конечного узла XML и элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b25c0-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="b25c0-137">Метод [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-138">Выбирает текст, содержащийся в изменяемом элементе управления, связанном с узлом, который указан объектом **XPathNavigator**, переданным в этот метод.</span><span class="sxs-lookup"><span data-stu-id="b25c0-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="b25c0-139">[SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метод</span><span class="sxs-lookup"><span data-stu-id="b25c0-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-140">Выбирает текст, содержащийся в изменяемом элементе управления, связанном с узлом, который указан объектом **XPathNavigator**, переданным в этот метод, а также с указанным элементом управления.</span><span class="sxs-lookup"><span data-stu-id="b25c0-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="b25c0-141">Метод [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="b25c0-142">Создает сообщение электронной почты, содержащее текущее представление.</span><span class="sxs-lookup"><span data-stu-id="b25c0-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="b25c0-143">Свойство [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="b25c0-144">Возвращает ссылку на объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , связанный с представлением.</span><span class="sxs-lookup"><span data-stu-id="b25c0-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="b25c0-145">Свойство [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)</span><span class="sxs-lookup"><span data-stu-id="b25c0-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="b25c0-146">Возвращает ссылку на объект [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , связанный с представлением.</span><span class="sxs-lookup"><span data-stu-id="b25c0-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b25c0-147">Объектная модель InfoPath также предоставляет классы [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) и [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , которые можно использовать для получения сведений обо всех представлениях, реализованных в форме.</span><span class="sxs-lookup"><span data-stu-id="b25c0-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="b25c0-148">Использование класса View</span><span class="sxs-lookup"><span data-stu-id="b25c0-148">Using the View Class</span></span>

<span data-ttu-id="b25c0-149">Доступ к классу [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) осуществляется с помощью свойства [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , доступ к которому осуществляется с помощью ключевого слова **this** (C#) или **Me** (Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="b25c0-149">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="b25c0-150">Чтобы получить доступ к имени представления, необходимо получить доступ к объекту [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , связанному с представлением.</span><span class="sxs-lookup"><span data-stu-id="b25c0-150">To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span> <span data-ttu-id="b25c0-151">В следующем примере демонстрируется отображение окна сообщения с именем активного в данный момент представления.</span><span class="sxs-lookup"><span data-stu-id="b25c0-151">The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="b25c0-152">Все шаблоны форм InfoPath содержат по крайней мере одно представление по умолчанию; Однако InfoPath также поддерживает создание нескольких представлений базового XML-документа формы.</span><span class="sxs-lookup"><span data-stu-id="b25c0-152">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document.</span></span> <span data-ttu-id="b25c0-153">При наличии нескольких представлений [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) можно использовать для работы со всеми представлениями, реализованными в шаблоне формы.</span><span class="sxs-lookup"><span data-stu-id="b25c0-153">When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template.</span></span> <span data-ttu-id="b25c0-154">Чтобы получить доступ к [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) шаблона формы, используйте свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b25c0-154">To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="b25c0-155">Можно программно изменить текущее активное представление с помощью метода [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) объекта [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="b25c0-155">You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="b25c0-156">Предыдущий пример по переключению представления будет работать только после открытия формы.</span><span class="sxs-lookup"><span data-stu-id="b25c0-156">The previous example for switching a view will work only after the form is opened.</span></span> <span data-ttu-id="b25c0-157">Чтобы задать представление по умолчанию во время события [Load](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , используйте свойство [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) класса [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b25c0-157">To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example.</span></span> <span data-ttu-id="b25c0-158">Однако обратите внимание, что это значение применяется только после сохранения и повторного открытия формы.</span><span class="sxs-lookup"><span data-stu-id="b25c0-158">Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="b25c0-159">Выбор элементов управления в представлении</span><span class="sxs-lookup"><span data-stu-id="b25c0-159">Selecting Controls in a View</span></span>

<span data-ttu-id="b25c0-160">InfoPath предоставляет два метода класса [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , которые перегружаются для программного выбора элемента управления в текущем представлении: методы [SelectText ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) и [SelectNodes ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b25c0-160">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods.</span></span> <span data-ttu-id="b25c0-161">Метод [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) используется для элементов управления вводом данных, например **текстового поля**, а метод **SelectNodes** используется для структурных элементов управления, таких как необязательный **раздел**.</span><span class="sxs-lookup"><span data-stu-id="b25c0-161">The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**.</span></span> <span data-ttu-id="b25c0-162">Для выбора конкретного элемента управления в представлении необходимо предоставить узел и, при желании, идентификатор ViewContext элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b25c0-162">To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID.</span></span> <span data-ttu-id="b25c0-163">Идентификатор ViewContext необходим, если к одному узлу в источнике данных привязано несколько элементов управления.</span><span class="sxs-lookup"><span data-stu-id="b25c0-163">The ViewContext ID is needed when you have multiple controls bound to the same node in the data source.</span></span> <span data-ttu-id="b25c0-164">InfoPath предоставляет сведения об идентификаторе ViewContext при создании формы.</span><span class="sxs-lookup"><span data-stu-id="b25c0-164">InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="b25c0-165">Идентификатор ViewContext элемента управления отображается на вкладке **Дополнительно** диалогового окна Свойства элемента управления, к которому можно получить доступ, щелкнув элемент управления правой кнопкой мыши, выбрав _контролнаме_ **Свойства**и выбрав вкладку **Дополнительно** . Идентификатор ViewContext элемента управления указан в разделе **код** вкладки **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="b25c0-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="b25c0-166">Когда используется SelectText и SelectNodes</span><span class="sxs-lookup"><span data-stu-id="b25c0-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="b25c0-167">Вы можете программным способом выбрать следующие элементы управления вводом данных с помощью метода [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) :</span><span class="sxs-lookup"><span data-stu-id="b25c0-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="b25c0-168">Текстовое поле</span><span class="sxs-lookup"><span data-stu-id="b25c0-168">Text Box</span></span>
    
- <span data-ttu-id="b25c0-169">Окно форматов RTF</span><span class="sxs-lookup"><span data-stu-id="b25c0-169">Rich Text Box</span></span>
    
- <span data-ttu-id="b25c0-170">Выбор даты</span><span class="sxs-lookup"><span data-stu-id="b25c0-170">Date Picker</span></span>
    
<span data-ttu-id="b25c0-171">С помощью метода [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) можно программно выбрать следующие структурные элементы управления:</span><span class="sxs-lookup"><span data-stu-id="b25c0-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="b25c0-172">Дополнительный раздел</span><span class="sxs-lookup"><span data-stu-id="b25c0-172">Optional Section</span></span>
    
- <span data-ttu-id="b25c0-173">Раздел выбора</span><span class="sxs-lookup"><span data-stu-id="b25c0-173">Choice Section</span></span>
    
- <span data-ttu-id="b25c0-174">Повторяющийся раздел (элементы)</span><span class="sxs-lookup"><span data-stu-id="b25c0-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="b25c0-175">Повторяющаяся таблица (строки)</span><span class="sxs-lookup"><span data-stu-id="b25c0-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="b25c0-176">Повторяющийся рекурсивный раздел (элементы)</span><span class="sxs-lookup"><span data-stu-id="b25c0-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="b25c0-177">Маркированный, нумерованный или простой список</span><span class="sxs-lookup"><span data-stu-id="b25c0-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="b25c0-178">Горизонтальная повторяющаяся таблица</span><span class="sxs-lookup"><span data-stu-id="b25c0-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="b25c0-179">Нельзя выбрать или переместить фокус программными средствами на следующие элементы управления:</span><span class="sxs-lookup"><span data-stu-id="b25c0-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="b25c0-180">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="b25c0-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="b25c0-181">Список</span><span class="sxs-lookup"><span data-stu-id="b25c0-181">List Box</span></span>
    
- <span data-ttu-id="b25c0-182">Флажок</span><span class="sxs-lookup"><span data-stu-id="b25c0-182">Check Box</span></span>
    
- <span data-ttu-id="b25c0-183">Переключатель</span><span class="sxs-lookup"><span data-stu-id="b25c0-183">Option Button</span></span>
    
- <span data-ttu-id="b25c0-184">Кнопка</span><span class="sxs-lookup"><span data-stu-id="b25c0-184">Button</span></span>
    
- <span data-ttu-id="b25c0-185">Изображение (связанное или включенное)</span><span class="sxs-lookup"><span data-stu-id="b25c0-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="b25c0-186">Рисунок от руки</span><span class="sxs-lookup"><span data-stu-id="b25c0-186">Ink Picture</span></span>
    
- <span data-ttu-id="b25c0-187">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="b25c0-187">Hyperlink</span></span>
    
- <span data-ttu-id="b25c0-188">Поле выражения</span><span class="sxs-lookup"><span data-stu-id="b25c0-188">Expression Box</span></span>
    
- <span data-ttu-id="b25c0-189">Вертикальная надпись</span><span class="sxs-lookup"><span data-stu-id="b25c0-189">Vertical Label</span></span>
    
- <span data-ttu-id="b25c0-190">Раздел ActiveX</span><span class="sxs-lookup"><span data-stu-id="b25c0-190">ActiveX Section</span></span>
    
- <span data-ttu-id="b25c0-191">Горизонтальная область.</span><span class="sxs-lookup"><span data-stu-id="b25c0-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="b25c0-192">Использование методов SelectText и SelectNodes</span><span class="sxs-lookup"><span data-stu-id="b25c0-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="b25c0-193">В следующем примере перегрузка [(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText** , который предоставляет один параметр _XmlNode_ , используется для выбора **текстового поля** , которое привязано к "My: поле1".</span><span class="sxs-lookup"><span data-stu-id="b25c0-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="b25c0-194">При наличии нескольких элементов управления, привязанных к "My: Field1", необходимо использовать перегрузку метода SelectText [(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText** , который предоставляет дополнительный параметр _ViewContext_ для выбора определенного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b25c0-194">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control.</span></span> <span data-ttu-id="b25c0-195">В следующем примере предполагается, что к "my:field1" привязано два элемента управления **Текстовое поле**, при этом идентификатор ViewContext первого элемента управления — "CTRL1", а второго — "CTRL8".</span><span class="sxs-lookup"><span data-stu-id="b25c0-195">The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8".</span></span> <span data-ttu-id="b25c0-196">Выбран второй элемент управления.</span><span class="sxs-lookup"><span data-stu-id="b25c0-196">The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="b25c0-197">В следующем примере перегрузка [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) метода **SelectNodes** , который предоставляет только один параметр _StartNode_ , используется для выбора первой строки в повторяющейся таблице, привязанной к повторяющейся группе "My: Employee (сотрудник).</span><span class="sxs-lookup"><span data-stu-id="b25c0-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="b25c0-198">В повторяющейся таблице также можно выбирать и несколько строк.</span><span class="sxs-lookup"><span data-stu-id="b25c0-198">You can also select multiple rows in a repeating table.</span></span> <span data-ttu-id="b25c0-199">В следующем примере первые три строки повторяющейся таблицы, привязанные к повторяющейся группе "My: Employee", выбираются с помощью перегрузки метода SelectNodes [(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) метода **SelectNodes** , который предоставляет  параметры _StartNode_ и _ендноде_ :</span><span class="sxs-lookup"><span data-stu-id="b25c0-199">In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
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


