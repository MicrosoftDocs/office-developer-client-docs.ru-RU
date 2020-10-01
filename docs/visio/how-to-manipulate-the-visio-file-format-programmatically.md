---
title: Программное управление форматами файлов Visio
manager: lindalu
ms.date: 04/17/2019
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Создайте в Visual Studio 2012 решение для чтения пакетов с новым форматом файлов, используемым в Visio 2013, выбора частей в пакете, изменения данных в части и добавления новых частей в пакет.
localization_priority: Priority
ms.openlocfilehash: 7103e094f58ee26ea2335d6cccd822dced1e1375
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293515"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a>Программное управление форматами файлов Visio

![Раздел "Инструкции"](media/mod_icon_howto.png)
  
Узнайте, как в Visual Studio 2012 создать решение для чтения пакетов с новым форматом файлов, используемым в Visio 2013, выбора частей в пакете, изменения данных в части и добавления новых частей в пакет.
   
## <a name="visio-file-format-manipulation-essentials"></a>Основные сведения об управлении форматами файлов Visio
<a name="vis15_ManipulateFF_Essentials"> </a>

Приложения Visio предыдущих версий сохраняли файлы в защищенном двоичном формате (VSD) или в однодокументном формате XML-данных документа Visio (VDX). В Visio 2013 появился новый формат файлов (VSDX), который основан на XML и технологии архивирования ZIP. Как и в предыдущих версиях Visio, файлы сохраняются в одном контейнере. В отличие от файлов, сохраненных в прежних версиях Visio, файлы нового формата можно открывать, читать, обновлять, изменять и создавать без автоматизации приложения Visio 2013. Разработчики, которые умеют управлять XML или работать с пространством имен [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8), могут быстро приступить к программному управлению файлами нового формата. Разработчики, которые уже работали с форматом XML-данных документа Visio в предыдущих версиях приложения, обнаружат, что многие структуры этого формата перенесены в новый формат. 
  
В этой статье мы расскажем, как программно работать с форматом файлов Visio 2013 с использованием Microsoft .NET Framework 4.5, C# или Visual Basic, а также Visual Studio 2012. Вы узнаете, как открыть файл Visio 2013, выбрать части документа в файле, изменить данные в частях и создать часть документа.
  
