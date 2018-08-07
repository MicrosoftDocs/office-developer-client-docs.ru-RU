---
title: Программное управление форматами файлов Visio
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: ''
ms.openlocfilehash: 92ef2c084409dbe017951ff7dfdbf93839ff4b51
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813923"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a>Программное управление форматами файлов Visio

![Раздел "Инструкции"](media/mod_icon_howto.png)
  
Узнайте, как создать решение в Visual Studio 2012 для чтения пакет новых форматов файлов в Visio 2013, выберите части в пакете, изменить данные в части и добавьте новый части пакета.
  
|||
|:-----|:-----|
|**В этой статье** [Основы обработки формат файла Visio](#vis15_ManipulateFF_Essentials) [Создайте файл vsdx (en) и новое решение Visual Studio](#vis15_ManipulateFF_CreateFile) [Откройте файл Visio 2013 виде пакета](#vis15_ManipulateFF_OpenPackage) [Выберите и чтение части пакета из пакета](#vis15_ManipulateFF_SelectPart) [Выберите и изменения данных XML в часть пакета](#vis15_ManipulateFF_ChangeXML) [Пересчет данных в файле](#vis15_ManipulateFF_Recalculate) [Добавить новую часть пакета для пакета](#vis15_ManipulateFF_AddNewPart) [Благодарности](#vis15_ManipulateFF_Ackn) [Дополнительные материалы](#vis15_ManipulateFF_Additional)                                                                                         ||
   
## <a name="visio-file-format-manipulation-essentials"></a>Основы обработки формат файла Visio
<a name="vis15_ManipulateFF_Essentials"> </a>

Предыдущие версии Visio сохранения файлов в формате конфиденциальным двоичный файл (.vsd) или формата файла отдельного документа XML документа Visio (.vdx). Visio 2013 представлен новый формат файла (vsdx) (en, который основан на основе технологий XML и ZIP-архив. Как и в предыдущих версиях Visio файлы сохраняются в одном контейнере. В отличие от прежних версий файлов тем не менее, новый формат файла может быть открыт, чтение, обновлены, изменены и создании без Автоматизация приложения Visio 2013. Разработчики, знакомые с работа с XML или работа с использованием пространства имен [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) можно быстро начать работу с новый формат файла программными средствами. Разработчики, работавших с помощью формата XML документа Visio в предыдущих версиях можно найти, что многие из структур из этого формата были сохранены в новый формат файла. 
  
В этой статье мы рассмотрим работа с формат файлов Visio 2013 программным способом, с помощью Microsoft .NET Framework 4.5, C# или Visual Basic и Visual Studio 2012. Можно узнать, как открыть файла Visio 2013, выберите части документа в файле, изменить данные в частях и создания новой части документа.
  
> [!NOTE]
> Примеры кода в этой статье предполагается, что вы элементарные общее представление о классов в пространствах имен [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) и [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) . > В этой статье также предполагается, что вы понимаете принципы и терминологию Open Packaging Conventions. Вы должны знакомы с понятиями, пакеты, части документа или части пакета и связей. Дополнительные сведения можно [OPC: новый стандарт упаковки данных](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx). > Кода демонстрируется создание запросов LINQ (синтаксиса запроса), чтобы выбрать XML. Большая часть образцов кода используйте синтаксис запроса для построения запросов LINQ. Можно переопределить запросов LINQ, заданный в коде с помощью метода синтаксис LINQ, если это необходимо. Дополнительные сведения о синтаксиса запросов LINQ и синтаксис метода можно [LINQ синтаксис запроса или синтаксис метода (C#)](http://msdn.microsoft.com/en-us/library/bb397947.aspx)> в таблице 1 приведены основные темы, которые вы должны быть знакомы с перед началом работы над в этой статье. 
  
**В таблице 1. Основные понятия, которые для работы в формат файлов Visio 2013**

|**Название статьи**|**Описание**|
|:-----|:-----|
|[Общие сведения о формате файлов Visio (VSDX)](introduction-to-the-visio-file-formatvsdx.md) <br/> |Общий обзор описываются некоторые основные функции в формат файлов Visio 2013. Его описание Open Packaging Conventions (OPC) в качестве их применения в формат файлов Visio 2013. Также описываются различия между предыдущей формат файла XML документа Visio (.vdx) и формат файлов Visio 2013.  <br/> |
|[OPC: Новый стандарт упаковки данных](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx) <br/> |Журнал MSDN Magazine описаны Open Packaging Conventions качестве концепции.  <br/> |
|[Основные моменты спецификаций Open Packaging Conventions](http://msdn.microsoft.com/en-us/library/ee361919.aspx) <br/> [Введение в форматы файлов Office (2007) Open XML](http://msdn.microsoft.com/en-us/library/aa338205.aspx) <br/> |В этих двух статьях рассматривается применение Open Packaging Conventions для файлов Microsoft Office. Они содержат описания как связей в пакете и также включите несколько примеров кода.  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a>Создайте файл vsdx (en) и новое решение Visual Studio
<a name="vis15_ManipulateFF_CreateFile"> </a>

Перед началом работы через процедур, описанных в этой статье, вам необходимо создать файл Visio 2013, чтобы открыть и работы с ними. Документ, используемые в примерах кода в этой статье содержит одну страницу с двумя подключенными фигурами на нем, одну из фигур, выполняется на основе шаблона «Простая блок-схема» фигуры «Начала или окончания».
  
Используйте следующую процедуру для создания нового файла Visio 2013 для использования в оставшихся процедур, описанных в этой статье.
  
### <a name="to-create-new-file-in-visio-2013"></a>Создание нового файла в Visio 2013

1. Откройте Visio 2013.
    
2. Создайте новый документ, основанный на шаблоне Простая блок-схема, выбрав **КАТЕГОРИЙ**, **блок-схема**, **Простая блок-схема**, **Создание**.
    
3. В окне **фигуры** Перетащите фигуру **Начала или окончания** на полотно. 
    
4. Выберите новый Начальная или завершающая фигура на полотне и введите «Приступить к процессу».
    
5. В окне **фигуры** Перетащите фигуру **процесса** на полотно. 
    
6. Выберите новый процесс фигуры на полотне и введите «Выполнения некоторых задач».
    
7. В контекстном меню Начальная или завершающая фигура выберите **Добавить один соединитель на страницу**и затем рисовать соединитель между начала или окончания и процесс фигуры на полотно, как показано на рисунке 1.
    
    **На рисунке 1. Простой документ Visio 2013**
    
     ![Начальная или завершающая фигура, подключенная к фигуре процесса](media/vis15_SimpleFlowchart.png)
  
8. Сохраните файл на рабочем столе как файл vsdx (en), выбрав **файл**, **Сохранить как**, **компьютер**, **рабочий стол**.
    
    В диалоговом окне **Сохранить как** введите пакет Visio в поле **имя файла** »», выберите **документ Visio (\*vsdx (en))** в **Тип** списка, а затем нажмите кнопку **Сохранить** . 
    
9. Закройте файл и закройте Visio 2013.
    
> [!TIP]
> В некоторых случаях Visio открывает файл успешно даже в том случае, если существуют проблемы с файлом. При тестировании решения, работа с элементами управления файлов Visio на уровне файла пакета, чтобы гарантировать, что Visio уведомлением неполадок файла, следует включить предупреждения об открытии файлов. > Для включения предупреждения об открытии файлов, в Visio 2013, выберите **файл**, **Параметры**, **Дополнительно**. В разделе **Сохранить и открыть**установите флажок **Показывать предупреждения об открытии файлов**. 
  
Эти процедуры используют консольного приложения Windows для работы с файла «Visio Package.vsdx». Используйте следующую процедуру, чтобы создать и настроить новое консольное приложение Windows в Visual Studio 2012.
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a>Чтобы создать новое решение в Visual Studio 2012

1. В меню **Файл** выберите пункт **Создать**, затем **Проект**.
    
2. В диалоговом окне **Новый проект** разверните узел **Visual C#** или **Visual Basic**и затем выберите **Windows**, **Консольного приложения**.
    
    В поле **имя** введите «VisioFileAccessor», выберите расположение проекта и нажмите кнопку « **ОК** ». 
    
3. В меню **проект** выберите команду **Добавить ссылку**. 
    
    В диалоговом окне **Диспетчер ссылок** в разделе **сборки**выберите **Framework**и добавьте ссылку на них **System.Xml** и **WindowsBase** . 
    
4. В файле Program.cs или Module1.vb проекта добавьте следующие директивы **using** (инструкции**Imports** в Visual Basic): 
    
  ```cs
  using System.Xml;
  using System.Xml.Linq;
  using System.IO;
  using System.IO.Packaging;
  using System.Text;
  
  ```

  ```vb
  Imports System.Xml
  Imports System.Xml.Linq
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Text
  
  ```

5. Также в файле Program.cs или Module1.vb до конца **методе класса **Program** (**модуль1** в Visual Basic),** добавьте следующий код, который останавливает выполнение консольного приложения до пользователь нажимает клавишу. 
    
  ```cs
  // This code stops the execution of the console application
  // so you can read the output.
  Console.WriteLine("Press any key to continue ...");
  Console.ReadKey();
  
  ```

  ```vb
  ' This code stops the execution of the console application
  ' so you can read the output.
  Console.WriteLine("Press any key to continue ...")
  Console.ReadKey()
  ```

## <a name="open-a-visio-2013-file-as-a-package"></a>Откройте файл Visio 2013 виде пакета
<a name="vis15_ManipulateFF_OpenPackage"> </a>

Перед могут управлять любыми данных в файле, необходимо сначала открыть файл в объекте [пакета](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) , который содержится в пространстве имен [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) . Объект **пакета** представляет собой файл Visio в целом. Она предоставляет члены, которые позволяют выбирать отдельным компонентам в пакете. В частности класс **пакет** предоставляет статический метод [Open (String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) , которая используется для открытия файла в виде пакета. Он также предоставляет метод [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) для закрытия пакета после завершения работы с ним. 
  
> [!TIP]
> Рекомендуется **с помощью** блок можно используйте для открытия файла Visio в объекте **пакета** , чтобы не требуется явно закрыть пакет файлов после завершения с ним. Можно также в явном виде вызовите метод **Package.Close** в блоке **finally** конструкции **try/catch/finally** . 
  
Используйте следующий код, чтобы получить полный путь для файла «Visio Package.vsdx» с помощью объекта [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) , передайте путь как аргумент методу **Package.Open** и затем возвращает объект **пакета** вызывающий код. 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a>Чтобы открыть файл vsdx (en) в виде пакета

1. После метода **Main** в классе **программа** (или **модуль1** в Visual Basic) добавьте следующий код. 
    
  ```cs
  private static Package OpenPackage(string fileName, 
      Environment.SpecialFolder folder)
  {
      Package visioPackage = null;
      // Get a reference to the location 
      // where the Visio file is stored.
      string directoryPath = System.Environment.GetFolderPath(
          folder);
      DirectoryInfo dirInfo = new DirectoryInfo(directoryPath);
      // Get the Visio file from the location.
      FileInfo[] fileInfos = dirInfo.GetFiles(fileName);
      if (fileInfos.Count() > 0)
      {
          FileInfo fileInfo = fileInfos[0];
          string filePathName = fileInfo.FullName;
          // Open the Visio file as a package with
          // read/write file access.
          visioPackage = Package.Open(
              filePathName,
              FileMode.Open,
              FileAccess.ReadWrite);
          }
          // Return the Visio file as a package.
          return visioPackage;
  }
  ```

  ```vb
  Private Function OpenPackage(fileName As String, _
      folder As Environment.SpecialFolder) As Package
      Dim visioPackage As Package = Nothing
      ' Get a reference to the location
      ' where the Visio file is stored.
      Dim directoryPath As String = System.Environment.GetFolderPath( _
          folder)
      Dim dirInfo As DirectoryInfo = New DirectoryInfo(directoryPath)
      ' Get the Visio file from the location.
      Dim fileInfos As FileInfo() = dirInfo.GetFiles(fileName)
      If (fileInfos.Count() > 0) Then
          Dim fileInfo As FileInfo = fileInfos(0)
          Dim filePathName As String = fileInfo.FullName
          ' Open the Visio file as a package 
          ' with read/write access.
          visioPackage = Package.Open( _
              filePathName,
              FileMode.Open,
              FileAccess.ReadWrite)
          End If
      ' Return the Visio file as a package.
      Return visioPackage
  End Function
  
  ```

2. В **методе класса **программа** (или **модуль1** в Visual Basic)** добавьте следующий код. 
    
  ```cs
  // Open the Visio file in a Package object.
  using (Package visioPackage = OpenPackage("Visio Package.vsdx", 
      Environment.SpecialFolder.Desktop))
  {
  }
  
  ```

  ```vb
  ' Open the Visio file in a Package object.
  Using visioPackage As Package = OpenPackage("Visio Package.vsdx", _
      Environment.SpecialFolder.Desktop)
  End Using
  
  ```

## <a name="select-and-read-package-parts-from-a-package"></a>Выберите и чтение части пакета из пакета
<a name="vis15_ManipulateFF_SelectPart"> </a>

После получения файла Visio 2013 откройте как пакет можно получить доступ к части документа в ней с помощью класса [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) , включенные в пространстве имен **System.IO.Packaging** . Объекты **PackagePart** могут быть созданы по отдельности или в виде коллекции. Класс **пакета** предоставляет метод [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) и метод [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) для получения объектов **PackagePart** из **пакета**. Метод **Package.GetParts** возвращает экземпляр класса [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) , который вы может взаимодействовать с как семейства сайтов, который реализует [IEnumerator\<T\> ](https://msdn.microsoft.com/library/System.Collections.Generic.IEnumerator`1.aspx) интерфейса. 
  
Использовать код в следующей процедуре для получения объекта **PackagePartCollection** из **пакета** как семейство, выполните итерацию по **PackagePart** объектов в коллекции и записи URI и типа контента для каждого **PackagePart **на консоль. 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a>Выполнять итерацию по части пакета в пакете

1. После `OpenPackage` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий код. 
    
  ```cs
  private static void IteratePackageParts(Package filePackage)
  {
      
      // Get all of the package parts contained in the package
      // and then write the URI and content type of each one to the console.
      PackagePartCollection packageParts = filePackage.GetParts();
      foreach (PackagePart part in packageParts)
      {
          Console.WriteLine("Package part URI: {0}", part.Uri);
          Console.WriteLine("Content type: {0}", part.ContentType.ToString());
      }
  }
  
  ```

  ```vb
  Private Sub IteratePackageParts(filePackage As Package)
      ' Get all of the package parts contained in the package
      ' and then write the URI and content type of each one to the console.
      Dim packageParts As PackagePartCollection = filePackage.GetParts()
      For Each part In packageParts
          Console.WriteLine("Package part: {0}", part.Uri)
          Console.WriteLine("Content type: {0}", part.ContentType.ToString())
      Next
  End Sub 
  
  ```

2. Добавьте следующий код внутри блока **using** в **методе класса **программы** (блок **с помощью** метода **Main** в **модуль1** в Visual Basic)** : 
    
  ```cs
  // Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage);
  
  ```

  ```vb
  ' Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage)
  
  ```

3. Нажмите клавишу F5 для отладки решения. После завершения работы программы нажмите любую клавишу, чтобы выйти из.
    
Консольное приложение создает выходные данные (некоторые из выходных данных включен для краткости) следующего вида:
  
 `Package part URI: /docProps/app.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.extended-properties+xml`
  
 `Package part URI: /docProps/core.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.core-properties+xml`
  
 `Package part URI: /docProps/custom.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.custom-properties+xml`
  
 `Package part URI: /docProps/thumbnail.emv`
  
 `Content type: image/x-emf`
  
 `Package part URI: /visio/document.xml`
  
 `Content type: application/vnd.ms-visio.drawing.main+xml`
  
 `Package part URI: /visio/_rels/document.xml.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Package part URI: /_rels/.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Press any key to continue …`
  
Чаще необходимо выбрать один **PackagePart** без необходимости для итерации по всем из них. Объект **PackagePart** можно получить из **пакета** с помощью ее отношения с **пакета** или другой **PackagePart**. Связь в Visio 2013, файл имеет формат дискретные сущности, описывающий, как часть документа относится к пакет файлов или как две части документа относятся друг с другом. К примеру сам пакет файла Visio 2013 имеет связь с его части документа Visio и части документа Visio имеет связь с частью Windows. Эти связи, представленные в виде экземпляров классов [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) или [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) . 
  
Класс **пакета** предоставляет несколько методов для получения отношений, которые он содержит как **PackageRelationship** или **PackageRelationshipCollection** объектов. Метод [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) можно использовать для создания объекта **PackageRelationshipCollection** , которая содержит объекты **PackageRelationship** одного определенного типа. Конечно с помощью метода **Package.GetRelationshipsByType** необходимо знать уже тип отношения, который требуется. Отношения типов являются строками в формате пространство имен XML. Например, тип связи из части документа Visio будет http://schemas.microsoft.com/visio/2010/relationships/document. 
  
После определения отношения **PackagePart** в **пакете** или в другой **PackagePart** (то есть, у вас есть объект **PackageRelationship** , который ссылается на **PackagePart** , который будет), можно использовать его связь для получения идентификатора URI, **PackagePart**. Затем передайте URI в метод **Package.GetPart** для возврата **PackagePart**.
  
> [!NOTE]
> Также можно получить ссылку на определенных **PackagePart** с помощью метода **Package.GetPart** и URI **PackagePart**обхода на этапе, где получить пакет части связи. Тем не менее некоторые части пакета в пакете файла Visio можно сохранить для расположений, отличных от их расположения по умолчанию в пакете. Не удается предполагается, что часть пакета всегда расположена в каталоге же URI для каждого файла. > Вместо этого рекомендуется использовать для доступа к отдельным объектам **PackagePart** отношения. 
  
Используйте следующую процедуру для получения **PackagePart** (часть документа Visio) с помощью **PackageRelationship** из **пакета** , который ссылается на части. 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a>Для выбора часть пакета в пакете с помощью отношения

1. После `IteratePackageParts` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий метод. 
    
  ```cs
  private static PackagePart GetPackagePart(Package filePackage, 
      string relationship)
  {
      
      // Use the namespace that describes the relationship 
      // to get the relationship.
      PackageRelationship packageRel = 
          filePackage.GetRelationshipsByType(relationship).FirstOrDefault();
      PackagePart part = null;
      // If the Visio file package contains this type of relationship with 
      // one of its parts, return that part.
      if (packageRel != null)
      {
          // Clean up the URI using a helper class and then get the part.
          Uri docUri = PackUriHelper.ResolvePartUri(
              new Uri("/", UriKind.Relative), packageRel.TargetUri);
          part = filePackage.GetPart(docUri);
      }
      return part;
  }
  
  ```

  ```vb
  Private Function GetPackagePart(filePackage As Package, relationship As String) _
      As PackagePart
      ' Use the namespace that describes the relationship 
      ' to get the relationship.
      Dim packageRel As PackageRelationship = 
          filePackage.GetRelationshipsByType(relationship).FirstOrDefault()
      Dim part As PackagePart = Nothing
      ' If the Visio file package contains this type of relationship with 
      ' one of its parts, return that part.
      If Not IsNothing(packageRel) Then
          ' Clean up the URI using a helper class and then get the part.
          Dim docUri = PackUriHelper.ResolvePartUri( _
              New Uri("/", UriKind.Relative), packageRel.TargetUri)
          part = filePackage.GetPart(docUri)
      End If
      Return part
  End Function
  
  ```

2. Замените код в блоке **с помощью** метода **Main** класса **Program** (блок **с помощью** метода **Main** в **модуль1** в Visual Basic) следующий код. 
    
  ```cs
  // Get a reference to the Visio Document part contained in the file package.
  PackagePart documentPart = GetPackagePart(visioPackage, 
      "http://schemas.microsoft.com/visio/2010/relationships/document");
  
  ```

  ```vb
  ' Get a reference to the Visio Document part contained in the file package.
  Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
      "http://schemas.microsoft.com/visio/2010/relationships/document")
  
  ```

Как уже было сказано ранее, можно также получить **PackagePart** объектов с помощью отношения с другими объектами **PackagePart** . Это важно, поскольку для документа Visio любой сложности большинство объектов **PackagePart** нет отношения в **пакет**. К примеру отдельных часть содержимого страницы в пакет файлов (то есть, /visio/pages/page1.xml) имеет отношение части индекса страницы (то есть, /visio/pages/pages.xml), но не сам пакет файла. Если у вас нет точное URI отдельной страницы в пакете, можно использовать ее отношения с часть страницы индекса для получения ссылки на него.
  
Класс **PackagePart** предоставляет метод [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) , которые можно использовать для возврата объекта **PackageRelationshipCollection** , который содержит только один тип объекта **PackageRelationship** . При наличии **PackageRelationshipCollection**, вы можете выбрать **PackageRelationship** из коллекции и затем ссылаются на объект **PackagePart** . 
  
Используйте следующий код для получения **PackagePart** из **пакета** с помощью ее отношения к (получение объекта **PackageRelationship** из) другой **PackagePart**.
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a>Чтобы выбрать часть пакета через ее отношения с другой части пакета

1. После `GetPackagePart` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий метод перегрузка. 
    
  ```cs
  private static PackagePart GetPackagePart(Package filePackage, 
      PackagePart sourcePart, string relationship)
  {
      // This gets only the first PackagePart that shares the relationship
      // with the PackagePart passed in as an argument. You can modify the code
      // here to return a different PackageRelationship from the collection.
      PackageRelationship packageRel = 
          sourcePart.GetRelationshipsByType(relationship).FirstOrDefault();
      PackagePart relatedPart = null;
      if (packageRel != null)
      {
          // Use the PackUriHelper class to determine the URI of PackagePart
          // that has the specified relationship to the PackagePart passed in
          // as an argument.
          Uri partUri = PackUriHelper.ResolvePartUri(
              sourcePart.Uri, packageRel.TargetUri);
          relatedPart = filePackage.GetPart(partUri);
      }
      return relatedPart;
  }
  
  ```

  ```vb
  Private Function GetPackagePart(filePackage As Package, 
      sourcePart As PackagePart, relationship As String) As PackagePart
      ' This gets only the first PackagePart that shares the relationship
      ' with the PackagePart passed in as an argument. You can modify the
      ' code to return a different PackageRelationship from the collection.
      Dim packageRel As PackageRelationship = sourcePart. _
          GetRelationshipsByType(relationship).FirstOrDefault()
      Dim relatedPart As PackagePart = Nothing
      If Not IsNothing(packageRel) Then
          ' Use the PackUriHelper class to determine the URI of the 
          ' PackagePart that has the specified relationship to the 
          ' PackagePart passed in as an argument.
          Dim partUri As Uri = PackUriHelper.ResolvePartUri( _
              sourcePart.Uri, packageRel.TargetUri)
          relatedPart = filePackage.GetPart(partUri)
      End If
      Return relatedPart
  End Function
  ```

2. Добавьте следующий код в **с помощью** блок в методе **Main** **программы** класса (блок **Using** метода **Main** в **модуль1** в Visual Basic), под кодом на предыдущем шаге. (Не удаляйте код, добавленный в предыдущей процедуре). 
    
  ```cs
  // Get a reference to the collection of pages in the document, 
  // and then to the first page in the document.
  PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
      "http://schemas.microsoft.com/visio/2010/relationships/pages");
  PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
      "http://schemas.microsoft.com/visio/2010/relationships/page");
  
  ```

  ```vb
  ' Get a reference to the collection of pages in the document,
  ' and then to the first page in the document.
  Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
      "http://schemas.microsoft.com/visio/2010/relationships/pages") 
  Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
      "http://schemas.microsoft.com/visio/2010/relationships/page") 
  ```

Прежде чем принять изменения в файл XML, включенные в части документа, необходимо сначала загрузить документ XML в объект, который позволяет читать XML-код, с помощью класса [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) или [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) . Оба класса предоставляют методы для задач, таких как выбор элементов XML, содержащиеся в XML-документов; Создание, чтение и запись атрибутов; и вставка новые элементы XML в документ. 
  
Двух класс **XDocument** позволяет запроса XML, с помощью LINQ. С помощью LINQ можно легко выбрать отдельные элементы из XML-документа путем создания запросов, а не итерации всех элементов в коллекции и тестирование для элементов, которые необходимо. По этим причинам следующих процедур, описанных в этой статье используйте класс **XDocument** и другие классы пространства имен **System.Xml.Linq** для работы с XML. 
  
Используйте следующую процедуру, чтобы открыть **PackagePart** документ в формате XML в объект **XDocument** . 
  
### <a name="to-read-the-xml-in-a-package-part"></a>Чтение XML-кода в часть пакета

1. После последнего перегрузка для `GetPackagePart` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий метод. 
    
  ```cs
  private static XDocument GetXMLFromPart(PackagePart packagePart)
  {
      XDocument partXml = null;
      // Open the packagePart as a stream and then 
      // open the stream in an XDocument object.
      Stream partStream = packagePart.GetStream();
      partXml = XDocument.Load(partStream);
      return partXml;
  }
  ```

  ```vb
  Private Function GetXMLFromPart(packagePart As PackagePart) As XDocument
      Dim partXml As XDocument = Nothing
      ' Open the packagePart as a stream and then
      ' open the stream in an an XDocument object.
      Dim partStream As Stream = packagePart.GetStream()
      partXml = XDocument.Load(partStream)
      Return partXml
  End Function
  ```

2. Добавьте следующий код в **с помощью** блок в методе **Main** **программы** класса (блок **Using** метода **Main** в **модуль1** в Visual Basic), под кодом на предыдущем шаге. 
    
  ```cs
  // Open the XML from the Page Contents part.
  XDocument pageXML = GetXMLFromPart(pagePart);
  ```

  ```vb
  ' Open the XML from the Page Contents part.
  Dim pageXML As XDocument = GetXMLFromPart(pagePart)
  ```

## <a name="select-and-change-xml-data-in-a-package-part"></a>Выберите и изменения данных XML в часть пакета
<a name="vis15_ManipulateFF_ChangeXML"> </a>

После загрузки части документа в объект **XDocument** можно использовать LINQ для выбора XML-элементы и внести изменения в XML-документе. Можно изменить XML-данные, добавить или удалить данные и сохранить XML-документа в часть документа. 
  
Наиболее распространенные задачи для управления формат файла Visio Выбор коллекции элементов или определенные элементы XML в документе. Пространство имен **System.Xml.Linq** включает в себя класс [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) , который представляет элемент XML. Класс **XElement** обеспечивает доступ к данным, содержащиеся в файле Visio по детальный уровень, из отдельных элементов **фигуры** в элементах **значение** (например). 
  
Выберите элементы **фигуры** **XDocument** (содержащем часть содержимого страницы) и затем выберите определенный элемент **фигуры** , используйте приведенный ниже код. 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a>Для выбора конкретного элемента в части пакета

1. После `GetXMLFromPart` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий метод. 
    
  ```cs
  private static IEnumerable<XElement> GetXElementsByName(
      XDocument packagePart, string elementType)
  {
      // Construct a LINQ query that selects elements by their element type.
      IEnumerable<XElement> elements = 
          from element in packagePart.Descendants() 
          where element.Name.LocalName == elementType 
          select element;
      // Return the selected elements to the calling code.
      return elements.DefaultIfEmpty(null);
  }
  
  ```

  ```vb
  Private Function GetXElementsByName(partXML As XDocument, _
      elementType As String) As IEnumerable(Of XElement)
      ' Construct a LINQ query that selects elements by their element type.
      Dim elements As IEnumerable(Of XElement) =
          From element In partXML.Descendants()
          Where element.Name.LocalName = elementType
          Select element
      ' If there aren't any elements of the specified type
      ' in the document, return Nothing to the calling code.
      Return elements.DefaultIfEmpty(Nothing)
  End Function
  ```

2. После `GetXElementsByName` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод. 
    
  ```cs
  private static XElement GetXElementByAttribute(IEnumerable<XElement> elements,
      string attributeName, string attributeValue) 
  {
      // Construct a LINQ query that selects elements from a group
      // of elements by the value of a specific attribute.
      IEnumerable<XElement> selectedElements = 
          from el in elements
          where el.Attribute(attributeName).Value == attributeValue
          select el;
      // If there aren't any elements of the specified type
      // with the specified attribute value in the document,
      // return null to the calling code.
      return selectedElements.DefaultIfEmpty(null).FirstOrDefault();
  }
  ```

  ```vb
  Private Function GetXElementByAttribute(elements As IEnumerable(Of XElement), _
      attributeName As String, attributeValue As String) As XElement
      ' Construct a LINQ query that selects elements from a group
      ' of elements by the value of a specific attribute.
      Dim selectedElements As IEnumerable(Of XElement) =
          From el In elements
          Where el.Attribute(attributeName).Value = attributeValue
          Select el
      ' If there aren't any elements of the specified type 
      ' with the specified attribute value in the document,
      ' return Nothing to the calling code.
      Return selectedElements.DefaultIfEmpty(Nothing).FirstOrDefault()
  End Function
  
  ```

3. Добавьте следующий код в **с помощью** блок в методе **Main** **программы** класса (блок **Using** метода **Main** в **модуль1** в Visual Basic), под кодом на предыдущем шаге. 
    
  ```cs
  // Get all of the shapes from the page by getting
  // all of the Shape elements from the pageXML document.
  IEnumerable<XElement> shapesXML = GetXElementsByName(pageXML, "Shape");
  // Select a Shape element from the shapes on the page by 
  // its name. You can modify this code to select elements
  // by other attributes and their values.
  XElement startEndShapeXML = 
      GetXElementByAttribute(shapesXML, "NameU", "Start/End");
  
  ```

  ```vb
  ' Get all of the shapes from the page by getting
  ' all of the Shape elements from the pageXML document.
  Dim shapesXML As IEnumerable(Of XElement) = GetXElementsByName( _
      pageXML, "Shape")
  ' Select a Shape element from the shapes on the page by
  ' its name. You can modify this code to select elements
  ' by other attributes and their values.
  Dim startEndShapeXML As XElement = GetXElementByAttribute( _
      shapesXML, "NameU", "Start/End")
  ```

После стали ссылку на объект **XElement** , содержащихся в объект **XDocument** , можно управлять как XML-данных и, таким образом, измените данные, содержащиеся в файле Visio. Например если фигуры текст при открытии в Visio, соответствующих элементов **фигуры** будет содержать по крайней мере один элемент **текста** . Чтобы изменить значение этого элемента **текст** , текст фигуры изменяется при просмотре файла в Visio. 
  
Добавьте следующий код в **с помощью** блок в методе **Main** класса **программы** (блок **с помощью** метода **Main** в **модуль1** в Visual Basic) для изменения текста в Начальная или завершающая фигура из «Начать процесс» Чтобы «Запуск процесса». 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName = "Text"
                               select element;
XElement textElement = textElements.ElementAt(0);
// Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process");

```

```vb
' Query the XML for the shape to get the Text element, and
' return the first Text element node.
Dim textElements As IEnumerable(Of XElement) =
    From element In startEndShapeXML.Elements()
    Where element.Name.LocalName = "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> В предыдущем примере существующий текст фигуры и строку, используемую для замены его имеют такое же число символов. Также Обратите внимание на то, что запрос LINQ изменяется значение последнего дочернего узла возвращаемый элемент (который в этом случае является текстовым). Это позволяет избежать изменения параметров элемент **позиции символа** , который является дочерним элементом **текст** . > Можно привести к нестабильности файл, если изменить текст фигуры программным путем с помощью перезаписи все дочерние элементы элемента **текста** . Как показано в приведенном выше примере форматирование текста представлены элементы **позиции символа** в разделе **текст** элемента в файле. Определение форматирования хранится в **разделе** родительского элемента. Если эти два элемента данных несогласованности, затем файл может работать некорректно. Visio heals много несоответствия, но она лучше подходит для обеспечения согласованности ее изменения, чтобы вы управляете ultimate поведение файла. 
  
После внесения изменений в XML-код части документа эти изменения существует только в памяти. Для сохранения изменений в файле XML-код должен быть сохранен обратно в части документа.
  
Следующий код использует класс [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) и класс [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) для обратной записи XML для части пакета. Несмотря на то, что можно использовать метод [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) для сохранения XML в часть **XmlWriter** и **XmlWriterSettings** классы позволяют позволяет контролировать выходные данные, включая указание типа кодировки. Класс **XDocument** предоставляет метод [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) , который принимает объект **XmlWriter** и записывает XML потока. 
  
Используйте следующую процедуру, чтобы сохранить XML-код на странице Visio часть содержимого страницы.
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a>Чтобы сохранить измененный XML-код пакета

1. После `GetXElementByAttribute` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод. 
    
  ```cs
  private static void SaveXDocumentToPart(PackagePart packagePart, 
      XDocument partXML)
  {
      
      // Create a new XmlWriterSettings object to 
      // define the characteristics for the XmlWriter
      XmlWriterSettings partWriterSettings = new XmlWriterSettings();
      partWriterSettings.Encoding = Encoding.UTF8;
      // Create a new XmlWriter and then write the XML
      // back to the document part.
      XmlWriter partWriter = XmlWriter.Create(packagePart.GetStream(),
          partWriterSettings);
      partXML.WriteTo(partWriter);
      // Flush and close the XmlWriter.
      partWriter.Flush();
      partWriter.Close();
  }
  ```

  ```vb
  Private Sub SaveXDocumentToPart(packagePart As PackagePart, _
      partXML As XDocument)
      ' Create a new XmlWriterSettings object to 
      ' define the characteristics for the XmlWriter.
      Dim partWriterSettings As XmlWriterSettings = New XmlWriterSettings()
      partWriterSettings.Encoding = Encoding.UTF8
      ' Create a new XmlWriter and then write the XML
      ' back to the document part.
      Dim partWriter As XmlWriter = XmlWriter.Create(packagePart.GetStream())
      partXML.WriteTo(partWriter)
      ' Flush and close the XmlWriter.
      partWriter.Flush()
      partWriter.Close()
  End Sub
  ```

2. Добавьте следующий код в **с помощью** блок в методе **Main** **программы** класса (блок **Using** метода **Main** в **модуль1** в Visual Basic), под кодом на предыдущем шаге. 
    
  ```cs
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

3. Нажмите клавишу F5 для отладки решения. После завершения работы программы нажмите любую клавишу, чтобы выйти из.
    
4. Откройте файл Visio Package.vsdx в Visio 2013. 
    
Начальная или завершающая фигура теперь должен содержать текст «Пуск процесса».
  
## <a name="recalculate-data-in-the-file"></a>Пересчет данных в файле
<a name="vis15_ManipulateFF_Recalculate"> </a>

Некоторые изменения данных в файле может потребоваться Visio для пересчета документ при открытии файла. Visio предоставляет множество логику для схемы, особенно для отношения фигур (то есть, когда один фигуры зависит от другого) и подключение фигур. Если какие-либо данные, которая использует настраиваемой логики при изменении Visio необходимо распространить изменения ко всем затронутых вычисляемых данных в файле. 
  
Формат файлов Visio 2013 включает в себя несколько методов, которые можно использовать для пересчета данных в файле. Существует три типа из сценариев, которые необходимо учитывать при решить, нужно ли пересчитывать файла Visio и как это сделать.
  
- Изменения в данные не влияют на другие значения в формате файлов. Добавьте любые дополнительные инструкции для Visio для пересчета документа не требуется. Как было показано ранее, зачастую можно изменить текстом фигуры без необходимости пересчитывать документа.
    
- Изменения данных ограничен изменение значения ячейки таблицы свойств фигуры в XML-КОДЕ, и других значений таблицы свойств фигуры, которые зависят от этих данных. В этом случае необходимо добавить инструкции (с помощью класса [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) ) на элемент **ячейки** , были ли изменены XML. Например ячейки **ThemeIndex** фигуры влияет на значений нескольких таблиц свойств фигур ячеек, содержащихся в форме. При изменении ячейки **ThemeIndex** в файле (например, элемент **ячейки** со значением **N** «ThemeIndex»), необходимо будет добавьте инструкции обработки в элемент **ячейки** , чтобы обновить зависимых значений . 
    
- Изменения данных влияет на расположение соединитель или подключение точек. Другая ситуация — когда существует множество изменений в данные таблицы свойств фигуры и обновить всего документа с одной инструкции (а не Добавление инструкции по обработке отдельных для каждого изменения). В этом случае можно указать Visio для пересчета весь документ при открытии. Это делается путем добавления свойство **RecalcDocument** часть настраиваемых свойств файла (/ docProps/custom.xml) пакета Visio. Настройка положения или размера фигур на схеме подключенных приводится пример этого типа сценария. 
    
    Имейте в виду, что это наиболее высоких вариант с точки зрения производительности.
    
Используйте следующую процедуру для вставки элемент **ячейки** в элемент **фигуры** , где другие элементы **ячеек** этой же **формы** нужно перерасчете из-за новое значение. Новый элемент **ячейки** включает в себя инструкцией по обработке дочерний элемент для оповещения Visio, необходимые для выполнения некоторых локального пересчета. 
  
### <a name="to-recalculate-values-for-a-single-shape"></a>Для пересчета значений для отдельных фигур

1. Замените код из предыдущих двух примерах (изменение текста фигуры и вызов `SaveXDocumentToPart`) в блоке **с помощью** метода **Main** класса **Program** (блок **Using** метода **Main** в **модуль1** в Visual Basic) с помощью следующего кода. 
    
  ```cs
  // Insert a new Cell element in the Start/End shape that adds an arbitrary
  // local ThemeIndex value. This code assumes that the shape does not 
  // already have a local ThemeIndex cell.
  startEndShapeXML.Add(new XElement("Cell",
      new XAttribute("N", "ThemeIndex"),
      new XAttribute("V", "25"),
      new XProcessingInstruction("NewValue", "V")));
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Insert a new Cell element in the shape that adds an arbitrary local
  ' ThemeIndex value. This code assumes that the shape does not
  ' alrady have a local ThemeIndex cell.
  startEndShapeXML.Add(New XElement("Cell", _
      New XAttribute("N", "ThemeIndex"),
      New XAttribute("V", "25"),
      New XProcessingInstruction("NewValue", "V")))
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

2. Нажмите клавишу F5 для отладки решения. После завершения работы программы нажмите любую клавишу, чтобы выйти из.
    
3. Откройте файл Visio Package.vsdx в Visio 2013. Начальная или завершающая фигура теперь должен иметь разные заливки.
    
Цвет фигуры зависит от значения ячейки **ThemeIndex** — определяет, наследующий active тем фигуры. В предыдущем примере фигуры устанавливается наследование от другой темы (ячейки **ThemeIndex** задано значение «25»). Если не использовать команды обработки, цвет текста фигуры, которой также влияет ячейки **ThemeIndex** — не перерасчете. Изменить цвет заливки фигуры на технический, но останется белый текст, а текст не будут считываться. Кроме того без команды обработки, возможно, что Visio может обновляться фигуры в нужный момент, отправляемых из файла в нестабильном состоянии, где форматирования значения фигуры могут быть обновлены непредсказуемым образом. 
  
При изменении данных в файл, который требует Visio для пересчета документов (например, изменение положения подключенных фигур и, таким образом, принудительную соединителей для перенаправления), необходимо добавить пересчета инструкции в файле Visio. Инструкции по создается путем добавления элемента **Свойства** со значением атрибута **имя** «RecalcDocument» к XML-части настраиваемых свойств файла пакета файла Visio. Рекомендуется следует проверить часть настраиваемые свойства файла убедитесь, что инструкции «RecalcDocument» еще не зарегистрирован в файле. 
  
Используйте следующий код, чтобы изменить значение ячейки **PinY** Начальная или завершающая фигура в предыдущих примерах. Код выбирает элемент **ячейки** , который содержит данные ячейки **PinY** как объект **XElement** с помощью значения атрибута **N** . Затем код добавляет пересчета инструкции в настраиваемых свойств файла часть файла Visio. 
  
> [!NOTE]
> Этот код основан на `GetPackagePart` и `SaveXDocumentToPart` методы, созданные ранее. 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a>Для пересчета весь документ при открытии

1. После `SaveXDocumentToPart` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод. 
    
  ```cs
  private static void RecalcDocument(Package filePackage)
  {
      // Get the Custom File Properties part from the package and
      // and then extract the XML from it.
      PackagePart customPart = GetPackagePart(filePackage, 
          "http://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
          "custom-properties");
      XDocument customPartXML = GetXMLFromPart(customPart);
      // Check to see whether document recalculation has already been 
      // set for this document. If it hasn't, use the integer
      // value returned by CheckForRecalc as the property ID.
      int pidValue = CheckForRecalc(customPartXML);
      if (pidValue > -1)
      {
          XElement customPartRoot = customPartXML.Elements().ElementAt(0);
          // Two XML namespaces are needed to add XML data to this 
          // document. Here, we're using the GetNamespaceOfPrefix and 
          // GetDefaultNamespace methods to get the namespaces that 
          // we need. You can specify the exact strings for the 
          // namespaces, but that is not recommended.
          XNamespace customVTypesNS = customPartRoot.GetNamespaceOfPrefix("vt");
          XNamespace customPropsSchemaNS = customPartRoot.GetDefaultNamespace();
          // Construct the XML for the new property in the XDocument.Add method.
          // This ensures that the XNamespace objects will resolve properly, 
          // apply the correct prefix, and will not default to an empty namespace.
          customPartRoot.Add(
              new XElement(customPropsSchemaNS + "property",
                  new XAttribute("pid", pidValue.ToString()),
                  new XAttribute("name", "RecalcDocument"),
                  new XAttribute("fmtid", 
                      "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"),
                  new XElement(customVTypesNS + "bool", "true")
              ));
      }
      // Save the Custom Properties package part back to the package.
      SaveXDocumentToPart(customPart, customPartXML);
  }
  ```

  ```vb
  Private Sub RecalcDocument(filePackage As Package)
          ' Get the Custom File Properties part from the package and
          ' then extract the XML from it.
          Dim customPart As PackagePart = GetPackagePart(filePackage, _
              "http://schemas.openxmlformats.org/officeDocument/2006/" + _
              "relationships/custom-properties")
          Dim customPartXML As XDocument = GetXMLFromPart(customPart)
          ' Check to see whether document recalculation has already been
          ' set for this document. If it hasn't, use the integer
          ' value returned by CheckForRecalc as the property ID.
          Dim pidValue As Integer = CheckForRecalc(customPartXML)
          If (pidValue > 1) Then
              Dim customPartRoot As XElement = _
                  customPartXML.Elements().ElementAt(0)
              ' Two XML namespaces are needed to add XML data to this 
              ' document. Here, we're using the GetNamespaceOfPrefix and
              ' GetDefaultNamespace methods to get the namespaces that
              ' we need. You can specify the exact strings for the 
              ' namespaces, but that is not recommended.
              Dim customVTypesNS As XNamespace = _
                  customPartRoot.GetNamespaceOfPrefix("vt")
              Dim customPropsSchemaNS As XNamespace = _
                  customPartRoot.GetDefaultNamespace()
              ' Contruct the XML for the new property in the XDocument.Add
              ' method. This ensures that the XML namespaces resolve 
              ' properly, apply the correct prefix, and do not default to 
              ' an empty namespace.
              customPartRoot.Add( _
                  New XElement(customPropsSchemaNS + "property", _
                      New XAttribute("pid", pidValue.ToString()), _
                      New XAttribute("name", "RecalcDocument"), _
                      New XAttribute("fmtid", _
                          "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"), _
                      New XElement(customVTypesNS + "bool", "true") _
              ))
          ' Save the Custom Properties package part back to the package.
          SaveXDocumentToPart(customPart, customPartXML)
          End If
      End Sub
  ```

2. После `RecalcDocument` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод. 
    
  ```cs
  private static int CheckForRecalc(XDocument customPropsXDoc) 
  {
      
      // Set the inital pidValue to -1, which is not an allowed value.
      // The calling code tests to see whether the pidValue is 
      // greater than -1.
      int pidValue = -1;
      // Get all of the property elements from the document. 
      IEnumerable<XElement> props = GetXElementsByName(
          customPropsXDoc, "property");
      // Get the RecalcDocument property from the document if it exists already.
      XElement recalcProp = GetXElementByAttribute(props, 
          "name", "RecalcDocument");
      // If there is already a RecalcDocument instruction in the 
      // Custom File Properties part, then we don't need to add another one. 
      // Otherwise, we need to create a unique pid value.
      if (recalcProp != null)
      {
          return pidValue;
      }
      else
      {
          // Get all of the pid values of the property elements and then
          // convert the IEnumerable object into an array.
          IEnumerable<string> propIDs = 
              from prop in props
              where prop.Name.LocalName == "property"
              select prop.Attribute("pid").Value;
          string[] propIDArray = propIDs.ToArray();
          // Increment this id value until a unique value is found.
          // This starts at 2, because 0 and 1 are not valid pid values.
          int id = 2;
          while (pidValue == -1)
          {
              if (propIDArray.Contains(id.ToString()))
              {
                  id++;
              }
              else
              {
                  pidValue = id;
              }
          }
      }
      return pidValue;
  }
  
  ```

  ```vb
  Private Function CheckForRecalc(customPropsXDoc As XDocument) As Integer
      ' Set the initial pidValue to -1, which is not an allowed value. 
      ' The calling code test to see whether the pidValue is
      ' greater than -1.
      Dim pidValue As Integer = -1
      ' Get all of the property elements from the document.
      Dim props As IEnumerable(Of XElement) = GetXElementsByName( _
          customPropsXDoc, "property")
      ' Get the RecalcDocument property from the document if 
      ' it exists already.
      Dim recalcProp As XElement = GetXElementByAttribute(props, _
          "name", "RecalcDocument")
      ' If there is already a RecalcDocument instruction in the 
      ' Custom File Properties part, then we don't need another one.
      ' Otherwise, we need to create a unique pid value.
      If Not IsNothing(recalcProp) Then
          Return pidValue
      Else
          ' Get all of the pid values of the proeprty elements and then
          ' convert the IEnumerable object into an array.
          Dim propIDs As IEnumerable(Of String) = _
          From prop In props
          Where prop.Name.LocalName = "property"
          Select prop.Attribute("pid").Value
          Dim propIDArray As String() = propIDs.ToArray()
          ' Increment this id value until a unique value is found.
          ' This starts at 2, because 0 and 1 are not valid pid values.
          Dim id As Integer = 2
          While (pidValue = -1)
              If (propIDArray.Contains(id.ToString())) Then
                  id = id + 1
              Else
                  pidValue = id
              End If
          End While
      End If
      Return pidValue
  End Function
  ```

3. Замените код из предыдущего примера в блоке **с помощью** метода **Main** класса **Program** (блок **Using** метода **Main** в **модуль1** в Visual Basic), с помощью следующего кода. 
    
  ```cs
  // Change the shape's horizontal position on the page 
  // by getting a reference to the Cell element for the PinY 
  // ShapeSheet cell and changing the value of its V attribute.
  XElement pinYCellXML = GetXElementByAttribute(
      startEndShapeXML.Elements(), "N", "PinY");
  pinYCellXML.SetAttributeValue("V", "2");
  // Add instructions to Visio to recalculate the entire document
  // when it is next opened.
  RecalcDocument(visioPackage);
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Change the shape's horizontal position on the page
  ' by getting a reference to the Cell element for the PinY
  ' ShapeSheet cell and changing the value of its V attribute.
  Dim pinYCellXML As XElement = GetXElementByAttribute(
      startEndShapeXML.Elements(), "N", "PinY")
  pinYCellXML.SetAttributeValue("V", "2")
  ' Add instructions to Visio to recalculate the entire document
  ' when it is next opened.
  RecalcDocument(visioPackage)
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

4. Нажмите клавишу F5 для отладки решения. После завершения работы программы нажмите любую клавишу, чтобы выйти из.
    
5. Откройте файл Visio Package.vsdx в Visio 2013. 
    
Начальная или завершающая фигура теперь должна появиться 2 дюйма от верхней границы документа. Соединитель между Начальная или завершающая фигура и форма процесс должен пересылаются внесения изменений в макет. Если свойство **RecalcDocument** еще не добавлена в файл, положения фигуры будут изменены, но соединитель не будет иметь переадресован в новом расположении фигуры. 
  
## <a name="add-a-new-package-part-to-a-package"></a>Добавьте новую часть пакета для пакета
<a name="vis15_ManipulateFF_AddNewPart"> </a>

Одним из наиболее распространенных сценариев для изменения файла пакета Добавление новой части документа в пакет. Например если вы хотите добавить страницу документа путем добавления контента в пакет Visio, необходимо добавить часть содержимого страницы в пакет. 
  
Процесс добавления новой части пакета осуществляется просто: 
  
1. Создание XML-документа с данными для **PackagePart**. Необходимо уделить особое внимание пространства имен XML, управляющие схемы для конкретного типа XML-документа, создаваемого.
    
2. Создайте новый файл для XML-код и сохраните файл в расположение, в **пакет**.
    
3. Создайте необходимые связи между новой **PackagePart** и **пакет** или другие объекты **PackagePart** . 
    
4. Обновите все существующие части, которые должны ссылаться на новую часть. Например при добавлении новой части содержимого страницы (новая страница) для файла также потребуется обновить часть страницы индекса (/visio/pages/pages.xml-файл) правильные сведения о новой страницы.
    
Используйте следующую процедуру, чтобы создать новую часть расширяемость ленты в файле Visio. Добавляет новую часть расширяемость ленты новую вкладку с одной группой, содержащий одну кнопку ленты.
  
### <a name="to-create-a-new-package-part"></a>Чтобы создать новую часть пакета

1. После `CheckForRecalc` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод. 
    
  ```cs
  private static XDocument CreateCustomUI()
  {
      // Add a new Custom User Interface document part to the package.
      // This code adds a new CUSTOM tab to the ribbon for this
      // document. The tab has one group that contains one button.
      XNamespace customUINS = 
          "http://schemas.microsoft.com/office/2006/01/customui";
      XDocument customUIXDoc = new XDocument(
          new XDeclaration("1.0", "utf-8", "true"),
          new XElement(customUINS + "customUI",
              new XElement(customUINS + "ribbon",
                  new XElement(customUINS + "tabs",
                      new XElement(customUINS + "tab",
                          new XAttribute("id", "customTab"),
                          new XAttribute("label", "CUSTOM"),
                          new XElement(customUINS + "group",
                              new XAttribute("id", "customGroup"),
                              new XAttribute("label", "Custom Group"),
                              new XElement(customUINS + "button",
                                  new XAttribute("id", "customButton"),
                                  new XAttribute("label", "Custom Button"),
                                  new XAttribute("size", "large"),
                                  new XAttribute("imageMso", "HappyFace")
                              )
                          )
                      )
                  )
              )
          )
      );
      return customUIXDoc;
  }
  ```

  ```vb
  Private Function CreateCustomUI() As XDocument
      ' Add a new Custom User Interface document part to the package.
      ' This code adds a new CUSTOM tab to the ribbon for this
      ' document. The tab has one group that contains one button.
      Dim customUINS As XNamespace = _
          "http://schemas.microsoft.com/office/2006/01/customui"
      Dim customUIXML = New XDocument( _
          New XDeclaration("1.0", "utf-8", "true"), _
          New XElement(customUINS + "customUI", _
              New XElement(customUINS + "ribbon",
                  New XElement(customUINS + "tabs",
                      New XElement(customUINS + "tab",
                          New XAttribute("id", "customTab"),
                          New XAttribute("label", "CUSTOM"),
                          New XElement(customUINS + "group",
                              New XAttribute("id", "customGroup"),
                              New XAttribute("label", "Custom Group"),
                              New XElement(customUINS + "button",
                                  New XAttribute("id", "customButton"),
                                  New XAttribute("label", "Custom Button"),
                                  New XAttribute("size", "large"),
                                  New XAttribute("imageMso", "HappyFace")
                              )
                          )
                      )
                  )
              )
          )
      )
      Return customUIXML
  End Function
  ```

2. После `CreateCustomUI` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод. 
    
  ```cs
  private static void CreateNewPackagePart(Package filePackage, 
      XDocument partXML, Uri packageLocation, string contentType, 
      string relationship)
  {
      // Need to check first to see whether the part exists already.
      if (!filePackage.PartExists(packageLocation))
      {
          // Create a new blank package part at the specified URI 
          // of the specified content type.
          PackagePart newPackagePart = filePackage.CreatePart(packageLocation,
              contentType);
          // Create a stream from the package part and save the 
          // XML document to the package part.
          using (Stream partStream = newPackagePart.GetStream(FileMode.Create,
              FileAccess.ReadWrite))
          {
              partXML.Save(partStream);
          }
      }
      // Add a relationship from the file package to this
      // package part. You can also create relationships
      // between an existing package part and a new part.
      filePackage.CreateRelationship(packageLocation,
          TargetMode.Internal,
          relationship);
  }
  ```

  ```vb
  Private Sub CreateNewPackagePart(filePackage As Package, _
      partXML As XDocument, packageLocation As Uri, contentType As String, _
      relationship As String)
      ' Need to check first to see whether the part exists already.
      If Not (filePackage.PartExists(packageLocation)) Then
          ' Create a new blank package part at the specified URI
          ' of the specified content type.
          Dim newPart As PackagePart = filePackage.CreatePart(packageLocation, _
              contentType)
          ' Create a stream from the package part and save the
          ' XML document to the package part.
          Using partStream As Stream = newPart.GetStream(FileMode.Create, _
              FileAccess.ReadWrite)
              partXML.Save(partStream)
          End Using
          ' Add a relationship from the file package to this
          ' package part. You can also create relationships
          ' between an existing package part and a new part.
          filePackage.CreateRelationship(packageLocation, _
              TargetMode.Internal, relationship)
      End If
  End Sub
  ```

3. Замените весь код в **с помощью** блокировки в **методе класса **программы** (блок **Using** метода **Main** в **модуль1** в Visual Basic),** с помощью следующего кода. 
    
  ```cs
  // Create a new Ribbon Extensibility part and add it to the file.
  XDocument customUIXML = CreateCustomUI();
  CreateNewPackagePart(visioPackage, customUIXML, 
      new Uri("/customUI/customUI1.xml", UriKind.Relative),
      "application/xml",
      "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
  ```

  ```vb
  ' Create a new Ribbon Extensibility part and add it to the file.
  Dim customUIXML As XDocument = CreateCustomUI()
  CreateNewPackagePart(visioPackage, customUIXML, _
      New Uri("/customUI/customUI1.xml", UriKind.Relative), _
      "application/xml", _
      "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
  ```

4. Нажмите клавишу F5 для отладки решения. После завершения работы программы нажмите любую клавишу, чтобы выйти из.
    
5. Откройте файл Visio Package.vsdx в Visio 2013 и затем выберите вкладку **НАСТРАИВАЕМЫЕ** . 
    
Настраиваемая лента похожа на рисунке 2 при открытии файла в Visio 2013.
  
 **На рисунке 2. Настраиваемая вкладка на ленте Visio 2013**
  
![Настраиваемая вкладка на ленте](media/vis15_CustomRibbonTab.PNG)
  
XML-код, созданный с `CreateCustomUI` метод выглядит следующим образом. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="http://schemas.microsoft.com/office/2006/01/customui">
  <ribbon>
    <tabs>
      <tab id="customTab" label="CUSTOM">
        <group id="customGroup" label="Custom Group">
          <button id="customButton" label="Custom Button" size="large"
              imageMso="HappyFace" />
        </group>
      </tab>
    </tabs>
  </ribbon>
</customUI>
```

## <a name="acknowledgements"></a>Благодарности
<a name="vis15_ManipulateFF_Ackn"> </a>

Мы хотим высказать распознает вклад и ввода Visio со статусом MVP **Al Edlund** при создании примеров кода, содержащихся в данной технической статье. Al является распознанный expert управления формат файла Visio, включая формат XML документа Visio (.vdx) и новый формат файла Visio (vsdx (en). Al создал проектов, изучите программными средствами в новые форматы файлов Visio и предоставляет структуры внутри. 
  
Дополнительные сведения о всех режимов могли работать с формат файла Visio воспользуйтесь ссылками в разделе Дополнительные ресурсы, исходя из.
  
## <a name="see-also"></a>См. также
<a name="vis15_ManipulateFF_Additional"> </a>

- С Al Edlund:
    
  - проект [pkgVisio - Visio 2013 XML выполнение различных операций](http://pkgvisio.codeplex.com/documentation) на сайте CodePlex. 
    
  - [pkgVisio_pt1](http://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) видео на YouTube. 
    
  - [pkgVisio_pt2](http://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) видео на YouTube. 
    
- [Центр по разработке для Visio](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [Работа с документами форматов Office Open XML](http://msdn.microsoft.com/en-us/library/aa982683%28v=office.12%29.aspx)
    
- [Создание документа с пространствами имен (C#) (LINQ to XML)](http://msdn.microsoft.com/en-us/library/bb387075.aspx)
    
- [Добавление пользовательской XML-части в документ без запуска Microsoft Office](http://msdn.microsoft.com/en-us/library/bb608597%28VS.90%29.aspx)
    

