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
localization_priority: Priority
ms.openlocfilehash: 7beda04d1f18014101f00078de1d125c1fd67a69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314569"
---
# <a name="sql-subqueries-microsoft-access-sql"></a><span data-ttu-id="c7e53-102">Вложенные запросы SQL (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c7e53-102">SQL Subqueries (Microsoft Access SQL)</span></span>


<span data-ttu-id="c7e53-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7e53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7e53-104">Вложенный запрос - это оператор [SELECT](select-statement-microsoft-access-sql.md), вложенный в оператор [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) или [UPDATE](update-statement-microsoft-access-sql.md) или в другой вложенный запрос.</span><span class="sxs-lookup"><span data-stu-id="c7e53-104">A subquery is a [SELECT](select-statement-microsoft-access-sql.md) statement nested inside a SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md), or [UPDATE](update-statement-microsoft-access-sql.md) statement or inside another subquery.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7e53-105">Syntax</span></span>

<span data-ttu-id="c7e53-106">Вы можете использовать три формы синтаксиса для создания вложенного запроса:</span><span class="sxs-lookup"><span data-stu-id="c7e53-106">You can use three forms of syntax to create a subquery:</span></span>

<span data-ttu-id="c7e53-107">*сравнение* \[ANY | ALL | SOME \] (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="c7e53-107">*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)</span></span>

