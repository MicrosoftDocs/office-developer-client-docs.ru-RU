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
# <a name="select-statement-microsoft-access-sql"></a>SELECT Statement (Microsoft Access SQL)

**Применимо к:** Access 2013 | Office 2013

Указывает, что ядро базы данных Microsoft Access, чтобы получить сведения из базы данных в виде набора записей.

## <a name="syntax"></a>Синтаксис

ВЫБЕРИТЕ \[ *предикат* \] { \*  |  *таблицы*.\*  |  \[ *в таблице*. \] *field1* \[как *псевдоним1* \] \[, \[ *в таблице*. \] *поле2* \[как *псевдоним2* \] \[,... \] \]} Из *выражение_таблиц* \[,... \] \[В *внешняя_база_данных* \] \[ГДЕ... \]\[Группировать по... \]\[HAVING... \]\[ORDER BY... \]\[С OWNERACCESS OPTION\]

Инструкция SELECT состоит из следующих частей:

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
<td><p><em>предикат</em></p></td>
<td><p>Предикаты одно из следующих значений: <a href="https://msdn.microsoft.com/library/ff195711(v=office.15)">ALL, DISTINCT, DISTINCTROW или TOP</a>. Предикаты используются для ограничения числа возвращаемых записей. Если не указано, по умолчанию используется ALL.</p></td>
</tr>
<tr class="even">
<td><p><em>*</em></p></td>
<td><p>Указывает, что выбраны все поля из таблицы или таблиц.</p></td>
</tr>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>Имя таблицы, содержащей поля, из которых выбраны записей.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Имена полей, содержащих данные, которые необходимо получить. Если включить более одного поля, их загрузки в указанном порядке.</p></td>
</tr>
<tr class="odd">
<td><p><em>псевдоним1</em>, <em>псевдоним2</em></p></td>
<td><p>Имена для использования в качестве заголовков столбцов, а не исходные имена столбцов в <em>таблице</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>выражение_таблиц</em></p></td>
<td><p>Имя таблицы или таблиц, содержащих данные, которые требуется получить.</p></td>
</tr>
<tr class="odd">
<td><p><em>внешняя_база_данных</em></p></td>
<td><p>Имя базы данных, содержащий таблиц в <em>выражение_таблиц</em> , если они не находятся в текущей базе данных.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Для выполнения этой операции, базы данных Microsoft® Jet выполняет поиск указанной таблицы или таблиц, извлекает соответствующие столбцы, выбирает строки, отвечающие критерия и сортирует полученные строки в указанном порядке.

Инструкции SELECT не изменяйте данные в базе данных.

Инструкция SELECT обычно является первое слово в инструкции SQL. Большинство инструкций SQL являются SELECT или [Выбор... В](select-into-statement-microsoft-access-sql.md) операторов.

— Это минимальный синтаксис инструкции SELECT:

ВЫБЕРИТЕ из *поля* *в таблице*

Можно использовать символ звездочки (\*) для выбора всех полей в таблице. В следующем примере выбираются все поля в таблице «Сотрудники»:

```sql
SELECT * FROM Employees;
```

Если имя поля включено в несколько таблиц в предложении FROM, вставьте перед ним имя таблицы и **.** (точка). В следующем примере в таблицу Employees и Начальники — поля отдела. Инструкция SQL выбирает отделы из имена таблиц и администратора сотрудников из таблицы руководителями.

```sql
SELECT Employees.Department, Supervisors.SupvName 
FROM Employees INNER JOIN Supervisors 
WHERE Employees.Department = Supervisors.Department;
```

При создании объекта **набора записей** ядро базы данных Microsoft Jet использует имя поля таблицы как имя объекта **поля** в объекте **набора записей** . Если требуется другое имя поля или имя не предоставляется выражением, используются для создания поля, используйте AS зарезервированным словом. В следующем примере используется заголовок рождения одно имя, возвращенного объекта **поля** в объекте результирующего **набора записей** :

```sql
SELECT BirthDate 
AS Birth FROM Employees;
```

При использовании агрегатных функций или запросов, возвращающих неоднозначные или одинаковые имена объектов **поля** , необходимо использовать предложение AS укажите альтернативное имя для объекта **поля** . В следующем примере используется название штата сотрудников одно имя, возвращенного объекта **поля** в объекте результирующего **набора записей** :

```sql
SELECT COUNT(EmployeeID)
AS HeadCount FROM Employees;
```

Можно использовать другие предложения в операторе SELECT для дальнейшего ограничения и упорядочения полученных данных. Для получения дополнительных сведений см раздел справки для предложения, которую вы используете.

**Автор ссылки** [UtterAccess](https://www.utteraccess.com) сообщества. UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.

- [SQL форматирования данных VBA](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

- [Просмотр записей в рамках определенного диапазона](https://www.utteraccess.com/wiki/index.php/records_within_a_defined_range)

## <a name="example"></a>Пример

Некоторые из приведенных ниже примерах предполагается наличие предполагаемую заработной платы поля в таблице «Сотрудники». Обратите внимание на то, что это поле фактически не существует в таблице Employees базы данных Northwind.

В этом примере создается добавляющий **набора записей** на основе инструкции SQL, которая выбирает поля LastName и FirstName всех записей в таблице сотрудников. Он вызывает процедуру EnumFields, который печатает содержимое объекта **набора записей** в окне **Отладка** .

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

В этом примере подсчитывает число записей, содержащих в поле PostalCode и имена возвращенных полей результатов голосования.

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

В этом примере показано число сотрудников и Зарплата средний и максимальный.

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

Процедуры **Sub** EnumFields передается объект **набора записей** из вызова процедуры. Затем процедура форматов и реализуется печать полей **набора записей** в окне **Отладка** . Переменная — это ширина нужного распечатанных поля. В некоторых полях может усекаться.

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




