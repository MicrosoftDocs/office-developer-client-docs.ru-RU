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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415343"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Использование элементов Microsoft. Office. Interop. InfoPath. SemiTrust, не совместимых с InfoPath

При добавлении кода в шаблон формы, созданный с помощью набора средств Microsoft Office InfoPath 2003 Toolkit, или создании нового шаблона формы, работающего с объектной моделью InfoPath, совместимой с InfoPath (как описано в разделе [Создание шаблона формы с помощью объекта InfoPath 2003) Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), по умолчанию Microsoft InfoPath будет использовать подмножество объектов и членов, предоставляемых пространством имен [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , идентичным тем, которые используются в InfoPath 2003. Это делается для обеспечения совместимости с InfoPath 2003. Однако объектная модель, предоставляемая пространством имен [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , включает в себя дополнительные объекты и члены, которые предоставляют новые функциональные возможности, добавленные в Office InfoPath 2007 и InfoPath. 
  
Например, интерфейсы [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) и [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) предоставляют новые функции управления правами на доступ к данным, недоступные в InfoPath 2003. Эти и другие новые объекты, добавленные в пространство имен Microsoft.Office.Interop.InfoPath.SemiTrust, по умолчанию недоступны при открытии или создании шаблона формы с управляемым кодом с помощью объектной модели, совместимой с InfoPath 2003. 
  
Аналогично, несмотря на то, что интерфейс [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) предоставляет те же функциональные возможности, что и InfoPath 2003; в интерфейсе [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) добавлена возможность добавления дополнительных свойств и методов, добавленных в Office InfoPath 2007, и в [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) добавлена возможность добавлять дополнительные свойства и методы, добавленные в InfoPath. . 
  
Если вы хотите использовать объекты и элементы, добавленные в Office InfoPath 2007 или InfoPath в проекте шаблона формы, созданного с помощью объектной модели, предоставляемой пространством имен **Microsoft. Office. Interop. InfoPath. SemiTrust** , вы можете сделать это, но код, использующий Эти элементы не будут совместимы с InfoPath 2003. 
  
> [!NOTE]
> Все шаблоны форм с бизнес-логикой, созданной с помощью объектной модели, предоставляемой пространством имен **Microsoft. Office. Interop. InfoPath. SemiTrust** , независимо от того, используют ли они объекты и элементы, совместимые с InfoPath, не поддерживаются для шаблоны форм с поддержкой браузера, развернутые в Microsoft SharePoint Server 2010 с помощью InfoPath Forms Services. Бизнес-логика для шаблонов форм с поддержкой веб-браузера должна использовать новую объектную модель управляемого кода InfoPath, предоставляемую пространством имен [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
  
## <a name="example"></a>Пример

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Создание объектной переменной приложения или XDocument для доступа к элементам новой объектной модели

Чтобы получить доступ к новым объектам и элементам, доступным в пространстве имен **Microsoft.Office.Interop.InfoPath.SemiTrust**, необходимо объявить и привести объектные переменные к корректной версии интерфейса, реализующей эти элементы. По умолчанию переменные `thisXDocument` и `thisApplication` переменные обращаются к версиям соответствующих интерфейсов **_XDocument2** и [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) , совместимых с InfoPath 2003. Чтобы получить доступ к интерфейсам **_XDocument3** и [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) , которые обеспечивают доступ к новым функциональным возможностям, необходимо объявить объектную переменную типа **_XDocument3** или **_Application3** , а затем привести объект, возвращенный свойством `thisXDocument`или `thisApplication` переменную до того же типа, как показано в следующих примерах. 
  
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

### <a name="accessing-a-new-object-from-the-xdocument-or-application-object-variable-using-an-accessor-property"></a>Доступ к новому объекту из объектной переменной приложения или XDocument с помощью метода доступа

После создания переменной более поздней версии _ **XDocument3** или **_Application3** ее можно использовать для доступа к объекту или члену, предоставляющим новые функции InfoPath. 
  
В приведенном ниже примере показано, как использовать объектную переменную типа _ **XDocument3** с свойством доступа к разрешениям для доступа к новому интерфейсу **разрешений** и его свойству [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) , чтобы определить, являются ли параметры разрешений [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) включен для формы. 
  
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

### <a name="accessing-a-versioned-object-and-casting-to-the-versioned-type"></a>Доступ к объекту с версией и приведение к типу версий

Если объект, существовавший в объектной модели InfoPath 2003, получает новые добавленные свойства или методы, то объект, реализующий эти новые элементы, получит имя с версией.
  
Например, объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) не предоставляет доступ к двум новым свойствам, которые доступны только при использовании объекта [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) с версиями: свойства [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) и [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) . 
  
Чтобы получить доступ к этим свойствам, необходимо объявить объектную переменную типа **ViewInfo2** и привести объект, возвращенный свойством [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) переменной _ **XDocument3** , к типу **ViewInfo2** , как показано в следующем примере. Примеры. 
  
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


