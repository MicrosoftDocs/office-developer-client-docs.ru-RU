---
title: Инициализация и очистка кода с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, clean-up code,InfoPath 2003-compatible form templates, initialization code
localization_priority: Normal
ms.assetid: 8d19e8fa-4e5c-40bb-ae89-7a552cc7914d
description: По умолчанию файл FormCode.cs или FormCode.vb, который создается для проекта шаблона формы, совместимого с InfoPath 2003, содержит полный исходный код для программирования логики формы. Шаблон проекта создает класс в файле FormCode.cs или FormCode.vb, схожий с классами, приведенными в указанных далее примерах, где можно указать инициализацию и очистку кода, а также обработчики для событий формы. Файлы FormCode.cs и FormCode.vb применяют атрибут уровня сборки System.ComponentModel.DescriptionAttribute, который идентифицирует класс в качестве единственного класса, где реализуются обработчики событий. Атрибут InfoPathNamespace (который реализуется типом InfoPathNamespaceAttribute ) применяется к классу для идентификации пространств имен выборки XML DOM, используемых в рамках класса. Пространства имен, указанные в InfoPathNamespace, обслуживаются системой проектов InfoPath.
ms.openlocfilehash: 1ae81c261ad9927195c0a4ac6d80f58a16a6ebf1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383123"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a><span data-ttu-id="9a377-108">Инициализация и очистка кода с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a377-108">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>

<span data-ttu-id="9a377-p102">По умолчанию файл FormCode.cs или FormCode.vb, который создается для проекта шаблона формы, совместимого с InfoPath 2003, содержит полный исходный код для программирования логики формы. Шаблон проекта создает класс в файле FormCode.cs или FormCode.vb, схожий с классами, приведенными в указанных далее примерах, где можно указать инициализацию и очистку кода, а также обработчики для событий формы. Файлы FormCode.cs и FormCode.vb применяют атрибут уровня сборки **System.ComponentModel.DescriptionAttribute**, который идентифицирует класс в качестве единственного класса, где реализуются обработчики событий. Атрибут **InfoPathNamespace** (который реализуется типом [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) ) применяется к классу для идентификации пространств имен выборки XML DOM, используемых в рамках класса. Пространства имен, указанные в **InfoPathNamespace**, обслуживаются системой проектов InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9a377-p102">By default, the FormCode.cs or FormCode.vb file that is created for a form template project that is compatible with InfoPath 2003 contains all the source code for the programming logic of the form. The template for the project generates a class in the FormCode.cs or FormCode.vb file much like the classes in the following examples where you can define initialization and clean-up code, as well as handlers for form events. The FormCode.cs and FormCode.vb files apply an assembly-level **System.ComponentModel.DescriptionAttribute** attribute, which identifies the class as the only class where event handlers are implemented. The **InfoPathNamespace** attribute (which is implemented by the [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) type) is applied to a class to identify the XML DOM selection namespaces used within the class. The namespaces referenced in the **InfoPathNamespace** are maintained by the InfoPath project system.</span></span> 
  
