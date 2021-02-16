---
title: Объектные модели, совместимые с InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, object model,InfoPath 2003-compatible object model,object models [InfoPath 2003], compatible with InfoPath 2007,object models [InfoPath 2007], InfoPath 2003 compatible
localization_priority: Normal
ms.assetid: e4511af6-d7e7-44ad-a50d-1b7ee04f8215
description: Приложение Microsoft InfoPath написано как приложение модели COM и предоставляет программируемые интерфейсы как для внешней автоматизации, так и для скриптов шаблонов форм в качестве COM-интерфейсов.
ms.openlocfilehash: f3351a0fee6e23de0785aa28b0970c6a90361f16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303523"
---
# <a name="infopath-2003-compatible-object-models"></a>Объектные модели, совместимые с InfoPath 2003

Приложение Microsoft InfoPath написано как приложение модели COM и предоставляет программируемые интерфейсы как для внешней автоматизации, так и для скриптов шаблонов форм в качестве COM-интерфейсов. Для поддержки создания решений InfoPath, использующих языки Visual C# и Visual Basic с управляемым кодом, программа установки InfoPath устанавливает три сборки взаимодействия. Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET. 
  
Файлы для трех сборок взаимодействия, устанавливаемых InfoPath, имеют следующие имена:
  
- Microsoft.Office.Interop.InfoPath.dll
    
- Microsoft.Office.Interop.InfoPath.SemiTrust.dll
    
- Microsoft.Office.Interop.InfoPath.Xml.dll
    
В этой теме описана объектная модель, предоставляемая через сборку взаимодействия Microsoft.Office.Interop.InfoPath.SemiTrust и используемая исключительно для написания и запуска бизнес-логики с управляемым кодом в рамках шаблонов форм InfoPath (XSN). 
  
Сведения о сборках Microsoft.Office.Interop.InfoPath и Microsoft.Office.Interop.InfoPath.Xml см. в документации по пространствам имен [Microsoft.Office.Interop.InfoPath](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.aspx) [иMicrosoft.Office.Interop.InfoPath.Xml.](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) 
  
## <a name="important-installation-information"></a>Важные сведения об установке

При **Стандартной** установке программа установки InfoPath по умолчанию устанавливает копии сборок Microsoft.Office.Interop.InfoPath.SemiTrust и Microsoft.Office.Interop.InfoPath.Xml в папку C:\Program Files\Microsoft Office\Office14. Сборки Microsoft.Office.Interop.InfoPath и Microsoft.Office.Interop.InfoPath.Xml также устанавливаются в глобальный кэш сборок (GAC), содержимое которого можно просмотреть в папке C:\Windows\Assembly. 
  
Если эти сборки не установлены, следует убедиться, что приложение Microsoft InfoPath было установлено правильно. Если перед запуском программы установки был установлен пакет .NET Framework 2.0 или более поздней версии, то параметр **Поддержка программирования .NET** в программе установки InfoPath устанавливается на значение **Запускать с моего компьютера** для **Стандартной** установки InfoPath. Если эти сборки взаимодействия недоступны на компьютере, то необходимо убедиться, что установлена платформа .NET Framework 2.0 или более поздней версии, а затем открыть окно **Установка и удаление программ** из **Панели управления** и установить для параметра **Поддержка программирования .NET** значение **Запускать с моего компьютера**.
  
Сведения о загрузке пакета .NET Framework 2.0 Redistributable см. в статье [.NET Framework 2.0 Redistributable](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=0856eacb-4362-4b0d-8edd-aab15c5e04f5).
  
## <a name="the-microsoftofficeinteropinfopathsemitrust-namespace"></a>Пространство имен Microsoft.Office.Interop.InfoPath.SemiTrust

До выпуска Microsoft Office InfoPath 2003 с пакетом обновления 1 и набора инструментов Microsoft Office InfoPath 2003 для Visual Studio® .NET вся программная логика для шаблонов форм InfoPath создавалась с помощью скриптов Microsoft JScript и Microsoft VBScript, написанных в среде разработки редактора скриптов Microsoft (MSE). Скрипт, написанный в MSE, интерпретировался во время выполнения и получал доступ к объектной модели COM, предоставляемой библиотекой динамической компоновки IPEDITOR.dll.
  
