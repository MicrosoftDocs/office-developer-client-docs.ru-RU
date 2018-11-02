---
title: Присоединение к СЛЕВА, RIGHT JOIN операции (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: a16df1e26e4ab5617e6bf76aa93a11a936ccb49b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925900"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="32fa7-102">Присоединение к СЛЕВА, RIGHT JOIN операции (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="32fa7-102">LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="32fa7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="32fa7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32fa7-104">Объединяет записи исходных таблиц при использовании в [любой FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="32fa7-104">Combines source-table records when used in any [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="32fa7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32fa7-105">Syntax</span></span>

<span data-ttu-id="32fa7-106">ИЗ *table1* \[ влево | ПРАВО \] СОЕДИНЕНИЯ *Таблица2* на *Таблица1.поле1* *оператор_сравнения Таблица2.поле2*</span><span class="sxs-lookup"><span data-stu-id="32fa7-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span></span>

<span data-ttu-id="32fa7-107">Операции JOIN СЛЕВА и СПРАВА JOIN состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="32fa7-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32fa7-108">Часть</span><span class="sxs-lookup"><span data-stu-id="32fa7-108">Part</span></span></p></th>
<th><p><span data-ttu-id="32fa7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="32fa7-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32fa7-110"><em>table1</em>, <em>Таблица2</em></span><span class="sxs-lookup"><span data-stu-id="32fa7-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="32fa7-111">Имена таблиц, из которых объединяются записи.</span><span class="sxs-lookup"><span data-stu-id="32fa7-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32fa7-112"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="32fa7-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="32fa7-113">Имена полей, входящих в состав.</span><span class="sxs-lookup"><span data-stu-id="32fa7-113">The names of the fields that are joined.</span></span> <span data-ttu-id="32fa7-114">Поля должны быть тот же тип данных и содержат одинаковые данные, но они не нужно с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="32fa7-114">The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32fa7-115"><em>оператор_сравнения</em></span><span class="sxs-lookup"><span data-stu-id="32fa7-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="32fa7-116">Любой оператор сравнения: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; или &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="32fa7-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="32fa7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="32fa7-117">Remarks</span></span>

<span data-ttu-id="32fa7-118">Используйте операцию LEFT JOIN для создания левого внешнего соединения.</span><span class="sxs-lookup"><span data-stu-id="32fa7-118">Use a LEFT JOIN operation to create a left outer join.</span></span> <span data-ttu-id="32fa7-119">Левые внешние соединения включают все записи из первой (левой) таблицы, даже если нет совпадающих значений для записей в таблице второй (справа).</span><span class="sxs-lookup"><span data-stu-id="32fa7-119">Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="32fa7-120">Используйте операцию RIGHT JOIN для создания правого внешнего соединения.</span><span class="sxs-lookup"><span data-stu-id="32fa7-120">Use a RIGHT JOIN operation to create a right outer join.</span></span> <span data-ttu-id="32fa7-121">Правые внешние соединения включают все записи из второй (правой) таблицы, даже в том случае, если нет совпадающих значений для записей в таблице первой (левой).</span><span class="sxs-lookup"><span data-stu-id="32fa7-121">Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="32fa7-122">Например можно использовать LEFT JOIN с отделов (слева) и сотрудникам (справа) таблицы для выбора всех отделов, включая те, которые не имеют сотрудников им.</span><span class="sxs-lookup"><span data-stu-id="32fa7-122">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them.</span></span> <span data-ttu-id="32fa7-123">Чтобы выбрать всех сотрудников, включая те, кто не назначается отдел, используйте RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="32fa7-123">To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="32fa7-124">В следующем примере показано, как можно объединить таблицы категорий и продуктов в поле Идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="32fa7-124">The following example shows how you could join the Categories and Products tables on the CategoryID field.</span></span> <span data-ttu-id="32fa7-125">Запрос создает список всех типов, включая те, которые не содержат товаров:</span><span class="sxs-lookup"><span data-stu-id="32fa7-125">The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="32fa7-126">В этом примере идентификатор категории — это поле объединения, но не включенный в результатах запроса, так как он не включен в операторе [SELECT](select-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="32fa7-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="32fa7-127">Чтобы включить поле объединения, введите имя поля в операторе SELECT — в данном случае Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="32fa7-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="32fa7-128">Чтобы создать запрос, который включает в себя только записей, в которых данные в полях соединения зависит от того, используйте операцию [INNER JOIN](inner-join-operation-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="32fa7-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="32fa7-129">LEFT JOIN или RIGHT JOIN может быть вложенным в ВНУТРЕННЕЕ соединение, но ВНУТРЕННЕЕ соединение, не могут быть вложенными внутри LEFT JOIN или RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="32fa7-129">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span> <span data-ttu-id="32fa7-130">В разделе обсуждения вложения в разделе INNER JOIN, чтобы узнать, как вложить объединения.</span><span class="sxs-lookup"><span data-stu-id="32fa7-130">See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="32fa7-131">Можно связать несколько предложений ON.</span><span class="sxs-lookup"><span data-stu-id="32fa7-131">You can link multiple ON clauses.</span></span> <span data-ttu-id="32fa7-132">В разделе обсуждения ссылки в разделе INNER JOIN, чтобы узнать, как это делается предложение.</span><span class="sxs-lookup"><span data-stu-id="32fa7-132">See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="32fa7-133">При попытке объединить поля, содержащие данные Memo или OLE-объектов, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="32fa7-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="32fa7-134">Пример</span><span class="sxs-lookup"><span data-stu-id="32fa7-134">Example</span></span>

<span data-ttu-id="32fa7-135">В этом примере:</span><span class="sxs-lookup"><span data-stu-id="32fa7-135">This example:</span></span>
- <span data-ttu-id="32fa7-136">Предполагается наличие предполагаемую имя отдела и отдела идентификатор поля в таблице «Сотрудники».</span><span class="sxs-lookup"><span data-stu-id="32fa7-136">Assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="32fa7-137">Обратите внимание на то, что фактически эти поля не существуют в таблице Employees базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="32fa7-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="32fa7-138">Выбирает все отделы, в том числе без сотрудников.</span><span class="sxs-lookup"><span data-stu-id="32fa7-138">Selects all departments, including those without employees.</span></span>

- <span data-ttu-id="32fa7-139">Вызывает процедуру EnumFields, которые можно найти в примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="32fa7-139">Calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>


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
