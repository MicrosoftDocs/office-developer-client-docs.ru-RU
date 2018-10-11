---
title: SELECT Statement (Microsoft Access SQL)
TOCTitle: SELECT Statement (Microsoft Access SQL)
ms:assetid: a5c9da94-5f9e-0fc0-767a-4117f38a5ef3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821148(v=office.15)
ms:contentKeyID: 48546837
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: ae7a63a3fe7647dde117db80a52e2322b9af75b9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480474"
---
# <a name="select-statement-microsoft-access-sql"></a><span data-ttu-id="b0a49-102">SELECT Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b0a49-102">SELECT Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="b0a49-103">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0a49-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="b0a49-104">Указывает, что ядро базы данных Microsoft Access, чтобы получить сведения из базы данных в виде набора записей.</span><span class="sxs-lookup"><span data-stu-id="b0a49-104">Instructs the Microsoft Access database engine to return information from the database as a set of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a49-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0a49-105">Syntax</span></span>

<span data-ttu-id="b0a49-106">ВЫБЕРИТЕ \[ *предикат* \] { \*  |  *таблицы*.\*  |  \[ *в таблице*. \] *field1* \[как *псевдоним1* \] \[, \[ *в таблице*. \] *поле2* \[как *псевдоним2* \] \[,... \] \]} Из *выражение_таблиц* \[,... \] \[В *внешняя_база_данных* \] \[ГДЕ...</span><span class="sxs-lookup"><span data-stu-id="b0a49-106">SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE…</span></span> <span data-ttu-id="b0a49-107">\]\[Группировать по...</span><span class="sxs-lookup"><span data-stu-id="b0a49-107">\] \[GROUP BY…</span></span> <span data-ttu-id="b0a49-108">\]\[HAVING...</span><span class="sxs-lookup"><span data-stu-id="b0a49-108">\] \[HAVING…</span></span> <span data-ttu-id="b0a49-109">\]\[ORDER BY...</span><span class="sxs-lookup"><span data-stu-id="b0a49-109">\] \[ORDER BY…</span></span> <span data-ttu-id="b0a49-110">\]\[С OWNERACCESS OPTION\]</span><span class="sxs-lookup"><span data-stu-id="b0a49-110">\] \[WITH OWNERACCESS OPTION\]</span></span>

<span data-ttu-id="b0a49-111">Инструкция SELECT состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="b0a49-111">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0a49-112">Часть</span><span class="sxs-lookup"><span data-stu-id="b0a49-112">Part</span></span></p></th>
<th><p><span data-ttu-id="b0a49-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b0a49-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0a49-114"><em>предикат</em></span><span class="sxs-lookup"><span data-stu-id="b0a49-114"><em>predicate</em></span></span></p></td>
<td><p><span data-ttu-id="b0a49-115">Предикаты одно из следующих значений: <a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL, DISTINCT, DISTINCTROW или TOP</a>.</span><span class="sxs-lookup"><span data-stu-id="b0a49-115">One of the following predicates: <a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL, DISTINCT, DISTINCTROW, or TOP</a>.</span></span> <span data-ttu-id="b0a49-116">Предикаты используются для ограничения числа возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="b0a49-116">You use the predicate to restrict the number of records returned.</span></span> <span data-ttu-id="b0a49-117">Если не указано, по умолчанию используется ALL.</span><span class="sxs-lookup"><span data-stu-id="b0a49-117">If none is specified, the default is ALL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p><span data-ttu-id="b0a49-118">Указывает, что выбраны все поля из таблицы или таблиц.</span><span class="sxs-lookup"><span data-stu-id="b0a49-118">Specifies that all fields from the specified table or tables are selected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0a49-119"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="b0a49-119"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="b0a49-120">Имя таблицы, содержащей поля, из которых выбраны записей.</span><span class="sxs-lookup"><span data-stu-id="b0a49-120">The name of the table containing the fields from which records are selected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0a49-121"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="b0a49-121"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="b0a49-122">Имена полей, содержащих данные, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="b0a49-122">The names of the fields containing the data you want to retrieve.</span></span> <span data-ttu-id="b0a49-123">Если включить более одного поля, их загрузки в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="b0a49-123">If you include more than one field, they are retrieved in the order listed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0a49-124"><em>псевдоним1</em>, <em>псевдоним2</em></span><span class="sxs-lookup"><span data-stu-id="b0a49-124"><em>alias1</em>, <em>alias2</em></span></span></p></td>
<td><p><span data-ttu-id="b0a49-125">Имена для использования в качестве заголовков столбцов, а не исходные имена столбцов в <em>таблице</em>.</span><span class="sxs-lookup"><span data-stu-id="b0a49-125">The names to use as column headers instead of the original column names in <em>table</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0a49-126"><em>выражение_таблиц</em></span><span class="sxs-lookup"><span data-stu-id="b0a49-126"><em>tableexpression</em></span></span></p></td>
<td><p><span data-ttu-id="b0a49-127">Имя таблицы или таблиц, содержащих данные, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b0a49-127">The name of the table or tables containing the data you want to retrieve.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0a49-128"><em>внешняя_база_данных</em></span><span class="sxs-lookup"><span data-stu-id="b0a49-128"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="b0a49-129">Имя базы данных, содержащий таблиц в <em>выражение_таблиц</em> , если они не находятся в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="b0a49-129">The name of the database containing the tables in <em>tableexpression</em> if they are not in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b0a49-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="b0a49-130">Remarks</span></span>

