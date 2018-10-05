---
title: Общие сведения о формате файлов Visio (VSDX)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Сведения о новом формате в Visio 2013 некоторые высокого уровня понятия по работе с формат файлов Visio 2013 программными средствами и создание простого консольного приложения, которое проверяет файл Visio 2013.
ms.openlocfilehash: 4efa90ee513def005653f4f8717b0149de1cdc3d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389367"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Общие сведения о формате файлов Visio (VSDX)

Сведения о новом формате в Visio 2013 некоторые высокого уровня понятия по работе с формат файлов Visio 2013 программными средствами и создание простого консольного приложения, которое проверяет файл Visio 2013.
  
|||
|:-----|:-----|
|**В этой статье** [Общие сведения](#vis15_IntroVSDX_Intro) [Формат файла Visio 2013 «за кулисами»?](#vis15_IntroVSDX_What)                             [Сценарии разработчика для работы с формат файлов Visio 2013](#vis15_IntroVSDX_Scenarios) [Обзор возможностей в формат файлов Visio 2013 программными средствами](#vis15_IntroVSDX_Explore) [Дополнительные материалы](#vis15_IntroVSDX_Resources)                    ||
   
## <a name="introduction"></a>Введение
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 представлен новый формат файла (vsdx (en) для Visio, которая заменяет формата двоичного файла Visio (.vsd) и формат файлов XML документа Visio (.vdx). Так как в формат файлов Visio 2013 основан на параметрах Open Packaging Conventions и XML, разработчики, так как они знакомы с этими технологиями можно быстро Узнайте, как для программной работы с файлами Visio 2013. Разработчики, знакомые с форматом файла документ XML Visio (.vdx) из предыдущих версий Visio можно найти многие из одной структуры XML внутри части формата файла vsdx (en). Взаимодействие с файлами Visio значительно возрастает с момента программного обеспечения сторонних производителей могут управлять файлов Visio на уровне формата файла. Формат файлов Visio 2013 поддерживается в службах Visio в Microsoft SharePoint Server 2013 без необходимости «промежуточный» формат файла для публикации в SharePoint Server.
  
Существует несколько типов файлов с расширением, образующих формат файлов Visio 2013. Файлы с этим расширением включают:
  
- VSDX (документ Visio),
    
- VSDM (документ Visio с поддержкой макросов),
    
- VSSX (набор элементов Visio),
    
- VSSM (набор элементов Visio с поддержкой макросов),
    
- VSTX (шаблон Visio),
    
- VSTM (шаблон Visio с поддержкой макросов).
    
> [!NOTE]
> Только с поддержкой макросов файлы (.vsdm, .vssm, .vstm) можно хранить макросов VBA. Нельзя хранить макросов в файлах с vsdx (en), .vssx или .vstx расширения. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>Что такое формат файлов Visio 2013 «за кулисами»
<a name="vis15_IntroVSDX_What"> </a>

Формат файлов Visio 2013 использует Open упаковки Conventions (OPC), определяющий структурированных означает, что для хранения данных приложения вместе с другими материалами, с помощью контейнера некоторые примеры sort─for в ZIP-файле. В общем случае файла Visio 2013 все сводится к ZIP-контейнер, содержащий других типов файлов. На самом деле сохранения документа в Visio 2013 в формате vsdx (en), измените расширение файла для "\*.zip» в проводнике Windows и затем откройте файл как папку, чтобы просмотреть его содержимое.
  
> [!NOTE]
>  В этой статье содержится краткий обзор Open Packaging Conventions. Можно найти более подробные покрытия условные обозначения в других статьях: > Дополнительные сведения об Open Packaging Conventions сами можно [OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx). > Дополнительные сведения об Open Packaging Conventions и их использование в файлы Microsoft Office можно [основные моменты спецификаций Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) и [Краткие сведения о форматах файлов Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Пакеты и части пакета

Как работы более ранних версий, файлов Visio 2013, контейнеров ZIP или «пакеты», который содержать другие файлы (называемого «части пакета») в них. Часть пакета может быть XML-файла, изображения, даже решения VBA. Части в пакете, можно разделить на две основные категории, «части документа» и «компоненты связей». Части документа содержит фактические контента и метаданных файла Visio, например имя файла, первой страницы и всех фигур, которые он содержит, и даже подключения к данным для фигур. Изображения и текстовые файлы в пакете, считаются частями документа. Связь частей описаны более подробно далее в этой статье.
  
> [!NOTE]
> При открытии файла Visio 2013, с помощью служебной программы ZIP, вероятно, можно увидеть несколько папок, содержащихся в ZIP-архив. Можно даже работы с этих вложенных адреса папок с помощью программы ZIP. Тем не менее эти «папки» представления подменю адресов в ZIP-архив, а не фактические папок. Программный эквивалентами папок нельзя использовать для работы с эти подменю адреса в решении. 
  
Части документа пакета parts─both и parts─also отношения связаны типов контента. Эти типы контента, строк, которые определяют тип мультимедиа MIME. Эти типы контента укажите и область вид типы MIME, которые могут содержаться в файле.
  
### <a name="relationships"></a>Связи

Связь частей (которого заканчивается на данное расширение имени файла "\*находится» и сохраняются в папке «_rels») описывается, как части в пакете, которые относятся к друг с другом и предоставляют структура файла. В XML-документ автономных использует отношения родительских и дочерних элементов для определения отношения сущностей друг с другом. Другие файлы использовать другие иерархии или структуру папок файла для описания взаимодействия содержимого в файле. Для формат файлов Visio 2013 пакета является файл Visio, если он содержит правильное набора частей и пакет содержит отношений между частями. 
  
Части отношения, XML-документов, которые описывают отношения между частями другого документа в пакете. Они определить связь между двумя элементами: указанного источника (определяется с помощью имя и расположение файла связи) и указанный целевой части документа. К примеру связь частей используются для описания, какие фигуры образцов связаны с файла, как страницы, которые относятся к файлу и друг с другом или как изображения и объекты связаны с конкретной страницы. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Сходства и различия с использованием схемы Visio VDX

Как уже было сказано, последние версии Visio также включаются XML-файл формата, формат XML документа Visio или .vdx. (В предыдущих версиях программы схемы, используемой для XML-документа Visio формат называется datadiagramml (en)). Некоторые элементы из схемы Visio XML лет между двумя форматах. Например элемент **Windows** и его дочерние элементы остаются unchanged─with исключение, что элемент **Windows** теперь является корневой элемент XML-документа (window.xml). 
  
Наибольшее различие между формата документа XML и формат файлов Visio 2013 — это упаковки. Файл XML-документ формате может таким образом, как обычный изолированный XML; формат файлов Visio 2013 должны обрабатываться как пакет. В Visio 2013 XML разделенный на части для удобства использования. Другое изменение заметно — это, что формат файлов Visio 2013 сохраняет все свойства документа в части документа описываемых OPC standard (app.xml, core.xml, custom.xml).
  
Однако существует один значительные изменения, необходимо иметь в виду всех разработчиков Visio: введение в элементы **ячеек**, **строк**и **раздел** . В этой схеме формат XML-файла документа отдельных строк и ячеек в таблице свойств фигуры представлены именованные элементы. Например предположим, что у вас есть документ с одной страницы, которая содержит фигуру со значением **PinX** «2» (то есть, что ПИН-код Поворот фигуры является 2 дюйма от левого края документа). В следующем примере кода показана соответствующих разметка для назначения в формате документа XML. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Здесь элемент **PinX** — дочерний элемент **XForm** , который в свою очередь является дочерним элементом **фигуры** . Эти модели пользовательского интерфейса таблицы свойств фигуры Visio, где ячейки **PinX** включен в разделе **Преобразование фигуры** фигуры. 
  
В формате файла Visio 2013, всем ячейкам в ShapeSheet─ **PinX**, **LinePattern** **X** ячейка в строке **MoveTo** раздел **геометрии** , etc.─are, представленный одного типа XML-элемент, элемент **ячейки** . Различные элементы **ячеек** individuated друг от друга, по значению атрибута их **N** . Таким образом в приведенном выше примере данные, содержащиеся в ячейке **PinX** в таблице свойств фигуры хранится в файле VSDX, как показано в следующем коде. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

Элемент **ячейки** для **PinX** (а также другие отдельных, именованные ячейки, называется «одного ячеек» как **LinePattern** или **LockSelect**) является прямым потомком элемент **фигуры** . Элемент не уникальный необходим для представления строку, содержащую ячейку **PinX** , как каждая фигура может иметь только один **PinX**.
  
Разделов, включая табличных данных, как в разделах **геометрии** ? Для ячеек в этих разделах схему форматов файлов Visio 2013 использует **раздел** и elements─also **строки** с их атрибута **N** или **T** как показано below─to содержит данные. Например фигуру из предыдущего примера может содержать данные в разделе **1 геометрии** , которая выглядит как следующий код в схеме XML-документа. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Geom IX="0">
        <!--- Other cells and rows in the Geometry 1 section -->
        <LineTo IX="1">
            <X F="Width*0">0</X>
            <Y F="Height*0">0</Y>
        </LineTo>
    </Geom>
</Shape>

```

Тем не менее он выглядит как следующий код в файле Visio 2013.
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <!--- Other cells in the ShapeSheet -->
    <Section N="Geometry" IX="0"> 
        <!--- Other cells and rows in the Geometry 1 section -->
        <Row IX="1" T="LineTo">
            <Cell V="0" N="X" V="Width*0" />
            <Cell V="0" N="Y" V="Height*0" />
        </Row>
    </Section>
</Shape>

```

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Сценарии разработчика для работы с формат файлов Visio 2013
<a name="vis15_IntroVSDX_Scenarios"> </a>

Как описано выше в формат файлов Visio 2013 использует несколько общепризнанным технологии, такие как ZIP-файлы и XML для хранения данных. Для работы с Visio 2013 рисования на уровне файлов, решения должны только для использования платформы .NET Framework пространства имен и классы, связанные с работой ZIP-файлы или XML, например, [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) или [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).
  
Ключевые преимущества для разработчиков в формат файлов Visio 2013 является чтение и запись файлов Visio 2013 без автоматизации клиентского приложения Visio. Некоторые сценарии, в которых может потребоваться разработчик, для работы с формат файлов Visio 2013 включают:
  
- Проверка отдельных файлов Visio 2013 для определенных данных. Избирательно могут читать один элемент из ZIP-контейнер без необходимости Извлеките файл целиком.
    
- Обновление библиотек файлов Visio 2013 с помощью определенного содержимого. Программными средствами можно изменить логотипа в всех страниц фона в соответствии с новой фирменной настройки правила.
    
- Создание приложения, использующие файлы Visio 2013. Например можно построить это средство, которое считывает схему Visio рабочего процесса, а затем выполняет собственную бизнес-логику на основе этого рабочего процесса.
    
Помните о том, что так как эти решения используйте стандартные сборки .NET Framework, большинство решений, которые могут работать на клиентской машине также можно запустить на сервере!
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Обзор возможностей в формат файлов Visio 2013 программными средствами
<a name="vis15_IntroVSDX_Explore"> </a>

Наиболее базовой и основных задач для разработчики, работающие с формат файлов Visio 2013 открытия файла в виде пакета и получении доступа к отдельным части в пакете. **System.IO.Packaging.Package** в WindowsBase.dll содержит множество классов, которые позволяют вам открывать и управлять пакеты и части. 
  
В следующем образце кода можно узнать, как открыть файл vsdx (en), чтение списка части в пакете и получение сведений о каждой части.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Откройте файл vsdx (en) и Просмотр части документа

1. Откройте Visio 2013 и создайте новый документ.
    
2. Создайте новый документ и сохраните его на рабочий стол.
    
3. Откройте Visual Studio 2012.
    
4. В меню **файл** выберите команду **Создать**и затем нажмите ** Project **.
    
5. В разделе **Visual C#** или **Visual Basic**разверните **Windows**и выберите **Консольное приложение**.
    
6. В поле **имя** введите «VisioFileExplorer». Открывает проект консольного приложения. 
    
7. В **Обозревателе решений**щелкните правой кнопкой мыши **VisioFileExplorer**и выберите команду **Добавить ссылку**. 
    
8. В диалоговом окне **Добавить ссылку** в разделе **сборки**разверните **Framework**и выберите **WindowsBase**.
    
9. Вставьте следующий код в решение.
    
  ```cs
  using System;
  using System.Collections.Generic;
  using System.Linq;
  using System.Text;
  using System.IO;
  using System.IO.Packaging;
  using System.Diagnostics;
  namespace VisioFileExplorer
  {
      class Program
      {
          static void Main(string[] args)
          {    
              try
              {
                  Console.WriteLine("Opening the VSDX file ...");
                  // Need to get the folder path for the Desktop
                  // where the file is saved.
                  string dirPath = System.Environment.GetFolderPath(
                      System.Environment.SpecialFolder.Desktop);
                  DirectoryInfo myDir = new DirectoryInfo(dirPath);
                  // It is a best practice to get the file name string
                  // using a FileInfo object, but it isn't necessary.
                  FileInfo[] fInfos = myDir.GetFiles("*.vsdx");
                  FileInfo fi = fInfos[0];
                  string fName = fi.FullName;
                  // We're not going to do any more than open
                  // and read the list of parts in the package, although
                  // we can create a package or read/write what's inside.
                  using (Package fPackage = Package.Open(
                      fName, FileMode.Open, FileAccess.Read))
                  {
                      
                      // The way to get a reference to a package part is
                      // by using its URI. Thus, we're reading the URI
                      // for each part in the package.
                      PackagePartCollection fParts = fPackage.GetParts();
                      foreach (PackagePart fPart in fParts)
                      {
                          Console.WriteLine("Package part: {0}", fPart.Uri);
                      }
                  }   
              }
              catch (Exception err)
              {
                  Console.WriteLine("Error: {0}", err.Message);
              }
              finally
              {
                  Console.Write("\nPress any key to continue ...");
                  Console.ReadKey();
              }   
          }
      }
  }
  ```

  ```vb
  Imports System
  Imports System.Collections.Generic
  Imports System.Linq
  Imports System.Text
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Diagnostics
  Module Module1
      Sub Main()
          Try
              Console.WriteLine("Opening the VSDX file ...")
              ' Need to get the folder path for the Desktop
              ' or where the file is saved.
              Dim dirPath As String = System.Environment.GetFolderPath( _
                  System.Environment.SpecialFolder.Desktop)
              Dim myDir As New DirectoryInfo(dirPath)
              ' It is a best practice to get the file name string
              ' using a FileInfo object, but it isn't necessary.
              Dim fInfos As FileInfo() = myDir.GetFiles("*.vsdx")
              Dim fi As FileInfo = fInfos(0)
              Dim fName As String = fi.FullName
              ' We don't need to do any more than open
              ' and read the list of parts in the package, although
              ' we can create a package or read/write what's inside.
              Using fPackage As Package = Package.Open( _
                  fName, FileMode.Open, FileAccess.Read)
                  ' The way to get a reference to a document part is
                  ' by using its URI. Thus, we're reading the URI
                  ' for each document part in the package.
                  Dim fParts As PackagePartCollection = fPackage.GetParts()
                  For Each fPart As PackagePart In fParts
                      Console.WriteLine("Package part: {0}", fPart.Uri)
                  Next
              End Using
          Catch err As Exception
              Console.WriteLine("Error: {0}", err.Message)
          Finally
              Console.Write(vbLf &amp; "Press any key to continue ...")
              Console.ReadKey()
          End Try
      End Sub
  End Module
  
  ```

10. Нажмите клавишу F5 для отладки решения. После завершения работы программы нажмите любую клавишу, чтобы выйти из.
    
## <a name="see-also"></a>См. также
<a name="vis15_IntroVSDX_Resources"> </a>

Дополнительные сведения о формате файла Visio 2013, Open Packaging Convention или как можно программно работать с файлами Office OpenXML 2013or Visio можно ознакомьтесь со следующими ресурсами:
  
- [Visio для разработчиков (en)](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx).
    
- [Основные моменты спецификаций Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [Введение в форматы файлов Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx)
    

