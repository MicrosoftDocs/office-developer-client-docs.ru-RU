---
title: Объявление ARAMETERS (Microsoft Access SQL)
TOCTitle: PARAMETERS declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: d78a6c043e99af1ca50ca798b94088400fd09f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287869"
---
# <a name="parameters-declaration-microsoft-access-sql"></a>Объявление ARAMETERS (Microsoft Access SQL)


**Область применения**: Access 2013, Office 2013

Используется для описания имен и типов данных параметров в запросе с параметрами.

## <a name="syntax"></a>Синтаксис

PARAMETERS *name datatype* \[, *name datatype* \[, ...\]\]

Объявление PARAMETERS включает следующие элементы:

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
<td><p><em>name</em></p></td>
<td><p>Имя параметра. Присваивается свойству <strong>Name</strong> объекта <strong>Parameter</strong> и используется для его идентификации в коллекции <strong>Parameters</strong>. Параметр <em>name</em> можно вывести в диалоговом окне во время обработки запроса приложением. Текст, содержащий пробелы или знаки пунктуации, необходимо заключить в квадратные скобки ([ ]). Например, [Низкая цена] или [С какого месяца начинать составление отчета?] — допустимые значения аргумента <em>name</em>.</p></td>
</tr>
<tr class="even">
<td><p><em>datatype</em></p></td>
<td><p>Один из основных <a href="sql-data-types.md">типов данных Microsoft Access SQL</a> или их синонимов.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Объявление PARAMETERS можно использовать для создания регулярно выполняемых запросов с параметрами. Запрос с параметрами позволяет автоматически вносить изменения в условия запроса. При использовании запросов с параметрами программа должна запрашивать параметры при каждом выполнении запроса.

Использование объявления PARAMETERS не является обязательным. Если оно используется, объявление PARAMETERS должно предшествовать всем остальным инструкциям, в том числе [SELECT](select-statement-microsoft-access-sql.md).

Если параметров в объявлении несколько, их необходимо разделять запятыми. В приведенном ниже примере использованы два параметра.

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

В предложении [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) нельзя использовать *datatype*, но можно использовать *name*. В следующем примере ожидается ввод двух параметров, которые затем используются в качестве условий отбора записей в таблице Orders:

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a>Пример

В этом примере пользователю нужно указать должность, которая затем используется в качестве условия запроса.

В этом примере выполняется вызов процедуры EnumFields, который вы можете найти в примере для [инструкции SELECT](select-statement-microsoft-access-sql.md).

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
