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
# <a name="shape-compute-clause"></a><span data-ttu-id="5ac1f-102">Предложение Compute команды Shape</span><span class="sxs-lookup"><span data-stu-id="5ac1f-102">Shape Compute clause</span></span>

<span data-ttu-id="5ac1f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ac1f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ac1f-104">Предложение COMPUTE фигуры создает родительский набор **записей,** столбцы которого состоят из ссылки на child **Recordset;** необязательные столбцы, содержимое которых является главой, новым или вычисляемым столбцом, или результатом выполнения агрегатных функций в наборе записей или ранее сформированном наборе **записей;**  и все столбцы из child **Recordset, перечисленные** в необязательном предложении BY.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac1f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ac1f-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="5ac1f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5ac1f-106">Description</span></span>

<span data-ttu-id="5ac1f-107">Часть этого предложения:</span><span class="sxs-lookup"><span data-stu-id="5ac1f-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="5ac1f-108">*child-command*</span><span class="sxs-lookup"><span data-stu-id="5ac1f-108">*child-command*</span></span>

  - <span data-ttu-id="5ac1f-109">Состоит из одного из следующих ок.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="5ac1f-110">Команда запроса в фигурных скобках (" "), которая возвращает {} объект **объекта Recordset.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-110">A query command within curly braces ("{}") that returns a child **Recordset** object.</span></span> <span data-ttu-id="5ac1f-111">Команда передается основному поставщику данных, и ее синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-111">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="5ac1f-112">Обычно это язык SQL, хотя ADO не требует определенного языка запросов.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-112">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="5ac1f-113">Имя существующего фигурного **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="5ac1f-114">Другая команда фигуры.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-114">Another shape command.</span></span>
    
    - <span data-ttu-id="5ac1f-115">Ключевое слово TABLE, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="5ac1f-116">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="5ac1f-116">*child-alias*</span></span>

  - <span data-ttu-id="5ac1f-117">Псевдоним, используемый для ссылки на **набор записей,** возвращаемого *командой-child.*</span><span class="sxs-lookup"><span data-stu-id="5ac1f-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="5ac1f-118">*Псевдоним-потомок* требуется в списке столбцов в предложении COMPUTE и определяет отношение между родительским и родительским **объектами Recordset.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="5ac1f-119">*appended-column-list*</span><span class="sxs-lookup"><span data-stu-id="5ac1f-119">*appended-column-list*</span></span>

  - <span data-ttu-id="5ac1f-120">Список, в котором каждый элемент определяет столбец в сформированных родительских элементах.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-120">A list in which each element defines a column in the generated parent.</span></span> <span data-ttu-id="5ac1f-121">Каждый элемент содержит столбец главы, новый столбец, вычисленный столбец или значение, которое является результатом агрегированной функции в наборе **записей.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-121">Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="5ac1f-122">*grp-field-list*</span><span class="sxs-lookup"><span data-stu-id="5ac1f-122">*grp-field-list*</span></span>

  - <span data-ttu-id="5ac1f-123">Список столбцов в родительских и родительских объектах **Recordset,** который указывает, как строки должны быть сгрупплены в потомке.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="5ac1f-124">Для каждого столбца в *списке grp-field-list* имеется соответствующий столбец в объектах child и parent **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="5ac1f-125">Для каждой строки в родительском наборе записей столбцы *списка grp-field-list* имеют уникальные значения, а набор записей, на который ссылается родительская строка, состоит исключительно из всех строк, столбцы списка *grp-field-list* которых имеют те же значения, что и родительская строка. </span><span class="sxs-lookup"><span data-stu-id="5ac1f-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="5ac1f-126">Если предложение BY включено, строки этого наборов записей будут сгруппироваться на основе столбцов в предложении COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-126">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause.</span></span> <span data-ttu-id="5ac1f-127">Родительский **набор записей** будет содержать по одной строке для каждой группы строк в этом наборе **записей.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-127">The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="5ac1f-128">Если предложение BY опущено,  весь набор записей будет рассматриваться как одна группа, а родительский набор **записей** будет содержать ровно одну строку.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-128">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row.</span></span> <span data-ttu-id="5ac1f-129">Эта строка будет ссылаться на весь набор **записей.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-129">That row will reference the entire child **Recordset**.</span></span> <span data-ttu-id="5ac1f-130">Опущение предложения BY позволяет вычислить итоговые суммы по всему набору **записей.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-130">Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="5ac1f-131">Например:</span><span class="sxs-lookup"><span data-stu-id="5ac1f-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="5ac1f-132">Независимо от того,  каким образом формируется родительский набор записей (с помощью COMPUTE или APPEND), он будет содержать столбец главы, который используется для его отношения с набором **записей.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-132">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**.</span></span> <span data-ttu-id="5ac1f-133">При желании родительский набор записей также может содержать столбцы, которые содержат сводки (SUM, MIN, MAX и так далее) по этим строкам. </span><span class="sxs-lookup"><span data-stu-id="5ac1f-133">If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</span></span> <span data-ttu-id="5ac1f-134">Родительский и родительский набор записей могут содержать столбцы, содержащие выражение в строке в наборе записей, а также новые и изначально пустые столбцы.  </span><span class="sxs-lookup"><span data-stu-id="5ac1f-134">Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="5ac1f-135">Operation</span><span class="sxs-lookup"><span data-stu-id="5ac1f-135">Operation</span></span>