> [!NOTE]
> В примерах кода в этой статье предполагается, что у вас есть элементарное понимание классов в пространствах имен [System.Xml.Linq](https://docs.microsoft.com/dotnet/api/system.xml.linq?view=netframework-4.8) и [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8). > В этой статье также предполагается, что вы знаете основные понятия и терминологию Open Packaging Conventions. Вы должны быть знакомы с основными понятиями о пакетах, частях документов или частях пакетов, а также о связях. Дополнительные сведения см. в статье [OPC: новый стандарт упаковки данных](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data). > В коде показано, как создавать запросы LINQ для выбора XML. В большей части примеров кода для создания запросов LINQ используется синтаксис запросов. При необходимости вы можете изменить любой из имеющихся в коде запросов LINQ, используя синтаксис методов LINQ. Дополнительные сведения о синтаксисе запросов и синтаксисе методов LINQ см. в статье [Синтаксис запросов и синтаксис методов в LINQ (C#)](https://docs.microsoft.com/dotnet/csharp/programming-guide/concepts/linq/query-syntax-and-method-syntax-in-linq)> В табл. 1 перечислены основные темы, с которыми вам необходимо ознакомиться, прежде чем вы приступите к работе с данной статьей. 
  
**Табл. 1. Основные понятия, необходимые для управления форматом файлов Visio 2013**

|**Название статьи**|**Описание**|
|:-----|:-----|
|[Общие сведения о формате файлов Visio (VSDX)](introduction-to-the-visio-file-formatvsdx.md) <br/> |В этом кратком обзоре описаны некоторые основные компоненты формата файлов Visio 2013. В статье рассказывается о соглашениях Open Packaging Conventions (OPC), так как они применяются в формате файлов Visio 2013. Кроме того, в статье перечислен ряд отличий формата файлов Visio 2013 и предыдущего формата файлов XML-данных документа Visio (VDX).  <br/> |
|[OPC: новый стандарт упаковки данных](https://docs.microsoft.com/archive/msdn-magazine/2007/august/opc-a-new-standard-for-packaging-your-data) <br/> |В этой статье MSDN Magazine описаны соглашения Open Packaging Conventions в виде основных понятий.  <br/> |
|[Основные понятия Open Packaging Conventions](https://docs.microsoft.com/previous-versions/office/office-12/ee361919(v=office.12)) <br/> [Общие сведения о форматах файлов Office (2007) Open XML](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa338205(v=office.12)) <br/> |В этих двух статьях рассказывается, каким образом соглашения Open Packaging Conventions используются в файлах Microsoft Office. В статьях описано, как работают связи в пакете, и приведены примеры кода.  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a>Создание VSDX-файла и решения Visual Studio
<a name="vis15_ManipulateFF_CreateFile"> </a>

Прежде чем приступить к действиям, описанным в этой статье, вам потребуется создать файл Visio 2013, который вы будете открывать и которым будете управлять. Документ, используемый в примерах кода в этой статье, содержит одну страницу с двумя соединенными фигурами, при этом одна из фигур представляет собой фигуру "Начало/конец" из шаблона "Простая блок-схема".
  
Создайте файл Visio 2013, выполнив указанные ниже действия. Вы будете использовать его на следующих этапах изучения этой статьи.
  
### <a name="to-create-new-file-in-visio-2013"></a>Создание файла в Visio 2013

1. Откройте Visio 2013.
    
2. Создайте документ на основе шаблона "Простая блок-схема". Для этого щелкните **КАТЕГОРИИ**, **Блок-схема**, **Простая блок-схема**, **Создать**.
    
3. В окне **Фигуры** перетащите фигуру **Начало/конец** на холст. 
    
4. Выберите новую фигуру "Начало/конец" на полотне и введите текст Begin Process (Начать процесс).
    
5. В окне **Фигуры** перетащите фигуру **Процесс** на холст. 
    
6. Выберите новую фигуру "Процесс" на полотне и введите текст Perform some task (Выполнить задачу).
    
7. В контекстном меню фигуры "Начало/конец" выберите пункт **Добавление на страницу одной соединительной линии** и нарисуйте соединительную линию между фигурами "Начало/конец" и "Процесс" на холсте, как показано на рис. 1.
    
    **Рис. 1. Простой документ Visio 2013**
    
     ![Фигура "Начало/конец", соединенная с фигурой "Процесс"](media/vis15_SimpleFlowchart.png)
  
8. Сохраните файл на рабочем столе в формате VSDX. Для этого щелкните **Файл**, **Сохранить как**, **Компьютер**, **Рабочий стол**.
    
    В диалоговом окне **Сохранить как** в поле **Имя файла** введите Visio Package, в списке **Тип файла** выберите пункт **Документ Visio (\*.vsdx)** и нажмите кнопку **Сохранить**. 
    
9. Закройте файл, а затем закройте Visio 2013.
    
> [!TIP]
> Иногда Visio успешно открывает файл, даже если в файле имеются проблемы. Чтобы приложение Visio сообщало вам о проблемах с файлами при тестировании решений, которые управляют файлами Visio на уровне пакета файлов, включите функцию предупреждений об открытии файлов. > Чтобы включить функцию предупреждений об открытии файлов в Visio 2013, щелкните **Файл**, **Параметры**, **Дополнительно**. В разделе **Сохранение и открытие** щелкните **Предупреждать об открытии файлов**. 
  
В этих процедурах для управления файлом Visio Package.vsdx используется консольное приложение Windows. Создайте и настройте консольное приложение Windows в Visual Studio 2012, выполнив указанные ниже действия.
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a>Создание решения в Visual Studio 2012

1. В меню **Файл** щелкните **Создать**, **Проект**.
    
2. В диалоговом окне **Создать проект** разверните пункт **Visual C#** или **Visual Basic** и щелкните **Windows**, **Консольное приложение**.
    
    В поле **Имя** введите VisioFileAccessor, выберите расположение для проекта и нажмите кнопку **OK**. 
    
3. В меню **Проект** выберите пункт **Добавить ссылку**. 
    
    В диалоговом окне **Менеджер ссылок** в разделе **Сборки** щелкните **Платформа** и добавьте ссылку на компоненты **System.Xml** и **WindowsBase**. 
    
4. В файле Program.cs или Module1.vb для проекта добавьте следующие директивы **using** (инструкции **Imports** в Visual Basic): 
    
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

5. Кроме того, в файле Program.cs или Module1.vb file перед концом метода **Main** класса **Program** (**Module1** в Visual Basic) добавьте указанный ниже код, который приостанавливает выполнение консольного приложения, пока пользователь не нажмет клавишу. 
    
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

## <a name="open-a-visio-2013-file-as-a-package"></a>Открытие файла Visio 2013 как пакета
<a name="vis15_ManipulateFF_OpenPackage"> </a>

Чтобы можно было управлять какими-либо данными в файле, необходимо сначала открыть файл в объекте [Package](https://docs.microsoft.com/dotnet/api/system.io.packaging.package?view=netframework-4.8), который содержится в пространстве имен [System.IO.Packaging](https://docs.microsoft.com/dotnet/api/system.io.packaging?view=netframework-4.8). Объект **Package** представляет весь файл Visio. Он предоставляет доступ к элементам, с помощью которых можно выбирать отдельные части документа в пакете файла. В частности, класс **Package** предоставляет доступ к статическому методу [Open(String, FileMode, FileAccess)](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.open?view=netframework-4.8), с помощью которого можно открывать файл как пакет. Кроме того, он предоставляет доступ к методу [Close()](https://docs.microsoft.com/dotnet/api/system.io.packaging.package.close?view=netframework-4.8), с помощью которого можно закрыть пакет после работы с ним. 
  
> [!TIP]
> Для открытия файла Visio в объекте **Package** рекомендуется использовать блок **using**, чтобы не пришлось явно закрывать пакет файла по завершении работы с ним. Кроме того, можно явно вызвать метод **Package.Close** в блоке **finally** конструкции **try/catch/finally**. 
  
Используя указанный ниже код, можно получить полный путь к файлу Visio Package.vsdx с помощью объекта [FileInfo](https://docs.microsoft.com/dotnet/api/system.io.fileinfo?view=netframework-4.8), передать этот путь в качестве аргумента в метод **Package.Open** и возвратить объект **Package** в вызывающий код. 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a>Открытие VSDX-файла в виде пакета

1. После метода **Main** в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже код. 
    
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

2. В методе **Main** класса **Program** (или **Module1** в Visual Basic) добавьте указанный ниже код. 
    
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

## <a name="select-and-read-package-parts-from-a-package"></a>Выбор и чтение частей пакета из пакета
<a name="vis15_ManipulateFF_SelectPart"> </a>

После того как вы откроете файл Visio 2013 как пакет, вы сможете получить доступ к частям документа в файле с помощью класса [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx), включенного в пространство имен **System.IO.Packaging**. Создавать экземпляры объектов **PackagePart** можно как отдельно, так и в виде коллекции. Класс **Package** предоставляет доступ к методам [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) и [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx), с помощью которых можно получить объекты **PackagePart** из объекта **Package**. Метод **Package.GetParts** возвращает экземпляр класса [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx), с которым можно взаимодействовать, как с любой другой коллекцией, реализующей интерфейс [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2). 
  
С помощью кода в указанной ниже процедуре можно получить объект **PackagePartCollection** из объекта **Package** в виде коллекции, выполнить итерацию объектов **PackagePart** в этой коллекции, а затем записать универсальный код ресурса (URI) и тип контента каждого объекта **PackagePart** в консоль. 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a>Выполнение итерации частей пакета в пакете

1. После метода `OpenPackage` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже код. 
    
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

2. Добавьте следующий код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic): 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. Выполните отладку решения, нажав клавишу F5. По завершении работы программы выйдите из нее, нажав любую клавишу.
    
Консольное приложение создает примерно следующие выходные данные (для краткости часть выходных данных опущена):
  
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
  
Обычно требуется выбрать один объект **PackagePart**, не выполняя итерацию всех таких объектов. Вы можете получить объект **PackagePart** из объекта **Package**, используя его связь с объектом **Package** или другим объектом **PackagePart**. В формате файлов Visio 2013 связь представляет собой дискретный объект, который описывает, каким образом часть документа связана с пакетом файла или как две части документа связаны друг с другом. Например, сам пакет файла Visio 2013 имеет связь со своей частью Visio Document, а часть Visio Document имеет связь с частью Windows. Эти связи представлены как экземпляры классов [PackageRelationship](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationship?view=netframework-4.8) или [PackageRelationshipCollection](https://docs.microsoft.com/dotnet/api/system.io.packaging.packagerelationshipcollection?view=netframework-4.8). 

Класс **Package** предоставляет доступ к нескольким методам, которые используются для получения связей и содержатся в нем в виде объектов **PackageRelationship** или **PackageRelationshipCollection**. С помощью метода [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) вы можете создать экземпляр объекта **PackageRelationshipCollection**, содержащий объекты **PackageRelationship** одного определенного типа. Безусловно, чтобы использовать метод **Package.GetRelationshipsByType**, вы должны знать, какой тип связи необходим вам. Типы связей представляют собой строки в формате пространства имен XML. Например, тип связи части Visio Document — http://schemas.microsoft.com/visio/2010/relationships/document. 
  
После того как вы получите сведения о связи объекта **PackagePart** с объектом **Package** или другим объектом **PackagePart** (то есть когда у вас будет объект **PackageRelationship**, который ссылается на необходимый вам объект **PackagePart**), вы сможете использовать эту связь для получения универсального кода ресурса (URI) этого объекта **PackagePart**. После этого можно передать универсальный код ресурса (URI) в метод **Package.GetPart**, чтобы возвратить объект **PackagePart**.
  
> [!NOTE]
> Кроме того, вы можете получить ссылку на определенный объект **PackagePart**, используя только метод **Package.GetPart** и универсальный код ресурса (URI) объекта **PackagePart**. В этом случае можно исключить этап получения связей части пакета. Некоторые части пакета в пакете файла Visio можно сохранять в расположения, отличные от расположений, используемых по умолчанию, в пакете. Не следует рассчитывать на то, что часть пакета всегда будет расположена в одном и том же универсальном коде ресурса (URI) для каждого файла. > Вместо этого для доступа к отдельным объектам **PackagePart** рекомендуется использовать связи. 
  
Выполните указанные ниже действия, чтобы получить объект **PackagePart** (часть Visio Document), используя объект **PackageRelationship** из объекта **Package**, который ссылается на часть. 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a>Выбор определенной части пакета в пакете с использованием связи

1. После метода `IteratePackageParts` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже метод. 
    
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

2. Замените код в блоке **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) указанным ниже кодом. 
    
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

Как было сказано выше, вы также можете получать объекты **PackagePart**, используя их связи с другими объектами **PackagePart**. Это важно, так как в документах Visio любой сложности у большинства объектов **PackagePart** нет связи с объектом **Package**. Например, у отдельной части Page Content в пакете файла (то есть /visio/pages/page1.xml) имеется связь с частью Page Index (то есть /visio/pages/pages.xml), но не с самим пакетом файла. Если у вас нет точного универсального кода ресурса (URI) отдельной страницы в пакете, вы можете использовать ее связь с частью Page Index, чтобы получить ссылку на нее.
  
Класс **PackagePart** предоставляет доступ к методу [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx), который можно использовать для возврата объекта **PackageRelationshipCollection**, содержащего объект **PackageRelationship** только одного типа. Если у вас есть объект **PackageRelationshipCollection**, вы можете выбрать необходимый вам объект **PackageRelationship** из коллекции и сослаться на объект **PackagePart**. 
  
С помощью указанного ниже кода можно получить объект **PackagePart** из объекта **Package**, используя его связь с другим объектом **PackagePart** (получив объект **PackageRelationship** из последнего).
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a>Выбор определенной части пакета с использованием ее связи с другой частью пакета

1. После метода `GetPackagePart` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже метод перегрузки. 
    
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

2. Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) после кода, указанного в предыдущей процедуре. (Не удаляйте код, который вы добавили в предыдущей процедуре.) 
    
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

Чтобы можно было вносить изменения в XML, включенный в часть документа, необходимо сначала загрузить документ XML в объект, который позволяет читать XML c помощью классов [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) или [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx). Оба эти класса предоставляют доступ к методам, используемым для решения таких задач, как выбор элементов XML, содержащихся в документах XML, создание, чтение и запись атрибутов, а также вставка новых элементов XML в документ. 
  
С помощью класса **XDocument** можно создавать запросы к XML, используя LINQ. Используя LINQ, можно легко выбирать отдельные элементы из документа XML, создавая запросы, а не выполняя итерацию всех элементов в коллекции и не проверяя их, чтобы выбрать необходимые элементы. По этим причинам в процедурах, описанных ниже в этой статье, для работы с XML используется класс **XDocument** и другие классы пространства имен **System.Xml.Linq**. 
  
С помощью указанных ниже процедур можно открыть объект **PackagePart** как документ XML в объекте **XDocument**. 
  
### <a name="to-read-the-xml-in-a-package-part"></a>Чтение XML в части пакета

1. После последней перегрузки для метода `GetPackagePart` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже метод. 
    
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

2. Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) после кода, указанного в предыдущей процедуре. 
    
    ```cs
    // Open the XML from the Page Contents part.
    XDocument pageXML = GetXMLFromPart(pagePart);
    ```

    ```vb
    ' Open the XML from the Page Contents part.
    Dim pageXML As XDocument = GetXMLFromPart(pagePart)
    ```

## <a name="select-and-change-xml-data-in-a-package-part"></a>Выбор и изменение данных XML в части пакета
<a name="vis15_ManipulateFF_ChangeXML"> </a>

После загрузки части документа в объект **XDocument** для выбора элементов XML и внесения изменений в документ XML можно использовать LINQ. Вы можете изменять данные XML, добавлять или удалять данные, а затем сохранять документ XML обратно в часть документа. 
  
Самая распространенная задача управления форматом файлов Visio — выбор определенных элементов или коллекций элементов XML в документе. Пространство имен **System.Xml.Linq** включает класс [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx), который представляет элемент XML. С помощью класса **XElement** можно на детальном уровне получить доступ к данным, содержащимся в файле Visio, от отдельных элементов **Shape** до элементов **ValidationRule** (в качестве примера). 
  
С помощью указанного ниже кода можно выбрать элементы **Shape** из объекта **XDocument** (содержащего часть Page Contents), а затем выбрать определенный элемент **Shape**. 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a>Выбор определенного элемента в части пакета

1. После метода `GetXMLFromPart` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже метод. 
        
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

2. После метода `GetXElementsByName` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод. 
    
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

3. Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) после кода, указанного в предыдущей процедуре. 
    
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

После получения ссылки на объект **XElement**, содержащийся в объекте **XDocument**, вы можете управлять им, как и любыми другими данными XML, и, соответственно, изменять данные, содержащиеся в файле Visio. Например, если при открытии в Visio у какой-либо фигуры имеется текст, соответствующий элемент **Shape** будет содержать по крайней мере один элемент **Text**. Если вы измените значение этого элемента **Text**, то при просмотре файла в Visio у текст фигуры изменится. 
  
Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic), чтобы изменить текст в фигуре Start/End (Начало/конец) с Begin process (Начать процесс) на Start process (Запустить процесс). 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName == "Text"
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
    Where element.Name.LocalName == "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> В предыдущем примере кода существующий текст фигуры и строка, используемая для его замены, содержат одинаковое количество символов. Кроме того, обратите внимание на то, что запрос LINQ изменяет значение последнего дочернего узла возвращаемого элемента (который в данном случае представляет собой текстовый узел). Это сделано, чтобы не допустить изменения параметров элемента **cp**, который представляет собой дочерний элемент элемента **Text**. > Если программно изменить текст фигуры путем перезаписи всех дочерних элементов элемента **Text**, это может привести к нестабильности файла. Как показано в примере выше, форматирование текста представлено элементами **cp** в элементе **Text** в файле. Определение форматирования хранится в родительском элементе **Section**. Если эти два элемента информации станут несогласованными, файл может вести себя непредсказуемо. Приложение Visio исправляет многие виды несогласованности, но лучше убедиться, что все изменения, внесенные программным способом, согласованы. В этом случае вы сможете контролировать поведение файла. 
  
