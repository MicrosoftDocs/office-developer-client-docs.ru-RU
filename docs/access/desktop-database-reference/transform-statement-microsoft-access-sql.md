---
title: Преобразование оператора (Microsoft Access SQL)
TOCTitle: TRANSFORM statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c0552d7b98fd0862b3d6b5130d9ad56886402d67
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872657"
---
# <a name="transform-statement-microsoft-access-sql"></a>Преобразование оператора (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Создание запроса.

## <a name="syntax"></a>Синтаксис

ПРЕОБРАЗОВАНИЕ *aggfunctionselectstatement* PIVOT *сводных полей* \[IN (*значение1*\[, *значение2*\[,... \]\])\]

Оператор ПРЕОБРАЗОВАНИЯ состоит из следующих частей:

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
<td><p><em>aggfunction</em></p></td>
<td><p><a href="sql-aggregate-functions-sql.md">Статистические функции SQL</a> , которая работает на выбранные данные.</p></td>
</tr>
<tr class="even">
<td><p><em>selectstatement</em></p></td>
<td><p>Инструкция <a href="select-statement-microsoft-access-sql.md">SELECT</a> .</p></td>
</tr>
<tr class="odd">
<td><p><em>сводных полей</em></p></td>
<td><p>Поле или выражение, которое будет использоваться для создания заголовков столбцов в результирующем наборе.</p></td>
</tr>
<tr class="even">
<td><p><em>значение1</em>, <em>значение2</em></p></td>
<td><p>Фиксированные значения, используемые для создания заголовков столбцов.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Замечания

Сведение данных с помощью перекрестного запроса, чтобы выбрать значения из указанного поля или выражения как заголовок столбца, чтобы просмотреть данные в формате compact более чем с запроса.

Преобразование обязательно инструкцию в строке SQL. Он предшествует ВЫБЕРИТЕ оператор, который определяет поля, которые используются как [предложение сортировку строк](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) и заголовков строк. Кроме того можно включить другие предложения, например, [ГДЕ](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), которые задают дополнительные выделения или критериев сортировки. Вы можете также включить —, особенно в предложении WHERE — в запросе перекрестного.

Значения, возвращаемые в *сводных полей* используются в качестве заголовков столбцов в набор результатов запроса. Например сведения о продажах и месяца продажи в запросе перекрестного будет создано 12 столбцов. Можно ограничить *сводных полей* для создания заголовков с фиксированными значениями (*значение1*, *значение2* ), перечисленные в необязательном предложении. Также можно включить фиксированные значения, для которых не содержит данных для создания дополнительных столбцов.

## <a name="example"></a>Пример

В этом примере используется предложение ПРЕОБРАЗОВАНИЯ SQL для создания перекрестного запроса, отражающая число заказов на каждого сотрудника, занимаемых для каждого Календарный квартал 1994. Функция SQLTRANSFORMOutput является обязательным для выполнения этой процедуры.

```vb
    Sub TransformX1() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SHORT; TRANSFORM " _ 
            & "Count(OrderID) " _ 
            & "SELECT FirstName & "" "" & LastName AS " _ 
            & "FullName FROM Employees INNER JOIN Orders " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart " _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
       
           strSQL = strSQL & "GROUP BY FirstName & " _ 
            & """ "" & LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"", OrderDate)" 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub
```

<br/>

В этом примере используется предложение ПРЕОБРАЗОВАНИЯ SQL для создания немного сложнее перекрестного запроса, отображение доллар общее количество заказов, занимаемых каждого сотрудника для каждого Календарный квартал 1994. Функция SQLTRANSFORMOutput является обязательным для выполнения этой процедуры.

```vb
    Sub TransformX2() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SMALLINT; TRANSFORM " _ 
            & "Sum(Subtotal) SELECT FirstName & "" """ _ 
            & "& LastName AS FullName " _ 
            & "FROM Employees INNER JOIN " _ 
            & "(Orders INNER JOIN [Order Subtotals] " _ 
            & "ON Orders.OrderID = " _ 
            & "[Order Subtotals].OrderID) " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart" _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
        
           strSQL = strSQL & "GROUP BY FirstName & "" """ _ 
            & "& LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"",OrderDate)"         
             
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub 
     
    Function SQLTRANSFORMOutput(qdfTemp As QueryDef, _ 
        intYear As Integer) 
         
        Dim rstTRANSFORM As Recordset 
        Dim fldLoop As Field 
        Dim booFirst As Boolean 
     
        qdfTemp.PARAMETERS!prmYear = intYear 
        Set rstTRANSFORM = qdfTemp.OpenRecordset() 
         
        Debug.Print qdfTemp.SQL 
        Debug.Print 
        Debug.Print , , "Quarter" 
     
        With rstTRANSFORM 
            booFirst = True 
            For Each fldLoop In .Fields 
                If booFirst = True Then 
                    Debug.Print fldLoop.Name 
                    Debug.Print , ; 
                    booFirst = False 
                Else 
                    Debug.Print , fldLoop.Name; 
                End If 
            Next fldLoop 
            Debug.Print 
             
            Do While Not .EOF 
                booFirst = True 
                For Each fldLoop In .Fields 
                    If booFirst = True Then 
                        Debug.Print fldLoop 
                        Debug.Print , ; 
                        booFirst = False 
                    Else 
                        Debug.Print , fldLoop; 
                    End If 
                Next fldLoop 
                Debug.Print 
                .MoveNext 
            Loop 
        End With 
         
    End Function
```
