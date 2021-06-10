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
# <a name="shape-compute-clause"></a><span data-ttu-id="03379-102">Предложение Compute команды Shape</span><span class="sxs-lookup"><span data-stu-id="03379-102">Shape Compute clause</span></span>

<span data-ttu-id="03379-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03379-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03379-104">Положение COMPUTE формы создает родительский **набор записей,** столбцы которого состоят из ссылки на детский **набор записей;** необязательные столбцы, содержимое которых — это главы, новые или рассчитанные столбцы, или результат выполнения совокупных функций в детском наборе записей или ранее сформированном **Наборе записей;**  и любые столбцы из списка **записей ребенка,** указанные в необязательных статьях BY.</span><span class="sxs-lookup"><span data-stu-id="03379-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="03379-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03379-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="03379-106">Описание</span><span class="sxs-lookup"><span data-stu-id="03379-106">Description</span></span>

<span data-ttu-id="03379-107">Части этого положения:</span><span class="sxs-lookup"><span data-stu-id="03379-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="03379-108">*детская команда*</span><span class="sxs-lookup"><span data-stu-id="03379-108">*child-command*</span></span>

  - <span data-ttu-id="03379-109">Состоит из одного из следующих:</span><span class="sxs-lookup"><span data-stu-id="03379-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="03379-110">Команда запроса в фигурных скобки ("), которая {} возвращает объект **recordset** ребенка.</span><span class="sxs-lookup"><span data-stu-id="03379-110">A query command within curly braces ("{}") that returns a child **Recordset** object.</span></span> <span data-ttu-id="03379-111">Команда выдана основному поставщику данных, и ее синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="03379-111">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="03379-112">Обычно это будет язык SQL, хотя ADO не требует какого-либо конкретного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="03379-112">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="03379-113">Имя существующего формы **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="03379-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="03379-114">Еще одна команда фигуры.</span><span class="sxs-lookup"><span data-stu-id="03379-114">Another shape command.</span></span>
    
    - <span data-ttu-id="03379-115">Ключевое слово TABLE с именем таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="03379-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="03379-116">*псевдоним ребенка*</span><span class="sxs-lookup"><span data-stu-id="03379-116">*child-alias*</span></span>

  - <span data-ttu-id="03379-117">Псевдоним, используемый для ссылки на **набор записей,** возвращенный *детской командой.*</span><span class="sxs-lookup"><span data-stu-id="03379-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="03379-118">Псевдоним *ребенка* требуется в списке столбцов в статье COMPUTE и определяет связь между родительскими и детскими **объектами Recordset.**</span><span class="sxs-lookup"><span data-stu-id="03379-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="03379-119">*appended-column-list*</span><span class="sxs-lookup"><span data-stu-id="03379-119">*appended-column-list*</span></span>

  - <span data-ttu-id="03379-120">Список, в котором каждый элемент определяет столбец в сгенерированной родительской.</span><span class="sxs-lookup"><span data-stu-id="03379-120">A list in which each element defines a column in the generated parent.</span></span> <span data-ttu-id="03379-121">Каждый элемент содержит столбец главы, новый столбец, вычисляемую колонку или значение, которое является результатом совокупной функции в детском **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="03379-121">Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="03379-122">*grp-field-list*</span><span class="sxs-lookup"><span data-stu-id="03379-122">*grp-field-list*</span></span>

  - <span data-ttu-id="03379-123">Список столбцов в родительских и детских объектах **Recordset,** который указывает, как следует сгруппировать строки в ребенке.</span><span class="sxs-lookup"><span data-stu-id="03379-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="03379-124">Для каждого столбца в *списке grp-field имеется* соответствующий столбец в объектах **recordset** для детей и родителей.</span><span class="sxs-lookup"><span data-stu-id="03379-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="03379-125">Для каждой строки в родительском Наборе записей столбцы списков grp-field имеют уникальные значения, а детский набор записей, на который ссылается родительская строка, состоит исключительно из детских строк, столбцы которых  *grp-field-list* имеют те же значения, что и родительская строка. </span><span class="sxs-lookup"><span data-stu-id="03379-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="03379-126">Если предложение BY включено, строки записи ребенка будут сгруппироваться на основе столбцов в пункте COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="03379-126">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause.</span></span> <span data-ttu-id="03379-127">Родительский **набор записей** будет содержать по одной строке для каждой группы строк в детском **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="03379-127">The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="03379-128">Если предложение BY опущено,  весь набор записей для детей рассматривается как одна группа, а родительский набор **записей** будет содержать ровно одну строку.</span><span class="sxs-lookup"><span data-stu-id="03379-128">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row.</span></span> <span data-ttu-id="03379-129">Эта строка будет ссылаться на весь набор **записей ребенка**.</span><span class="sxs-lookup"><span data-stu-id="03379-129">That row will reference the entire child **Recordset**.</span></span> <span data-ttu-id="03379-130">Опущение пункта BY позволяет вычислять совокупные суммы по всему детскому **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="03379-130">Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="03379-131">Пример.</span><span class="sxs-lookup"><span data-stu-id="03379-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="03379-132">Независимо от того,  каким образом формируется родительский набор записей (с помощью COMPUTE или с помощью APPEND), он будет содержать столбец главы, который используется для его соотноски с ребенком **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="03379-132">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**.</span></span> <span data-ttu-id="03379-133">При желании родительский набор **записей** также может содержать столбцы, содержащие сводки (SUM, MIN, MAX и так далее) над детскими строками.</span><span class="sxs-lookup"><span data-stu-id="03379-133">If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</span></span> <span data-ttu-id="03379-134">Родительский и детский  набор записей могут содержать столбцы, содержащие выражение строки в Наборе записей, а также столбцы, которые являются новыми и изначально пустыми.</span><span class="sxs-lookup"><span data-stu-id="03379-134">Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="03379-135">Операция</span><span class="sxs-lookup"><span data-stu-id="03379-135">Operation</span></span>