Для поддержки создания шаблонов форм, которые используют языки управляемого кода, такие как Visual C# и Visual Basic для программирования логики, в InfoPath добавлены функциональные возможности для размещения общей языковой цепи (CLR) и сборки межпрограммного управления Microsoft.Office.Interop.InfoPath.SemiTrust, чтобы обеспечить безопасное межпрограммное использование управляемого кода с объектной моделью COM, которая обеспечивается InfoPath. Сведения о модели безопасности, применяемой к шаблонам форм InfoPath с управляемым кодом, см. в сведениях о модели безопасности для шаблонов форм [с кодом.](about-the-security-model-for-form-templates-with-code.md) 
  
Хотя процедура написания управляемого кода для конкретной задачи в шаблоне формы InfoPath крайне похожа на выполнение аналогичной задачи программирования путем написания скрипта, объектная модель, совместимая с InfoPath 2003, предоставляемая при просмотре пространства имен **Microsoft.Office.Interop.InfoPath.SemiTrust** из **Обозревателя объектов** в наборе Visual Studio 2012 выглядит гораздо сложнее. Это объясняется тем, что технология взаимодействия .NET Framework, используемая для поддержки объектной модели, совместимой с InfoPath 2003, требует, чтобы COM-сервер представлял все свои открытые интерфейсы, а также некоторые дополнительные конструкции, необходимые для самой платформы .NET Framework. 
  
### <a name="how-com-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Как COM-объекты могут быть открыты для объектной модели, совместимой с InfoPath 2003

