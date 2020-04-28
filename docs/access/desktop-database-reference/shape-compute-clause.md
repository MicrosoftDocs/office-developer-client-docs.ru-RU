---
title: Предложение Compute команды Shape
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306456"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="91c29-102">Предложение Compute команды Shape</span><span class="sxs-lookup"><span data-stu-id="91c29-102">Shape Compute clause</span></span>

<span data-ttu-id="91c29-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91c29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91c29-104">Предложение COMPUTE для Shape создает родительский объект **Recordset**, столбцы которого состоят из ссылки на дочерний **набор записей**; необязательные столбцы, содержимое которых — это глава, новые или вычисляемые столбцы, а также результат выполнения статистических функций в дочернем **наборе записей** или ранее фигурном **наборе записей**. и все столбцы из дочернего **набора записей** , перечисленные в дополнительном предложении by.</span><span class="sxs-lookup"><span data-stu-id="91c29-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="91c29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91c29-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="91c29-106">Описание</span><span class="sxs-lookup"><span data-stu-id="91c29-106">Description</span></span>

<span data-ttu-id="91c29-107">Ниже приведен список частей этого предложения.</span><span class="sxs-lookup"><span data-stu-id="91c29-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="91c29-108">*Дочерняя команда*</span><span class="sxs-lookup"><span data-stu-id="91c29-108">*child-command*</span></span>

  - <span data-ttu-id="91c29-109">Состоит из одного из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="91c29-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="91c29-110">Команда запроса в фигурных скобках ("{}"), которая возвращает дочерний объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="91c29-110">A query command within curly braces ("{}") that returns a child **Recordset** object.</span></span> <span data-ttu-id="91c29-111">Команда выдается базовому поставщику данных, а его синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="91c29-111">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="91c29-112">Как правило, это язык SQL, хотя для ADO не требуется определенный язык запросов.</span><span class="sxs-lookup"><span data-stu-id="91c29-112">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="91c29-113">Имя существующего **набора записей**в форме.</span><span class="sxs-lookup"><span data-stu-id="91c29-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="91c29-114">Другая команда "Фигура".</span><span class="sxs-lookup"><span data-stu-id="91c29-114">Another shape command.</span></span>
    
    - <span data-ttu-id="91c29-115">Ключевое слово TABLE, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="91c29-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="91c29-116">*дочерний псевдоним*</span><span class="sxs-lookup"><span data-stu-id="91c29-116">*child-alias*</span></span>

  - <span data-ttu-id="91c29-117">Псевдоним, используемый для ссылки на **набор записей** , возвращенный *дочерней командой.*</span><span class="sxs-lookup"><span data-stu-id="91c29-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="91c29-118">В списке столбцов в выражении COMPUTE должен быть указан *дочерний псевдоним* и определено отношение между родительским и дочерним объектами **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="91c29-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="91c29-119">*добавленный список столбцов*</span><span class="sxs-lookup"><span data-stu-id="91c29-119">*appended-column-list*</span></span>

  - <span data-ttu-id="91c29-120">Список, в котором каждый элемент определяет столбец в созданном родительском объекте.</span><span class="sxs-lookup"><span data-stu-id="91c29-120">A list in which each element defines a column in the generated parent.</span></span> <span data-ttu-id="91c29-121">Каждый элемент содержит столбец раздела, новый столбец, вычисляемый столбец или значение, полученное в результате статистической функции в дочернем **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="91c29-121">Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="91c29-122">*GRP — список полей*</span><span class="sxs-lookup"><span data-stu-id="91c29-122">*grp-field-list*</span></span>

  - <span data-ttu-id="91c29-123">Список столбцов в родительских и дочерних объектах **Recordset** , указывающих способ группировки строк в дочернем элементе.</span><span class="sxs-lookup"><span data-stu-id="91c29-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="91c29-124">Для каждого столбца в *списке GRP-Field* присутствует соответствующий столбец в дочерних и родительских объектах **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="91c29-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="91c29-125">Для каждой строки в родительском **наборе записей**столбцы *списка GRP* имеют уникальные значения, а дочерний **набор записей** , на который ссылается родительская строка, состоит только из дочерних строк, у которых столбцы "GRP" и " *список* " имеют те же значения, что и в родительской строке.</span><span class="sxs-lookup"><span data-stu-id="91c29-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="91c29-126">Если включено предложение BY, строки дочернего **набора записей**будут сгруппированы на основе столбцов в предложении COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="91c29-126">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause.</span></span> <span data-ttu-id="91c29-127">Родительский **набор записей** будет содержать по одной строке для каждой группы строк в дочернем **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="91c29-127">The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="91c29-128">Если предложение BY опущено, весь дочерний **набор записей** обрабатывается как единственная группа, а родительский **набор записей** будет содержать ровно одну строку.</span><span class="sxs-lookup"><span data-stu-id="91c29-128">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row.</span></span> <span data-ttu-id="91c29-129">Эта строка будет ссылаться на весь дочерний **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="91c29-129">That row will reference the entire child **Recordset**.</span></span> <span data-ttu-id="91c29-130">Пропуск предложения BY позволяет вычислять статистические значения "Общая сумма" для всего дочернего объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="91c29-130">Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="91c29-131">Например:</span><span class="sxs-lookup"><span data-stu-id="91c29-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="91c29-132">Независимо от способа формирования родительского **набора записей** (с помощью COMPUTE или using Append), он будет содержать столбец Chapter, который используется для связывания с дочерним **набором записей**.</span><span class="sxs-lookup"><span data-stu-id="91c29-132">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**.</span></span> <span data-ttu-id="91c29-133">При желании родительский **набор записей** также может содержать столбцы, содержащие статистические выражения (SUM, min, Max и т. д.), над дочерними строками.</span><span class="sxs-lookup"><span data-stu-id="91c29-133">If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</span></span> <span data-ttu-id="91c29-134">Как родительский, так и дочерний **набор записей** могут содержать столбцы, которые содержат выражение для строки в **наборе записей**, а также столбцы, которые являются новыми и изначально пусты.</span><span class="sxs-lookup"><span data-stu-id="91c29-134">Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="91c29-135">Операция</span><span class="sxs-lookup"><span data-stu-id="91c29-135">Operation</span></span>

