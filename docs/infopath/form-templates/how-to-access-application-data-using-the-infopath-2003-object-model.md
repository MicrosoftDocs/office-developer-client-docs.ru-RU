---
title: Доступ к данным приложения с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- шаблоны форм [InfoPath 2007], доступ к данным с помощью объектной модели 2003, шаблоны форм, совместимые с InfoPath 2003, доступ к данным приложения
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: Объектная модель, совместимая с InfoPath 2003, предоставляет объекты и семейства, которые можно использовать для получения доступа к сведениям о приложении InfoPath, в том числе к сведениям, связанным с базовым XML-документом формы и файлом определения формы (XSF-файл). Доступ к этим данным осуществляется с помощью объекта верхнего уровня в иерархии объектной модели InfoPath, который создается с помощью интерфейса приложения.
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303684"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a><span data-ttu-id="4680f-105">Доступ к данным приложения с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="4680f-105">Access Application Data Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="4680f-106">Объектная модель, совместимая с InfoPath 2003, предоставляет объекты и семейства, которые можно использовать для получения доступа к сведениям о приложении InfoPath, в том числе к сведениям, связанным с базовым XML-документом формы и файлом определения формы (XSF-файл).</span><span class="sxs-lookup"><span data-stu-id="4680f-106">The InfoPath 2003-compatible object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="4680f-107">Доступ к этим данным осуществляется с помощью объекта верхнего уровня в иерархии объектной модели InfoPath, который создается с помощью интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4680f-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> 
  
<span data-ttu-id="4680f-108">Проект шаблона формы с управляемым кодом, совместимый с InfoPath 2003, созданный с помощью Visual `thisApplication` Studio 2012, `_Startup` инициализирует переменную в методе класса кода формы, который можно использовать для доступа к членам интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4680f-108">An InfoPath 2003-compatible managed code form template project created using Visual Studio 2012 initializes the  `thisApplication` variable in the  `_Startup` method of the form code class, which can be used to access the members of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> <span data-ttu-id="4680f-109">В следующем примере свойства [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) и [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) интерфейса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) используются для возврата имени и номера версии запущенного экземпляра InfoPath.</span><span class="sxs-lookup"><span data-stu-id="4680f-109">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="4680f-110">Эти сведения отображаются в окне сообщения с помощью метода [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) интерфейса [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4680f-110">This information is displayed in a message box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

<span data-ttu-id="4680f-111">В примере на языке Visual C# ссылка на `\n` символ в строке сообщения оповещения отображается неуправляемым кодом InfoPath как стандартный новый перевод строки, что приводит к разрыву текста и помещается на новую строку в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="4680f-111">In the Visual C# example, the reference to the  `\n` character in the string for the alert message is rendered by InfoPath unmanaged code as a standard new line feed that causes the text to break and be placed on a new line in the message box.</span></span> <span data-ttu-id="4680f-112">Чтобы явно использовать значение новой строки, указанное для текущей среды и платформы, используйте вместо этого свойство **Environment.NewLine**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="4680f-112">To explicitly use the new line value defined for the current environment and platform, use the **Environment.NewLine** property instead, as shown in the following example.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a><span data-ttu-id="4680f-113">Доступ к данным из базового XML-документа формы</span><span class="sxs-lookup"><span data-stu-id="4680f-113">Accessing Data from the Underlying XML Document of a Form</span></span>

<span data-ttu-id="4680f-114">Разработчики могут использовать интерфейс [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) для получения доступа к сведениям о БАЗОВОМ XML-документе формы, включая ссылку на модель объектов документа XML (DOM), СОДЕРЖАЩУЮ исходные XML-данные формы.</span><span class="sxs-lookup"><span data-stu-id="4680f-114">Developers can use the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface to gain access to information about a form's underlying XML document, including a reference to an XML Document Object Model (DOM) that contains the source XML data of the form.</span></span> 
  
<span data-ttu-id="4680f-115">В следующем примере в первом окне сообщения отображаются некоторые данные, доступные в интерфейсе [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , например сведения об изменении базового XML-документа (с помощью свойства [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) и о том, является ли оно Цифровая подпись (с использованием свойства [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) с подписыванием).</span><span class="sxs-lookup"><span data-stu-id="4680f-115">In the following example, the first message box displays some of the data that is available from the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, such as whether the underlying XML document has been changed (by using the [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) property) and whether it has been digitally signed (using the [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) property).</span></span> <span data-ttu-id="4680f-116">В следующем окне сообщения используется свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) для отображения ИСХОДНОГО XML базового XML-документа формы.</span><span class="sxs-lookup"><span data-stu-id="4680f-116">The next message box uses the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface's [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) property to display the source XML of the form's underlying XML document.</span></span> 
  
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

<span data-ttu-id="4680f-117">Использованное в предыдущем примере свойство **xml** является свойством модели XML DOM.</span><span class="sxs-lookup"><span data-stu-id="4680f-117">The **xml** property used in the previous example is a property of the XML Document Object Model (DOM).</span></span> <span data-ttu-id="4680f-118">Дополнительные сведения о модели XML DOM см. в документации по пакету SDK MSXML 5.0.</span><span class="sxs-lookup"><span data-stu-id="4680f-118">For more information about the XML DOM, see the MSXML 5.0 SDK documentation.</span></span> 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a><span data-ttu-id="4680f-119">Доступ к данным из файла определения формы</span><span class="sxs-lookup"><span data-stu-id="4680f-119">Accessing Data from a Form's Form Definition File</span></span>

<span data-ttu-id="4680f-120">Сведения о файле формы xsf, включая ссылку XML DOM на исходные XML-данные, которые он содержит, можно также получить с помощью интерфейса [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4680f-120">Information about a form's .xsf file, including an XML DOM reference to the source XML data that it contains, can also be accessed using the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface.</span></span> <span data-ttu-id="4680f-121">Доступ к этой информации осуществляется с помощью свойства [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , которое возвращает ссылку на интерфейс [солутионобжект](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4680f-121">This information is accessed using the [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) property, which returns a reference to the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface.</span></span> 
  
<span data-ttu-id="4680f-122">В следующем примере первое оповещение отображает некоторые данные, доступные через интерфейс [солутионобжект](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) , например, расположение URI (с использованием свойства [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) и номер его версии (с помощью [ Свойство Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="4680f-122">In the following example, the first alert displays some of the data that is available through the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface, such as its Uniform Resource Identifier (URI) location (using the [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) property) and its version number (using the [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) property).</span></span> <span data-ttu-id="4680f-123">Следующее оповещение использует свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) интерфейса [солутионобжект](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) для отображения исходного XML-файла XSF-файла.</span><span class="sxs-lookup"><span data-stu-id="4680f-123">The next alert uses the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) property of the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface to display the source XML of the .xsf file.</span></span> 
  
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


