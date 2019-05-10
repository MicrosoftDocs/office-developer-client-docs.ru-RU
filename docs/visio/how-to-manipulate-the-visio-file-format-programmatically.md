---
title: Программное управление форматами файлов Visio
manager: soliver
ms.date: 04/17/2019
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Создайте в Visual Studio 2012 решение для чтения пакетов с новым форматом файлов, используемым в Visio 2013, выбора частей в пакете, изменения данных в части и добавления новых частей в пакет.
localization_priority: Priority
ms.openlocfilehash: 2b031a74fa8d2df9b9baa15e97652b8d8afdaf23
ms.sourcegitcommit: 6f3f42b656afb45a0189a0ad4c81c095e285b3d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "33655613"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a><span data-ttu-id="ce394-103">Программное управление форматами файлов Visio</span><span class="sxs-lookup"><span data-stu-id="ce394-103">Manipulate the Visio file format programmatically</span></span>

![Раздел "Инструкции"](media/mod_icon_howto.png)
  
<span data-ttu-id="ce394-105">Узнайте, как в Visual Studio 2012 создать решение для чтения пакетов с новым форматом файлов, используемым в Visio 2013, выбора частей в пакете, изменения данных в части и добавления новых частей в пакет.</span><span class="sxs-lookup"><span data-stu-id="ce394-105">Learn how to create a solution in Visual Studio 2012 to read the new file format package in Visio 2013, select parts in the package, change the data in a part, and add new parts to the package.</span></span>
   
## <a name="visio-file-format-manipulation-essentials"></a><span data-ttu-id="ce394-106">Основные сведения об управлении форматами файлов Visio</span><span class="sxs-lookup"><span data-stu-id="ce394-106">Visio file format manipulation essentials</span></span>
<span data-ttu-id="ce394-107"><a name="vis15_ManipulateFF_Essentials"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-107"><a name="vis15_ManipulateFF_Essentials"> </a></span></span>

<span data-ttu-id="ce394-108">Приложения Visio предыдущих версий сохраняли файлы в защищенном двоичном формате (VSD) или в однодокументном формате XML-данных документа Visio (VDX).</span><span class="sxs-lookup"><span data-stu-id="ce394-108">Previous versions of Visio saved files in a proprietary binary file format (.vsd) or a single-document Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="ce394-109">В Visio 2013 появился новый формат файлов (VSDX), который основан на XML и технологии архивирования ZIP.</span><span class="sxs-lookup"><span data-stu-id="ce394-109">Visio 2013 introduces a new file format (.vsdx), which is based on XML and ZIP archive technologies.</span></span> <span data-ttu-id="ce394-110">Как и в предыдущих версиях Visio, файлы сохраняются в одном контейнере.</span><span class="sxs-lookup"><span data-stu-id="ce394-110">Just as in previous versions of Visio, files are saved in a single container.</span></span> <span data-ttu-id="ce394-111">В отличие от файлов, сохраненных в прежних версиях Visio, файлы нового формата можно открывать, читать, обновлять, изменять и создавать без автоматизации приложения Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ce394-111">Unlike legacy files, however, the new file format can be opened, read, updated, changed, and constructed without automating the Visio 2013 application.</span></span> <span data-ttu-id="ce394-112">Разработчики, которые умеют управлять XML или работать с пространством имен [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx), могут быстро приступить к программному управлению файлами нового формата.</span><span class="sxs-lookup"><span data-stu-id="ce394-112">Developers who are familiar with manipulating XML or working with the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace can quickly get started working with the new file format programmatically.</span></span> <span data-ttu-id="ce394-113">Разработчики, которые уже работали с форматом XML-данных документа Visio в предыдущих версиях приложения, обнаружат, что многие структуры этого формата перенесены в новый формат.</span><span class="sxs-lookup"><span data-stu-id="ce394-113">Developers who have worked with the Visio XML Drawing format from previous versions can find that many of the structures from that format have been retained in the new file format.</span></span> 
  
<span data-ttu-id="ce394-114">В этой статье мы расскажем, как программно работать с форматом файлов Visio 2013 с использованием Microsoft .NET Framework 4.5, C# или Visual Basic, а также Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="ce394-114">In this article, we examine how to work with the Visio 2013 file format programmatically, using the Microsoft .NET Framework 4.5, C# or Visual Basic, and Visual Studio 2012.</span></span> <span data-ttu-id="ce394-115">Вы узнаете, как открыть файл Visio 2013, выбрать части документа в файле, изменить данные в частях и создать часть документа.</span><span class="sxs-lookup"><span data-stu-id="ce394-115">You can see how to open a Visio 2013 file, select document parts within the file, change data in parts, and create a new document part.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ce394-116">В примерах кода в этой статье предполагается, что у вас есть элементарное понимание классов в пространствах имен [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) и [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce394-116">The code samples in this article assume that you have a rudimentary understanding of the classes in the [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) and [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespaces.</span></span> <span data-ttu-id="ce394-117">> В этой статье также предполагается, что вы знаете основные понятия и терминологию Open Packaging Conventions.</span><span class="sxs-lookup"><span data-stu-id="ce394-117">> This article also assumes that you understand the concepts and terminology of the Open Packaging Conventions.</span></span> <span data-ttu-id="ce394-118">Вы должны быть знакомы с основными понятиями о пакетах, частях документов или частях пакетов, а также о связях.</span><span class="sxs-lookup"><span data-stu-id="ce394-118">You should have some familiarity with the concepts of packages, document parts or package parts, and relationships.</span></span> <span data-ttu-id="ce394-119">Дополнительные сведения см. в статье [OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce394-119">For more information, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="ce394-120">> В коде показано, как создавать запросы LINQ для выбора XML.</span><span class="sxs-lookup"><span data-stu-id="ce394-120">> The code demonstrates how to create LINQ (Language-Integrated Query) queries to select XML.</span></span> <span data-ttu-id="ce394-121">В большей части примеров кода для создания запросов LINQ используется синтаксис запросов.</span><span class="sxs-lookup"><span data-stu-id="ce394-121">Most of the code samples use the query syntax for building LINQ queries.</span></span> <span data-ttu-id="ce394-122">При необходимости вы можете изменить любой из имеющихся в коде запросов LINQ, используя синтаксис методов LINQ.</span><span class="sxs-lookup"><span data-stu-id="ce394-122">You can rewrite any of the LINQ queries provided in the code by using the LINQ method syntax, if necessary.</span></span> <span data-ttu-id="ce394-123">Дополнительные сведения о синтаксисе запросов и синтаксисе методов LINQ см. в статье [Синтаксис запросов и синтаксис методов в LINQ (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> В табл. 1 перечислены основные темы, с которыми вам необходимо ознакомиться, прежде чем вы приступите к работе с данной статьей.</span><span class="sxs-lookup"><span data-stu-id="ce394-123">For more information about LINQ query syntax and method syntax, see [LINQ Query Syntax versus Method Syntax (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> Table 1 shows the essential topics that you should be familiar with before you work through this article.</span></span> 
  
<span data-ttu-id="ce394-124">**Табл. 1. Основные понятия, необходимые для управления форматом файлов Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="ce394-124">**Table 1. Core concepts for manipulating the Visio 2013 file format**</span></span>

