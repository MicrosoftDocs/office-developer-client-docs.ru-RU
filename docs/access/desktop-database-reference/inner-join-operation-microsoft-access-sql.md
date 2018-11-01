---
title: INNER JOIN Operation (Microsoft Access SQL)
TOCTitle: INNER JOIN Operation (Microsoft Access SQL)
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
ms.openlocfilehash: 874f685a1db38c4a381f08289cb0c612e7e2eb4c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888897"
---
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="b4a58-102">INNER JOIN Operation (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b4a58-102">INNER JOIN Operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="b4a58-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4a58-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b4a58-104">Объединяет записи из двух таблиц при каждом содержат одинаковые значения общего поля.</span><span class="sxs-lookup"><span data-stu-id="b4a58-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a58-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4a58-105">Syntax</span></span>

<span data-ttu-id="b4a58-106">ИЗ внутреннего СОЕДИНЕНИЯ *table1* *Таблица2* на *table1*. *field1* *оператор_сравнения Таблица2*. *поле2*</span><span class="sxs-lookup"><span data-stu-id="b4a58-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span></span>

<span data-ttu-id="b4a58-107">Операция INNER JOIN состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="b4a58-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4a58-108">Часть</span><span class="sxs-lookup"><span data-stu-id="b4a58-108">Part</span></span></p></th>
<th><p><span data-ttu-id="b4a58-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b4a58-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4a58-110"><em>table1</em>, <em>Таблица2</em></span><span class="sxs-lookup"><span data-stu-id="b4a58-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="b4a58-111">Имена таблиц, из которых объединяются записи.</span><span class="sxs-lookup"><span data-stu-id="b4a58-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a58-112"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="b4a58-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="b4a58-113">Имена полей, входящих в состав.</span><span class="sxs-lookup"><span data-stu-id="b4a58-113">The names of the fields that are joined.</span></span> <span data-ttu-id="b4a58-114">Если они не числовое, поля должны быть тот же тип данных и содержат одинаковые данные, но нет необходимости с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="b4a58-114">If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a58-115"><em>оператор_сравнения</em></span><span class="sxs-lookup"><span data-stu-id="b4a58-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="b4a58-116">Любой оператор сравнения: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; или &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="b4a58-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b4a58-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="b4a58-117">Remarks</span></span>

<span data-ttu-id="b4a58-118">Можно использовать операцию INNER JOIN в [любой FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="b4a58-118">You can use an INNER JOIN operation in any [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause.</span></span> <span data-ttu-id="b4a58-119">Это наиболее распространенный тип объединения.</span><span class="sxs-lookup"><span data-stu-id="b4a58-119">This is the most common type of join.</span></span> <span data-ttu-id="b4a58-120">Объединение записей из двух таблиц всякий раз, когда они соответствуют в поле обеих таблицах.</span><span class="sxs-lookup"><span data-stu-id="b4a58-120">Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="b4a58-121">Можно использовать INNER JOIN с таблицами отделов и сотрудников для выбора всех сотрудников в каждого подразделения.</span><span class="sxs-lookup"><span data-stu-id="b4a58-121">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department.</span></span> <span data-ttu-id="b4a58-122">С другой стороны чтобы выбрать все отделы (даже если некоторые имеют нет сотрудников) или всех сотрудников (даже если некоторые не назначены отделом), можно использовать операцию [LEFT JOIN или RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) для создания внешнего соединения.</span><span class="sxs-lookup"><span data-stu-id="b4a58-122">In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="b4a58-123">При попытке объединить поля, содержащие данные Memo или OLE-объектов, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b4a58-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="b4a58-124">Можно объединить два числовых поля из как типы.</span><span class="sxs-lookup"><span data-stu-id="b4a58-124">You can join any two numeric fields of like types.</span></span> <span data-ttu-id="b4a58-125">Например можно объединить для счетчика и много полей, так как они являются как типы.</span><span class="sxs-lookup"><span data-stu-id="b4a58-125">For example, you can join on AutoNumber and Long fields because they are like types.</span></span> <span data-ttu-id="b4a58-126">Тем не менее не может присоединиться к Single и Double типов полей.</span><span class="sxs-lookup"><span data-stu-id="b4a58-126">However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="b4a58-127">В следующем примере показано, как можно объединить таблицы категорий и продуктов в поле Идентификатор категории:</span><span class="sxs-lookup"><span data-stu-id="b4a58-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="b4a58-128">В предыдущем примере идентификатор категории — это поле объединения, но не включенный в выходных данных запроса, так как он не включен в операторе [SELECT](select-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a58-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="b4a58-129">Чтобы включить поле объединения, добавьте имя поля в операторе SELECT — в данном случае Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="b4a58-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="b4a58-130">Также можно связать несколько предложений ON в операторе JOIN, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="b4a58-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="b4a58-131">ВЫБЕРИТЕ из *поля* *table1* INNER JOIN *Таблица2* д *table1*. *field1* *оператор_сравнения* *Таблица2*. *field1* И на *table1*. *поле2* *оператор_сравнения* *Таблица2*. *поле2*) ИЛИ на *table1*. *поле3* *оператор_сравнения* *Таблица2*. *поле3*) \];</span><span class="sxs-lookup"><span data-stu-id="b4a58-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND ON *table1*.*field2* *compopr* *table2*.*field2*) OR ON *table1*.*field3* *compopr* *table2*.*field3*)\];</span></span>

<span data-ttu-id="b4a58-132">Кроме того, можно вкладывать инструкций СОЕДИНЕНИЯ, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="b4a58-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="b4a58-133">ВЫБЕРИТЕ из *поля* *table1* INNER JOIN (*Таблица2* INNER JOIN \[( \] *Таблица3* \[INNER JOIN \[( \] *tablex* \[INNER JOIN...) \] На *Таблица3*. *поле3* *оператор_сравнения* *tablex*. *fieldx*) \] На *Таблица2*. *поле2* *оператор_сравнения* *Таблица3*. *поле3*) НА *table1*. *field1* *оператор_сравнения* *Таблица2*. *поле2*;</span><span class="sxs-lookup"><span data-stu-id="b4a58-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span></span>

<span data-ttu-id="b4a58-134">LEFT JOIN или RIGHT JOIN может быть вложена в ВНУТРЕННЕЕ соединение, но ВНУТРЕННЕЕ соединение не могут быть вложены внутри LEFT JOIN или RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="b4a58-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="b4a58-135">Пример</span><span class="sxs-lookup"><span data-stu-id="b4a58-135">Example</span></span>

<span data-ttu-id="b4a58-136">В этом примере создается два эквивалентные соединения: один между сведения о заказе и заказы таблиц между таблицами заказы и сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b4a58-136">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables.</span></span> <span data-ttu-id="b4a58-137">Это необходимо, так как в таблице сотрудников не содержит данные о продажах и в таблице сведения о заказе не содержит данные о сотрудниках.</span><span class="sxs-lookup"><span data-stu-id="b4a58-137">This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data.</span></span> <span data-ttu-id="b4a58-138">Запрос создает список сотрудников и общего объема продаж.</span><span class="sxs-lookup"><span data-stu-id="b4a58-138">The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="b4a58-139">В этом примере вызывается процедура EnumFields, которые можно найти в примере инструкции SELECT.</span><span class="sxs-lookup"><span data-stu-id="b4a58-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
