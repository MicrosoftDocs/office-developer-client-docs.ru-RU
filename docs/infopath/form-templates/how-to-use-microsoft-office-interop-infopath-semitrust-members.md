---
title: Используйте Microsoft. Office.Interop.InfoPath.SemiTrust не совместимы с InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using infopath 2007 features
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Объектная модель, предоставленная Корпорацией Майкрософт. Office.Interop.InfoPath.SemiTrust пространство имен включает объекты и члены, которые предоставляют новые функции, которые были добавлены в Office InfoPath 2007 и InfoPath.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415343"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="47480-104">Используйте Microsoft. Office.Interop.InfoPath.SemiTrust не совместимы с InfoPath</span><span class="sxs-lookup"><span data-stu-id="47480-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="47480-105">При добавлении кода в шаблон формы, созданном с Microsoft Office InfoPath 2003 набор средств или создании нового шаблона формы, который работает с объектной моделью InfoPath 2003 (как описано в описании Create [a Form Template Using the InfoPath 2003 Object Model),](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)по умолчанию, Microsoft InfoPath будет использовать подмножество объектов и членов, предоставляемых пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) которые идентичны тем, которые используются в InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="47480-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="47480-106">Это делается для обеспечения совместимости с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="47480-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="47480-107">Однако объектная модель, предоставленная пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) включает дополнительные объекты и члены, которые предоставляют новые функции, добавленные в Office InfoPath 2007 и InfoPath.</span><span class="sxs-lookup"><span data-stu-id="47480-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="47480-108">Например, [интерфейсы PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) и [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) предоставляют новые функции управления правами на информацию, недоступные в InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="47480-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="47480-109">Эти и другие новые объекты, добавленные в пространство имен Microsoft.Office.Interop.InfoPath.SemiTrust, по умолчанию недоступны при открытии или создании шаблона формы с управляемым кодом с помощью объектной модели, совместимой с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="47480-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="47480-110">Аналогично, хотя интерфейс [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) обеспечивает те же функции, что и InfoPath 2003; интерфейс [_XDocument3,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) который включает дополнительные свойства и методы, которые были добавлены в Office InfoPath 2007, а _XDocument4 был включен в него дополнительные свойства и методы, добавленные в InfoPath. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx)</span><span class="sxs-lookup"><span data-stu-id="47480-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="47480-111">Если вы хотите использовать объекты и члены, добавленные в Office InfoPath 2007 или InfoPath в проекте шаблона форм, созданном с помощью объектной модели, предоставленной пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust,** вы можете сделать это, но код, использующий эти члены, не будет совместим с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="47480-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="47480-112">Все шаблоны форм с бизнес-логикой, созданные с помощью объектной модели, предоставляемой пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust,** независимо от того, используются ли они объекты и члены, совместимые с InfoPath или нет, не поддерживаются для шаблонов форм с поддержкой браузера, развернутых в Microsoft SharePoint Server 2010 г. с InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="47480-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="47480-113">Бизнес-логика шаблонов форм с поддержкой браузера должна использовать новую объектную модель управляемого кода InfoPath, предоставленную [Microsoft.Office. Пространство имен InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx)</span><span class="sxs-lookup"><span data-stu-id="47480-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="47480-114">Пример</span><span class="sxs-lookup"><span data-stu-id="47480-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="47480-115">Создание объектной переменной приложения или XDocument для доступа к элементам новой объектной модели</span><span class="sxs-lookup"><span data-stu-id="47480-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="47480-116">Чтобы получить доступ к новым объектам и элементам, доступным в пространстве имен **Microsoft.Office.Interop.InfoPath.SemiTrust**, необходимо объявить и привести объектные переменные к корректной версии интерфейса, реализующей эти элементы.</span><span class="sxs-lookup"><span data-stu-id="47480-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="47480-117">По умолчанию переменные и переменные имеют доступ к версиям, совместимым с `thisXDocument` `thisApplication` InfoPath 2003,  соответствующих _XDocument2 и [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="47480-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="47480-118">Чтобы получить доступ к интерфейсам **_XDocument3** и [_Application3,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) которые предоставляют доступ к новым функциям, необходимо объявить переменную объекта типа **_XDocument3** **или _Application3,** а затем отвести объект, возвращаемый переменной, в тот же тип, который показан в следующих примерах. `thisXDocument` `thisApplication`</span><span class="sxs-lookup"><span data-stu-id="47480-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

```cs
// Declare an object variable of type _Application3 and
// cast the object returned by the thisApplication variable to
// the same type.
_Application3 thisApplication3 = (_Application3)thisXDocument;
```

```vb
' Declare an object variable of type _Application3 and
' cast the object returned by the thisXApplication variable to
' the same type.
Dim thisDocument As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
```

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="47480-119">Доступ к новому объекту из объектной переменной приложения или XDocument с помощью метода доступа</span><span class="sxs-lookup"><span data-stu-id="47480-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="47480-120">После создания переменной более поздней версии _ **XDocument3** или **_Application3,** вы можете использовать ее для доступа к объекту или члену, который предоставляет новые функции InfoPath.</span><span class="sxs-lookup"><span data-stu-id="47480-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="47480-121">В следующем примере показано, как использовать объектную переменную [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) типа _ **XDocument3** с свойством вспомогательного разрешения для доступа к новому интерфейсу **Permission** и его свойству [Enabled,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) чтобы определить, включены ли параметры разрешений для формы.</span><span class="sxs-lookup"><span data-stu-id="47480-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Use the object variable to access the later version object and
// property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Use the object variable to access the later version object and
' property.
thisXDocument.UI.Alert(thisDocument3.Permission.Enabled.ToString())
```

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="47480-122">Доступ к объекту с версией и приведение к типу версий</span><span class="sxs-lookup"><span data-stu-id="47480-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="47480-123">Если объект, существовавший в объектной модели InfoPath 2003, получает новые добавленные свойства или методы, то объект, реализующий эти новые элементы, получит имя с версией.</span><span class="sxs-lookup"><span data-stu-id="47480-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="47480-124">Например, объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) не предоставляет доступ к двум новым свойствам, доступным только при использовании версии [объекта ViewInfo2:](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) свойств [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) и [HideName.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx)</span><span class="sxs-lookup"><span data-stu-id="47480-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="47480-125">Чтобы получить доступ к этим свойствам, необходимо объявить объектную переменную типа **ViewInfo2** и отменить объект, возвращенный свойством [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) переменной объекта **_XDocument3** в тип **ViewInfo2,** как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="47480-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
```cs
// Declare an object variable of type _XDocument3 and
// cast the object returned by the thisXDocument variable to
// the same type.
_XDocument3 thisXDocument3 = (_XDocument3)thisXDocument;
// Declare an object variable of type ViewInfo2 and cast the object 
// returned by the ViewInfos property to that type.
ViewInfo2 thisView = (ViewInfo2)thisXDocument3.ViewInfos["View2"];
// Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString());
```

```vb
' Declare an object variable of type _XDocument3 and
' cast the object returned by the thisXDocument variable to
' the same type.
Dim thisXDocument3 As _XDocument3 = _
   DirectCast(thisXDocument, _XDocument3)
' Declare an object variable of type ViewInfo2 and cast the object 
' returned by the ViewInfos property to that type.
Dim thisView As ViewInfo2 = _
   DirectCast(thisXDocument3.ViewInfos("View2"), ViewInfo2)
' Display the value of the new HideName property.
thisXDocument3.UI.Alert(thisView.HideName.ToString())
```


