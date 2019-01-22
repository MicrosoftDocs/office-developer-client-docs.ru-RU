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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699074"
---
# <a name="introduction-to-the-visio-file-format-vsdx"></a><span data-ttu-id="25e8d-103">Общие сведения о формате файлов Visio (VSDX)</span><span class="sxs-lookup"><span data-stu-id="25e8d-103">Introduction to the Visio file format (.vsdx)</span></span>

<span data-ttu-id="25e8d-104">Узнайте о новом формате файлов в Visio 2013, изучите некоторые высокоуровневые концепции программной работы с форматом файлов Visio 2013 и создайте простое консольное приложение, которое проверяет файл Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="25e8d-104">Learn about the new file format in Visio 2013, explore some high-level concepts for working with the Visio 2013 file format programmatically, and create a simple console application that examines a Visio 2013 file.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25e8d-105">**В этой статье** [Введение](#vis15_IntroVSDX_Intro) [Что из себя представляет формат файлов Visio 2013?](#vis15_IntroVSDX_What)</span><span class="sxs-lookup"><span data-stu-id="25e8d-105">**In this article**         [Introduction](#vis15_IntroVSDX_Intro)          [What is the Visio 2013 file format "under the hood"?](#vis15_IntroVSDX_What)</span></span>          <span data-ttu-id="25e8d-106">[Сценарии разработчика для работы с форматом файлов Visio 2013](#vis15_IntroVSDX_Scenarios) [Программное изучение формата файлов Visio 2013](#vis15_IntroVSDX_Explore) [Дополнительные ресурсы](#vis15_IntroVSDX_Resources)</span><span class="sxs-lookup"><span data-stu-id="25e8d-106">[Developer scenarios for working with the Visio 2013 file format](#vis15_IntroVSDX_Scenarios)          [Exploring the Visio 2013 file format programmatically](#vis15_IntroVSDX_Explore)          [Additional resources](#vis15_IntroVSDX_Resources)</span></span>||
   
## <a name="introduction"></a><span data-ttu-id="25e8d-107">Введение</span><span class="sxs-lookup"><span data-stu-id="25e8d-107">Introduction</span></span>
<span data-ttu-id="25e8d-108"><a name="vis15_IntroVSDX_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="25e8d-108"></span></span>

<span data-ttu-id="25e8d-109">Visio 2013 представляет новый формат файла (.vsdx) для Visio, который заменяет формат двоичного файла Visio (.vsd) и файл документа Visio в формате XML (.vdx).</span><span class="sxs-lookup"><span data-stu-id="25e8d-109">Visio 2013 introduces a new file format (.vsdx) for Visio that replaces the Visio binary file format (.vsd) and Visio XML Drawing file format (.vdx).</span></span> <span data-ttu-id="25e8d-110">Так как формат файла Visio 2013 основывается на соглашениях Open Packaging Conventions и XML, разработчики, имеющие представление об этих технологиях, могут быстро научиться программной работе с файлами Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="25e8d-110">Because the Visio 2013 file format is based upon Open Packaging Conventions and XML, developers who are familiar with these technologies can quickly learn how to work with Visio 2013 files programmatically.</span></span> <span data-ttu-id="25e8d-111">Разработчики, знакомые с файлами документов Visio в формате XML (.vdx) из предыдущих версий Visio, могут найти множество одинаковых XML-структур внутри частей файла в формате VSDX.</span><span class="sxs-lookup"><span data-stu-id="25e8d-111">Developers who are familiar with the Visio XML Drawing file format (.vdx) from previous versions of Visio can find many of the same XML structures within the parts of .vsdx file format.</span></span> <span data-ttu-id="25e8d-112">Взаимодействие с файлами Visio значительно повысилось, поскольку стороннее программное обеспечение может работать с файлами Visio на уровне формата файлов.</span><span class="sxs-lookup"><span data-stu-id="25e8d-112">Interoperability with Visio files is greatly increased since third-party software can manipulate Visio files at a file format level.</span></span> <span data-ttu-id="25e8d-113">Формат файлов Visio 2013 поддерживается в службах Visio в Microsoft SharePoint Server 2013, при этом использование промежуточного формата файлов для публикации в SharePoint Server не требуется.</span><span class="sxs-lookup"><span data-stu-id="25e8d-113">The Visio 2013 file format is supported on Visio Services in Microsoft SharePoint Server 2013, without the need of an "intermediary" file format for publishing to SharePoint Server.</span></span>
  