<span data-ttu-id="9a377-114">Класс FormCode непосредственно предоставляет методы  `_Startup` и  `_Shutdown`, которые используются для выполнения процедур инициализации и очистки любых компонентов, которые требуются в дополнение к стандартным возможностям InfoPath во время открытия формы.</span><span class="sxs-lookup"><span data-stu-id="9a377-114">The FormCode class itself provides  `_Startup` and  `_Shutdown` methods that are used to perform initialization and clean-up routines for any components that are required in addition to standard InfoPath functionality while the form is open.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9a377-p103">[!Важно!] Не вызывайте элементы объектной модели InfoPath из методов  `_Startup` и  `_Shutdown`. В этих методах следует выполнять инициализацию и вызов только элементов внешних компонентов.</span><span class="sxs-lookup"><span data-stu-id="9a377-p103">Do not call members of the InfoPath object model from within the  `_Startup` and  `_Shutdown` methods. You should initialize and call only members of external components in these methods.</span></span> 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-27-27'")]
    public partial class FormCode
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // You can add additional initialization code here.
        }
        public void _Shutdown()
        {
        }
    }
}
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
    ' The namespace prefixes defined in this attribute must remain synchronized with
    ' those in the form definition file (.xsf).
    <InfoPathNamespace( _
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-36-40'")> _
    Public Class FormCode
        Private thisXDocument As XDocument
        Private thisApplication As Application
        Public Sub _Startup(app As Application, doc As XDocument)
            thisXDocument = doc
            thisApplication = app
            ' You can add additional initialization code here.
        End Sub
        Public Sub _Shutdown()
        End Sub
    End Class
End Namespace
```

## <a name="the-startup-method"></a><span data-ttu-id="9a377-117">Метод _Startup</span><span class="sxs-lookup"><span data-stu-id="9a377-117">The _Startup Method</span></span>

<span data-ttu-id="9a377-p104">Помимо предоставления области для написания кода инициализации дополнительных компонентов, метод  `_Startup` инициализирует переменные  `thisXDocument` и  `thisApplication`, которые можно использовать в коде формы для доступа к элементам классов [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) и [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) в объектной модели InfoPath. Код, необходимый для инициализации этих двух переменных, автоматически создается шаблоном проекта.</span><span class="sxs-lookup"><span data-stu-id="9a377-p104">In addition to providing a place to write initialization code for additional components, the  `_Startup` method initializes the  `thisXDocument` and  `thisApplication` variables that can be used in your form code to access the members of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) and [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) classes in the InfoPath object model. The code necessary to initialize the two variables is generated automatically by the project template.</span></span> 
  
```cs
    private XDocument thisXDocument;
    private Application thisApplication;
    public void _Startup(Application app, XDocument doc)
    {
        thisXDocument = doc;
        thisApplication = app;
        // You can add additional initialization code here.
    }
```

```vb
    Private thisXDocument As XDocument
    Private thisApplication As Application
    Public Sub _Startup(app As Application, doc As XDocument)
        thisXDocument = doc
        thisApplication = app
        ' You can add additional initialization code here.
    End Sub

```

<span data-ttu-id="9a377-120">В следующих примерах демонстрируется простой обработчик событий для кнопки, использующей переменную  `thisXDocument` для доступа к методу [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) типа [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9a377-120">The following examples show a simple event handler for a button that uses the  `thisXDocument` variable to access the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) type.</span></span> 
  
```cs
[InfoPathEventHandler(MatchPath="CTRL1_5", EventType=InfoPathEventType.OnClick)]
public void CTRL1_5_OnClick(DocActionEvent e)
{
    // Write your code here.
    thisXDocument.UI.Alert("Hello!");
}
```

```vb
<InfoPathEventHandler(MatchPath:="CTRL1_5", EventType:=InfoPathEventType.OnClick)> _
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
    ' Write your code here.
    thisXDocument.UI.Alert("Hello!")
End Sub
```

<span data-ttu-id="9a377-121">Сведения о том, как создать обработчик событий в разделе [Add события обработчик с помощью объектной модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="9a377-121">For information on how to create an event handler, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
  
## <a name="the-shutdown-method"></a><span data-ttu-id="9a377-122">Метод _ShutDown</span><span class="sxs-lookup"><span data-stu-id="9a377-122">The _ShutDown Method</span></span>

<span data-ttu-id="9a377-p105">Метод  `_Shutdown` является последним методом, вызываемым при закрытии формы. В этом методе можно написать любой код, необходимый для очистки и завершения компонентов, используемых в форме.</span><span class="sxs-lookup"><span data-stu-id="9a377-p105">The  `_Shutdown` method is the last method called when a form is closed. You can write any code in this method that is needed to clean up or finalize components used in the form.</span></span> 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a><span data-ttu-id="9a377-125">Пример кода инициализации и очистки</span><span class="sxs-lookup"><span data-stu-id="9a377-125">Initialization and Clean-up Code Example</span></span>

<span data-ttu-id="9a377-p106">В следующем примере демонстрируется инициализация подключения к базе данных Microsoft SQL Server в методе  `_Startup` и закрытие подключения в методе  `_Shutdown`. Чтобы этот пример работал правильно, необходимо сначала указать ссылку на сборку System.Data для платформы .NET Framework, выбрав пункт **Добавить ссылку** в меню **Проект**, а затем выбрать компонент System.Data.dll на вкладке **.NET**. Кроме того, обратите внимание, что в верхней части файла кода формы добавлена директива  `using System.Data.SqlClient` (или  `Imports System.Data.SqlClient)` для уменьшения числа нажатий клавиш.</span><span class="sxs-lookup"><span data-stu-id="9a377-p106">The following example shows how to initialize a connection to a Microsoft SQL Server database in the  `_Startup` method and close the connection in the  `_Shutdown` method. In order for this example to work correctly, you must first set a reference to the System.Data assembly of the .NET Framework by clicking **Add Reference** on the **Project** menu, and then selecting the System.Data.dll component on the **.NET** tab. Also note that the  `using System.Data.SqlClient` (or  `Imports System.Data.SqlClient)` directive was added at the top of the form code file to reduce keystrokes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9a377-128">Пользователи формы InfoPath, который содержит код формы, который подключается к базе данных SQL Server может потребоваться разрешения безопасности в зависимости от того, как развернуть формы и определена политика безопасности.</span><span class="sxs-lookup"><span data-stu-id="9a377-128">Users of an InfoPath form that contains form code that connects to a SQL Server database may require security permissions depending on how the form is deployed and security policy is defined.</span></span> <span data-ttu-id="9a377-129">Дополнительные сведения о безопасности содержатся в разделе [О модели безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md) и [Настройка параметров безопасности для шаблонов форм с кодом](how-to-configure-security-settings-for-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="9a377-129">For more information on security see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md) and [Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md).</span></span> 
  
```cs
using System;
using System.Data.SqlClient;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-05T20-56-13'")]
    public partial class Template1
    {
        private XDocument    thisXDocument;
        private Application    thisApplication;
        private SqlConnection sqlConnect;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // Initialize variable for SQL Server connection.
            sqlConnect= new SqlConnection("server=localhost;Trusted_Connection=yes;database=Northwind");
        }
        public void _Shutdown()
        {
            // Close SQL Server connection at shut down.
            sqlConnect.Close();
        }
    }
}
```

```vb
Imports System
Imports System.Data.SqlClient
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
        ' The namespace prefixes defined in this attribute must remain synchronized with
        ' those in the form definition file (.xsf).
        <InfoPathNamespace( _
            "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-08T18-47-33'")>        _
        Public Class Template1
            Private thisXDocument As XDocument
            Private thisApplication As Application
            Private sqlConnect As SqlConnection
            Public Sub _Startup(app As Application, doc As XDocument)
                thisXDocument = doc
                thisApplication = app
                ' Initialize variable for SQL Server connection.
                sqlConnect = New SqlConnection _("server=localhost;Trusted_Connection=yes;database=Northwind")
            End Sub
        Public Sub _Shutdown()
            ' Close SQL Server connection.
            sqlConnect.Close()
        End Sub
    End Class
End Namespace
```

## <a name="see-also"></a><span data-ttu-id="9a377-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9a377-130">See also</span></span>



[<span data-ttu-id="9a377-131">Добавление обработчика события, использующего объектную модель InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9a377-131">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