|<span data-ttu-id="ce394-125">**Название статьи**</span><span class="sxs-lookup"><span data-stu-id="ce394-125">**Article title**</span></span>|<span data-ttu-id="ce394-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ce394-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce394-127">Общие сведения о формате файлов Visio (VSDX)</span><span class="sxs-lookup"><span data-stu-id="ce394-127">Introduction to the Visio file format (.vsdx)</span></span>](introduction-to-the-visio-file-formatvsdx.md) <br/> |<span data-ttu-id="ce394-128">В этом кратком обзоре описаны некоторые основные компоненты формата файлов Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ce394-128">This high-level overview describes some of the major features of the Visio 2013 file format.</span></span> <span data-ttu-id="ce394-129">В статье рассказывается о соглашениях Open Packaging Conventions (OPC), так как они применяются в формате файлов Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ce394-129">It discusses the Open Packaging Conventions (OPC) as they have been applied to the Visio 2013 file format.</span></span> <span data-ttu-id="ce394-130">Кроме того, в статье перечислен ряд отличий формата файлов Visio 2013 и предыдущего формата файлов XML-данных документа Visio (VDX).</span><span class="sxs-lookup"><span data-stu-id="ce394-130">It also lists some differences between the Visio 2013 file format and the previous Visio XML Drawing file format (.vdx).</span></span>  <br/> |
|[<span data-ttu-id="ce394-131">OPC: новый стандарт упаковки данных</span><span class="sxs-lookup"><span data-stu-id="ce394-131">OPC: A New Standard for Packaging Your Data</span></span>](https://msdn.microsoft.com/magazine/cc163372.aspx) <br/> |<span data-ttu-id="ce394-132">В этой статье MSDN Magazine описаны соглашения Open Packaging Conventions в виде основных понятий.</span><span class="sxs-lookup"><span data-stu-id="ce394-132">This MSDN Magazine article describes the Open Packaging Conventions as a concept.</span></span>  <br/> |
|[<span data-ttu-id="ce394-133">Основные понятия Open Packaging Conventions</span><span class="sxs-lookup"><span data-stu-id="ce394-133">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx) <br/> [<span data-ttu-id="ce394-134">Общие сведения о форматах файлов Office (2007) Open XML</span><span class="sxs-lookup"><span data-stu-id="ce394-134">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx) <br/> |<span data-ttu-id="ce394-135">В этих двух статьях рассказывается, каким образом соглашения Open Packaging Conventions используются в файлах Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="ce394-135">These two articles discuss how the Open Packaging Conventions have been applied to Microsoft Office files.</span></span> <span data-ttu-id="ce394-136">В статьях описано, как работают связи в пакете, и приведены примеры кода.</span><span class="sxs-lookup"><span data-stu-id="ce394-136">They contain descriptions of how relationships work in a package and also include some code examples.</span></span>  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a><span data-ttu-id="ce394-137">Создание VSDX-файла и решения Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ce394-137">Create a .vsdx file and a new Visual Studio solution</span></span>
<span data-ttu-id="ce394-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span></span>

<span data-ttu-id="ce394-139">Прежде чем приступить к действиям, описанным в этой статье, вам потребуется создать файл Visio 2013, который вы будете открывать и которым будете управлять.</span><span class="sxs-lookup"><span data-stu-id="ce394-139">Before you can begin working through the procedures in this article, you need to create a Visio 2013 file to open and manipulate.</span></span> <span data-ttu-id="ce394-140">Документ, используемый в примерах кода в этой статье, содержит одну страницу с двумя соединенными фигурами, при этом одна из фигур представляет собой фигуру "Начало/конец" из шаблона "Простая блок-схема".</span><span class="sxs-lookup"><span data-stu-id="ce394-140">The drawing used in the code examples in this article contains a single page with two connected shapes on it, one of the shapes being a "Start/End" shape from the "Basic Flowchart" template.</span></span>
  
<span data-ttu-id="ce394-141">Создайте файл Visio 2013, выполнив указанные ниже действия. Вы будете использовать его на следующих этапах изучения этой статьи.</span><span class="sxs-lookup"><span data-stu-id="ce394-141">Use the following procedure to create a new Visio 2013 file to use in the remaining procedures in this article.</span></span>
  
### <a name="to-create-new-file-in-visio-2013"></a><span data-ttu-id="ce394-142">Создание файла в Visio 2013</span><span class="sxs-lookup"><span data-stu-id="ce394-142">To create new file in Visio 2013</span></span>

1. <span data-ttu-id="ce394-143">Откройте Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ce394-143">Open Visio 2013.</span></span>
    
2. <span data-ttu-id="ce394-144">Создайте документ на основе шаблона "Простая блок-схема". Для этого щелкните **КАТЕГОРИИ**, **Блок-схема**, **Простая блок-схема**, **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ce394-144">Create a new document based on the Basic Flowchart template by choosing **CATEGORIES**, **Flowchart**, **Basic Flowchart**, **Create**.</span></span>
    
3. <span data-ttu-id="ce394-145">В окне **Фигуры** перетащите фигуру **Начало/конец** на холст.</span><span class="sxs-lookup"><span data-stu-id="ce394-145">From the **Shapes** window, drag a **Start/End** shape onto the canvas.</span></span> 
    
4. <span data-ttu-id="ce394-146">Выберите новую фигуру "Начало/конец" на полотне и введите текст Begin Process (Начать процесс).</span><span class="sxs-lookup"><span data-stu-id="ce394-146">Select the new Start/End shape on the drawing canvas and type 'Begin Process'.</span></span>
    
5. <span data-ttu-id="ce394-147">В окне **Фигуры** перетащите фигуру **Процесс** на холст.</span><span class="sxs-lookup"><span data-stu-id="ce394-147">From the **Shapes** window, drag a **Process** shape onto the canvas.</span></span> 
    
6. <span data-ttu-id="ce394-148">Выберите новую фигуру "Процесс" на полотне и введите текст Perform some task (Выполнить задачу).</span><span class="sxs-lookup"><span data-stu-id="ce394-148">Select the new Process shape on the drawing canvas and type 'Perform some task'.</span></span>
    
7. <span data-ttu-id="ce394-149">В контекстном меню фигуры "Начало/конец" выберите пункт **Добавление на страницу одной соединительной линии** и нарисуйте соединительную линию между фигурами "Начало/конец" и "Процесс" на холсте, как показано на рис. 1.</span><span class="sxs-lookup"><span data-stu-id="ce394-149">On the shortcut menu for the Start/End shape, select **Add One Connector to the Page**, and then draw a connector between the Start/End and Process shapes on the canvas, as shown in Figure 1.</span></span>
    
    <span data-ttu-id="ce394-150">**Рис. 1. Простой документ Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="ce394-150">**Figure 1. Simple Visio 2013 drawing**</span></span>
    
     ![Фигура "Начало/конец", соединенная с фигурой "Процесс"](media/vis15_SimpleFlowchart.png)
  
8. <span data-ttu-id="ce394-152">Сохраните файл на рабочем столе в формате VSDX. Для этого щелкните **Файл**, **Сохранить как**, **Компьютер**, **Рабочий стол**.</span><span class="sxs-lookup"><span data-stu-id="ce394-152">Save the file to your Desktop as a .vsdx file by choosing **File**, **Save As**, **Computer**, **Desktop**.</span></span>
    
    <span data-ttu-id="ce394-153">В диалоговом окне **Сохранить как** в поле **Имя файла** введите Visio Package, в списке **Тип файла** выберите пункт **Документ Visio (\*.vsdx)** и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ce394-153">In the **Save As** dialog box, enter Visio Package in the **File name** box"", select **Visio Drawing (\*.vsdx)** in the **Save as type** list, and then choose the **Save** button.</span></span> 
    
9. <span data-ttu-id="ce394-154">Закройте файл, а затем закройте Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ce394-154">Close the file and then close Visio 2013.</span></span>
    
> [!TIP]
> <span data-ttu-id="ce394-155">Иногда Visio успешно открывает файл, даже если в файле имеются проблемы.</span><span class="sxs-lookup"><span data-stu-id="ce394-155">Sometimes Visio opens a file successfully even if there are issues with the file.</span></span> <span data-ttu-id="ce394-156">Чтобы приложение Visio сообщало вам о проблемах с файлами при тестировании решений, которые управляют файлами Visio на уровне пакета файлов, включите функцию предупреждений об открытии файлов.</span><span class="sxs-lookup"><span data-stu-id="ce394-156">To ensure that Visio notifies you of any file issues, you should enable file open warnings when testing solutions that manipulate Visio files at the file package level.</span></span> <span data-ttu-id="ce394-157">> Чтобы включить функцию предупреждений об открытии файлов в Visio 2013, щелкните **Файл**, **Параметры**, **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="ce394-157">> To enable file open warnings, in Visio 2013, choose **File**, **Options**, **Advanced**.</span></span> <span data-ttu-id="ce394-158">В разделе **Сохранение и открытие** щелкните **Предупреждать об открытии файлов**.</span><span class="sxs-lookup"><span data-stu-id="ce394-158">Under **Save/Open**, select **Show file open warnings**.</span></span> 
  
<span data-ttu-id="ce394-159">В этих процедурах для управления файлом Visio Package.vsdx используется консольное приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="ce394-159">These procedures use a Windows console application to manipulate the "Visio Package.vsdx" file.</span></span> <span data-ttu-id="ce394-160">Создайте и настройте консольное приложение Windows в Visual Studio 2012, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ce394-160">Use the following procedure to create and set up a new Windows console application in Visual Studio 2012.</span></span>
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a><span data-ttu-id="ce394-161">Создание решения в Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="ce394-161">To create a new solution in Visual Studio 2012</span></span>

1. <span data-ttu-id="ce394-162">В меню **Файл** щелкните **Создать**, **Проект**.</span><span class="sxs-lookup"><span data-stu-id="ce394-162">On the **File** menu, choose **New**, **Project**.</span></span>
    
2. <span data-ttu-id="ce394-163">В диалоговом окне **Создать проект** разверните пункт **Visual C#** или **Visual Basic** и щелкните **Windows**, **Консольное приложение**.</span><span class="sxs-lookup"><span data-stu-id="ce394-163">In the **New Project** dialog box, expand either **Visual C#** or **Visual Basic**, and then choose **Windows**, **Console Application**.</span></span>
    
    <span data-ttu-id="ce394-164">В поле **Имя** введите VisioFileAccessor, выберите расположение для проекта и нажмите кнопку **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce394-164">In the **Name** box, enter ' VisioFileAccessor', select a location for the project, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="ce394-165">В меню **Проект** выберите пункт **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="ce394-165">On the **Project** menu, choose **Add Reference**.</span></span> 
    
    <span data-ttu-id="ce394-166">В диалоговом окне **Менеджер ссылок** в разделе **Сборки** щелкните **Платформа** и добавьте ссылку на компоненты **System.Xml** и **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="ce394-166">In the **Reference Manager** dialog box, under **Assemblies**, choose **Framework**, and then add a reference to the **System.Xml** and **WindowsBase** components.</span></span> 
    
4. <span data-ttu-id="ce394-167">В файле Program.cs или Module1.vb для проекта добавьте следующие директивы **using** (инструкции **Imports** в Visual Basic):</span><span class="sxs-lookup"><span data-stu-id="ce394-167">In the Program.cs or Module1.vb file for the project, add the following **using** directives (**Imports** statements in Visual Basic):</span></span> 
    
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

5. <span data-ttu-id="ce394-168">Кроме того, в файле Program.cs или Module1.vb file перед концом метода **Main** класса **Program** (**Module1** в Visual Basic) добавьте указанный ниже код, который приостанавливает выполнение консольного приложения, пока пользователь не нажмет клавишу.</span><span class="sxs-lookup"><span data-stu-id="ce394-168">Also in the Program.cs or Module1.vb file, before the end of the **Main** method of the **Program** class (**Module1** in Visual Basic), add the following code that stops execution of the console application until the user presses a key.</span></span> 
    
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

## <a name="open-a-visio-2013-file-as-a-package"></a><span data-ttu-id="ce394-169">Открытие файла Visio 2013 как пакета</span><span class="sxs-lookup"><span data-stu-id="ce394-169">Open a Visio 2013 file as a package</span></span>
<span data-ttu-id="ce394-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span></span>

<span data-ttu-id="ce394-171">Чтобы можно было управлять какими-либо данными в файле, необходимо сначала открыть файл в объекте [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx), который содержится в пространстве имен [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce394-171">Before you can manipulate any of the data within the file, you need to first open the file within a [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) object, which is contained within the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace.</span></span> <span data-ttu-id="ce394-172">Объект **Package** представляет весь файл Visio.</span><span class="sxs-lookup"><span data-stu-id="ce394-172">The **Package** object represents the Visio file as a whole.</span></span> <span data-ttu-id="ce394-173">Он предоставляет доступ к элементам, с помощью которых можно выбирать отдельные части документа в пакете файла.</span><span class="sxs-lookup"><span data-stu-id="ce394-173">It exposes members that allow you to select individual document parts within the file package.</span></span> <span data-ttu-id="ce394-174">В частности, класс **Package** предоставляет доступ к статическому методу [Open(String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx), с помощью которого можно открывать файл как пакет.</span><span class="sxs-lookup"><span data-stu-id="ce394-174">In particular, the **Package** class exposes the static [Open(String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) method that you use to open a file as a package.</span></span> <span data-ttu-id="ce394-175">Кроме того, он предоставляет доступ к методу [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx), с помощью которого можно закрыть пакет после работы с ним.</span><span class="sxs-lookup"><span data-stu-id="ce394-175">It also exposes a [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) method for closing the package once you've finished with it.</span></span> 
  
> [!TIP]
> <span data-ttu-id="ce394-176">Для открытия файла Visio в объекте **Package** рекомендуется использовать блок **using**, чтобы не пришлось явно закрывать пакет файла по завершении работы с ним.</span><span class="sxs-lookup"><span data-stu-id="ce394-176">As a best practice, use a **using** block to open the Visio file in the **Package** object so that you don't have to explicitly close the file package when you're done with it.</span></span> <span data-ttu-id="ce394-177">Кроме того, можно явно вызвать метод **Package.Close** в блоке **finally** конструкции **try/catch/finally**.</span><span class="sxs-lookup"><span data-stu-id="ce394-177">You can also explicitly call the **Package.Close** method in the **finally** block of a **try/catch/finally** construction.</span></span> 
  
<span data-ttu-id="ce394-178">Используя указанный ниже код, можно получить полный путь к файлу Visio Package.vsdx с помощью объекта [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx), передать этот путь в качестве аргумента в метод **Package.Open** и возвратить объект **Package** в вызывающий код.</span><span class="sxs-lookup"><span data-stu-id="ce394-178">Use the following code to get the full path for the "Visio Package.vsdx" file by using a [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) object, pass the path as an argument to the **Package.Open** method, and then return a **Package** object to the calling code.</span></span> 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a><span data-ttu-id="ce394-179">Открытие VSDX-файла в виде пакета</span><span class="sxs-lookup"><span data-stu-id="ce394-179">To open a .vsdx file as a package</span></span>

1. <span data-ttu-id="ce394-180">После метода **Main** в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже код.</span><span class="sxs-lookup"><span data-stu-id="ce394-180">After the **Main** method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

2. <span data-ttu-id="ce394-181">В методе **Main** класса **Program** (или **Module1** в Visual Basic) добавьте указанный ниже код.</span><span class="sxs-lookup"><span data-stu-id="ce394-181">In the **Main** method of the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

## <a name="select-and-read-package-parts-from-a-package"></a><span data-ttu-id="ce394-182">Выбор и чтение частей пакета из пакета</span><span class="sxs-lookup"><span data-stu-id="ce394-182">Select and read package parts from a package</span></span>
<span data-ttu-id="ce394-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span></span>

<span data-ttu-id="ce394-184">После того как вы откроете файл Visio 2013 как пакет, вы сможете получить доступ к частям документа в файле с помощью класса [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx), включенного в пространство имен **System.IO.Packaging**.</span><span class="sxs-lookup"><span data-stu-id="ce394-184">Once you have the Visio 2013 file open as a package, you can access the document parts within it using the [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) class included in the **System.IO.Packaging** namespace.</span></span> <span data-ttu-id="ce394-185">Создавать экземпляры объектов **PackagePart** можно как отдельно, так и в виде коллекции.</span><span class="sxs-lookup"><span data-stu-id="ce394-185">**PackagePart** objects can be instantiated individually or as a collection.</span></span> <span data-ttu-id="ce394-186">Класс **Package** предоставляет доступ к методам [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) и [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx), с помощью которых можно получить объекты **PackagePart** из объекта **Package**.</span><span class="sxs-lookup"><span data-stu-id="ce394-186">The **Package** class exposes a [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) method and a [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) method for getting **PackagePart** objects out of the **Package**.</span></span> <span data-ttu-id="ce394-187">Метод **Package.GetParts** возвращает экземпляр класса [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx), с которым можно взаимодействовать, как с любой другой коллекцией, реализующей интерфейс [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2).</span><span class="sxs-lookup"><span data-stu-id="ce394-187">The **Package.GetParts** method returns an instance of the [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) class, which you can then interact with like any other collection that implements the [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2) interface.</span></span> 
  
<span data-ttu-id="ce394-188">С помощью кода в указанной ниже процедуре можно получить объект **PackagePartCollection** из объекта **Package** в виде коллекции, выполнить итерацию объектов **PackagePart** в этой коллекции, а затем записать универсальный код ресурса (URI) и тип контента каждого объекта **PackagePart** в консоль.</span><span class="sxs-lookup"><span data-stu-id="ce394-188">Use the code in the following procedure to get a **PackagePartCollection** object from the **Package** as a collection, iterate through the **PackagePart** objects in the collection, and write the URI and content type of each **PackagePart** to the console.</span></span> 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a><span data-ttu-id="ce394-189">Выполнение итерации частей пакета в пакете</span><span class="sxs-lookup"><span data-stu-id="ce394-189">To iterate through the package parts in a package</span></span>

1. <span data-ttu-id="ce394-190">После метода `OpenPackage` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже код.</span><span class="sxs-lookup"><span data-stu-id="ce394-190">After the  `OpenPackage` method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

2. <span data-ttu-id="ce394-191">Добавьте следующий код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic):</span><span class="sxs-lookup"><span data-stu-id="ce394-191">Add the following code inside the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic):</span></span> 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. <span data-ttu-id="ce394-192">Выполните отладку решения, нажав клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="ce394-192">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="ce394-193">По завершении работы программы выйдите из нее, нажав любую клавишу.</span><span class="sxs-lookup"><span data-stu-id="ce394-193">When the program has completed running, choose any key to exit.</span></span>
    
