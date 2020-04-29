---
title: Сведения об основной сборке взаимодействия Microsoft Office InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2007, основная сборка взаимодействия, основная сборка взаимодействия InfoPath, PIA [InfoPath 2007], основные сборки взаимодействия [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Для поддержки создания решений InfoPath, использующих языки с управляемым кодом, такие как Visual C# и Visual Basic, параметр Поддержка программирования .NET в программе установки InfoPath устанавливает три сборки взаимодействия.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310138"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Сведения об основной сборке взаимодействия Microsoft Office InfoPath

Приложение InfoPath создается как приложение модели компонентных объектов (COM), которое предоставляет интерфейсы программирования для внешней автоматизации как интерфейсы COM. Для поддержки создания решений InfoPath, использующих языки с управляемым кодом, такие как Visual C# и Visual Basic, параметр **Поддержка программирования .NET** в программе установки InfoPath устанавливает три сборки взаимодействия. Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET. 
  
Файлы для трех сборок взаимодействия, устанавливаемых InfoPath, имеют следующие имена:
  
- Microsoft. Office. Interop. InfoPath. dll
    
- Microsoft. Office. Interop. InfoPath. SemiTrust. dll
    
- Microsoft. Office. Interop. InfoPath. XML. dll
    
В этом разделе рассматривается объектная модель, доступная через сборку взаимодействия Microsoft. Office. Interop. InfoPath, которая используется исключительно для внешнего кода автоматизации. Для получения сведений о сборке Microsoft. Office. Interop. InfoPath. SemiTrust, которая используется исключительно для написания и выполнения управляемого кода, который выполняется в шаблонах форм InfoPath (XSN), ознакомьтесь с [объектными моделями infopath 2003, совместимыми с infopath](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Важная информация об установке

Параметр установки по умолчанию для программы установки InfoPath устанавливает сборку Microsoft. Office. Interop. InfoPath в глобальном кэше сборок (GAC), содержимое которого можно просмотреть из папки C:\WINDOWS\assembly. (или в К:\виндовс\ассембли\ GAC_MSIL при непосредственном просмотре файловой системы). Эта сборка называется "основной сборкой взаимодействия Microsoft Office InfoPath" и часто используется вместе с сборкой Microsoft. Office. Interop. InfoPath. XML, которая также установлена в глобальном кэше сборок, для автоматизации приложения InfoPath из внешних приложений, использующих управляемый код. Для получения сведений о сборке Microsoft. Office. Interop. InfoPath. XML ознакомьтесь со статьей [о сборке взаимодействия InfoPath в InfoPath](about-the-infopath-xml-interop-assembly.md).
  
Если сборка Microsoft. Office. Interop. InfoPath не отображается в глобальном кэше сборок, убедитесь, что приложение InfoPath установлено правильно. По умолчанию параметр **поддержки программирования .NET** в программе установки настроен на **Запуск с моего компьютера** при условии, что распространяемый пакет .NET Framework 1,1, пакет средств разработки .NET Framework 1,1 или более поздней версии .NET Framework установлен перед запуском программы установки. Если эти сборки взаимодействия недоступны на вашем компьютере, необходимо убедиться, что установлено приложение .NET Framework 1,1 или более поздней версии, а затем использовать **программы и компоненты** из **панели управления** для изменения настроек с помощью параметра **поддержки программирования .NET** в разделе **Microsoft Office InfoPath** для **запуска с моего компьютера**.
  
Сведения о загрузке распространяемого пакета .NET Framework 1,1 можно найти в разделе [распространяемый пакет .NET framework 1,1](https://www.microsoft.com/en-us/download/details.aspx?id=26).
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>Пространство имен Microsoft. Office. Interop. InfoPath

Несмотря на то, что процесс написания управляемого кода для конкретной задачи очень похож на выполнение той же задачи с помощью языка Visual Basic для приложений или JScript, объектная модель, доступная при просмотре пространства имен **Microsoft. Office. Interop. InfoPath** из **обозревателя объектов** в Microsoft Visual Studio, выглядит более сложной. Это связано с тем, что для взаимодействия с .NET Framework требуется сервер COM для предоставления доступа ко всем общедоступным интерфейсам, а также некоторые дополнительные конструкции, необходимые для .NET Framework. Для получения дополнительных сведений о том, как и почему объектная модель, предоставляемая сборкой взаимодействия, становится более сложной, ознакомьтесь с разделом "как объекты COM представлены в управляемом коде" статьи, посвященной [объектной модели, совместимой с InfoPath 2003](../form-templates/infopath-2003-compatible-object-models.md) . 
  
### <a name="using-intellisense"></a>Использование IntelliSense

В примерах, приведенных в этом разделе, предполагается, что вы установили ссылки на сборки Microsoft. Office. Interop. InfoPath и Microsoft. Office. Interop. InfoPath. XML. Сведения о том, как задать ссылки и дополнительные примеры внешней автоматизации, можно найти в статье [Внешние сценарии автоматизации и примеры](external-automation-scenarios-and-examples.md).
  
Прежде чем можно будет использовать функцию завершения операторов Microsoft IntelliSense в внешнем коде автоматизации, необходимо создать объектную переменную для экземпляра класса [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , как показано в следующей строке кода. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

После создания объектной переменной при вводе имени переменной, за которым следует точка, отображается раскрывающийся список с элементами класса **приложения** , которые необходимо выбрать. 
  
Для работы с формой InfoPath объявите объектную переменную типа [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) , а затем инициализируйте ее, открыв форму из коллекции [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) объекта объекта **Application** , как показано в следующей строке кода. 
  
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

Раскрывающийся список завершения операторов IntelliSense для членов класса **XDocument** будет отображаться при вводе имени переменной, за которой следует точка. 
  
Чтобы работать с содержимым базового XML-документа для формы с использованием служб MSXML (MSXML), необходимо создать переменную типа [IXMLDOMDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) , а затем использовать свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) класса **XDocument** , чтобы назначить объектную модель документа XML (DOM) формы для этой переменной. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

Раскрывающийся список завершения операторов IntelliSense для членов класса **IXMLDOMDocument2** будет отображаться при вводе имени переменной, за которой следует точка, что позволит использовать MSXML для работы с XML-документом. 
  
### <a name="using-the-class-library-reference-documentation"></a>Использование ссылочной документации библиотеки классов

Структура справочной документации по библиотеке классов пространства имен [Microsoft. Office. Interop. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) отражает отношения между интерфейсами coclass и наследуемыми ими унаследованными интерфейсами. 
  
При открытии раздела для интерфейса компонентного класса, такого как [приложение](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) , ссылка на элементы интерфейса компонентного класса, приведенного в начале раздела, содержит пустой раздел. Чтобы отобразить список членов, реализуемых интерфейсом компонентного класса, необходимо открыть раздел для самого свежего интерфейса, наследуемого компонентным классом, и затем открыть таблицу его членов. Ссылка на унаследованный интерфейс располагается вначале раздела "Заметки" в главе, посвященной интерфейсу компонентного класса. 
  
При нажатии клавиши F1 в редакторе кода Visual Studio поведение аналогично, за исключением того, что член, для которого вызывается Справка F1, будет отображаться напрямую, так как чаще всего работает работа с членами интерфейса. Однако тот факт, что элемент может быть реализован из интерфейса с контролем версий, может создать неопределенность при первом его появлении. Например, если ввести команду  `myXDocument.UI.Alert`, установить курсор на  `Alert` и нажать клавишу F1, отобразится раздел "UI2.Alert Method". Это объясняется тем, что метод **Alert** является реализацией члена интерфейса **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Передача необязательных параметров членам объектной модели InfoPath

Если элемент объектной модели InfoPath содержит необязательный параметр, а значение этого параметра не указано, необходимо передать **тип. отсутствует** поле для этого параметра. Если не произвести передачу поля **Type.Missing**, когда его фактическое значение опущено, это может привести к ошибке построения. Это справедливо для кода, написанного на языках C# и Visual Basic. Например, метод [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) включает два необязательных параметра:  _varEndNode_ и  _varViewContext_. Строка кода, в которой не определены фактические значения для этих необязательных параметров, должна выглядеть так, как показано в следующих примерах.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>См. также

- [Сценарии и примеры автоматизации с использованием внешних решений](external-automation-scenarios-and-examples.md)

