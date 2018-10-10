---
title: Shape Compute Clause
TOCTitle: Shape Compute Clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 634a0ea648646d95995054ce7458cea492c40e47
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482942"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="87bc6-102">Shape Compute Clause</span><span class="sxs-lookup"><span data-stu-id="87bc6-102">Shape Compute Clause</span></span>

<span data-ttu-id="87bc6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="87bc6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="87bc6-104">Предложение COMPUTE фигуры создает родительский объект **набора записей**, столбцы которых состоят из ссылки на дочерних **записей**; необязательные столбцы, содержимое которых главы новыми, или вычисляемых столбцов или в результате выполнения агрегатных функций на дочерних **записей** или ранее формы **набора записей**; и все столбцы из дочерних **записей** из списка в необязательном ПРЕДЛОЖЕНИЕМ.</span><span class="sxs-lookup"><span data-stu-id="87bc6-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="87bc6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87bc6-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="87bc6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="87bc6-106">Description</span></span>

<span data-ttu-id="87bc6-107">Части это предложение, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="87bc6-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="87bc6-108">*Команда дочерних*</span><span class="sxs-lookup"><span data-stu-id="87bc6-108">*child-command*</span></span>

  - <span data-ttu-id="87bc6-109">Состоит из одной из следующих:</span><span class="sxs-lookup"><span data-stu-id="87bc6-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="87bc6-110">Команды запроса в фигурные скобки (»{}«), который возвращает дочернего объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="87bc6-110">A query command within curly braces ("{}") that returns a child **Recordset** object.</span></span> <span data-ttu-id="87bc6-111">Команды для базового поставщика данных, и его синтаксис зависит от требований этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="87bc6-111">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="87bc6-112">Обычно это будет языка SQL, несмотря на то, что ADO не требуется любой язык, определенного запроса.</span><span class="sxs-lookup"><span data-stu-id="87bc6-112">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="87bc6-113">Имя существующего форме **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="87bc6-114">Другой команды фигуры.</span><span class="sxs-lookup"><span data-stu-id="87bc6-114">Another shape command.</span></span>
    
    - <span data-ttu-id="87bc6-115">В ТАБЛИЦЕ ключевого слова, за которым следует имя таблицы в поставщике данных.</span><span class="sxs-lookup"><span data-stu-id="87bc6-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="87bc6-116">*псевдоним дочерних*</span><span class="sxs-lookup"><span data-stu-id="87bc6-116">*child-alias*</span></span>

  - <span data-ttu-id="87bc6-117">Псевдоним, используемое для ссылки на **набор записей** , возвращаемых *дочерних command.*</span><span class="sxs-lookup"><span data-stu-id="87bc6-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="87bc6-118">*Псевдоним дочерних* требуется в список столбцов в предложении COMPUTE и определяет отношение между родительских и дочерних объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="87bc6-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="87bc6-119">*добавлено--список столбцов*</span><span class="sxs-lookup"><span data-stu-id="87bc6-119">*appended-column-list*</span></span>

  - <span data-ttu-id="87bc6-120">Список, в котором каждый элемент определяет столбец в созданный родительского.</span><span class="sxs-lookup"><span data-stu-id="87bc6-120">A list in which each element defines a column in the generated parent.</span></span> <span data-ttu-id="87bc6-121">Каждый элемент содержит столбец, новый столбец, вычисляемый столбец или значение, полученное статистические функции на дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-121">Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="87bc6-122">*Список полей группу*</span><span class="sxs-lookup"><span data-stu-id="87bc6-122">*grp-field-list*</span></span>

  - <span data-ttu-id="87bc6-123">Список столбцов в родительских и дочерних объектов **набора записей** , который определяет группировку строк в дочернем.</span><span class="sxs-lookup"><span data-stu-id="87bc6-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="87bc6-124">Для каждого столбца в *группу--список полей,* существует соответствующий столбец дочерних и родительских объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="87bc6-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="87bc6-125">Для каждой строки в родительском **записей**столбцы *списка полей группу* иметь уникальные значения и дочерних **записей** ссылается родительской строки состоит только из дочерних строк, *список полей группу* столбцы имеют те же значения, как родительской строки.</span><span class="sxs-lookup"><span data-stu-id="87bc6-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="87bc6-126">Если предложение по включено, дочерних **записей**в строках будут группироваться основанным на столбцы в предложении COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="87bc6-126">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause.</span></span> <span data-ttu-id="87bc6-127">Родительский **набор записей** будет содержать одну строку для каждой группы строк в дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-127">The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="87bc6-128">Если предложение по указано, все дочерние **записей** обрабатывается как единая группа и родительских **записей** будет содержать только одну строку.</span><span class="sxs-lookup"><span data-stu-id="87bc6-128">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row.</span></span> <span data-ttu-id="87bc6-129">Соответствующая строка ссылаются на всей дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-129">That row will reference the entire child **Recordset**.</span></span> <span data-ttu-id="87bc6-130">Пропуск предложения по позволяет вычисления «Итого» статистических данных по всей дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-130">Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="87bc6-131">Пример:</span><span class="sxs-lookup"><span data-stu-id="87bc6-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="87bc6-132">Независимо от того, какой способ родительского **набора записей** сформирован (с помощью COMPUTE или APPEND) он будет содержать столбец, используемый для связи дочерних **записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-132">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**.</span></span> <span data-ttu-id="87bc6-133">Если вы хотите родительского **набора записей** также может содержать столбцы, содержащие статистические функции (SUM, MIN, MAX и т.д.) через дочерние строки.</span><span class="sxs-lookup"><span data-stu-id="87bc6-133">If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows.</span></span> <span data-ttu-id="87bc6-134">Родительских и дочерних **записей** может содержать столбцы, которые содержат выражения в строке, в **набор записей**, а также столбцы, которые являются новыми и изначально очистить.</span><span class="sxs-lookup"><span data-stu-id="87bc6-134">Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="87bc6-135">Операция</span><span class="sxs-lookup"><span data-stu-id="87bc6-135">Operation</span></span>

