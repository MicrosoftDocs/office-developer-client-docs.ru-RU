---
title: Свойство QueryDef.SQL (DAO)
TOCTitle: SQL property
ms:assetid: 16446789-c8be-bff0-eddd-b5f6a8530128
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845522(v=office.15)
ms:contentKeyID: 48543429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053054
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 43acce256d3a46fd7b01122a8502e0af502eb3e9
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937682"
---
# <a name="querydefsql-property-dao"></a><span data-ttu-id="daa91-102">Свойство QueryDef.SQL (DAO)</span><span class="sxs-lookup"><span data-stu-id="daa91-102">QueryDef.SQL property (DAO)</span></span>

<span data-ttu-id="daa91-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="daa91-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="daa91-104">Задает или возвращает SQL, который определяет запрос, выполняемый с помощью объекта **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="daa91-104">Sets or returns the SQL statement that defines the query executed by a **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daa91-105">Syntax</span></span>

<span data-ttu-id="daa91-106">*выражение* . SQL</span><span class="sxs-lookup"><span data-stu-id="daa91-106">*expression* .SQL</span></span>

<span data-ttu-id="daa91-107">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="daa91-107">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="daa91-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="daa91-108">Remarks</span></span>

<span data-ttu-id="daa91-109">Свойство **SQL** содержит инструкции SQL, которая определяет как запись, сгруппированных и упорядоченные при выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="daa91-109">The **SQL** property contains the SQL statement that determines how records are selected, grouped, and ordered when you execute the query.</span></span> <span data-ttu-id="daa91-110">Запрос можно использовать для выбора записей для включения в объект **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="daa91-110">You can use the query to select records to include in a **[Recordset](recordset-object-dao.md)** object.</span></span> <span data-ttu-id="daa91-111">Можно также определить запросы для изменения данных без возвращения записей.</span><span class="sxs-lookup"><span data-stu-id="daa91-111">You can also define action queries to modify data without returning records.</span></span>

<span data-ttu-id="daa91-112">Синтаксис SQL, используемый в запросе должен соответствовать типу диалект SQL модуля запроса, который определяется тип рабочей области.</span><span class="sxs-lookup"><span data-stu-id="daa91-112">The SQL syntax used in a query must conform to the SQL dialect of the query engine, which is determined by the type of workspace.</span></span> <span data-ttu-id="daa91-113">В рабочей области Microsoft Access, используйте диалект Microsoft Access SQL, если не создать запрос к серверу, в этом случае следует использовать диалект сервера.</span><span class="sxs-lookup"><span data-stu-id="daa91-113">In a Microsoft Access workspace, use the Microsoft Access SQL dialect, unless you create an SQL pass-through query, in which case you should use the dialect of the server.</span></span>

<span data-ttu-id="daa91-114">Если оператор SQL включает параметры для запроса, необходимо выбрать данные перед выполнением.</span><span class="sxs-lookup"><span data-stu-id="daa91-114">If the SQL statement includes parameters for the query, you must set these before execution.</span></span> <span data-ttu-id="daa91-115">Только после сброса параметров те же значения параметра, применяются при каждом выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="daa91-115">Until you reset the parameters, the same parameter values are applied each time you execute the query.</span></span>

<span data-ttu-id="daa91-116">В рабочей области Microsoft Access с помощью объекта **QueryDef** является предпочтительным для выполнения операций к серверу SQL в источники данных ODBC подключением модуля Microsoft Access базы данных.</span><span class="sxs-lookup"><span data-stu-id="daa91-116">In a Microsoft Access workspace, using a **QueryDef** object is the preferred way to perform SQL pass-through operations on Microsoft Access database engine-connected ODBC data sources.</span></span> <span data-ttu-id="daa91-117">Путем установки свойства объекта **QueryDef** **[подключение](querydef-connect-property-dao.md)** к источнику данных ODBC, можно использовать SQL не – – – базы данных Microsoft Access в запрос для передачи на внешний сервер.</span><span class="sxs-lookup"><span data-stu-id="daa91-117">By setting the **QueryDef** object's **[Connect](querydef-connect-property-dao.md)** property to an ODBC data source, you can use non–Microsoft–Access–database SQL in the query to be passed to the external server.</span></span> <span data-ttu-id="daa91-118">Например можно использовать инструкции TRANSACT SQL (с Microsoft SQL Server или Sybase SQL Server базы данных), которые в противном случае — не обрабатывает ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="daa91-118">For example, you can use TRANSACT SQL statements (with Microsoft SQL Server or Sybase SQL Server databases), which the Microsoft Access database engine would otherwise not process.</span></span>

> [!NOTE]
> <span data-ttu-id="daa91-119">Если свойству присвоено значение string, объединяется с дробное значение и системных параметров укажите десятичных знаков например запятой (например, `strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50`), будет выдана ошибка при попытке выполнить объекта **QueryDef** в Microsoft База данных модуля базы данных Access.</span><span class="sxs-lookup"><span data-stu-id="daa91-119">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, `strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50`), an error will result when you try to execute the **QueryDef** object in a Microsoft Access database engine database.</span></span> <span data-ttu-id="daa91-120">Это так, как во время объединения, номер будет преобразован в строку с помощью системы по умолчанию десятичных знаков и Microsoft Access SQL принимает только США десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="daa91-120">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="daa91-121">Пример</span><span class="sxs-lookup"><span data-stu-id="daa91-121">Example</span></span>