<span data-ttu-id="25e8d-114">Существует несколько типов (расширений) файлов, которые входят в формат файла Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="25e8d-114">There are several file types, by extension, that comprise the Visio 2013 file format.</span></span> <span data-ttu-id="25e8d-115">Эти расширения перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="25e8d-115">These extensions include:</span></span>
  
- <span data-ttu-id="25e8d-116">VSDX (документ Visio);</span><span class="sxs-lookup"><span data-stu-id="25e8d-116">.vsdx (Visio drawing)</span></span>
    
- <span data-ttu-id="25e8d-117">VSDM (документ Visio с поддержкой макросов);</span><span class="sxs-lookup"><span data-stu-id="25e8d-117">.vsdm (Visio macro-enabled drawing)</span></span>
    
- <span data-ttu-id="25e8d-118">VSSX (набор элементов Visio);</span><span class="sxs-lookup"><span data-stu-id="25e8d-118">.vssx (Visio stencil)</span></span>
    
- <span data-ttu-id="25e8d-119">VSSM (набор элементов Visio с поддержкой макросов);</span><span class="sxs-lookup"><span data-stu-id="25e8d-119">.vssm (Visio macro-enabled stencil)</span></span>
    
- <span data-ttu-id="25e8d-120">VSTX (шаблон Visio);</span><span class="sxs-lookup"><span data-stu-id="25e8d-120">.vstx (Visio template)</span></span>
    
- <span data-ttu-id="25e8d-121">VSTM (шаблон Visio с поддержкой макросов).</span><span class="sxs-lookup"><span data-stu-id="25e8d-121">.vstm (Visio macro-enabled template)</span></span>
    
> [!NOTE]
> <span data-ttu-id="25e8d-122">Макросы VBA можно хранить только в файлах с поддержкой макросов (VSDM, VSSM, VSTM).</span><span class="sxs-lookup"><span data-stu-id="25e8d-122">Only the macro-enabled files (.vsdm, .vssm, .vstm) can store VBA macros.</span></span> <span data-ttu-id="25e8d-123">Хранение макросов в файлах с расширением VSDX, VSSX или VSTX невозможно.</span><span class="sxs-lookup"><span data-stu-id="25e8d-123">You cannot store macros in files with a .vsdx, .vssx, or .vstx extension.</span></span> 
  
## <a name="what-is-the-visio-2013-file-format-under-the-hood"></a><span data-ttu-id="25e8d-124">Что из себя представляет формат файлов Visio 2013?</span><span class="sxs-lookup"><span data-stu-id="25e8d-124">What is the Visio 2013 file format "under the hood"?</span></span>
<span data-ttu-id="25e8d-125"><a name="vis15_IntroVSDX_What"> </a></span><span class="sxs-lookup"><span data-stu-id="25e8d-125"></span></span>