<span data-ttu-id="ce394-194">Консольное приложение создает примерно следующие выходные данные (для краткости часть выходных данных опущена):</span><span class="sxs-lookup"><span data-stu-id="ce394-194">The console application produces output similar to the following (some of the output has been omitted for brevity):</span></span>
  
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
  
<span data-ttu-id="ce394-195">Обычно требуется выбрать один объект **PackagePart**, не выполняя итерацию всех таких объектов.</span><span class="sxs-lookup"><span data-stu-id="ce394-195">More often than not, you need to select one **PackagePart** without having to iterate over all of them.</span></span> <span data-ttu-id="ce394-196">Вы можете получить объект **PackagePart** из объекта **Package**, используя его связь с объектом **Package** или другим объектом **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ce394-196">You can get a **PackagePart** object from a **Package** by using its relationship to the **Package** or another **PackagePart**.</span></span> <span data-ttu-id="ce394-197">В формате файлов Visio 2013 связь представляет собой дискретный объект, который описывает, каким образом часть документа связана с пакетом файла или как две части документа связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="ce394-197">A relationship in the Visio 2013 file format is a discrete entity that describes how a document part relates to the file package or how two document parts relate to each other.</span></span> <span data-ttu-id="ce394-198">Например, сам пакет файла Visio 2013 имеет связь со своей частью Visio Document, а часть Visio Document имеет связь с частью Windows.</span><span class="sxs-lookup"><span data-stu-id="ce394-198">For example, the Visio 2013 file package itself has a relationship to its Visio Document part, and the Visio Document part has a relationship to the Windows part.</span></span> <span data-ttu-id="ce394-199">Эти связи представлены как экземпляры классов [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) или [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce394-199">These relationships are represented as instances of the [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) or [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) classes.</span></span> 
  
