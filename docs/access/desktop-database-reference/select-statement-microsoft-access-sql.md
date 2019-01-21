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
# <a name="select-statement-microsoft-access-sql"></a>Оператор SELECT (Microsoft Access SQL)

**Область применения**: Access 2013 | Office 2013

Указывает ядру СУБД Microsoft Access возвращать информацию из базы данных в виде наборе записей.

## <a name="syntax"></a>Синтаксис

SELECT \[*predicate*\] { \* | *table*.\* | \[*table*.\]*field1* \[AS *alias1*\] \[, \[*table*.\]*field2* \[AS *alias2*\] \[, …\]\]} FROM *tableexpression* \[, …\] \[IN *externaldatabase*\] \[WHERE… \] \[GROUP BY… \] \[HAVING… \] \[ORDER BY… \] \[WITH OWNERACCESS OPTION\]

Оператор SELECT состоит из следующих частей:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>predicate</em></p></td>
<td><p>Одно из следующих предикатов: <a href="https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql">ALL, DISTINCT, DISTINCTROW, or TOP</a> Вы можете использовать предикаты для ограничения числа возвращаемых записей. Если ничего не указано, значение по умолчанию ALL.</p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p>Указывает, что все поля из указанной таблицы или таблиц выбраны.</p></td>
</tr>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>Имя таблицы с полями, из которых происходит выборка записей.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Имена полей, содержащих данные, которые необходимо извлечь. Если вы включите более одного поля, они будут извлечены в порядке по списку.</p></td>
</tr>
<tr class="odd">
<td><p><em>alias1</em>, <em>alias2</em></p></td>
<td><p>Имена, предназначенные для использования в качестве заголовков столбцов вместо исходного названия столбцов в <em>table</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>tableexpression</em></p></td>
<td><p>Имя таблицы или таблиц, содержащих данные, которые необходимо извлечь.</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>Имя базы данных, содержащей таблицы в <em>tableexpression</em>, если они еще не содержатся в текущей базе данных.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Комментарии

Чтобы выполнить это действие, ядро СУБД Microsoft Jet выполняет поиск указанной таблицы или таблиц, извлекает выбранные столбцы, выбирает строки, которые удовлетворяют критерию и сортирует или группирует итоговые строки в указанном порядке.

Операторы SELECT не изменяют данные в базе данных.

SELECT обычно является первым словом в операторе SQL. Большинство операторов SQL — операторы SELECT или [SELECT…INTO](select-into-statement-microsoft-access-sql.md).

Минимальный синтаксис для оператора SELECT:

SELECT *fields* FROM *table*

Вы можете использовать звездочку (\*), чтобы выбрать все поля в таблице. В приведенном ниже примере выделяются все поля в таблице "Сотрудники":

```sql
SELECT * FROM Employees;
```

Если имя поля добавляется в несколько таблиц в предложении FROM, укажите перед ним имя таблицы и **.** (dot) operator. В приведенном ниже примере поле "Отдел" находится в таблице Руководители и таблице Сотрудники. Оператор SQL выделяет отделы в таблице Сотрудники в таблицы и имена руководителей в таблице Руководители:

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

Когда создается объект **Recordset**, ядро СУБД Microsoft Jet использует имя поля таблицы в качестве имени объекта **Field** в объекте **Recordset**. Если вы хотите использовать другое имя поля или имя, которое не подразумевается выражением, используемые для генерации поля, используйте зарезервированное слово AS. В следующем примере используется название Birth в качестве имени возвращаемого объекта **Field** в итоговом объекте **Recordset**:

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

При каждом использовании агрегатных функций или запросов, которые возвращают неоднозначные или повторяющиеся имена объекта **Field**, воспользуйтесь оператором AS для предоставления запасного имени объекта **Field**. В следующем примере используется название HeadCount в качестве имени возвращаемого объекта **Field** в итоговом объекте **Recordset**:

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

Для дополнительного ограничения и организации возвращаемых данных, можно использовать другие предложения в операторе SELECT. Дополнительные сведения см. в статье справки для предложения, которое вы используете.

**Ссылки, предоставляемые** сообществом [UtterAccess](https://www.utteraccess.com). UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.

- [Форматирования SQL в VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [Просмотр записи в заданном диапазоне](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a>Пример

В некоторых из примеров ниже предполагается, что существует гипотетическое поле Salary (Оклад) в таблице Employees (Сотрудники). Обратите внимание, что это поле на самом деле не существует в таблице Employees (Сотрудники) базы данных Northwind.

В данном примере создается объект **Recordset** типа dynaset на основании оператора SQL, который выбирает поля "Фамилия" и "Имя" среди всех записи в таблице "Сотрудники". Он вызывает процедуру EnumFields, которая печатает содержимое объекта **Recordset** в окне **Debug**.

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

В данном примере выполняется подсчет количества записей, которые содержат информацию в поле "Индекс", и присваивается имя "Путь" возвращаемому полю.

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

В этом примере показано количество сотрудников и среднее и максимальное вознаграждения.

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

**Суб** процедура EnumFields передает объект **Recordset** из процедуры вызова. Затем процедура форматирует и печатает поля **Recordset** в окне **Отладка**. Переменная - это желаемая ширина печатного поля. Некоторые поля могут быть обрезаны.

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