<span data-ttu-id="25e8d-126">Формат файлов Visio 2013 использует соглашения Open Packing Conventions (OPC), которые определяют структурированные средства для хранения данных приложения вместе со связанными ресурсами с помощью контейнера, например ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="25e8d-126">The Visio 2013 file format uses the Open Packing Conventions (OPC), which defines a structured means to store application data together with related resources using a container of some sort─for example, a ZIP file.</span></span> <span data-ttu-id="25e8d-127">На базовом уровне файл Visio 2013 действительно представляет собой ZIP-контейнер, содержащий файлы других типов.</span><span class="sxs-lookup"><span data-stu-id="25e8d-127">At a basic level, a Visio 2013 file is really a ZIP container that contains other types of files.</span></span> <span data-ttu-id="25e8d-128">Фактически вы можете сохранить чертеж в Visio 2013 в виде VSDX-файла, в проводнике переименовать расширение на "\*.zip", а затем открыть этот файл как папку, чтобы просмотреть его содержимое.</span><span class="sxs-lookup"><span data-stu-id="25e8d-128">In fact, you can save a drawing in Visio 2013 as a .vsdx file, rename the file extension to "\*.zip" in Windows Explorer, and then open the file like a folder to see the contents inside.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="25e8d-129">В этой статье приведен краткий обзор Open Packaging Conventions.</span><span class="sxs-lookup"><span data-stu-id="25e8d-129">This article contains only a brief overview of the Open Packaging Conventions.</span></span> <span data-ttu-id="25e8d-130">Более подробное описание этих соглашений можно найти в других статьях. > Дополнительные сведения непосредственно об Open Packaging Conventions см. в статье [OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx).</span><span class="sxs-lookup"><span data-stu-id="25e8d-130">You can find more detailed coverage of the conventions in other articles: >  For more information about the Open Packaging Conventions themselves, see [OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span> <span data-ttu-id="25e8d-131">> Дополнительные сведения о соглашениях Open Packaging Conventions и их использовании в файлах Microsoft Office см. в статьях [Основные понятия Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) и [Общие сведения о форматах файлов Office (2007) Open XML](https://msdn.microsoft.com/library/aa338205.aspx).</span><span class="sxs-lookup"><span data-stu-id="25e8d-131">>  For more information about the Open Packaging Conventions and their use in Microsoft Office files, see [Essentials of the Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) and [Introducing the Office (2007) Open XML File Formats](https://msdn.microsoft.com/library/aa338205.aspx).</span></span> 
  
### <a name="packages-and-package-parts"></a><span data-ttu-id="25e8d-132">Пакеты и части пакетов</span><span class="sxs-lookup"><span data-stu-id="25e8d-132">Packages and Document Parts</span></span>

<span data-ttu-id="25e8d-133">Как уже говорилось ранее, файлы Visio 2013 являются ZIP-контейнерами или "пакетами", в которых находятся другие файлы (называемые "частями пакета").</span><span class="sxs-lookup"><span data-stu-id="25e8d-133">As started earlier, Visio 2013 files are ZIP containers or "packages" that hold other files (called "package parts") within them.</span></span> <span data-ttu-id="25e8d-134">Часть пакета может быть XML-файлом, изображением или даже решением VBA.</span><span class="sxs-lookup"><span data-stu-id="25e8d-134">A package part can be an XML file, an image, even a VBA solution.</span></span> <span data-ttu-id="25e8d-135">Части, находящиеся в пакете, можно разделить на две большие категории: "части документов" и "части отношений".</span><span class="sxs-lookup"><span data-stu-id="25e8d-135">The parts within the package can be further divided into two broad categories, "document parts" and "relationship parts."</span></span> <span data-ttu-id="25e8d-136">Части документов содержат фактическое содержимое и метаданные файла Visio, такие как имя файла, первая страница и все содержащиеся на ней фигуры, а также соединения данных для этих фигур.</span><span class="sxs-lookup"><span data-stu-id="25e8d-136">The document parts contain the actual content and metadata of the Visio file, like the name of the file, the first page and all of the shapes that it contains, and even the data connections for the shapes.</span></span> <span data-ttu-id="25e8d-137">Изображения и текстовые файлы в пакете считаются частями документа.</span><span class="sxs-lookup"><span data-stu-id="25e8d-137">Images and text files within the package are considered document parts.</span></span> <span data-ttu-id="25e8d-138">Более подробное описание частей отношений будет приведено далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="25e8d-138">Relationship parts are described in more detail later in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="25e8d-139">Если открыть файл Visio 2013 с помощью служебной программы ZIP, скорее всего вы увидите, что в этом ZIP-пакете находится несколько папок.</span><span class="sxs-lookup"><span data-stu-id="25e8d-139">If you open a Visio 2013 file using a ZIP utility, you can probably see several folders contained inside of the ZIP package.</span></span> <span data-ttu-id="25e8d-140">Вы даже сможете управлять этими подадресами как папками, используя служебную программу ZIP.</span><span class="sxs-lookup"><span data-stu-id="25e8d-140">You can even manipulate these sub-addresses like folders using a ZIP utility.</span></span> <span data-ttu-id="25e8d-141">Однако эти "папки" являются подадресами в пакете ZIP, а не реальными папками.</span><span class="sxs-lookup"><span data-stu-id="25e8d-141">However, these "folders" represent sub-addresses within the ZIP package, not actual folders.</span></span> <span data-ttu-id="25e8d-142">Вы не сможете использовать программные эквиваленты папок, чтобы работать с этими подадресами в вашем решении.</span><span class="sxs-lookup"><span data-stu-id="25e8d-142">You cannot use the programmatic equivalents of folders to work with these sub-addresses in your solution.</span></span> 
  
<span data-ttu-id="25e8d-143">Части пакета (как части документов, так и части отношений) также имеют связанные типы контента.</span><span class="sxs-lookup"><span data-stu-id="25e8d-143">Package parts─both document parts and relationship parts─also have associated content types.</span></span> <span data-ttu-id="25e8d-144">Этими типами контента являются строки, которые определяют тип мультимедиа MIME.</span><span class="sxs-lookup"><span data-stu-id="25e8d-144">These content types are strings that define a MIME media type.</span></span> <span data-ttu-id="25e8d-145">Эти типы контента устанавливают и определяют MIME-типы, которые могут содержаться в файле.</span><span class="sxs-lookup"><span data-stu-id="25e8d-145">These content types specify and scope the kind of MIME types that can be contained in the file.</span></span>
  
### <a name="relationships"></a><span data-ttu-id="25e8d-146">Отношения</span><span class="sxs-lookup"><span data-stu-id="25e8d-146">Relationships</span></span>

<span data-ttu-id="25e8d-147">Части отношений (оканчивающиеся расширением "\*.rels" и хранимые в папке "_rels") описывают, каким образом эти части в пакете связаны друг с другом, и определяют структуру файла.</span><span class="sxs-lookup"><span data-stu-id="25e8d-147">The relationship parts (which end with the extension "\*.rels" and are stored in a "_rels" folder) describe how the parts within the package relate to each other and provide the structure of the file.</span></span> <span data-ttu-id="25e8d-148">Отдельный XML-документ использует иерархическое ("родитель — потомок") отношение элементов для определения связи объектов друг с другом.</span><span class="sxs-lookup"><span data-stu-id="25e8d-148">A standalone XML document uses the parent/child relationship of elements to determine the relationship of entities to each other.</span></span> <span data-ttu-id="25e8d-149">Другие файлы могут использовать другую иерархию или структуру папок с файлами для описания взаимодействия содержимого в файле.</span><span class="sxs-lookup"><span data-stu-id="25e8d-149">Other files may use other hierarchies or file folder structure to describe the interaction of content in the file.</span></span> <span data-ttu-id="25e8d-150">В формате файлов Visio 2013 допустимым файлом Visio является пакет, содержащий правильный набор частей и отношения между частями.</span><span class="sxs-lookup"><span data-stu-id="25e8d-150">For the Visio 2013 file format, the package is a valid Visio file if it contains the correct set of parts and the package contains the relationships between the parts.</span></span> 
  
<span data-ttu-id="25e8d-151">Части отношений — это XML-документы, описывающие отношения между различными частями документа в пакете.</span><span class="sxs-lookup"><span data-stu-id="25e8d-151">Relationship parts are XML documents that describe the relationships between different document parts within the package.</span></span> <span data-ttu-id="25e8d-152">Они определяют связь между двумя элементами: указанным источником (который задается именем и расположением файла отношений) и указанной частью целевого документа.</span><span class="sxs-lookup"><span data-stu-id="25e8d-152">They define an association between two items: a specified source (defined by the name and location of the relationship file) and a specified target document part.</span></span> <span data-ttu-id="25e8d-153">Например, части отношений используются для описания того, какие мастеры форм связаны с файлом, как страницы связаны с файлом и друг с другом или как изображения и объекты связаны с конкретной страницей.</span><span class="sxs-lookup"><span data-stu-id="25e8d-153">For example, relationship parts are used to describe which shape masters are associated with the file, how pages relate to the file and to each other, or how images and objects relate to a specific page.</span></span> 
  
### <a name="similarities-and-differences-with-visio-vdx-schema"></a><span data-ttu-id="25e8d-154">Сходства и различия со схемой Visio VDX</span><span class="sxs-lookup"><span data-stu-id="25e8d-154">Similarities and differences with Visio VDX schema</span></span>

<span data-ttu-id="25e8d-155">Как уже было сказано, предыдущие версии Visio также имели формат файлов на основе XML, т. е. документ Visio в формате XML (VDX).</span><span class="sxs-lookup"><span data-stu-id="25e8d-155">As mentioned, past versions of Visio also included an XML-based file format, the Visio XML Drawing Format or .vdx.</span></span> <span data-ttu-id="25e8d-156">(В предыдущих версиях Visio схема, используемая для документов Visio в формате XML, называлась DatadiagramML.) Некоторые фрагменты схемы Visio XML не изменились.</span><span class="sxs-lookup"><span data-stu-id="25e8d-156">(In previous versions of Visio, the schema used for the Visio XML Drawing Format is called DatadiagramML.) Some pieces from the Visio XML schema have stayed the same between the two file formats.</span></span> <span data-ttu-id="25e8d-157">Например, элемент **Windows** и его дочерние элементы остались неизменными, за исключением того, что теперь элемент **Windows** является корневым элементом документа XML (window.xml).</span><span class="sxs-lookup"><span data-stu-id="25e8d-157">For example, the **Windows** element and its children remain unchanged─with the exception that the **Windows** element is now a root element of an XML document (window.xml).</span></span> 
  
<span data-ttu-id="25e8d-158">Самое большое различие между документом в формате XML и форматом файлов Visio 2013 заключается в упаковке.</span><span class="sxs-lookup"><span data-stu-id="25e8d-158">The largest difference between the XML Drawing Format and the Visio 2013 file format is the packaging.</span></span> <span data-ttu-id="25e8d-159">С файлом документа в формате XML можно работать как с обычным автономным XML-файлом; файл в формате Visio 2013 необходимо обрабатывать как пакет.</span><span class="sxs-lookup"><span data-stu-id="25e8d-159">An XML Drawing Format file could be manipulated like a normal stand-alone XML; the Visio 2013 file format must be manipulated as a package.</span></span> <span data-ttu-id="25e8d-160">Для удобства использования в Visio 2013 код XML разделен на две части.</span><span class="sxs-lookup"><span data-stu-id="25e8d-160">In the Visio 2013, the XML has been divided up into parts for easier consumption.</span></span> <span data-ttu-id="25e8d-161">Еще одно значимое изменение состоит в том, что формат файлов Visio 2013 хранит все свойства документа в частях документа, которые описаны стандартом OPC (app.xml, core.xml, custom.xml).</span><span class="sxs-lookup"><span data-stu-id="25e8d-161">Another noticeable change is that the Visio 2013 file format stores all document properties in document parts described by the OPC standard (app.xml, core.xml, custom.xml).</span></span>
  
<span data-ttu-id="25e8d-162">Однако есть одно существенное изменение, которое должны учитывать все разработчики Visio: появление элементов **Cell**, **Row** и **Section**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-162">However, there is one significant change that all Visio developers must be aware of: the introduction of the **Cell**, **Row**, and **Section** elements.</span></span> <span data-ttu-id="25e8d-163">В схеме файла документа в формате XML отдельные строки и ячейки в ShapeSheet представлены именованными элементами.</span><span class="sxs-lookup"><span data-stu-id="25e8d-163">In the XML Drawing File Format schema, individual rows and cells in the ShapeSheet are represented by named elements.</span></span> <span data-ttu-id="25e8d-164">Предположим, что у вас есть одностраничный документ, содержащий фигуру, элемент **PinX** которой имеет значение "2" (это означает, что ось вращения фигуры находится в 2 дюймах от левого края чертежа).</span><span class="sxs-lookup"><span data-stu-id="25e8d-164">For example, imagine that you have a document with a single page that contains a shape with a **PinX** value of "2" (meaning that the rotation pin of the shape is 2 inches from the left edge of the drawing).</span></span> <span data-ttu-id="25e8d-165">Соответствующая разметка для этого параметра в файле документа в формате XML представлена в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="25e8d-165">The relevant markup for that setting in the XML Drawing File Format is shown in the following code.</span></span> 
  
```XML
<Shape ID="1" TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape">
    <XForm> 
        <PinX Unit="IN">2</Pinx>
        <!--- Other cells in the Shape Transform section -->
    </XForm>
    <!--- Other rows and cells in the ShapeSheet -->
</Shape>

```

<span data-ttu-id="25e8d-166">Здесь элемент **PinX** является дочерним по отношению к элементу **XForm**, который, в свою очередь, является дочерним по отношению к элементу **Shape**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-166">Here, the **PinX** element is a child of the **XForm** element, which is in turn a child of the **Shape** element.</span></span> <span data-ttu-id="25e8d-167">Этот код строит модель пользовательского интерфейса Visio ShapeSheet, где ячейка **PinX** включена в раздел **Shape Transform** фигуры.</span><span class="sxs-lookup"><span data-stu-id="25e8d-167">This models the Visio ShapeSheet UI, where the **PinX** cell is included in the **Shape Transform** section of a shape.</span></span> 
  
<span data-ttu-id="25e8d-168">В формате файлов Visio 2013 все ячейки в ShapeSheet (**PinX**, **LinePattern**, ячейка **X** в строке **MoveTo** из раздела **Geometry** и т. д.) представлены одним типом XML-элемента — элементом **Cell**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-168">In the Visio 2013 file format, all cells in the ShapeSheet─ **PinX**, **LinePattern**, an **X** cell in a **MoveTo** row in a **Geometry** section, etc.─are represented by one type of XML element, the **Cell** element.</span></span> <span data-ttu-id="25e8d-169">Различные элементы **Cell** отличаются друг от друга значением атрибута **N**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-169">Different **Cell** elements are individuated from each other by the value of their **N** attribute.</span></span> <span data-ttu-id="25e8d-170">Таким образом, данные, содержащиеся в ячейке **PinX** в ShapeSheet в приведенном выше примере, хранятся в VSDX-файле, как представлено в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="25e8d-170">Thus, in the example from above, the data contained in the **PinX** cell in the ShapeSheet is stored in a VSDX file as shown in the following code.</span></span> 
  
```XML
<Shape TextStyle="3" FillStyle="3" LineStyle="3" Type="Shape" ID="1">
    <Cell N="PinX" U="IN" V="2"/>
    <!--- Other cells in the ShapeSheet --> 
</Shape>
```

<span data-ttu-id="25e8d-171">Элемент **Cell** для **PinX** (а также другие отдельные именованные ячейки, называемые "singleton-ячейками", например **LinePattern** или **LockSelect**) является прямым потомком элемента **Shape**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-171">The **Cell** element for **PinX** (as well as other individual, named cells called "singleton cells" like **LinePattern** or **LockSelect**) is a direct child of the **Shape** element.</span></span> <span data-ttu-id="25e8d-172">Для представления строки, содержащей ячейку **PinX**, уникальный элемент не требуется, поскольку каждая фигура может иметь только один элемент **PinX**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-172">No unique element is needed to represent the row that contains the **PinX** cell, as each shape can only have one **PinX**.</span></span>
  
<span data-ttu-id="25e8d-173">Что насчет разделов, которые содержат табличные данные, например раздел **Geometry**?</span><span class="sxs-lookup"><span data-stu-id="25e8d-173">What about sections that include tabular data, like **Geometry** sections?</span></span> <span data-ttu-id="25e8d-174">В ячейках из этих разделов для хранения данных схема формата файлов Visio 2013 использует элементы **Section** и **Row**, которые различаются атрибутами **N** или **T**, как показано ниже</span><span class="sxs-lookup"><span data-stu-id="25e8d-174">For the cells in those sections, the Visio 2013 file format schema uses **Section** and **Row** elements─also distinguished by their **N** attribute or **T** attribute as shown below─to contain the data.</span></span> <span data-ttu-id="25e8d-175">Например, фигура из предыдущего примера может содержать данные в разделе **Geometry 1**, код которого в схеме документа в формате XML выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="25e8d-175">For example, the same shape from the previous example might contain data in the **Geometry 1** section that looks like the following code in the XML Drawing schema.</span></span> 
  
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

<span data-ttu-id="25e8d-176">Но в файле Visio 2013 код выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="25e8d-176">However, it looks like the following code in the Visio 2013 file.</span></span>
  
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

## <a name="developer-scenarios-for-working-with-the-visio-2013-file-format"></a><span data-ttu-id="25e8d-177">Сценарии разработчика для работы с форматом файлов Visio 2013</span><span class="sxs-lookup"><span data-stu-id="25e8d-177">Developer scenarios for working with the Visio 2013 file format</span></span>
<span data-ttu-id="25e8d-178"><a name="vis15_IntroVSDX_Scenarios"> </a></span><span class="sxs-lookup"><span data-stu-id="25e8d-178"></span></span>

<span data-ttu-id="25e8d-179">Как было пояснено выше, формат файлов Visio 2013 использует для хранения данных несколько широко известных технологий, таких как ZIP-файлы и XML.</span><span class="sxs-lookup"><span data-stu-id="25e8d-179">As explained above, the Visio 2013 file format leverages several well-understood technologies like ZIP files and XML to store data.</span></span> <span data-ttu-id="25e8d-180">Для обработки документов Visio 2013 на уровне файлов решение должно использовать только пространства имен и классы .NET Framework, которые связаны с работой с файлами ZIP или XML, например [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) или [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="25e8d-180">To manipulate a Visio 2013 drawing at the file level, a solution need only to use the .NET Framework namespaces and classes associated with working with ZIP files or XML, like [System.IO.Packaging](https://msdn.microsoft.com/library/system.io.packaging%28v=vs.110%29.aspx) or [System.Xml](https://msdn.microsoft.com/library/system.xml%28v=vs.110%29.aspx).</span></span>
  
<span data-ttu-id="25e8d-181">Ключевое преимущество для разработчиков формата файлов Visio 2013 заключается в том, что чтение и запись файлов Visio 2013 можно выполнять без автоматизации клиентского приложения Visio.</span><span class="sxs-lookup"><span data-stu-id="25e8d-181">The key benefit to developers of the Visio 2013 file format is that you can read and write to Visio 2013 files without automating the Visio client application.</span></span> <span data-ttu-id="25e8d-182">Вот некоторые сценарии, которыми может воспользоваться разработчик при работе с форматом файлов Visio 2013:</span><span class="sxs-lookup"><span data-stu-id="25e8d-182">Some scenarios that you might consider as a developer for working with Visio 2013 file format include:</span></span>
  
- <span data-ttu-id="25e8d-183">Проверка отдельных файлов Visio 2013 на наличие определенных данных.</span><span class="sxs-lookup"><span data-stu-id="25e8d-183">Checking individual Visio 2013 files for specific data.</span></span> <span data-ttu-id="25e8d-184">Вы можете выборочно прочитать один элемент из ZIP-контейнера, не извлекая содержимое всего файла.</span><span class="sxs-lookup"><span data-stu-id="25e8d-184">You can selectively read one item out of the ZIP container without having to extract the whole file.</span></span>
    
- <span data-ttu-id="25e8d-185">Обновление библиотек файлов Visio 2013 с определенным содержимым.</span><span class="sxs-lookup"><span data-stu-id="25e8d-185">Updating libraries of Visio 2013 files with specific content.</span></span> <span data-ttu-id="25e8d-186">Вы можете программно изменить логотип на всех фоновых страницах, чтобы отразить новые рекомендации по фирменной символике.</span><span class="sxs-lookup"><span data-stu-id="25e8d-186">You can programmatically change the logo in all of the background pages to reflect new branding guidelines.</span></span>
    
- <span data-ttu-id="25e8d-187">Создание приложений, использующих файлы Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="25e8d-187">Creating applications that consume Visio 2013 files.</span></span> <span data-ttu-id="25e8d-188">Например, вы можете создать инструмент, который считывает схему рабочего процесса Visio, а затем на основе этого рабочего процесса выполняет собственную бизнес-логику.</span><span class="sxs-lookup"><span data-stu-id="25e8d-188">For example, you can build a tool that reads a Visio workflow diagram and then executes its own business logic based upon that workflow.</span></span>
    
<span data-ttu-id="25e8d-189">Помните, что поскольку в этих решениях используются стандартные сборки .NET Framework, большинство решений, которые могут быть запущены на клиентском компьютере, также могут выполняться на сервере!</span><span class="sxs-lookup"><span data-stu-id="25e8d-189">Be aware that because these solutions use standard .NET Framework assemblies, most solutions that can be run on a client machine can also be run on a server!</span></span>
  
## <a name="exploring-the-visio-2013-file-format-programmatically"></a><span data-ttu-id="25e8d-190">Программное изучение формата файлов Visio 2013</span><span class="sxs-lookup"><span data-stu-id="25e8d-190">Manipulate the Visio file format programmatically</span></span>
<span data-ttu-id="25e8d-191"><a name="vis15_IntroVSDX_Explore"> </a></span><span class="sxs-lookup"><span data-stu-id="25e8d-191"></span></span>

<span data-ttu-id="25e8d-192">Основная и фундаментальная задача любого разработчика, работающего с форматом файлов Visio 2013, заключается в том, чтобы открыть файл как пакет, а затем получить доступ к отдельным частям в пакете.</span><span class="sxs-lookup"><span data-stu-id="25e8d-192">The most basic and fundamental task for any developer working with the Visio 2013 file format is opening the file as a package and then accessing individual parts within the package.</span></span> <span data-ttu-id="25e8d-193">Класс **System.IO.Packaging.Package** в WindowsBase.dll содержит множество классов, которые позволяют открывать пакеты и части и работать с ними.</span><span class="sxs-lookup"><span data-stu-id="25e8d-193">The **System.IO.Packaging.Package** in the WindowsBase.dll contains many classes that enable you to open and manipulate packages and parts.</span></span> 
  
<span data-ttu-id="25e8d-194">В следующем примере кода вы увидите, как открыть VSDX-файл, прочитать список частей в пакете и получить информацию о каждой части.</span><span class="sxs-lookup"><span data-stu-id="25e8d-194">In the following code sample, you can see how to open a .vsdx file, read the list of parts in the package, and get information about each part.</span></span>
  
### <a name="to-open-a-vsdx-file-and-view-the-document-parts"></a><span data-ttu-id="25e8d-195">Открытие VSDX-файла и просмотр частей документа</span><span class="sxs-lookup"><span data-stu-id="25e8d-195">To open a .vsdx file and view the document parts</span></span>

1. <span data-ttu-id="25e8d-196">Откройте Visio 2013 и создайте новый документ.</span><span class="sxs-lookup"><span data-stu-id="25e8d-196">Open Visio 2013 and create a new document.</span></span>
    
2. <span data-ttu-id="25e8d-197">Создайте новый документ и сохраните его на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="25e8d-197">Create a new document and save it to the Desktop.</span></span>
    
3. <span data-ttu-id="25e8d-198">Откройте Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="25e8d-198">Open Visual Studio 2012.</span></span>
    
4. <span data-ttu-id="25e8d-199">В меню **Файл** выберите команду **Создать**, а затем пункт **Проект**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-199">On the **File** menu, point to **New**, and then choose Project.</span></span>
    
5. <span data-ttu-id="25e8d-200">В разделе **Visual C#** или **Visual Basic** разверните узел **Windows** и выберите пункт **Консольное приложение**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-200">Under **Visual C#** or **Visual Basic**, expand **Windows**, and then select **Console Application**.</span></span>
    
6. <span data-ttu-id="25e8d-201">В поле **Имя** введите "VisioFileExplorer".</span><span class="sxs-lookup"><span data-stu-id="25e8d-201">In the Name box, type SampleApplication.</span></span> <span data-ttu-id="25e8d-202">Откроется проект консольного приложения.</span><span class="sxs-lookup"><span data-stu-id="25e8d-202">The Console Application project opens.</span></span> 
    
7. <span data-ttu-id="25e8d-203">В **обозревателей решений** щелкните правой кнопкой мыши пункт **VisioFileExplorer**, а затем выберите команду **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-203">In Solution Explorer, right-click **References** and then click **Add Reference**.</span></span> 
    
8. <span data-ttu-id="25e8d-204">В диалоговом окне **Добавление ссылки** в разделе **Сборки** разверните узел **Платформа**, а затем выберите пункт **WindowsBase**.</span><span class="sxs-lookup"><span data-stu-id="25e8d-204">In the **Add Reference** dialog box, under **Assemblies**, expand **Framework**, and then choose **WindowsBase**.</span></span>
    
9. <span data-ttu-id="25e8d-205">Вставьте в решение следующий код.</span><span class="sxs-lookup"><span data-stu-id="25e8d-205">Paste the following code into the file.</span></span>
    
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

10. <span data-ttu-id="25e8d-206">Нажмите клавишу F5, чтобы отладить решение.</span><span class="sxs-lookup"><span data-stu-id="25e8d-206">Press F5 to debug the add-in.</span></span> <span data-ttu-id="25e8d-207">По завершении работы программы выйдите из нее, нажав любую клавишу.</span><span class="sxs-lookup"><span data-stu-id="25e8d-207">When the program has completed running, press any key to exit.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25e8d-208">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="25e8d-208">See also</span></span>
<span data-ttu-id="25e8d-209"><a name="vis15_IntroVSDX_Resources"> </a></span><span class="sxs-lookup"><span data-stu-id="25e8d-209"></span></span>

<span data-ttu-id="25e8d-210">Дополнительные сведения о формате файлов Visio 2013, соглашении Open Packaging Convention и программной работе с файлами Visio 2013 или Office OpenXML см. в следующих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="25e8d-210">For more information about the Visio 2013 file format, the Open Packaging Convention, or how to work with Visio 2013or Office OpenXML files programmatically, see the following resources:</span></span>
  
- [<span data-ttu-id="25e8d-211">Visio для разработчиков</span><span class="sxs-lookup"><span data-stu-id="25e8d-211">New in Visio for developers</span></span>](https://msdn.microsoft.com/office/aa905478.aspx)
    
- <span data-ttu-id="25e8d-212">[OPC: новый стандарт упаковки данных](https://msdn.microsoft.com/magazine/cc163372.aspx)</span><span class="sxs-lookup"><span data-stu-id="25e8d-212">[OPC: A New Standard for Packaging Your Data](https://msdn.microsoft.com/magazine/cc163372.aspx).</span></span>
    
- [<span data-ttu-id="25e8d-213">Основные понятия Open Packaging Conventions</span><span class="sxs-lookup"><span data-stu-id="25e8d-213">Essentials of the Open Packaging Conventions</span></span>](https://msdn.microsoft.com/library/ee361919.aspx)
    
- [<span data-ttu-id="25e8d-214">Общие сведения о форматах файлов Office (2007) Open XML</span><span class="sxs-lookup"><span data-stu-id="25e8d-214">Introducing the Office (2007) Open XML File Formats</span></span>](https://msdn.microsoft.com/library/aa338205.aspx)
    

