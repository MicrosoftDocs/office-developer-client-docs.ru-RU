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
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="d6607-103">Общие сведения о формате файлов Visio (VSDX)</span><span class="sxs-lookup"><span data-stu-id="d6607-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="d6607-104">Сведения о новом формате в Visio 2013 некоторые высокого уровня понятия по работе с формат файлов Visio 2013 программными средствами и создание простого консольного приложения, которое проверяет файл Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d6607-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6607-105">**В этой статье** [Общие сведения](#vis15_IntroVSDX_Intro) [Формат файла Visio 2013 «за кулисами»?](#vis15_IntroVSDX_What)                   </span><span class="sxs-lookup"><span data-stu-id="d6607-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="d6607-106">[Сценарии разработчика для работы с формат файлов Visio 2013](#vis15_IntroVSDX_Scenarios) [Обзор возможностей в формат файлов Visio 2013 программными средствами](#vis15_IntroVSDX_Explore) [Дополнительные материалы](#vis15_IntroVSDX_Resources)                    </span><span class="sxs-lookup"><span data-stu-id="d6607-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="d6607-107">Введение</span><span class="sxs-lookup"><span data-stu-id="d6607-107">Introduction</span></span>
<span data-ttu-id="d6607-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="d6607-108"></span></span>

<span data-ttu-id="d6607-109">Visio 2013 представлен новый формат файла (vsdx (en) для Visio, которая заменяет формата двоичного файла Visio (.vsd) и формат файлов XML документа Visio (.vdx).</span><span class="sxs-lookup"><span data-stu-id="d6607-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="d6607-110">Так как в формат файлов Visio 2013 основан на параметрах Open Packaging Conventions и XML, разработчики, так как они знакомы с этими технологиями можно быстро Узнайте, как для программной работы с файлами Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d6607-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="d6607-111">Разработчики, знакомые с форматом файла документ XML Visio (.vdx) из предыдущих версий Visio можно найти многие из одной структуры XML внутри части формата файла vsdx (en).</span><span class="sxs-lookup"><span data-stu-id="d6607-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="d6607-112">Взаимодействие с файлами Visio значительно возрастает с момента программного обеспечения сторонних производителей могут управлять файлов Visio на уровне формата файла.</span><span class="sxs-lookup"><span data-stu-id="d6607-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="d6607-113">Формат файлов Visio 2013 поддерживается в службах Visio в Microsoft SharePoint Server 2013 без необходимости «промежуточный» формат файла для публикации в SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="d6607-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="d6607-114">Существует несколько типов файлов с расширением, образующих формат файлов Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d6607-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="d6607-115">Файлы с этим расширением включают:</span><span class="sxs-lookup"><span data-stu-id="d6607-115">These extensions include:</span></span>
  
- <span data-ttu-id="d6607-116">VSDX (документ Visio),</span><span class="sxs-lookup"><span data-stu-id="d6607-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="d6607-117">VSDM (документ Visio с поддержкой макросов),</span><span class="sxs-lookup"><span data-stu-id="d6607-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="d6607-118">VSSX (набор элементов Visio),</span><span class="sxs-lookup"><span data-stu-id="d6607-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="d6607-119">VSSM (набор элементов Visio с поддержкой макросов),</span><span class="sxs-lookup"><span data-stu-id="d6607-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="d6607-120">VSTX (шаблон Visio),</span><span class="sxs-lookup"><span data-stu-id="d6607-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="d6607-121">VSTM (шаблон Visio с поддержкой макросов).</span><span class="sxs-lookup"><span data-stu-id="d6607-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="d6607-122">Только с поддержкой макросов файлы (.vsdm, .vssm, .vstm) можно хранить макросов VBA.</span><span class="sxs-lookup"><span data-stu-id="d6607-122">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros.</span></span> <span data-ttu-id="d6607-123">Нельзя хранить макросов в файлах с vsdx (en), .vssx или .vstx расширения.</span><span class="sxs-lookup"><span data-stu-id="d6607-123">You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="d6607-124">Что такое формат файлов Visio 2013 «за кулисами»</span><span class="sxs-lookup"><span data-stu-id="d6607-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="d6607-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="d6607-125"></span></span>

<span data-ttu-id="d6607-126">Формат файлов Visio 2013 использует Open упаковки Conventions (OPC), определяющий структурированных означает, что для хранения данных приложения вместе с другими материалами, с помощью контейнера некоторые примеры sort─for в ZIP-файле.</span><span class="sxs-lookup"><span data-stu-id="d6607-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="d6607-127">В общем случае файла Visio 2013 все сводится к ZIP-контейнер, содержащий других типов файлов.</span><span class="sxs-lookup"><span data-stu-id="d6607-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="d6607-128">На самом деле сохранения документа в Visio 2013 в формате vsdx (en), измените расширение файла для "\*.zip» в проводнике Windows и затем откройте файл как папку, чтобы просмотреть его содержимое.</span><span class="sxs-lookup"><span data-stu-id="d6607-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="d6607-129">В этой статье содержится краткий обзор Open Packaging Conventions.</span><span class="sxs-lookup"><span data-stu-id="d6607-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="d6607-130">Можно найти более подробные покрытия условные обозначения в других статьях: > Дополнительные сведения об Open Packaging Conventions сами можно [OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6607-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="d6607-131">> Дополнительные сведения об Open Packaging Conventions и их использование в файлы Microsoft Office можно [основные моменты спецификаций Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) и [Краткие сведения о форматах файлов Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6607-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](https://msdn.microsoft.com/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="d6607-132">Пакеты и части пакета</span><span class="sxs-lookup"><span data-stu-id="d6607-132">Packages and Package Parts</span></span>

<span data-ttu-id="d6607-133">Как работы более ранних версий, файлов Visio 2013, контейнеров ZIP или «пакеты», который содержать другие файлы (называемого «части пакета») в них.</span><span class="sxs-lookup"><span data-stu-id="d6607-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="d6607-134">Часть пакета может быть XML-файла, изображения, даже решения VBA.</span><span class="sxs-lookup"><span data-stu-id="d6607-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="d6607-135">Части в пакете, можно разделить на две основные категории, «части документа» и «компоненты связей».</span><span class="sxs-lookup"><span data-stu-id="d6607-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="d6607-136">Части документа содержит фактические контента и метаданных файла Visio, например имя файла, первой страницы и всех фигур, которые он содержит, и даже подключения к данным для фигур.</span><span class="sxs-lookup"><span data-stu-id="d6607-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="d6607-137">Изображения и текстовые файлы в пакете, считаются частями документа.</span><span class="sxs-lookup"><span data-stu-id="d6607-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="d6607-138">Связь частей описаны более подробно далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="d6607-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d6607-139">При открытии файла Visio 2013, с помощью служебной программы ZIP, вероятно, можно увидеть несколько папок, содержащихся в ZIP-архив.</span><span class="sxs-lookup"><span data-stu-id="d6607-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="d6607-140">Можно даже работы с этих вложенных адреса папок с помощью программы ZIP.</span><span class="sxs-lookup"><span data-stu-id="d6607-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="d6607-141">Тем не менее эти «папки» представления подменю адресов в ZIP-архив, а не фактические папок.</span><span class="sxs-lookup"><span data-stu-id="d6607-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="d6607-142">Программный эквивалентами папок нельзя использовать для работы с эти подменю адреса в решении.</span><span class="sxs-lookup"><span data-stu-id="d6607-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="d6607-143">Части документа пакета parts─both и parts─also отношения связаны типов контента.</span><span class="sxs-lookup"><span data-stu-id="d6607-143">Package parts─both document parts and relationship parts─also have associated content types.</span></span> <span data-ttu-id="d6607-144">Эти типы контента, строк, которые определяют тип мультимедиа MIME.</span><span class="sxs-lookup"><span data-stu-id="d6607-144">These content types are strings that define a MIME media type.</span></span> <span data-ttu-id="d6607-145">Эти типы контента укажите и область вид типы MIME, которые могут содержаться в файле.</span><span class="sxs-lookup"><span data-stu-id="d6607-145">These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="d6607-146">Связи</span><span class="sxs-lookup"><span data-stu-id="d6607-146">Relationships</span></span>

<span data-ttu-id="d6607-147">Связь частей (которого заканчивается на данное расширение имени файла "\*находится» и сохраняются в папке «_rels») описывается, как части в пакете, которые относятся к друг с другом и предоставляют структура файла.</span><span class="sxs-lookup"><span data-stu-id="d6607-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="d6607-148">В XML-документ автономных использует отношения родительских и дочерних элементов для определения отношения сущностей друг с другом.</span><span class="sxs-lookup"><span data-stu-id="d6607-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="d6607-149">Другие файлы использовать другие иерархии или структуру папок файла для описания взаимодействия содержимого в файле.</span><span class="sxs-lookup"><span data-stu-id="d6607-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="d6607-150">Для формат файлов Visio 2013 пакета является файл Visio, если он содержит правильное набора частей и пакет содержит отношений между частями.</span><span class="sxs-lookup"><span data-stu-id="d6607-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="d6607-151">Части отношения, XML-документов, которые описывают отношения между частями другого документа в пакете.</span><span class="sxs-lookup"><span data-stu-id="d6607-151">Relationship parts are XML documents that describe the relationships between different document parts within the package.</span></span> <span data-ttu-id="d6607-152">Они определить связь между двумя элементами: указанного источника (определяется с помощью имя и расположение файла связи) и указанный целевой части документа.</span><span class="sxs-lookup"><span data-stu-id="d6607-152">They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part.</span></span> <span data-ttu-id="d6607-153">К примеру связь частей используются для описания, какие фигуры образцов связаны с файла, как страницы, которые относятся к файлу и друг с другом или как изображения и объекты связаны с конкретной страницы.</span><span class="sxs-lookup"><span data-stu-id="d6607-153">For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="d6607-154">Сходства и различия с использованием схемы Visio VDX</span><span class="sxs-lookup"><span data-stu-id="d6607-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="d6607-155">Как уже было сказано, последние версии Visio также включаются XML-файл формата, формат XML документа Visio или .vdx.</span><span class="sxs-lookup"><span data-stu-id="d6607-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="d6607-156">(В предыдущих версиях программы схемы, используемой для XML-документа Visio формат называется datadiagramml (en)). Некоторые элементы из схемы Visio XML лет между двумя форматах.</span><span class="sxs-lookup"><span data-stu-id="d6607-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="d6607-157">Например элемент **Windows** и его дочерние элементы остаются unchanged─with исключение, что элемент **Windows** теперь является корневой элемент XML-документа (window.xml).</span><span class="sxs-lookup"><span data-stu-id="d6607-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="d6607-158">Наибольшее различие между формата документа XML и формат файлов Visio 2013 — это упаковки.</span><span class="sxs-lookup"><span data-stu-id="d6607-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="d6607-159">Файл XML-документ формате может таким образом, как обычный изолированный XML; формат файлов Visio 2013 должны обрабатываться как пакет.</span><span class="sxs-lookup"><span data-stu-id="d6607-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="d6607-160">В Visio 2013 XML разделенный на части для удобства использования.</span><span class="sxs-lookup"><span data-stu-id="d6607-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="d6607-161">Другое изменение заметно — это, что формат файлов Visio 2013 сохраняет все свойства документа в части документа описываемых OPC standard (app.xml, core.xml, custom.xml).</span><span class="sxs-lookup"><span data-stu-id="d6607-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="d6607-162">Однако существует один значительные изменения, необходимо иметь в виду всех разработчиков Visio: введение в элементы **ячеек**, **строк**и **раздел** .</span><span class="sxs-lookup"><span data-stu-id="d6607-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="d6607-163">В этой схеме формат XML-файла документа отдельных строк и ячеек в таблице свойств фигуры представлены именованные элементы.</span><span class="sxs-lookup"><span data-stu-id="d6607-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="d6607-164">Например предположим, что у вас есть документ с одной страницы, которая содержит фигуру со значением **PinX** «2» (то есть, что ПИН-код Поворот фигуры является 2 дюйма от левого края документа).</span><span class="sxs-lookup"><span data-stu-id="d6607-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="d6607-165">В следующем примере кода показана соответствующих разметка для назначения в формате документа XML.</span><span class="sxs-lookup"><span data-stu-id="d6607-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="d6607-166">Здесь элемент **PinX** — дочерний элемент **XForm** , который в свою очередь является дочерним элементом **фигуры** .</span><span class="sxs-lookup"><span data-stu-id="d6607-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="d6607-167">Эти модели пользовательского интерфейса таблицы свойств фигуры Visio, где ячейки **PinX** включен в разделе **Преобразование фигуры** фигуры.</span><span class="sxs-lookup"><span data-stu-id="d6607-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="d6607-168">В формате файла Visio 2013, всем ячейкам в ShapeSheet─ **PinX**, **LinePattern** **X** ячейка в строке **MoveTo** раздел **геометрии** , etc.─are, представленный одного типа XML-элемент, элемент **ячейки** .</span><span class="sxs-lookup"><span data-stu-id="d6607-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="d6607-169">Различные элементы **ячеек** individuated друг от друга, по значению атрибута их **N** .</span><span class="sxs-lookup"><span data-stu-id="d6607-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="d6607-170">Таким образом в приведенном выше примере данные, содержащиеся в ячейке **PinX** в таблице свойств фигуры хранится в файле VSDX, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="d6607-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="d6607-171">Элемент **ячейки** для **PinX** (а также другие отдельных, именованные ячейки, называется «одного ячеек» как **LinePattern** или **LockSelect**) является прямым потомком элемент **фигуры** .</span><span class="sxs-lookup"><span data-stu-id="d6607-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="d6607-172">Элемент не уникальный необходим для представления строку, содержащую ячейку **PinX** , как каждая фигура может иметь только один **PinX**.</span><span class="sxs-lookup"><span data-stu-id="d6607-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="d6607-173">Разделов, включая табличных данных, как в разделах **геометрии** ?</span><span class="sxs-lookup"><span data-stu-id="d6607-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="d6607-174">Для ячеек в этих разделах схему форматов файлов Visio 2013 использует **раздел** и elements─also **строки** с их атрибута **N** или **T** как показано below─to содержит данные.</span><span class="sxs-lookup"><span data-stu-id="d6607-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="d6607-175">Например фигуру из предыдущего примера может содержать данные в разделе **1 геометрии** , которая выглядит как следующий код в схеме XML-документа.</span><span class="sxs-lookup"><span data-stu-id="d6607-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="d6607-176">Тем не менее он выглядит как следующий код в файле Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d6607-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="d6607-177">Сценарии разработчика для работы с формат файлов Visio 2013</span><span class="sxs-lookup"><span data-stu-id="d6607-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="d6607-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="d6607-178"></span></span>

<span data-ttu-id="d6607-179">Как описано выше в формат файлов Visio 2013 использует несколько общепризнанным технологии, такие как ZIP-файлы и XML для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="d6607-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="d6607-180">Для работы с Visio 2013 рисования на уровне файлов, решения должны только для использования платформы .NET Framework пространства имен и классы, связанные с работой ZIP-файлы или XML, например, [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) или [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6607-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="d6607-181">Ключевые преимущества для разработчиков в формат файлов Visio 2013 является чтение и запись файлов Visio 2013 без автоматизации клиентского приложения Visio.</span><span class="sxs-lookup"><span data-stu-id="d6607-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="d6607-182">Некоторые сценарии, в которых может потребоваться разработчик, для работы с формат файлов Visio 2013 включают:</span><span class="sxs-lookup"><span data-stu-id="d6607-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="d6607-183">Проверка отдельных файлов Visio 2013 для определенных данных.</span><span class="sxs-lookup"><span data-stu-id="d6607-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="d6607-184">Избирательно могут читать один элемент из ZIP-контейнер без необходимости Извлеките файл целиком.</span><span class="sxs-lookup"><span data-stu-id="d6607-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="d6607-185">Обновление библиотек файлов Visio 2013 с помощью определенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="d6607-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="d6607-186">Программными средствами можно изменить логотипа в всех страниц фона в соответствии с новой фирменной настройки правила.</span><span class="sxs-lookup"><span data-stu-id="d6607-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="d6607-187">Создание приложения, использующие файлы Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d6607-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="d6607-188">Например можно построить это средство, которое считывает схему Visio рабочего процесса, а затем выполняет собственную бизнес-логику на основе этого рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="d6607-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="d6607-189">Помните о том, что так как эти решения используйте стандартные сборки .NET Framework, большинство решений, которые могут работать на клиентской машине также можно запустить на сервере!</span><span class="sxs-lookup"><span data-stu-id="d6607-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="d6607-190">Обзор возможностей в формат файлов Visio 2013 программными средствами</span><span class="sxs-lookup"><span data-stu-id="d6607-190">Exploring the Visio 2013 file format programmatically</span></span>
<span data-ttu-id="d6607-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="d6607-191"></span></span>

<span data-ttu-id="d6607-192">Наиболее базовой и основных задач для разработчики, работающие с формат файлов Visio 2013 открытия файла в виде пакета и получении доступа к отдельным части в пакете.</span><span class="sxs-lookup"><span data-stu-id="d6607-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="d6607-193">**System.IO.Packaging.Package** в WindowsBase.dll содержит множество классов, которые позволяют вам открывать и управлять пакеты и части.</span><span class="sxs-lookup"><span data-stu-id="d6607-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="d6607-194">В следующем образце кода можно узнать, как открыть файл vsdx (en), чтение списка части в пакете и получение сведений о каждой части.</span><span class="sxs-lookup"><span data-stu-id="d6607-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="d6607-195">Откройте файл vsdx (en) и Просмотр части документа</span><span class="sxs-lookup"><span data-stu-id="d6607-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="d6607-196">Откройте Visio 2013 и создайте новый документ.</span><span class="sxs-lookup"><span data-stu-id="d6607-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="d6607-197">Создайте новый документ и сохраните его на рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="d6607-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="d6607-198">Откройте Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="d6607-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="d6607-199">В меню **файл** выберите команду **Создать**и затем нажмите \*\* Project \*\*.</span><span class="sxs-lookup"><span data-stu-id="d6607-199">On the **File** menu, choose **New**, and then choose \*\* Project \*\*.</span></span>
    
5. <span data-ttu-id="d6607-200">В разделе **Visual C#** или **Visual Basic**разверните **Windows**и выберите **Консольное приложение**.</span><span class="sxs-lookup"><span data-stu-id="d6607-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="d6607-201">В поле **имя** введите «VisioFileExplorer».</span><span class="sxs-lookup"><span data-stu-id="d6607-201">In the **Name** box, type 'VisioFileExplorer'.</span></span> <span data-ttu-id="d6607-202">Открывает проект консольного приложения.</span><span class="sxs-lookup"><span data-stu-id="d6607-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="d6607-203">В **Обозревателе решений**щелкните правой кнопкой мыши **VisioFileExplorer**и выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="d6607-203">In the **Solution Explorer**, right-click **VisioFileExplorer**, and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="d6607-204">В диалоговом окне **Добавить ссылку** в разделе **сборки**разверните **Framework**и выберите **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="d6607-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="d6607-205">Вставьте следующий код в решение.</span><span class="sxs-lookup"><span data-stu-id="d6607-205">Paste the following code into the solution.</span></span>
    
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

10. <span data-ttu-id="d6607-206">Нажмите клавишу F5 для отладки решения.</span><span class="sxs-lookup"><span data-stu-id="d6607-206">Press F5 to debug the solution.</span></span> <span data-ttu-id="d6607-207">После завершения работы программы нажмите любую клавишу, чтобы выйти из.</span><span class="sxs-lookup"><span data-stu-id="d6607-207">When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6607-208">См. также</span><span class="sxs-lookup"><span data-stu-id="d6607-208">See also</span></span>
<span data-ttu-id="d6607-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="d6607-209"></span></span>

<span data-ttu-id="d6607-210">Дополнительные сведения о формате файла Visio 2013, Open Packaging Convention или как можно программно работать с файлами Office OpenXML 2013or Visio можно ознакомьтесь со следующими ресурсами:</span><span class="sxs-lookup"><span data-stu-id="d6607-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="d6607-211">Visio для разработчиков (en)</span><span class="sxs-lookup"><span data-stu-id="d6607-211">Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="d6607-212">[OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6607-212">[OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="d6607-213">Основные моменты спецификаций Open Packaging Conventions</span><span class="sxs-lookup"><span data-stu-id="d6607-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="d6607-214">Введение в форматы файлов Office (2007) Open XML</span><span class="sxs-lookup"><span data-stu-id="d6607-214">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

