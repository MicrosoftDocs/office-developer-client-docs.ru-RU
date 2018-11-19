---
title: Описание PARAMETERS (Microsoft Access SQL)
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
ms.openlocfilehash: 64e40da96dc6d82c0f682cba5a3ebc7cfb82bb50
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026409"
---
# <a name="parameters-declaration-microsoft-access-sql"></a><span data-ttu-id="18a98-102">Описание PARAMETERS (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="18a98-102">PARAMETERS declaration (Microsoft Access SQL)</span></span>


<span data-ttu-id="18a98-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18a98-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18a98-104">Объявляет имя и тип данных для каждого параметра в запросе с параметрами.</span><span class="sxs-lookup"><span data-stu-id="18a98-104">Declares the name and data type of each parameter in a parameter query.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a98-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18a98-105">Syntax</span></span>

<span data-ttu-id="18a98-106">Параметры *типа данных имя* \[, *тип данных имя* \[,...\]\]</span><span class="sxs-lookup"><span data-stu-id="18a98-106">PARAMETERS *name datatype* \[, *name datatype* \[, …\]\]</span></span>

<span data-ttu-id="18a98-107">Описание PARAMETERS состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="18a98-107">The PARAMETERS declaration has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18a98-108">Часть</span><span class="sxs-lookup"><span data-stu-id="18a98-108">Part</span></span></p></th>
<th><p><span data-ttu-id="18a98-109">Описание</span><span class="sxs-lookup"><span data-stu-id="18a98-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18a98-110"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="18a98-110"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="18a98-111">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="18a98-111">The name of the parameter.</span></span> <span data-ttu-id="18a98-112">Назначается свойство <strong>Name</strong> объекта <strong>параметра</strong> и используется для идентификации этого параметра в коллекции <strong>параметров</strong> .</span><span class="sxs-lookup"><span data-stu-id="18a98-112">Assigned to the <strong>Name</strong> property of the <strong>Parameter</strong> object and used to identify this parameter in the <strong>Parameters</strong> collection.</span></span> <span data-ttu-id="18a98-113">Можно использовать <em>имя</em> как строка, которая отображается в диалоговом окне во время запроса приложением.</span><span class="sxs-lookup"><span data-stu-id="18a98-113">You can use <em>name</em> as a string that is displayed in a dialog box while your application runs the query.</span></span> <span data-ttu-id="18a98-114">Используйте скобки ([]), чтобы заключить текст, который содержит пробелов и знаков препинания.</span><span class="sxs-lookup"><span data-stu-id="18a98-114">Use brackets ([ ]) to enclose text that contains spaces or punctuation.</span></span> <span data-ttu-id="18a98-115">Например, [Низкая цена] и [приступить к отчет с какой month?] — допустимое <em>имя</em> аргументов.</span><span class="sxs-lookup"><span data-stu-id="18a98-115">For example, [Low price] and [Begin report with which month?] are valid <em>name</em> arguments.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18a98-116"><em>Тип данных</em></span><span class="sxs-lookup"><span data-stu-id="18a98-116"><em>datatype</em></span></span></p></td>
<td><p><span data-ttu-id="18a98-117">Одна из основных <a href="sql-data-types.md">типов данных Microsoft Access SQL</a> или их синонимы.</span><span class="sxs-lookup"><span data-stu-id="18a98-117">One of the primary <a href="sql-data-types.md">Microsoft Access SQL data types</a> or their synonyms.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="18a98-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="18a98-118">Remarks</span></span>

<span data-ttu-id="18a98-119">Для запросов, на которых выполняется регулярно можно использовать параметры объявления для создания запроса с параметрами.</span><span class="sxs-lookup"><span data-stu-id="18a98-119">For queries that you run regularly, you can use a PARAMETERS declaration to create a parameter query.</span></span> <span data-ttu-id="18a98-120">Параметр запроса может помочь автоматизировать процесс изменения условия запроса.</span><span class="sxs-lookup"><span data-stu-id="18a98-120">A parameter query can help automate the process of changing query criteria.</span></span> <span data-ttu-id="18a98-121">С помощью параметра запроса кода потребуется для предоставления параметров при каждом выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="18a98-121">With a parameter query, your code will need to provide the parameters each time the query is run.</span></span>

<span data-ttu-id="18a98-122">Описание PARAMETERS обязательно предшествует любой другой инструкции, включая [Выбор](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="18a98-122">The PARAMETERS declaration is optional but when included precedes any other statement, including [SELECT](select-statement-microsoft-access-sql.md).</span></span>

<span data-ttu-id="18a98-123">Если объявление включает несколько параметров, разделяйте их запятыми.</span><span class="sxs-lookup"><span data-stu-id="18a98-123">If the declaration includes more than one parameter, separate them with commas.</span></span> <span data-ttu-id="18a98-124">Следующий пример включает в себя два параметра:</span><span class="sxs-lookup"><span data-stu-id="18a98-124">The following example includes two parameters:</span></span>

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

<span data-ttu-id="18a98-125">*Имя* , но не *тип данных* можно использовать в предложении [ГДЕ](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) или [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) .</span><span class="sxs-lookup"><span data-stu-id="18a98-125">You can use *name* but not *datatype* in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/having-clause-microsoft-access-sql) clause.</span></span> <span data-ttu-id="18a98-126">В следующем примере описаны два параметра предоставляемую и применено условие в записи в таблице Orders:</span><span class="sxs-lookup"><span data-stu-id="18a98-126">The following example expects two parameters to be provided and then applies the criteria to records in the Orders table:</span></span>

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a><span data-ttu-id="18a98-127">Пример</span><span class="sxs-lookup"><span data-stu-id="18a98-127">Example</span></span>

<span data-ttu-id="18a98-128">В этом примере пользователю требуется укажите название задания, а затем использует данной должности как критерии для запроса.</span><span class="sxs-lookup"><span data-stu-id="18a98-128">This example requires the user to provide a job title and then uses that job title as the criteria for the query.</span></span>

<span data-ttu-id="18a98-129">Он вызывает процедуру EnumFields, которые можно найти в примере [оператор SELECT](select-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="18a98-129">It calls the EnumFields procedure, which you can find in the [SELECT statement](select-statement-microsoft-access-sql.md) example.</span></span>

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
