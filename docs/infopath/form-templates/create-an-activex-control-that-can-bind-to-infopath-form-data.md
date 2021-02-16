---
title: Создание элемента управления ActiveX, который можно прикрепить к данным формы InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: В формах InfoPath, предназначенных для открытия в редакторе InfoPath, разработчики могут размещать элементы управления ActiveX. Такие элементы управления могут уже существовать (при этом применяются некоторые ограничения) или могут создаваться специально для InfoPath.
ms.openlocfilehash: 70ac6a16b305403ffa99d8fe840a165913642f57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300191"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a><span data-ttu-id="2d49d-104">Создание элемента управления ActiveX, который можно прикрепить к данным формы InfoPath</span><span class="sxs-lookup"><span data-stu-id="2d49d-104">Create an ActiveX Control that can Bind to InfoPath Form Data</span></span>

<span data-ttu-id="2d49d-p102">В формах InfoPath, предназначенных для открытия в редакторе InfoPath, разработчики могут размещать элементы управления ActiveX. Такие элементы управления могут уже существовать (при этом применяются некоторые ограничения) или могут создаваться специально для InfoPath.</span><span class="sxs-lookup"><span data-stu-id="2d49d-p102">You can host ActiveX controls in InfoPath forms that are designed to be opened in the InfoPath editor. These controls can be preexisting (with some constraints) or can be written specifically for InfoPath.</span></span>
  
## <a name="write-an-activex-control"></a><span data-ttu-id="2d49d-107">Создание элемента управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="2d49d-107">Write an ActiveX Control</span></span>

<span data-ttu-id="2d49d-108">Как и в случае с другими элементами управления InfoPath, элементы управления ActiveX должны поддерживать существующие интерфейсы модели COM:</span><span class="sxs-lookup"><span data-stu-id="2d49d-108">As with other controls in InfoPath, ActiveX controls should support existing Component Object Model (COM) interfaces:</span></span>
  
- <span data-ttu-id="2d49d-109">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="2d49d-109">**IDispatch**</span></span>
    
- <span data-ttu-id="2d49d-110">**IPersistPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="2d49d-110">**IPersistPropertyBag**</span></span>
    
- <span data-ttu-id="2d49d-111">**IPersistStreamInit**</span><span class="sxs-lookup"><span data-stu-id="2d49d-111">**IPersistStreamInit**</span></span>
    
- <span data-ttu-id="2d49d-112">**IPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="2d49d-112">**IPropertyPage**</span></span>
    
- <span data-ttu-id="2d49d-113">**IObjectSafety**</span><span class="sxs-lookup"><span data-stu-id="2d49d-113">**IObjectSafety**</span></span>
    
- <span data-ttu-id="2d49d-114">**IPropertyNotifySink**</span><span class="sxs-lookup"><span data-stu-id="2d49d-114">**IPropertyNotifySink**</span></span>
    
- <span data-ttu-id="2d49d-115">**IViewObject**</span><span class="sxs-lookup"><span data-stu-id="2d49d-115">**IViewObject**</span></span>
    
- <span data-ttu-id="2d49d-116">**IOleObject**</span><span class="sxs-lookup"><span data-stu-id="2d49d-116">**IOleObject**</span></span>
    
- <span data-ttu-id="2d49d-117">**IOleInPlaceObject**</span><span class="sxs-lookup"><span data-stu-id="2d49d-117">**IOleInPlaceObject**</span></span>
    
<span data-ttu-id="2d49d-118">Для обновления свойств модели DOM при изменении ими элемента управления в InfoPath этот элемент должен реализовывать следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="2d49d-118">In order for InfoPath to update properties in the Document Object Model (DOM) at the time that they change in the control, the control should implement the following interfaces:</span></span>
  
- <span data-ttu-id="2d49d-119">**IConnectionPointContainer**</span><span class="sxs-lookup"><span data-stu-id="2d49d-119">**IConnectionPointContainer**</span></span>
    
- <span data-ttu-id="2d49d-120">**IEnumConnectionPoints**</span><span class="sxs-lookup"><span data-stu-id="2d49d-120">**IEnumConnectionPoints**</span></span>
    
- <span data-ttu-id="2d49d-121">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="2d49d-121">**IConnectionPoint**</span></span>
    
- <span data-ttu-id="2d49d-122">**IEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="2d49d-122">**IEnumConnections**</span></span>
    
<span data-ttu-id="2d49d-123">Кроме того, существует два интерфейса COM для InfoPath, обеспечивающие более тесную интеграцию элементов управления:</span><span class="sxs-lookup"><span data-stu-id="2d49d-123">Also, there are two InfoPath-specific COM interfaces that provide tighter integration of controls:</span></span>
  