<span data-ttu-id="daa91-122">В этом примере демонстрируется свойство **SQL** , Настройка и изменение свойства **SQL** временные **QueryDef** и сравнения результатов.</span><span class="sxs-lookup"><span data-stu-id="daa91-122">This example demonstrates the **SQL** property by setting and changing the **SQL** property of a temporary **QueryDef** and comparing the results.</span></span> <span data-ttu-id="daa91-123">Функция SQLOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="daa91-123">The SQLOutput function is required for this procedure to run.</span></span>

```vb
    Sub SQLX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim rstEmployees As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfTemp = dbsNorthwind.CreateQueryDef("") 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'USA' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       ' Open Recordset using temporary QueryDef object and  
       ' print report. 
       SQLOutput "SELECT * FROM Employees " & _ 
          "WHERE Country = 'UK' " & _ 
          "ORDER BY LastName", qdfTemp 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Function SQLOutput(strSQL As String, qdfTemp As QueryDef) 
     
       Dim rstEmployees As Recordset 
     
       ' Set SQL property of temporary QueryDef object and open  
       ' a Recordset. 
       qdfTemp.SQL = strSQL 
       Set rstEmployees = qdfTemp.OpenRecordset 
     
       Debug.Print strSQL 
     
       With rstEmployees 
          ' Enumerate Recordset. 
          Do While Not .EOF 
             Debug.Print "  " & !FirstName & " " & _ 
                !LastName & ", " & !Country 
             .MoveNext 
          Loop 
          .Close 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="daa91-124">В этом примере используется метод **CopyQueryDef** для создания копии **QueryDef** из существующих **записей** и изменяет эту копию, добавив предложение свойство **SQL** .</span><span class="sxs-lookup"><span data-stu-id="daa91-124">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the **SQL** property.</span></span> <span data-ttu-id="daa91-125">При создании постоянной **QueryDef**пробелы, точки с запятой или каретки могут быть добавлены к свойству **SQL** ; необходимо очищено от вложения эти дополнительные символы, прежде чем любые новые предложения можно присоединить к инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="daa91-125">When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the **SQL** property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
       strAdd As String) As QueryDef 
     
       Dim strSQL As String 
       Dim strRightSQL As String 
     
       Set CopyQueryNew = rstTemp.CopyQueryDef 
       With CopyQueryNew 
          ' Strip extra characters. 
          strSQL = .SQL 
          strRightSQL = Right(strSQL, 1) 
          Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
                strRightSQL = Chr(10) Or strRightSQL = vbCr 
             strSQL = Left(strSQL, Len(strSQL) - 1) 
             strRightSQL = Right(strSQL, 1) 
          Loop 
          .SQL = strSQL & strAdd 
       End With 
     
    End Function 
```

<br/>

<span data-ttu-id="daa91-126">В этом примере показано возможное использование CopyQueryNew().</span><span class="sxs-lookup"><span data-stu-id="daa91-126">This example shows a possible use of CopyQueryNew().</span></span> 
     
