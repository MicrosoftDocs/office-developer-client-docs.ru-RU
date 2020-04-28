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
# <a name="shape-commands-in-general"></a><span data-ttu-id="46fac-102">Общие сведения о командах Shape</span><span class="sxs-lookup"><span data-stu-id="46fac-102">Shape commands in general</span></span>

<span data-ttu-id="46fac-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46fac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46fac-104">При создании данных определяются столбцы объекта **Recordset**в форме, отношения между сущностями, представленные столбцами, и способ заполнения объекта **Recordset** данными.</span><span class="sxs-lookup"><span data-stu-id="46fac-104">Data shaping defines the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="46fac-105">Объект **Recordset** в форме может состоять из следующих типов столбцов.</span><span class="sxs-lookup"><span data-stu-id="46fac-105">A shaped **Recordset** may consist of the following types of columns.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46fac-106">Тип столбца</span><span class="sxs-lookup"><span data-stu-id="46fac-106">Column type</span></span></p></th>
<th><p><span data-ttu-id="46fac-107">Описание</span><span class="sxs-lookup"><span data-stu-id="46fac-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46fac-108">data</span><span class="sxs-lookup"><span data-stu-id="46fac-108">data</span></span></p></td>
<td><p><span data-ttu-id="46fac-109">Поля из <strong>набора записей</strong> , возвращенные командой запроса к поставщику данных, таблице или ранее фигурному <strong>набору записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="46fac-109">Fields from a <strong>Recordset</strong> returned by a query command to a data provider, table, or previously shaped <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46fac-110">части</span><span class="sxs-lookup"><span data-stu-id="46fac-110">chapter</span></span></p></td>
<td><p><span data-ttu-id="46fac-111">Ссылка на другой <strong>набор записей</strong>, называемый <em>главой</em>.</span><span class="sxs-lookup"><span data-stu-id="46fac-111">A reference to another <strong>Recordset</strong>, called a <em>chapter</em>.</span></span> <span data-ttu-id="46fac-112">В столбцах главы можно определить связь типа " <em>родители-потомки</em> ", в которой <em>родитель</em> — это объект <strong>Recordset</strong> , содержащий столбец Chapter, а <em>дочерний</em> элемент — это <strong>набор записей</strong> , представленный главой.</span><span class="sxs-lookup"><span data-stu-id="46fac-112">Chapter columns make it possible to define a <em>parent-child</em> relationship where the <em>parent</em> is the <strong>Recordset</strong> containing the chapter column and the <em>child</em> is the <strong>Recordset</strong> represented by the chapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46fac-113">объединит</span><span class="sxs-lookup"><span data-stu-id="46fac-113">aggregate</span></span></p></td>
<td><p><span data-ttu-id="46fac-114">Значение столбца извлекается путем выполнения <em>статистической функции</em> для всех строк или столбцов всех строк дочернего объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="46fac-114">The value of the column is derived by executing an <em>aggregate function</em> on all the rows or a column of all the rows of a child <strong>Recordset</strong>.</span></span> <span data-ttu-id="46fac-115">(См. статистические функции в следующих разделах, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">статистические функции, функция calc и ключевое слово New</a>.)</span><span class="sxs-lookup"><span data-stu-id="46fac-115">(See Aggregate Functions in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46fac-116">Вычисляемое выражение</span><span class="sxs-lookup"><span data-stu-id="46fac-116">calculated expression</span></span></p></td>
<td><p><span data-ttu-id="46fac-117">Значение столбца извлекается путем вычисления выражения Visual Basic для приложений для столбцов в той же строке <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="46fac-117">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="46fac-118">Выражение является аргументом функции CALC.</span><span class="sxs-lookup"><span data-stu-id="46fac-118">The expression is the argument to the CALC function.</span></span> <span data-ttu-id="46fac-119">(См. вычисленное выражение в следующих разделах, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">статистические функции, функция calc и ключевое слово New</a> и в <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений</a>.)</span><span class="sxs-lookup"><span data-stu-id="46fac-119">(See Calculated Expression in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a> and in <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications Functions</a>.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46fac-120">Новые функции</span><span class="sxs-lookup"><span data-stu-id="46fac-120">new</span></span></p></td>
<td><p><span data-ttu-id="46fac-121">Пустые, заполненные поля, которые могут быть заполнены данными позже.</span><span class="sxs-lookup"><span data-stu-id="46fac-121">Empty, fabricated fields, which may be populated with data at a later time.</span></span> <span data-ttu-id="46fac-122">Столбец определяется с помощью ключевого слова NEW.</span><span class="sxs-lookup"><span data-stu-id="46fac-122">The column is defined with the NEW keyword.</span></span> <span data-ttu-id="46fac-123">(См. ключевое слово NEW в следующих разделах, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">статистические функции, функция calc и ключевое слово New</a>.)</span><span class="sxs-lookup"><span data-stu-id="46fac-123">(See NEW keyword in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="46fac-124">Команда Shape может содержать предложение, задающее команду запроса для базового поставщика данных, который будет возвращать объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="46fac-124">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object.</span></span> <span data-ttu-id="46fac-125">Синтаксис запроса зависит от требований базового поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="46fac-125">The query's syntax depends on the requirements of the underlying data provider.</span></span> <span data-ttu-id="46fac-126">Как правило, это будет язык структурированных запросов (SQL), хотя для ADO не требуется использование какого-либо конкретного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="46fac-126">This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span></span>

<span data-ttu-id="46fac-127">Вы можете использовать предложение JOIN SQL, чтобы связать две таблицы; Однако иерархический **набор записей** может представлять данные более эффективно.</span><span class="sxs-lookup"><span data-stu-id="46fac-127">You could use a SQL JOIN clause to relate two tables; however, a hierarchical **Recordset** may represent the information more efficiently.</span></span> <span data-ttu-id="46fac-128">Каждая строка **набора записей** , созданная при объединении, повторяет данные из одной из таблиц.</span><span class="sxs-lookup"><span data-stu-id="46fac-128">Each row of a **Recordset** created by a JOIN repeats information redundantly from one of the tables.</span></span> <span data-ttu-id="46fac-129">Иерархический **набор** записей имеет только один родительский **набор записей** для каждого из нескольких дочерних объектов **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="46fac-129">A hierarchical **Recordset** has only one parent **Recordset** for each of multiple child **Recordset** objects.</span></span>

<span data-ttu-id="46fac-130">Команды Shape могут выдаваться объектами **Recordset** или путем установки свойства [CommandText](commandtext-property-ado.md) объекта [Command](command-object-ado.md) , а затем вызова метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .</span><span class="sxs-lookup"><span data-stu-id="46fac-130">Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

<span data-ttu-id="46fac-131">Команды фигур могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="46fac-131">Shape commands can be nested.</span></span> <span data-ttu-id="46fac-132">То есть *родительская команда* или *дочерняя команда* может быть другой командой Shape.</span><span class="sxs-lookup"><span data-stu-id="46fac-132">That is, the *parent-command* or *child-command* may itself be another shape command.</span></span>

<span data-ttu-id="46fac-133">Поставщик фигур всегда возвращает клиентский курсор, даже если пользователь указывает расположение курсора **адусесервер**.</span><span class="sxs-lookup"><span data-stu-id="46fac-133">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span></span>

<span data-ttu-id="46fac-134">Сведения о переходе на иерархический **набор записей**содержатся [в разделе доступ к строкам в иерархическом наборе записей](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="46fac-134">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="46fac-135">Точные сведения о синтаксически правильных командах формы можно узнать в статье [формальное описание грамматики фигур](formal-shape-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="46fac-135">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="46fac-136">См. также</span><span class="sxs-lookup"><span data-stu-id="46fac-136">See also</span></span>

- [<span data-ttu-id="46fac-137">Issuing Commands to the Underlying Data Provider</span><span class="sxs-lookup"><span data-stu-id="46fac-137">Issuing Commands to the Underlying Data Provider</span></span>](issuing-commands-to-the-underlying-data-provider.md)