<span data-ttu-id="b0a49-131">Для выполнения этой операции, базы данных Microsoft® Jet выполняет поиск указанной таблицы или таблиц, извлекает соответствующие столбцы, выбирает строки, отвечающие критерия и сортирует полученные строки в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="b0a49-131">To perform this operation, the Microsoft® Jet database engine searches the specified table or tables, extracts the chosen columns, selects rows that meet the criterion, and sorts or groups the resulting rows into the order specified.</span></span>

<span data-ttu-id="b0a49-132">Инструкции SELECT не изменяйте данные в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b0a49-132">SELECT statements do not change data in the database.</span></span>

<span data-ttu-id="b0a49-133">Инструкция SELECT обычно является первое слово в инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="b0a49-133">SELECT is usually the first word in an SQL statement.</span></span> <span data-ttu-id="b0a49-134">Большинство инструкций SQL являются SELECT или [Выбор... В](select-into-statement-microsoft-access-sql.md) операторов.</span><span class="sxs-lookup"><span data-stu-id="b0a49-134">Most SQL statements are either SELECT or [SELECT…INTO](select-into-statement-microsoft-access-sql.md) statements.</span></span>

<span data-ttu-id="b0a49-135">— Это минимальный синтаксис инструкции SELECT:</span><span class="sxs-lookup"><span data-stu-id="b0a49-135">The minimum syntax for a SELECT statement is:</span></span>

<span data-ttu-id="b0a49-136">ВЫБЕРИТЕ из *поля* *в таблице*</span><span class="sxs-lookup"><span data-stu-id="b0a49-136">SELECT *fields* FROM *table*</span></span>

<span data-ttu-id="b0a49-137">Можно использовать символ звездочки (\*) для выбора всех полей в таблице.</span><span class="sxs-lookup"><span data-stu-id="b0a49-137">You can use an asterisk (\*) to select all fields in a table.</span></span> <span data-ttu-id="b0a49-138">В следующем примере выбираются все поля в таблице «Сотрудники»:</span><span class="sxs-lookup"><span data-stu-id="b0a49-138">The following example selects all of the fields in the Employees table:</span></span>

```sql
SELECT * FROM Employees;
```

<span data-ttu-id="b0a49-139">Если имя поля включено в несколько таблиц в предложении FROM, вставьте перед ним имя таблицы и **.**</span><span class="sxs-lookup"><span data-stu-id="b0a49-139">If a field name is included in more than one table in the FROM clause, precede it with the table name and the **.**</span></span> <span data-ttu-id="b0a49-140">(точка).</span><span class="sxs-lookup"><span data-stu-id="b0a49-140">(dot) operator.</span></span> <span data-ttu-id="b0a49-141">В следующем примере в таблицу Employees и Начальники — поля отдела.</span><span class="sxs-lookup"><span data-stu-id="b0a49-141">In the following example, the Department field is in both the Employees table and the Supervisors table.</span></span> <span data-ttu-id="b0a49-142">Инструкция SQL выбирает отделы из имена таблиц и администратора сотрудников из таблицы руководителями.</span><span class="sxs-lookup"><span data-stu-id="b0a49-142">The SQL statement selects departments from the Employees table and supervisor names from the Supervisors table:</span></span>

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

<span data-ttu-id="b0a49-143">При создании объекта **набора записей** ядро базы данных Microsoft Jet использует имя поля таблицы как имя объекта **поля** в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b0a49-143">When a **Recordset** object is created, the Microsoft Jet database engine uses the table's field name as the **Field** object name in the **Recordset** object.</span></span> <span data-ttu-id="b0a49-144">Если требуется другое имя поля или имя не предоставляется выражением, используются для создания поля, используйте AS зарезервированным словом.</span><span class="sxs-lookup"><span data-stu-id="b0a49-144">If you want a different field name or a name is not implied by the expression used to generate the field, use the AS reserved word.</span></span> <span data-ttu-id="b0a49-145">В следующем примере используется заголовок рождения одно имя, возвращенного объекта **поля** в объекте результирующего **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="b0a49-145">The following example uses the title Birth to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

