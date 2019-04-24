---
title: Использование элементов Microsoft. Office. Interop. InfoPath. SemiTrust, не совместимых с InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- шаблоны форм, совместимые с InfoPath 2003, с помощью функций InfoPath 2007
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Объектная модель, предоставляемая пространством имен Microsoft. Office. Interop. InfoPath. SemiTrust, включает объекты и члены, которые предоставляют новые функциональные возможности, добавленные в Office InfoPath 2007 и InfoPath.
ms.openlocfilehash: 45f7607aec8ccfd653780a550df0823730835a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300086"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a><span data-ttu-id="8452c-104">Использование элементов Microsoft. Office. Interop. InfoPath. SemiTrust, не совместимых с InfoPath</span><span class="sxs-lookup"><span data-stu-id="8452c-104">Use Microsoft.Office.Interop.InfoPath.SemiTrust members not compatible with InfoPath</span></span>

<span data-ttu-id="8452c-105">При добавлении кода в шаблон формы, созданный с помощью набора средств Microsoft Office InfoPath 2003 Toolkit, или создании нового шаблона формы, работающего с объектной моделью InfoPath, совместимой с InfoPath (как описано в разделе [Создание шаблона формы с помощью объекта InfoPath 2003) Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), по умолчанию Microsoft InfoPath будет использовать подмножество объектов и членов, предоставляемых пространством имен [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , идентичным тем, которые используются в InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8452c-105">When you add code to a form template that was created with the Microsoft Office InfoPath 2003 Toolkit or create a new form template that works with the InfoPath 2003-compatible object model (as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), by default, Microsoft InfoPath will use a subset of the objects and members provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace that are identical to those used by InfoPath 2003.</span></span> <span data-ttu-id="8452c-106">Это делается для обеспечения совместимости с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8452c-106">This is done to provide compatibility with InfoPath 2003.</span></span> <span data-ttu-id="8452c-107">Однако объектная модель, предоставляемая пространством имен [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , включает в себя дополнительные объекты и члены, которые предоставляют новые функциональные возможности, добавленные в Office InfoPath 2007 и InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8452c-107">However, the object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace includes additional objects and members that provide new functionality that was added to Office InfoPath 2007 and InfoPath.</span></span> 
  
<span data-ttu-id="8452c-108">Например, интерфейсы [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) и [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) предоставляют новые функции управления правами на доступ к данным, недоступные в InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8452c-108">For example, the [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) and [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) interfaces provide new information rights management functionality that is not available in InfoPath 2003.</span></span> <span data-ttu-id="8452c-109">Эти и другие новые объекты, добавленные в пространство имен Microsoft.Office.Interop.InfoPath.SemiTrust, по умолчанию недоступны при открытии или создании шаблона формы с управляемым кодом с помощью объектной модели, совместимой с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8452c-109">This, and other new objects added to the Microsoft.Office.Interop.InfoPath.SemiTrust namespace are not available by default when you open or create managed code form template with InfoPath 2003-compatible object model.</span></span> 
  
<span data-ttu-id="8452c-110">Аналогично, несмотря на то, что интерфейс [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) предоставляет те же функциональные возможности, что и InfoPath 2003; в интерфейсе [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) добавлена возможность добавления дополнительных свойств и методов, добавленных в Office InfoPath 2007, и в [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) добавлена возможность добавлять дополнительные свойства и методы, добавленные в InfoPath. .</span><span class="sxs-lookup"><span data-stu-id="8452c-110">Similarly, while the [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) interface provides the same functionality as InfoPath 2003; the [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) interface has been versioned to include additional properties and methods that were added in Office InfoPath 2007, and the [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) has been versioned to include additional properties and methods that were added in InfoPath.</span></span> 
  
<span data-ttu-id="8452c-111">Если вы хотите использовать объекты и элементы, добавленные в Office InfoPath 2007 или InfoPath в проекте шаблона формы, созданного с помощью объектной модели, предоставляемой пространством имен **Microsoft. Office. Interop. InfoPath. SemiTrust** , вы можете сделать это, но код, использующий Эти элементы не будут совместимы с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8452c-111">If you want to use objects and members that were added in Office InfoPath 2007 or InfoPath in a form template project created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you can do so, but code that uses these members will not be compatible with InfoPath 2003.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8452c-112">Все шаблоны форм с бизнес-логикой, созданной с помощью объектной модели, предоставляемой пространством имен **Microsoft. Office. Interop. InfoPath. SemiTrust** , независимо от того, используют ли они объекты и элементы, совместимые с InfoPath, не поддерживаются для шаблоны форм с поддержкой браузера, развернутые в Microsoft SharePoint Server 2010 с помощью InfoPath Forms Services.</span><span class="sxs-lookup"><span data-stu-id="8452c-112">All form templates with business logic created using the object model provided by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, whether they use objects and members compatible with InfoPath or not, are not supported for browser-enabled form templates deployed to Microsoft SharePoint Server 2010 with InfoPath Forms Services.</span></span> <span data-ttu-id="8452c-113">Бизнес-логика для шаблонов форм с поддержкой веб-браузера должна использовать новую объектную модель управляемого кода InfoPath, предоставляемую пространством имен [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8452c-113">Business logic for browser-enabled form templates must use the new InfoPath managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8452c-114">Пример</span><span class="sxs-lookup"><span data-stu-id="8452c-114">Example</span></span>

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a><span data-ttu-id="8452c-115">Создание объектной переменной приложения или XDocument для доступа к элементам новой объектной модели</span><span class="sxs-lookup"><span data-stu-id="8452c-115">Creating an XDocument or Application Object Variable to Access New Object Model Members</span></span>

<span data-ttu-id="8452c-116">Чтобы получить доступ к новым объектам и элементам, доступным в пространстве имен **Microsoft.Office.Interop.InfoPath.SemiTrust**, необходимо объявить и привести объектные переменные к корректной версии интерфейса, реализующей эти элементы.</span><span class="sxs-lookup"><span data-stu-id="8452c-116">To access the new objects and members that are available in the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace, you must declare and cast object variables to the correct version of the interface that implements these members.</span></span> <span data-ttu-id="8452c-117">По умолчанию переменные `thisXDocument` и `thisApplication` переменные обращаются к версиям соответствующих интерфейсов **_XDocument2** и [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) , совместимых с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="8452c-117">By default, the  `thisXDocument` and  `thisApplication` variables access the InfoPath 2003-compatible versions of the corresponding **_XDocument2** and [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) interfaces.</span></span> <span data-ttu-id="8452c-118">Чтобы получить доступ к интерфейсам **_XDocument3** и [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) , которые обеспечивают доступ к новым функциональным возможностям, необходимо объявить объектную переменную типа **_XDocument3** или **_Application3** , а затем привести объект, возвращенный свойством `thisXDocument`или `thisApplication` переменную до того же типа, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="8452c-118">To access the **_XDocument3** and [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) interfaces that provide access to new functionality, you must declare an object variable of the **_XDocument3** or **_Application3** type, and then cast the object returned by the  `thisXDocument` or  `thisApplication` variable to the same type as shown in the following examples.</span></span> 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a><span data-ttu-id="8452c-119">Доступ к новому объекту из объектной переменной приложения или XDocument с помощью метода доступа</span><span class="sxs-lookup"><span data-stu-id="8452c-119">Accessing a New Object From The XDocument or Application Object Variable Using an Accessor Property</span></span>

<span data-ttu-id="8452c-120">После создания переменной более поздней версии _ **XDocument3** или **_Application3** ее можно использовать для доступа к объекту или члену, предоставляющим новые функции InfoPath.</span><span class="sxs-lookup"><span data-stu-id="8452c-120">After you have created a variable of the later version _ **XDocument3** or **_Application3** type, you can use it to access an object or member that provides new InfoPath functionality.</span></span> 
  
<span data-ttu-id="8452c-121">В приведенном ниже примере показано, как использовать объектную переменную типа _ **XDocument3** с свойством доступа к разрешениям для доступа к новому интерфейсу **разрешений** и его свойству [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) , чтобы определить, являются ли параметры разрешений [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) включен для формы.</span><span class="sxs-lookup"><span data-stu-id="8452c-121">The following example shows how to use an object variable of type _ **XDocument3** with the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) accessor property to access the new **Permission** interface and its [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) property to determine if permission settings are enabled for the form.</span></span> 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a><span data-ttu-id="8452c-122">Доступ к объекту с версией и приведение к типу версий</span><span class="sxs-lookup"><span data-stu-id="8452c-122">Accessing a Versioned Object and Casting to the Versioned Type</span></span>

<span data-ttu-id="8452c-123">Если объект, существовавший в объектной модели InfoPath 2003, получает новые добавленные свойства или методы, то объект, реализующий эти новые элементы, получит имя с версией.</span><span class="sxs-lookup"><span data-stu-id="8452c-123">If an object that existed in the InfoPath 2003 object model has new properties or methods added to it, the object that implements those new members will have a name that is versioned.</span></span>
  
<span data-ttu-id="8452c-124">Например, объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) не предоставляет доступ к двум новым свойствам, которые доступны только при использовании объекта [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) с версиями: свойства [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) и [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8452c-124">For example, the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) object does not provide access to two new properties that are only available when using the versioned [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) object: the [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) and [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) properties.</span></span> 
  
<span data-ttu-id="8452c-125">Чтобы получить доступ к этим свойствам, необходимо объявить объектную переменную типа **ViewInfo2** и привести объект, возвращенный свойством [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) переменной _ **XDocument3** , к типу **ViewInfo2** , как показано в следующем примере. Примеры.</span><span class="sxs-lookup"><span data-stu-id="8452c-125">To access these properties, you must declare an object variable of type **ViewInfo2** and cast the object returned by the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) property of the _ **XDocument3** object variable to the **ViewInfo2** type as shown in the following example.</span></span> 
  
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


