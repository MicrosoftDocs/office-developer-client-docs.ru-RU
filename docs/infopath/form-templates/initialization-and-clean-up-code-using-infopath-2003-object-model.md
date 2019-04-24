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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299744"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a>Инициализация и очистка кода с помощью объектной модели InfoPath 2003

По умолчанию файл FormCode.cs или FormCode.vb, который создается для проекта шаблона формы, совместимого с InfoPath 2003, содержит полный исходный код для программирования логики формы. Шаблон проекта создает класс в файле FormCode.cs или FormCode.vb, схожий с классами, приведенными в указанных далее примерах, где можно указать инициализацию и очистку кода, а также обработчики для событий формы. Файлы FormCode.cs и FormCode.vb применяют атрибут уровня сборки **System.ComponentModel.DescriptionAttribute**, который идентифицирует класс в качестве единственного класса, где реализуются обработчики событий. Атрибут **InfoPathNamespace** (который реализуется типом [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) ) применяется к классу для идентификации пространств имен выборки XML DOM, используемых в рамках класса. Пространства имен, указанные в **InfoPathNamespace**, обслуживаются системой проектов InfoPath. 
  
Класс FormCode непосредственно предоставляет методы  `_Startup` и  `_Shutdown`, которые используются для выполнения процедур инициализации и очистки любых компонентов, которые требуются в дополнение к стандартным возможностям InfoPath во время открытия формы. 
  
> [!IMPORTANT]
> [!Важно!] Не вызывайте элементы объектной модели InfoPath из методов  `_Startup` и  `_Shutdown`. В этих методах следует выполнять инициализацию и вызов только элементов внешних компонентов. 
  
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

## <a name="the-startup-method"></a>Метод _Startup

Помимо предоставления области для написания кода инициализации дополнительных компонентов, метод  `_Startup` инициализирует переменные  `thisXDocument` и  `thisApplication`, которые можно использовать в коде формы для доступа к элементам классов [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) и [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) в объектной модели InfoPath. Код, необходимый для инициализации этих двух переменных, автоматически создается шаблоном проекта. 
  
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

В следующих примерах демонстрируется простой обработчик событий для кнопки, использующей переменную  `thisXDocument` для доступа к методу [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) типа [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) . 
  
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

Сведения о том, как создать обработчик событий, можно найти в статье [Добавление обработчика событий с помощью объектНой модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="the-shutdown-method"></a>Метод _ShutDown

Метод  `_Shutdown` является последним методом, вызываемым при закрытии формы. В этом методе можно написать любой код, необходимый для очистки и завершения компонентов, используемых в форме. 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a>Пример кода инициализации и очистки

В следующем примере демонстрируется инициализация подключения к базе данных Microsoft SQL Server в методе  `_Startup` и закрытие подключения в методе  `_Shutdown`. Чтобы этот пример работал правильно, необходимо сначала указать ссылку на сборку System.Data для платформы .NET Framework, выбрав пункт **Добавить ссылку** в меню **Проект**, а затем выбрать компонент System.Data.dll на вкладке **.NET**. Кроме того, обратите внимание, что в верхней части файла кода формы добавлена директива  `using System.Data.SqlClient` (или  `Imports System.Data.SqlClient)` для уменьшения числа нажатий клавиш. 
  
> [!NOTE]
> Пользователям формы InfoPath, содержащей код формы для подключения к базе данных SQL Server, могут потребоваться разрешения безопасности, зависящие от метода развертывания формы и определения политики безопасности. Дополнительные сведения о безопасности см. в статье [модель безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md) и [Настройка параметров безопасности для шаблонов форм с кодом](how-to-configure-security-settings-for-form-templates-with-code.md). 
  
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

## <a name="see-also"></a>См. также



[Добавление обработчика событий с помощью объектной модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

