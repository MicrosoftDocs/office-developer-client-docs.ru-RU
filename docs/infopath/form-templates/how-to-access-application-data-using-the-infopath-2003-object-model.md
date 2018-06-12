---
title: Доступ к данным приложения с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- шаблоны форм [infopath 2007], доступ к данным с помощью объектной модели 2003, совместимых с InfoPath 2003 шаблонов форм, доступ к данным приложения
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Объектная модель совместимых с InfoPath 2003, предоставляет объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, а также приведены сведения, относящиеся к XML-документом формы и файла определения формы (XSF). Эти данные осуществляется с помощью объекта верхнего уровня в иерархии модели объектов InfoPath, который создается с помощью интерфейса приложения.
ms.openlocfilehash: e9cf01ff2ffa939fce5af277e756e679478f8b39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807474"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Доступ к данным приложения с помощью объектной модели InfoPath 2003

Объектная модель совместимых с InfoPath 2003, предоставляет объекты и коллекции, которые можно использовать для получения доступа к сведениям о приложении InfoPath, а также приведены сведения, относящиеся к XML-документом формы и файла определения формы (XSF). Эти данные осуществляется с помощью объекта верхнего уровня в иерархии модели объектов InfoPath, который создается с помощью интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . 
  
Инициализирует проект шаблона формы управляемый код совместимых с InfoPath 2003, созданных с помощью Visual Studio 2012 `thisApplication` переменной в `_Startup` метод класса кода формы, который можно использовать для доступа к элементам интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . В следующем примере свойства [имя](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) и [версию](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) интерфейса [приложений](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) используются для возврата имя и номер версии выполняемый экземпляр InfoPath. Эти сведения отображаются в окне сообщения с помощью метода [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) интерфейс [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) . 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

В примере Visual C#, ссылку на файл `\n` символов в строке для отображения сообщения оповещения в InfoPath, неуправляемый код как стандартная новой строки выводит текст для приостановки выполнения и помещенных на новую строку в окне сообщения. Чтобы явно использовать новое значение строки, определенное для текущей среде и платформе, используйте свойство **Environment.NewLine** , как показано в следующем примере. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Доступ к данным из базового XML-документа формы

Разработчики могут использовать интерфейс [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) для получения доступа к сведениям о базовом XML-документе формы, включая ссылку на документ модели объектов XML (DOM), содержащее источник XML-данные формы. 
  
В следующем примере в первом окне сообщения отображаются некоторые данные, доступные из интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , например, были ли изменены базового XML-документа (с помощью свойства [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) и ли ее Цифровая подпись (с использованием свойство [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) ). Далее окно сообщения использует свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) интерфейс [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) для отображения исходного XML базового документа XML формы. 
  
```cs
thisXDocument.UI.Alert("\nIsDirty: " + thisXDocument.IsDirty +
   "\nIsDOMReadOnly: " + thisXDocument.IsDOMReadOnly +
   "\nIsNew: " + thisXDocument.IsNew +
   "\nIsReadOnly: " + thisXDocument.IsReadOnly +
   "\nIsSigned: " + thisXDocument.IsSigned);
thisXDocument.UI.Alert(thisXDocument.DOM.xml);
```

```vb
thisXDocument.UI.Alert("IsDirty: " &amp; thisXDocument.IsDirty &amp; vbNewLine &amp; _
   "IsDOMReadOnly: " &amp; thisXDocument.IsDOMReadOnly &amp; vbNewLine &amp; _
   "IsNew: " &amp; thisXDocument.IsNew &amp; vbNewLine &amp; _
   "IsReadOnly: " &amp; thisXDocument.IsReadOnly &amp; vbNewLine &amp; _
   "IsSigned: " &amp; thisXDocument.IsSigned)
thisXDocument.UI.Alert(thisXDocument.DOM.xml)
```

Свойство **xml** , используемые в предыдущем примере — это свойство из модели объектов документа XML (DOM). Дополнительные сведения о XML DOM обратитесь к документации MSXML 5.0 SDK. 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>Доступ к данным из файла определения формы

Сведения о файла XSF формы, включая ссылку на модель XML DOM в источник данных XML, которые он содержит также осуществляется с помощью интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) . Эти сведения осуществляется с помощью свойства [решение](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , которое возвращает ссылку на интерфейс [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) . 
  
В следующем примере первое оповещение отображает данные, доступные через интерфейс [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) , такие как расположение универсальный код ресурса (URI) (с помощью свойства [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) и номер версии (с использованием [ Версия](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) свойства). В следующем оповещении используется свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) интерфейса [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) для отображения исходного XML XSF-файла. 
  
```cs
thisXDocument.UI.Alert("PackageURL: " +
   thisXDocument.Solution.PackageURL +
   "\nURI: " + thisXDocument.Solution.URI +
   "\nVersion: " + thisXDocument.Solution.Version);
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml);
```

```vb
thisXDocument.UI.Alert("PackageURL: " &amp; _
   thisXDocument.Solution.PackageURL &amp; vbNewLine &amp; _
   "URI: " &amp; thisXDocument.Solution.URI &amp; vbNewLine &amp; _
   "Version: " &amp; thisXDocument.Solution.Version)
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml)
```