- [<span data-ttu-id="2d49d-124">IInfoPathControl</span><span class="sxs-lookup"><span data-stu-id="2d49d-124">IInfoPathControl</span></span>](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [<span data-ttu-id="2d49d-125">IInfoPathControlSite</span><span class="sxs-lookup"><span data-stu-id="2d49d-125">IInfoPathControlSite</span></span>](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a><span data-ttu-id="2d49d-126">Добавление элемента управления ActiveX в среду разработки InfoPath</span><span class="sxs-lookup"><span data-stu-id="2d49d-126">Add an ActiveX Control to the InfoPath Design Environment</span></span>

<span data-ttu-id="2d49d-p103">Команда **Добавление или удаление пользовательских элементов управления** в области задач **Элементы управления** позволяет использовать **мастер добавления пользовательских элементов управления** для добавления таких элементов. Мастер позволяет выбрать уже зарегистрированный элемент управления ActiveX или найти дополнительные пользовательские элементы управления на сайте Office Marketplace. После выбора элемента управления можно указать следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="2d49d-p103">The **Add or Remove Custom Controls** command on the **Controls** task pane enables you to use the **Add Custom Control Wizard** to add a custom control. By using the wizard, you can select an ActiveX control that has already been registered or find additional custom controls on Office Marketplace. After you select a control, you can specify the following items.</span></span> 
  
- <span data-ttu-id="2d49d-130">Укажите CAB-файл для установки элемента управления ActiveX с шаблоном формы.</span><span class="sxs-lookup"><span data-stu-id="2d49d-130">Specify a CAB to install the ActiveX control with your form template.</span></span>
    
- <span data-ttu-id="2d49d-131">Укажите свойство привязки, чтобы выполнить привязку к XML.</span><span class="sxs-lookup"><span data-stu-id="2d49d-131">Specify a binding property to bind to the XML.</span></span>
    
- <span data-ttu-id="2d49d-132">Укажите свойство, используемое для включения или отключения элемента управления в зависимости от правил или цифровых подписей. Например, это полезно в том случае, если XML отсутствует или используется условное форматирование.</span><span class="sxs-lookup"><span data-stu-id="2d49d-132">Specify a property that is used to enable or disable the control in response to rules or digital signatures, which can be useful, for example, when the XML is not present or when conditional formatting is used.</span></span>
    
- <span data-ttu-id="2d49d-133">Укажите привязку типа данных.</span><span class="sxs-lookup"><span data-stu-id="2d49d-133">Specify data type binding.</span></span>
    
> [!NOTE]
> <span data-ttu-id="2d49d-134">[!Примечание] Если разрабатываемый элемент управления ActiveX добавлен в область задач **Элементы управления** в InfoPath, то повторное создание элемента управления ActiveX будет невозможно до закрытия InfoPath.</span><span class="sxs-lookup"><span data-stu-id="2d49d-134">If you are developing an ActiveX control and have added it to the **Controls** task pane in InfoPath, you will be unable to rebuild the ActiveX control until InfoPath is closed.</span></span> 
  
## <a name="deploy-an-activex-control"></a><span data-ttu-id="2d49d-135">Развертывание элемента управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="2d49d-135">Deploy an ActiveX Control</span></span>

<span data-ttu-id="2d49d-p104">Чтобы распространить элемент управления ActiveX, можно создать установщик, который устанавливает элемент управления на целевом компьютере и копирует ICT-файл шаблона InfoPath вместе с CAB-файлом в папку пользователя \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls. Обратите внимание на то, что при работе нескольких разработчиков над формами, использующими элементы управления ActiveX, каждый разработчик должен иметь элементы, добавленные в среду разработки InfoPath. В противном случае изменение свойств элементов управления из InfoPath будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="2d49d-p104">To distribute an ActiveX control, you can write an installer that installs the control on the target computer and copies the InfoPath Control Template (ICT) file and the CAB file to the user's folder, \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls. Note that if two or more developers are collaborating on developing forms that use ActiveX controls, each developer should have the controls that were added to the InfoPath design environment, or they will be unable to modify the properties of the controls from InfoPath.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d49d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="2d49d-138">See also</span></span>

<span data-ttu-id="2d49d-139">Пример 6. Добавление элементов управления ActiveX в InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="2d49d-139">Lab 6: Adding ActiveX Controls in InfoPath 2003</span></span>
  
[<span data-ttu-id="2d49d-140">Создание пользовательского элемента управления InfoPath с помощью C# и .NET (блог команды разработчиков InfoPath) (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="2d49d-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span></span>](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