Когда вы вносите изменения в XML части документа, эти изменения хранятся только в памяти. Чтобы сохранить их в файл, необходимо сохранить XML обратно в часть документа.
  
В указанном ниже коде показано, как с помощью классов [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) и [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) записать XML обратно в часть пакета. Несмотря на то что для сохранения XML обратно в часть можно использовать метод [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx), классы **XmlWriter** и **XmlWriterSettings** позволяют более тонко управлять выводом данных, в том числе указывать тип кодировки. Класс **XDocument** предоставляет доступ к методу [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx), который берет объект **XmlWriter** и записывает XML обратно в поток. 
  
С помощью указанных ниже действий можно сохранить XML из страницы Visio обратно в часть Page Contents.
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a>Сохранение измененного XML обратно в пакет

1. После метода `GetXElementByAttribute` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод. 
    
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

2. Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) после кода, указанного в предыдущей процедуре. 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. Выполните отладку решения, нажав клавишу F5. По завершении работы программы выйдите из нее, нажав любую клавишу.
    
4. Откройте файл Visio Package.vsdx в Visio 2013. 
    
Теперь фигура "Начало/конец" должна содержать текст Start process (Запустить процесс).
  
## <a name="recalculate-data-in-the-file"></a>Пересчет данных в файле
<a name="vis15_ManipulateFF_Recalculate"> </a>

