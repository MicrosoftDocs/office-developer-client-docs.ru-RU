---
title: Сведения об основной сборке взаимодействия Microsoft Office InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2007, основная сборка интеропов, основная сборка интероп-групп InfoPath,PIAs [InfoPath 2007], первичные сборки интеропов [InfoPath 2007]
localization_priority: Normal
ms.assetid: 1b3ae03c-6951-49e4-a489-4712d3f7ba72
description: Для поддержки создания решений InfoPath, которые используют языки управляемого кода, такие как Visual C# и Visual Basic, в программе установки InfoPath параметр .NET Programmability устанавливает три сборки межоперативов.
ms.openlocfilehash: 51773ad46b1371c410c4249e13a489f0c5550cd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310138"
---
# <a name="about-the-microsoft-office-infopath-primary-interop-assembly"></a>Сведения об основной сборке взаимодействия Microsoft Office InfoPath

Приложение InfoPath построено как приложение Component Object Model (COM), которое предоставляет свои интерфейсы программируемости для внешней автоматизации в качестве интерфейсов COM. Для поддержки создания решений InfoPath, которые используют языки управляемого кода, такие как Visual C# и Visual Basic, параметр поддержки программируемости **.NET** в программе установки InfoPath устанавливает три сборки интеропопов. Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET. 
  
