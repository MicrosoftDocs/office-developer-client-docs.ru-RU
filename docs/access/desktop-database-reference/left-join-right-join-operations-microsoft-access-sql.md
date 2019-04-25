---
title: Операции LEFT JOIN, RIGHT JOIN (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: c6e37cd68d586e39a06fd650ccb453f35477253f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290147"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="8d985-102">Операции LEFT JOIN, RIGHT JOIN (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="8d985-102">LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="8d985-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d985-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d985-104">Объединяют записи исходных таблиц при использовании в любом предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="8d985-104">Combines source-table records when used in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d985-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d985-105">Syntax</span></span>

<span data-ttu-id="8d985-106">FROM *таблица1* \[ LEFT | RIGHT \] JOIN *таблица2* ON *таблица1.поле1* *оператор_сравнения таблица2.поле2*</span><span class="sxs-lookup"><span data-stu-id="8d985-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span></span>

<span data-ttu-id="8d985-107">Операции LEFT JOIN и RIGHT JOIN состоят из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="8d985-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d985-108">Часть</span><span class="sxs-lookup"><span data-stu-id="8d985-108">Part</span></span></p></th>
<th><p><span data-ttu-id="8d985-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8d985-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d985-110"><em>таблица1</em>, <em>таблица2</em></span><span class="sxs-lookup"><span data-stu-id="8d985-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="8d985-111">Имена таблиц, содержащих объединяемые записи.</span><span class="sxs-lookup"><span data-stu-id="8d985-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d985-112"><em>поле1</em>, <em>поле2</em></span><span class="sxs-lookup"><span data-stu-id="8d985-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="8d985-113">Имена объединяемых полей.</span><span class="sxs-lookup"><span data-stu-id="8d985-113">The names of the fields that are joined.</span></span> <span data-ttu-id="8d985-114">Поля должны относиться к одному типу данных и содержать данные одного вида. Однако имена этих полей могут быть разными.</span><span class="sxs-lookup"><span data-stu-id="8d985-114">The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d985-115"><em>оператор_сравнения</em></span><span class="sxs-lookup"><span data-stu-id="8d985-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="8d985-116">Любой оператор сравнения: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; или &quot;&lt;&gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="8d985-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8d985-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d985-117">Remarks</span></span>

<span data-ttu-id="8d985-118">Операция LEFT JOIN создает левое внешнее соединение.</span><span class="sxs-lookup"><span data-stu-id="8d985-118">Use a LEFT JOIN operation to create a left outer join.</span></span> <span data-ttu-id="8d985-119">С помощью левого внешнего соединения выбираются все записи первой (левой) таблицы, даже если они не соответствуют записям во второй (правой) таблице.</span><span class="sxs-lookup"><span data-stu-id="8d985-119">Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="8d985-120">Операция RIGHT JOIN создает правое внешнее соединение.</span><span class="sxs-lookup"><span data-stu-id="8d985-120">Use a RIGHT JOIN operation to create a right outer join.</span></span> <span data-ttu-id="8d985-121">С помощью правого внешнего соединения выбираются все записи второй (правой) таблицы, даже если они не соответствуют записям в первой (левой) таблице.</span><span class="sxs-lookup"><span data-stu-id="8d985-121">Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="8d985-122">Например, в случае с таблицами "Отделы" (левая) и "Сотрудники" (правая) можно воспользоваться операцией LEFT JOIN для выбора всех отделов (включая те, в которых нет сотрудников).</span><span class="sxs-lookup"><span data-stu-id="8d985-122">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them.</span></span> <span data-ttu-id="8d985-123">Чтобы выбрать всех сотрудников (в том числе и не закрепленных за каким-либо отделом), используйте RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="8d985-123">To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="8d985-124">В следующем примере показано, как можно объединить таблицы Categories и Products по полю CategoryID.</span><span class="sxs-lookup"><span data-stu-id="8d985-124">The following example shows how you could join the Categories and Products tables on the CategoryID field.</span></span> <span data-ttu-id="8d985-125">Результат запроса представляет собой список категорий, включая те, которые не содержат товаров.</span><span class="sxs-lookup"><span data-stu-id="8d985-125">The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="8d985-126">В этом примере CategoryID является объединенным полем, но оно не включается в результаты запроса, поскольку не указано в инструкции [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="8d985-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="8d985-127">Чтобы включить объединенное поле в результаты запроса, укажите его имя в инструкции SELECT. В данном случае это Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="8d985-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="8d985-128">Чтобы создать запрос, результатом которого являются только те записи, для которых совпадают данные в объединенных полях, воспользуйтесь операцией [INNER JOIN](inner-join-operation-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="8d985-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="8d985-129">Операции LEFT JOIN и RIGHT JOIN могут быть вложены в операцию INNER JOIN, но операция INNER JOIN не может быть вложена в операцию LEFT JOIN или RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="8d985-129">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span> <span data-ttu-id="8d985-130">Подробные сведения о вложении объединений можно найти в статье, посвященной операции INNER JOIN.</span><span class="sxs-lookup"><span data-stu-id="8d985-130">See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="8d985-131">Вы можете связать несколько предложений ON.</span><span class="sxs-lookup"><span data-stu-id="8d985-131">You can link multiple ON clauses.</span></span> <span data-ttu-id="8d985-132">Сведения о связывании предложений см. в статье, посвященной операции INNER JOIN.</span><span class="sxs-lookup"><span data-stu-id="8d985-132">See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="8d985-133">При попытке связи полей, содержащих данные типа Memo или объекты OLE, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="8d985-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="8d985-134">Пример</span><span class="sxs-lookup"><span data-stu-id="8d985-134">Example</span></span>

<span data-ttu-id="8d985-135">В этом примере:</span><span class="sxs-lookup"><span data-stu-id="8d985-135">This example sets</span></span>
- <span data-ttu-id="8d985-136">Предполагается существование гипотетических полей Department Name (Название отдела) и Department ID (Код отдела) в таблице Employees (Сотрудники).</span><span class="sxs-lookup"><span data-stu-id="8d985-136">Assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="8d985-137">Обратите внимание, что эти поля на самом деле не существуют в таблице Employees (Сотрудники) базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="8d985-137">Note that this field does not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="8d985-138">Выбираются все отделы, в том числе без сотрудников.</span><span class="sxs-lookup"><span data-stu-id="8d985-138">Selects all departments, including those without employees.</span></span>

- <span data-ttu-id="8d985-139">Выполняется вызов процедуры EnumFields, которую можно найти в примере для инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="8d985-139">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