При внесении некоторых изменений в данные в файле приложению Visio может потребоваться пересчитать документ при открытии файла. В Visio имеется большое количество логики для схем, особенно для связей фигур (то есть когда одна фигура зависит от другой) и соединения фигур. Если изменить какие-либо данные, которые используются в пользовательской логике, приложению Visio потребуется распространить изменения на все затронутые вычисляемые данные в файле. 
  
Формат файла Visio 2013 включает пару методов, которые вы можете использовать для пересчета данных в файле. Существует три типа сценариев, которые необходимо учесть, принимая решение о том, необходимо ли выполнить пересчет в файле Visio, и о том, как сделать это.
  
- Изменения данных не затрагивают другие значения в формате файла. Вам не нужно добавлять дополнительные инструкции в Visio для пересчета документа. Как было показано выше, вы можете часто изменять текст фигуры без необходимости пересчитывать документ.
    
- Изменения данных ограничиваются изменением значений ячеек ShapeSheet в XML и при этом имеются другие значения ShapeSheet, зависящие от этих данных. В этом случае необходимо добавить инструкцию по обработке XML (используя класс [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)) в элемент **Cell**, который был изменен. Например, ячейка **ThemeIndex** для фигуры влияет на значения нескольких других ячеек ShapeSheet, содержащихся в фигуре. Если вы измените ячейку **ThemeIndex** в самом файле (например, элемент **Cell** со значением **N**, равным ThemeIndex), то для обновления зависимых значений вам придется добавить инструкцию по обработке в элемент **Cell**. 
    
