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
ms.openlocfilehash: 16b88f2cf441802c6246425d5bb7bb2efb71a679
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861220"
---
# <a name="transform-statement-microsoft-access-sql"></a><span data-ttu-id="736d1-102">Преобразование оператора (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="736d1-102">TRANSFORM statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="736d1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="736d1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="736d1-104">Создание запроса.</span><span class="sxs-lookup"><span data-stu-id="736d1-104">Creates a crosstab query.</span></span>

## <a name="syntax"></a><span data-ttu-id="736d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="736d1-105">Syntax</span></span>

<span data-ttu-id="736d1-106">ПРЕОБРАЗОВАНИЕ *aggfunctionselectstatement* PIVOT *сводных полей* \[IN (*значение1*\[, *значение2*\[,... \]\])\]</span><span class="sxs-lookup"><span data-stu-id="736d1-106">TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]</span></span>

<span data-ttu-id="736d1-107">Оператор ПРЕОБРАЗОВАНИЯ состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="736d1-107">The TRANSFORM statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="736d1-108">Часть</span><span class="sxs-lookup"><span data-stu-id="736d1-108">Part</span></span></p></th>
<th><p><span data-ttu-id="736d1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="736d1-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="736d1-110"><em>aggfunction</em></span><span class="sxs-lookup"><span data-stu-id="736d1-110"><em>aggfunction</em></span></span></p></td>
<td><p><span data-ttu-id="736d1-111"><a href="sql-aggregate-functions-sql.md">Статистические функции SQL</a> , которая работает на выбранные данные.</span><span class="sxs-lookup"><span data-stu-id="736d1-111">An <a href="sql-aggregate-functions-sql.md">SQL aggregate function</a> that operates on the selected data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="736d1-112"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="736d1-112"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="736d1-113">Инструкция <a href="select-statement-microsoft-access-sql.md">SELECT</a> .</span><span class="sxs-lookup"><span data-stu-id="736d1-113">A <a href="select-statement-microsoft-access-sql.md">SELECT</a> statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="736d1-114"><em>сводных полей</em></span><span class="sxs-lookup"><span data-stu-id="736d1-114"><em>pivotfield</em></span></span></p></td>
<td><p><span data-ttu-id="736d1-115">Поле или выражение, которое будет использоваться для создания заголовков столбцов в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="736d1-115">The field or expression you want to use to create column headings in the query's result set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="736d1-116"><em>значение1</em>, <em>значение2</em></span><span class="sxs-lookup"><span data-stu-id="736d1-116"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="736d1-117">Фиксированные значения, используемые для создания заголовков столбцов.</span><span class="sxs-lookup"><span data-stu-id="736d1-117">Fixed values used to create column headings.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="736d1-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="736d1-118">Remarks</span></span>

<span data-ttu-id="736d1-119">Сведение данных с помощью перекрестного запроса, чтобы выбрать значения из указанного поля или выражения как заголовок столбца, чтобы просмотреть данные в формате compact более чем с запроса.</span><span class="sxs-lookup"><span data-stu-id="736d1-119">When you summarize data using a crosstab query, you select values from specified fields or expressions as column headings so you can view data in a more compact format than with a select query.</span></span>

<span data-ttu-id="736d1-120">Преобразование обязательно инструкцию в строке SQL.</span><span class="sxs-lookup"><span data-stu-id="736d1-120">TRANSFORM is optional but when included is the first statement in an SQL string.</span></span> <span data-ttu-id="736d1-121">Он предшествует ВЫБЕРИТЕ оператор, который определяет поля, которые используются как [предложение сортировку строк](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) и заголовков строк.</span><span class="sxs-lookup"><span data-stu-id="736d1-121">It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping.</span></span> <span data-ttu-id="736d1-122">Кроме того можно включить другие предложения, например, [ГДЕ](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), которые задают дополнительные выделения или критериев сортировки.</span><span class="sxs-lookup"><span data-stu-id="736d1-122">Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria.</span></span> <span data-ttu-id="736d1-123">Вы можете также включить —, особенно в предложении WHERE — в запросе перекрестного.</span><span class="sxs-lookup"><span data-stu-id="736d1-123">You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.</span></span>

<span data-ttu-id="736d1-124">Значения, возвращаемые в *сводных полей* используются в качестве заголовков столбцов в набор результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="736d1-124">The values returned in *pivotfield* are used as column headings in the query's result set.</span></span> <span data-ttu-id="736d1-125">Например сведения о продажах и месяца продажи в запросе перекрестного будет создано 12 столбцов.</span><span class="sxs-lookup"><span data-stu-id="736d1-125">For example, pivoting the sales figures on the month of the sale in a crosstab query would create 12 columns.</span></span> <span data-ttu-id="736d1-126">Можно ограничить *сводных полей* для создания заголовков с фиксированными значениями (*значение1*, *значение2* ), перечисленные в необязательном предложении.</span><span class="sxs-lookup"><span data-stu-id="736d1-126">You can restrict *pivotfield* to create headings from fixed values (*value1*, *value2* ) listed in the optional IN clause.</span></span> <span data-ttu-id="736d1-127">Также можно включить фиксированные значения, для которых не содержит данных для создания дополнительных столбцов.</span><span class="sxs-lookup"><span data-stu-id="736d1-127">You can also include fixed values for which no data exists to create additional columns.</span></span>

## <a name="example"></a><span data-ttu-id="736d1-128">Пример</span><span class="sxs-lookup"><span data-stu-id="736d1-128">Example</span></span>

<span data-ttu-id="736d1-129">В этом примере используется предложение ПРЕОБРАЗОВАНИЯ SQL для создания перекрестного запроса, отражающая число заказов на каждого сотрудника, занимаемых для каждого Календарный квартал 1994.</span><span class="sxs-lookup"><span data-stu-id="736d1-129">This example uses the SQL TRANSFORM clause to create a crosstab query showing the number of orders taken by each employee for each calendar quarter of 1994.</span></span> <span data-ttu-id="736d1-130">Функция SQLTRANSFORMOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="736d1-130">The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

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

<span data-ttu-id="736d1-131">В этом примере используется предложение ПРЕОБРАЗОВАНИЯ SQL для создания немного сложнее перекрестного запроса, отображение доллар общее количество заказов, занимаемых каждого сотрудника для каждого Календарный квартал 1994.</span><span class="sxs-lookup"><span data-stu-id="736d1-131">This example uses the SQL TRANSFORM clause to create a slightly more complex crosstab query showing the total dollar amount of orders taken by each employee for each calendar quarter of 1994.</span></span> <span data-ttu-id="736d1-132">Функция SQLTRANSFORMOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="736d1-132">The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

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
