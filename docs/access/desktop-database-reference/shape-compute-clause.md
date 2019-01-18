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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711527"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="073bf-102">Предложение Compute команды Shape</span><span class="sxs-lookup"><span data-stu-id="073bf-102">Shape Compute clause</span></span>

<span data-ttu-id="073bf-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="073bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="073bf-104">Предложение COMPUTE фигуры создает родительский объект **набора записей**, столбцы которых состоят из ссылки на дочерних **записей**; необязательные столбцы, содержимое которых главы новыми, или вычисляемых столбцов или в результате выполнения агрегатных функций на дочерних **записей** или ранее формы **набора записей**; и все столбцы из дочерних **записей** из списка в необязательном ПРЕДЛОЖЕНИЕМ.</span><span class="sxs-lookup"><span data-stu-id="073bf-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="073bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="073bf-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="073bf-106">Описание</span><span class="sxs-lookup"><span data-stu-id="073bf-106">Description</span></span>

<span data-ttu-id="073bf-107">Части это предложение, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="073bf-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="073bf-108">*Команда дочерних*</span><span class="sxs-lookup"><span data-stu-id="073bf-108">*child-command*</span></span>

  - <span data-ttu-id="073bf-109">Состоит из одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="073bf-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="073bf-110">Команды запроса в фигурные скобки (»{}«), который возвращает дочернего объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="073bf-110">A query command within curly braces ("{}") that returns a child **Recordset** object.</span></span> <span data-ttu-id="073bf-111">Команды для базового поставщика данных, и его синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="073bf-111">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="073bf-112">Обычно это будет языка SQL, несмотря на то, что ADO не требуется любой язык, определенного запроса.</span><span class="sxs-lookup"><span data-stu-id="073bf-112">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="073bf-113">Имя существующего форме **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="073bf-114">Другой команды фигуры.</span><span class="sxs-lookup"><span data-stu-id="073bf-114">Another shape command.</span></span>
    
    - <span data-ttu-id="073bf-115">В ТАБЛИЦЕ ключевого слова, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="073bf-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="073bf-116">*псевдоним дочерних*</span><span class="sxs-lookup"><span data-stu-id="073bf-116">*child-alias*</span></span>

  - <span data-ttu-id="073bf-117">Псевдоним, используемое для ссылки на **набор записей** , возвращаемых *дочерних command.*</span><span class="sxs-lookup"><span data-stu-id="073bf-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="073bf-118">*Псевдоним дочерних* требуется в список столбцов в предложении COMPUTE и определяет отношение между родительских и дочерних объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="073bf-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="073bf-119">*добавлено--список столбцов*</span><span class="sxs-lookup"><span data-stu-id="073bf-119">*appended-column-list*</span></span>

  - <span data-ttu-id="073bf-120">Список, в котором каждый элемент определяет столбец в созданный родительского.</span><span class="sxs-lookup"><span data-stu-id="073bf-120">A list in which each element defines a column in the generated parent.</span></span> <span data-ttu-id="073bf-121">Каждый элемент содержит столбец, новый столбец, вычисляемый столбец или значение, полученное статистические функции на дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-121">Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="073bf-122">*Список полей группу*</span><span class="sxs-lookup"><span data-stu-id="073bf-122">*grp-field-list*</span></span>

  - <span data-ttu-id="073bf-123">Список столбцов в родительских и дочерних объектов **набора записей** , который определяет группировку строк в дочернем.</span><span class="sxs-lookup"><span data-stu-id="073bf-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="073bf-124">Для каждого столбца в *группу--список полей,* существует соответствующий столбец дочерних и родительских объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="073bf-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="073bf-125">Для каждой строки в родительском **записей**столбцы *списка полей группу* иметь уникальные значения и дочерних **записей** ссылается родительской строки состоит только из дочерних строк, *список полей группу* столбцы имеют те же значения, как родительской строки.</span><span class="sxs-lookup"><span data-stu-id="073bf-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="073bf-126">Если предложение по включено, дочерних **записей**в строках будут группироваться основанным на столбцы в предложении COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="073bf-126">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause.</span></span> <span data-ttu-id="073bf-127">Родительский **набор записей** будет содержать одну строку для каждой группы строк в дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-127">The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="073bf-128">Если предложение по указано, все дочерние **записей** обрабатывается как единая группа и родительских **записей** будет содержать только одну строку.</span><span class="sxs-lookup"><span data-stu-id="073bf-128">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row.</span></span> <span data-ttu-id="073bf-129">Соответствующая строка ссылаются на всей дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-129">That row will reference the entire child **Recordset**.</span></span> <span data-ttu-id="073bf-130">Пропуск предложения по позволяет вычисления «Итого» статистических данных по всей дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-130">Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="073bf-131">Пример:</span><span class="sxs-lookup"><span data-stu-id="073bf-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="073bf-132">Независимо от того, какой способ родительского **набора записей** сформирован (с помощью COMPUTE или APPEND) он будет содержать столбец, используемый для связи дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-132">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**.</span></span> <span data-ttu-id="073bf-133">Если вы хотите родительского **набора записей** также может содержать столбцы, содержащие статистические функции (SUM, MIN, MAX и т.д.) через дочерние строки.</span><span class="sxs-lookup"><span data-stu-id="073bf-133">If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</span></span> <span data-ttu-id="073bf-134">Родительских и дочерних **записей** может содержать столбцы, которые содержат выражения в строке, в **набор записей**, а также столбцы, которые являются новыми и изначально очистить.</span><span class="sxs-lookup"><span data-stu-id="073bf-134">Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="073bf-135">Operation</span><span class="sxs-lookup"><span data-stu-id="073bf-135">Operation</span></span>

