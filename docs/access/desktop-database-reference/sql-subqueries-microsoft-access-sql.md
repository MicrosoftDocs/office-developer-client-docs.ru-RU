---
title: Вложенные запросы SQL (Microsoft Access SQL)
TOCTitle: SQL subqueries (Microsoft Access SQL)
ms:assetid: 3b6c0a5d-ab24-e1cf-0175-3f8e68c2dfbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192664(v=office.15)
ms:contentKeyID: 48544285
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277580
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4efa4e92d7fab2dc8a4aae932ccb1ffe69c7c6c8
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026101"
---
# <a name="sql-subqueries-microsoft-access-sql"></a><span data-ttu-id="9a43d-102">Вложенные запросы SQL (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="9a43d-102">SQL subqueries (Microsoft Access SQL)</span></span>


<span data-ttu-id="9a43d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a43d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a43d-104">Вложенный запрос — это инструкция [SELECT](select-statement-microsoft-access-sql.md) , вложенных в SELECT, [SELECT... В](select-into-statement-microsoft-access-sql.md), [Вставка... В](insert-into-statement-microsoft-access-sql.md), [Удаление](delete-statement-microsoft-access-sql.md)или [обновление](update-statement-microsoft-access-sql.md) оператор или в другой вложенный запрос.</span><span class="sxs-lookup"><span data-stu-id="9a43d-104">A subquery is a [SELECT](select-statement-microsoft-access-sql.md) statement nested inside a SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md), or [UPDATE](update-statement-microsoft-access-sql.md) statement or inside another subquery.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a43d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a43d-105">Syntax</span></span>

<span data-ttu-id="9a43d-106">Чтобы создать вложенный запрос можно использовать три вида синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="9a43d-106">You can use three forms of syntax to create a subquery:</span></span>

<span data-ttu-id="9a43d-107">*Сравнение* \[ANY | ВСЕ | НЕКОТОРЫЕ\] (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="9a43d-107">*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)</span></span>