- Изменения данных влияют на расположение соединительных линий или точек соединений. Вот еще одна ситуация: в данные ShapeSheet внесено много изменений, и вы хотите пересчитать весь документ с помощью одной инструкции (а не добавлять отдельные инструкции по обработке для каждого изменения). В этом случае вы можете дать приложению Visio указание пересчитать весь документ при открытии документа. Для этого добавьте свойство **RecalcDocument** в часть Custom File Properties (/docProps/custom.xml) пакета Visio. Пример сценария такого типа — изменение положения или размера фигур на связанной схеме. 
    
    Учтите, что это самый затратный вариант с точки рения производительности.
    
Выполните указанные ниже действия, чтобы вставить элемент **Cell** в элемент **Shape**, где из-за нового значения необходимо пересчитать другие элементы **Cell** в том же объекте **Shape**. Новый элемент **Cell** включает инструкцию по обработке в виде дочернего элемента. Это позволяет сообщить приложению Visio о том, что необходимо выполнить локальный пересчет. 
  
### <a name="to-recalculate-values-for-a-single-shape"></a>Пересчет значений для одной фигуры

1. Замените код из двух предыдущих примеров (изменение текста фигуры и вызов метода `SaveXDocumentToPart`) в блоке **using** в методе **Main** класса **Program** (в блоке **Using** метода **Main** в модуле **Module1** в Visual Basic) указанным ниже кодом. 
    
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
    ' already have a local ThemeIndex cell.
    startEndShapeXML.Add(New XElement("Cell", _
        New XAttribute("N", "ThemeIndex"),
        New XAttribute("V", "25"),
        New XProcessingInstruction("NewValue", "V")))
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

