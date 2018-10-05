---
title: Программное управление форматами файлов Visio
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: ''
ms.openlocfilehash: 3da5d0c0c63ba58649435d2e2289b58ab30de2ef
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395821"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a><span data-ttu-id="cb828-102">Программное управление форматами файлов Visio</span><span class="sxs-lookup"><span data-stu-id="cb828-102">Manipulate the Visio file format programmatically</span></span>

![Раздел "Инструкции"](media/mod_icon_howto.png)
  
<span data-ttu-id="cb828-104">Узнайте, как создать решение в Visual Studio 2012 для чтения пакет новых форматов файлов в Visio 2013, выберите части в пакете, изменить данные в части и добавьте новый части пакета.</span><span class="sxs-lookup"><span data-stu-id="cb828-104">Learn how to create a solution in Visual Studio 2012 to read the new file format package in Visio 2013, select parts in the package, change the data in a part, and add new parts to the package.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb828-105">**В этой статье** [Основы обработки формат файла Visio](#vis15_ManipulateFF_Essentials) [Создайте файл vsdx (en) и новое решение Visual Studio](#vis15_ManipulateFF_CreateFile) [Откройте файл Visio 2013 виде пакета](#vis15_ManipulateFF_OpenPackage) [Выберите и чтение части пакета из пакета](#vis15_ManipulateFF_SelectPart) [Выберите и изменения данных XML в часть пакета](#vis15_ManipulateFF_ChangeXML) [Пересчет данных в файле](#vis15_ManipulateFF_Recalculate) [Добавить новую часть пакета для пакета](#vis15_ManipulateFF_AddNewPart) [Благодарности](#vis15_ManipulateFF_Ackn) [Дополнительные материалы](#vis15_ManipulateFF_Additional)                                                                                         </span><span class="sxs-lookup"><span data-stu-id="cb828-105">**In this article**         [Visio file format manipulation essentials](#vis15_ManipulateFF_Essentials)          [Create a .vsdx file and a new Visual Studio solution](#vis15_ManipulateFF_CreateFile)          [Open a Visio 2013 file as a package](#vis15_ManipulateFF_OpenPackage)          [Select and read package parts from a package](#vis15_ManipulateFF_SelectPart)          [Select and change XML data in a package part](#vis15_ManipulateFF_ChangeXML)          [Recalculate data in the file](#vis15_ManipulateFF_Recalculate)          [Add a new package part to a package](#vis15_ManipulateFF_AddNewPart)          [Acknowledgements](#vis15_ManipulateFF_Ackn)          [Additional resources](#vis15_ManipulateFF_Additional)</span></span>||
   
## <a name="visio-file-format-manipulation-essentials"></a><span data-ttu-id="cb828-106">Основы обработки формат файла Visio</span><span class="sxs-lookup"><span data-stu-id="cb828-106">Visio file format manipulation essentials</span></span>
<span data-ttu-id="cb828-107"><a name="vis15_ManipulateFF_Essentials"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-107"></span></span>

