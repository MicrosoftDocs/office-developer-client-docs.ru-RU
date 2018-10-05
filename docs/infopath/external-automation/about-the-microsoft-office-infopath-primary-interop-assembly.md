---
title: Сведения об основной сборке взаимодействия Microsoft Office InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, основной сборки взаимодействия основной сборке взаимодействия InfoPath, основные сборки взаимодействия [InfoPath 2007] основных сборок взаимодействия [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Для поддержки создания решений InfoPath, использующих языки управляемого кода, например Visual C# и Visual Basic, параметр поддержка программирования .NET в программе установки InfoPath устанавливает трех сборок взаимодействия.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393357"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Сведения об основной сборке взаимодействия Microsoft Office InfoPath

Как приложение модели компонентных объектов (COM), который предоставляет его интерфейсы программирования для внешней автоматизации COM-интерфейсами создается приложение InfoPath. Для поддержки создания решений InfoPath, использующих языки управляемого кода, например Visual C# и Visual Basic, параметр **Поддержка программирования .NET** в программе установки InfoPath устанавливает трех сборок взаимодействия. Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET. 
  
Файлы для трех сборок взаимодействия, устанавливаемых InfoPath, имеют следующие имена:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
В этом разделе описана объектная модель, предоставляемые посредством сборки взаимодействия Microsoft.Office.Interop.InfoPath, который используется только для кода внешней автоматизации. Сведения о сборки Microsoft.Office.Interop.InfoPath.SemiTrust, используемый исключительно для написания и выполнения управляемого кода, который выполняется от в шаблонах форм InfoPath (XSN-), видеть [InfoPath 2003 совместимой объектных моделей](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Важная информация об установке

Вариант установки по умолчанию в программе установки InfoPath устанавливает Microsoft.Office.Interop.InfoPath сборку в глобальный кэш сборок (GAC), в содержимое которой можно просматривать в папке C:\Windows\Assembly (или в C:\Windows\assembly\GAC_ MSIL при просмотре в файловой системе напрямую). Эта сборка называется «Microsoft Office InfoPath основной сборки взаимодействия» и часто используется в сочетании с Microsoft.Office.Interop.InfoPath.Xml сборки, который устанавливается в глобальный кэш СБОРОК, для автоматизации приложения InfoPath из внешних приложений, использующих управляемый код. Для получения сведений о сборке, Microsoft.Office.Interop.InfoPath.Xml разделе [О InfoPath XML сборки взаимодействия](about-the-infopath-xml-interop-assembly.md).
  
Microsoft.Office.Interop.InfoPath сборка не отображается в глобальном кэше СБОРОК, следует убедиться, что InfoPath был установлен правильно. По умолчанию **Поддержка программирования .NET** в программе установки включен режим **запускать с моего компьютера** , если распространяемый пакет .NET Framework 1.1, .NET Framework 1.1 Software Development Kit (SDK) или более поздней версии .NET Framework установлен перед запуском программы установки. Если эти сборки взаимодействия недоступны на вашем компьютере, необходимо подтвердить установки .NET Framework 1.1 или более поздней версии и затем использовать **программы и компоненты** **Панели управления** для изменения программы установки, задав **программирования .NET Поддержка** в узле **Microsoft Office InfoPath** , чтобы **запускать с моего компьютера**.
  
Сведения о загрузке распространяемый пакет .NET Framework 1.1 можно [1.1 распространяемый пакет .NET Framework](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Пространство имен Microsoft.Office.Interop.InfoPath

Несмотря на то, что процесс написания управляемого кода для указанных задач очень похоже на использовании языка, например Visual Basic для приложений или JScript, объектной модели, предоставляемые при просмотре **Microsoft.Office.Interop.InfoPath** задачу для выполнения пространство имен из **Обозревателя объектов** в Microsoft Visual Studio выполняет более сложных. Это, так как для взаимодействия с помощью .NET Framework требуется COM-сервера для предоставления из общедоступных интерфейсов, а также некоторые дополнительные конструкции, необходимые для .NET Framework. Дополнительные сведения о как и почему объектной модели, предоставляемые элементом сборки взаимодействия отображается более сложных см раздел «Как COM объекты будут доступны для управляемого кода» в разделе [InfoPath 2003 совместимой объектных моделей](../form-templates/infopath-2003-compatible-object-models.md) . 
  
### <a name="using-intellisense"></a>Использование IntelliSense

Примеров, описанных в этом разделе предполагается, что установки ссылки на сборки Microsoft.Office.Interop.InfoPath и Microsoft.Office.Interop.InfoPath.Xml. Сведения о том, как задать справочные материалы и примеры дополнительных внешней автоматизации видеть [внешней автоматизации сценарии и примеры](external-automation-scenarios-and-examples.md).
  
До завершения инструкций Microsoft можно использовать в коде внешней автоматизации, необходимо создать объектную переменную для экземпляра класса [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , как показано в следующей строке кода. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

После создания объектной переменной, при введите имя переменной, а затем за период с членами класса **приложения** для выбора отображается раскрывающийся список. 
  
Для работы с формой InfoPath, объявите объектную переменную типа [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) и его инициализация путем открытия формы из коллекции [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) объектной переменной **приложения** , как показано в следующей строке кода. 
  
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

При вводе имени переменной, а затем за период, отображается список раскрывающийся список завершения оператора IntelliSense для членов класса **XDocument** . 
  
Для работы с содержимым основной XML-документ формы, с помощью Microsoft XML Core Services (MSXML), необходимо создать переменную типа [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) и затем используйте свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) класса **XDocument** назначение XML Документ объектной модели (DOM) формы для этой переменной. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

Список раскрывающийся список завершения оператора IntelliSense для членов класса **IXMLDOMDocument2** отображается при вводе имени переменной, следуют периода, который позволяет использовать MSXML для работы с XML-документа. 
  
### <a name="using-the-class-library-reference-documentation"></a>Использование ссылочной документации библиотеки классов

Организация пространства имен [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) ссылочной документации библиотеки классов отражает отношения между интерфейсах и унаследованные интерфейсы, которые реализуют. 
  
При открытии раздела интерфейс компонентного класса, такие как [приложения](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , ссылки на элементы интерфейса компонентного класса, выполнив описание интерфейса в начале раздел отображает пустой раздел. Чтобы отобразить список членов, реализуемых интерфейсом компонентного класса, необходимо открыть раздел для самого свежего интерфейса, наследуемого компонентным классом, и затем открыть таблицу его членов. Ссылка на унаследованный интерфейс располагается вначале раздела "Заметки" в главе, посвященной интерфейсу компонентного класса. 
  
При нажатии клавиши F1 в редакторе кода Visual Studio, поведение аналогична за исключением того, что участник, на котором вызова справки F1 будет отображаться напрямую, так как вы работаете с члены интерфейса чаще всего. Однако тот факт, что элемент может быть реализован из интерфейса с контролем версий, может создать неопределенность при первом его появлении. Например, если ввести команду  `myXDocument.UI.Alert`, установить курсор на  `Alert` и нажать клавишу F1, отобразится раздел "UI2.Alert Method". Это объясняется тем, что метод **Alert** является реализацией члена интерфейса **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Передача необязательных параметров членам объектной модели InfoPath

Если не указать значение для параметра член объектной модели InfoPath содержит необязательный параметр, необходимо передать **Type.Missing** поля для этого параметра. Если не произвести передачу поля **Type.Missing**, когда его фактическое значение опущено, это может привести к ошибке построения. Это характерно для кода, написанного на языках C# и Visual Basic. Например, метод [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) включает два необязательных параметра:  _varEndNode_ и  _varViewContext_. Строка кода, в которой не определены фактические значения для этих необязательных параметров, должна выглядеть так, как показано в следующих примерах.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>См. также

- [Сценарии внешней автоматизации и примеры](external-automation-scenarios-and-examples.md)