<span data-ttu-id="ce394-200">Класс **Package** предоставляет доступ к нескольким методам, которые используются для получения связей и содержатся в нем в виде объектов **PackageRelationship** или **PackageRelationshipCollection**.</span><span class="sxs-lookup"><span data-stu-id="ce394-200">The **Package** class exposes several methods for getting the relationships that it contains as **PackageRelationship** or **PackageRelationshipCollection** objects.</span></span> <span data-ttu-id="ce394-201">С помощью метода [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) вы можете создать экземпляр объекта **PackageRelationshipCollection**, содержащий объекты **PackageRelationship** одного определенного типа.</span><span class="sxs-lookup"><span data-stu-id="ce394-201">You can use the [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) method to instantiate a **PackageRelationshipCollection** object that contains **PackageRelationship** objects of a single specific type.</span></span> <span data-ttu-id="ce394-202">Безусловно, чтобы использовать метод **Package.GetRelationshipsByType**, вы должны знать, какой тип связи необходим вам.</span><span class="sxs-lookup"><span data-stu-id="ce394-202">Of course, using the **Package.GetRelationshipsByType** method requires that you already know the relationship type that you need.</span></span> <span data-ttu-id="ce394-203">Типы связей представляют собой строки в формате пространства имен XML.</span><span class="sxs-lookup"><span data-stu-id="ce394-203">Relationship types are strings in XML namespace format.</span></span> <span data-ttu-id="ce394-204">Например, тип связи части Visio Document — http://schemas.microsoft.com/visio/2010/relationships/document.</span><span class="sxs-lookup"><span data-stu-id="ce394-204">For example, the relationship type of the Visio Document part is http://schemas.microsoft.com/visio/2010/relationships/document.</span></span> 
  
<span data-ttu-id="ce394-205">После того как вы получите сведения о связи объекта **PackagePart** с объектом **Package** или другим объектом **PackagePart** (то есть когда у вас будет объект **PackageRelationship**, который ссылается на необходимый вам объект **PackagePart**), вы сможете использовать эту связь для получения универсального кода ресурса (URI) этого объекта **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ce394-205">Once you know the relationship of a **PackagePart** to the **Package** or to another **PackagePart** (that is, you have a **PackageRelationship** object that references the **PackagePart** that you want), you can use that relationship to get the URI of that **PackagePart**.</span></span> <span data-ttu-id="ce394-206">После этого можно передать универсальный код ресурса (URI) в метод **Package.GetPart**, чтобы возвратить объект **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ce394-206">You then pass the URI to the **Package.GetPart** method to return the **PackagePart**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ce394-207">Кроме того, вы можете получить ссылку на определенный объект **PackagePart**, используя только метод **Package.GetPart** и универсальный код ресурса (URI) объекта **PackagePart**. В этом случае можно исключить этап получения связей части пакета.</span><span class="sxs-lookup"><span data-stu-id="ce394-207">You can also get a reference to a specific **PackagePart** by using just the **Package.GetPart** method and the URI of the **PackagePart**, bypassing the step where you get the package part's relationships.</span></span> <span data-ttu-id="ce394-208">Некоторые части пакета в пакете файла Visio можно сохранять в расположения, отличные от расположений, используемых по умолчанию, в пакете.</span><span class="sxs-lookup"><span data-stu-id="ce394-208">However, some package parts in the Visio file package can be saved to locations other than their default locations in a package.</span></span> <span data-ttu-id="ce394-209">Не следует рассчитывать на то, что часть пакета всегда будет расположена в одном и том же универсальном коде ресурса (URI) для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="ce394-209">You cannot assume that a package part is always located at the same URI for every file.</span></span> <span data-ttu-id="ce394-210">> Вместо этого для доступа к отдельным объектам **PackagePart** рекомендуется использовать связи.</span><span class="sxs-lookup"><span data-stu-id="ce394-210">> Instead, it is a best practice to use relationships to access individual **PackagePart** objects.</span></span> 
  
<span data-ttu-id="ce394-211">Выполните указанные ниже действия, чтобы получить объект **PackagePart** (часть Visio Document), используя объект **PackageRelationship** из объекта **Package**, который ссылается на часть.</span><span class="sxs-lookup"><span data-stu-id="ce394-211">Use the following procedure to get a **PackagePart** (the Visio Document part) by using the **PackageRelationship** from the **Package** that references the part.</span></span> 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a><span data-ttu-id="ce394-212">Выбор определенной части пакета в пакете с использованием связи</span><span class="sxs-lookup"><span data-stu-id="ce394-212">To select a specific package part in the package by relationship</span></span>

1. <span data-ttu-id="ce394-213">После метода `IteratePackageParts` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-213">After the  `IteratePackageParts` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
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

2. <span data-ttu-id="ce394-214">Замените код в блоке **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) указанным ниже кодом.</span><span class="sxs-lookup"><span data-stu-id="ce394-214">Replace the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
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

<span data-ttu-id="ce394-215">Как было сказано выше, вы также можете получать объекты **PackagePart**, используя их связи с другими объектами **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ce394-215">As mentioned previously, you can also get **PackagePart** objects by using their relationship to other **PackagePart** objects.</span></span> <span data-ttu-id="ce394-216">Это важно, так как в документах Visio любой сложности у большинства объектов **PackagePart** нет связи с объектом **Package**.</span><span class="sxs-lookup"><span data-stu-id="ce394-216">This is important because, for a Visio document of any complexity, most of the **PackagePart** objects don't have a relationship to the **Package**.</span></span> <span data-ttu-id="ce394-217">Например, у отдельной части Page Content в пакете файла (то есть /visio/pages/page1.xml) имеется связь с частью Page Index (то есть /visio/pages/pages.xml), но не с самим пакетом файла.</span><span class="sxs-lookup"><span data-stu-id="ce394-217">For example, an individual Page Content part in the file package (that is, /visio/pages/page1.xml) has a relationship to the Page Index part (that is, /visio/pages/pages.xml) but not to the file package itself.</span></span> <span data-ttu-id="ce394-218">Если у вас нет точного универсального кода ресурса (URI) отдельной страницы в пакете, вы можете использовать ее связь с частью Page Index, чтобы получить ссылку на нее.</span><span class="sxs-lookup"><span data-stu-id="ce394-218">If you don't have the exact URI of the individual page in the package, you can use its relationship to the Page Index part to get a reference to it.</span></span>
  
<span data-ttu-id="ce394-219">Класс **PackagePart** предоставляет доступ к методу [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx), который можно использовать для возврата объекта **PackageRelationshipCollection**, содержащего объект **PackageRelationship** только одного типа.</span><span class="sxs-lookup"><span data-stu-id="ce394-219">The **PackagePart** class exposes a [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) method that you can use to return a **PackageRelationshipCollection** object that contains only one type of **PackageRelationship** object.</span></span> <span data-ttu-id="ce394-220">Если у вас есть объект **PackageRelationshipCollection**, вы можете выбрать необходимый вам объект **PackageRelationship** из коллекции и сослаться на объект **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ce394-220">Once you have the **PackageRelationshipCollection**, you can select the **PackageRelationship** that you need from the collection and then reference the **PackagePart** object.</span></span> 
  
<span data-ttu-id="ce394-221">С помощью указанного ниже кода можно получить объект **PackagePart** из объекта **Package**, используя его связь с другим объектом **PackagePart** (получив объект **PackageRelationship** из последнего).</span><span class="sxs-lookup"><span data-stu-id="ce394-221">Use the following code to get a **PackagePart** from the **Package** by using its relationship to (getting a **PackageRelationship** object from) another **PackagePart**.</span></span>
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a><span data-ttu-id="ce394-222">Выбор определенной части пакета с использованием ее связи с другой частью пакета</span><span class="sxs-lookup"><span data-stu-id="ce394-222">To select a specific package part through its relationship to another package part</span></span>

1. <span data-ttu-id="ce394-223">После метода `GetPackagePart` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже метод перегрузки.</span><span class="sxs-lookup"><span data-stu-id="ce394-223">After the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following overload method.</span></span> 
    
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

2. <span data-ttu-id="ce394-224">Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) после кода, указанного в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="ce394-224">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> <span data-ttu-id="ce394-225">(Не удаляйте код, который вы добавили в предыдущей процедуре.)</span><span class="sxs-lookup"><span data-stu-id="ce394-225">(Do not delete the code that you added in the previous procedure.)</span></span> 
    
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

