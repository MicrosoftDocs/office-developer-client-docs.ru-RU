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
# <a name="work-with-views"></a><span data-ttu-id="6224c-105">Работа с представлениями</span><span class="sxs-lookup"><span data-stu-id="6224c-105">Work with Views</span></span>

<span data-ttu-id="6224c-106">При работе с шаблона формы InfoPath можно написать код для доступа к представлениям формы и выполните ряд действий на данные, которые содержат представления.</span><span class="sxs-lookup"><span data-stu-id="6224c-106">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain.</span></span> <span data-ttu-id="6224c-107">Объектная модель InfoPath, предоставленные поддерживает доступ пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) для представления формы посредством использования членов класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6224c-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="6224c-108">Обзор класса View</span><span class="sxs-lookup"><span data-stu-id="6224c-108">Overview of the View Class</span></span>

<span data-ttu-id="6224c-109">Класс [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) предоставляет следующие методы и свойства, которые могут использоваться разработчиками форм для взаимодействия с представлением InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6224c-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6224c-110">Методы и свойства класса [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) недоступны во время события [загрузки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6224c-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="6224c-111">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6224c-111">**Name**</span></span>|<span data-ttu-id="6224c-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6224c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6224c-113">Метод [DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-114">Отключает автоматическую синхронизацию между базовым XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="6224c-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="6224c-115">Метод [EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-116">Включает автоматическую синхронизацию между базовым XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="6224c-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="6224c-117">Метод [ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-118">Выполняет команду редактирования для базового XML-документа формы, основываясь на выбранных в данный момент данных в представлении.</span><span class="sxs-lookup"><span data-stu-id="6224c-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="6224c-119">Метод [ExecuteAction (тип действия, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-120">Выполняет команду редактирования для базового XML-документа формы, основываясь на указанном поле или группе.</span><span class="sxs-lookup"><span data-stu-id="6224c-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="6224c-121">Метод [Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-122">Экспортирует представление в файл определенного формата.</span><span class="sxs-lookup"><span data-stu-id="6224c-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="6224c-123">Метод [ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-124">Выполняет синхронизацию между базовым XML-документом формы и связанным представлением.</span><span class="sxs-lookup"><span data-stu-id="6224c-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="6224c-125">Метод [GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-126">Возвращает ссылку на объект **XPathNodeIterator** для прохода по возвращенным XML-узлам, начиная с указанного узла.</span><span class="sxs-lookup"><span data-stu-id="6224c-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="6224c-127">Метод [GetContextNodes (XPathNavigator, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-128">Возвращает ссылку на объект **XPathNodeIterator** для выполнения итерации в возвращенных узлах XML в текущем выборе в элементе управления, привязанном к указанного поля или группы.</span><span class="sxs-lookup"><span data-stu-id="6224c-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="6224c-129">Метод [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-130">Возвращает ссылку на объект **XPathNodeIterator** для прохода по всем XML-узлам в текущем выборе элементов в представлении.</span><span class="sxs-lookup"><span data-stu-id="6224c-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="6224c-131">Метод [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-132">Выбирает диапазон узлов в представлении, основываясь на указанном начальном XML-узле. </span><span class="sxs-lookup"><span data-stu-id="6224c-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="6224c-133">Метод [SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-134">Выбирает диапазон узлов в представлении, основываясь на указанных начальном и конечном XML-узлах.</span><span class="sxs-lookup"><span data-stu-id="6224c-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="6224c-135">Метод [SelectNodes (XPathNavigator, XPathNavigator, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-136">Выбирает диапазон узлов в представлении, основываясь на указанных начальном и конечном XML-узлах, а также на указанном элементе управления. </span><span class="sxs-lookup"><span data-stu-id="6224c-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="6224c-137">Метод [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-138">Выделяет текст, содержащийся в редактируемом элементе управления, привязанном к узлу, указанному объектом **XPathNavigator** , переданным в этот метод.</span><span class="sxs-lookup"><span data-stu-id="6224c-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="6224c-139">Метод [SelectText (XPathNavigator, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-140">Выделяет текст, содержащийся в редактируемом элементе управления, привязанном к узлу, указанному объектом **XPathNavigator** , переданным в этот метод и указанного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6224c-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="6224c-141">Метод [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="6224c-142">Создает сообщение электронной почты, содержащее текущее представление.</span><span class="sxs-lookup"><span data-stu-id="6224c-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="6224c-143">Свойство [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="6224c-144">Возвращает ссылку на объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , связанный с представлением.</span><span class="sxs-lookup"><span data-stu-id="6224c-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="6224c-145">Свойство [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)</span><span class="sxs-lookup"><span data-stu-id="6224c-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="6224c-146">Возвращает ссылку на объект [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , связанный с представлением.</span><span class="sxs-lookup"><span data-stu-id="6224c-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6224c-147">Объектная модель InfoPath также предоставляет классы [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) и [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , которые можно использовать для получения сведений обо всех представлениях, реализованных в форме.</span><span class="sxs-lookup"><span data-stu-id="6224c-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="6224c-148">Использование класса View</span><span class="sxs-lookup"><span data-stu-id="6224c-148">Using the View Class</span></span>

<span data-ttu-id="6224c-149">Класс [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) доступен через свойство [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) , к которому можно получить с помощью **этой** (C#) или ключевое слово **Me** (Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="6224c-149">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="6224c-150">Для доступа к имени представления, необходимо получить доступ к объекту [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) , связанный с представлением.</span><span class="sxs-lookup"><span data-stu-id="6224c-150">To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span> <span data-ttu-id="6224c-151">Следующий пример демонстрирует для отображения окна сообщения с именем активного представления.</span><span class="sxs-lookup"><span data-stu-id="6224c-151">The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="6224c-152">Все шаблоны форм InfoPath содержит по крайней мере один представление по умолчанию; Тем не менее InfoPath поддерживает создание нескольких представлений формы XML-документом.</span><span class="sxs-lookup"><span data-stu-id="6224c-152">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document.</span></span> <span data-ttu-id="6224c-153">При наличии нескольких представлений [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) можно использовать для работы со всех представлениях, реализованных в шаблоне формы.</span><span class="sxs-lookup"><span data-stu-id="6224c-153">When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template.</span></span> <span data-ttu-id="6224c-154">Для доступа к коллекции [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) шаблона формы, используйте свойство [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) класса [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6224c-154">To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="6224c-155">Программными средствами можно изменить представление, в настоящее время active, используя метод [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="6224c-155">You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="6224c-156">Для предыдущего примера для переключения представления будут работать только после открыта форма.</span><span class="sxs-lookup"><span data-stu-id="6224c-156">The previous example for switching a view will work only after the form is opened.</span></span> <span data-ttu-id="6224c-157">Чтобы задать представление по умолчанию во время события [загрузки](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , воспользуйтесь свойством [начальной](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) класса [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="6224c-157">To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example.</span></span> <span data-ttu-id="6224c-158">Обратите внимание, что это значение только вступят в силу после сохранения и повторного открытия формы.</span><span class="sxs-lookup"><span data-stu-id="6224c-158">Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="6224c-159">Выбор элементов управления в представлении</span><span class="sxs-lookup"><span data-stu-id="6224c-159">Selecting Controls in a View</span></span>

<span data-ttu-id="6224c-160">InfoPath предоставляет два метода класса [представления](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) , которые являются перегруженными, чтобы программно выбрать элемент управления в текущем представлении: методы [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) и [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6224c-160">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods.</span></span> <span data-ttu-id="6224c-161">Метод [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) используется для данных элементов управления, например **Текстовое поле**, а метод **SelectNodes** для структурные элементы управления, такие как **Дополнительный раздел**.</span><span class="sxs-lookup"><span data-stu-id="6224c-161">The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**.</span></span> <span data-ttu-id="6224c-162">Чтобы выбрать определенный элемент управления в представлении, необходимо указать узел и, возможно, идентификатором ViewContext элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6224c-162">To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID.</span></span> <span data-ttu-id="6224c-163">Идентификатор ViewContext необходим, когда у вас есть несколько элементов управления, привязанных на том же узле в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="6224c-163">The ViewContext ID is needed when you have multiple controls bound to the same node in the data source.</span></span> <span data-ttu-id="6224c-164">InfoPath предоставляет сведения идентификатор ViewContext, при создании формы.</span><span class="sxs-lookup"><span data-stu-id="6224c-164">InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="6224c-165">Идентификатор ViewContext элемента управления отображается на вкладке **Дополнительно** диалоговое окно "Свойства" для элемента управления, к которому можно получить, щелкнув правой кнопкой мыши элемент управления, нажав кнопку _ИмяЭлементаУправления_ **Свойства**и перейдите на вкладку **Дополнительно** . Идентификатор ViewContext элемента управления отображается в разделе **код** на вкладку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="6224c-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="6224c-166">Когда используется SelectText и SelectNodes</span><span class="sxs-lookup"><span data-stu-id="6224c-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="6224c-167">Следующие элементы управления запись данных можно выбрать программными средствами с помощью метода [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) :</span><span class="sxs-lookup"><span data-stu-id="6224c-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="6224c-168">Текстовое поле</span><span class="sxs-lookup"><span data-stu-id="6224c-168">Text Box</span></span>
    
- <span data-ttu-id="6224c-169">Окно форматов RTF</span><span class="sxs-lookup"><span data-stu-id="6224c-169">Rich Text Box</span></span>
    
- <span data-ttu-id="6224c-170">Выбор даты</span><span class="sxs-lookup"><span data-stu-id="6224c-170">Date Picker</span></span>
    
<span data-ttu-id="6224c-171">Следующие структурные элементы управления можно выбрать программными средствами с помощью метода [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) :</span><span class="sxs-lookup"><span data-stu-id="6224c-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="6224c-172">Дополнительный раздел</span><span class="sxs-lookup"><span data-stu-id="6224c-172">Optional Section</span></span>
    
- <span data-ttu-id="6224c-173">Раздел выбора</span><span class="sxs-lookup"><span data-stu-id="6224c-173">Choice Section</span></span>
    
- <span data-ttu-id="6224c-174">Повторяющийся раздел (элементы)</span><span class="sxs-lookup"><span data-stu-id="6224c-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="6224c-175">Повторяющаяся таблица (строки)</span><span class="sxs-lookup"><span data-stu-id="6224c-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="6224c-176">Повторяющийся рекурсивный раздел (элементы)</span><span class="sxs-lookup"><span data-stu-id="6224c-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="6224c-177">Маркированный, нумерованный или простой список</span><span class="sxs-lookup"><span data-stu-id="6224c-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="6224c-178">Горизонтальная повторяющаяся таблица</span><span class="sxs-lookup"><span data-stu-id="6224c-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="6224c-179">Нельзя выбрать или переместить фокус программными средствами на следующие элементы управления:</span><span class="sxs-lookup"><span data-stu-id="6224c-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="6224c-180">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="6224c-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="6224c-181">Список</span><span class="sxs-lookup"><span data-stu-id="6224c-181">List Box</span></span>
    
- <span data-ttu-id="6224c-182">Флажок</span><span class="sxs-lookup"><span data-stu-id="6224c-182">Check Box</span></span>
    
- <span data-ttu-id="6224c-183">Переключатель</span><span class="sxs-lookup"><span data-stu-id="6224c-183">Option Button</span></span>
    
- <span data-ttu-id="6224c-184">Кнопка</span><span class="sxs-lookup"><span data-stu-id="6224c-184">Button</span></span>
    
- <span data-ttu-id="6224c-185">Изображение (связанное или включенное)</span><span class="sxs-lookup"><span data-stu-id="6224c-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="6224c-186">Рисунок от руки</span><span class="sxs-lookup"><span data-stu-id="6224c-186">Ink Picture</span></span>
    
- <span data-ttu-id="6224c-187">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="6224c-187">Hyperlink</span></span>
    
- <span data-ttu-id="6224c-188">Поле выражения</span><span class="sxs-lookup"><span data-stu-id="6224c-188">Expression Box</span></span>
    
- <span data-ttu-id="6224c-189">Вертикальная надпись</span><span class="sxs-lookup"><span data-stu-id="6224c-189">Vertical Label</span></span>
    
- <span data-ttu-id="6224c-190">Раздел ActiveX</span><span class="sxs-lookup"><span data-stu-id="6224c-190">ActiveX Section</span></span>
    
- <span data-ttu-id="6224c-191">Горизонтальная область.</span><span class="sxs-lookup"><span data-stu-id="6224c-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="6224c-192">Использование методов SelectText и SelectNodes</span><span class="sxs-lookup"><span data-stu-id="6224c-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="6224c-193">В следующем примере перегрузка [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText** , предоставляющего один параметр _xmlNode_ , используется в **Текстовое поле** , связанное с «my: field1».</span><span class="sxs-lookup"><span data-stu-id="6224c-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="6224c-194">Если у вас есть несколько элементов управления, привязанных к «my: field1», необходимо использовать перегруженный метод [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) метода **SelectText** , который предоставляется параметр Дополнительные _viewContext_ для выбора конкретного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="6224c-194">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control.</span></span> <span data-ttu-id="6224c-195">В следующем примере предполагается, что существует два элемента управления **Текстового поля** , привязанных к «my: field1», с помощью первый элемент управления с Идентификатором ViewContext «CTRL1» и второй элемент управления с Идентификатором ViewContext «CTRL8».</span><span class="sxs-lookup"><span data-stu-id="6224c-195">The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8".</span></span> <span data-ttu-id="6224c-196">Второй элемент управления установлен.</span><span class="sxs-lookup"><span data-stu-id="6224c-196">The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="6224c-197">В следующем примере перегрузка [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) методу **SelectNodes** , который содержит только один параметр _Начальный_узел_ используется для выберите первую строку в повторяющейся таблицы, привязанных к повторяющейся группе «my: Сотрудник».</span><span class="sxs-lookup"><span data-stu-id="6224c-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="6224c-198">Также можно выбрать несколько строк в повторяющейся таблицы.</span><span class="sxs-lookup"><span data-stu-id="6224c-198">You can also select multiple rows in a repeating table.</span></span> <span data-ttu-id="6224c-199">В следующем примере первые три строки повторяющейся таблицы, привязанных к повторяющейся группе «my: сотрудников» выбраны с помощью метода **SelectNodes** , который предоставляет перегрузки [SelectNodes (XPathNavigator, XPathNavigator, строка)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  Параметры _Начальный_узел_ и _endNode_ :</span><span class="sxs-lookup"><span data-stu-id="6224c-199">In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
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


