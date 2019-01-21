---
title: Оператор SELECT (Microsoft Access SQL)
TOCTitle: SELECT statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 10/18/2018
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: 962e425c2c69511b6d7770fb03e954588249cf2a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718786"
---
# <a name="select-statement-microsoft-access-sql"></a><span data-ttu-id="74f33-102">Оператор SELECT (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="74f33-102">SELECT Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="74f33-103">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="74f33-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="74f33-104">Указывает ядру СУБД Microsoft Access возвращать информацию из базы данных в виде наборе записей.</span><span class="sxs-lookup"><span data-stu-id="74f33-104">Instructs the Microsoft Access database engine to return information from the database as a set of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="74f33-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74f33-105">Syntax</span></span>

<span data-ttu-id="74f33-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span><span class="sxs-lookup"><span data-stu-id="74f33-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span></span> <span data-ttu-id="74f33-107">\] \[GROUP BY…</span><span class="sxs-lookup"><span data-stu-id="74f33-107">GROUP BY</span></span> <span data-ttu-id="74f33-108">\] \[HAVING…</span><span class="sxs-lookup"><span data-stu-id="74f33-108">HAVING</span></span> <span data-ttu-id="74f33-109">\] \[ORDER BY…</span><span class="sxs-lookup"><span data-stu-id="74f33-109">ORDER BY</span></span> <span data-ttu-id="74f33-110">\] \[WITH OWNERACCESS OPTION\]</span><span class="sxs-lookup"><span data-stu-id="74f33-110">WITH OWNERACCESS OPTION declaration</span></span>

<span data-ttu-id="74f33-111">Оператор SELECT состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="74f33-111">The For…Next statement syntax has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="74f33-112">Часть</span><span class="sxs-lookup"><span data-stu-id="74f33-112">Part</span></span></p></th>
<th><p><span data-ttu-id="74f33-113">Описание</span><span class="sxs-lookup"><span data-stu-id="74f33-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74f33-114"><em>predicate</em></span><span class="sxs-lookup"><span data-stu-id="74f33-114"><em>predicate</em></span></span></p></td>
<td><p><span data-ttu-id="74f33-115">Одно из следующих предикатов: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW, or TOP</a></span><span class="sxs-lookup"><span data-stu-id="74f33-115">One of the following predicates: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW, or TOP</a>.</span></span> <span data-ttu-id="74f33-116">Вы можете использовать предикаты для ограничения числа возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="74f33-116">You use the predicate to restrict the number of records returned.</span></span> <span data-ttu-id="74f33-117">Если ничего не указано, значение по умолчанию ALL.</span><span class="sxs-lookup"><span data-stu-id="74f33-117">If none is specified, the default is ALL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p><span data-ttu-id="74f33-118">Указывает, что все поля из указанной таблицы или таблиц выбраны.</span><span class="sxs-lookup"><span data-stu-id="74f33-118">Specifies that all fields from the specified table or tables are selected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f33-119"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="74f33-119"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="74f33-120">Имя таблицы с полями, из которых происходит выборка записей.</span><span class="sxs-lookup"><span data-stu-id="74f33-120">The name of the table containing the fields from which records are selected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f33-121"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="74f33-121"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="74f33-122">Имена полей, содержащих данные, которые необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="74f33-122">The names of the fields containing the data you want to retrieve.</span></span> <span data-ttu-id="74f33-123">Если вы включите более одного поля, они будут извлечены в порядке по списку.</span><span class="sxs-lookup"><span data-stu-id="74f33-123">If you include more than one field, they are retrieved in the order listed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f33-124"><em>alias1</em>, <em>alias2</em></span><span class="sxs-lookup"><span data-stu-id="74f33-124"><em>alias1</em>, <em>alias2</em></span></span></p></td>
<td><p><span data-ttu-id="74f33-125">Имена, предназначенные для использования в качестве заголовков столбцов вместо исходного названия столбцов в <em>table</em>.</span><span class="sxs-lookup"><span data-stu-id="74f33-125">The names to use as column headers instead of the original column names in <em>table</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74f33-126"><em>tableexpression</em></span><span class="sxs-lookup"><span data-stu-id="74f33-126"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="74f33-127">Имя таблицы или таблиц, содержащих данные, которые необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="74f33-127">The name of the table or tables containing the data you want to retrieve.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74f33-128"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="74f33-128"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="74f33-129">Имя базы данных, содержащей таблицы в <em>tableexpression</em>, если они еще не содержатся в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="74f33-129">The name of the database containing the tables in <em>tableexpression</em> if they are not in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="74f33-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74f33-130">Remarks</span></span>