2. Выполните отладку решения, нажав клавишу F5. По завершении работы программы выйдите из нее, нажав любую клавишу.
    
3. Откройте файл Visio Package.vsdx в Visio 2013. Теперь у фигуры "Начало/конец" должен быть другой цвет заливки.
    
Цвет фигуры зависит от значения ячейки **ThemeIndex**: оно определяет активную тему, из которой фигура наследует параметры. В предыдущем примере фигура настроена так, чтобы наследовать параметры другой темы (ячейка **ThemeIndex** имеет значение 25). Если вы не используете инструкцию по обработке, цвет текста фигуры (который также зависит от значения ячейки **ThemeIndex**) не будет пересчитан. Цвет заливки фигуры изменится на белый, а текст будет по-прежнему белый и станет нечитаемым. Кроме того, если не использовать инструкцию по обработке, Visio может обновить фигуру позже, и файл будет в нестабильном состоянии, при котором значения параметров форматирования фигуры могут быть обновлены непредсказуемым образом. 
  
Если вы изменяете данные в файле таким образом, что приложению Visio требуется пересчитать документ (например, изменяете положение связанной фигуры, из-за чего приложению Visio необходимо принудительно изменить маршруты соединительных линий), вам необходимо добавить инструкцию по пересчету в файл Visio. Чтобы создать инструкцию, добавьте элемент **property**, атрибут **name** которого имеет значение RecalcDocument, в XML в часть Custom File Properties пакета файла Visio. Рекомендуется проверить часть Custom File Properties и убедиться, что инструкция RecalcDocument еще не зарегистрирована в файле. 
  