<span data-ttu-id="91c29-136">Для поставщика отправляется *дочерняя команда* , которая возвращает дочерний **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="91c29-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="91c29-137">Предложение COMPUTE указывает столбцы родительского объекта **Recordset**, которые могут быть ссылками на дочерний **набор записей**, одно или несколько статистических выражений, вычисляемых выражений или новых столбцов.</span><span class="sxs-lookup"><span data-stu-id="91c29-137">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns.</span></span> <span data-ttu-id="91c29-138">При наличии предложения BY столбцы, которые он определяет, также добавляются в родительский **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="91c29-138">If there is a BY clause, the columns it defines are also appended to the parent **Recordset**.</span></span> <span data-ttu-id="91c29-139">Предложение BY определяет, как группируются строки дочернего **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="91c29-139">The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="91c29-140">Например, предположим, что у вас есть таблица — демографические сведения, состоящие из полей "штат", "город" и "Заполнение" (для иллюстрации используются только цифры заполнения).</span><span class="sxs-lookup"><span data-stu-id="91c29-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91c29-141">Состояние</span><span class="sxs-lookup"><span data-stu-id="91c29-141">State</span></span></p></th>
<th><p><span data-ttu-id="91c29-142">Город</span><span class="sxs-lookup"><span data-stu-id="91c29-142">City</span></span></p></th>
<th><p><span data-ttu-id="91c29-143">Установки</span><span class="sxs-lookup"><span data-stu-id="91c29-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91c29-144">ШТАТ</span><span class="sxs-lookup"><span data-stu-id="91c29-144">WA</span></span></p></td>
<td><p><span data-ttu-id="91c29-145">Seattle</span><span class="sxs-lookup"><span data-stu-id="91c29-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="91c29-146">700 000</span><span class="sxs-lookup"><span data-stu-id="91c29-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91c29-147">OR</span><span class="sxs-lookup"><span data-stu-id="91c29-147">OR</span></span></p></td>
<td><p><span data-ttu-id="91c29-148">медфорд</span><span class="sxs-lookup"><span data-stu-id="91c29-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="91c29-149">200 000</span><span class="sxs-lookup"><span data-stu-id="91c29-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91c29-150">OR</span><span class="sxs-lookup"><span data-stu-id="91c29-150">OR</span></span></p></td>
<td><p><span data-ttu-id="91c29-151">Портленд</span><span class="sxs-lookup"><span data-stu-id="91c29-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="91c29-152">400,000</span><span class="sxs-lookup"><span data-stu-id="91c29-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91c29-153">ЦЕНТРОВ</span><span class="sxs-lookup"><span data-stu-id="91c29-153">CA</span></span></p></td>
<td><p><span data-ttu-id="91c29-154">Лос, Лос</span><span class="sxs-lookup"><span data-stu-id="91c29-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="91c29-155">800 000</span><span class="sxs-lookup"><span data-stu-id="91c29-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91c29-156">ЦЕНТРОВ</span><span class="sxs-lookup"><span data-stu-id="91c29-156">CA</span></span></p></td>
<td><p><span data-ttu-id="91c29-157">Сан Диего</span><span class="sxs-lookup"><span data-stu-id="91c29-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="91c29-158">600 000</span><span class="sxs-lookup"><span data-stu-id="91c29-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91c29-159">ШТАТ</span><span class="sxs-lookup"><span data-stu-id="91c29-159">WA</span></span></p></td>
<td><p><span data-ttu-id="91c29-160">такома</span><span class="sxs-lookup"><span data-stu-id="91c29-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="91c29-161">500 000</span><span class="sxs-lookup"><span data-stu-id="91c29-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91c29-162">OR</span><span class="sxs-lookup"><span data-stu-id="91c29-162">OR</span></span></p></td>
<td><p><span data-ttu-id="91c29-163">корваллис</span><span class="sxs-lookup"><span data-stu-id="91c29-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="91c29-164">300 000</span><span class="sxs-lookup"><span data-stu-id="91c29-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91c29-165">Теперь выполните следующую команду фигуры:</span><span class="sxs-lookup"><span data-stu-id="91c29-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="91c29-166">Эта команда открывает объект **Recordset** в форме с двумя уровнями.</span><span class="sxs-lookup"><span data-stu-id="91c29-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="91c29-167">Родительский уровень — это созданный **набор записей** со столбцом статистической обработки (SUM (RS. Population)), столбцом, ссылающимся на дочерний объект **Recordset** (RS), и столбцом для группирования дочернего объекта **Recordset** (State).</span><span class="sxs-lookup"><span data-stu-id="91c29-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="91c29-168">Дочерний уровень — это **набор записей** , возвращенный командой запроса (), столбец, ссылающийся на дочерний объект **Recordset** (RS), и столбец для группирования дочернего объекта **Recordset** (State).</span><span class="sxs-lookup"><span data-stu-id="91c29-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="91c29-169">Дочерний уровень — это **набор записей** , возвращенный командой запроса \* (выберите из демографических данных).</span><span class="sxs-lookup"><span data-stu-id="91c29-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="91c29-170">Строки сведений о дочернем **наборе записей** группируются по состоянию, но в противном случае нет определенного порядка.</span><span class="sxs-lookup"><span data-stu-id="91c29-170">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order.</span></span> <span data-ttu-id="91c29-171">То есть группы не будут отображаться в алфавитном или числовом порядке.</span><span class="sxs-lookup"><span data-stu-id="91c29-171">That is, the groups will not be in alphabetical or numerical order.</span></span> <span data-ttu-id="91c29-172">Если требуется упорядочить родительский **набор записей** , можно использовать метод **сортировки** **Recordset** , чтобы упорядочить родительский **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="91c29-172">If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="91c29-173">Теперь вы можете перейти на открытый родительский **набор записей** и получить доступ к дочерним объектам **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="91c29-173">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects.</span></span> <span data-ttu-id="91c29-174">Более подробную информацию можно узнать [в статье доступ к строкам в иерархическом наборе записей](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="91c29-174">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="91c29-175">**Результирующие наборы записей результирующего родительского и дочернего элементов**</span><span class="sxs-lookup"><span data-stu-id="91c29-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="91c29-176">**Parent**</span><span class="sxs-lookup"><span data-stu-id="91c29-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91c29-177">SUM (RS. Установки</span><span class="sxs-lookup"><span data-stu-id="91c29-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="91c29-178">кабел</span><span class="sxs-lookup"><span data-stu-id="91c29-178">rs</span></span></p></th>
<th><p><span data-ttu-id="91c29-179">Состояние</span><span class="sxs-lookup"><span data-stu-id="91c29-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91c29-180">1 300 000</span><span class="sxs-lookup"><span data-stu-id="91c29-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="91c29-181">Ссылка на child1</span><span class="sxs-lookup"><span data-stu-id="91c29-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="91c29-182">ЦЕНТРОВ</span><span class="sxs-lookup"><span data-stu-id="91c29-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91c29-183">1 200 000</span><span class="sxs-lookup"><span data-stu-id="91c29-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="91c29-184">Ссылка на Child2</span><span class="sxs-lookup"><span data-stu-id="91c29-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="91c29-185">ШТАТ</span><span class="sxs-lookup"><span data-stu-id="91c29-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91c29-186">1 100 000</span><span class="sxs-lookup"><span data-stu-id="91c29-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="91c29-187">Ссылка на child3</span><span class="sxs-lookup"><span data-stu-id="91c29-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="91c29-188">OR</span><span class="sxs-lookup"><span data-stu-id="91c29-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91c29-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="91c29-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91c29-190">Состояние</span><span class="sxs-lookup"><span data-stu-id="91c29-190">State</span></span></p></th>
<th><p><span data-ttu-id="91c29-191">Город</span><span class="sxs-lookup"><span data-stu-id="91c29-191">City</span></span></p></th>
<th><p><span data-ttu-id="91c29-192">Установки</span><span class="sxs-lookup"><span data-stu-id="91c29-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91c29-193">ЦЕНТРОВ</span><span class="sxs-lookup"><span data-stu-id="91c29-193">CA</span></span></p></td>
<td><p><span data-ttu-id="91c29-194">Лос, Лос</span><span class="sxs-lookup"><span data-stu-id="91c29-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="91c29-195">800 000</span><span class="sxs-lookup"><span data-stu-id="91c29-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91c29-196">ЦЕНТРОВ</span><span class="sxs-lookup"><span data-stu-id="91c29-196">CA</span></span></p></td>
<td><p><span data-ttu-id="91c29-197">Сан Диего</span><span class="sxs-lookup"><span data-stu-id="91c29-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="91c29-198">600 000</span><span class="sxs-lookup"><span data-stu-id="91c29-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91c29-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="91c29-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91c29-200">Состояние</span><span class="sxs-lookup"><span data-stu-id="91c29-200">State</span></span></p></th>
<th><p><span data-ttu-id="91c29-201">Город</span><span class="sxs-lookup"><span data-stu-id="91c29-201">City</span></span></p></th>
<th><p><span data-ttu-id="91c29-202">Установки</span><span class="sxs-lookup"><span data-stu-id="91c29-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91c29-203">ШТАТ</span><span class="sxs-lookup"><span data-stu-id="91c29-203">WA</span></span></p></td>
<td><p><span data-ttu-id="91c29-204">Seattle</span><span class="sxs-lookup"><span data-stu-id="91c29-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="91c29-205">700 000</span><span class="sxs-lookup"><span data-stu-id="91c29-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91c29-206">ШТАТ</span><span class="sxs-lookup"><span data-stu-id="91c29-206">WA</span></span></p></td>
<td><p><span data-ttu-id="91c29-207">такома</span><span class="sxs-lookup"><span data-stu-id="91c29-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="91c29-208">500 000</span><span class="sxs-lookup"><span data-stu-id="91c29-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91c29-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="91c29-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91c29-210">Состояние</span><span class="sxs-lookup"><span data-stu-id="91c29-210">State</span></span></p></th>
<th><p><span data-ttu-id="91c29-211">Город</span><span class="sxs-lookup"><span data-stu-id="91c29-211">City</span></span></p></th>
<th><p><span data-ttu-id="91c29-212">Установки</span><span class="sxs-lookup"><span data-stu-id="91c29-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91c29-213">OR</span><span class="sxs-lookup"><span data-stu-id="91c29-213">OR</span></span></p></td>
<td><p><span data-ttu-id="91c29-214">медфорд</span><span class="sxs-lookup"><span data-stu-id="91c29-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="91c29-215">200 000</span><span class="sxs-lookup"><span data-stu-id="91c29-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91c29-216">OR</span><span class="sxs-lookup"><span data-stu-id="91c29-216">OR</span></span></p></td>
<td><p><span data-ttu-id="91c29-217">Портленд</span><span class="sxs-lookup"><span data-stu-id="91c29-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="91c29-218">400,000</span><span class="sxs-lookup"><span data-stu-id="91c29-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91c29-219">OR</span><span class="sxs-lookup"><span data-stu-id="91c29-219">OR</span></span></p></td>
<td><p><span data-ttu-id="91c29-220">корваллис</span><span class="sxs-lookup"><span data-stu-id="91c29-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="91c29-221">300 000</span><span class="sxs-lookup"><span data-stu-id="91c29-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