При работе непосредственно с COM-сервером на языках высокого уровня, таких как JScript, VBScript и Visual Basic (но не версии .NET языков Visual Basic и Visual C#) представляемая объектная модель проще, чем базовые классы и интерфейсы COM. Например, при работе с этими языками объект InfoPath **UI** предоставляет набор из семи методов, например метод **Alert** для отображения пользователям окна сообщения. 
  
Однако базовая конструкция COM, поддерживающая объект **UI**, в действительности состоит из трех компонентов: двух интерфейсов **UI** и **UI2**, а также компонентного класса COM, реализующего элементы этих двух интерфейсов. Существует две версии интерфейса **UI**, поскольку платформе COM требуется сохранять смешанное определение интерфейса для обеспечения обратной совместимости программ и компонентов, вызывающих реализацию этого интерфейса. 
  
В данном случае интерфейс **UI**, который был определен для исходной версии InfoPath, предоставляет четыре метода, включая метод **Alert**. Интерфейс **UI2** может считаться второй версией интерфейса **UI**, и он был определен для версии InfoPath с пакетом обновления 1. Интерфейс **UI2** наследует четыре метода исходного интерфейса **UI** и добавляет три новых метода, например метод **Confirm**. Хотя в рамках скрипта или управляемого кода можно написать строку кода, вызывающую метод **Confirm** с помощью  `XDocument.UI.Confirm`, но в действительности базовый код вызывает метод **Confirm** интерфейса **UI2** из реализации этого метода в компонентном классе COM. 
  
Объектная модель, которая предоставляется для скриптов, скрывает эти подробности, но сборка взаимодействия, которая требуется для работы с COM-сервером из управляемого кода, обеспечивает открытость компонентного класса и обоих интерфейсов. Для отдельного объекта **UI**, используемого в среде скриптов MSE, пространство имен **Microsoft.Office.Interop.InfoPath.SemiTrust** предоставляет следующие три элемента: 
  
- [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI.aspx) T:Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject 
    
- [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) T:Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject 
    
- Интерфейс компонентного класса [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) 
    
Хотя все три этих интерфейса предоставляются в **Обозревателе объектов** и содержатся в документации по библиотекам классов для пространства имен, работа осуществляется только с интерфейсом компонентного класса **UIObject**, который реализует объект **UI**, а также с элементами интерфейса **UI2**, который представляет собой наиболее актуальную версию интерфейса, реализованного интерфейсом компонентного класса **UIObject**. Чтобы получить доступ к интерфейсу компонентного класса **UIObject** из родительского объекта [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) аналогично доступу из скрипта, следует использовать метод доступа [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) . За исключением некоторых существенных деталей, эта схема применяется для всех объектов из исходной версии InfoPath, которые были обновлены при выпуске версии InfoPath с пакетом обновления 1 (SP1). 
  
Хотя в целом эта схема во всех случаях одинакова, но ситуация несколько проще для полностью новых объектов, которые были добавлены в пакете обновления 1 для InfoPath, например, для объекта **Certificate**. В этом случае следует учитывать только два компонента: интерфейс компонентного класса [CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) и элементы интерфейса [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Certificate.aspx) , представляющего собой наиболее актуальный и единственный интерфейс, реализованный интерфейсом компонентного класса **CertificateObject**. Как и при использовании COM-объектов InfoPath из скрипта, для доступа к объекту из родительского объекта используется метод доступа [Certificate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Certificate.aspx) . 
  
Эта же схема применяется к интерфейсам семейств, за исключением того, что к имени интерфейса компонентного класса для семейства добавляется слово "Collection", а не "Object". Например, интерфейс компонентного класса для семейства COM **DataAdapters** называется [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) , а интерфейс, реализующий его, называется [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdapters.aspx) . Аналогичным образом, для доступа к семейству используется метод доступа [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) родительского объекта **XDocument**. 
  
Из этой схемы именования существует три исключения. К именам интерфейсов компонентных классов для COM-объектов **Application** и **XDocument** не добавляется слово "Object". Их имена идентичны именам соответствующим COM-объектов: [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) и **XDocument**. Кроме того, к именам интерфейсов, реализованных интерфейсами компонентных классов **Application** и **XDocument**, добавляется префикс в виде символа подчеркивания (_): [_Application2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.aspx) и [_XDocument2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.aspx) . Третьим исключением является COM-объект **DataObject**. Интерфейс компонентного класса для этого объекта называется [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) , но, как и для других COM-объектов InfoPath, интерфейс, реализующий его, называется [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.aspx) . 
  
### <a name="how-microsoft-xml-core-services-msxml-50-for-microsoft-office-objects-are-exposed-to-the-infopath-2003-compatible-object-model"></a>Как MSXML (MSXML) 5.0 для Microsoft Office объектной модели, совместимой с InfoPath 2003

Подмножество объектов и элементов объектной модели, предоставляемых службами MSXML, которые также являются COM-сервером, реализуется интерфейсами, предоставляемыми сборкой взаимодействия Microsoft.Office.Interop.InfoPath.SemiTrust. Необходимость в этом обусловлена тем, что некоторые элементы объектной модели InfoPath COM основываются на MSXML и должны иметь возможность безопасного доступа к этим элементам. Имена интерфейсов в пространстве имен **Microsoft.Office.Interop.InfoPath.SemiTrust**, реализующем объекты и элементы объектной модели MSXML идентичны именам, предоставляемым COM-сервером MSXML. В большинстве случаев к этим именам добавляется префикс "IXMLDOM", поскольку они используются для работы с моделью XML DOM. Например, свойство [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) интерфейса **XDocument**, которое используется для возвращения ссылки на базовый XML-документ формы, возвращает интерфейс [IXMLDOMDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.IXMLDOMDocument.aspx) , который реализуется сборкой взаимодействия Microsoft.Office.Interop.InfoPath.SemiTrust. Вызов и использование элементов интерфейса **IXMLDOMDocument** осуществляется в целом аналогично использованию скрипта в шаблонах форм, не использующих управляемый код. 
  
Дополнительные сведения об использовании элементов объектной модели MSXML для Microsoft Office в шаблонах форм с управляемым кодом см. в статье [Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003](working-with-msxml-and-system-xml-using-the-infopath-2003-object-model.md).
  
### <a name="using-intellisense"></a>Использование IntelliSense

Как правило, при написании кода для шаблона формы с управляемым кодом, совместимым с InfoPath 2003, используются переменные  `thisXDocument` и  `thisApplication`, которые инициализируются в методе  `_Startup` файла классов по умолчанию FormCode.cs или FormCode.vb. Переменные  `thisXDocument` и  `thisApplication` можно использовать для доступа к элементам интерфейсов компонентных классов [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) и [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) . После того, как будет введено имя любой переменной с точкой в конце, автозавершение инструкции IntelliSense отобразит список элементов в соответствующем интерфейсе компонентного класса. Эту процедуру можно продолжить для получения доступа к элементу объектной модели, с которым требуется осуществить работу. 
  
Далее приведен простой пример с использованием переменной  `thisXDocument` для доступа к методу [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) с целью отображения версии приложения InfoPath с помощью свойства [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) , доступ к которому предоставляется из переменной  `thisApplication`. 
  
```cs
thisXDocument.UI.Alert(thisApplication.Version);
```

```vb
thisXDocument.UI.Alert(thisApplication.Version)
```

### <a name="using-the-class-library-reference-documentation"></a>Использование справочной документации по библиотеке классов

Организация ссылочной документации библиотеки классов пространства имен **Microsoft.Office.Interop.InfoPath.SemiTrust** отражает взаимоотношения между интерфейсами компонентных классов и унаследованными интерфейсами, которые они реализуют. Это описано в предыдущем разделе "Представление COM-объектов для управляемого кода" этой статьи. 
  
Хотя структура и именование в справочной документации по пространству имен **Microsoft.Office.Interop.InfoPath.SemiTrust** могут вначале показать запутанными, темы в целом упорядочены аналогично руководству по объектной модели InfoPath, которая входит в состав руководства разработчика InfoPath, включенного в приложение InfoPath. За исключением разделов, посвященных интерфейсам **Application** и **XDocument**, все разделы интерфейсов компонентных классов COM соответствуют эквивалентным разделам "Объект" и "Семейство" в ссылке на скрипты InfoPath. Например, темы "Интерфейс UIObject" и "Интерфейс WindowsCollection" в справочной документации по пространству имен **Microsoft.Office.Interop.InfoPath.SemiTrust** соответствует аналогичному содержимому в темах "Объект пользовательского интерфейса" и "Семейство Windows" справочного руководства по скриптам объектной модели InfoPath. 
  
Однако ссылка на членов интерфейса компонентного класса, следующая за описанием интерфейса в начале раздела, отображает пустой раздел. Чтобы отобразить список членов, реализуемых интерфейсом компонентного класса, необходимо открыть раздел для самого свежего интерфейса, наследуемого компонентным классом, и затем открыть таблицу его членов. Ссылка на унаследованный интерфейс располагается вначале раздела "Заметки" в главе, посвященной интерфейсу компонентного класса.
  
Если в редакторе кода нажать клавишу F1, то процедура будет аналогична, за исключением того, что элемент, по которому вызвана справка, будет отображен непосредственно, поскольку работа, как правило, осуществляется с элементами интерфейса. Однако тот факт, что элемент может быть реализован из интерфейса с контролем версий, может создать неопределенность при первом его появлении. Например, если ввести команду  `thisXDocument.UI.Alert`, установить курсор на  `Alert` и нажать клавишу F1, отобразится раздел "UI2.Alert Method". Это объясняется тем, что метод **Alert** является реализацией члена интерфейса **UI2**. 
  
### <a name="passing-optional-parameters-to-infopath-object-model-members"></a>Передача необязательных параметров членам объектной модели InfoPath

Если элемент объектной модели, совместимой с InfoPath 2003, содержит необязательный параметр, и значение этого параметра не указано, то вместо значения необходимо передать поле **Type.Missing**. Если не произвести передачу поля **Type.Missing**, когда его фактическое значение опущено, это может привести к ошибке построения. Это действительно для кода, написанного как на Visual C#, так и на Visual Basic. Например, метод [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) интерфейса [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) включает два необязательных параметра:  _varEndNode_ и  _varViewContext_. Строка кода, в которой не определены фактические значения для этих необязательных параметров, должна выглядеть так, как показано в следующих примерах.
  
```cs
IXMLDOMNode group1 = 
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1");
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing);
```

```vb
Dim group1 As IXMLDOMNode = _
   thisXDocument.DOM.selectSingleNode("/my:myFields/my:group1")
thisXDocument.View.SelectNodes(group1, Type.Missing, Type.Missing)
```

### <a name="about-common-language-specification-compliance"></a>О соответствии спецификаций общих языков

С точки зрения внутренней структуры каждый интерфейс и элемент в сборке Microsoft.Office.Interop.InfoPath.SemiTrust использует атрибут **CLSCompliant** со значением **false**. Поскольку справочная документация создается с использованием, в том числе, **System.Reflection**, то к описанию каждого интерфейса и элемента добавляется строка "Этот интерфейс (метод/свойство) несовместим с CLS". Однако фактически большинство интерфейсов и элементов пространства имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) совместимо с CLS. 
  
## <a name="see-also"></a>См. также

- [Типичные задачи по разработке шаблонов форм, использующих объектную модель InfoPath 2003](common-tasks-for-developing-form-templates-using-infopath-object-model.md)
- [О модели безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md)
- [Создание шаблонов форм с помощью объектной модели InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
- [Ознакомление с объектной моделью InfoPath 2003](understanding-the-infopath-2003-object-model.md)

