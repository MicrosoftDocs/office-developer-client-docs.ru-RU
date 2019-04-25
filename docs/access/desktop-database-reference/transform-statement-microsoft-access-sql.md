---
title: Инструкция TRANSFORM (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: 9abe91d4ce6996a725e246da6922015d15a8bd39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314044"
---
# <a name="transform-statement-microsoft-access-sql"></a>Инструкция TRANSFORM (Microsoft Access SQL)

**Область применения**: Access 2013, Office 2013

Создает перекрестный запрос.

## <a name="syntax"></a>Синтаксис

TRANSFORM *агрегатная_функция инструкция_select* PIVOT *поле_сводной_таблицы* \[IN (*значение1*\[, *значение2*\[, ...\]\])\]

Инструкция TRANSFORM состоит из следующих элементов:

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
<td><p><em>агрегатная_функция</em></p></td>
<td><p><a href="sql-aggregate-functions-sql.md">Агрегатная функция SQL</a>, обрабатывающая выбранные данные.</p></td>
</tr>
<tr class="even">
<td><p><em>инструкция_select</em></p></td>
<td><p>Инструкция <a href="select-statement-microsoft-access-sql.md">SELECT</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>поле_сводной_таблицы</em></p></td>
<td><p>Поле или выражение, которое нужно использовать для создания заголовков столбцов в наборе результатов запроса.</p></td>
</tr>
<tr class="even">
<td><p><em>значение1</em>, <em>значение2</em></p></td>
<td><p>Фиксированные значения, используемые для создания заголовков столбцов.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Примечания

При суммировании данных с помощью перекрестного запроса значения выбираются из указанных полей или выражений, например из заголовков столбцов. Таким образом, данные отображаются в более сжатом формате, чем при использовании запроса на выборку.

Инструкция TRANSFORM является необязательной, но если она используется, она должна быть первой инструкцией в строке SQL. Она предшествует инструкции SELECT, в которой задаются поля, используемые в качестве заголовков строк, и предложению [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql), определяющему группировку строк. При необходимости вы можете добавить другие предложения, например [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), чтобы задать дополнительные условия выбора или сортировки. В перекрестном запросе также можно использовать вложенные запросы в качестве предикатов, например в предложении WHERE.

Значения, возвращаемые *полем_сводной_таблицы*, используются в качестве заголовков столбцов в результирующем наборе записей. Например, при сведении данных объемов продаж и месяца продажи в перекрестном запросе будет создано 12 столбцов. Вы можете ограничить действие *поля_сводной_таблицы* и создать заголовки, используя фиксированные значения (*значение1*, *значение2*), указанные в необязательном предложении IN. Чтобы создать дополнительные столбцы, можно ввести фиксированные значения, для которых не существует данных.

## <a name="example"></a>Пример

В этом примере используется предложение SQL TRANSFORM, чтобы создать перекрестный запрос, показывающий количество заказов, принятых каждым сотрудником, за каждый календарный квартал 1994 года. Для запуска этой процедуры необходима функция SQLTRANSFORMOutput.

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

В этом примере используется предложение SQL TRANSFORM, чтобы создать немного более сложный перекрестный запрос, показывающий общую сумму (в долларах) заказов, принятых каждым сотрудником, за каждый календарный квартал 1994 года. Для запуска этой процедуры необходима функция SQLTRANSFORMOutput.

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