<span data-ttu-id="ce394-226">Чтобы можно было вносить изменения в XML, включенный в часть документа, необходимо сначала загрузить документ XML в объект, который позволяет читать XML c помощью классов [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) или [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce394-226">Before you can make changes to the XML included in a document part, you need to first load the XML document into an object that allows you to read the XML, using the [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) class or [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) class.</span></span> <span data-ttu-id="ce394-227">Оба эти класса предоставляют доступ к методам, используемым для решения таких задач, как выбор элементов XML, содержащихся в документах XML, создание, чтение и запись атрибутов, а также вставка новых элементов XML в документ.</span><span class="sxs-lookup"><span data-stu-id="ce394-227">Both classes expose methods for tasks such as selecting XML elements contained within the XML documents; creating, reading, and writing attributes; and inserting new XML elements into a document.</span></span> 
  
<span data-ttu-id="ce394-228">С помощью класса **XDocument** можно создавать запросы к XML, используя LINQ.</span><span class="sxs-lookup"><span data-stu-id="ce394-228">Of the two, the **XDocument** class allows you to query the XML using LINQ.</span></span> <span data-ttu-id="ce394-229">Используя LINQ, можно легко выбирать отдельные элементы из документа XML, создавая запросы, а не выполняя итерацию всех элементов в коллекции и не проверяя их, чтобы выбрать необходимые элементы.</span><span class="sxs-lookup"><span data-stu-id="ce394-229">With LINQ, you can easily select individual elements from an XML document by creating queries, rather than iterating over all of the elements in a collection and testing for the elements that you need.</span></span> <span data-ttu-id="ce394-230">По этим причинам в процедурах, описанных ниже в этой статье, для работы с XML используется класс **XDocument** и другие классы пространства имен **System.Xml.Linq**.</span><span class="sxs-lookup"><span data-stu-id="ce394-230">For these reasons, the following procedures in this article use the **XDocument** class and other classes of the **System.Xml.Linq** namespace for working with XML.</span></span> 
  
<span data-ttu-id="ce394-231">С помощью указанных ниже процедур можно открыть объект **PackagePart** как документ XML в объекте **XDocument**.</span><span class="sxs-lookup"><span data-stu-id="ce394-231">Use the following procedure to open a **PackagePart** as an XML document in an **XDocument** object.</span></span> 
  
### <a name="to-read-the-xml-in-a-package-part"></a><span data-ttu-id="ce394-232">Чтение XML в части пакета</span><span class="sxs-lookup"><span data-stu-id="ce394-232">To read the XML in a package part</span></span>

1. <span data-ttu-id="ce394-233">После последней перегрузки для метода `GetPackagePart` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-233">After the last overload for the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
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

2. <span data-ttu-id="ce394-234">Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) после кода, указанного в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="ce394-234">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Open the XML from the Page Contents part.
    XDocument pageXML = GetXMLFromPart(pagePart);
    ```

    ```vb
    ' Open the XML from the Page Contents part.
    Dim pageXML As XDocument = GetXMLFromPart(pagePart)
    ```

## <a name="select-and-change-xml-data-in-a-package-part"></a><span data-ttu-id="ce394-235">Выбор и изменение данных XML в части пакета</span><span class="sxs-lookup"><span data-stu-id="ce394-235">Select and change XML data in a package part</span></span>
<span data-ttu-id="ce394-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span></span>

<span data-ttu-id="ce394-237">После загрузки части документа в объект **XDocument** для выбора элементов XML и внесения изменений в документ XML можно использовать LINQ.</span><span class="sxs-lookup"><span data-stu-id="ce394-237">Once you have loaded a document part into an **XDocument** object, you can use LINQ to select XML elements and make changes to the XML document.</span></span> <span data-ttu-id="ce394-238">Вы можете изменять данные XML, добавлять или удалять данные, а затем сохранять документ XML обратно в часть документа.</span><span class="sxs-lookup"><span data-stu-id="ce394-238">You can change XML data, add or remove data, and then save the XML document back to the document part.</span></span> 
  
<span data-ttu-id="ce394-239">Самая распространенная задача управления форматом файлов Visio — выбор определенных элементов или коллекций элементов XML в документе.</span><span class="sxs-lookup"><span data-stu-id="ce394-239">The most common task for manipulating the Visio file format is selecting specific XML elements or collections of elements in the document.</span></span> <span data-ttu-id="ce394-240">Пространство имен **System.Xml.Linq** включает класс [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx), который представляет элемент XML.</span><span class="sxs-lookup"><span data-stu-id="ce394-240">The **System.Xml.Linq** namespace includes the [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) class, which represents an XML element.</span></span> <span data-ttu-id="ce394-241">С помощью класса **XElement** можно на детальном уровне получить доступ к данным, содержащимся в файле Visio, от отдельных элементов **Shape** до элементов **ValidationRule** (в качестве примера).</span><span class="sxs-lookup"><span data-stu-id="ce394-241">The **XElement** class gives you access to the data contained in the Visio file at a granular level, from individual **Shape** elements to **ValidationRule** elements (as examples).</span></span> 
  
<span data-ttu-id="ce394-242">С помощью указанного ниже кода можно выбрать элементы **Shape** из объекта **XDocument** (содержащего часть Page Contents), а затем выбрать определенный элемент **Shape**.</span><span class="sxs-lookup"><span data-stu-id="ce394-242">Use the following code to select the **Shape** elements from an **XDocument** (containing a Page Contents part) and to then select a specific **Shape** element.</span></span> 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a><span data-ttu-id="ce394-243">Выбор определенного элемента в части пакета</span><span class="sxs-lookup"><span data-stu-id="ce394-243">To select a specific element in a package part</span></span>

1. <span data-ttu-id="ce394-244">После метода `GetXMLFromPart` в классе **Program** (или **Module1** в Visual Basic) добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-244">After the  `GetXMLFromPart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
        
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

2. <span data-ttu-id="ce394-245">После метода `GetXElementsByName` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-245">After the  `GetXElementsByName` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="ce394-246">Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) после кода, указанного в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="ce394-246">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
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

<span data-ttu-id="ce394-247">После получения ссылки на объект **XElement**, содержащийся в объекте **XDocument**, вы можете управлять им, как и любыми другими данными XML, и, соответственно, изменять данные, содержащиеся в файле Visio.</span><span class="sxs-lookup"><span data-stu-id="ce394-247">Once you have gotten a reference to a **XElement** object contained within an **XDocument** object, you can manipulate it like any other XML data and, thereby, change the data contained in the Visio file.</span></span> <span data-ttu-id="ce394-248">Например, если при открытии в Visio у какой-либо фигуры имеется текст, соответствующий элемент **Shape** будет содержать по крайней мере один элемент **Text**.</span><span class="sxs-lookup"><span data-stu-id="ce394-248">For example, if a shape has text when it is opened in Visio, the corresponding **Shape** element will contain at least one **Text** element.</span></span> <span data-ttu-id="ce394-249">Если вы измените значение этого элемента **Text**, то при просмотре файла в Visio у текст фигуры изменится.</span><span class="sxs-lookup"><span data-stu-id="ce394-249">If you change the value of that **Text** element, the shape's text is changed when the file is viewed in Visio.</span></span> 
  
<span data-ttu-id="ce394-250">Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic), чтобы изменить текст в фигуре Start/End (Начало/конец) с Begin process (Начать процесс) на Start process (Запустить процесс).</span><span class="sxs-lookup"><span data-stu-id="ce394-250">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) to change the text in the Start/End shape from "Begin process" to "Start process".</span></span> 
  
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
> <span data-ttu-id="ce394-251">В предыдущем примере кода существующий текст фигуры и строка, используемая для его замены, содержат одинаковое количество символов.</span><span class="sxs-lookup"><span data-stu-id="ce394-251">In the previous code example, the existing shape text and the string used to replace it have the same number of characters.</span></span> <span data-ttu-id="ce394-252">Кроме того, обратите внимание на то, что запрос LINQ изменяет значение последнего дочернего узла возвращаемого элемента (который в данном случае представляет собой текстовый узел).</span><span class="sxs-lookup"><span data-stu-id="ce394-252">Also note that the LINQ query changes the value of the last child node of the returned element (which, in this case, is a text node).</span></span> <span data-ttu-id="ce394-253">Это сделано, чтобы не допустить изменения параметров элемента **cp**, который представляет собой дочерний элемент элемента **Text**.</span><span class="sxs-lookup"><span data-stu-id="ce394-253">This is done to avoid changing the settings of the **cp** element that is a child of the **Text** element.</span></span> <span data-ttu-id="ce394-254">> Если программно изменить текст фигуры путем перезаписи всех дочерних элементов элемента **Text**, это может привести к нестабильности файла.</span><span class="sxs-lookup"><span data-stu-id="ce394-254">> It is possible to cause file instability if you alter shape text programmatically by overwriting all children of the **Text** element.</span></span> <span data-ttu-id="ce394-255">Как показано в примере выше, форматирование текста представлено элементами **cp** в элементе **Text** в файле.</span><span class="sxs-lookup"><span data-stu-id="ce394-255">As in the example above, the text formatting is represented by **cp** elements under the **Text** element in the file.</span></span> <span data-ttu-id="ce394-256">Определение форматирования хранится в родительском элементе **Section**.</span><span class="sxs-lookup"><span data-stu-id="ce394-256">The definition of the formatting is stored in the parent **Section** element.</span></span> <span data-ttu-id="ce394-257">Если эти два элемента информации станут несогласованными, файл может вести себя непредсказуемо.</span><span class="sxs-lookup"><span data-stu-id="ce394-257">If these two pieces of information become inconsistent, then the file may not behave as expected.</span></span> <span data-ttu-id="ce394-258">Приложение Visio исправляет многие виды несогласованности, но лучше убедиться, что все изменения, внесенные программным способом, согласованы. В этом случае вы сможете контролировать поведение файла.</span><span class="sxs-lookup"><span data-stu-id="ce394-258">Visio heals many inconsistencies, but it is better to ensure that any programmatic changes are consistent so that you are controlling the ultimate behavior of the file.</span></span> 
  
<span data-ttu-id="ce394-259">Когда вы вносите изменения в XML части документа, эти изменения хранятся только в памяти.</span><span class="sxs-lookup"><span data-stu-id="ce394-259">When you make changes to the XML of a document part, those changes exist in memory only.</span></span> <span data-ttu-id="ce394-260">Чтобы сохранить их в файл, необходимо сохранить XML обратно в часть документа.</span><span class="sxs-lookup"><span data-stu-id="ce394-260">To persist the changes in the file, you must save the XML back to the document part.</span></span>
  
