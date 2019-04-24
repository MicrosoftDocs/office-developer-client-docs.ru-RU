---
title: Общие сведения о формате файлов Visio (VSDX)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 69736f40-8f67-46c2-abf6-82dffecb2274
description: Узнайте о новом формате файлов в Visio 2013, изучите некоторые высокоуровневые концепции программной работы с форматом файлов Visio 2013 и создайте простое консольное приложение, которое проверяет файл Visio 2013.
localization_priority: Priority
ms.openlocfilehash: 74c0f05a1db280386f3dc9dfd23da73a9b2daaf5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357276"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a>Общие сведения о формате файлов Visio (VSDX)

Узнайте о новом формате файлов в Visio 2013, изучите некоторые высокоуровневые концепции программной работы с форматом файлов Visio 2013 и создайте простое консольное приложение, которое проверяет файл Visio 2013.
  
|||
|:-----|:-----|
|**В этой статье** [Введение](#vis15_IntroVSDX_Intro) [Что из себя представляет формат файлов Visio 2013?](#vis15_IntroVSDX_What)          [Сценарии разработчика для работы с форматом файлов Visio 2013](#vis15_IntroVSDX_Scenarios) [Программное изучение формата файлов Visio 2013](#vis15_IntroVSDX_Explore) [Дополнительные ресурсы](#vis15_IntroVSDX_Resources)||
   
## <a name="introduction"></a>Введение
<a name="vis15_IntroVSDX_Intro"> </a>

Visio 2013 представляет новый формат файла (.vsdx) для Visio, который заменяет формат двоичного файла Visio (.vsd) и файл документа Visio в формате XML (.vdx). Так как формат файла Visio 2013 основывается на соглашениях Open Packaging Conventions и XML, разработчики, имеющие представление об этих технологиях, могут быстро научиться программной работе с файлами Visio 2013. Разработчики, знакомые с файлами документов Visio в формате XML (.vdx) из предыдущих версий Visio, могут найти множество одинаковых XML-структур внутри частей файла в формате VSDX. Взаимодействие с файлами Visio значительно повысилось, поскольку стороннее программное обеспечение может работать с файлами Visio на уровне формата файлов. Формат файлов Visio 2013 поддерживается в службах Visio в Microsoft SharePoint Server 2013, при этом использование промежуточного формата файлов для публикации в SharePoint Server не требуется.
  
Существует несколько типов (расширений) файлов, которые входят в формат файла Visio 2013. Эти расширения перечислены ниже.
  
- VSDX (документ Visio);
    
- VSDM (документ Visio с поддержкой макросов);
    
- VSSX (набор элементов Visio);
    
- VSSM (набор элементов Visio с поддержкой макросов);
    
- VSTX (шаблон Visio);
    
- VSTM (шаблон Visio с поддержкой макросов).
    
> [!NOTE]
> Макросы VBA можно хранить только в файлах с поддержкой макросов (VSDM, VSSM, VSTM). Хранение макросов в файлах с расширением VSDX, VSSX или VSTX невозможно. 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a>Что из себя представляет формат файлов Visio 2013?
<a name="vis15_IntroVSDX_What"> </a>

Формат файлов Visio 2013 использует соглашения Open Packing Conventions (OPC), которые определяют структурированные средства для хранения данных приложения вместе со связанными ресурсами с помощью контейнера, например ZIP-файла. На базовом уровне файл Visio 2013 действительно представляет собой ZIP-контейнер, содержащий файлы других типов. Фактически вы можете сохранить чертеж в Visio 2013 в виде VSDX-файла, в проводнике переименовать расширение на "\*.zip", а затем открыть этот файл как папку, чтобы просмотреть его содержимое.
  
> [!NOTE]
>  В этой статье приведен краткий обзор Open Packaging Conventions. Более подробное описание этих соглашений можно найти в других статьях. > Дополнительные сведения непосредственно об Open Packaging Conventions см. в статье [OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx). > Дополнительные сведения о соглашениях Open Packaging Conventions и их использовании в файлах Microsoft Office см. в статьях [Основные понятия Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) и [Общие сведения о форматах файлов Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx). 
  
### <a name="packages-and-package-parts"></a>Пакеты и части пакетов

Как уже говорилось ранее, файлы Visio 2013 являются ZIP-контейнерами или "пакетами", в которых находятся другие файлы (называемые "частями пакета"). Часть пакета может быть XML-файлом, изображением или даже решением VBA. Части, находящиеся в пакете, можно разделить на две большие категории: "части документов" и "части отношений". Части документов содержат фактическое содержимое и метаданные файла Visio, такие как имя файла, первая страница и все содержащиеся на ней фигуры, а также соединения данных для этих фигур. Изображения и текстовые файлы в пакете считаются частями документа. Более подробное описание частей отношений будет приведено далее в этой статье.
  
> [!NOTE]
> Если открыть файл Visio 2013 с помощью служебной программы ZIP, скорее всего вы увидите, что в этом ZIP-пакете находится несколько папок. Вы даже сможете управлять этими подадресами как папками, используя служебную программу ZIP. Однако эти "папки" являются подадресами в пакете ZIP, а не реальными папками. Вы не сможете использовать программные эквиваленты папок, чтобы работать с этими подадресами в вашем решении. 
  
Части пакета (как части документов, так и части отношений) также имеют связанные типы контента. Этими типами контента являются строки, которые определяют тип мультимедиа MIME. Эти типы контента устанавливают и определяют MIME-типы, которые могут содержаться в файле.
  
### <a name="relationships"></a>Отношения

Части отношений (оканчивающиеся расширением "\*.rels" и хранимые в папке "_rels") описывают, каким образом эти части в пакете связаны друг с другом, и определяют структуру файла. Отдельный XML-документ использует иерархическое ("родитель — потомок") отношение элементов для определения связи объектов друг с другом. Другие файлы могут использовать другую иерархию или структуру папок с файлами для описания взаимодействия содержимого в файле. В формате файлов Visio 2013 допустимым файлом Visio является пакет, содержащий правильный набор частей и отношения между частями. 
  
Части отношений — это XML-документы, описывающие отношения между различными частями документа в пакете. Они определяют связь между двумя элементами: указанным источником (который задается именем и расположением файла отношений) и указанной частью целевого документа. Например, части отношений используются для описания того, какие мастеры форм связаны с файлом, как страницы связаны с файлом и друг с другом или как изображения и объекты связаны с конкретной страницей. 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a>Сходства и различия со схемой Visio VDX

Как уже было сказано, предыдущие версии Visio также имели формат файлов на основе XML, т. е. документ Visio в формате XML (VDX). (В предыдущих версиях Visio схема, используемая для документов Visio в формате XML, называлась DatadiagramML.) Некоторые фрагменты схемы Visio XML не изменились. Например, элемент **Windows** и его дочерние элементы остались неизменными, за исключением того, что теперь элемент **Windows** является корневым элементом документа XML (window.xml). 
  
Самое большое различие между документом в формате XML и форматом файлов Visio 2013 заключается в упаковке. С файлом документа в формате XML можно работать как с обычным автономным XML-файлом; файл в формате Visio 2013 необходимо обрабатывать как пакет. Для удобства использования в Visio 2013 код XML разделен на две части. Еще одно значимое изменение состоит в том, что формат файлов Visio 2013 хранит все свойства документа в частях документа, которые описаны стандартом OPC (app.xml, core.xml, custom.xml).
  
Однако есть одно существенное изменение, которое должны учитывать все разработчики Visio: появление элементов **Cell**, **Row** и **Section**. В схеме файла документа в формате XML отдельные строки и ячейки в ShapeSheet представлены именованными элементами. Предположим, что у вас есть одностраничный документ, содержащий фигуру, элемент **PinX** которой имеет значение "2" (это означает, что ось вращения фигуры находится в 2 дюймах от левого края чертежа). Соответствующая разметка для этого параметра в файле документа в формате XML представлена в следующем коде. 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

Здесь элемент **PinX** является дочерним по отношению к элементу **XForm**, который, в свою очередь, является дочерним по отношению к элементу **Shape**. Этот код строит модель пользовательского интерфейса Visio ShapeSheet, где ячейка **PinX** включена в раздел **Shape Transform** фигуры. 
  
В формате файлов Visio 2013 все ячейки в ShapeSheet (**PinX**, **LinePattern**, ячейка **X** в строке **MoveTo** из раздела **Geometry** и т. д.) представлены одним типом XML-элемента — элементом **Cell**. Различные элементы **Cell** отличаются друг от друга значением атрибута **N**. Таким образом, данные, содержащиеся в ячейке **PinX** в ShapeSheet в приведенном выше примере, хранятся в VSDX-файле, как представлено в следующем коде. 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

Элемент **Cell** для **PinX** (а также другие отдельные именованные ячейки, называемые "singleton-ячейками", например **LinePattern** или **LockSelect**) является прямым потомком элемента **Shape**. Для представления строки, содержащей ячейку **PinX**, уникальный элемент не требуется, поскольку каждая фигура может иметь только один элемент **PinX**.
  
Что насчет разделов, которые содержат табличные данные, например раздел **Geometry**? В ячейках из этих разделов для хранения данных схема формата файлов Visio 2013 использует элементы **Section** и **Row**, которые различаются атрибутами **N** или **T**, как показано ниже Например, фигура из предыдущего примера может содержать данные в разделе **Geometry 1**, код которого в схеме документа в формате XML выглядит следующим образом. 
  
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

Но в файле Visio 2013 код выглядит следующим образом.
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a>Сценарии разработчика для работы с форматом файлов Visio 2013
<a name="vis15_IntroVSDX_Scenarios"> </a>

Как было пояснено выше, формат файлов Visio 2013 использует для хранения данных несколько широко известных технологий, таких как ZIP-файлы и XML. Для обработки документов Visio 2013 на уровне файлов решение должно использовать только пространства имен и классы .NET Framework, которые связаны с работой с файлами ZIP или XML, например [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) или [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).
  
Ключевое преимущество для разработчиков формата файлов Visio 2013 заключается в том, что чтение и запись файлов Visio 2013 можно выполнять без автоматизации клиентского приложения Visio. Вот некоторые сценарии, которыми может воспользоваться разработчик при работе с форматом файлов Visio 2013:
  
- Проверка отдельных файлов Visio 2013 на наличие определенных данных. Вы можете выборочно прочитать один элемент из ZIP-контейнера, не извлекая содержимое всего файла.
    
- Обновление библиотек файлов Visio 2013 с определенным содержимым. Вы можете программно изменить логотип на всех фоновых страницах, чтобы отразить новые рекомендации по фирменной символике.
    
- Создание приложений, использующих файлы Visio 2013. Например, вы можете создать инструмент, который считывает схему рабочего процесса Visio, а затем на основе этого рабочего процесса выполняет собственную бизнес-логику.
    
Помните, что поскольку в этих решениях используются стандартные сборки .NET Framework, большинство решений, которые могут быть запущены на клиентском компьютере, также могут выполняться на сервере!
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a>Программное изучение формата файлов Visio 2013
<a name="vis15_IntroVSDX_Explore"> </a>

Основная и фундаментальная задача любого разработчика, работающего с форматом файлов Visio 2013, заключается в том, чтобы открыть файл как пакет, а затем получить доступ к отдельным частям в пакете. Класс **System.IO.Packaging.Package** в WindowsBase.dll содержит множество классов, которые позволяют открывать пакеты и части и работать с ними. 
  
В следующем примере кода вы увидите, как открыть VSDX-файл, прочитать список частей в пакете и получить информацию о каждой части.
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a>Открытие VSDX-файла и просмотр частей документа

1. Откройте Visio 2013 и создайте новый документ.
    
2. Создайте новый документ и сохраните его на рабочем столе.
    
3. Откройте Visual Studio 2012.
    
4. В меню **Файл** выберите команду **Создать**, а затем пункт **Проект**.
    
5. В разделе **Visual C#** или **Visual Basic** разверните узел **Windows** и выберите пункт **Консольное приложение**.
    
6. В поле **Имя** введите "VisioFileExplorer". Откроется проект консольного приложения. 
    
7. В **обозревателей решений** щелкните правой кнопкой мыши пункт **VisioFileExplorer**, а затем выберите команду **Добавить ссылку**. 
    
8. В диалоговом окне **Добавление ссылки** в разделе **Сборки** разверните узел **Платформа**, а затем выберите пункт **WindowsBase**.
    
9. Вставьте в решение следующий код.
    
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

10. Нажмите клавишу F5, чтобы отладить решение. По завершении работы программы выйдите из нее, нажав любую клавишу.
    
## <a name="see-also"></a>См. также
<a name="vis15_IntroVSDX_Resources"> </a>

Дополнительные сведения о формате файлов Visio 2013, соглашении Open Packaging Convention и программной работе с файлами Visio 2013 или Office OpenXML см. в следующих ресурсах.
  
- [Visio для разработчиков](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx)
    
- [Основные понятия Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [Общие сведения о форматах файлов Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx)
    

