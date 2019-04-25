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
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="af31a-102">Объявление ARAMETERS (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="af31a-102">PARAMETERS Declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="af31a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="af31a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="af31a-104">Используется для описания имен и типов данных параметров в запросе с параметрами.</span><span class="sxs-lookup"><span data-stu-id="af31a-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="af31a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af31a-105">Syntax</span></span>

<span data-ttu-id="af31a-106">PARAMETERS *name datatype* \[, *name datatype* \[, ...\]\]</span><span class="sxs-lookup"><span data-stu-id="af31a-106">PARAMETERS *name datatype* \[, *name datatype* \[, …\]\]</span></span>

<span data-ttu-id="af31a-107">Объявление PARAMETERS включает следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="af31a-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af31a-108">Часть</span><span class="sxs-lookup"><span data-stu-id="af31a-108">Part</span></span></p></th>
<th><p><span data-ttu-id="af31a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="af31a-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af31a-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="af31a-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="af31a-111">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="af31a-111">The name of the parameter.</span></span> <span data-ttu-id="af31a-112">Присваивается свойству <strong>Name</strong> объекта <strong>Parameter</strong> и используется для его идентификации в коллекции <strong>Parameters</strong>.</span><span class="sxs-lookup"><span data-stu-id="af31a-112">Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection.</span></span> <span data-ttu-id="af31a-113">Параметр <em>name</em> можно вывести в диалоговом окне во время обработки запроса приложением.</span><span class="sxs-lookup"><span data-stu-id="af31a-113">You can use <em>name</em> as a string that is displayed in a dialog box while your application runs the query.</span></span> <span data-ttu-id="af31a-114">Текст, содержащий пробелы или знаки пунктуации, необходимо заключить в квадратные скобки ([ ]).</span><span class="sxs-lookup"><span data-stu-id="af31a-114">Use brackets ([ ]) to enclose text that contains spaces or punctuation.</span></span> <span data-ttu-id="af31a-115">Например, [Низкая цена] или [С какого месяца начинать составление отчета?] — допустимые значения аргумента <em>name</em>.</span><span class="sxs-lookup"><span data-stu-id="af31a-115">For example, [Low price] and [Begin report with which month?] are valid <em>name</em> arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af31a-116"><em>datatype</em></span><span class="sxs-lookup"><span data-stu-id="af31a-116"><em>datatype</em></span></span></p></td>
<td><p><span data-ttu-id="af31a-117">Один из основных <a href="sql-data-types.md">типов данных Microsoft Access SQL</a> или их синонимов.</span><span class="sxs-lookup"><span data-stu-id="af31a-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="af31a-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="af31a-118">Remarks</span></span>

<span data-ttu-id="af31a-119">Объявление PARAMETERS можно использовать для создания регулярно выполняемых запросов с параметрами.</span><span class="sxs-lookup"><span data-stu-id="af31a-119">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query.</span></span> <span data-ttu-id="af31a-120">Запрос с параметрами позволяет автоматически вносить изменения в условия запроса.</span><span class="sxs-lookup"><span data-stu-id="af31a-120">A parameter query can help automate the process of changing query criteria.</span></span> <span data-ttu-id="af31a-121">При использовании запросов с параметрами программа должна запрашивать параметры при каждом выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="af31a-121">With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="af31a-122">Использование объявления PARAMETERS не является обязательным. Если оно используется, объявление PARAMETERS должно предшествовать всем остальным инструкциям, в том числе [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="af31a-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="af31a-123">Если параметров в объявлении несколько, их необходимо разделять запятыми.</span><span class="sxs-lookup"><span data-stu-id="af31a-123">If the declaration includes more than one parameter, separate them with commas.</span></span> <span data-ttu-id="af31a-124">В приведенном ниже примере использованы два параметра.</span><span class="sxs-lookup"><span data-stu-id="af31a-124">The following example shows a URL that includes the two query parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="af31a-125">В предложении [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) нельзя использовать *datatype*, но можно использовать *name*.</span><span class="sxs-lookup"><span data-stu-id="af31a-125">You can use *name* but not *datatype* in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) clause.</span></span> <span data-ttu-id="af31a-126">В следующем примере ожидается ввод двух параметров, которые затем используются в качестве условий отбора записей в таблице Orders:</span><span class="sxs-lookup"><span data-stu-id="af31a-126">The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="af31a-127">Пример</span><span class="sxs-lookup"><span data-stu-id="af31a-127">Example</span></span>

<span data-ttu-id="af31a-128">В этом примере пользователю нужно указать должность, которая затем используется в качестве условия запроса.</span><span class="sxs-lookup"><span data-stu-id="af31a-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="af31a-129">В этом примере выполняется вызов процедуры EnumFields, который вы можете найти в примере для [инструкции SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="af31a-129">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