<span data-ttu-id="ce394-261">В указанном ниже коде показано, как с помощью классов [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) и [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) записать XML обратно в часть пакета.</span><span class="sxs-lookup"><span data-stu-id="ce394-261">The following code uses the [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) class and [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) class to write the XML back to the package part.</span></span> <span data-ttu-id="ce394-262">Несмотря на то что для сохранения XML обратно в часть можно использовать метод [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx), классы **XmlWriter** и **XmlWriterSettings** позволяют более тонко управлять выводом данных, в том числе указывать тип кодировки.</span><span class="sxs-lookup"><span data-stu-id="ce394-262">Although you can use the [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) method to save the XML back to the part, the **XmlWriter** and **XmlWriterSettings** classes allow you finer control over the output, including specifying the type of encoding.</span></span> <span data-ttu-id="ce394-263">Класс **XDocument** предоставляет доступ к методу [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx), который берет объект **XmlWriter** и записывает XML обратно в поток.</span><span class="sxs-lookup"><span data-stu-id="ce394-263">The **XDocument** class exposes a [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) method that takes an **XmlWriter** object and writes XML back to a stream.</span></span> 
  
<span data-ttu-id="ce394-264">С помощью указанных ниже действий можно сохранить XML из страницы Visio обратно в часть Page Contents.</span><span class="sxs-lookup"><span data-stu-id="ce394-264">Use the following procedure to save the XML from the Visio page back to the Page Contents part.</span></span>
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a><span data-ttu-id="ce394-265">Сохранение измененного XML обратно в пакет</span><span class="sxs-lookup"><span data-stu-id="ce394-265">To save the changed XML back to the package</span></span>

1. <span data-ttu-id="ce394-266">После метода `GetXElementByAttribute` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-266">After the  `GetXElementByAttribute` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

2. <span data-ttu-id="ce394-267">Добавьте указанный ниже код в блок **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) после кода, указанного в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="ce394-267">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. <span data-ttu-id="ce394-268">Выполните отладку решения, нажав клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="ce394-268">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="ce394-269">По завершении работы программы выйдите из нее, нажав любую клавишу.</span><span class="sxs-lookup"><span data-stu-id="ce394-269">When the program has completed running, choose any key to exit.</span></span>
    
4. <span data-ttu-id="ce394-270">Откройте файл Visio Package.vsdx в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ce394-270">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="ce394-271">Теперь фигура "Начало/конец" должна содержать текст Start process (Запустить процесс).</span><span class="sxs-lookup"><span data-stu-id="ce394-271">The Start/End shape should now contain the text "Start process".</span></span>
  
## <a name="recalculate-data-in-the-file"></a><span data-ttu-id="ce394-272">Пересчет данных в файле</span><span class="sxs-lookup"><span data-stu-id="ce394-272">Recalculate data in the file</span></span>
<span data-ttu-id="ce394-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span></span>

<span data-ttu-id="ce394-274">При внесении некоторых изменений в данные в файле приложению Visio может потребоваться пересчитать документ при открытии файла.</span><span class="sxs-lookup"><span data-stu-id="ce394-274">Some changes to the data in a file may require Visio to recalculate the document when it opens the file.</span></span> <span data-ttu-id="ce394-275">В Visio имеется большое количество логики для схем, особенно для связей фигур (то есть когда одна фигура зависит от другой) и соединения фигур.</span><span class="sxs-lookup"><span data-stu-id="ce394-275">Visio provides a lot of logic for a diagram, particularly for shape relationships (that is, when one shape depends on another) and connecting shapes.</span></span> <span data-ttu-id="ce394-276">Если изменить какие-либо данные, которые используются в пользовательской логике, приложению Visio потребуется распространить изменения на все затронутые вычисляемые данные в файле.</span><span class="sxs-lookup"><span data-stu-id="ce394-276">If any of the data that the custom logic relies upon is changed, Visio needs to propagate the changes to all of the affected calculated data in the file.</span></span> 
  
<span data-ttu-id="ce394-277">Формат файла Visio 2013 включает пару методов, которые вы можете использовать для пересчета данных в файле.</span><span class="sxs-lookup"><span data-stu-id="ce394-277">The Visio 2013 file format includes a couple of techniques that you can use to recalculate data in the file.</span></span> <span data-ttu-id="ce394-278">Существует три типа сценариев, которые необходимо учесть, принимая решение о том, необходимо ли выполнить пересчет в файле Visio, и о том, как сделать это.</span><span class="sxs-lookup"><span data-stu-id="ce394-278">There are three types of scenarios that you must consider when you decide whether you need to recalculate the Visio file and how to do it:</span></span>
  
- <span data-ttu-id="ce394-279">Изменения данных не затрагивают другие значения в формате файла.</span><span class="sxs-lookup"><span data-stu-id="ce394-279">The changes to the data do not affect any other values in the file format.</span></span> <span data-ttu-id="ce394-280">Вам не нужно добавлять дополнительные инструкции в Visio для пересчета документа.</span><span class="sxs-lookup"><span data-stu-id="ce394-280">You don't need to add any additional instructions to Visio to recalculate the document.</span></span> <span data-ttu-id="ce394-281">Как было показано выше, вы можете часто изменять текст фигуры без необходимости пересчитывать документ.</span><span class="sxs-lookup"><span data-stu-id="ce394-281">As demonstrated previously, you can often change a shape's text without needing to recalculate the document.</span></span>
    
- <span data-ttu-id="ce394-282">Изменения данных ограничиваются изменением значений ячеек ShapeSheet в XML и при этом имеются другие значения ShapeSheet, зависящие от этих данных.</span><span class="sxs-lookup"><span data-stu-id="ce394-282">The changes to the data are limited to changing the values of ShapeSheet cells in the XML, and there are other ShapeSheet values that depend on this data.</span></span> <span data-ttu-id="ce394-283">В этом случае необходимо добавить инструкцию по обработке XML (используя класс [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)) в элемент **Cell**, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="ce394-283">In this case, you must add an XML processing instruction (using the [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) class) to the **Cell** element that has been changed.</span></span> <span data-ttu-id="ce394-284">Например, ячейка **ThemeIndex** для фигуры влияет на значения нескольких других ячеек ShapeSheet, содержащихся в фигуре.</span><span class="sxs-lookup"><span data-stu-id="ce394-284">For example, the **ThemeIndex** cell for a shape affects the values of several other ShapeSheet cells contained in the shape.</span></span> <span data-ttu-id="ce394-285">Если вы измените ячейку **ThemeIndex** в самом файле (например, элемент **Cell** со значением **N**, равным ThemeIndex), то для обновления зависимых значений вам придется добавить инструкцию по обработке в элемент **Cell**.</span><span class="sxs-lookup"><span data-stu-id="ce394-285">If you change the **ThemeIndex** cell within the file itself (for example, the **Cell** element with an **N** value of "ThemeIndex"), you will need to add a processing instruction to the **Cell** element so that the dependent values are updated.</span></span> 
    
- <span data-ttu-id="ce394-286">Изменения данных влияют на расположение соединительных линий или точек соединений.</span><span class="sxs-lookup"><span data-stu-id="ce394-286">The changes to the data affect the location of a connector or connection points.</span></span> <span data-ttu-id="ce394-287">Вот еще одна ситуация: в данные ShapeSheet внесено много изменений, и вы хотите пересчитать весь документ с помощью одной инструкции (а не добавлять отдельные инструкции по обработке для каждого изменения).</span><span class="sxs-lookup"><span data-stu-id="ce394-287">Another situation is when there are many changes to the ShapeSheet data and you want to recalculate the whole document with one instruction (rather than adding individual processing instructions for each change).</span></span> <span data-ttu-id="ce394-288">В этом случае вы можете дать приложению Visio указание пересчитать весь документ при открытии документа.</span><span class="sxs-lookup"><span data-stu-id="ce394-288">In this case you can instruct Visio to recalculate the entire document when it is opened.</span></span> <span data-ttu-id="ce394-289">Для этого добавьте свойство **RecalcDocument** в часть Custom File Properties (/docProps/custom.xml) пакета Visio.</span><span class="sxs-lookup"><span data-stu-id="ce394-289">You do this by adding a **RecalcDocument** property to the Custom File Properties part (/docProps/custom.xml) of the Visio package.</span></span> <span data-ttu-id="ce394-290">Пример сценария такого типа — изменение положения или размера фигур на связанной схеме.</span><span class="sxs-lookup"><span data-stu-id="ce394-290">Adjusting the position or size of shapes in a connected diagram is an example of this type of scenario.</span></span> 
    
    <span data-ttu-id="ce394-291">Учтите, что это самый затратный вариант с точки рения производительности.</span><span class="sxs-lookup"><span data-stu-id="ce394-291">Keep in mind that this is the most costly option from a performance standpoint.</span></span>
    
<span data-ttu-id="ce394-292">Выполните указанные ниже действия, чтобы вставить элемент **Cell** в элемент **Shape**, где из-за нового значения необходимо пересчитать другие элементы **Cell** в том же объекте **Shape**.</span><span class="sxs-lookup"><span data-stu-id="ce394-292">Use the following procedure to insert a **Cell** element into a **Shape** element, where other **Cell** elements in the same **Shape** need to be recalculated because of the new value.</span></span> <span data-ttu-id="ce394-293">Новый элемент **Cell** включает инструкцию по обработке в виде дочернего элемента. Это позволяет сообщить приложению Visio о том, что необходимо выполнить локальный пересчет.</span><span class="sxs-lookup"><span data-stu-id="ce394-293">The new **Cell** element includes a processing instruction as a child element, to inform Visio that it needs to perform some local recalculation.</span></span> 
  