<span data-ttu-id="5ac1f-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="5ac1f-137">Предложение COMPUTE указывает столбцы родительского наборов записей, которые могут быть ссылкой на набор записей, один или несколько агрегатов, вычисленное выражение или новые столбцы. </span><span class="sxs-lookup"><span data-stu-id="5ac1f-137">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns.</span></span> <span data-ttu-id="5ac1f-138">Если есть предложение BY, определенные в нем столбцы также будут приданы родительскому **набору записей.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-138">If there is a BY clause, the columns it defines are also appended to the parent **Recordset**.</span></span> <span data-ttu-id="5ac1f-139">Предложение BY указывает, как группировать строки из этого **наборов** записей.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-139">The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="5ac1f-140">Например, предположим, что у вас есть таблица "Демографические данные", состоящая из полей "State", "City" и "Population" (рисунки исключительно для иллюстрации).</span><span class="sxs-lookup"><span data-stu-id="5ac1f-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ac1f-141">Состояние</span><span class="sxs-lookup"><span data-stu-id="5ac1f-141">State</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-142">Город</span><span class="sxs-lookup"><span data-stu-id="5ac1f-142">City</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-143">Population</span><span class="sxs-lookup"><span data-stu-id="5ac1f-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-144">WA</span><span class="sxs-lookup"><span data-stu-id="5ac1f-144">WA</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-145">Сиэтл</span><span class="sxs-lookup"><span data-stu-id="5ac1f-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-146">700,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ac1f-147">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ac1f-147">OR</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-148">Medford</span><span class="sxs-lookup"><span data-stu-id="5ac1f-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-149">200 000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-150">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ac1f-150">OR</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-151">Портленд</span><span class="sxs-lookup"><span data-stu-id="5ac1f-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-152">400,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ac1f-153">ЦС</span><span class="sxs-lookup"><span data-stu-id="5ac1f-153">CA</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-154">Нью-Йорк</span><span class="sxs-lookup"><span data-stu-id="5ac1f-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-155">800,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-156">ЦС</span><span class="sxs-lookup"><span data-stu-id="5ac1f-156">CA</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-157">Сан-Кио</span><span class="sxs-lookup"><span data-stu-id="5ac1f-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-158">600 000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ac1f-159">WA</span><span class="sxs-lookup"><span data-stu-id="5ac1f-159">WA</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-160">Такома</span><span class="sxs-lookup"><span data-stu-id="5ac1f-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-161">500 000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-162">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ac1f-162">OR</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="5ac1f-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-164">300,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5ac1f-165">Теперь выдаем данной команде фигуры:</span><span class="sxs-lookup"><span data-stu-id="5ac1f-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="5ac1f-166">Эта команда открывает фигурный набор **записей с** двумя уровнями.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="5ac1f-167">Родительский уровень —  это созданный набор записей со сводным столбцом (SUM(rs.population) ), столбцом, ссылаясь на потомок **recordset** (rs) и столбцом для группировки child **Recordset** (state).</span><span class="sxs-lookup"><span data-stu-id="5ac1f-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="5ac1f-168">Уровень потомка  — это набор записей, возвращаемой командой запроса (), столбец, ссылающийся на потомок **Recordset** (rs), и столбец для группировки child **Recordset** (state).</span><span class="sxs-lookup"><span data-stu-id="5ac1f-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="5ac1f-169">Уровень child — это **набор записей,** возвращаемой командой запроса (выберите \* из демографических данных).</span><span class="sxs-lookup"><span data-stu-id="5ac1f-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="5ac1f-170">Строки **подробных данных в** наборе записей будут сгруппироваться по состояниям, но в противном случае в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-170">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order.</span></span> <span data-ttu-id="5ac1f-171">То есть группы не будут в алфавитном или числовом порядке.</span><span class="sxs-lookup"><span data-stu-id="5ac1f-171">That is, the groups will not be in alphabetical or numerical order.</span></span> <span data-ttu-id="5ac1f-172">Если необходимо указать **родительский** набор записей, можно использовать метод **Recordset** **Sort** для упорядочения родительского **recordset.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-172">If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="5ac1f-173">Теперь вы можете перемещаться по открытому родительскому набору **записей** и получать доступ к объектам **объекта Recordset для подробных данных.**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-173">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects.</span></span> <span data-ttu-id="5ac1f-174">Дополнительные сведения см. в подсети "Доступ к [строкам в иерархическом наборе записей".](accessing-rows-in-a-hierarchical-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="5ac1f-174">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="5ac1f-175">**Resultant Parent and Child Detail Recordsets**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="5ac1f-176">**Parent**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ac1f-177">SUM (rs. Population)</span><span class="sxs-lookup"><span data-stu-id="5ac1f-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-178">rs</span><span class="sxs-lookup"><span data-stu-id="5ac1f-178">rs</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-179">Состояние</span><span class="sxs-lookup"><span data-stu-id="5ac1f-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-181">Ссылка на child1</span><span class="sxs-lookup"><span data-stu-id="5ac1f-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-182">ЦС</span><span class="sxs-lookup"><span data-stu-id="5ac1f-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ac1f-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-184">Ссылка на child2</span><span class="sxs-lookup"><span data-stu-id="5ac1f-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-185">WA</span><span class="sxs-lookup"><span data-stu-id="5ac1f-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-187">Ссылка на child3</span><span class="sxs-lookup"><span data-stu-id="5ac1f-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-188">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ac1f-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5ac1f-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ac1f-190">Состояние</span><span class="sxs-lookup"><span data-stu-id="5ac1f-190">State</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-191">Город</span><span class="sxs-lookup"><span data-stu-id="5ac1f-191">City</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-192">Population</span><span class="sxs-lookup"><span data-stu-id="5ac1f-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-193">ЦС</span><span class="sxs-lookup"><span data-stu-id="5ac1f-193">CA</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-194">Нью-Йорк</span><span class="sxs-lookup"><span data-stu-id="5ac1f-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-195">800,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ac1f-196">ЦС</span><span class="sxs-lookup"><span data-stu-id="5ac1f-196">CA</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-197">Сан-Кио</span><span class="sxs-lookup"><span data-stu-id="5ac1f-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-198">600 000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5ac1f-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ac1f-200">Состояние</span><span class="sxs-lookup"><span data-stu-id="5ac1f-200">State</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-201">Город</span><span class="sxs-lookup"><span data-stu-id="5ac1f-201">City</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-202">Population</span><span class="sxs-lookup"><span data-stu-id="5ac1f-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-203">WA</span><span class="sxs-lookup"><span data-stu-id="5ac1f-203">WA</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-204">Сиэтл</span><span class="sxs-lookup"><span data-stu-id="5ac1f-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-205">700,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ac1f-206">WA</span><span class="sxs-lookup"><span data-stu-id="5ac1f-206">WA</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-207">Такома</span><span class="sxs-lookup"><span data-stu-id="5ac1f-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-208">500 000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5ac1f-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="5ac1f-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ac1f-210">Состояние</span><span class="sxs-lookup"><span data-stu-id="5ac1f-210">State</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-211">Город</span><span class="sxs-lookup"><span data-stu-id="5ac1f-211">City</span></span></p></th>
<th><p><span data-ttu-id="5ac1f-212">Population</span><span class="sxs-lookup"><span data-stu-id="5ac1f-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-213">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ac1f-213">OR</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-214">Medford</span><span class="sxs-lookup"><span data-stu-id="5ac1f-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-215">200 000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ac1f-216">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ac1f-216">OR</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-217">Портленд</span><span class="sxs-lookup"><span data-stu-id="5ac1f-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-218">400,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ac1f-219">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="5ac1f-219">OR</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="5ac1f-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="5ac1f-221">300,000</span><span class="sxs-lookup"><span data-stu-id="5ac1f-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