<span data-ttu-id="9a43d-108">*выражение* \[Не\] в (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="9a43d-108">*expression* \[NOT\] IN (*sqlstatement*)</span></span>

<span data-ttu-id="9a43d-109">\[НЕ\] EXISTS (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="9a43d-109">\[NOT\] EXISTS (*sqlstatement*)</span></span>

<span data-ttu-id="9a43d-110">Вложенный состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="9a43d-110">A subquery has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9a43d-111">Часть</span><span class="sxs-lookup"><span data-stu-id="9a43d-111">Part</span></span></p></th>
<th><p><span data-ttu-id="9a43d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9a43d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9a43d-113"><em>Сравнение</em></span><span class="sxs-lookup"><span data-stu-id="9a43d-113"><em>comparison</em></span></span></p></td>
<td><p><span data-ttu-id="9a43d-114">Выражение и оператор сравнения, сравнивает выражение с результатами подчиненного запроса.</span><span class="sxs-lookup"><span data-stu-id="9a43d-114">An expression and a comparison operator that compares the expression with the results of the subquery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a43d-115"><em>expression</em></span><span class="sxs-lookup"><span data-stu-id="9a43d-115"><em>expression</em></span></span></p></td>
<td><p><span data-ttu-id="9a43d-116">Выражение, для которого осуществляется в наборе результатов вложенного запроса.</span><span class="sxs-lookup"><span data-stu-id="9a43d-116">An expression for which the result set of the subquery is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a43d-117"><em>SQLStatement</em></span><span class="sxs-lookup"><span data-stu-id="9a43d-117"><em>sqlstatement</em></span></span></p></td>
<td><p><span data-ttu-id="9a43d-118">Инструкция SELECT, выполнив же формат и правила как любая другая инструкция SELECT.</span><span class="sxs-lookup"><span data-stu-id="9a43d-118">A SELECT statement, following the same format and rules as any other SELECT statement.</span></span> <span data-ttu-id="9a43d-119">Она должна быть включена в скобки.</span><span class="sxs-lookup"><span data-stu-id="9a43d-119">It must be enclosed in parentheses.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9a43d-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a43d-120">Remarks</span></span>

<span data-ttu-id="9a43d-121">Вложенный запрос можно использовать вместо выражения в списке полей инструкции SELECT или в предложении [ГДЕ](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) .</span><span class="sxs-lookup"><span data-stu-id="9a43d-121">You can use a subquery instead of an expression in the field list of a SELECT statement or in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause.</span></span> <span data-ttu-id="9a43d-122">Во вложенном запросе используйте инструкции SELECT для предоставления набора из одного или нескольких конкретных значений для оценки в WHERE или у выражения предложения.</span><span class="sxs-lookup"><span data-stu-id="9a43d-122">In a subquery, you use a SELECT statement to provide a set of one or more specific values to evaluate in the WHERE or HAVING clause expression.</span></span>

<span data-ttu-id="9a43d-123">С помощью предиката любой или НЕКОТОРЫЕ, которые являются синонимами, извлекаются записи в главном запросе, удовлетворяющие сравнению с любыми записями, полученные на вложенный запрос.</span><span class="sxs-lookup"><span data-stu-id="9a43d-123">Use the ANY or SOME predicate, which are synonymous, to retrieve records in the main query that satisfy the comparison with any records retrieved in the subquery.</span></span> <span data-ttu-id="9a43d-124">Следующий пример возвращает все продукты, цена больше, чем любого товара, проданных со скидкой от 25% и выше:</span><span class="sxs-lookup"><span data-stu-id="9a43d-124">The following example returns all products whose unit price is greater than that of any product sold at a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="9a43d-125">С помощью предиката [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) извлекаются только те записи в главном запросе, которые удовлетворяют сравнению со всех записей, полученных во вложенном.</span><span class="sxs-lookup"><span data-stu-id="9a43d-125">Use the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to retrieve only those records in the main query that satisfy the comparison with all records retrieved in the subquery.</span></span> <span data-ttu-id="9a43d-126">При изменении любой ко всем в предыдущем примере запрос возвращает только продукты, чьи цена больше всех продуктов, проданных со скидкой от 25% и выше.</span><span class="sxs-lookup"><span data-stu-id="9a43d-126">If you changed ANY to ALL in the previous example, the query would return only those products whose unit price is greater than that of all products sold at a discount of 25 percent or more.</span></span> <span data-ttu-id="9a43d-127">Это намного более жесткие.</span><span class="sxs-lookup"><span data-stu-id="9a43d-127">This is much more restrictive.</span></span>

<span data-ttu-id="9a43d-128">С помощью предиката IN извлекаются только те записи в главном запросе, для которого некоторые записи во вложенном содержат одинаковые значения.</span><span class="sxs-lookup"><span data-stu-id="9a43d-128">Use the IN predicate to retrieve only those records in the main query for which some record in the subquery contains an equal value.</span></span> <span data-ttu-id="9a43d-129">Следующий пример возвращает все продукты со скидкой 25 процентов или более:</span><span class="sxs-lookup"><span data-stu-id="9a43d-129">The following example returns all products with a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="9a43d-130">С другой стороны можно использовать NOT IN извлекаются только те записи в главном запросе, для которого нет записи во вложенном содержат одинаковые значения.</span><span class="sxs-lookup"><span data-stu-id="9a43d-130">Conversely, you can use NOT IN to retrieve only those records in the main query for which no record in the subquery contains an equal value.</span></span>

<span data-ttu-id="9a43d-131">Предикат EXISTS (с НЕОБЯЗАТЕЛЬНЫМ зарезервированным словом) при сравнении ИСТИНА/ЛОЖЬ для определения, является ли вложенный запрос возвращает все записи.</span><span class="sxs-lookup"><span data-stu-id="9a43d-131">Use the EXISTS predicate (with the optional NOT reserved word) in true/false comparisons to determine whether the subquery returns any records.</span></span>

<span data-ttu-id="9a43d-132">Можно также использовать псевдонимы таблиц во вложенном запросе для обращения к таблицам, перечисленных в предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) за пределами подчиненного запроса.</span><span class="sxs-lookup"><span data-stu-id="9a43d-132">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause outside the subquery.</span></span> <span data-ttu-id="9a43d-133">Следующий пример возвращает имена сотрудников, зарплата которых равно или больше средней заработной платы всех сотрудников, занимающих одну должность.</span><span class="sxs-lookup"><span data-stu-id="9a43d-133">The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title.</span></span> <span data-ttu-id="9a43d-134">В таблице сотрудников задается псевдоним «Т1».</span><span class="sxs-lookup"><span data-stu-id="9a43d-134">The Employees table is given the alias "T1":</span></span>

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

<span data-ttu-id="9a43d-135">В предыдущем примере зарезервированным словом является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a43d-135">In the preceding example, the AS reserved word is optional.</span></span>

<span data-ttu-id="9a43d-136">Некоторые подчиненные запросы разрешены в перекрестных запросов — только в качестве предикатов (в предложении WHERE).</span><span class="sxs-lookup"><span data-stu-id="9a43d-136">Some subqueries are allowed in crosstab queries— specifically, as predicates (those in the WHERE clause).</span></span> <span data-ttu-id="9a43d-137">Подчиненные запросы в качестве выходных данных (в списке SELECT) в перекрестных запросах не разрешены.</span><span class="sxs-lookup"><span data-stu-id="9a43d-137">Subqueries as output (those in the SELECT list) are not allowed in crosstab queries.</span></span>

## <a name="example"></a><span data-ttu-id="9a43d-138">Пример</span><span class="sxs-lookup"><span data-stu-id="9a43d-138">Example</span></span>

<span data-ttu-id="9a43d-139">В этом примере перечислены имя и контактов каждого клиента, выполнившим заказа во втором квартале 1995.</span><span class="sxs-lookup"><span data-stu-id="9a43d-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span></span> <span data-ttu-id="9a43d-140">Он вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="9a43d-140">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub SubQueryX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' List the name and contact of every customer  
        ' who placed an order in the second quarter of 
        ' 1995. 
        Set rst = dbs.OpenRecordset("SELECT ContactName," _ 
            & " CompanyName, ContactTitle, Phone" _ 
            & " FROM Customers" _ 
            & " WHERE CustomerID" _ 
            & " IN (SELECT CustomerID FROM Orders" _ 
            & " WHERE OrderDate Between #04/1/95#" _ 
            & " And #07/1/95#);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 25 
     
        dbs.Close 
     
    End Sub
```