Файлы для трех сборок взаимодействия, устанавливаемых InfoPath, имеют следующие имена:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
В этом разделе обсуждается объектная модель, выставленная через Microsoft. Office.Interop.InfoPath сборка, которая используется исключительно для внешнего кода автоматизации. Сведения о Microsoft. Office.Interop.InfoPath.SemiTrust, которая используется исключительно для записи и запуска управляемого кода, который выполняется из шаблонов форм InfoPath (.xsn), см. в материале [InfoPath 2003 Compatible Object Models](https://msdn.microsoft.com/library/e4511af6-d7e7-44ad-a50d-1b7ee04f8215%28Office.15%29.aspx).
  
## <a name="important-installation-information"></a>Важная информация об установке

Параметр установки по умолчанию программы установки InfoPath устанавливает Microsoft. Office.Interop.InfoPath в кэше глобальной сборки (GAC), содержимое которой можно просмотреть из папки C:\Windows\Assembly (или в C:\Windows\assembly\GAC_MSIL при непосредственном просмотре файловой системы). Эта сборка называется "сборкой Microsoft Office InfoPath Primary Interop" и часто используется совместно с сборкой Microsoft.Office.Interop.InfoPath.Xml, которая также установлена в GAC, для автоматизации приложения InfoPath из внешних приложений, которые используют управляемый код. Сведения о сборке Microsoft.Office.Interop.InfoPath.Xml см. в сайте [InfoPath XML Interop Assembly](about-the-infopath-xml-interop-assembly.md).
  
Если Microsoft. Office.Interop.InfoPath сборка не отображается в GAC, необходимо подтвердить правильность установки InfoPath. По умолчанию параметр **.NET Programmability Support** в программе  установки должен запускаться с моего компьютера до тех пор, пока перед запуском установки устанавливается платформа .NET Framework 1.1, платформа .NET Framework 1.1 Комплект разработки программного обеспечения (SDK) или более поздний вариант платформа .NET Framework. Если эти сборки не доступны на компьютере, необходимо подтвердить, что установлен платформа .NET Framework 1.1  или более поздней  стадии, а затем с помощью программ и функций панели управления изменить установку, установив параметр **.NET Programmability Support** в **Microsoft Office InfoPath** для запуска с моего компьютера **.**
  
Сведения о загрузке платформа .NET Framework 1.1 Redistributable см. в платформа .NET Framework [1.1.](https://www.microsoft.com/en-us/download/details.aspx?id=26)
  
## <a name="the-microsoftofficeinteropinfopath-namespace"></a>The Microsoft. Office.Interop.InfoPath Namespace

Хотя процесс написания управляемого кода для данной задачи очень похож на выполнение одной задачи с использованием языка, например Visual Basic для приложений или JScript, объектная модель, выставленная при просмотре пространства имен **Microsoft.Office.Interop.InfoPath** из браузера объектов в Microsoft Visual Studio, выглядит более сложной.  Это потому, что для взаимодействия с сервером платформа .NET Framework com-сервер должен выставлять все его общедоступные интерфейсы, а также некоторые дополнительные конструкции, необходимые самому платформа .NET Framework. Дополнительные сведения о том, как и почему объектная модель, подвергаемая сборке интеропов, выглядит более сложной, см. в разделе "Как объекты COM подвергаются управляемому коду" в разделе [InfoPath 2003 Compatible Object Models.](../form-templates/infopath-2003-compatible-object-models.md) 
  
### <a name="using-intellisense"></a>Использование IntelliSense

В примерах этого раздела предполагается, что вы установили ссылки на Microsoft. Office.Interop.InfoPath и Microsoft.Office.Interop.InfoPath.Xml сборки. Сведения о том, как устанавливать ссылки и дополнительные примеры внешней автоматизации, см. в статьи Внешние сценарии автоматизации [и примеры.](external-automation-scenarios-and-examples.md)
  
Прежде чем использовать microsoft IntelliSense в коде внешней автоматизации, необходимо создать переменную [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) объекта для экземпляра класса Application, как показано в следующей строке кода. 
  
```cs
Application myApp = 
    new Microsoft.Office.Interop.InfoPath.Application();
```

```vb
Dim myApp As Application = _
    New Microsoft.Office.Interop.InfoPath.Application()
```

После создания переменной объекта при введите имя переменной, за которым следует период,  будет отображаться отображимый список с выбранными участниками класса Приложения. 
  
Чтобы работать с формой InfoPath, объявите объектную переменную типа [XDocument,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocument.aspx) а затем инициализируете ее, открыв форму из коллекции [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.XDocuments.aspx) переменной объекта **Приложения,** как показано в следующей строке кода. 
  
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

Список IntelliSense для участников **класса XDocument** будет отображаться при введите имя переменной, за которой следует период. 
  
Чтобы работать с содержимым документа XML для формы с помощью MSXML (MSXML), необходимо создать переменную типа [IXMLDOMDocument2,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Xml.IXMLDOMDocument2.aspx) а затем использовать свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._XDocument2.DOM.aspx) класса **XDocument** для назначения объектной модели XML документа (DOM) формы к этой переменной. 
  
```cs
IXMLDOMDocument2 doc= myXDoc.DOM as IXMLDOMDocument2;
```

```vb
Dim doc As IXMLDOMDocument2 = myXDoc.DOM
```

Список IntelliSense для участников класса **IXMLDOMDocument2** будет отображаться при введите имя переменной, за которой следует период, который позволяет использовать MSXML для работы с документом XML. 
  
### <a name="using-the-class-library-reference-documentation"></a>Использование ссылочной документации библиотеки классов

Организация справочной документации по библиотеке имен [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.aspx) отражает связи между интерфейсами coclass и наследуемыми интерфейсами, которые они реализуют. 
  
При открываемой теме для интерфейса coclass, например [Application,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.Application.aspx) ссылка на членов интерфейса coclass, следующая за описанием интерфейса в начале темы, отображает пустую тему. Чтобы отобразить список членов, реализуемых интерфейсом компонентного класса, необходимо открыть раздел для самого свежего интерфейса, наследуемого компонентным классом, и затем открыть таблицу его членов. Ссылка на унаследованный интерфейс располагается вначале раздела "Заметки" в главе, посвященной интерфейсу компонентного класса. 
  
При нажатии F1 в редакторе Visual Studio Code аналогичное поведение, за исключением того, что член, на который вы вызываете справку F1, будет отображаться непосредственно, так как обычно вы работаете с участниками интерфейса. Однако тот факт, что элемент может быть реализован из интерфейса с контролем версий, может создать неопределенность при первом его появлении. Например, если ввести команду  `myXDocument.UI.Alert`, установить курсор на  `Alert` и нажать клавишу F1, отобразится раздел "UI2.Alert Method". Это объясняется тем, что метод **Alert** является реализацией члена интерфейса **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Передача необязательных параметров членам объектной модели InfoPath

Если член объектной модели InfoPath содержит необязательный параметр и не указывает значение для этого параметра, необходимо передать поле **Type.Missing** для этого параметра. Если не произвести передачу поля **Type.Missing**, когда его фактическое значение опущено, это может привести к ошибке построения. Это относится к коду, записанного в C# и Visual Basic. Например, метод [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.View2.SelectNodes.aspx) интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ViewObject.aspx) включает два необязательных параметра:  _varEndNode_ и  _varViewContext_. Строка кода, в которой не определены фактические значения для этих необязательных параметров, должна выглядеть так, как показано в следующих примерах.
  
```cs
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
myXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

## <a name="see-also"></a>См. также

- [Сценарии и примеры автоматизации с использованием внешних решений](external-automation-scenarios-and-examples.md)