### <a name="to-recalculate-values-for-a-single-shape"></a><span data-ttu-id="ce394-294">Пересчет значений для одной фигуры</span><span class="sxs-lookup"><span data-stu-id="ce394-294">To recalculate values for a single shape</span></span>

1. <span data-ttu-id="ce394-295">Замените код из двух предыдущих примеров (изменение текста фигуры и вызов метода `SaveXDocumentToPart`) в блоке **using** в методе **Main** класса **Program** (в блоке **Using** метода **Main** в модуле **Module1** в Visual Basic) указанным ниже кодом.</span><span class="sxs-lookup"><span data-stu-id="ce394-295">Replace the code from the previous two examples (changing the shape's text and the call to  `SaveXDocumentToPart`) in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
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

2. <span data-ttu-id="ce394-296">Выполните отладку решения, нажав клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="ce394-296">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="ce394-297">По завершении работы программы выйдите из нее, нажав любую клавишу.</span><span class="sxs-lookup"><span data-stu-id="ce394-297">When the program has completed running, choose any key to exit.</span></span>
    
3. <span data-ttu-id="ce394-298">Откройте файл Visio Package.vsdx в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ce394-298">Open the Visio Package.vsdx file in Visio 2013.</span></span> <span data-ttu-id="ce394-299">Теперь у фигуры "Начало/конец" должен быть другой цвет заливки.</span><span class="sxs-lookup"><span data-stu-id="ce394-299">The Start/End shape should now have a different fill color.</span></span>
    
<span data-ttu-id="ce394-300">Цвет фигуры зависит от значения ячейки **ThemeIndex**: оно определяет активную тему, из которой фигура наследует параметры.</span><span class="sxs-lookup"><span data-stu-id="ce394-300">The shape's color relies on the value of the **ThemeIndex** cell—it determines which of the active themes the shape inherits from.</span></span> <span data-ttu-id="ce394-301">В предыдущем примере фигура настроена так, чтобы наследовать параметры другой темы (ячейка **ThemeIndex** имеет значение 25).</span><span class="sxs-lookup"><span data-stu-id="ce394-301">In the previous example, the shape is set to inherit from a different theme (the **ThemeIndex** cell is set to a value of "25").</span></span> <span data-ttu-id="ce394-302">Если вы не используете инструкцию по обработке, цвет текста фигуры (который также зависит от значения ячейки **ThemeIndex**) не будет пересчитан.</span><span class="sxs-lookup"><span data-stu-id="ce394-302">If you don't use a processing instruction, the shape's text color—which is also affected by the **ThemeIndex** cell—isn't recalculated.</span></span> <span data-ttu-id="ce394-303">Цвет заливки фигуры изменится на белый, а текст будет по-прежнему белый и станет нечитаемым.</span><span class="sxs-lookup"><span data-stu-id="ce394-303">The shape's fill color would change to white, but its text would remain white—leaving the text unreadable.</span></span> <span data-ttu-id="ce394-304">Кроме того, если не использовать инструкцию по обработке, Visio может обновить фигуру позже, и файл будет в нестабильном состоянии, при котором значения параметров форматирования фигуры могут быть обновлены непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="ce394-304">Also, without the processing instruction, it is possible that Visio may update the shape at a later date, leaving the file in an unstable state where the formatting values of the shape could be updated unpredictably.</span></span> 
  
<span data-ttu-id="ce394-305">Если вы изменяете данные в файле таким образом, что приложению Visio требуется пересчитать документ (например, изменяете положение связанной фигуры, из-за чего приложению Visio необходимо принудительно изменить маршруты соединительных линий), вам необходимо добавить инструкцию по пересчету в файл Visio.</span><span class="sxs-lookup"><span data-stu-id="ce394-305">If you change data in the file that requires Visio to recalculate the document (for example, changing a connected shape's position and, therefore, forcing the connectors to reroute), you must add a recalculation instruction to the Visio file.</span></span> <span data-ttu-id="ce394-306">Чтобы создать инструкцию, добавьте элемент **property**, атрибут **name** которого имеет значение RecalcDocument, в XML в часть Custom File Properties пакета файла Visio.</span><span class="sxs-lookup"><span data-stu-id="ce394-306">The instruction is created by adding a **property** element with a **name** attribute value of "RecalcDocument" to the XML of the Custom File Properties part of the Visio file package.</span></span> <span data-ttu-id="ce394-307">Рекомендуется проверить часть Custom File Properties и убедиться, что инструкция RecalcDocument еще не зарегистрирована в файле.</span><span class="sxs-lookup"><span data-stu-id="ce394-307">As a best practice, you should check the Custom File Properties part to be sure that a "RecalcDocument" instruction hasn't already been registered in the file.</span></span> 
  
<span data-ttu-id="ce394-308">С помощью указанного ниже кода можно изменить значение ячейки **PinY** фигуры "Начало/конец" из предыдущих примеров.</span><span class="sxs-lookup"><span data-stu-id="ce394-308">Use the following code to change the value of the **PinY** cell of the Start/End shape from the previous examples.</span></span> <span data-ttu-id="ce394-309">Этот код выбирает элемент **Cell**, который содержит данные ячейки **PinY** в виде объекта **XElement**, путем использования значения его атрибута **N**.</span><span class="sxs-lookup"><span data-stu-id="ce394-309">The code selects the **Cell** element that contains the **PinY** cell data as an **XElement** object by using the value of its **N** attribute.</span></span> <span data-ttu-id="ce394-310">Затем код добавляет инструкцию по пересчету в часть Custom File Properties файла Visio.</span><span class="sxs-lookup"><span data-stu-id="ce394-310">The code then adds a recalculation instruction to the Custom File Properties part of the Visio file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ce394-311">В этом коде используются созданные ранее в этой статье методы `GetPackagePart` и `SaveXDocumentToPart`.</span><span class="sxs-lookup"><span data-stu-id="ce394-311">This code relies on the  `GetPackagePart` and  `SaveXDocumentToPart` methods created previously.</span></span> 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a><span data-ttu-id="ce394-312">Пересчет всего документа, когда он открыт</span><span class="sxs-lookup"><span data-stu-id="ce394-312">To recalculate the entire document when it is opened</span></span>

1. <span data-ttu-id="ce394-313">После метода `SaveXDocumentToPart` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-313">After the  `SaveXDocumentToPart` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
    ```cs
    private static void RecalcDocument(Package filePackage)
    {
        // Get the Custom File Properties part from the package and
        // and then extract the XML from it.
        PackagePart customPart = GetPackagePart(filePackage, 
            "https://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
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
                "https://schemas.openxmlformats.org/officeDocument/2006/" + _
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

2. <span data-ttu-id="ce394-314">После метода `RecalcDocument` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-314">After the  `RecalcDocument` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="ce394-315">Замените код из предыдущего примера в блоке **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) указанным ниже кодом.</span><span class="sxs-lookup"><span data-stu-id="ce394-315">Replace the code from the previous example in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
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

4. <span data-ttu-id="ce394-316">Выполните отладку решения, нажав клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="ce394-316">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="ce394-317">По завершении работы программы выйдите из нее, нажав любую клавишу.</span><span class="sxs-lookup"><span data-stu-id="ce394-317">When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="ce394-318">Откройте файл Visio Package.vsdx в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="ce394-318">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="ce394-319">Теперь фигура "Начало/конец" должна быть расположена в 2 дюймах от верхнего края схемы.</span><span class="sxs-lookup"><span data-stu-id="ce394-319">The Start/End shape should now be 2 inches from the bottom edge of the drawing.</span></span> <span data-ttu-id="ce394-320">Маршрут соединительной линии между фигурами "Начало/конец" и "Процесс" должен быть изменен согласно изменениям макета.</span><span class="sxs-lookup"><span data-stu-id="ce394-320">The connector between the Start/End shape and the Process shape should have rerouted to accommodate the change in layout.</span></span> <span data-ttu-id="ce394-321">Если не добавить свойство **RecalcDocument** в файл, положение фигуры изменится, а маршрут соединительной линии не будет изменен, и соединительная линия не будет вести к новому расположению фигуры.</span><span class="sxs-lookup"><span data-stu-id="ce394-321">If the **RecalcDocument** property had not been added to the file, the shape position would have been changed, but the connector would not have rerouted to the new location of the shape.</span></span> 
  
## <a name="add-a-new-package-part-to-a-package"></a><span data-ttu-id="ce394-322">Добавление новой части пакета в пакет</span><span class="sxs-lookup"><span data-stu-id="ce394-322">Add a new package part to a package</span></span>
<span data-ttu-id="ce394-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span></span>

<span data-ttu-id="ce394-324">Один из самых распространенных сценариев изменения пакета файла — добавление новой части документа в пакет.</span><span class="sxs-lookup"><span data-stu-id="ce394-324">One of the most common scenarios for modifying a file package is adding a new document part to the package.</span></span> <span data-ttu-id="ce394-325">Например, если вы хотите добавить страницу в документ Visio путем добавления контента в пакет, вам потребуется добавить часть Page Contents в пакет.</span><span class="sxs-lookup"><span data-stu-id="ce394-325">For example, if you want to add a page to the Visio drawing by adding content to the package, you need to add a Page Contents part to the package.</span></span> 
  
<span data-ttu-id="ce394-326">Процесс добавления новой части в пакет прост.</span><span class="sxs-lookup"><span data-stu-id="ce394-326">The process for adding a new part to the package is straightforward:</span></span> 
  
1. <span data-ttu-id="ce394-327">Создайте документ XML с данными для объекта **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ce394-327">You create the XML document with the data for the **PackagePart**.</span></span> <span data-ttu-id="ce394-328">Уделите особое внимание пространствам имен XML, управляющим схемой для определенного типа документа XML, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="ce394-328">You need to pay special attention to the XML namespaces that govern the schema for the specific type of XML document that you create.</span></span>
    
2. <span data-ttu-id="ce394-329">Создайте файл, в котором будет содержаться XML, и сохраните его в расположение в объекте **Package**.</span><span class="sxs-lookup"><span data-stu-id="ce394-329">You create a new file to contain the XML and save the file to a location in the **Package**.</span></span>
    
3. <span data-ttu-id="ce394-330">Создайте необходимые связи между новым объектом **PackagePart** и объектом **Package** или другими объектами **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="ce394-330">You create the necessary relationships between the new **PackagePart** and the **Package** or other **PackagePart** objects.</span></span> 
    
4. <span data-ttu-id="ce394-331">Обновите все существующие части, которые должны ссылаться на новую часть.</span><span class="sxs-lookup"><span data-stu-id="ce394-331">You update any existing parts that need to reference the new part.</span></span> <span data-ttu-id="ce394-332">Например, если вы добавляете новую часть Page Contents (новую страницу) в файл, вам потребуется обновить часть Page Index (файл /visio/pages/pages.xml), чтобы она включала правильные сведения о новой странице.</span><span class="sxs-lookup"><span data-stu-id="ce394-332">For example, if you add a new Page Contents part (a new page) to the file, you also need to update the Page Index part (/visio/pages/pages.xml file) to include the correct information about the new page.</span></span>
    
<span data-ttu-id="ce394-333">Выполните указанные ниже действия, чтобы создать часть Ribbon Extensibility в файле Visio.</span><span class="sxs-lookup"><span data-stu-id="ce394-333">Use the following procedure to create a new Ribbon Extensibility part in the Visio file.</span></span> <span data-ttu-id="ce394-334">Новая часть Ribbon Extensibility добавляет на ленту новую вкладку с одной группой, содержащей одну кнопку.</span><span class="sxs-lookup"><span data-stu-id="ce394-334">The new Ribbon Extensibility part adds to the ribbon a new tab with a single group that contains a single button.</span></span>
  
### <a name="to-create-a-new-package-part"></a><span data-ttu-id="ce394-335">Создание части пакета</span><span class="sxs-lookup"><span data-stu-id="ce394-335">To create a new package part</span></span>

1. <span data-ttu-id="ce394-336">После метода `CheckForRecalc` в классе **Program** (или **Module1** в Visual Basic) из предыдущей процедуры добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-336">After the  `CheckForRecalc` method in the **Program** class (or **Module1** in Visual Basic) from the previous procedure, add the following method.</span></span> 
    
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

2. <span data-ttu-id="ce394-337">После метода `CreateCustomUI` в классе **Program** (или **Module1** в Visual Basic), описанного на предыдущем этапе, добавьте указанный ниже метод.</span><span class="sxs-lookup"><span data-stu-id="ce394-337">After the  `CreateCustomUI` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="ce394-338">Замените весь код в блоке **using** в методе **Main** класса **Program** (блок **Using** метода **Main** в модуле **Module1** в Visual Basic) указанным ниже кодом.</span><span class="sxs-lookup"><span data-stu-id="ce394-338">Replace all the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
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

4. <span data-ttu-id="ce394-339">Выполните отладку решения, нажав клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="ce394-339">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="ce394-340">По завершении работы программы выйдите из нее, нажав любую клавишу.</span><span class="sxs-lookup"><span data-stu-id="ce394-340">When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="ce394-341">Откройте файл Visio Package.vsdx в Visio 2013 и перейдите на вкладку **CUSTOM** (Настраиваемая).</span><span class="sxs-lookup"><span data-stu-id="ce394-341">Open the Visio Package.vsdx file in Visio 2013, and then choose the **CUSTOM** tab.</span></span> 
    
<span data-ttu-id="ce394-342">При открытии файла в Visio 2013 настроенная лента выглядит, как показано на рис. 2.</span><span class="sxs-lookup"><span data-stu-id="ce394-342">The custom ribbon looks like Figure 2 when the file is opened in Visio 2013.</span></span>
  
 <span data-ttu-id="ce394-343">**Рис. 2. Вкладка Custom (Настраиваемая) на ленте Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="ce394-343">**Figure 2. Custom tab in the Visio 2013 ribbon**</span></span>
  
![Настраиваемая вкладка на ленте](media/vis15_CustomRibbonTab.PNG)
  
<span data-ttu-id="ce394-345">XML, созданный методом `CreateCustomUI`, выглядит, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ce394-345">The XML created by the  `CreateCustomUI` method looks like the following.</span></span> 
  
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

## <a name="acknowledgements"></a><span data-ttu-id="ce394-346">Благодарности</span><span class="sxs-lookup"><span data-stu-id="ce394-346">Acknowledgements</span></span>
<span data-ttu-id="ce394-347"><a name="vis15_ManipulateFF_Ackn"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-347"><a name="vis15_ManipulateFF_Ackn"> </a></span></span>

<span data-ttu-id="ce394-348">Мы хотим поблагодарить Visio MVP **Эла Эдланда (Al Edlund)** за его вклад в создание примеров кода, изложенных в данной технической статье.</span><span class="sxs-lookup"><span data-stu-id="ce394-348">We would like to recognize the contribution and input of Visio MVP **Al Edlund** in creating the code examples contained in this technical article.</span></span> <span data-ttu-id="ce394-349">Эл — признанный специалист по управлению форматами файлов Visio, в том числе форматом XML-данных документа Visio (VDX) и новым форматом файлов Visio (VSDX).</span><span class="sxs-lookup"><span data-stu-id="ce394-349">Al is a recognized expert in manipulating the Visio file format, including both the Visio XML Drawing format (.vdx) and the new Visio file format (.vsdx).</span></span> <span data-ttu-id="ce394-350">Эл создал проекты, которые позволяют программным способом изучить форматы файлов Visio и показать их внутреннюю структуру.</span><span class="sxs-lookup"><span data-stu-id="ce394-350">Al has created projects that explore the Visio file formats programmatically and exposes the structures inside.</span></span> 
  
<span data-ttu-id="ce394-351">Дополнительные сведения о том, как Эл работает с форматом файлов Visio, см. по ссылкам в разделе "Дополнительные ресурсы" ниже.</span><span class="sxs-lookup"><span data-stu-id="ce394-351">For more information about Al's work with the Visio file format, see the links in the Additional Resources section that follows.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce394-352">См. также</span><span class="sxs-lookup"><span data-stu-id="ce394-352">See also</span></span>
<span data-ttu-id="ce394-353"><a name="vis15_ManipulateFF_Additional"> </a></span><span class="sxs-lookup"><span data-stu-id="ce394-353"><a name="vis15_ManipulateFF_Additional"> </a></span></span>

- <span data-ttu-id="ce394-354">Автор Эл Эдланд:</span><span class="sxs-lookup"><span data-stu-id="ce394-354">By Al Edlund:</span></span>
    
  - <span data-ttu-id="ce394-355">Проект [pkgVisio — управление XML в Visio 2013](https://pkgvisio.codeplex.com/documentation) на веб-сайте CodePlex.</span><span class="sxs-lookup"><span data-stu-id="ce394-355">[pkgVisio - Visio 2013 XML manipulation](https://pkgvisio.codeplex.com/documentation) project on CodePlex.</span></span> 
    
  - <span data-ttu-id="ce394-356">Видеоролик [pkgVisio_pt1](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) на веб-сайте YouTube.</span><span class="sxs-lookup"><span data-stu-id="ce394-356">[pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) video on YouTube.</span></span> 
    
  - <span data-ttu-id="ce394-357">Видеоролик [pkgVisio_pt2](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) на веб-сайте YouTube.</span><span class="sxs-lookup"><span data-stu-id="ce394-357">[pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) video on YouTube.</span></span> 
    
- [<span data-ttu-id="ce394-358">Центр разработчиков Visio</span><span class="sxs-lookup"><span data-stu-id="ce394-358">Visio Developer Center</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [<span data-ttu-id="ce394-359">Управление документами форматов Office Open XML</span><span class="sxs-lookup"><span data-stu-id="ce394-359">Manipulate Office Open XML Formats Documents</span></span>](https://msdn.microsoft.com/library/aa982683%28v=office.12%29.aspx)
    
- [<span data-ttu-id="ce394-360">Создание документа с пространствами имен (C#) (из LINQ в XML)</span><span class="sxs-lookup"><span data-stu-id="ce394-360">Create a Document with Namespaces (C#) (LINQ to XML)</span></span>](https://msdn.microsoft.com/library/bb387075.aspx)
    
- [<span data-ttu-id="ce394-361">Добавление XML-частей в документ без запуска Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="ce394-361">Add Custom XML Parts to Documents Without Starting Microsoft Office</span></span>](https://msdn.microsoft.com/library/bb608597%28VS.90%29.aspx)
    