<span data-ttu-id="b0a49-146">При использовании агрегатных функций или запросов, возвращающих неоднозначные или одинаковые имена объектов **поля** , необходимо использовать предложение AS укажите альтернативное имя для объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="b0a49-146">Whenever you use aggregate functions or queries that return ambiguous or duplicate **Field** object names, you must use the AS clause to provide an alternate name for the **Field** object.</span></span> <span data-ttu-id="b0a49-147">В следующем примере используется название штата сотрудников одно имя, возвращенного объекта **поля** в объекте результирующего **набора записей** :</span><span class="sxs-lookup"><span data-stu-id="b0a49-147">The following example uses the title HeadCount to name the returned **Field** object in the resulting **Recordset** object:</span></span>

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

<span data-ttu-id="b0a49-148">Можно использовать другие предложения в операторе SELECT для дальнейшего ограничения и упорядочения полученных данных.</span><span class="sxs-lookup"><span data-stu-id="b0a49-148">You can use the other clauses in a SELECT statement to further restrict and organize your returned data.</span></span> <span data-ttu-id="b0a49-149">Для получения дополнительных сведений см раздел справки для предложения, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="b0a49-149">For more information, see the Help topic for the clause you are using.</span></span>

<span data-ttu-id="b0a49-150">**Автор ссылки** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="b0a49-150">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="b0a49-151">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b0a49-151">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="b0a49-152">SQL форматирования данных VBA</span><span class="sxs-lookup"><span data-stu-id="b0a49-152">SQL to VBA Formatter</span></span>](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [<span data-ttu-id="b0a49-153">Просмотр записей в рамках определенного диапазона</span><span class="sxs-lookup"><span data-stu-id="b0a49-153">Viewing Records Within A Defined Range</span></span>](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a><span data-ttu-id="b0a49-154">Пример</span><span class="sxs-lookup"><span data-stu-id="b0a49-154">Example</span></span>

<span data-ttu-id="b0a49-155">Некоторые из приведенных ниже примерах предполагается наличие предполагаемую заработной платы поля в таблице «Сотрудники».</span><span class="sxs-lookup"><span data-stu-id="b0a49-155">Some of the following examples assume the existence of a hypothetical Salary field in an Employees table.</span></span> <span data-ttu-id="b0a49-156">Обратите внимание на то, что это поле фактически не существует в таблице Employees базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="b0a49-156">Note that this field does not actually exist in the Northwind database Employees table.</span></span>

<span data-ttu-id="b0a49-157">В этом примере создается добавляющий **набора записей** на основе инструкции SQL, которая выбирает поля LastName и FirstName всех записей в таблице сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b0a49-157">This example creates a dynaset-type **Recordset** based on an SQL statement that selects the LastName and FirstName fields of all records in the Employees table.</span></span> <span data-ttu-id="b0a49-158">Он вызывает процедуру EnumFields, который печатает содержимое объекта **набора записей** в окне **Отладка** .</span><span class="sxs-lookup"><span data-stu-id="b0a49-158">It calls the EnumFields procedure, which prints the contents of a **Recordset** object to the **Debug** window.</span></span>

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

<span data-ttu-id="b0a49-159">В этом примере подсчитывает число записей, содержащих в поле PostalCode и имена возвращенных полей результатов голосования.</span><span class="sxs-lookup"><span data-stu-id="b0a49-159">This example counts the number of records that have an entry in the PostalCode field and names the returned field Tally.</span></span>

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

<span data-ttu-id="b0a49-160">В этом примере показано число сотрудников и Зарплата средний и максимальный.</span><span class="sxs-lookup"><span data-stu-id="b0a49-160">This example shows the number of employees and the average and maximum salaries.</span></span>

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

<span data-ttu-id="b0a49-161">Процедуры **Sub** EnumFields передается объект **набора записей** из вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="b0a49-161">The **Sub** procedure EnumFields is passed a **Recordset** object from the calling procedure.</span></span> <span data-ttu-id="b0a49-162">Затем процедура форматов и реализуется печать полей **набора записей** в окне **Отладка** .</span><span class="sxs-lookup"><span data-stu-id="b0a49-162">The procedure then formats and prints the fields of the **Recordset** to the **Debug** window.</span></span> <span data-ttu-id="b0a49-163">Переменная — это ширина нужного распечатанных поля.</span><span class="sxs-lookup"><span data-stu-id="b0a49-163">The variable is the desired printed field width.</span></span> <span data-ttu-id="b0a49-164">В некоторых полях может усекаться.</span><span class="sxs-lookup"><span data-stu-id="b0a49-164">Some fields may be truncated.</span></span>

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




