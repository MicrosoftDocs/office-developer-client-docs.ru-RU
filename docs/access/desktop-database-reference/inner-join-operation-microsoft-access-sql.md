---
title: Операция INNER JOIN (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: d865d005604ed7422c8e33ff8508551b720c30ba
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734219"
---
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="1bed6-102">Операция INNER JOIN (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1bed6-102">INNER JOIN operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="1bed6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1bed6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1bed6-104">Объединяет записи из двух таблиц, если в связующих полях этих таблиц содержатся одинаковые значения.</span><span class="sxs-lookup"><span data-stu-id="1bed6-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bed6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bed6-105">Syntax</span></span>

<span data-ttu-id="1bed6-106">FROM *таблица1* INNER JOIN *таблица2* ON *таблица1*.*поле1* *оператор_сравнения таблица2*.*поле2*</span><span class="sxs-lookup"><span data-stu-id="1bed6-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span></span>

<span data-ttu-id="1bed6-107">Операция INNER JOIN состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="1bed6-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1bed6-108">Часть</span><span class="sxs-lookup"><span data-stu-id="1bed6-108">Part</span></span></p></th>
<th><p><span data-ttu-id="1bed6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1bed6-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1bed6-110"><em>таблица1</em>, <em>таблица2</em></span><span class="sxs-lookup"><span data-stu-id="1bed6-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="1bed6-111">Имена таблиц, содержащих объединяемые записи.</span><span class="sxs-lookup"><span data-stu-id="1bed6-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1bed6-112"><em>поле1</em>, <em>поле2</em></span><span class="sxs-lookup"><span data-stu-id="1bed6-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="1bed6-113">Имена объединяемых полей.</span><span class="sxs-lookup"><span data-stu-id="1bed6-113">The names of the fields that are joined.</span></span> <span data-ttu-id="1bed6-114">Поля, не являющиеся числовыми, должны относиться к одному типу данных и содержать данные одного вида. Однако имена этих полей могут быть разными.</span><span class="sxs-lookup"><span data-stu-id="1bed6-114">If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1bed6-115"><em>оператор_сравнения</em></span><span class="sxs-lookup"><span data-stu-id="1bed6-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="1bed6-116">Любой оператор сравнения: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; или &quot;&lt;&gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="1bed6-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1bed6-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="1bed6-117">Remarks</span></span>

<span data-ttu-id="1bed6-118">Операцию INNER JOIN можно использовать в любом предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="1bed6-118">You can use an INNER JOIN operation in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause.</span></span> <span data-ttu-id="1bed6-119">Это самый распространенный тип объединения.</span><span class="sxs-lookup"><span data-stu-id="1bed6-119">This is the most common type of join.</span></span> <span data-ttu-id="1bed6-120">С его помощью происходит объединение записей из двух таблиц по связующему полю, если оно содержит одинаковые значения в обеих таблицах.</span><span class="sxs-lookup"><span data-stu-id="1bed6-120">Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="1bed6-121">При работе с таблицами "Отделы" и "Сотрудники" операцией INNER JOIN можно воспользоваться для выбора всех сотрудников в каждом отделе.</span><span class="sxs-lookup"><span data-stu-id="1bed6-121">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department.</span></span> <span data-ttu-id="1bed6-122">Если же требуется выбрать все отделы (включая те из них, в которых нет сотрудников) или всех сотрудников (в том числе и не закрепленных за отделом), можно при помощи операции [LEFT JOIN или RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) создать внешнее соединение.</span><span class="sxs-lookup"><span data-stu-id="1bed6-122">In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="1bed6-123">При попытке связи полей, содержащих данные типа Memo или объекты OLE, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="1bed6-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="1bed6-124">Можно связать любые два числовых поля аналогичных типов.</span><span class="sxs-lookup"><span data-stu-id="1bed6-124">You can join any two numeric fields of like types.</span></span> <span data-ttu-id="1bed6-125">Например, можно связать поля AutoNumber и Long, так как эти типы аналогичны,</span><span class="sxs-lookup"><span data-stu-id="1bed6-125">For example, you can join on AutoNumber and Long fields because they are like types.</span></span> <span data-ttu-id="1bed6-126">однако не поля Single и Double.</span><span class="sxs-lookup"><span data-stu-id="1bed6-126">However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="1bed6-127">В следующем примере показано, как можно объединить таблицы Categories и Products по полю CategoryID.</span><span class="sxs-lookup"><span data-stu-id="1bed6-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="1bed6-128">В предыдущем примере CategoryID является объединенным полем, но оно не включается в результаты запроса, поскольку не указано в инструкции [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="1bed6-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="1bed6-129">Чтобы включить объединенное поле в результаты запроса, добавьте его имя в инструкцию SELECT. В данном случае это Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="1bed6-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="1bed6-130">В инструкции JOIN можно также связать несколько предложений ON, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="1bed6-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="1bed6-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;</span><span class="sxs-lookup"><span data-stu-id="1bed6-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;</span></span>

<span data-ttu-id="1bed6-132">Ниже приведен пример синтаксиса, с помощью которого можно составлять вложенные инструкции JOIN.</span><span class="sxs-lookup"><span data-stu-id="1bed6-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="1bed6-133">SELECT *поля* FROM *таблица1* INNER JOIN (*таблица2* INNER JOIN \[( \]*таблица3* \[INNER JOIN \[( \]*таблицаx* \[INNER JOIN …)\] ON *таблица3*.*поле3* *оператор_сравнения* *таблицаx*.*полеx*)\] ON *таблица2*.*поле2* *оператор_сравнения* *таблица3*.*поле3*) ON *таблица1*.*поле1* *оператор_сравнения* *таблица2*.*поле2*;</span><span class="sxs-lookup"><span data-stu-id="1bed6-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span></span>

<span data-ttu-id="1bed6-134">Операции LEFT JOIN и RIGHT JOIN могут быть вложены в операцию INNER JOIN, но операция INNER JOIN не может быть вложена в операцию LEFT JOIN или RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="1bed6-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="1bed6-135">Пример</span><span class="sxs-lookup"><span data-stu-id="1bed6-135">Example</span></span>

<span data-ttu-id="1bed6-136">В этом примере создается два уравнивающих соединения: одно между таблицами Order Details (Сведения о заказах) и Orders (Заказы), а другое между таблицами Orders (Заказы) и Employees (Сотрудники).</span><span class="sxs-lookup"><span data-stu-id="1bed6-136">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables.</span></span> <span data-ttu-id="1bed6-137">Это необходимо, так как таблица Employees (Сотрудники) не содержит данные о продажах, а таблица Order Details (Сведения о заказах) не содержит данные сотрудников.</span><span class="sxs-lookup"><span data-stu-id="1bed6-137">This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data.</span></span> <span data-ttu-id="1bed6-138">Результат запроса представляет собой список сотрудников и их общие объемы продаж.</span><span class="sxs-lookup"><span data-stu-id="1bed6-138">The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="1bed6-139">В этом примере вызывается процедура EnumFields, которую можно найти в примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="1bed6-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
