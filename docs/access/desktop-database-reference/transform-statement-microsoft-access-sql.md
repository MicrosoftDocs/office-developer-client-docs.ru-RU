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
# <a name="transform-statement-microsoft-access-sql"></a><span data-ttu-id="30189-102">Инструкция TRANSFORM (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="30189-102">TRANSFORM Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="30189-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30189-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30189-104">Создает перекрестный запрос.</span><span class="sxs-lookup"><span data-stu-id="30189-104">Creates a crosstab query.</span></span>

## <a name="syntax"></a><span data-ttu-id="30189-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30189-105">Syntax</span></span>

<span data-ttu-id="30189-106">TRANSFORM *агрегатная_функция инструкция_select* PIVOT *поле_сводной_таблицы* \[IN (*значение1*\[, *значение2*\[, ...\]\])\]</span><span class="sxs-lookup"><span data-stu-id="30189-106">TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]</span></span>

<span data-ttu-id="30189-107">Инструкция TRANSFORM состоит из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="30189-107">The SELECT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30189-108">Часть</span><span class="sxs-lookup"><span data-stu-id="30189-108">Part</span></span></p></th>
<th><p><span data-ttu-id="30189-109">Описание</span><span class="sxs-lookup"><span data-stu-id="30189-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30189-110"><em>агрегатная_функция</em></span><span class="sxs-lookup"><span data-stu-id="30189-110"><em>aggfunction</em></span></span></p></td>
<td><p><span data-ttu-id="30189-111"><a href="sql-aggregate-functions-sql.md">Агрегатная функция SQL</a>, обрабатывающая выбранные данные.</span><span class="sxs-lookup"><span data-stu-id="30189-111">An <a href="sql-aggregate-functions-sql.md">SQL aggregate function</a> that operates on the selected data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30189-112"><em>инструкция_select</em></span><span class="sxs-lookup"><span data-stu-id="30189-112"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="30189-113">Инструкция <a href="select-statement-microsoft-access-sql.md">SELECT</a>.</span><span class="sxs-lookup"><span data-stu-id="30189-113">A <a href="select-statement-microsoft-access-sql.md">SELECT</a> statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30189-114"><em>поле_сводной_таблицы</em></span><span class="sxs-lookup"><span data-stu-id="30189-114"><em>PivotField</em></span></span></p></td>
<td><p><span data-ttu-id="30189-115">Поле или выражение, которое нужно использовать для создания заголовков столбцов в наборе результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="30189-115">The field or expression you want to use to create column headings in the query's result set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30189-116"><em>значение1</em>, <em>значение2</em></span><span class="sxs-lookup"><span data-stu-id="30189-116"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="30189-117">Фиксированные значения, используемые для создания заголовков столбцов.</span><span class="sxs-lookup"><span data-stu-id="30189-117">Fixed values used to create column headings.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="30189-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="30189-118">Remarks</span></span>

<span data-ttu-id="30189-119">При суммировании данных с помощью перекрестного запроса значения выбираются из указанных полей или выражений, например из заголовков столбцов. Таким образом, данные отображаются в более сжатом формате, чем при использовании запроса на выборку.</span><span class="sxs-lookup"><span data-stu-id="30189-119">When you summarize data using a crosstab query, you select values from specified fields or expressions as column headings so you can view data in a more compact format than with a select query.</span></span>

<span data-ttu-id="30189-120">Инструкция TRANSFORM является необязательной, но если она используется, она должна быть первой инструкцией в строке SQL.</span><span class="sxs-lookup"><span data-stu-id="30189-120">TRANSFORM is optional but when included is the first statement in an SQL string.</span></span> <span data-ttu-id="30189-121">Она предшествует инструкции SELECT, в которой задаются поля, используемые в качестве заголовков строк, и предложению [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql), определяющему группировку строк.</span><span class="sxs-lookup"><span data-stu-id="30189-121">It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping.</span></span> <span data-ttu-id="30189-122">При необходимости вы можете добавить другие предложения, например [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), чтобы задать дополнительные условия выбора или сортировки.</span><span class="sxs-lookup"><span data-stu-id="30189-122">Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria.</span></span> <span data-ttu-id="30189-123">В перекрестном запросе также можно использовать вложенные запросы в качестве предикатов, например в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="30189-123">You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.</span></span>

<span data-ttu-id="30189-124">Значения, возвращаемые *полем_сводной_таблицы*, используются в качестве заголовков столбцов в результирующем наборе записей.</span><span class="sxs-lookup"><span data-stu-id="30189-124">The values returned in *pivotfield* are used as column headings in the query's result set.</span></span> <span data-ttu-id="30189-125">Например, при сведении данных объемов продаж и месяца продажи в перекрестном запросе будет создано 12 столбцов.</span><span class="sxs-lookup"><span data-stu-id="30189-125">For example, pivoting the sales figures on the month of the sale in a crosstab query would create 12 columns.</span></span> <span data-ttu-id="30189-126">Вы можете ограничить действие *поля_сводной_таблицы* и создать заголовки, используя фиксированные значения (*значение1*, *значение2*), указанные в необязательном предложении IN.</span><span class="sxs-lookup"><span data-stu-id="30189-126">You can restrict *pivotfield* to create headings from fixed values (*value1*, *value2* ) listed in the optional IN clause.</span></span> <span data-ttu-id="30189-127">Чтобы создать дополнительные столбцы, можно ввести фиксированные значения, для которых не существует данных.</span><span class="sxs-lookup"><span data-stu-id="30189-127">You can also include fixed values for which no data exists to create additional columns.</span></span>

## <a name="example"></a><span data-ttu-id="30189-128">Пример</span><span class="sxs-lookup"><span data-stu-id="30189-128">Example</span></span>

<span data-ttu-id="30189-129">В этом примере используется предложение SQL TRANSFORM, чтобы создать перекрестный запрос, показывающий количество заказов, принятых каждым сотрудником, за каждый календарный квартал 1994 года.</span><span class="sxs-lookup"><span data-stu-id="30189-129">This example uses the SQL TRANSFORM clause to create a crosstab query showing the number of orders taken by each employee for each calendar quarter of 1994.</span></span> <span data-ttu-id="30189-130">Для запуска этой процедуры необходима функция SQLTRANSFORMOutput.</span><span class="sxs-lookup"><span data-stu-id="30189-130">The SortOutput function is required for this procedure to run.</span></span>

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

<span data-ttu-id="30189-131">В этом примере используется предложение SQL TRANSFORM, чтобы создать немного более сложный перекрестный запрос, показывающий общую сумму (в долларах) заказов, принятых каждым сотрудником, за каждый календарный квартал 1994 года.</span><span class="sxs-lookup"><span data-stu-id="30189-131">This example uses the SQL TRANSFORM clause to create a slightly more complex crosstab query showing the total dollar amount of orders taken by each employee for each calendar quarter of 1994.</span></span> <span data-ttu-id="30189-132">Для запуска этой процедуры необходима функция SQLTRANSFORMOutput.</span><span class="sxs-lookup"><span data-stu-id="30189-132">The AddName function is required for this procedure to run.</span></span>

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