С помощью указанного ниже кода можно изменить значение ячейки **PinY** фигуры "Начало/конец" из предыдущих примеров. Этот код выбирает элемент **Cell**, который содержит данные ячейки **PinY** в виде объекта **XElement**, путем использования значения его атрибута **N**. Затем код добавляет инструкцию по пересчету в часть Custom File Properties файла Visio. 
  
> [!NOTE]
> В этом коде используются созданные ранее в этой статье методы `GetPackagePart` и `SaveXDocumentToPart`. 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a>Пересчет всего документа, когда он открыт

1. После метода `SaveXDocumentToPart` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод. 
    
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

2. После метода `RecalcDocument` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод. 
    
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

3. Замените код из предыдущего примера в блоке **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) указанным ниже кодом. 
    
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

4. Выполните отладку решения, нажав клавишу F5. По завершении работы программы выйдите из нее, нажав любую клавишу.
    
5. Откройте файл Visio Package.vsdx в Visio 2013. 
    
Теперь фигура "Начало/конец" должна быть расположена в 2 дюймах от верхнего края схемы. Маршрут соединительной линии между фигурами "Начало/конец" и "Процесс" должен быть изменен согласно изменениям макета. Если не добавить свойство **RecalcDocument** в файл, положение фигуры изменится, а маршрут соединительной линии не будет изменен, и соединительная линия не будет вести к новому расположению фигуры. 
  
