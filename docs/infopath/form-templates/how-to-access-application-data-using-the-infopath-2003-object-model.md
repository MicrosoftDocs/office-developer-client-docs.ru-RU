---
title: Доступ к данным приложений с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- шаблоны форм [infopath 2007], доступ к данным с помощью объектной модели 2003, шаблоны форм, совместимые с InfoPath 2003, доступ к данным приложений
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Объектная модель, совместимая с InfoPath 2003, предоставляет объекты и семейства, которые можно использовать для получения доступа к сведениям о приложении InfoPath, в том числе к сведениям, связанным с базовым XML-документом формы и файлом определения формы (XSF-файл). Эти данные можно получить через объект верхнего уровня в иерархии объектной модели InfoPath, который мгновенно используется с помощью интерфейса Приложения.
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437443"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>Доступ к данным приложений с помощью объектной модели InfoPath 2003

Объектная модель, совместимая с InfoPath 2003, предоставляет объекты и семейства, которые можно использовать для получения доступа к сведениям о приложении InfoPath, в том числе к сведениям, связанным с базовым XML-документом формы и файлом определения формы (XSF-файл). Эти данные можно получить через объект верхнего уровня в иерархии объектной модели InfoPath, который мгновенно используется с помощью [интерфейса Приложения.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) 
  
Проект шаблона управляемых форм кода, совместимый с InfoPath 2003, созданный с Visual Studio 2012 г., инициализирует переменную в методе класса кода формы, который можно использовать для доступа к участникам интерфейса `thisApplication` `_Startup` [приложения.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) В следующем примере свойства [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) и [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) интерфейса [Приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) используются для возврата имени и номера версии запущенного экземпляра InfoPath. Эти сведения отображаются в поле сообщений с помощью метода [Оповещения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) [интерфейса UI2.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

В примере Visual C# ссылку на символ в строке для сообщения оповещения отрисовывается неугодным кодом InfoPath в качестве стандартного нового канала строки, из-за которого текст ломается и помещается на новую строку в поле  `\n` сообщений. Чтобы явно использовать значение новой строки, указанное для текущей среды и платформы, используйте вместо этого свойство **Environment.NewLine**, как показано в следующем примере. 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>Доступ к данным из базового XML-документа формы

Разработчики могут использовать [интерфейс XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) для получения доступа к сведениям о основном XML-документе формы, включая ссылку на объектную модель XML-документа (DOM), содержаную исходные XML-данные формы. 
  
В следующем примере в первом окне сообщений отображаются некоторые данные, доступные из интерфейса [XDocument,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) например, изменен ли документ XML(с помощью свойства [IsDirty)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) и был ли он подписан в цифровом формате (с помощью свойства [IsSigned).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) В следующем поле сообщений используется свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) для отображения источника XML в основном XML-документе формы. 
  
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

Использованное в предыдущем примере свойство **xml** является свойством модели XML DOM. Дополнительные сведения о модели XML DOM см. в документации по пакету SDK MSXML 5.0. 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>Доступ к данным из файла определения формы

Сведения о файле XSF формы, включая ссылку XML DOM на исходные XML-данные, которые он содержит, также можно получить с помощью интерфейса [XDocument.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) Эти сведения доступны с помощью свойства [Solution,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) которое возвращает ссылку на [интерфейс SolutionObject.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) 
  
В следующем примере первое оповещение отображает некоторые данные, доступные через интерфейс [SolutionObject,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) например расположение единого идентификатора ресурсов (URI) (с помощью свойства [URI)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) и номер версии (с помощью свойства [Version).](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) В следующем оповещении используется [свойство DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) [интерфейса SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) для отображения источника XML файла .xsf. 
  
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


