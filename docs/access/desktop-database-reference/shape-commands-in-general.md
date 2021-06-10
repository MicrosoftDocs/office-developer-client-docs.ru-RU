---
title: Общие сведения о командах Shape
TOCTitle: Shape commands in general
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 399836158084f07b30b06a9fb099da74527d0cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308654"
---
# <a name="shape-commands-in-general"></a><span data-ttu-id="866ab-102">Общие сведения о командах Shape</span><span class="sxs-lookup"><span data-stu-id="866ab-102">Shape commands in general</span></span>

<span data-ttu-id="866ab-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="866ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="866ab-104">Формирование данных определяет столбцы фигурного набора **записей,** связи между сущностями, представленными столбцами, и способ заполнения данных **в Наборе** записей.</span><span class="sxs-lookup"><span data-stu-id="866ab-104">Data shaping defines the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="866ab-105">Сформированный **набор записей** может состоять из следующих типов столбцов.</span><span class="sxs-lookup"><span data-stu-id="866ab-105">A shaped **Recordset** may consist of the following types of columns.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="866ab-106">Тип столбца</span><span class="sxs-lookup"><span data-stu-id="866ab-106">Column type</span></span></p></th>
<th><p><span data-ttu-id="866ab-107">Описание</span><span class="sxs-lookup"><span data-stu-id="866ab-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="866ab-108">data</span><span class="sxs-lookup"><span data-stu-id="866ab-108">data</span></span></p></td>
<td><p><span data-ttu-id="866ab-109">Поля из <strong>recordset,</strong> возвращаемой командой запроса поставщику данных, таблице или ранее сформированным <strong>Набору записей.</strong></span><span class="sxs-lookup"><span data-stu-id="866ab-109">Fields from a <strong>Recordset</strong> returned by a query command to a data provider, table, or previously shaped <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="866ab-110">глава</span><span class="sxs-lookup"><span data-stu-id="866ab-110">chapter</span></span></p></td>
<td><p><span data-ttu-id="866ab-111">Ссылка на другой <strong>Набор записей</strong>, называемый <em>главой</em>.</span><span class="sxs-lookup"><span data-stu-id="866ab-111">A reference to another <strong>Recordset</strong>, called a <em>chapter</em>.</span></span> <span data-ttu-id="866ab-112">Столбцы глав делают возможным <em></em> определение отношения между <em></em> родителем и ребенком, в <em></em> котором родитель — набор записей, содержащий столбец главы, а ребенок — набор <strong>записей,</strong> представленный главой. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="866ab-112">Chapter columns make it possible to define a <em>parent-child</em> relationship where the <em>parent</em> is the <strong>Recordset</strong> containing the chapter column and the <em>child</em> is the <strong>Recordset</strong> represented by the chapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="866ab-113">сводка</span><span class="sxs-lookup"><span data-stu-id="866ab-113">aggregate</span></span></p></td>
<td><p><span data-ttu-id="866ab-114">Значение столбца выводится путем выполнения <em></em> совокупной функции во всех строках или столбце всех строк детского <strong>recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="866ab-114">The value of the column is derived by executing an <em>aggregate function</em> on all the rows or a column of all the rows of a child <strong>Recordset</strong>.</span></span> <span data-ttu-id="866ab-115">(См. агрегированные функции в следующей статье, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Агрегированные функции, функция CALC и новое ключевое</a>слово .)</span><span class="sxs-lookup"><span data-stu-id="866ab-115">(See Aggregate Functions in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="866ab-116">вычисляемая экспрессия</span><span class="sxs-lookup"><span data-stu-id="866ab-116">calculated expression</span></span></p></td>
<td><p><span data-ttu-id="866ab-117">Значение столбца выводится путем вычисления выражения Visual Basic для приложений на столбцах в том же ряду <strong>Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="866ab-117">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="866ab-118">Выражение является аргументом для функции CALC.</span><span class="sxs-lookup"><span data-stu-id="866ab-118">The expression is the argument to the CALC function.</span></span> <span data-ttu-id="866ab-119">(См. вычисляемую экспрессию в следующей статье, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Агрегированные функции, функции CALC,</a> а также новое ключевое слово и <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений Функции.)</a></span><span class="sxs-lookup"><span data-stu-id="866ab-119">(See Calculated Expression in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a> and in <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications Functions</a>.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="866ab-120">Новые функции</span><span class="sxs-lookup"><span data-stu-id="866ab-120">new</span></span></p></td>
<td><p><span data-ttu-id="866ab-121">Пустые, сфабрикованные поля, которые могут быть заполнены данными в более позднее время.</span><span class="sxs-lookup"><span data-stu-id="866ab-121">Empty, fabricated fields, which may be populated with data at a later time.</span></span> <span data-ttu-id="866ab-122">Столбец определяется с помощью ключевого слова NEW.</span><span class="sxs-lookup"><span data-stu-id="866ab-122">The column is defined with the NEW keyword.</span></span> <span data-ttu-id="866ab-123">(См. новое ключевое слово в следующей статье, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Агрегированные функции, функция CALC и новое ключевое</a>слово .)</span><span class="sxs-lookup"><span data-stu-id="866ab-123">(See NEW keyword in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="866ab-124">Команда фигуры может содержать пункт, указывающий команду запроса основному поставщику данных, который возвращает объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="866ab-124">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object.</span></span> <span data-ttu-id="866ab-125">Синтаксис запроса зависит от требований поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="866ab-125">The query's syntax depends on the requirements of the underlying data provider.</span></span> <span data-ttu-id="866ab-126">Обычно это язык SQL (SQL), хотя ADO не требует использования какого-либо конкретного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="866ab-126">This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span></span>

<span data-ttu-id="866ab-127">Вы можете использовать пункт SQL JOIN, чтобы связать две таблицы; однако иерархический **набор записей может** представлять информацию более эффективно.</span><span class="sxs-lookup"><span data-stu-id="866ab-127">You could use a SQL JOIN clause to relate two tables; however, a hierarchical **Recordset** may represent the information more efficiently.</span></span> <span data-ttu-id="866ab-128">Каждая строка **наборов записей,** созданных join, повторяет сведения из одной из таблиц.</span><span class="sxs-lookup"><span data-stu-id="866ab-128">Each row of a **Recordset** created by a JOIN repeats information redundantly from one of the tables.</span></span> <span data-ttu-id="866ab-129">Иерархический **набор записей имеет** только один родительский **набор записей** для каждого из нескольких объектов **recordset** для детей.</span><span class="sxs-lookup"><span data-stu-id="866ab-129">A hierarchical **Recordset** has only one parent **Recordset** for each of multiple child **Recordset** objects.</span></span>

<span data-ttu-id="866ab-130">Команды формы могут быть выданы **объектами Recordset** или путем установки свойства [CommandText](commandtext-property-ado.md) объекта [Command](command-object-ado.md) и вызова метода [Execute.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)</span><span class="sxs-lookup"><span data-stu-id="866ab-130">Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

<span data-ttu-id="866ab-131">Команды формы можно вложены.</span><span class="sxs-lookup"><span data-stu-id="866ab-131">Shape commands can be nested.</span></span> <span data-ttu-id="866ab-132">То есть *родительская или* *детская* команда может сама быть другой командой фигуры.</span><span class="sxs-lookup"><span data-stu-id="866ab-132">That is, the *parent-command* or *child-command* may itself be another shape command.</span></span>

<span data-ttu-id="866ab-133">Поставщик фигур всегда возвращает курсор клиента, даже если пользователь указывает расположение **курсора adUseServer.**</span><span class="sxs-lookup"><span data-stu-id="866ab-133">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span></span>

<span data-ttu-id="866ab-134">Сведения о навигации по иерархическому **набору записей** см. в сайте [Accessing Rows in a Hierarchical Recordset.](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="866ab-134">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="866ab-135">Точные сведения о синтаксически правильных командах фигур см. в [разделе Formal Shape Grammar](formal-shape-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="866ab-135">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="866ab-136">См. также</span><span class="sxs-lookup"><span data-stu-id="866ab-136">See also</span></span>

- [<span data-ttu-id="866ab-137">Issuing Commands to the Underlying Data Provider</span><span class="sxs-lookup"><span data-stu-id="866ab-137">Issuing Commands to the Underlying Data Provider</span></span>](issuing-commands-to-the-underlying-data-provider.md)