<span data-ttu-id="073bf-136">*Команда дочерних* должен быть выдан поставщика, который возвращает дочерний элемент **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="073bf-137">Предложение COMPUTE указывает столбцы родительского **набора записей**, который может быть ссылку на дочерних **записей**, статистические выражения на один или несколько, расчетного выражения или новых столбцов.</span><span class="sxs-lookup"><span data-stu-id="073bf-137">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns.</span></span> <span data-ttu-id="073bf-138">В случае предложение BY столбцы, которые он определяет также присоединяются к родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-138">If there is a BY clause, the columns it defines are also appended to the parent **Recordset**.</span></span> <span data-ttu-id="073bf-139">Предложение по указывает способ группировки строк дочерних **записей** .</span><span class="sxs-lookup"><span data-stu-id="073bf-139">The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="073bf-140">Предположим, у вас есть таблицы — демографии, состоящий из состояний, города и заполнения полей (данные совокупности предназначены исключительно для иллюстрации).</span><span class="sxs-lookup"><span data-stu-id="073bf-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="073bf-141">Состояние</span><span class="sxs-lookup"><span data-stu-id="073bf-141">State</span></span></p></th>
<th><p><span data-ttu-id="073bf-142">City</span><span class="sxs-lookup"><span data-stu-id="073bf-142">City</span></span></p></th>
<th><p><span data-ttu-id="073bf-143">Заполнение</span><span class="sxs-lookup"><span data-stu-id="073bf-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="073bf-144">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="073bf-144">WA</span></span></p></td>
<td><p><span data-ttu-id="073bf-145">Сиэтл</span><span class="sxs-lookup"><span data-stu-id="073bf-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="073bf-146">700 000</span><span class="sxs-lookup"><span data-stu-id="073bf-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="073bf-147">OR</span><span class="sxs-lookup"><span data-stu-id="073bf-147">OR</span></span></p></td>
<td><p><span data-ttu-id="073bf-148">Medford</span><span class="sxs-lookup"><span data-stu-id="073bf-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="073bf-149">200 000</span><span class="sxs-lookup"><span data-stu-id="073bf-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="073bf-150">OR</span><span class="sxs-lookup"><span data-stu-id="073bf-150">OR</span></span></p></td>
<td><p><span data-ttu-id="073bf-151">Портленд</span><span class="sxs-lookup"><span data-stu-id="073bf-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="073bf-152">400 000 долларов</span><span class="sxs-lookup"><span data-stu-id="073bf-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="073bf-153">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="073bf-153">CA</span></span></p></td>
<td><p><span data-ttu-id="073bf-154">Лос-Анджелес</span><span class="sxs-lookup"><span data-stu-id="073bf-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="073bf-155">800,000</span><span class="sxs-lookup"><span data-stu-id="073bf-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="073bf-156">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="073bf-156">CA</span></span></p></td>
<td><p><span data-ttu-id="073bf-157">Москва</span><span class="sxs-lookup"><span data-stu-id="073bf-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="073bf-158">600 000</span><span class="sxs-lookup"><span data-stu-id="073bf-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="073bf-159">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="073bf-159">WA</span></span></p></td>
<td><p><span data-ttu-id="073bf-160">Москва</span><span class="sxs-lookup"><span data-stu-id="073bf-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="073bf-161">500 000</span><span class="sxs-lookup"><span data-stu-id="073bf-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="073bf-162">OR</span><span class="sxs-lookup"><span data-stu-id="073bf-162">OR</span></span></p></td>
<td><p><span data-ttu-id="073bf-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="073bf-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="073bf-164">300 000</span><span class="sxs-lookup"><span data-stu-id="073bf-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="073bf-165">Теперь выполните эту команду фигуры:</span><span class="sxs-lookup"><span data-stu-id="073bf-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="073bf-166">Эта команда открывает формы **набора записей** с двумя уровнями.</span><span class="sxs-lookup"><span data-stu-id="073bf-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="073bf-167">Родительский уровень — это созданный **набора записей** с составного столбца (SUM(rs.population)), столбец, создание ссылок на дочерних **записей** (rs) и столбца для группировки дочерних **записей** (состояние).</span><span class="sxs-lookup"><span data-stu-id="073bf-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="073bf-168">Дочерний уровень — это **набор записей** , возвращаемых () команду запроса, столбец, создание ссылок на дочерних **записей** (rs) и столбца для группировки дочерних **записей** (состояние).</span><span class="sxs-lookup"><span data-stu-id="073bf-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="073bf-169">Уровень дочерних — это **набор записей** , возвращаемые командой запроса (выберите \* из демографии).</span><span class="sxs-lookup"><span data-stu-id="073bf-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="073bf-170">Строки сведений о дочерних **наборов записей** будут, сгруппированных по состоянию, но в произвольном порядке, в противном случае —.</span><span class="sxs-lookup"><span data-stu-id="073bf-170">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order.</span></span> <span data-ttu-id="073bf-171">То есть группы не будет находиться в или алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="073bf-171">That is, the groups will not be in alphabetical or numerical order.</span></span> <span data-ttu-id="073bf-172">Если вы хотите родительского **набора записей** упорядоченный, можно использовать метод **сортировки** **набора записей** для упорядочения родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="073bf-172">If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="073bf-173">Теперь можно перейдите открыт родительского **набора записей** и доступ к сведений о **записей** дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="073bf-173">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects.</span></span> <span data-ttu-id="073bf-174">Для получения дополнительных сведений см. [Доступ к строк в иерархической записей](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="073bf-174">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="073bf-175">**Результирующее родительских и дочерних наборов записей подробно**</span><span class="sxs-lookup"><span data-stu-id="073bf-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="073bf-176">**Parent**</span><span class="sxs-lookup"><span data-stu-id="073bf-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="073bf-177">Сумма (rs. Заполнение)</span><span class="sxs-lookup"><span data-stu-id="073bf-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="073bf-178">RS</span><span class="sxs-lookup"><span data-stu-id="073bf-178">rs</span></span></p></th>
<th><p><span data-ttu-id="073bf-179">Состояние</span><span class="sxs-lookup"><span data-stu-id="073bf-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="073bf-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="073bf-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="073bf-181">Ссылка на child1</span><span class="sxs-lookup"><span data-stu-id="073bf-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="073bf-182">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="073bf-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="073bf-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="073bf-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="073bf-184">Ссылка на child2</span><span class="sxs-lookup"><span data-stu-id="073bf-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="073bf-185">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="073bf-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="073bf-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="073bf-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="073bf-187">Ссылка на child3</span><span class="sxs-lookup"><span data-stu-id="073bf-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="073bf-188">OR</span><span class="sxs-lookup"><span data-stu-id="073bf-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="073bf-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="073bf-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="073bf-190">Состояние</span><span class="sxs-lookup"><span data-stu-id="073bf-190">State</span></span></p></th>
<th><p><span data-ttu-id="073bf-191">City</span><span class="sxs-lookup"><span data-stu-id="073bf-191">City</span></span></p></th>
<th><p><span data-ttu-id="073bf-192">Заполнение</span><span class="sxs-lookup"><span data-stu-id="073bf-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="073bf-193">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="073bf-193">CA</span></span></p></td>
<td><p><span data-ttu-id="073bf-194">Лос-Анджелес</span><span class="sxs-lookup"><span data-stu-id="073bf-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="073bf-195">800,000</span><span class="sxs-lookup"><span data-stu-id="073bf-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="073bf-196">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="073bf-196">CA</span></span></p></td>
<td><p><span data-ttu-id="073bf-197">Москва</span><span class="sxs-lookup"><span data-stu-id="073bf-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="073bf-198">600 000</span><span class="sxs-lookup"><span data-stu-id="073bf-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="073bf-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="073bf-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="073bf-200">Состояние</span><span class="sxs-lookup"><span data-stu-id="073bf-200">State</span></span></p></th>
<th><p><span data-ttu-id="073bf-201">City</span><span class="sxs-lookup"><span data-stu-id="073bf-201">City</span></span></p></th>
<th><p><span data-ttu-id="073bf-202">Заполнение</span><span class="sxs-lookup"><span data-stu-id="073bf-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="073bf-203">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="073bf-203">WA</span></span></p></td>
<td><p><span data-ttu-id="073bf-204">Сиэтл</span><span class="sxs-lookup"><span data-stu-id="073bf-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="073bf-205">700 000</span><span class="sxs-lookup"><span data-stu-id="073bf-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="073bf-206">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="073bf-206">WA</span></span></p></td>
<td><p><span data-ttu-id="073bf-207">Москва</span><span class="sxs-lookup"><span data-stu-id="073bf-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="073bf-208">500 000</span><span class="sxs-lookup"><span data-stu-id="073bf-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="073bf-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="073bf-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="073bf-210">Состояние</span><span class="sxs-lookup"><span data-stu-id="073bf-210">State</span></span></p></th>
<th><p><span data-ttu-id="073bf-211">City</span><span class="sxs-lookup"><span data-stu-id="073bf-211">City</span></span></p></th>
<th><p><span data-ttu-id="073bf-212">Заполнение</span><span class="sxs-lookup"><span data-stu-id="073bf-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="073bf-213">OR</span><span class="sxs-lookup"><span data-stu-id="073bf-213">OR</span></span></p></td>
<td><p><span data-ttu-id="073bf-214">Medford</span><span class="sxs-lookup"><span data-stu-id="073bf-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="073bf-215">200 000</span><span class="sxs-lookup"><span data-stu-id="073bf-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="073bf-216">OR</span><span class="sxs-lookup"><span data-stu-id="073bf-216">OR</span></span></p></td>
<td><p><span data-ttu-id="073bf-217">Портленд</span><span class="sxs-lookup"><span data-stu-id="073bf-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="073bf-218">400 000 долларов</span><span class="sxs-lookup"><span data-stu-id="073bf-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="073bf-219">OR</span><span class="sxs-lookup"><span data-stu-id="073bf-219">OR</span></span></p></td>
<td><p><span data-ttu-id="073bf-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="073bf-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="073bf-221">300 000</span><span class="sxs-lookup"><span data-stu-id="073bf-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