<span data-ttu-id="87bc6-136">*Команда дочерних* должен быть выдан поставщика, который возвращает дочерний элемент **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="87bc6-137">Предложение COMPUTE указывает столбцы родительского **набора записей**, который может быть ссылку на дочерних **записей**, статистические выражения на один или несколько, расчетного выражения или новых столбцов.</span><span class="sxs-lookup"><span data-stu-id="87bc6-137">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns.</span></span> <span data-ttu-id="87bc6-138">В случае предложение BY столбцы, которые он определяет также присоединяются к родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-138">If there is a BY clause, the columns it defines are also appended to the parent **Recordset**.</span></span> <span data-ttu-id="87bc6-139">Предложение по указывает способ группировки строк дочерних **записей** .</span><span class="sxs-lookup"><span data-stu-id="87bc6-139">The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="87bc6-140">Предположим, у вас есть таблицы — демографии, состоящий из состояний, города и заполнения полей (данные совокупности предназначены исключительно для иллюстрации).</span><span class="sxs-lookup"><span data-stu-id="87bc6-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87bc6-141">State</span><span class="sxs-lookup"><span data-stu-id="87bc6-141">State</span></span></p></th>
<th><p><span data-ttu-id="87bc6-142">City</span><span class="sxs-lookup"><span data-stu-id="87bc6-142">City</span></span></p></th>
<th><p><span data-ttu-id="87bc6-143">Заполнение</span><span class="sxs-lookup"><span data-stu-id="87bc6-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-144">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="87bc6-144">WA</span></span></p></td>
<td><p><span data-ttu-id="87bc6-145">Сиэтл</span><span class="sxs-lookup"><span data-stu-id="87bc6-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="87bc6-146">700 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87bc6-147">OR</span><span class="sxs-lookup"><span data-stu-id="87bc6-147">OR</span></span></p></td>
<td><p><span data-ttu-id="87bc6-148">Medford</span><span class="sxs-lookup"><span data-stu-id="87bc6-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="87bc6-149">200 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-150">OR</span><span class="sxs-lookup"><span data-stu-id="87bc6-150">OR</span></span></p></td>
<td><p><span data-ttu-id="87bc6-151">Портленд</span><span class="sxs-lookup"><span data-stu-id="87bc6-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="87bc6-152">400 000 долларов</span><span class="sxs-lookup"><span data-stu-id="87bc6-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87bc6-153">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="87bc6-153">CA</span></span></p></td>
<td><p><span data-ttu-id="87bc6-154">Лос-Анджелес</span><span class="sxs-lookup"><span data-stu-id="87bc6-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="87bc6-155">800,000</span><span class="sxs-lookup"><span data-stu-id="87bc6-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-156">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="87bc6-156">CA</span></span></p></td>
<td><p><span data-ttu-id="87bc6-157">Москва</span><span class="sxs-lookup"><span data-stu-id="87bc6-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="87bc6-158">600 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87bc6-159">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="87bc6-159">WA</span></span></p></td>
<td><p><span data-ttu-id="87bc6-160">Москва</span><span class="sxs-lookup"><span data-stu-id="87bc6-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="87bc6-161">500 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-162">OR</span><span class="sxs-lookup"><span data-stu-id="87bc6-162">OR</span></span></p></td>
<td><p><span data-ttu-id="87bc6-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="87bc6-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="87bc6-164">300 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87bc6-165">Теперь выполните эту команду фигуры:</span><span class="sxs-lookup"><span data-stu-id="87bc6-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="87bc6-166">Эта команда открывает формы **набора записей** с двумя уровнями.</span><span class="sxs-lookup"><span data-stu-id="87bc6-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="87bc6-167">Родительский уровень — это созданный **набора записей** с составного столбца (SUM(rs.population)), столбец, создание ссылок на дочерних **записей** (rs) и столбца для группировки дочерних **записей** (состояние).</span><span class="sxs-lookup"><span data-stu-id="87bc6-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="87bc6-168">Дочерний уровень — это **набор записей** , возвращаемых () команду запроса, столбец, создание ссылок на дочерних **записей** (rs) и столбца для группировки дочерних **записей** (состояние).</span><span class="sxs-lookup"><span data-stu-id="87bc6-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="87bc6-169">Уровень дочерних — это **набор записей** , возвращаемые командой запроса (выберите \* из демографии).</span><span class="sxs-lookup"><span data-stu-id="87bc6-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="87bc6-170">Строки сведений о дочерних **наборов записей** будут, сгруппированных по состоянию, но в произвольном порядке, в противном случае —.</span><span class="sxs-lookup"><span data-stu-id="87bc6-170">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order.</span></span> <span data-ttu-id="87bc6-171">То есть группы не будет находиться в или алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="87bc6-171">That is, the groups will not be in alphabetical or numerical order.</span></span> <span data-ttu-id="87bc6-172">Если вы хотите родительского **набора записей** упорядоченный, можно использовать метод **сортировки** **набора записей** для упорядочения родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="87bc6-172">If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="87bc6-173">Теперь можно перейдите открыт родительского **набора записей** и доступ к сведений о **записей** дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="87bc6-173">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects.</span></span> <span data-ttu-id="87bc6-174">Для получения дополнительных сведений см. [Доступ к строк в иерархической записей](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="87bc6-174">For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="87bc6-175">**Результирующее родительских и дочерних наборов записей подробно**</span><span class="sxs-lookup"><span data-stu-id="87bc6-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="87bc6-176">**Parent**</span><span class="sxs-lookup"><span data-stu-id="87bc6-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87bc6-177">Сумма (rs. Заполнение)</span><span class="sxs-lookup"><span data-stu-id="87bc6-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="87bc6-178">RS</span><span class="sxs-lookup"><span data-stu-id="87bc6-178">rs</span></span></p></th>
<th><p><span data-ttu-id="87bc6-179">State</span><span class="sxs-lookup"><span data-stu-id="87bc6-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="87bc6-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="87bc6-181">Ссылка на child1</span><span class="sxs-lookup"><span data-stu-id="87bc6-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="87bc6-182">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="87bc6-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87bc6-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="87bc6-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="87bc6-184">Ссылка на child2</span><span class="sxs-lookup"><span data-stu-id="87bc6-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="87bc6-185">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="87bc6-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="87bc6-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="87bc6-187">Ссылка на child3</span><span class="sxs-lookup"><span data-stu-id="87bc6-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="87bc6-188">OR</span><span class="sxs-lookup"><span data-stu-id="87bc6-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87bc6-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="87bc6-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87bc6-190">State</span><span class="sxs-lookup"><span data-stu-id="87bc6-190">State</span></span></p></th>
<th><p><span data-ttu-id="87bc6-191">City</span><span class="sxs-lookup"><span data-stu-id="87bc6-191">City</span></span></p></th>
<th><p><span data-ttu-id="87bc6-192">Заполнение</span><span class="sxs-lookup"><span data-stu-id="87bc6-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-193">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="87bc6-193">CA</span></span></p></td>
<td><p><span data-ttu-id="87bc6-194">Лос-Анджелес</span><span class="sxs-lookup"><span data-stu-id="87bc6-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="87bc6-195">800,000</span><span class="sxs-lookup"><span data-stu-id="87bc6-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87bc6-196">ЦЕНТР СЕРТИФИКАЦИИ</span><span class="sxs-lookup"><span data-stu-id="87bc6-196">CA</span></span></p></td>
<td><p><span data-ttu-id="87bc6-197">Москва</span><span class="sxs-lookup"><span data-stu-id="87bc6-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="87bc6-198">600 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87bc6-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="87bc6-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87bc6-200">State</span><span class="sxs-lookup"><span data-stu-id="87bc6-200">State</span></span></p></th>
<th><p><span data-ttu-id="87bc6-201">City</span><span class="sxs-lookup"><span data-stu-id="87bc6-201">City</span></span></p></th>
<th><p><span data-ttu-id="87bc6-202">Заполнение</span><span class="sxs-lookup"><span data-stu-id="87bc6-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-203">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="87bc6-203">WA</span></span></p></td>
<td><p><span data-ttu-id="87bc6-204">Сиэтл</span><span class="sxs-lookup"><span data-stu-id="87bc6-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="87bc6-205">700 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87bc6-206">ШТАТ ВАШИНГТОН</span><span class="sxs-lookup"><span data-stu-id="87bc6-206">WA</span></span></p></td>
<td><p><span data-ttu-id="87bc6-207">Москва</span><span class="sxs-lookup"><span data-stu-id="87bc6-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="87bc6-208">500 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87bc6-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="87bc6-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87bc6-210">State</span><span class="sxs-lookup"><span data-stu-id="87bc6-210">State</span></span></p></th>
<th><p><span data-ttu-id="87bc6-211">City</span><span class="sxs-lookup"><span data-stu-id="87bc6-211">City</span></span></p></th>
<th><p><span data-ttu-id="87bc6-212">Заполнение</span><span class="sxs-lookup"><span data-stu-id="87bc6-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-213">OR</span><span class="sxs-lookup"><span data-stu-id="87bc6-213">OR</span></span></p></td>
<td><p><span data-ttu-id="87bc6-214">Medford</span><span class="sxs-lookup"><span data-stu-id="87bc6-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="87bc6-215">200 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87bc6-216">OR</span><span class="sxs-lookup"><span data-stu-id="87bc6-216">OR</span></span></p></td>
<td><p><span data-ttu-id="87bc6-217">Портленд</span><span class="sxs-lookup"><span data-stu-id="87bc6-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="87bc6-218">400 000 долларов</span><span class="sxs-lookup"><span data-stu-id="87bc6-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87bc6-219">OR</span><span class="sxs-lookup"><span data-stu-id="87bc6-219">OR</span></span></p></td>
<td><p><span data-ttu-id="87bc6-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="87bc6-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="87bc6-221">300 000</span><span class="sxs-lookup"><span data-stu-id="87bc6-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