<span data-ttu-id="c7e53-108">*выражение* \[NOT\] IN (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="c7e53-108">*expression* \[NOT\] IN (*sqlstatement*)</span></span>

<span data-ttu-id="c7e53-109">\[NOT\] EXISTS (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="c7e53-109">\[NOT\] EXISTS (*sqlstatement*)</span></span>

<span data-ttu-id="c7e53-110">Вложенный запрос состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="c7e53-110">A subquery has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7e53-111">Часть</span><span class="sxs-lookup"><span data-stu-id="c7e53-111">Part</span></span></p></th>
<th><p><span data-ttu-id="c7e53-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c7e53-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7e53-113"><em>сравнение</em></span><span class="sxs-lookup"><span data-stu-id="c7e53-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="c7e53-114">Выражение и оператор сравнения, который сравнивает выражение с результатами вложенного запроса.</span><span class="sxs-lookup"><span data-stu-id="c7e53-114">An expression and a comparison operator that compares the expression with the results of the subquery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7e53-115"><em>выражение</em></span><span class="sxs-lookup"><span data-stu-id="c7e53-115"><em>expression</em></span></span></p></td>
<td><p><span data-ttu-id="c7e53-116">Выражение, для которого выполняется поиск по набору результатов для вложенного запроса.</span><span class="sxs-lookup"><span data-stu-id="c7e53-116">An expression for which the result set of the subquery is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7e53-117"><em>sqlstatement</em></span><span class="sxs-lookup"><span data-stu-id="c7e53-117"><em>sqlstatement</em></span></span></p></td>
<td><p><span data-ttu-id="c7e53-118">Оператор SELECT с тем же форматом и правилами, что и любой другой оператор SELECT.</span><span class="sxs-lookup"><span data-stu-id="c7e53-118">A SELECT statement, following the same format and rules as any other SELECT statement.</span></span> <span data-ttu-id="c7e53-119">Его необходимо включать в скобки.</span><span class="sxs-lookup"><span data-stu-id="c7e53-119">It must be enclosed in parentheses.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c7e53-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7e53-120">Remarks</span></span>

<span data-ttu-id="c7e53-121">Вы можете использовать вложенный запрос вместо выражения в списке полей оператора SELECT или предложении [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="c7e53-121">You can use a subquery instead of an expression in the field list of a SELECT statement or in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause.</span></span> <span data-ttu-id="c7e53-122">Во вложенном запросе вы используете оператор SELECT для предоставления набора одного или нескольких определенных значений для оценки в выражении для предложения WHERE или HAVING.</span><span class="sxs-lookup"><span data-stu-id="c7e53-122">In a subquery, you use a SELECT statement to provide a set of one or more specific values to evaluate in the WHERE or HAVING clause expression.</span></span>

<span data-ttu-id="c7e53-123">Используйте предикат ANY или SOME, которые являются синонимами, для получения записей в основном запросе, который удовлетворяет сравнению с любыми записями, полученными во вложенном запросе.</span><span class="sxs-lookup"><span data-stu-id="c7e53-123">Use the ANY or SOME predicate, which are synonymous, to retrieve records in the main query that satisfy the comparison with any records retrieved in the subquery.</span></span> <span data-ttu-id="c7e53-124">Следующий пример возвращает все продукты, для которых цена за единицу выше, чем у любого продукта, продаваемого со скидкой 25 процентов или более:</span><span class="sxs-lookup"><span data-stu-id="c7e53-124">The following example returns all products whose unit price is greater than that of any product sold at a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="c7e53-125">Используйте предикат [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) для получения записей в основном запросе, который удовлетворяет сравнению со всеми записями, полученными во вложенном запросе.</span><span class="sxs-lookup"><span data-stu-id="c7e53-125">Use the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to retrieve only those records in the main query that satisfy the comparison with all records retrieved in the subquery.</span></span> <span data-ttu-id="c7e53-126">Если вы изменили предикат с ANY на ALL в предыдущем примере, запрос будет возвращать только те продукты, у которых цена за единицу больше, чем у всех продуктов, проданных со скидкой 25 процентов или более.</span><span class="sxs-lookup"><span data-stu-id="c7e53-126">If you changed ANY to ALL in the previous example, the query would return only those products whose unit price is greater than that of all products sold at a discount of 25 percent or more.</span></span> <span data-ttu-id="c7e53-127">Это гораздо более строгое ограничение.</span><span class="sxs-lookup"><span data-stu-id="c7e53-127">This is much more restrictive.</span></span>

<span data-ttu-id="c7e53-128">Используйте предикат IN для получения только тех записей в основном запросе, для которых определенная запись во вложенном запросе содержит одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="c7e53-128">Use the IN predicate to retrieve only those records in the main query for which some record in the subquery contains an equal value.</span></span> <span data-ttu-id="c7e53-129">В примере ниже возвращаются все продукты со скидкой 25 процентов или больше:</span><span class="sxs-lookup"><span data-stu-id="c7e53-129">The following example returns all products with a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="c7e53-130">С другой стороны, вы можете использовать NOT IN для получения только тех записей в основном запросе, для которых ни одна запись во вложенном запросе не содержит одинаковое значение.</span><span class="sxs-lookup"><span data-stu-id="c7e53-130">Conversely, you can use NOT IN to retrieve only those records in the main query for which no record in the subquery contains an equal value.</span></span>

<span data-ttu-id="c7e53-131">Используйте предикат EXISTS (с необязательным зарезервированным словом NOT) в сравнениях ИСТИНА/ЛОЖЬ, чтобы определить, возвращает ли вложенный запрос какие-либо записи.</span><span class="sxs-lookup"><span data-stu-id="c7e53-131">Use the EXISTS predicate (with the optional NOT reserved word) in true/false comparisons to determine whether the subquery returns any records.</span></span>

<span data-ttu-id="c7e53-132">Также можно использовать псевдонимы имени таблицы во вложенном запросе для ссылки на таблицы, указанные в предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) за пределами вложенного запроса.</span><span class="sxs-lookup"><span data-stu-id="c7e53-132">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause outside the subquery.</span></span> <span data-ttu-id="c7e53-133">Пример ниже возвращает имена сотрудников, чья заработная плата равна или выше средней заработной платы всех сотрудников на аналогичной должности.</span><span class="sxs-lookup"><span data-stu-id="c7e53-133">The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title.</span></span> <span data-ttu-id="c7e53-134">Для таблицы "Сотрудники" присваивается псевдоним "T1":</span><span class="sxs-lookup"><span data-stu-id="c7e53-134">The Employees table is given the alias "T1":</span></span>

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

<span data-ttu-id="c7e53-135">В приведенном выше примере зарезервированное слово AS не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c7e53-135">In the preceding example, the AS reserved word is optional.</span></span>

<span data-ttu-id="c7e53-136">Некоторые вложенные запросы поддерживаются в перекрестных запросах, в частности, в качестве предикатов (например в предложении WHERE).</span><span class="sxs-lookup"><span data-stu-id="c7e53-136">Some subqueries are allowed in crosstab queries— specifically, as predicates (those in the WHERE clause).</span></span> <span data-ttu-id="c7e53-137">Вложенные запросы в виде выходных данных (в списке SELECT) не поддерживаются в перекрестных запросах.</span><span class="sxs-lookup"><span data-stu-id="c7e53-137">Subqueries as output (those in the SELECT list) are not allowed in crosstab queries.</span></span>

## <a name="example"></a><span data-ttu-id="c7e53-138">Пример</span><span class="sxs-lookup"><span data-stu-id="c7e53-138">Example</span></span>

<span data-ttu-id="c7e53-139">В данном примере перечислены имена и контактные данные каждого клиента, разместившего заказ во втором квартале 1995 года.</span><span class="sxs-lookup"><span data-stu-id="c7e53-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span></span> <span data-ttu-id="c7e53-140">В этом примере выполняется вызов процедуры EnumFields, которую можно найти в примере для оператора SELECT.</span><span class="sxs-lookup"><span data-stu-id="c7e53-140">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
