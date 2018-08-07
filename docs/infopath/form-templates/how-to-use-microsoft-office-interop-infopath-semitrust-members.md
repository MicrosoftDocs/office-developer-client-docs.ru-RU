---
title: Использование элементов Microsoft.Office.Interop.InfoPath.SemiTrust, не совместимый с InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- шаблоны форм с поддержкой веб-2003 InfoPath, с помощью функции infopath 2007
localization_priority: Normal
ms.assetid: d082f3a3-387a-4db1-bbad-495c326b8ee3
description: Объектная модель, предоставляемой пространством имен Microsoft.Office.Interop.InfoPath.SemiTrust содержит объекты и члены, которые предоставляют новые функциональные возможности, который был добавлен в Office InfoPath 2007 и InfoPath.
ms.openlocfilehash: 3d0e9b450dab6a821af1f698d9859b21e85abf81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807500"
---
# <a name="use-microsoftofficeinteropinfopathsemitrust-members-not-compatible-with-infopath"></a>Использование элементов Microsoft.Office.Interop.InfoPath.SemiTrust, не совместимый с InfoPath

При добавлении кода в шаблон формы, который был создан с помощью набора инструментов Microsoft Office InfoPath 2003 или создание нового шаблона формы, работающий с объектной моделью совместимых с InfoPath 2003 (как описано в [Создать шаблон формы с помощью объекта InfoPath 2003 Модель](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)), по умолчанию Microsoft InfoPath будет использовать подмножество объекты и члены предоставляемой пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , что совпадают используются с InfoPath 2003. Это делается в целях обеспечения совместимости с InfoPath 2003. Тем не менее объектной модели, предоставляемой пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) включает в себя дополнительные объекты и члены, которые предоставляют новые функциональные возможности, который был добавлен в Office InfoPath 2007 и InfoPath. 
  
Например [PermissionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.PermissionObject.aspx) и [разрешение](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.aspx) интерфейсы предоставляют новые возможности управления правами сведения, недоступны в InfoPath 2003. Это и других новых объектов, добавленных в пространстве имен Microsoft.Office.Interop.InfoPath.SemiTrust, недоступны по умолчанию при открытии или создание шаблона формы с управляемым кодом с помощью объектной модели, совместимой с InfoPath 2003. 
  
Аналогично, в то время как [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) интерфейс предоставляет функциональные возможности, аналогичные InfoPath 2003; интерфейс [_XDocument3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.aspx) была версии включают в себя дополнительные свойства и методы, которые были добавлены в Microsoft Office InfoPath 2007 и [_XDocument4](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument4.aspx) был версии включают в себя дополнительные свойства и методы, которые были добавлены в InfoPath . 
  
Если вы хотите использовать объекты и члены, которые были добавлены в Microsoft Office InfoPath 2007 или InfoPath в проект шаблона формы, созданные с помощью объектной модели, предоставляемой пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust** , это можно сделать, но код, использующий Эти элементы не совместимы с InfoPath 2003. 
  
> [!NOTE]
> Все шаблоны форм с бизнес-логики, созданных с помощью объектной модели, предоставляемой пространством имен **Microsoft.Office.Interop.InfoPath.SemiTrust** , будет ли они используют объекты и члены, совместимые с InfoPath, или нет, не поддерживаются для шаблоны форм с поддержкой веб-браузера, развернут в Microsoft SharePoint Server 2010 с помощью службы InfoPath Forms Services. Бизнес-логика для шаблонов форм с поддержкой веб-браузера необходимо использовать новые модели объектов управляемого кода InfoPath, предоставляемой пространством имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) . 
  
## <a name="example"></a>Пример

### <a name="creating-an-xdocument-or-application-object-variable-to-access-new-object-model-members"></a>Создание объектной переменной приложения или XDocument для доступа к элементам новой объектной модели

Для доступа к новые объекты и члены, доступные в пространстве имен **Microsoft.Office.Interop.InfoPath.SemiTrust** , необходимо объявить и приведение объектных переменных правильную версию интерфейса, который реализует эти элементы. По умолчанию `thisXDocument` и `thisApplication` переменные доступ к версиям совместимых с InfoPath 2003 соответствующие **_XDocument2** и [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) интерфейсов. Для доступа к **_XDocument3** и [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application3.aspx) интерфейсы, которые обеспечивают доступ к новые функциональные возможности, необходимо объявить объектную переменную типа **_XDocument3** или **_Application3** и затем привести объект, возвращенный свойством `thisXDocument`или `thisApplication` переменных для того же типа, как показано в следующих примерах. 
  
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

После создания переменной более поздние версии _ **XDocument3** или **_Application3** тип, его можно использовать для доступа к объекта или элемента, который предоставляет новые функциональные возможности InfoPath. 
  
Следующем примере показано, как использовать объектную переменную типа _ **XDocument3** со свойством [разрешение](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.Permission.aspx) доступа к данным для доступа к новым интерфейсом **разрешений** и его свойства [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Permission.Enabled.aspx) , чтобы определить, если параметры разрешений включить для формы. 
  
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
  
Например, объект [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.aspx) не предоставляет доступ к двум новым свойствам, которые доступны только при использовании версии объекта [ViewInfo2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.aspx) : свойства [Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.Caption.aspx) и [HideName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo2.HideName.aspx) . 
  
Для доступа к этим свойствам, необходимо объявить объектную переменную типа **ViewInfo2** и привести объект, возвращенный свойством [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument3.ViewInfos.aspx) объектной переменной **XDocument3** _ **ViewInfo2** тип, как показано в следующем Пример. 
  
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


