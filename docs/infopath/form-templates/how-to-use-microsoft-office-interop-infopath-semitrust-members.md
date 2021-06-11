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
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Используйте Microsoft. Office.Interop.InfoPath.SemiTrust не совместимы с InfoPath

При добавлении кода в шаблон формы, созданном с Microsoft Office InfoPath 2003 набор средств или создании нового шаблона формы, который работает с объектной моделью InfoPath 2003 (как описано в описании Create [a Form Template Using the InfoPath 2003 Object Model),](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)по умолчанию, Microsoft InfoPath будет использовать подмножество объектов и членов, предоставляемых пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) которые идентичны тем, которые используются в InfoPath 2003. Это делается для обеспечения совместимости с InfoPath 2003. Однако объектная модель, предоставленная пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) включает дополнительные объекты и члены, которые предоставляют новые функции, добавленные в Office InfoPath 2007 и InfoPath. 
  
Например, [интерфейсы PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) и [Permission](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) предоставляют новые функции управления правами на информацию, недоступные в InfoPath 2003. Эти и другие новые объекты, добавленные в пространство имен Microsoft.Office.Interop.InfoPath.SemiTrust, по умолчанию недоступны при открытии или создании шаблона формы с управляемым кодом с помощью объектной модели, совместимой с InfoPath 2003. 
  
Аналогично, хотя интерфейс [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) обеспечивает те же функции, что и InfoPath 2003; интерфейс [_XDocument3,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) который включает дополнительные свойства и методы, которые были добавлены в Office InfoPath 2007, а _XDocument4 был включен в него дополнительные свойства и методы, добавленные в InfoPath. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) 
  
Если вы хотите использовать объекты и члены, добавленные в Office InfoPath 2007 или InfoPath в проекте шаблона форм, созданном с помощью объектной модели, предоставленной пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust,** вы можете сделать это, но код, использующий эти члены, не будет совместим с InfoPath 2003. 
  
> [!NOTE]
> Все шаблоны форм с бизнес-логикой, созданные с помощью объектной модели, предоставляемой пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust,** независимо от того, используются ли они объекты и члены, совместимые с InfoPath или нет, не поддерживаются для шаблонов форм с поддержкой браузера, развернутых в Microsoft SharePoint Server 2010 г. с InfoPath Forms Services. Бизнес-логика шаблонов форм с поддержкой браузера должна использовать новую объектную модель управляемого кода InfoPath, предоставленную [Microsoft.Office. Пространство имен InfoPath.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
  
## <a name="example"></a>Пример

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Создание объектной переменной приложения или XDocument для доступа к элементам новой объектной модели

Чтобы получить доступ к новым объектам и элементам, доступным в пространстве имен **Microsoft.Office.Interop.InfoPath.SemiTrust**, необходимо объявить и привести объектные переменные к корректной версии интерфейса, реализующей эти элементы. По умолчанию переменные и переменные имеют доступ к версиям, совместимым с `thisXDocument` `thisApplication` InfoPath 2003,  соответствующих _XDocument2 и [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) интерфейсов. Чтобы получить доступ к интерфейсам **_XDocument3** и [_Application3,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) которые предоставляют доступ к новым функциям, необходимо объявить переменную объекта типа **_XDocument3** **или _Application3,** а затем отвести объект, возвращаемый переменной, в тот же тип, который показан в следующих примерах. `thisXDocument` `thisApplication` 
  
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

После создания переменной более поздней версии _ **XDocument3** или **_Application3,** вы можете использовать ее для доступа к объекту или члену, который предоставляет новые функции InfoPath. 
  
В следующем примере показано, как использовать объектную переменную [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) типа _ **XDocument3** с свойством вспомогательного разрешения для доступа к новому интерфейсу **Permission** и его свойству [Enabled,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) чтобы определить, включены ли параметры разрешений для формы. 
  
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
  
Например, объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) не предоставляет доступ к двум новым свойствам, доступным только при использовании версии [объекта ViewInfo2:](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) свойств [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) и [HideName.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) 
  
Чтобы получить доступ к этим свойствам, необходимо объявить объектную переменную типа **ViewInfo2** и отменить объект, возвращенный свойством [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) переменной объекта **_XDocument3** в тип **ViewInfo2,** как показано в следующем примере. 
  
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