<span data-ttu-id="03379-136">Команда *для детей* выдана поставщику, который возвращает детский набор **записей.**</span><span class="sxs-lookup"><span data-stu-id="03379-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="03379-137">В статье COMPUTE указаны столбцы родительского набора записей, которые могут быть ссылкой на детский набор записей, один или несколько агрегатов, вычислимое выражение или новые столбцы.</span><span class="sxs-lookup"><span data-stu-id="03379-137">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns.</span></span> <span data-ttu-id="03379-138">Если есть пункт BY, столбцы, которые он определяет, также примыкают к родительскому **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="03379-138">If there is a BY clause, the columns it defines are also appended to the parent **Recordset**.</span></span> <span data-ttu-id="03379-139">В статье BY указывается, как сгруппировать строки детского **набора** записей.</span><span class="sxs-lookup"><span data-stu-id="03379-139">The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="03379-140">Например, предположим, что у вас есть таблица — Демографические поля, состоящие из областей состояния, города и населения (цифры населения являются исключительно иллюстрациями).</span><span class="sxs-lookup"><span data-stu-id="03379-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03379-141">Состояние</span><span class="sxs-lookup"><span data-stu-id="03379-141">State</span></span></p></th>
<th><p><span data-ttu-id="03379-142">Город</span><span class="sxs-lookup"><span data-stu-id="03379-142">City</span></span></p></th>
<th><p><span data-ttu-id="03379-143">Население</span><span class="sxs-lookup"><span data-stu-id="03379-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03379-144">Wa</span><span class="sxs-lookup"><span data-stu-id="03379-144">WA</span></span></p></td>
<td><p><span data-ttu-id="03379-145">Сиэтл</span><span class="sxs-lookup"><span data-stu-id="03379-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="03379-146">700,000</span><span class="sxs-lookup"><span data-stu-id="03379-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03379-147">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="03379-147">OR</span></span></p></td>
<td><p><span data-ttu-id="03379-148">Medford</span><span class="sxs-lookup"><span data-stu-id="03379-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="03379-149">200 000</span><span class="sxs-lookup"><span data-stu-id="03379-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03379-150">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="03379-150">OR</span></span></p></td>
<td><p><span data-ttu-id="03379-151">Портленд</span><span class="sxs-lookup"><span data-stu-id="03379-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="03379-152">400,000</span><span class="sxs-lookup"><span data-stu-id="03379-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03379-153">CA</span><span class="sxs-lookup"><span data-stu-id="03379-153">CA</span></span></p></td>
<td><p><span data-ttu-id="03379-154">Лос-Анджелес</span><span class="sxs-lookup"><span data-stu-id="03379-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="03379-155">800,000</span><span class="sxs-lookup"><span data-stu-id="03379-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03379-156">CA</span><span class="sxs-lookup"><span data-stu-id="03379-156">CA</span></span></p></td>
<td><p><span data-ttu-id="03379-157">Сан-Диего</span><span class="sxs-lookup"><span data-stu-id="03379-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="03379-158">600 000</span><span class="sxs-lookup"><span data-stu-id="03379-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03379-159">Wa</span><span class="sxs-lookup"><span data-stu-id="03379-159">WA</span></span></p></td>
<td><p><span data-ttu-id="03379-160">Tacoma</span><span class="sxs-lookup"><span data-stu-id="03379-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="03379-161">500 000</span><span class="sxs-lookup"><span data-stu-id="03379-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03379-162">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="03379-162">OR</span></span></p></td>
<td><p><span data-ttu-id="03379-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="03379-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="03379-164">300,000</span><span class="sxs-lookup"><span data-stu-id="03379-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03379-165">Теперь выдай эту команду фигуры:</span><span class="sxs-lookup"><span data-stu-id="03379-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="03379-166">Эта команда открывает сформированный **набор записей с** двумя уровнями.</span><span class="sxs-lookup"><span data-stu-id="03379-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="03379-167">Родительский уровень —  это созданный набор записей со сводным столбцом (SUM(rs.population), столбец, ссылающийся на детский набор записей  (rs) и столбец для группировки детского **recordset** (состояние).</span><span class="sxs-lookup"><span data-stu-id="03379-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="03379-168">Уровень ребенка —  это набор записей, возвращаемый командой запроса (), столбец, отсылающий к детскому набору записей  (rs) и столбец для группировки ребенка **Recordset** (состояние).</span><span class="sxs-lookup"><span data-stu-id="03379-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="03379-169">Уровень ребенка — это **набор записей,** возвращаемый командой запросов (выберите \* из демографических показателей).</span><span class="sxs-lookup"><span data-stu-id="03379-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="03379-170">Строки **данных о** ребенке будут сгруппироваться по состояниям, но в противном случае не будут в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="03379-170">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order.</span></span> <span data-ttu-id="03379-171">То есть группы не будут в алфавитном или числовом порядке.</span><span class="sxs-lookup"><span data-stu-id="03379-171">That is, the groups will not be in alphabetical or numerical order.</span></span> <span data-ttu-id="03379-172">Если необходимо заказать **родительский** набор записей, можно заказать родительский набор записей с помощью метода  **сортировки** **recordset.**</span><span class="sxs-lookup"><span data-stu-id="03379-172">If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="03379-173">Теперь можно перемещаться по открываемой родительской **записи и** получать доступ к объектам **учетной** записи для детей.</span><span class="sxs-lookup"><span data-stu-id="03379-173">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects.</span></span> <span data-ttu-id="03379-174">Дополнительные сведения см. [в рублях Accessing Rows in a Hierarchical Recordset.](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="03379-174">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="03379-175">**Итоги записей родительских и детских деталей**</span><span class="sxs-lookup"><span data-stu-id="03379-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="03379-176">**Parent**</span><span class="sxs-lookup"><span data-stu-id="03379-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03379-177">SUM (rs. Население)</span><span class="sxs-lookup"><span data-stu-id="03379-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="03379-178">rs</span><span class="sxs-lookup"><span data-stu-id="03379-178">rs</span></span></p></th>
<th><p><span data-ttu-id="03379-179">Состояние</span><span class="sxs-lookup"><span data-stu-id="03379-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03379-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="03379-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="03379-181">Ссылка на child1</span><span class="sxs-lookup"><span data-stu-id="03379-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="03379-182">CA</span><span class="sxs-lookup"><span data-stu-id="03379-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03379-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="03379-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="03379-184">Ссылка на child2</span><span class="sxs-lookup"><span data-stu-id="03379-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="03379-185">Wa</span><span class="sxs-lookup"><span data-stu-id="03379-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03379-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="03379-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="03379-187">Ссылка на child3</span><span class="sxs-lookup"><span data-stu-id="03379-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="03379-188">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="03379-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03379-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="03379-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03379-190">Состояние</span><span class="sxs-lookup"><span data-stu-id="03379-190">State</span></span></p></th>
<th><p><span data-ttu-id="03379-191">Город</span><span class="sxs-lookup"><span data-stu-id="03379-191">City</span></span></p></th>
<th><p><span data-ttu-id="03379-192">Население</span><span class="sxs-lookup"><span data-stu-id="03379-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03379-193">CA</span><span class="sxs-lookup"><span data-stu-id="03379-193">CA</span></span></p></td>
<td><p><span data-ttu-id="03379-194">Лос-Анджелес</span><span class="sxs-lookup"><span data-stu-id="03379-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="03379-195">800,000</span><span class="sxs-lookup"><span data-stu-id="03379-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03379-196">CA</span><span class="sxs-lookup"><span data-stu-id="03379-196">CA</span></span></p></td>
<td><p><span data-ttu-id="03379-197">Сан-Диего</span><span class="sxs-lookup"><span data-stu-id="03379-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="03379-198">600 000</span><span class="sxs-lookup"><span data-stu-id="03379-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03379-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="03379-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03379-200">Состояние</span><span class="sxs-lookup"><span data-stu-id="03379-200">State</span></span></p></th>
<th><p><span data-ttu-id="03379-201">Город</span><span class="sxs-lookup"><span data-stu-id="03379-201">City</span></span></p></th>
<th><p><span data-ttu-id="03379-202">Население</span><span class="sxs-lookup"><span data-stu-id="03379-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03379-203">Wa</span><span class="sxs-lookup"><span data-stu-id="03379-203">WA</span></span></p></td>
<td><p><span data-ttu-id="03379-204">Сиэтл</span><span class="sxs-lookup"><span data-stu-id="03379-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="03379-205">700,000</span><span class="sxs-lookup"><span data-stu-id="03379-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03379-206">Wa</span><span class="sxs-lookup"><span data-stu-id="03379-206">WA</span></span></p></td>
<td><p><span data-ttu-id="03379-207">Tacoma</span><span class="sxs-lookup"><span data-stu-id="03379-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="03379-208">500 000</span><span class="sxs-lookup"><span data-stu-id="03379-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="03379-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="03379-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03379-210">Состояние</span><span class="sxs-lookup"><span data-stu-id="03379-210">State</span></span></p></th>
<th><p><span data-ttu-id="03379-211">Город</span><span class="sxs-lookup"><span data-stu-id="03379-211">City</span></span></p></th>
<th><p><span data-ttu-id="03379-212">Население</span><span class="sxs-lookup"><span data-stu-id="03379-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03379-213">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="03379-213">OR</span></span></p></td>
<td><p><span data-ttu-id="03379-214">Medford</span><span class="sxs-lookup"><span data-stu-id="03379-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="03379-215">200 000</span><span class="sxs-lookup"><span data-stu-id="03379-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03379-216">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="03379-216">OR</span></span></p></td>
<td><p><span data-ttu-id="03379-217">Портленд</span><span class="sxs-lookup"><span data-stu-id="03379-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="03379-218">400,000</span><span class="sxs-lookup"><span data-stu-id="03379-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03379-219">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="03379-219">OR</span></span></p></td>
<td><p><span data-ttu-id="03379-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="03379-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="03379-221">300,000</span><span class="sxs-lookup"><span data-stu-id="03379-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