```vb
    Sub CopyQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfEmployees As QueryDef 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
       Dim strOrderBy As String 
       Dim qdfCopy As QueryDef 
       Dim rstCopy As Recordset 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
          "NewQueryDef", "SELECT FirstName, LastName, " & _ 
          "BirthDate FROM Employees") 
       Set rstEmployees = qdfEmployees.OpenRecordset( _ 
          dbOpenForwardOnly) 
     
       Do While True 
          intCommand = Val(InputBox( _ 
             "Choose field on which to order a new " & _ 
             "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
             "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
             "[Cancel - exit]")) 
          Select Case intCommand 
             Case 1 
                strOrderBy = " ORDER BY FirstName" 
             Case 2 
                strOrderBy = " ORDER BY LastName" 
             Case 3 
                strOrderBy = " ORDER BY BirthDate" 
             Case Else 
                Exit Do 
          End Select 
          Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
          Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
             dbForwardOnly) 
          With rstCopy 
             Do While Not .EOF 
                Debug.Print !LastName & ", " & !FirstName & _ 
                   " - " & !BirthDate 
                .MoveNext 
             Loop 
             .Close 
          End With 
          Exit Do 
       Loop 
     
       rstEmployees.Close 
       ' Delete new QueryDef because this is a demonstration. 
       dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="daa91-127">В этом примере использует **CreateQueryDef** и **OpenRecordset** методы и свойства **SQL** для запроса к таблице заголовки в образце базы данных Pubs Microsoft SQL Server и вернуть название и идентификатор заголовка лидера продаж.</span><span class="sxs-lookup"><span data-stu-id="daa91-127">This example uses the **CreateQueryDef** and **OpenRecordset** methods and the **SQL** property to query the table of titles in the Microsoft SQL Server sample database Pubs and return the title and title identifier of the best-selling book.</span></span> <span data-ttu-id="daa91-128">Затем запрашивает таблицы авторов и указывает на отправку выполняется проверка премии каждого автора на его основе или совместно использовать свой прямые (общее вознаграждение равно 1000 долларов США и каждого автора должны принимать процент это значение).</span><span class="sxs-lookup"><span data-stu-id="daa91-128">The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

```vb
    Sub ClientServerX2() 
     
       Dim dbsCurrent As Database 
       Dim qdfBestSellers As QueryDef 
       Dim qdfBonusEarners As QueryDef 
       Dim rstTopSeller As Recordset 
       Dim rstBonusRecipients As Recordset 
       Dim strAuthorList As String 
     
       ' Open a database from which QueryDef objects can be  
       ' created. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a temporary QueryDef object to retrieve 
       ' data from a Microsoft SQL Server database. 
       Set qdfBestSellers = dbsCurrent.CreateQueryDef("") 
       With qdfBestSellers 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT title, title_id FROM titles " & _ 
             "ORDER BY ytd_sales DESC" 
          Set rstTopSeller = .OpenRecordset() 
          rstTopSeller.MoveFirst 
       End With 
     
       ' Create a temporary QueryDef to retrieve data from 
       ' a Microsoft SQL Server database based on the results from 
       ' the first query. 
       Set qdfBonusEarners = dbsCurrent.CreateQueryDef("") 
       With qdfBonusEarners 
          ' Note: The DSN referenced below must be configured to  
          '       use Microsoft Windows NT Authentication Mode to  
          '       authorize user access to the Microsoft SQL Server. 
          .Connect = "ODBC;DATABASE=pubs;DSN=Publishers" 
          .SQL = "SELECT * FROM titleauthor " & _ 
             "WHERE title_id = '" & _ 
             rstTopSeller!title_id & "'" 
          Set rstBonusRecipients = .OpenRecordset() 
       End With 
     
       ' Build the output string. 
       With rstBonusRecipients 
          Do While Not .EOF 
             strAuthorList = strAuthorList & "  " & _ 
                !au_id & ":  $" & (10 * !royaltyper) & vbCr 
             .MoveNext 
          Loop 
       End With 
     
       ' Display results. 
       MsgBox "Please send a check to the following " & _ 
          "authors in the amounts shown:" & vbCr & _ 
          strAuthorList & "for outstanding sales of " & _ 
          rstTopSeller!Title & "." 
     
       rstTopSeller.Close 
       dbsCurrent.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="daa91-129">Следующий пример демонстрирует создание запроса с параметрами.</span><span class="sxs-lookup"><span data-stu-id="daa91-129">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="daa91-130">Запрос с именем **myQuery** создается с двумя параметрами, с именем Param1 и Param2.</span><span class="sxs-lookup"><span data-stu-id="daa91-130">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="daa91-131">Для этого свойства SQL запроса значение оператор структурированный язык запросов (SQL), который определяет параметры.</span><span class="sxs-lookup"><span data-stu-id="daa91-131">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="daa91-132">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="daa91-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateQueryWithParameters()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
        Dim strSQL As String
    
        Set dbs = CurrentDb
        Set qdf = dbs.CreateQueryDef("myQuery")
        Application.RefreshDatabaseWindow
    
        strSQL = "PARAMETERS Param1 TEXT, Param2 INT; "
        strSQL = strSQL & "SELECT * FROM [Table1] "
        strSQL = strSQL & "WHERE [Field1] = [Param1] AND [Field2] = [Param2];"
        qdf.SQL = strSQL
    
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="daa91-133">Следующем примере показано, как заменить оператор структурированный язык запросов (SQL) в сохраненный запрос.</span><span class="sxs-lookup"><span data-stu-id="daa91-133">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

```vb
    Dim qdf as QueryDef
    Dim db as Database
    Set db = CurrentDB
    Set qdf = db.QueryDefs("YourQueryName")
    qdf.SQL = ReplaceWhereClause(qdf.SQL, strYourNewWhereClause)
    set qdf = Nothing
    set db = Nothing
    
    Public Function ReplaceWhereClause(strSQL As Variant, strNewWHERE As Variant)
    On Error GoTo Error_Handler
    
    ‘This subroutine accepts a valid SQL string and Where clause, and
    ‘returns the same SQL statement with the original Where clause (if any)
    ‘replaced by the passed in Where clause.
    ‘
    ‘INPUT:
    ‘ strSQL valid SQL string to change
    ‘OUTPUT:
    ‘ strNewWHERE New WHERE clause to insert into SQL statement
    ‘
    Dim strSELECT As String, strWhere As String
    Dim strOrderBy As String, strGROUPBY As String, strHAVING As String
    
    Call ParseSQL(strSQL, strSELECT, strWhere, strOrderBy, _
    strGROUPBY, strHAVING)
    
    ReplaceWhereClause = strSELECT &""& strNewWHERE &""_
    & strGROUPBY &""& strHAVING &""& strOrderBy
    
    Exit_Procedure:
      Exit Function
    
    Error_Handler:
      MsgBox (Err.Number & ": " & Err.Description)
      Resume Exit_Procedure
    
    End Function
```
