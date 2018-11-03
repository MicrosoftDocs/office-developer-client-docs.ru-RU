---
title: В общем команды фигуры
TOCTitle: Shape commands in general
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a670c5c6d266da390528810935016d8c1e4aaae
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943950"
---
# <a name="shape-commands-in-general"></a><span data-ttu-id="a8b70-102">В общем команды фигуры</span><span class="sxs-lookup"><span data-stu-id="a8b70-102">Shape commands in general</span></span>

<span data-ttu-id="a8b70-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8b70-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8b70-104">Формирование данных определяет столбцы формы **записей**отношений между сущностями, представленные в столбцы и порядка, в котором выполняется заполнение **набора записей** с данными.</span><span class="sxs-lookup"><span data-stu-id="a8b70-104">Data shaping defines the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="a8b70-105">Формы **записей** может состоять из следующих типов столбцов.</span><span class="sxs-lookup"><span data-stu-id="a8b70-105">A shaped **Recordset** may consist of the following types of columns.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8b70-106">Тип столбца</span><span class="sxs-lookup"><span data-stu-id="a8b70-106">Column type</span></span></p></th>
<th><p><span data-ttu-id="a8b70-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a8b70-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8b70-108">data</span><span class="sxs-lookup"><span data-stu-id="a8b70-108">data</span></span></p></td>
<td><p><span data-ttu-id="a8b70-109">Поля из <strong>набора записей</strong> , возвращаемые командой запросов для поставщика данных, таблицы или ранее формы <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8b70-109">Fields from a <strong>Recordset</strong> returned by a query command to a data provider, table, or previously shaped <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8b70-110">главы</span><span class="sxs-lookup"><span data-stu-id="a8b70-110">chapter</span></span></p></td>
<td><p><span data-ttu-id="a8b70-111">Ссылки на другой <strong>набор записей</strong>, называется <em>главы</em>.</span><span class="sxs-lookup"><span data-stu-id="a8b70-111">A reference to another <strong>Recordset</strong>, called a <em>chapter</em>.</span></span> <span data-ttu-id="a8b70-112">Глава столбцов позволяют Определение отношения <em>родительских и дочерних</em> где <em>родительский</em> — <strong>набора записей</strong> , содержащий столбец главы и <em>дочерние</em> — <strong>набора записей</strong> , представленный в главе.</span><span class="sxs-lookup"><span data-stu-id="a8b70-112">Chapter columns make it possible to define a <em>parent-child</em> relationship where the <em>parent</em> is the <strong>Recordset</strong> containing the chapter column and the <em>child</em> is the <strong>Recordset</strong> represented by the chapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8b70-113">выполняется статистическая обработка</span><span class="sxs-lookup"><span data-stu-id="a8b70-113">aggregate</span></span></p></td>
<td><p><span data-ttu-id="a8b70-114">Значение столбца определяется путем выполнения <em>агрегатных функций</em> для всех строк или столбцов всех строк дочернего объекта <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8b70-114">The value of the column is derived by executing an <em>aggregate function</em> on all the rows or a column of all the rows of a child <strong>Recordset</strong>.</span></span> <span data-ttu-id="a8b70-115">(Увидеть агрегатных функций в следующем разделе <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">агрегатных функций, функция CALC и ключевое слово NEW</a>).</span><span class="sxs-lookup"><span data-stu-id="a8b70-115">(See Aggregate Functions in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8b70-116">расчетного выражения</span><span class="sxs-lookup"><span data-stu-id="a8b70-116">calculated expression</span></span></p></td>
<td><p><span data-ttu-id="a8b70-117">Значение столбца определяется с помощью вычисления Visual Basic для приложений выражения на столбцы в той же строке <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="a8b70-117">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="a8b70-118">Выражение — это аргумент в функцию Вычисление.</span><span class="sxs-lookup"><span data-stu-id="a8b70-118">The expression is the argument to the CALC function.</span></span> <span data-ttu-id="a8b70-119">(См вычисляется выражение в следующем разделе <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">агрегатных функций, функция CALC и НОВОЕ ключевое слово</a> и в <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений функций</a>).</span><span class="sxs-lookup"><span data-stu-id="a8b70-119">(See Calculated Expression in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a> and in <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications Functions</a>.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8b70-120">Новые функции</span><span class="sxs-lookup"><span data-stu-id="a8b70-120">new</span></span></p></td>
<td><p><span data-ttu-id="a8b70-121">Поля пустой, создано, которые могут быть установлены данных в будущем.</span><span class="sxs-lookup"><span data-stu-id="a8b70-121">Empty, fabricated fields, which may be populated with data at a later time.</span></span> <span data-ttu-id="a8b70-122">Столбец определен с НОВЫМ ключевым словом.</span><span class="sxs-lookup"><span data-stu-id="a8b70-122">The column is defined with the NEW keyword.</span></span> <span data-ttu-id="a8b70-123">(НОВОЕ ключевое слово в следующем разделе <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">агрегатных функций, функция CALC и НОВОЕ ключевое слово</a>см).</span><span class="sxs-lookup"><span data-stu-id="a8b70-123">(See NEW keyword in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8b70-124">Команда фигура может содержать предложение, определяющее команду запроса для базового поставщика данных, который возвращает объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a8b70-124">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object.</span></span> <span data-ttu-id="a8b70-125">Синтаксис запроса зависит от требований, предъявляемых базового поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="a8b70-125">The query's syntax depends on the requirements of the underlying data provider.</span></span> <span data-ttu-id="a8b70-126">Это обычно будет структурированный язык SQL (Query), несмотря на то, что ADO не требуется использовать любой язык, определенного запроса.</span><span class="sxs-lookup"><span data-stu-id="a8b70-126">This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span></span>

<span data-ttu-id="a8b70-127">Можно использовать предложение присоединиться к SQL для связи двух таблиц; Тем не менее иерархические **записей** может представлять данные более эффективно.</span><span class="sxs-lookup"><span data-stu-id="a8b70-127">You could use a SQL JOIN clause to relate two tables; however, a hierarchical **Recordset** may represent the information more efficiently.</span></span> <span data-ttu-id="a8b70-128">Каждая строка **набора записей** , созданных с помощью СОЕДИНЕНИЯ повторяет сведения о избыточностью из одной из таблиц.</span><span class="sxs-lookup"><span data-stu-id="a8b70-128">Each row of a **Recordset** created by a JOIN repeats information redundantly from one of the tables.</span></span> <span data-ttu-id="a8b70-129">Иерархическая **набора записей** имеет только один родительский **набор записей** для каждого из нескольких дочерних объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a8b70-129">A hierarchical **Recordset** has only one parent **Recordset** for each of multiple child **Recordset** objects.</span></span>

<span data-ttu-id="a8b70-130">Фигура команды могут выполняться с помощью объектов **набора записей** или путем установки свойства [CommandText](commandtext-property-ado.md) объекта [команды](command-object-ado.md) и вызова метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .</span><span class="sxs-lookup"><span data-stu-id="a8b70-130">Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

<span data-ttu-id="a8b70-131">Фигура команды могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="a8b70-131">Shape commands can be nested.</span></span> <span data-ttu-id="a8b70-132">То есть *команда родительского* или *дочернего командной* самого возможно другую фигуру, команда.</span><span class="sxs-lookup"><span data-stu-id="a8b70-132">That is, the *parent-command* or *child-command* may itself be another shape command.</span></span>

<span data-ttu-id="a8b70-133">Поставщик фигуры всегда возвращает курсор клиента, даже в том случае, когда пользователь указывает местоположение курсора из **adUseServer**.</span><span class="sxs-lookup"><span data-stu-id="a8b70-133">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span></span>

<span data-ttu-id="a8b70-134">Сведения о навигации в иерархической **набора записей** [Доступ к строк в иерархической записей](accessing-rows-in-a-hierarchical-recordset.md)см.</span><span class="sxs-lookup"><span data-stu-id="a8b70-134">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="a8b70-135">Точные сведения о командах синтаксически правильные фигуры видеть [Официальные грамматики фигуры](formal-shape-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="a8b70-135">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a8b70-136">См. также</span><span class="sxs-lookup"><span data-stu-id="a8b70-136">See also</span></span>

- [<span data-ttu-id="a8b70-137">Отправка команд базовому поставщику данных</span><span class="sxs-lookup"><span data-stu-id="a8b70-137">Issuing Commands to the Underlying Data Provider</span></span>](issuing-commands-to-the-underlying-data-provider.md)

