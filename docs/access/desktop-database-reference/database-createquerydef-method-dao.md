---
title: Database.CreateQueryDef Method (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15577750d7c6a2373178bce9fefff16fef512023
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602674"
---
# <a name="databasecreatequerydef-method-dao"></a><span data-ttu-id="4b756-102">Database.CreateQueryDef Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="4b756-102">Database.CreateQueryDef Method (DAO)</span></span>

<span data-ttu-id="4b756-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b756-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4b756-104">Создает новый объект **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="4b756-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b756-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b756-105">Syntax</span></span>

<span data-ttu-id="4b756-106">*выражение* . CreateQueryDef (***имя***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="4b756-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="4b756-107">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="4b756-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="4b756-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b756-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b756-109">Имя</span><span class="sxs-lookup"><span data-stu-id="4b756-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4b756-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="4b756-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="4b756-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4b756-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="4b756-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4b756-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b756-113">Имя</span><span class="sxs-lookup"><span data-stu-id="4b756-113">Name</span></span></p></td>
<td><p><span data-ttu-id="4b756-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4b756-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="4b756-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4b756-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4b756-116"><strong>Variant</strong> (<strong>String</strong> подтип), уникальным образом новые <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b756-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b756-117">SQLText</span><span class="sxs-lookup"><span data-stu-id="4b756-117">SQLText</span></span></p></td>
<td><p><span data-ttu-id="4b756-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4b756-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="4b756-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4b756-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4b756-120"><strong>Variant</strong> (<strong>String</strong> подтип), которая является инструкцией SQL, определение <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b756-120">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>.</span></span> <span data-ttu-id="4b756-121">Если опустить аргумент, можно определить <strong>QueryDef</strong> путем установки свойства <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> до или после добавления его в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="4b756-121">If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b756-122"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="4b756-122"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="4b756-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b756-123">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="4b756-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b756-124">Return value</span></span>
>>>>>>> <span data-ttu-id="4b756-125">master</span><span class="sxs-lookup"><span data-stu-id="4b756-125">master</span></span>

<span data-ttu-id="4b756-126">QueryDef</span><span class="sxs-lookup"><span data-stu-id="4b756-126">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="4b756-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="4b756-127">Remarks</span></span>

<span data-ttu-id="4b756-128">В рабочей области Microsoft Access Если вы укажите отличное от строку нулевой длины имени при создании **QueryDef**результирующего объекта **QueryDef** автоматически добавляется к коллекции **[QueryDefs](querydefs-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="4b756-128">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="4b756-129">Если объектом, заданным с именем уже должна быть членом **QueryDefs** коллекции, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="4b756-129">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="4b756-130">Временные **QueryDef** можно создать с помощью строку нулевой длины для аргумента имени, при выполнении метода **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="4b756-130">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="4b756-131">Это также можно сделать, задав свойство **[Name](querydef-name-property-dao.md)** только что созданный **QueryDef** в строку нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="4b756-131">You can also accomplish this by setting the **[Name](querydef-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> 

<span data-ttu-id="4b756-132">Временные объекты **QueryDef** полезны, если требуется повторно использовать динамические инструкции SQL, не создавая для создания новых постоянных объектов в коллекции **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="4b756-132">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="4b756-133">Временные **QueryDef** невозможно добавить в любой коллекции, так как строку нулевой длины не является допустимым именем для постоянного объекта **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="4b756-133">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="4b756-134">Всегда можно задать **имя** и свойства **SQL** объекта **QueryDef** только что созданный и затем добавьте **QueryDef** в коллекцию **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="4b756-134">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="4b756-135">Чтобы запустить инструкции SQL в объект **QueryDef** , используйте метод **[Execute](querydef-execute-method-dao.md)** или **[OpenRecordset](database-openrecordset-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="4b756-135">To run the SQL statement in a **QueryDef** object, use the **[Execute](querydef-execute-method-dao.md)** or **[OpenRecordset](database-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="4b756-136">С помощью объекта **QueryDef** является предпочтительным для выполнения запросов к серверу с использованием баз данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="4b756-136">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="4b756-137">Для удаления объекта **QueryDef** из коллекции **QueryDefs** в базе данных ядра базы данных Microsoft Access, используйте метод **[Delete](querydefs-delete-method-dao.md)** в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="4b756-137">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](querydefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="4b756-138">Пример</span><span class="sxs-lookup"><span data-stu-id="4b756-138">Example</span></span>

<span data-ttu-id="4b756-139">В этом примере используется метод **CreateQueryDef** для создания и выполнения временное и постоянное **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="4b756-139">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="4b756-140">Функция GetrstTemp является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="4b756-140">The GetrstTemp function is required for this procedure to run.</span></span>

```vb
    Sub CreateQueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfTemp As QueryDef 
       Dim qdfNew As QueryDef 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       With dbsNorthwind 
          ' Create temporary QueryDef. 
          Set qdfTemp = .CreateQueryDef("", _ 
             "SELECT * FROM Employees") 
          ' Open Recordset and print report. 
          GetrstTemp qdfTemp 
          ' Create permanent QueryDef. 
          Set qdfNew = .CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
          ' Open Recordset and print report. 
          GetrstTemp qdfNew 
          ' Delete new QueryDef because this is a demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
     
    Function GetrstTemp(qdfTemp As QueryDef) 
     
       Dim rstTemp As Recordset 
     
       With qdfTemp 
          Debug.Print .Name 
          Debug.Print "  " & .SQL 
          ' Open Recordset from QueryDef. 
          Set rstTemp = .OpenRecordset(dbOpenSnapshot) 
     
          With rstTemp 
             ' Populate Recordset and print number of records. 
             .MoveLast 
             Debug.Print "  Number of records = " & _ 
                .RecordCount 
             Debug.Print 
             .Close 
          End With 
     
       End With 
     
    End Function 
```

<br/>

В этом примере использует **CreateQueryDef** и **OpenRecordset** методы и свойства **SQL** для запроса к таблице заголовки в образце базы данных Pubs Microsoft SQL Server и вернуть название и идентификатор заголовка лидера продаж. <span data-ttu-id="4b756-142">Затем запрашивает таблицы авторов и указывает на отправку выполняется проверка премии каждого автора на его основе или совместно использовать свой прямые (общее вознаграждение равно 1000 долларов США и каждого автора должны принимать процент это значение).</span><span class="sxs-lookup"><span data-stu-id="4b756-142">The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

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

<span data-ttu-id="4b756-143">Следующий пример демонстрирует создание запроса с параметрами.</span><span class="sxs-lookup"><span data-stu-id="4b756-143">The following example shows how to create a parameter query.</span></span> <span data-ttu-id="4b756-144">Запрос с именем **myQuery** создается с двумя параметрами, с именем Param1 и Param2.</span><span class="sxs-lookup"><span data-stu-id="4b756-144">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="4b756-145">Для этого свойства SQL запроса значение оператор структурированный язык запросов (SQL), который определяет параметры.</span><span class="sxs-lookup"><span data-stu-id="4b756-145">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="4b756-146">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4b756-146">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