## <a name="add-a-new-package-part-to-a-package"></a>Добавление новой части пакета в пакет
<a name="vis15_ManipulateFF_AddNewPart"> </a>

Один из самых распространенных сценариев изменения пакета файла — добавление новой части документа в пакет. Например, если вы хотите добавить страницу в документ Visio путем добавления контента в пакет, вам потребуется добавить часть Page Contents в пакет. 
  
Процесс добавления новой части в пакет прост. 
  
1. Создайте документ XML с данными для объекта **PackagePart**. Уделите особое внимание пространствам имен XML, управляющим схемой для определенного типа документа XML, который вы создаете.
    
2. Создайте файл, в котором будет содержаться XML, и сохраните его в расположение в объекте **Package**.
    
3. Создайте необходимые связи между новым объектом **PackagePart** и объектом **Package** или другими объектами **PackagePart**. 
    
4. Обновите все существующие части, которые должны ссылаться на новую часть. Например, если вы добавляете новую часть Page Contents (новую страницу) в файл, вам потребуется обновить часть Page Index (файл /visio/pages/pages.xml), чтобы она включала правильные сведения о новой странице.
    
Выполните указанные ниже действия, чтобы создать часть Ribbon Extensibility в файле Visio. Новая часть Ribbon Extensibility добавляет на ленту новую вкладку с одной группой, содержащей одну кнопку.
  
### <a name="to-create-a-new-package-part"></a>Создание части пакета

1. После метода `CheckForRecalc` в классе **Program** (или **Module1** в Visual Basic) из предыдущей процедуры добавьте указанный ниже метод. 
    
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

2. После метода `CreateCustomUI` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод. 
    
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

3. Замените весь код в блоке **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) указанным ниже кодом. 
    
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

4. Выполните отладку решения, нажав клавишу F5. По завершении работы программы выйдите из нее, нажав любую клавишу.
    
5. Откройте файл Visio Package.vsdx в Visio 2013 и перейдите на вкладку **CUSTOM** (Настраиваемая). 
    
При открытии файла в Visio 2013 настроенная лента выглядит, как показано на рис. 2.
  
 **Рис. 2. Вкладка Custom (Настраиваемая) на ленте Visio 2013**
  
![Настраиваемая вкладка на ленте](media/vis15_CustomRibbonTab.PNG)
  
XML, созданный методом `CreateCustomUI`, выглядит, как показано ниже. 
  
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

Мы хотим поблагодарить Visio MVP **Эла Эдланда (Al Edlund)** за его вклад в создание примеров кода, изложенных в данной технической статье. Эл — признанный специалист по управлению форматами файлов Visio, в том числе форматом XML-данных документа Visio (VDX) и новым форматом файлов Visio (VSDX). Эл создал проекты, которые позволяют программным способом изучить форматы файлов Visio и показать их внутреннюю структуру. 
  
Дополнительные сведения о том, как Эл работает с форматом файлов Visio, см. по ссылкам в разделе "Дополнительные ресурсы" ниже.
  
## <a name="see-also"></a>См. также
<a name="vis15_ManipulateFF_Additional"> </a>

- Автор Эл Эдланд:
    
  - Проект [pkgVisio — управление XML в Visio 2013](https://pkgvisio.codeplex.com/documentation) на веб-сайте CodePlex. 
    
  - Видеоролик [pkgVisio_pt1](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) на веб-сайте YouTube. 
    
  - Видеоролик [pkgVisio_pt2](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) на веб-сайте YouTube. 
    
- [Центр разработчиков Visio](https://developer.microsoft.com/visio)
    
- [Управление документами форматов Office Open XML](https://docs.microsoft.com/previous-versions/office/developer/office-2007/aa982683(v=office.12))
    
- [Создание документа с пространствами имен (C#) (из LINQ в XML)](https://docs.microsoft.com/previous-versions/bb387075(v=vs.140))
    
- [Добавление XML-частей в документ без запуска Microsoft Office](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/bb608597(v=vs.90))
    

