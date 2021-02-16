---
title: Сведения об основной сборке взаимодействия Microsoft Office InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007, основная сборка межсоедания,основная сборка interop InfoPath,PIAs [InfoPath 2007],primary interop assemblies [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Для поддержки создания решений InfoPath, которые используют языки управляемого кода, такие как Visual C# и Visual Basic, параметр поддержки программирования .NET в программе установки InfoPath устанавливает три сборки для межпрограммного использования.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310138"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Сведения об основной сборке взаимодействия Microsoft Office InfoPath

Приложение InfoPath построено как приложение модели COM, которое предоставляет свои программные интерфейсы для внешней автоматизации в качестве COM-интерфейсов. Для поддержки создания решений InfoPath, которые используют языки управляемого кода, такие как Visual C# и Visual Basic, параметр поддержки программирования **.NET** в программе установки InfoPath устанавливает три сборки для межпрограммного использования. Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET. 
  
Файлы для трех сборок взаимодействия, устанавливаемых InfoPath, имеют следующие имена:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
В этом разделе обсуждается объектная модель, доступная в сборке межсайтовой связи Microsoft.Office.Interop.InfoPath, которая используется исключительно для кода внешней автоматизации. Сведения о сборке Microsoft.Office.Interop.InfoPath.SemiTrust, которая используется исключительно для написания и запуска управляемого кода, который выполняется из шаблонов форм InfoPath (XSN), см. в [infoPath 2003 Compatible Object Models](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Важная информация об установке

По умолчанию программа установки InfoPath устанавливает сборку Microsoft.Office.Interop.InfoPath в глобальном кэше сборок (GAC), содержимое которой можно просмотреть из папки C:\Windows\Assembly (или в папке C:\Windows\assembly\GAC_MSIL при просмотре файловой системы напрямую). Эта сборка называется "основной сборкой Microsoft Office InfoPath" и часто используется вместе со сборкой Microsoft.Office.Interop.InfoPath.Xml, которая также устанавливается в GAC, для автоматизации приложения InfoPath из внешних приложений, которые используют управляемый код. Сведения о сборке Microsoft.Office.Interop.InfoPath.Xml см. в сведениях о [сборке XML-межпарамента InfoPath.](about-the-infopath-xml-interop-assembly.md)
  
Если сборка Microsoft.Office.Interop.InfoPath не отображается в GAC, следует подтвердить, что InfoPath установлен правильно. По умолчанию для параметра "Поддержка программирования **.NET"** в программе установки установлено значение **"Запускать** с моего компьютера", если перед запуском установки установлен распространяемый пакет .NET Framework 1.1, пакет SDK .NET Framework 1.1 или более поздней версии .NET Framework. Если эти сборки межпрограммного обеспечения недоступны на компьютере, необходимо подтвердить установку .NET Framework  1.1  или более поздней, а затем с помощью программ и компонентов панели управления изменить настройку, установив параметр поддержки программируемости **.NET** в области **Microsoft Office InfoPath** для запуска с моего **компьютера.**
  
Сведения о загрузке распространяемого приложения .NET Framework 1.1 см. в [.NET Framework 1.1 Redistributable.](https://www.microsoft.com/en-us/download/details.aspx?id=26)
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Пространство имен Microsoft.Office.Interop.InfoPath

Хотя процесс написания управляемого кода для данной задачи очень похож на выполнение той же задачи с использованием языка, например Visual Basic для приложений или JScript, объектная модель,  предоставленная при просмотре пространства имен **Microsoft.Office.Interop.InfoPath** из обозревателя объектов в Microsoft Visual Studio выглядит более сложной. Это необходимо, так как для взаимодействия с .NET Framework требуется COM-сервер для использования всех своих общедоступных интерфейсов, а также некоторых дополнительных конструкций, необходимых самой .NET Framework. Дополнительные сведения о том, как и почему объектная модель, которая представляется более сложной, см. в подразделе "Как COM-объекты представят управляемому коду" статьи "Объектные модели, совместимые [с InfoPath 2003".](../form-templates/infopath-2003-compatible-object-models.md) 
  
### <a name="using-intellisense"></a>Использование IntelliSense

В примерах этого раздела предполагается, что вы установили ссылки на сборки Microsoft.Office.Interop.InfoPath и Microsoft.Office.Interop.InfoPath.Xml сборки. Сведения о том, как установить ссылки и дополнительные примеры внешней автоматизации, см. в примерах и сценариях внешней [автоматизации.](external-automation-scenarios-and-examples.md)
  
Прежде чем использовать завершение IntelliSense Microsoft IntelliSense во внешнем коде автоматизации, необходимо создать объектную переменную для экземпляра класса [Application,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) как показано в следующей строке кода. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

После создания объектной переменной при введите имя переменной, за которой следует точка, отобразится список с участниками выбранного класса **Application.** 
  
Для работы с формой InfoPath объявите объектную переменную типа [XDocument,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) а затем инициализирует ее, открыв форму из коллекции [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) переменной объекта **Application,** как показано в следующей строке кода. 
  
```cs
XDocument myXDoc = myApp.XDocuments.Open(
    "c:\\temp\\Form1.xml",
    (int) XdDocumentVersionMode.xdFailOnVersionOlder);
```

```vb
Dim myXDoc As XDocument = myApp.XDocuments.Open( _
    "c:\\temp\\Form1.xml", _
    XdDocumentVersionMode.xdFailOnVersionOlder)
```

При IntelliSense переменной будет отображаться выпаданый список завершения для членов класса **XDocument,** за которым следует точка. 
  
Чтобы работать с содержимым документа XML для формы с помощью MSXML (MSXML), необходимо создать переменную типа [IXMLDOMDocument2,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) а затем использовать свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) класса **XDocument** для назначения модели объектов документа XML (DOM) формы этой переменной. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

При IntelliSense переменной, за которой следует точка, будет отображаться список завершения MSXML для членов класса **IXMLDOMDocument2.** 
  
### <a name="using-the-class-library-reference-documentation"></a>Использование ссылочной документации библиотеки классов

Организация справочной документации по библиотеке классов пространства имен [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) отражает отношения между интерфейсами классов и наследуемыми интерфейсами, которые они реализуют. 
  
Когда вы открываете раздел для интерфейса сокласса, например [Application,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) ссылка на члены интерфейса coclass, следующая за описанием интерфейса в начале раздела, отображает пустую тему. Чтобы отобразить список членов, реализуемых интерфейсом компонентного класса, необходимо открыть раздел для самого свежего интерфейса, наследуемого компонентным классом, и затем открыть таблицу его членов. Ссылка на унаследованный интерфейс располагается вначале раздела "Заметки" в главе, посвященной интерфейсу компонентного класса. 
  
При нажатии F1 в редакторе кода Visual Studio поведение аналогично, за исключением того, что участник, на котором вызывается справка F1, будет отображаться напрямую, так как обычно вы работаете с членами интерфейса. Однако тот факт, что элемент может быть реализован из интерфейса с контролем версий, может создать неопределенность при первом его появлении. Например, если ввести команду  `myXDocument.UI.Alert`, установить курсор на  `Alert` и нажать клавишу F1, отобразится раздел "UI2.Alert Method". Это объясняется тем, что метод **Alert** является реализацией члена интерфейса **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Передача необязательных параметров членам объектной модели InfoPath

Если член объектной модели InfoPath содержит необязательный параметр и значение этого параметра не задано, необходимо передать поле **Type.Missing** для этого параметра. Если не произвести передачу поля **Type.Missing**, когда его фактическое значение опущено, это может привести к ошибке построения. Это справедливо для кода, написанного на C# и Visual Basic. Например, метод [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) включает два необязательных параметра:  _varEndNode_ и  _varViewContext_. Строка кода, в которой не определены фактические значения для этих необязательных параметров, должна выглядеть так, как показано в следующих примерах.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>См. также

- [Сценарии и примеры автоматизации с использованием внешних решений](external-automation-scenarios-and-examples.md)