<span data-ttu-id="74f33-131">Чтобы выполнить это действие, ядро СУБД Microsoft Jet выполняет поиск указанной таблицы или таблиц, извлекает выбранные столбцы, выбирает строки, которые удовлетворяют критерию и сортирует или группирует итоговые строки в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="74f33-131">To perform this operation, the Microsoft Jet database engine searches the specified table or tables, extracts the chosen columns, selects rows that meet the criterion, and sorts or groups the resulting rows into the order specified.</span></span>

<span data-ttu-id="74f33-132">Операторы SELECT не изменяют данные в базе данных.</span><span class="sxs-lookup"><span data-stu-id="74f33-132">SELECT statements do not change data in the database.</span></span>

<span data-ttu-id="74f33-133">SELECT обычно является первым словом в операторе SQL.</span><span class="sxs-lookup"><span data-stu-id="74f33-133">SELECT is usually the first word in an SQL statement.</span></span> <span data-ttu-id="74f33-134">Большинство операторов SQL — операторы SELECT или [SELECT…INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="74f33-134">Most SQL statements are either SELECT or [SELECT…INTO](select-into-statement-microsoft-access-sql.md) statements.</span></span>

<span data-ttu-id="74f33-135">Минимальный синтаксис для оператора SELECT:</span><span class="sxs-lookup"><span data-stu-id="74f33-135">The minimum syntax for a SELECT statement is:</span></span>

<span data-ttu-id="74f33-136">SELECT *fields* FROM *table*</span><span class="sxs-lookup"><span data-stu-id="74f33-136">SELECT *fields* FROM *table*</span></span>

<span data-ttu-id="74f33-137">Вы можете использовать звездочку (\*), чтобы выбрать все поля в таблице.</span><span class="sxs-lookup"><span data-stu-id="74f33-137">You can use an asterisk (\*) to select all fields in a table.</span></span> <span data-ttu-id="74f33-138">В приведенном ниже примере выделяются все поля в таблице "Сотрудники":</span><span class="sxs-lookup"><span data-stu-id="74f33-138">The following example selects all of the fields in the Employees table:</span></span>

```sql
SELECT * FROM Employees;
```

<span data-ttu-id="74f33-139">Если имя поля добавляется в несколько таблиц в предложении FROM, укажите перед ним имя таблицы и **.**</span><span class="sxs-lookup"><span data-stu-id="74f33-139">If a field name is included in more than one table in the FROM clause, precede it with the table name and the **.**</span></span> <span data-ttu-id="74f33-140">(dot) operator.</span><span class="sxs-lookup"><span data-stu-id="74f33-140">(dot) operator.</span></span> <span data-ttu-id="74f33-141">В приведенном ниже примере поле "Отдел" находится в таблице Руководители и таблице Сотрудники.</span><span class="sxs-lookup"><span data-stu-id="74f33-141">In the following example, the Department field is in both the Employees table and the Supervisors table.</span></span> <span data-ttu-id="74f33-142">Оператор SQL выделяет отделы в таблице Сотрудники в таблицы и имена руководителей в таблице Руководители:</span><span class="sxs-lookup"><span data-stu-id="74f33-142">The SQL statement selects departments from the Employees table and supervisor names from the Supervisors table:</span></span>

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

<span data-ttu-id="74f33-143">Когда создается объект **Recordset**, ядро СУБД Microsoft Jet использует имя поля таблицы в качестве имени объекта **Field** в объекте **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="74f33-143">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object.</span></span> <span data-ttu-id="74f33-144">Если вы хотите использовать другое имя поля или имя, которое не подразумевается выражением, используемые для генерации поля, используйте зарезервированное слово AS.</span><span class="sxs-lookup"><span data-stu-id="74f33-144">If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word.</span></span> <span data-ttu-id="74f33-145">В следующем примере используется название Birth в качестве имени возвращаемого объекта **Field** в итоговом объекте **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="74f33-145">The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

<span data-ttu-id="74f33-146">При каждом использовании агрегатных функций или запросов, которые возвращают неоднозначные или повторяющиеся имена объекта **Field**, воспользуйтесь оператором AS для предоставления запасного имени объекта **Field**.</span><span class="sxs-lookup"><span data-stu-id="74f33-146">Whenever you use aggregate functions or queries that return ambiguous or duplicate **Field** object names, you must use the AS clause to provide an alternate name for the **Field** object.</span></span> <span data-ttu-id="74f33-147">В следующем примере используется название HeadCount в качестве имени возвращаемого объекта **Field** в итоговом объекте **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="74f33-147">The following example uses the title HeadCount to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

<span data-ttu-id="74f33-148">Для дополнительного ограничения и организации возвращаемых данных, можно использовать другие предложения в операторе SELECT.</span><span class="sxs-lookup"><span data-stu-id="74f33-148">You can use the other clauses in a SELECT statement to further restrict and organize your returned data.</span></span> <span data-ttu-id="74f33-149">Дополнительные сведения см. в статье справки для предложения, которое вы используете.</span><span class="sxs-lookup"><span data-stu-id="74f33-149">For more information, see the Help topic for the clause you are using.</span></span>

<span data-ttu-id="74f33-150">**Ссылки, предоставляемые** сообществом [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="74f33-150">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="74f33-151">UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="74f33-151">UtterAccess is the premier Microsoft Access wiki and help forum. Click here to join.
</span></span>

- [<span data-ttu-id="74f33-152">Форматирования SQL в VBA</span><span class="sxs-lookup"><span data-stu-id="74f33-152">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [<span data-ttu-id="74f33-153">Просмотр записи в заданном диапазоне</span><span class="sxs-lookup"><span data-stu-id="74f33-153">Viewing Records Within A Defined Range</span></span>](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a><span data-ttu-id="74f33-154">Пример</span><span class="sxs-lookup"><span data-stu-id="74f33-154">Example</span></span>

<span data-ttu-id="74f33-155">В некоторых из примеров ниже предполагается, что существует гипотетическое поле Salary (Оклад) в таблице Employees (Сотрудники).</span><span class="sxs-lookup"><span data-stu-id="74f33-155">Some of the following examples assume the existence of a hypothetical Salary field in an Employees table.</span></span> <span data-ttu-id="74f33-156">Обратите внимание, что это поле на самом деле не существует в таблице Employees (Сотрудники) базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="74f33-156">Note that this field does not actually exist in the Northwind database Employees table.</span></span>

<span data-ttu-id="74f33-157">В данном примере создается объект **Recordset** типа dynaset на основании оператора SQL, который выбирает поля "Фамилия" и "Имя" среди всех записи в таблице "Сотрудники".</span><span class="sxs-lookup"><span data-stu-id="74f33-157">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table.</span></span> <span data-ttu-id="74f33-158">Он вызывает процедуру EnumFields, которая печатает содержимое объекта **Recordset** в окне **Debug**.</span><span class="sxs-lookup"><span data-stu-id="74f33-158">It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span></span>

```sql
    Sub SelectX1() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select the last name and first name values of all  
        ' records in the Employees table. 
        Set rst = dbs.OpenRecordset("SELECT LastName, " _ 
            & "FirstName FROM Employees;") 
     
        ' Populate the recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of the 
        ' Recordset. 
        EnumFields rst,12 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="74f33-159">В данном примере выполняется подсчет количества записей, которые содержат информацию в поле "Индекс", и присваивается имя "Путь" возвращаемому полю.</span><span class="sxs-lookup"><span data-stu-id="74f33-159">This example counts the number of records that have an entry in the PostalCode field and names the returned field Tally.</span></span>

```sql
    Sub SelectX2() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of records with a PostalCode  
        ' value and return the total in the Tally field. 
        Set rst = dbs.OpenRecordset("SELECT Count " _ 
            & "(PostalCode) AS Tally FROM Customers;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of  
        ' the Recordset. Specify field width = 12. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="74f33-160">В этом примере показано количество сотрудников и среднее и максимальное вознаграждения.</span><span class="sxs-lookup"><span data-stu-id="74f33-160">This example shows the number of employees and the average and maximum salaries.</span></span>

```sql
    Sub SelectX3() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Count the number of employees, calculate the  
        ' average salary, and return the highest salary. 
        Set rst = dbs.OpenRecordset("SELECT Count (*) " _ 
            & "AS TotalEmployees, Avg(Salary) " _ 
            & "AS AverageSalary, Max(Salary) " _ 
            & "AS MaximumSalary FROM Employees;") 
     
        ' Populate the Recordset. 
        rst.MoveLast 
     
        ' Call EnumFields to print the contents of 
        ' the Recordset. Pass the Recordset object and 
        ' desired field width. 
        EnumFields rst, 17 
     
        dbs.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="74f33-161">**Суб** процедура EnumFields передает объект **Recordset** из процедуры вызова.</span><span class="sxs-lookup"><span data-stu-id="74f33-161">The **Sub** procedure EnumFields is passed a **Recordset** object from the calling procedure.</span></span> <span data-ttu-id="74f33-162">Затем процедура форматирует и печатает поля **Recordset** в окне **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="74f33-162">The procedure then formats and prints the fields of the **Recordset** to the **Debug** window.</span></span> <span data-ttu-id="74f33-163">Переменная - это желаемая ширина печатного поля.</span><span class="sxs-lookup"><span data-stu-id="74f33-163">The variable is the desired printed field width.</span></span> <span data-ttu-id="74f33-164">Некоторые поля могут быть обрезаны.</span><span class="sxs-lookup"><span data-stu-id="74f33-164">Some fields may be truncated.</span></span>

```sql
    Sub EnumFields(rst As Recordset, intFldLen As Integer) 
     
        Dim lngRecords As Long, lngFields As Long 
        Dim lngRecCount As Long, lngFldCount As Long 
        Dim strTitle As String, strTemp As String 
     
        ' Set the lngRecords variable to the number of 
        ' records in the Recordset. 
        lngRecords = rst.RecordCount 
     
        ' Set the lngFields variable to the number of 
        ' fields in the Recordset. 
        lngFields = rst.Fields.Count 
     
        Debug.Print "There are " & lngRecords _ 
            & " records containing " & lngFields _ 
            & " fields in the recordset." 
        Debug.Print 
     
        ' Form a string to print the column heading. 
        strTitle = "Record  " 
        For lngFldCount = 0 To lngFields - 1 
            strTitle = strTitle _ 
            & Left(rst.Fields(lngFldCount).Name _ 
            & Space(intFldLen), intFldLen) 
        Next lngFldCount     
     
        ' Print the column heading. 
        Debug.Print strTitle 
        Debug.Print 
     
        ' Loop through the Recordset; print the record 
        ' number and field values. 
        rst.MoveFirst 
     
        For lngRecCount = 0 To lngRecords - 1 
            Debug.Print Right(Space(6) & _ 
                Str(lngRecCount), 6) & "  "; 
     
            For lngFldCount = 0 To lngFields - 1 
                ' Check for Null values. 
                If IsNull(rst.Fields(lngFldCount)) Then 
                    strTemp = "<null>" 
                Else 
                    ' Set strTemp to the field contents.  
                    Select Case _ 
                        rst.Fields(lngFldCount).Type 
                        Case 11 
                            strTemp = "" 
                        Case dbText, dbMemo 
                            strTemp = _ 
                                rst.Fields(lngFldCount) 
                        Case Else 
                            strTemp = _ 
                                str(rst.Fields(lngFldCount)) 
                    End Select 
                End If 
     
                Debug.Print Left(strTemp _  
                    & Space(intFldLen), intFldLen); 
            Next lngFldCount 
     
            Debug.Print 
     
            rst.MoveNext 
     
        Next lngRecCount 
     
    End Sub 
```