<span data-ttu-id="cb828-108">Предыдущие версии Visio сохранения файлов в формате конфиденциальным двоичный файл (.vsd) или формата файла отдельного документа XML документа Visio (.vdx).</span><span class="sxs-lookup"><span data-stu-id="cb828-108">Previous versions of Visio saved files in a proprietary binary file format (.vsd) or a single-document Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="cb828-109">Visio 2013 представлен новый формат файла (vsdx) (en, который основан на основе технологий XML и ZIP-архив.</span><span class="sxs-lookup"><span data-stu-id="cb828-109">Visio 2013 introduces a new file format (.vsdx), which is based on XML and ZIP archive technologies.</span></span> <span data-ttu-id="cb828-110">Как и в предыдущих версиях Visio файлы сохраняются в одном контейнере.</span><span class="sxs-lookup"><span data-stu-id="cb828-110">Just as in previous versions of Visio, files are saved in a single container.</span></span> <span data-ttu-id="cb828-111">В отличие от прежних версий файлов тем не менее, новый формат файла может быть открыт, чтение, обновлены, изменены и создании без Автоматизация приложения Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-111">Unlike legacy files, however, the new file format can be opened, read, updated, changed, and constructed without automating the Visio 2013 application.</span></span> <span data-ttu-id="cb828-112">Разработчики, знакомые с работа с XML или работа с использованием пространства имен [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) можно быстро начать работу с новый формат файла программными средствами.</span><span class="sxs-lookup"><span data-stu-id="cb828-112">Developers who are familiar with manipulating XML or working with the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace can quickly get started working with the new file format programmatically.</span></span> <span data-ttu-id="cb828-113">Разработчики, работавших с помощью формата XML документа Visio в предыдущих версиях можно найти, что многие из структур из этого формата были сохранены в новый формат файла.</span><span class="sxs-lookup"><span data-stu-id="cb828-113">Developers who have worked with the Visio XML Drawing format from previous versions can find that many of the structures from that format have been retained in the new file format.</span></span> 
  
<span data-ttu-id="cb828-114">В этой статье мы рассмотрим работа с формат файлов Visio 2013 программным способом, с помощью Microsoft .NET Framework 4.5, C# или Visual Basic и Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="cb828-114">In this article, we examine how to work with the Visio 2013 file format programmatically, using the Microsoft .NET Framework 4.5, C# or Visual Basic, and Visual Studio 2012.</span></span> <span data-ttu-id="cb828-115">Можно узнать, как открыть файла Visio 2013, выберите части документа в файле, изменить данные в частях и создания новой части документа.</span><span class="sxs-lookup"><span data-stu-id="cb828-115">You can see how to open a Visio 2013 file, select document parts within the file, change data in parts, and create a new document part.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cb828-116">Примеры кода в этой статье предполагается, что вы элементарные общее представление о классов в пространствах имен [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) и [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cb828-116">The code samples in this article assume that you have a rudimentary understanding of the classes in the [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) and [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespaces.</span></span> <span data-ttu-id="cb828-117">> В этой статье также предполагается, что вы понимаете принципы и терминологию Open Packaging Conventions.</span><span class="sxs-lookup"><span data-stu-id="cb828-117">> This article also assumes that you understand the concepts and terminology of the Open Packaging Conventions.</span></span> <span data-ttu-id="cb828-118">Вы должны знакомы с понятиями, пакеты, части документа или части пакета и связей.</span><span class="sxs-lookup"><span data-stu-id="cb828-118">You should have some familiarity with the concepts of packages, document parts or package parts, and relationships.</span></span> <span data-ttu-id="cb828-119">Дополнительные сведения можно [OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="cb828-119">For more information, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="cb828-120">> Кода демонстрируется создание запросов LINQ (синтаксиса запроса), чтобы выбрать XML.</span><span class="sxs-lookup"><span data-stu-id="cb828-120">> The code demonstrates how to create LINQ (Language-Integrated Query) queries to select XML.</span></span> <span data-ttu-id="cb828-121">Большая часть образцов кода используйте синтаксис запроса для построения запросов LINQ.</span><span class="sxs-lookup"><span data-stu-id="cb828-121">Most of the code samples use the query syntax for building LINQ queries.</span></span> <span data-ttu-id="cb828-122">Можно переопределить запросов LINQ, заданный в коде с помощью метода синтаксис LINQ, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="cb828-122">You can rewrite any of the LINQ queries provided in the code by using the LINQ method syntax, if necessary.</span></span> <span data-ttu-id="cb828-123">Дополнительные сведения о синтаксиса запросов LINQ и синтаксис метода можно [LINQ синтаксис запроса или синтаксис метода (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> в таблице 1 приведены основные темы, которые вы должны быть знакомы с перед началом работы над в этой статье.</span><span class="sxs-lookup"><span data-stu-id="cb828-123">For more information about LINQ query syntax and method syntax, see [LINQ Query Syntax versus Method Syntax (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> Table 1 shows the essential topics that you should be familiar with before you work through this article.</span></span> 
  
<span data-ttu-id="cb828-124">**В таблице 1. Основные понятия, которые для работы в формат файлов Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="cb828-124">**Table 1. Core concepts for manipulating the Visio 2013 file format**</span></span>

|<span data-ttu-id="cb828-125">**Название статьи**</span><span class="sxs-lookup"><span data-stu-id="cb828-125">**Article title**</span></span>|<span data-ttu-id="cb828-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cb828-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb828-127">Общие сведения о формате файлов Visio (VSDX)</span><span class="sxs-lookup"><span data-stu-id="cb828-127">Introduction to the Visio file format (.vsdx)</span></span>](introduction-to-the-visio-file-formatvsdx.md) <br/> |<span data-ttu-id="cb828-128">Общий обзор описываются некоторые основные функции в формат файлов Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-128">This high-level overview describes some of the major features of the Visio 2013 file format.</span></span> <span data-ttu-id="cb828-129">Его описание Open Packaging Conventions (OPC) в качестве их применения в формат файлов Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-129">It discusses the Open Packaging Conventions (OPC) as they have been applied to the Visio 2013 file format.</span></span> <span data-ttu-id="cb828-130">Также описываются различия между предыдущей формат файла XML документа Visio (.vdx) и формат файлов Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-130">It also lists some differences between the Visio 2013 file format and the previous Visio XML Drawing file format (.vdx).</span></span>  <br/> |
|[<span data-ttu-id="cb828-131">OPC: Новый стандарт упаковки данных</span><span class="sxs-lookup"><span data-stu-id="cb828-131">OPC: A New Standard for Packaging Your Data</span></span>](https://msdn.microsoft.com/magazine/cc163372.aspx) <br/> |<span data-ttu-id="cb828-132">Журнал MSDN Magazine описаны Open Packaging Conventions качестве концепции.</span><span class="sxs-lookup"><span data-stu-id="cb828-132">This MSDN Magazine article describes the Open Packaging Conventions as a concept.</span></span>  <br/> |
|[<span data-ttu-id="cb828-133">Основные моменты спецификаций Open Packaging Conventions</span><span class="sxs-lookup"><span data-stu-id="cb828-133">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx) <br/> [<span data-ttu-id="cb828-134">Введение в форматы файлов Office (2007) Open XML</span><span class="sxs-lookup"><span data-stu-id="cb828-134">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx) <br/> |<span data-ttu-id="cb828-135">В этих двух статьях рассматривается применение Open Packaging Conventions для файлов Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="cb828-135">These two articles discuss how the Open Packaging Conventions have been applied to Microsoft Office files.</span></span> <span data-ttu-id="cb828-136">Они содержат описания как связей в пакете и также включите несколько примеров кода.</span><span class="sxs-lookup"><span data-stu-id="cb828-136">They contain descriptions of how relationships work in a package and also include some code examples.</span></span>  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a><span data-ttu-id="cb828-137">Создайте файл vsdx (en) и новое решение Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cb828-137">Create a .vsdx file and a new Visual Studio solution</span></span>
<span data-ttu-id="cb828-138"><a name="vis15_ManipulateFF_CreateFile"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-138"></span></span>

<span data-ttu-id="cb828-139">Перед началом работы через процедур, описанных в этой статье, вам необходимо создать файл Visio 2013, чтобы открыть и работы с ними.</span><span class="sxs-lookup"><span data-stu-id="cb828-139">Before you can begin working through the procedures in this article, you need to create a Visio 2013 file to open and manipulate.</span></span> <span data-ttu-id="cb828-140">Документ, используемые в примерах кода в этой статье содержит одну страницу с двумя подключенными фигурами на нем, одну из фигур, выполняется на основе шаблона «Простая блок-схема» фигуры «Начала или окончания».</span><span class="sxs-lookup"><span data-stu-id="cb828-140">The drawing used in the code examples in this article contains a single page with two connected shapes on it, one of the shapes being a "Start/End" shape from the "Basic Flowchart" template.</span></span>
  
<span data-ttu-id="cb828-141">Используйте следующую процедуру для создания нового файла Visio 2013 для использования в оставшихся процедур, описанных в этой статье.</span><span class="sxs-lookup"><span data-stu-id="cb828-141">Use the following procedure to create a new Visio 2013 file to use in the remaining procedures in this article.</span></span>
  
### <a name="to-create-new-file-in-visio-2013"></a><span data-ttu-id="cb828-142">Создание нового файла в Visio 2013</span><span class="sxs-lookup"><span data-stu-id="cb828-142">To create new file in Visio 2013</span></span>

1. <span data-ttu-id="cb828-143">Откройте Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-143">Open Visio 2013.</span></span>
    
2. <span data-ttu-id="cb828-144">Создайте новый документ, основанный на шаблоне Простая блок-схема, выбрав **КАТЕГОРИЙ**, **блок-схема**, **Простая блок-схема**, **Создание**.</span><span class="sxs-lookup"><span data-stu-id="cb828-144">Create a new document based on the Basic Flowchart template by choosing **CATEGORIES**, **Flowchart**, **Basic Flowchart**, **Create**.</span></span>
    
3. <span data-ttu-id="cb828-145">В окне **фигуры** Перетащите фигуру **Начала или окончания** на полотно.</span><span class="sxs-lookup"><span data-stu-id="cb828-145">From the **Shapes** window, drag a **Start/End** shape onto the canvas.</span></span> 
    
4. <span data-ttu-id="cb828-146">Выберите новый Начальная или завершающая фигура на полотне и введите «Приступить к процессу».</span><span class="sxs-lookup"><span data-stu-id="cb828-146">Select the new Start/End shape on the drawing canvas and type 'Begin Process'.</span></span>
    
5. <span data-ttu-id="cb828-147">В окне **фигуры** Перетащите фигуру **процесса** на полотно.</span><span class="sxs-lookup"><span data-stu-id="cb828-147">From the **Shapes** window, drag a **Process** shape onto the canvas.</span></span> 
    
6. <span data-ttu-id="cb828-148">Выберите новый процесс фигуры на полотне и введите «Выполнения некоторых задач».</span><span class="sxs-lookup"><span data-stu-id="cb828-148">Select the new Process shape on the drawing canvas and type 'Perform some task'.</span></span>
    
7. <span data-ttu-id="cb828-149">В контекстном меню Начальная или завершающая фигура выберите **Добавить один соединитель на страницу**и затем рисовать соединитель между начала или окончания и процесс фигуры на полотно, как показано на рисунке 1.</span><span class="sxs-lookup"><span data-stu-id="cb828-149">On the shortcut menu for the Start/End shape, select **Add One Connector to the Page**, and then draw a connector between the Start/End and Process shapes on the canvas, as shown in Figure 1.</span></span>
    
    <span data-ttu-id="cb828-150">**На рисунке 1. Простой документ Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="cb828-150">**Figure 1. Simple Visio 2013 drawing**</span></span>
    
     ![Начальная или завершающая фигура, подключенная к фигуре процесса](media/vis15_SimpleFlowchart.png)
  
8. <span data-ttu-id="cb828-152">Сохраните файл на рабочем столе как файл vsdx (en), выбрав **файл**, **Сохранить как**, **компьютер**, **рабочий стол**.</span><span class="sxs-lookup"><span data-stu-id="cb828-152">Save the file to your Desktop as a .vsdx file by choosing **File**, **Save As**, **Computer**, **Desktop**.</span></span>
    
    <span data-ttu-id="cb828-153">В диалоговом окне **Сохранить как** введите пакет Visio в поле **имя файла** »», выберите **документ Visio (\*vsdx (en))** в **Тип** списка, а затем нажмите кнопку **Сохранить** .</span><span class="sxs-lookup"><span data-stu-id="cb828-153">In the **Save As** dialog box, enter Visio Package in the **File name** box"", select **Visio Drawing (\*.vsdx)** in the **Save as type** list, and then choose the **Save** button.</span></span> 
    
9. <span data-ttu-id="cb828-154">Закройте файл и закройте Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-154">Close the file and then close Visio 2013.</span></span>
    
> [!TIP]
> <span data-ttu-id="cb828-155">В некоторых случаях Visio открывает файл успешно даже в том случае, если существуют проблемы с файлом.</span><span class="sxs-lookup"><span data-stu-id="cb828-155">Sometimes Visio opens a file successfully even if there are issues with the file.</span></span> <span data-ttu-id="cb828-156">При тестировании решения, работа с элементами управления файлов Visio на уровне файла пакета, чтобы гарантировать, что Visio уведомлением неполадок файла, следует включить предупреждения об открытии файлов.</span><span class="sxs-lookup"><span data-stu-id="cb828-156">To ensure that Visio notifies you of any file issues, you should enable file open warnings when testing solutions that manipulate Visio files at the file package level.</span></span> <span data-ttu-id="cb828-157">> Для включения предупреждения об открытии файлов, в Visio 2013, выберите **файл**, **Параметры**, **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="cb828-157">> To enable file open warnings, in Visio 2013, choose **File**, **Options**, **Advanced**.</span></span> <span data-ttu-id="cb828-158">В разделе **Сохранить и открыть**установите флажок **Показывать предупреждения об открытии файлов**.</span><span class="sxs-lookup"><span data-stu-id="cb828-158">Under **Save/Open**, select **Show file open warnings**.</span></span> 
  
<span data-ttu-id="cb828-159">Эти процедуры используют консольного приложения Windows для работы с файла «Visio Package.vsdx».</span><span class="sxs-lookup"><span data-stu-id="cb828-159">These procedures use a Windows console application to manipulate the "Visio Package.vsdx" file.</span></span> <span data-ttu-id="cb828-160">Используйте следующую процедуру, чтобы создать и настроить новое консольное приложение Windows в Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="cb828-160">Use the following procedure to create and set up a new Windows console application in Visual Studio 2012.</span></span>
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a><span data-ttu-id="cb828-161">Чтобы создать новое решение в Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="cb828-161">To create a new solution in Visual Studio 2012</span></span>

1. <span data-ttu-id="cb828-162">В меню **Файл** выберите пункт **Создать**, затем **Проект**.</span><span class="sxs-lookup"><span data-stu-id="cb828-162">On the **File** menu, choose **New**, **Project**.</span></span>
    
2. <span data-ttu-id="cb828-163">В диалоговом окне **Новый проект** разверните узел **Visual C#** или **Visual Basic**и затем выберите **Windows**, **Консольного приложения**.</span><span class="sxs-lookup"><span data-stu-id="cb828-163">In the **New Project** dialog box, expand either **Visual C#** or **Visual Basic**, and then choose **Windows**, **Console Application**.</span></span>
    
    <span data-ttu-id="cb828-164">В поле **имя** введите «VisioFileAccessor», выберите расположение проекта и нажмите кнопку « **ОК** ».</span><span class="sxs-lookup"><span data-stu-id="cb828-164">In the **Name** box, enter ' VisioFileAccessor', select a location for the project, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="cb828-165">В меню **проект** выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="cb828-165">On the **Project** menu, choose **Add Reference**.</span></span> 
    
    <span data-ttu-id="cb828-166">В диалоговом окне **Диспетчер ссылок** в разделе **сборки**выберите **Framework**и добавьте ссылку на них **System.Xml** и **WindowsBase** .</span><span class="sxs-lookup"><span data-stu-id="cb828-166">In the **Reference Manager** dialog box, under **Assemblies**, choose **Framework**, and then add a reference to the **System.Xml** and **WindowsBase** components.</span></span> 
    
4. <span data-ttu-id="cb828-167">В файле Program.cs или Module1.vb проекта добавьте следующие директивы **using** (инструкции**Imports** в Visual Basic):</span><span class="sxs-lookup"><span data-stu-id="cb828-167">In the Program.cs or Module1.vb file for the project, add the following **using** directives (**Imports** statements in Visual Basic):</span></span> 
    
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

5. <span data-ttu-id="cb828-168">Также в файле Program.cs или Module1.vb до конца **методе класса **Program** (**модуль1\*\* в Visual Basic),\*\* добавьте следующий код, который останавливает выполнение консольного приложения до пользователь нажимает клавишу.</span><span class="sxs-lookup"><span data-stu-id="cb828-168">Also in the Program.cs or Module1.vb file, before the end of the **Main** method of the **Program** class (**Module1** in Visual Basic), add the following code that stops execution of the console application until the user presses a key.</span></span> 
    
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

## <a name="open-a-visio-2013-file-as-a-package"></a><span data-ttu-id="cb828-169">Откройте файл Visio 2013 виде пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-169">Open a Visio 2013 file as a package</span></span>
<span data-ttu-id="cb828-170"><a name="vis15_ManipulateFF_OpenPackage"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-170"></span></span>

<span data-ttu-id="cb828-171">Перед могут управлять любыми данных в файле, необходимо сначала открыть файл в объекте [пакета](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) , который содержится в пространстве имен [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cb828-171">Before you can manipulate any of the data within the file, you need to first open the file within a [Package](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) object, which is contained within the [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) namespace.</span></span> <span data-ttu-id="cb828-172">Объект **пакета** представляет собой файл Visio в целом.</span><span class="sxs-lookup"><span data-stu-id="cb828-172">The **Package** object represents the Visio file as a whole.</span></span> <span data-ttu-id="cb828-173">Она предоставляет члены, которые позволяют выбирать отдельным компонентам в пакете.</span><span class="sxs-lookup"><span data-stu-id="cb828-173">It exposes members that allow you to select individual document parts within the file package.</span></span> <span data-ttu-id="cb828-174">В частности класс **пакет** предоставляет статический метод [Open (String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) , которая используется для открытия файла в виде пакета.</span><span class="sxs-lookup"><span data-stu-id="cb828-174">In particular, the **Package** class exposes the static [Open(String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) method that you use to open a file as a package.</span></span> <span data-ttu-id="cb828-175">Он также предоставляет метод [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) для закрытия пакета после завершения работы с ним.</span><span class="sxs-lookup"><span data-stu-id="cb828-175">It also exposes a [Close()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) method for closing the package once you've finished with it.</span></span> 
  
> [!TIP]
> <span data-ttu-id="cb828-176">Рекомендуется **с помощью** блок можно используйте для открытия файла Visio в объекте **пакета** , чтобы не требуется явно закрыть пакет файлов после завершения с ним.</span><span class="sxs-lookup"><span data-stu-id="cb828-176">As a best practice, use a **using** block to open the Visio file in the **Package** object so that you don't have to explicitly close the file package when you're done with it.</span></span> <span data-ttu-id="cb828-177">Можно также в явном виде вызовите метод **Package.Close** в блоке **finally** конструкции **try/catch/finally** .</span><span class="sxs-lookup"><span data-stu-id="cb828-177">You can also explicitly call the **Package.Close** method in the **finally** block of a **try/catch/finally** construction.</span></span> 
  
<span data-ttu-id="cb828-178">Используйте следующий код, чтобы получить полный путь для файла «Visio Package.vsdx» с помощью объекта [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) , передайте путь как аргумент методу **Package.Open** и затем возвращает объект **пакета** вызывающий код.</span><span class="sxs-lookup"><span data-stu-id="cb828-178">Use the following code to get the full path for the "Visio Package.vsdx" file by using a [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) object, pass the path as an argument to the **Package.Open** method, and then return a **Package** object to the calling code.</span></span> 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a><span data-ttu-id="cb828-179">Чтобы открыть файл vsdx (en) в виде пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-179">To open a .vsdx file as a package</span></span>

1. <span data-ttu-id="cb828-180">После метода **Main** в классе **программа** (или **модуль1** в Visual Basic) добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="cb828-180">After the **Main** method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

2. <span data-ttu-id="cb828-181">В **методе класса **программа** (или **модуль1** в Visual Basic)** добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="cb828-181">In the **Main** method of the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

## <a name="select-and-read-package-parts-from-a-package"></a><span data-ttu-id="cb828-182">Выберите и чтение части пакета из пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-182">Select and read package parts from a package</span></span>
<span data-ttu-id="cb828-183"><a name="vis15_ManipulateFF_SelectPart"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-183"></span></span>

<span data-ttu-id="cb828-184">После получения файла Visio 2013 откройте как пакет можно получить доступ к части документа в ней с помощью класса [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) , включенные в пространстве имен **System.IO.Packaging** .</span><span class="sxs-lookup"><span data-stu-id="cb828-184">Once you have the Visio 2013 file open as a package, you can access the document parts within it using the [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) class included in the **System.IO.Packaging** namespace.</span></span> <span data-ttu-id="cb828-185">Объекты **PackagePart** могут быть созданы по отдельности или в виде коллекции.</span><span class="sxs-lookup"><span data-stu-id="cb828-185">**PackagePart** objects can be instantiated individually or as a collection.</span></span> <span data-ttu-id="cb828-186">Класс **пакета** предоставляет метод [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) и метод [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) для получения объектов **PackagePart** из **пакета**.</span><span class="sxs-lookup"><span data-stu-id="cb828-186">The **Package** class exposes a [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) method and a [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) method for getting **PackagePart** objects out of the **Package**.</span></span> <span data-ttu-id="cb828-187">Метод **Package.GetParts** возвращает экземпляр класса [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) , который вы может взаимодействовать с как семейства сайтов, который реализует [IEnumerator\<T\> ](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cb828-187">The **Package.GetParts** method returns an instance of the [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) class, which you can then interact with like any other collection that implements the [IEnumerator\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2) interface.</span></span> 
  
<span data-ttu-id="cb828-188">Использовать код в следующей процедуре для получения объекта **PackagePartCollection** из **пакета** как семейство, выполните итерацию по **PackagePart** объектов в коллекции и записи URI и типа контента для каждого \*\*PackagePart \*\*на консоль.</span><span class="sxs-lookup"><span data-stu-id="cb828-188">Use the code in the following procedure to get a **PackagePartCollection** object from the **Package** as a collection, iterate through the **PackagePart** objects in the collection, and write the URI and content type of each **PackagePart** to the console.</span></span> 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a><span data-ttu-id="cb828-189">Выполнять итерацию по части пакета в пакете</span><span class="sxs-lookup"><span data-stu-id="cb828-189">To iterate through the package parts in a package</span></span>

1. <span data-ttu-id="cb828-190">После `OpenPackage` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="cb828-190">After the  `OpenPackage` method in the **Program** class (or **Module1** in Visual Basic), add the following code.</span></span> 
    
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

2. <span data-ttu-id="cb828-191">Добавьте следующий код внутри блока **using** в **методе класса **программы** (блок **с помощью** метода **Main** в **модуль1** в Visual Basic)** :</span><span class="sxs-lookup"><span data-stu-id="cb828-191">Add the following code inside the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic):</span></span> 
    
  ```cs
  // Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage);
  
  ```

  ```vb
  ' Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage)
  
  ```

3. <span data-ttu-id="cb828-192">Нажмите клавишу F5 для отладки решения.</span><span class="sxs-lookup"><span data-stu-id="cb828-192">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="cb828-193">После завершения работы программы нажмите любую клавишу, чтобы выйти из.</span><span class="sxs-lookup"><span data-stu-id="cb828-193">When the program has completed running, choose any key to exit.</span></span>
    
<span data-ttu-id="cb828-194">Консольное приложение создает выходные данные (некоторые из выходных данных включен для краткости) следующего вида:</span><span class="sxs-lookup"><span data-stu-id="cb828-194">The console application produces output similar to the following (some of the output has been omitted for brevity):</span></span>
  
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
  
<span data-ttu-id="cb828-195">Чаще необходимо выбрать один **PackagePart** без необходимости для итерации по всем из них.</span><span class="sxs-lookup"><span data-stu-id="cb828-195">More often than not, you need to select one **PackagePart** without having to iterate over all of them.</span></span> <span data-ttu-id="cb828-196">Объект **PackagePart** можно получить из **пакета** с помощью ее отношения с **пакета** или другой **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="cb828-196">You can get a **PackagePart** object from a **Package** by using its relationship to the **Package** or another **PackagePart**.</span></span> <span data-ttu-id="cb828-197">Связь в Visio 2013, файл имеет формат дискретные сущности, описывающий, как часть документа относится к пакет файлов или как две части документа относятся друг с другом.</span><span class="sxs-lookup"><span data-stu-id="cb828-197">A relationship in the Visio 2013 file format is a discrete entity that describes how a document part relates to the file package or how two document parts relate to each other.</span></span> <span data-ttu-id="cb828-198">К примеру сам пакет файла Visio 2013 имеет связь с его части документа Visio и части документа Visio имеет связь с частью Windows.</span><span class="sxs-lookup"><span data-stu-id="cb828-198">For example, the Visio 2013 file package itself has a relationship to its Visio Document part, and the Visio Document part has a relationship to the Windows part.</span></span> <span data-ttu-id="cb828-199">Эти связи, представленные в виде экземпляров классов [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) или [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cb828-199">These relationships are represented as instances of the [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) or [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) classes.</span></span> 
  
<span data-ttu-id="cb828-200">Класс **пакета** предоставляет несколько методов для получения отношений, которые он содержит как **PackageRelationship** или **PackageRelationshipCollection** объектов.</span><span class="sxs-lookup"><span data-stu-id="cb828-200">The **Package** class exposes several methods for getting the relationships that it contains as **PackageRelationship** or **PackageRelationshipCollection** objects.</span></span> <span data-ttu-id="cb828-201">Метод [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) можно использовать для создания объекта **PackageRelationshipCollection** , которая содержит объекты **PackageRelationship** одного определенного типа.</span><span class="sxs-lookup"><span data-stu-id="cb828-201">You can use the [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) method to instantiate a **PackageRelationshipCollection** object that contains **PackageRelationship** objects of a single specific type.</span></span> <span data-ttu-id="cb828-202">Конечно с помощью метода **Package.GetRelationshipsByType** необходимо знать уже тип отношения, который требуется.</span><span class="sxs-lookup"><span data-stu-id="cb828-202">Of course, using the **Package.GetRelationshipsByType** method requires that you already know the relationship type that you need.</span></span> <span data-ttu-id="cb828-203">Отношения типов являются строками в формате пространство имен XML.</span><span class="sxs-lookup"><span data-stu-id="cb828-203">Relationship types are strings in XML namespace format.</span></span> <span data-ttu-id="cb828-204">Например, тип связи из части документа Visio будет https://schemas.microsoft.com/visio/2010/relationships/document.</span><span class="sxs-lookup"><span data-stu-id="cb828-204">For example, the relationship type of the Visio Document part is https://schemas.microsoft.com/visio/2010/relationships/document.</span></span> 
  
<span data-ttu-id="cb828-205">После определения отношения **PackagePart** в **пакете** или в другой **PackagePart** (то есть, у вас есть объект **PackageRelationship** , который ссылается на **PackagePart** , который будет), можно использовать его связь для получения идентификатора URI, **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="cb828-205">Once you know the relationship of a **PackagePart** to the **Package** or to another **PackagePart** (that is, you have a **PackageRelationship** object that references the **PackagePart** that you want), you can use that relationship to get the URI of that **PackagePart**.</span></span> <span data-ttu-id="cb828-206">Затем передайте URI в метод **Package.GetPart** для возврата **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="cb828-206">You then pass the URI to the **Package.GetPart** method to return the **PackagePart**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cb828-207">Также можно получить ссылку на определенных **PackagePart** с помощью метода **Package.GetPart** и URI **PackagePart**обхода на этапе, где получить пакет части связи.</span><span class="sxs-lookup"><span data-stu-id="cb828-207">You can also get a reference to a specific **PackagePart** by using just the **Package.GetPart** method and the URI of the **PackagePart**, bypassing the step where you get the package part's relationships.</span></span> <span data-ttu-id="cb828-208">Тем не менее некоторые части пакета в пакете файла Visio можно сохранить для расположений, отличных от их расположения по умолчанию в пакете.</span><span class="sxs-lookup"><span data-stu-id="cb828-208">However, some package parts in the Visio file package can be saved to locations other than their default locations in a package.</span></span> <span data-ttu-id="cb828-209">Не удается предполагается, что часть пакета всегда расположена в каталоге же URI для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="cb828-209">You cannot assume that a package part is always located at the same URI for every file.</span></span> <span data-ttu-id="cb828-210">> Вместо этого рекомендуется использовать для доступа к отдельным объектам **PackagePart** отношения.</span><span class="sxs-lookup"><span data-stu-id="cb828-210">> Instead, it is a best practice to use relationships to access individual **PackagePart** objects.</span></span> 
  
<span data-ttu-id="cb828-211">Используйте следующую процедуру для получения **PackagePart** (часть документа Visio) с помощью **PackageRelationship** из **пакета** , который ссылается на части.</span><span class="sxs-lookup"><span data-stu-id="cb828-211">Use the following procedure to get a **PackagePart** (the Visio Document part) by using the **PackageRelationship** from the **Package** that references the part.</span></span> 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a><span data-ttu-id="cb828-212">Для выбора часть пакета в пакете с помощью отношения</span><span class="sxs-lookup"><span data-stu-id="cb828-212">To select a specific package part in the package by relationship</span></span>

1. <span data-ttu-id="cb828-213">После `IteratePackageParts` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-213">After the  `IteratePackageParts` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
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

2. <span data-ttu-id="cb828-214">Замените код в блоке **с помощью** метода **Main** класса **Program** (блок **с помощью** метода **Main** в **модуль1** в Visual Basic) следующий код.</span><span class="sxs-lookup"><span data-stu-id="cb828-214">Replace the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
  ```cs
  // Get a reference to the Visio Document part contained in the file package.
  PackagePart documentPart = GetPackagePart(visioPackage, 
      "https://schemas.microsoft.com/visio/2010/relationships/document");
  
  ```

  ```vb
  ' Get a reference to the Visio Document part contained in the file package.
  Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
      "https://schemas.microsoft.com/visio/2010/relationships/document")
  
  ```

<span data-ttu-id="cb828-215">Как уже было сказано ранее, можно также получить **PackagePart** объектов с помощью отношения с другими объектами **PackagePart** .</span><span class="sxs-lookup"><span data-stu-id="cb828-215">As mentioned previously, you can also get **PackagePart** objects by using their relationship to other **PackagePart** objects.</span></span> <span data-ttu-id="cb828-216">Это важно, поскольку для документа Visio любой сложности большинство объектов **PackagePart** нет отношения в **пакет**.</span><span class="sxs-lookup"><span data-stu-id="cb828-216">This is important because, for a Visio document of any complexity, most of the **PackagePart** objects don't have a relationship to the **Package**.</span></span> <span data-ttu-id="cb828-217">К примеру отдельных часть содержимого страницы в пакет файлов (то есть, /visio/pages/page1.xml) имеет отношение части индекса страницы (то есть, /visio/pages/pages.xml), но не сам пакет файла.</span><span class="sxs-lookup"><span data-stu-id="cb828-217">For example, an individual Page Content part in the file package (that is, /visio/pages/page1.xml) has a relationship to the Page Index part (that is, /visio/pages/pages.xml) but not to the file package itself.</span></span> <span data-ttu-id="cb828-218">Если у вас нет точное URI отдельной страницы в пакете, можно использовать ее отношения с часть страницы индекса для получения ссылки на него.</span><span class="sxs-lookup"><span data-stu-id="cb828-218">If you don't have the exact URI of the individual page in the package, you can use its relationship to the Page Index part to get a reference to it.</span></span>
  
<span data-ttu-id="cb828-219">Класс **PackagePart** предоставляет метод [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) , которые можно использовать для возврата объекта **PackageRelationshipCollection** , который содержит только один тип объекта **PackageRelationship** .</span><span class="sxs-lookup"><span data-stu-id="cb828-219">The **PackagePart** class exposes a [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) method that you can use to return a **PackageRelationshipCollection** object that contains only one type of **PackageRelationship** object.</span></span> <span data-ttu-id="cb828-220">При наличии **PackageRelationshipCollection**, вы можете выбрать **PackageRelationship** из коллекции и затем ссылаются на объект **PackagePart** .</span><span class="sxs-lookup"><span data-stu-id="cb828-220">Once you have the **PackageRelationshipCollection**, you can select the **PackageRelationship** that you need from the collection and then reference the **PackagePart** object.</span></span> 
  
<span data-ttu-id="cb828-221">Используйте следующий код для получения **PackagePart** из **пакета** с помощью ее отношения к (получение объекта **PackageRelationship** из) другой **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="cb828-221">Use the following code to get a **PackagePart** from the **Package** by using its relationship to (getting a **PackageRelationship** object from) another **PackagePart**.</span></span>
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a><span data-ttu-id="cb828-222">Чтобы выбрать часть пакета через ее отношения с другой части пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-222">To select a specific package part through its relationship to another package part</span></span>

1. <span data-ttu-id="cb828-223">После `GetPackagePart` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий метод перегрузка.</span><span class="sxs-lookup"><span data-stu-id="cb828-223">After the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following overload method.</span></span> 
    
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

2. <span data-ttu-id="cb828-224">Добавьте следующий код в **с помощью** блок в методе **Main** **программы** класса (блок **Using** метода **Main** в **модуль1** в Visual Basic), под кодом на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="cb828-224">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> <span data-ttu-id="cb828-225">(Не удаляйте код, добавленный в предыдущей процедуре).</span><span class="sxs-lookup"><span data-stu-id="cb828-225">(Do not delete the code that you added in the previous procedure.)</span></span> 
    
  ```cs
  // Get a reference to the collection of pages in the document, 
  // and then to the first page in the document.
  PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
      "https://schemas.microsoft.com/visio/2010/relationships/pages");
  PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
      "https://schemas.microsoft.com/visio/2010/relationships/page");
  
  ```

  ```vb
  ' Get a reference to the collection of pages in the document,
  ' and then to the first page in the document.
  Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
      "https://schemas.microsoft.com/visio/2010/relationships/pages") 
  Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
      "https://schemas.microsoft.com/visio/2010/relationships/page") 
  ```

<span data-ttu-id="cb828-226">Прежде чем принять изменения в файл XML, включенные в части документа, необходимо сначала загрузить документ XML в объект, который позволяет читать XML-код, с помощью класса [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) или [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cb828-226">Before you can make changes to the XML included in a document part, you need to first load the XML document into an object that allows you to read the XML, using the [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) class or [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) class.</span></span> <span data-ttu-id="cb828-227">Оба класса предоставляют методы для задач, таких как выбор элементов XML, содержащиеся в XML-документов; Создание, чтение и запись атрибутов; и вставка новые элементы XML в документ.</span><span class="sxs-lookup"><span data-stu-id="cb828-227">Both classes expose methods for tasks such as selecting XML elements contained within the XML documents; creating, reading, and writing attributes; and inserting new XML elements into a document.</span></span> 
  
<span data-ttu-id="cb828-228">Двух класс **XDocument** позволяет запроса XML, с помощью LINQ.</span><span class="sxs-lookup"><span data-stu-id="cb828-228">Of the two, the **XDocument** class allows you to query the XML using LINQ.</span></span> <span data-ttu-id="cb828-229">С помощью LINQ можно легко выбрать отдельные элементы из XML-документа путем создания запросов, а не итерации всех элементов в коллекции и тестирование для элементов, которые необходимо.</span><span class="sxs-lookup"><span data-stu-id="cb828-229">With LINQ, you can easily select individual elements from an XML document by creating queries, rather than iterating over all of the elements in a collection and testing for the elements that you need.</span></span> <span data-ttu-id="cb828-230">По этим причинам следующих процедур, описанных в этой статье используйте класс **XDocument** и другие классы пространства имен **System.Xml.Linq** для работы с XML.</span><span class="sxs-lookup"><span data-stu-id="cb828-230">For these reasons, the following procedures in this article use the **XDocument** class and other classes of the **System.Xml.Linq** namespace for working with XML.</span></span> 
  
<span data-ttu-id="cb828-231">Используйте следующую процедуру, чтобы открыть **PackagePart** документ в формате XML в объект **XDocument** .</span><span class="sxs-lookup"><span data-stu-id="cb828-231">Use the following procedure to open a **PackagePart** as an XML document in an **XDocument** object.</span></span> 
  
### <a name="to-read-the-xml-in-a-package-part"></a><span data-ttu-id="cb828-232">Чтение XML-кода в часть пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-232">To read the XML in a package part</span></span>

1. <span data-ttu-id="cb828-233">После последнего перегрузка для `GetPackagePart` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-233">After the last overload for the  `GetPackagePart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
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

2. <span data-ttu-id="cb828-234">Добавьте следующий код в **с помощью** блок в методе **Main** **программы** класса (блок **Using** метода **Main** в **модуль1** в Visual Basic), под кодом на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="cb828-234">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
  ```cs
  // Open the XML from the Page Contents part.
  XDocument pageXML = GetXMLFromPart(pagePart);
  ```

  ```vb
  ' Open the XML from the Page Contents part.
  Dim pageXML As XDocument = GetXMLFromPart(pagePart)
  ```

## <a name="select-and-change-xml-data-in-a-package-part"></a><span data-ttu-id="cb828-235">Выберите и изменения данных XML в часть пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-235">Select and change XML data in a package part</span></span>
<span data-ttu-id="cb828-236"><a name="vis15_ManipulateFF_ChangeXML"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-236"></span></span>

<span data-ttu-id="cb828-237">После загрузки части документа в объект **XDocument** можно использовать LINQ для выбора XML-элементы и внести изменения в XML-документе.</span><span class="sxs-lookup"><span data-stu-id="cb828-237">Once you have loaded a document part into an **XDocument** object, you can use LINQ to select XML elements and make changes to the XML document.</span></span> <span data-ttu-id="cb828-238">Можно изменить XML-данные, добавить или удалить данные и сохранить XML-документа в часть документа.</span><span class="sxs-lookup"><span data-stu-id="cb828-238">You can change XML data, add or remove data, and then save the XML document back to the document part.</span></span> 
  
<span data-ttu-id="cb828-239">Наиболее распространенные задачи для управления формат файла Visio Выбор коллекции элементов или определенные элементы XML в документе.</span><span class="sxs-lookup"><span data-stu-id="cb828-239">The most common task for manipulating the Visio file format is selecting specific XML elements or collections of elements in the document.</span></span> <span data-ttu-id="cb828-240">Пространство имен **System.Xml.Linq** включает в себя класс [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) , который представляет элемент XML.</span><span class="sxs-lookup"><span data-stu-id="cb828-240">The **System.Xml.Linq** namespace includes the [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) class, which represents an XML element.</span></span> <span data-ttu-id="cb828-241">Класс **XElement** обеспечивает доступ к данным, содержащиеся в файле Visio по детальный уровень, из отдельных элементов **фигуры** в элементах **значение** (например).</span><span class="sxs-lookup"><span data-stu-id="cb828-241">The **XElement** class gives you access to the data contained in the Visio file at a granular level, from individual **Shape** elements to **ValidationRule** elements (as examples).</span></span> 
  
<span data-ttu-id="cb828-242">Выберите элементы **фигуры** **XDocument** (содержащем часть содержимого страницы) и затем выберите определенный элемент **фигуры** , используйте приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="cb828-242">Use the following code to select the **Shape** elements from an **XDocument** (containing a Page Contents part) and to then select a specific **Shape** element.</span></span> 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a><span data-ttu-id="cb828-243">Для выбора конкретного элемента в части пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-243">To select a specific element in a package part</span></span>

1. <span data-ttu-id="cb828-244">После `GetXMLFromPart` метод в **программе** класс (или **модуль1** в Visual Basic), добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-244">After the  `GetXMLFromPart` method in the **Program** class (or **Module1** in Visual Basic), add the following method.</span></span> 
    
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

2. <span data-ttu-id="cb828-245">После `GetXElementsByName` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-245">After the  `GetXElementsByName` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="cb828-246">Добавьте следующий код в **с помощью** блок в методе **Main** **программы** класса (блок **Using** метода **Main** в **модуль1** в Visual Basic), под кодом на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="cb828-246">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
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

<span data-ttu-id="cb828-247">После стали ссылку на объект **XElement** , содержащихся в объект **XDocument** , можно управлять как XML-данных и, таким образом, измените данные, содержащиеся в файле Visio.</span><span class="sxs-lookup"><span data-stu-id="cb828-247">Once you have gotten a reference to a **XElement** object contained within an **XDocument** object, you can manipulate it like any other XML data and, thereby, change the data contained in the Visio file.</span></span> <span data-ttu-id="cb828-248">Например если фигуры текст при открытии в Visio, соответствующих элементов **фигуры** будет содержать по крайней мере один элемент **текста** .</span><span class="sxs-lookup"><span data-stu-id="cb828-248">For example, if a shape has text when it is opened in Visio, the corresponding **Shape** element will contain at least one **Text** element.</span></span> <span data-ttu-id="cb828-249">Чтобы изменить значение этого элемента **текст** , текст фигуры изменяется при просмотре файла в Visio.</span><span class="sxs-lookup"><span data-stu-id="cb828-249">If you change the value of that **Text** element, the shape's text is changed when the file is viewed in Visio.</span></span> 
  
<span data-ttu-id="cb828-250">Добавьте следующий код в **с помощью** блок в методе **Main** класса **программы** (блок **с помощью** метода **Main** в **модуль1** в Visual Basic) для изменения текста в Начальная или завершающая фигура из «Начать процесс» Чтобы «Запуск процесса».</span><span class="sxs-lookup"><span data-stu-id="cb828-250">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) to change the text in the Start/End shape from "Begin process" to "Start process".</span></span> 
  
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
> <span data-ttu-id="cb828-251">В предыдущем примере существующий текст фигуры и строку, используемую для замены его имеют такое же число символов.</span><span class="sxs-lookup"><span data-stu-id="cb828-251">In the previous code example, the existing shape text and the string used to replace it have the same number of characters.</span></span> <span data-ttu-id="cb828-252">Также Обратите внимание на то, что запрос LINQ изменяется значение последнего дочернего узла возвращаемый элемент (который в этом случае является текстовым).</span><span class="sxs-lookup"><span data-stu-id="cb828-252">Also note that the LINQ query changes the value of the last child node of the returned element (which, in this case, is a text node).</span></span> <span data-ttu-id="cb828-253">Это позволяет избежать изменения параметров элемент **позиции символа** , который является дочерним элементом **текст** .</span><span class="sxs-lookup"><span data-stu-id="cb828-253">This is done to avoid changing the settings of the **cp** element that is a child of the **Text** element.</span></span> <span data-ttu-id="cb828-254">> Можно привести к нестабильности файл, если изменить текст фигуры программным путем с помощью перезаписи все дочерние элементы элемента **текста** .</span><span class="sxs-lookup"><span data-stu-id="cb828-254">> It is possible to cause file instability if you alter shape text programmatically by overwriting all children of the **Text** element.</span></span> <span data-ttu-id="cb828-255">Как показано в приведенном выше примере форматирование текста представлены элементы **позиции символа** в разделе **текст** элемента в файле.</span><span class="sxs-lookup"><span data-stu-id="cb828-255">As in the example above, the text formatting is represented by **cp** elements under the **Text** element in the file.</span></span> <span data-ttu-id="cb828-256">Определение форматирования хранится в **разделе** родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="cb828-256">The definition of the formatting is stored in the parent **Section** element.</span></span> <span data-ttu-id="cb828-257">Если эти два элемента данных несогласованности, затем файл может работать некорректно.</span><span class="sxs-lookup"><span data-stu-id="cb828-257">If these two pieces of information become inconsistent, then the file may not behave as expected.</span></span> <span data-ttu-id="cb828-258">Visio heals много несоответствия, но она лучше подходит для обеспечения согласованности ее изменения, чтобы вы управляете ultimate поведение файла.</span><span class="sxs-lookup"><span data-stu-id="cb828-258">Visio heals many inconsistencies, but it is better to ensure that any programmatic changes are consistent so that you are controlling the ultimate behavior of the file.</span></span> 
  
<span data-ttu-id="cb828-259">После внесения изменений в XML-код части документа эти изменения существует только в памяти.</span><span class="sxs-lookup"><span data-stu-id="cb828-259">When you make changes to the XML of a document part, those changes exist in memory only.</span></span> <span data-ttu-id="cb828-260">Для сохранения изменений в файле XML-код должен быть сохранен обратно в части документа.</span><span class="sxs-lookup"><span data-stu-id="cb828-260">To persist the changes in the file, you must save the XML back to the document part.</span></span>
  
<span data-ttu-id="cb828-261">Следующий код использует класс [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) и класс [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) для обратной записи XML для части пакета.</span><span class="sxs-lookup"><span data-stu-id="cb828-261">The following code uses the [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) class and [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) class to write the XML back to the package part.</span></span> <span data-ttu-id="cb828-262">Несмотря на то, что можно использовать метод [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) для сохранения XML в часть **XmlWriter** и **XmlWriterSettings** классы позволяют позволяет контролировать выходные данные, включая указание типа кодировки.</span><span class="sxs-lookup"><span data-stu-id="cb828-262">Although you can use the [Save()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) method to save the XML back to the part, the **XmlWriter** and **XmlWriterSettings** classes allow you finer control over the output, including specifying the type of encoding.</span></span> <span data-ttu-id="cb828-263">Класс **XDocument** предоставляет метод [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) , который принимает объект **XmlWriter** и записывает XML потока.</span><span class="sxs-lookup"><span data-stu-id="cb828-263">The **XDocument** class exposes a [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) method that takes an **XmlWriter** object and writes XML back to a stream.</span></span> 
  
<span data-ttu-id="cb828-264">Используйте следующую процедуру, чтобы сохранить XML-код на странице Visio часть содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="cb828-264">Use the following procedure to save the XML from the Visio page back to the Page Contents part.</span></span>
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a><span data-ttu-id="cb828-265">Чтобы сохранить измененный XML-код пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-265">To save the changed XML back to the package</span></span>

1. <span data-ttu-id="cb828-266">После `GetXElementByAttribute` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-266">After the  `GetXElementByAttribute` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

2. <span data-ttu-id="cb828-267">Добавьте следующий код в **с помощью** блок в методе **Main** **программы** класса (блок **Using** метода **Main** в **модуль1** в Visual Basic), под кодом на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="cb828-267">Add the following code to the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), beneath the code from the previous procedure.</span></span> 
    
  ```cs
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

3. <span data-ttu-id="cb828-268">Нажмите клавишу F5 для отладки решения.</span><span class="sxs-lookup"><span data-stu-id="cb828-268">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="cb828-269">После завершения работы программы нажмите любую клавишу, чтобы выйти из.</span><span class="sxs-lookup"><span data-stu-id="cb828-269">When the program has completed running, choose any key to exit.</span></span>
    
4. <span data-ttu-id="cb828-270">Откройте файл Visio Package.vsdx в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-270">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="cb828-271">Начальная или завершающая фигура теперь должен содержать текст «Пуск процесса».</span><span class="sxs-lookup"><span data-stu-id="cb828-271">The Start/End shape should now contain the text "Start process".</span></span>
  
## <a name="recalculate-data-in-the-file"></a><span data-ttu-id="cb828-272">Пересчет данных в файле</span><span class="sxs-lookup"><span data-stu-id="cb828-272">Recalculate data in the file</span></span>
<span data-ttu-id="cb828-273"><a name="vis15_ManipulateFF_Recalculate"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-273"></span></span>

<span data-ttu-id="cb828-274">Некоторые изменения данных в файле может потребоваться Visio для пересчета документ при открытии файла.</span><span class="sxs-lookup"><span data-stu-id="cb828-274">Some changes to the data in a file may require Visio to recalculate the document when it opens the file.</span></span> <span data-ttu-id="cb828-275">Visio предоставляет множество логику для схемы, особенно для отношения фигур (то есть, когда один фигуры зависит от другого) и подключение фигур.</span><span class="sxs-lookup"><span data-stu-id="cb828-275">Visio provides a lot of logic for a diagram, particularly for shape relationships (that is, when one shape depends on another) and connecting shapes.</span></span> <span data-ttu-id="cb828-276">Если какие-либо данные, которая использует настраиваемой логики при изменении Visio необходимо распространить изменения ко всем затронутых вычисляемых данных в файле.</span><span class="sxs-lookup"><span data-stu-id="cb828-276">If any of the data that the custom logic relies upon is changed, Visio needs to propagate the changes to all of the affected calculated data in the file.</span></span> 
  
<span data-ttu-id="cb828-277">Формат файлов Visio 2013 включает в себя несколько методов, которые можно использовать для пересчета данных в файле.</span><span class="sxs-lookup"><span data-stu-id="cb828-277">The Visio 2013 file format includes a couple of techniques that you can use to recalculate data in the file.</span></span> <span data-ttu-id="cb828-278">Существует три типа из сценариев, которые необходимо учитывать при решить, нужно ли пересчитывать файла Visio и как это сделать.</span><span class="sxs-lookup"><span data-stu-id="cb828-278">There are three types of scenarios that you must consider when you decide whether you need to recalculate the Visio file and how to do it:</span></span>
  
- <span data-ttu-id="cb828-279">Изменения в данные не влияют на другие значения в формате файлов.</span><span class="sxs-lookup"><span data-stu-id="cb828-279">The changes to the data do not affect any other values in the file format.</span></span> <span data-ttu-id="cb828-280">Добавьте любые дополнительные инструкции для Visio для пересчета документа не требуется.</span><span class="sxs-lookup"><span data-stu-id="cb828-280">You don't need to add any additional instructions to Visio to recalculate the document.</span></span> <span data-ttu-id="cb828-281">Как было показано ранее, зачастую можно изменить текстом фигуры без необходимости пересчитывать документа.</span><span class="sxs-lookup"><span data-stu-id="cb828-281">As demonstrated previously, you can often change a shape's text without needing to recalculate the document.</span></span>
    
- <span data-ttu-id="cb828-282">Изменения данных ограничен изменение значения ячейки таблицы свойств фигуры в XML-КОДЕ, и других значений таблицы свойств фигуры, которые зависят от этих данных.</span><span class="sxs-lookup"><span data-stu-id="cb828-282">The changes to the data are limited to changing the values of ShapeSheet cells in the XML, and there are other ShapeSheet values that depend on this data.</span></span> <span data-ttu-id="cb828-283">В этом случае необходимо добавить инструкции (с помощью класса [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) ) на элемент **ячейки** , были ли изменены XML.</span><span class="sxs-lookup"><span data-stu-id="cb828-283">In this case, you must add an XML processing instruction (using the [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) class) to the **Cell** element that has been changed.</span></span> <span data-ttu-id="cb828-284">Например ячейки **ThemeIndex** фигуры влияет на значений нескольких таблиц свойств фигур ячеек, содержащихся в форме.</span><span class="sxs-lookup"><span data-stu-id="cb828-284">For example, the **ThemeIndex** cell for a shape affects the values of several other ShapeSheet cells contained in the shape.</span></span> <span data-ttu-id="cb828-285">При изменении ячейки **ThemeIndex** в файле (например, элемент **ячейки** со значением **N** «ThemeIndex»), необходимо будет добавьте инструкции обработки в элемент **ячейки** , чтобы обновить зависимых значений .</span><span class="sxs-lookup"><span data-stu-id="cb828-285">If you change the **ThemeIndex** cell within the file itself (for example, the **Cell** element with an **N** value of "ThemeIndex"), you will need to add a processing instruction to the **Cell** element so that the dependent values are updated.</span></span> 
    
- <span data-ttu-id="cb828-286">Изменения данных влияет на расположение соединитель или подключение точек.</span><span class="sxs-lookup"><span data-stu-id="cb828-286">The changes to the data affect the location of a connector or connection points.</span></span> <span data-ttu-id="cb828-287">Другая ситуация — когда существует множество изменений в данные таблицы свойств фигуры и обновить всего документа с одной инструкции (а не Добавление инструкции по обработке отдельных для каждого изменения).</span><span class="sxs-lookup"><span data-stu-id="cb828-287">Another situation is when there are many changes to the ShapeSheet data and you want to recalculate the whole document with one instruction (rather than adding individual processing instructions for each change).</span></span> <span data-ttu-id="cb828-288">В этом случае можно указать Visio для пересчета весь документ при открытии.</span><span class="sxs-lookup"><span data-stu-id="cb828-288">In this case you can instruct Visio to recalculate the entire document when it is opened.</span></span> <span data-ttu-id="cb828-289">Это делается путем добавления свойство **RecalcDocument** часть настраиваемых свойств файла (/ docProps/custom.xml) пакета Visio.</span><span class="sxs-lookup"><span data-stu-id="cb828-289">You do this by adding a **RecalcDocument** property to the Custom File Properties part (/docProps/custom.xml) of the Visio package.</span></span> <span data-ttu-id="cb828-290">Настройка положения или размера фигур на схеме подключенных приводится пример этого типа сценария.</span><span class="sxs-lookup"><span data-stu-id="cb828-290">Adjusting the position or size of shapes in a connected diagram is an example of this type of scenario.</span></span> 
    
    <span data-ttu-id="cb828-291">Имейте в виду, что это наиболее высоких вариант с точки зрения производительности.</span><span class="sxs-lookup"><span data-stu-id="cb828-291">Keep in mind that this is the most costly option from a performance standpoint.</span></span>
    
<span data-ttu-id="cb828-292">Используйте следующую процедуру для вставки элемент **ячейки** в элемент **фигуры** , где другие элементы **ячеек** этой же **формы** нужно перерасчете из-за новое значение.</span><span class="sxs-lookup"><span data-stu-id="cb828-292">Use the following procedure to insert a **Cell** element into a **Shape** element, where other **Cell** elements in the same **Shape** need to be recalculated because of the new value.</span></span> <span data-ttu-id="cb828-293">Новый элемент **ячейки** включает в себя инструкцией по обработке дочерний элемент для оповещения Visio, необходимые для выполнения некоторых локального пересчета.</span><span class="sxs-lookup"><span data-stu-id="cb828-293">The new **Cell** element includes a processing instruction as a child element, to inform Visio that it needs to perform some local recalculation.</span></span> 
  
### <a name="to-recalculate-values-for-a-single-shape"></a><span data-ttu-id="cb828-294">Для пересчета значений для отдельных фигур</span><span class="sxs-lookup"><span data-stu-id="cb828-294">To recalculate values for a single shape</span></span>

1. <span data-ttu-id="cb828-295">Замените код из предыдущих двух примерах (изменение текста фигуры и вызов `SaveXDocumentToPart`) в блоке **с помощью** метода **Main** класса **Program** (блок **Using** метода **Main** в **модуль1** в Visual Basic) с помощью следующего кода.</span><span class="sxs-lookup"><span data-stu-id="cb828-295">Replace the code from the previous two examples (changing the shape's text and the call to  `SaveXDocumentToPart`) in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic) with the following code.</span></span> 
    
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

2. <span data-ttu-id="cb828-296">Нажмите клавишу F5 для отладки решения.</span><span class="sxs-lookup"><span data-stu-id="cb828-296">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="cb828-297">После завершения работы программы нажмите любую клавишу, чтобы выйти из.</span><span class="sxs-lookup"><span data-stu-id="cb828-297">When the program has completed running, choose any key to exit.</span></span>
    
3. <span data-ttu-id="cb828-298">Откройте файл Visio Package.vsdx в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-298">Open the Visio Package.vsdx file in Visio 2013.</span></span> <span data-ttu-id="cb828-299">Начальная или завершающая фигура теперь должен иметь разные заливки.</span><span class="sxs-lookup"><span data-stu-id="cb828-299">The Start/End shape should now have a different fill color.</span></span>
    
<span data-ttu-id="cb828-300">Цвет фигуры зависит от значения ячейки **ThemeIndex** — определяет, наследующий active тем фигуры.</span><span class="sxs-lookup"><span data-stu-id="cb828-300">The shape's color relies on the value of the **ThemeIndex** cell—it determines which of the active themes the shape inherits from.</span></span> <span data-ttu-id="cb828-301">В предыдущем примере фигуры устанавливается наследование от другой темы (ячейки **ThemeIndex** задано значение «25»).</span><span class="sxs-lookup"><span data-stu-id="cb828-301">In the previous example, the shape is set to inherit from a different theme (the **ThemeIndex** cell is set to a value of "25").</span></span> <span data-ttu-id="cb828-302">Если не использовать команды обработки, цвет текста фигуры, которой также влияет ячейки **ThemeIndex** — не перерасчете.</span><span class="sxs-lookup"><span data-stu-id="cb828-302">If you don't use a processing instruction, the shape's text color—which is also affected by the **ThemeIndex** cell—isn't recalculated.</span></span> <span data-ttu-id="cb828-303">Изменить цвет заливки фигуры на технический, но останется белый текст, а текст не будут считываться.</span><span class="sxs-lookup"><span data-stu-id="cb828-303">The shape's fill color would change to white, but its text would remain white—leaving the text unreadable.</span></span> <span data-ttu-id="cb828-304">Кроме того без команды обработки, возможно, что Visio может обновляться фигуры в нужный момент, отправляемых из файла в нестабильном состоянии, где форматирования значения фигуры могут быть обновлены непредсказуемым образом.</span><span class="sxs-lookup"><span data-stu-id="cb828-304">Also, without the processing instruction, it is possible that Visio may update the shape at a later date, leaving the file in an unstable state where the formatting values of the shape could be updated unpredictably.</span></span> 
  
<span data-ttu-id="cb828-305">При изменении данных в файл, который требует Visio для пересчета документов (например, изменение положения подключенных фигур и, таким образом, принудительную соединителей для перенаправления), необходимо добавить пересчета инструкции в файле Visio.</span><span class="sxs-lookup"><span data-stu-id="cb828-305">If you change data in the file that requires Visio to recalculate the document (for example, changing a connected shape's position and, therefore, forcing the connectors to reroute), you must add a recalculation instruction to the Visio file.</span></span> <span data-ttu-id="cb828-306">Инструкции по создается путем добавления элемента **Свойства** со значением атрибута **имя** «RecalcDocument» к XML-части настраиваемых свойств файла пакета файла Visio.</span><span class="sxs-lookup"><span data-stu-id="cb828-306">The instruction is created by adding a **property** element with a **name** attribute value of "RecalcDocument" to the XML of the Custom File Properties part of the Visio file package.</span></span> <span data-ttu-id="cb828-307">Рекомендуется следует проверить часть настраиваемые свойства файла убедитесь, что инструкции «RecalcDocument» еще не зарегистрирован в файле.</span><span class="sxs-lookup"><span data-stu-id="cb828-307">As a best practice, you should check the Custom File Properties part to be sure that a "RecalcDocument" instruction hasn't already been registered in the file.</span></span> 
  
<span data-ttu-id="cb828-308">Используйте следующий код, чтобы изменить значение ячейки **PinY** Начальная или завершающая фигура в предыдущих примерах.</span><span class="sxs-lookup"><span data-stu-id="cb828-308">Use the following code to change the value of the **PinY** cell of the Start/End shape from the previous examples.</span></span> <span data-ttu-id="cb828-309">Код выбирает элемент **ячейки** , который содержит данные ячейки **PinY** как объект **XElement** с помощью значения атрибута **N** .</span><span class="sxs-lookup"><span data-stu-id="cb828-309">The code selects the **Cell** element that contains the **PinY** cell data as an **XElement** object by using the value of its **N** attribute.</span></span> <span data-ttu-id="cb828-310">Затем код добавляет пересчета инструкции в настраиваемых свойств файла часть файла Visio.</span><span class="sxs-lookup"><span data-stu-id="cb828-310">The code then adds a recalculation instruction to the Custom File Properties part of the Visio file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cb828-311">Этот код основан на `GetPackagePart` и `SaveXDocumentToPart` методы, созданные ранее.</span><span class="sxs-lookup"><span data-stu-id="cb828-311">This code relies on the  `GetPackagePart` and  `SaveXDocumentToPart` methods created previously.</span></span> 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a><span data-ttu-id="cb828-312">Для пересчета весь документ при открытии</span><span class="sxs-lookup"><span data-stu-id="cb828-312">To recalculate the entire document when it is opened</span></span>

1. <span data-ttu-id="cb828-313">После `SaveXDocumentToPart` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-313">After the  `SaveXDocumentToPart` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

2. <span data-ttu-id="cb828-314">После `RecalcDocument` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-314">After the  `RecalcDocument` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="cb828-315">Замените код из предыдущего примера в блоке **с помощью** метода **Main** класса **Program** (блок **Using** метода **Main** в **модуль1** в Visual Basic), с помощью следующего кода.</span><span class="sxs-lookup"><span data-stu-id="cb828-315">Replace the code from the previous example in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
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

4. <span data-ttu-id="cb828-316">Нажмите клавишу F5 для отладки решения.</span><span class="sxs-lookup"><span data-stu-id="cb828-316">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="cb828-317">После завершения работы программы нажмите любую клавишу, чтобы выйти из.</span><span class="sxs-lookup"><span data-stu-id="cb828-317">When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="cb828-318">Откройте файл Visio Package.vsdx в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-318">Open the Visio Package.vsdx file in Visio 2013.</span></span> 
    
<span data-ttu-id="cb828-319">Начальная или завершающая фигура теперь должна появиться 2 дюйма от верхней границы документа.</span><span class="sxs-lookup"><span data-stu-id="cb828-319">The Start/End shape should now be 2 inches from the bottom edge of the drawing.</span></span> <span data-ttu-id="cb828-320">Соединитель между Начальная или завершающая фигура и форма процесс должен пересылаются внесения изменений в макет.</span><span class="sxs-lookup"><span data-stu-id="cb828-320">The connector between the Start/End shape and the Process shape should have rerouted to accommodate the change in layout.</span></span> <span data-ttu-id="cb828-321">Если свойство **RecalcDocument** еще не добавлена в файл, положения фигуры будут изменены, но соединитель не будет иметь переадресован в новом расположении фигуры.</span><span class="sxs-lookup"><span data-stu-id="cb828-321">If the **RecalcDocument** property had not been added to the file, the shape position would have been changed, but the connector would not have rerouted to the new location of the shape.</span></span> 
  
## <a name="add-a-new-package-part-to-a-package"></a><span data-ttu-id="cb828-322">Добавьте новую часть пакета для пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-322">Add a new package part to a package</span></span>
<span data-ttu-id="cb828-323"><a name="vis15_ManipulateFF_AddNewPart"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-323"></span></span>

<span data-ttu-id="cb828-324">Одним из наиболее распространенных сценариев для изменения файла пакета Добавление новой части документа в пакет.</span><span class="sxs-lookup"><span data-stu-id="cb828-324">One of the most common scenarios for modifying a file package is adding a new document part to the package.</span></span> <span data-ttu-id="cb828-325">Например если вы хотите добавить страницу документа путем добавления контента в пакет Visio, необходимо добавить часть содержимого страницы в пакет.</span><span class="sxs-lookup"><span data-stu-id="cb828-325">For example, if you want to add a page to the Visio drawing by adding content to the package, you need to add a Page Contents part to the package.</span></span> 
  
<span data-ttu-id="cb828-326">Процесс добавления новой части пакета осуществляется просто:</span><span class="sxs-lookup"><span data-stu-id="cb828-326">The process for adding a new part to the package is straightforward:</span></span> 
  
1. <span data-ttu-id="cb828-327">Создание XML-документа с данными для **PackagePart**.</span><span class="sxs-lookup"><span data-stu-id="cb828-327">You create the XML document with the data for the **PackagePart**.</span></span> <span data-ttu-id="cb828-328">Необходимо уделить особое внимание пространства имен XML, управляющие схемы для конкретного типа XML-документа, создаваемого.</span><span class="sxs-lookup"><span data-stu-id="cb828-328">You need to pay special attention to the XML namespaces that govern the schema for the specific type of XML document that you create.</span></span>
    
2. <span data-ttu-id="cb828-329">Создайте новый файл для XML-код и сохраните файл в расположение, в **пакет**.</span><span class="sxs-lookup"><span data-stu-id="cb828-329">You create a new file to contain the XML and save the file to a location in the **Package**.</span></span>
    
3. <span data-ttu-id="cb828-330">Создайте необходимые связи между новой **PackagePart** и **пакет** или другие объекты **PackagePart** .</span><span class="sxs-lookup"><span data-stu-id="cb828-330">You create the necessary relationships between the new **PackagePart** and the **Package** or other **PackagePart** objects.</span></span> 
    
4. <span data-ttu-id="cb828-331">Обновите все существующие части, которые должны ссылаться на новую часть.</span><span class="sxs-lookup"><span data-stu-id="cb828-331">You update any existing parts that need to reference the new part.</span></span> <span data-ttu-id="cb828-332">Например при добавлении новой части содержимого страницы (новая страница) для файла также потребуется обновить часть страницы индекса (/visio/pages/pages.xml-файл) правильные сведения о новой страницы.</span><span class="sxs-lookup"><span data-stu-id="cb828-332">For example, if you add a new Page Contents part (a new page) to the file, you also need to update the Page Index part (/visio/pages/pages.xml file) to include the correct information about the new page.</span></span>
    
<span data-ttu-id="cb828-333">Используйте следующую процедуру, чтобы создать новую часть расширяемость ленты в файле Visio.</span><span class="sxs-lookup"><span data-stu-id="cb828-333">Use the following procedure to create a new Ribbon Extensibility part in the Visio file.</span></span> <span data-ttu-id="cb828-334">Добавляет новую часть расширяемость ленты новую вкладку с одной группой, содержащий одну кнопку ленты.</span><span class="sxs-lookup"><span data-stu-id="cb828-334">The new Ribbon Extensibility part adds to the ribbon a new tab with a single group that contains a single button.</span></span>
  
### <a name="to-create-a-new-package-part"></a><span data-ttu-id="cb828-335">Чтобы создать новую часть пакета</span><span class="sxs-lookup"><span data-stu-id="cb828-335">To create a new package part</span></span>

1. <span data-ttu-id="cb828-336">После `CheckForRecalc` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-336">After the  `CheckForRecalc` method in the **Program** class (or **Module1** in Visual Basic) from the previous procedure, add the following method.</span></span> 
    
  ```cs
  private static XDocument CreateCustomUI()
  {
      // Add a new Custom User Interface document part to the package.
      // This code adds a new CUSTOM tab to the ribbon for this
      // document. The tab has one group that contains one button.
      XNamespace customUINS = 
          "https://schemas.microsoft.com/office/2006/01/customui";
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
          "https://schemas.microsoft.com/office/2006/01/customui"
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

2. <span data-ttu-id="cb828-337">После `CreateCustomUI` метода в класс **программа** (или **модуль1** в Visual Basic) на предыдущем шаге, добавьте следующий метод.</span><span class="sxs-lookup"><span data-stu-id="cb828-337">After the  `CreateCustomUI` method in the **Program** class (or **Module1** in Visual Basic) from the previous step, add the following method.</span></span> 
    
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

3. <span data-ttu-id="cb828-338">Замените весь код в **с помощью** блокировки в **методе класса **программы** (блок **Using** метода **Main** в **модуль1** в Visual Basic),** с помощью следующего кода.</span><span class="sxs-lookup"><span data-stu-id="cb828-338">Replace all the code in the **using** block in the **Main** method of the **Program** class (the **Using** block of the **Main** method in **Module1** in Visual Basic), with the following code.</span></span> 
    
  ```cs
  // Create a new Ribbon Extensibility part and add it to the file.
  XDocument customUIXML = CreateCustomUI();
  CreateNewPackagePart(visioPackage, customUIXML, 
      new Uri("/customUI/customUI1.xml", UriKind.Relative),
      "application/xml",
      "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
  ```

  ```vb
  ' Create a new Ribbon Extensibility part and add it to the file.
  Dim customUIXML As XDocument = CreateCustomUI()
  CreateNewPackagePart(visioPackage, customUIXML, _
      New Uri("/customUI/customUI1.xml", UriKind.Relative), _
      "application/xml", _
      "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
  ```

4. <span data-ttu-id="cb828-339">Нажмите клавишу F5 для отладки решения.</span><span class="sxs-lookup"><span data-stu-id="cb828-339">Choose the F5 key to debug the solution.</span></span> <span data-ttu-id="cb828-340">После завершения работы программы нажмите любую клавишу, чтобы выйти из.</span><span class="sxs-lookup"><span data-stu-id="cb828-340">When the program has completed running, choose any key to exit.</span></span>
    
5. <span data-ttu-id="cb828-341">Откройте файл Visio Package.vsdx в Visio 2013 и затем выберите вкладку **НАСТРАИВАЕМЫЕ** .</span><span class="sxs-lookup"><span data-stu-id="cb828-341">Open the Visio Package.vsdx file in Visio 2013, and then choose the **CUSTOM** tab.</span></span> 
    
<span data-ttu-id="cb828-342">Настраиваемая лента похожа на рисунке 2 при открытии файла в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cb828-342">The custom ribbon looks like Figure 2 when the file is opened in Visio 2013.</span></span>
  
 <span data-ttu-id="cb828-343">**На рисунке 2. Настраиваемая вкладка на ленте Visio 2013**</span><span class="sxs-lookup"><span data-stu-id="cb828-343">**Figure 2. Custom tab in the Visio 2013 ribbon**</span></span>
  
![Настраиваемая вкладка на ленте](media/vis15_CustomRibbonTab.PNG)
  
<span data-ttu-id="cb828-345">XML-код, созданный с `CreateCustomUI` метод выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="cb828-345">The XML created by the  `CreateCustomUI` method looks like the following.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="https://schemas.microsoft.com/office/2006/01/customui">
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

## <a name="acknowledgements"></a><span data-ttu-id="cb828-346">Благодарности</span><span class="sxs-lookup"><span data-stu-id="cb828-346">Acknowledgements</span></span>
<span data-ttu-id="cb828-347"><a name="vis15_ManipulateFF_Ackn"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-347"></span></span>

<span data-ttu-id="cb828-348">Мы хотим высказать распознает вклад и ввода Visio со статусом MVP **Al Edlund** при создании примеров кода, содержащихся в данной технической статье.</span><span class="sxs-lookup"><span data-stu-id="cb828-348">We would like to recognize the contribution and input of Visio MVP **Al Edlund** in creating the code examples contained in this technical article.</span></span> <span data-ttu-id="cb828-349">Al является распознанный expert управления формат файла Visio, включая формат XML документа Visio (.vdx) и новый формат файла Visio (vsdx (en).</span><span class="sxs-lookup"><span data-stu-id="cb828-349">Al is a recognized expert in manipulating the Visio file format, including both the Visio XML Drawing format (.vdx) and the new Visio file format (.vsdx).</span></span> <span data-ttu-id="cb828-350">Al создал проектов, изучите программными средствами в новые форматы файлов Visio и предоставляет структуры внутри.</span><span class="sxs-lookup"><span data-stu-id="cb828-350">Al has created projects that explore the Visio file formats programmatically and exposes the structures inside.</span></span> 
  
<span data-ttu-id="cb828-351">Дополнительные сведения о всех режимов могли работать с формат файла Visio воспользуйтесь ссылками в разделе Дополнительные ресурсы, исходя из.</span><span class="sxs-lookup"><span data-stu-id="cb828-351">For more information about Al's work with the Visio file format, see the links in the Additional Resources section that follows.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb828-352">См. также</span><span class="sxs-lookup"><span data-stu-id="cb828-352">See also</span></span>
<span data-ttu-id="cb828-353"><a name="vis15_ManipulateFF_Additional"> </a></span><span class="sxs-lookup"><span data-stu-id="cb828-353"></span></span>

- <span data-ttu-id="cb828-354">С Al Edlund:</span><span class="sxs-lookup"><span data-stu-id="cb828-354">By Al Edlund:</span></span>
    
  - <span data-ttu-id="cb828-355">проект [pkgVisio - Visio 2013 XML выполнение различных операций](https://pkgvisio.codeplex.com/documentation) на сайте CodePlex.</span><span class="sxs-lookup"><span data-stu-id="cb828-355">[pkgVisio - Visio 2013 XML manipulation](https://pkgvisio.codeplex.com/documentation) project on CodePlex.</span></span> 
    
  - <span data-ttu-id="cb828-356">[pkgVisio_pt1](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) видео на YouTube.</span><span class="sxs-lookup"><span data-stu-id="cb828-356">[pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) video on YouTube.</span></span> 
    
  - <span data-ttu-id="cb828-357">[pkgVisio_pt2](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) видео на YouTube.</span><span class="sxs-lookup"><span data-stu-id="cb828-357">[pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) video on YouTube.</span></span> 
    
- [<span data-ttu-id="cb828-358">Центр по разработке для Visio</span><span class="sxs-lookup"><span data-stu-id="cb828-358">Visio Developer Center</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [<span data-ttu-id="cb828-359">Работа с документами форматов Office Open XML</span><span class="sxs-lookup"><span data-stu-id="cb828-359">Manipulate Office Open XML Formats Documents</span></span>](https://msdn.microsoft.com/library/aa982683%28v=office.12%29.aspx)
    
- [<span data-ttu-id="cb828-360">Создание документа с пространствами имен (C#) (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="cb828-360">Create a Document with Namespaces (C#) (LINQ to XML)</span></span>](https://msdn.microsoft.com/library/bb387075.aspx)
    
- [<span data-ttu-id="cb828-361">Добавление пользовательской XML-части в документ без запуска Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="cb828-361">Add Custom XML Parts to Documents Without Starting Microsoft Office</span></span>](https://msdn.microsoft.com/library/bb608597%28VS.90%29.aspx)
    

