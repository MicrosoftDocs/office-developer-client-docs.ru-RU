---
title: Метод Database.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 75ee7cac-dcd0-b4c5-b55b-9cbaaae2cbf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195966(v=office.15)
ms:contentKeyID: 48545686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c19ef8ab8ef2e937ba7467b3695f9aa5780c21c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294983"
---
# <a name="databasecreatequerydef-method-dao"></a><span data-ttu-id="35477-102">Метод Database.CreateQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="35477-102">Database.CreateQueryDef Method (DAO)</span></span>

<span data-ttu-id="35477-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35477-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35477-104">Создает новый объект **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="35477-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="35477-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35477-105">Syntax</span></span>

<span data-ttu-id="35477-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="35477-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="35477-107">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="35477-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="35477-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="35477-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="35477-109">Имя</span><span class="sxs-lookup"><span data-stu-id="35477-109">Name</span></span></p></th>
<th><p><span data-ttu-id="35477-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="35477-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="35477-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="35477-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="35477-112">Описание</span><span class="sxs-lookup"><span data-stu-id="35477-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35477-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="35477-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="35477-114">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="35477-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="35477-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="35477-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="35477-116">Объект типа <strong>Variant</strong> (подтип <strong>String</strong>), однозначно определяющий новый объект <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="35477-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>TableDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="35477-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="35477-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="35477-118">Необязательный</span><span class="sxs-lookup"><span data-stu-id="35477-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="35477-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="35477-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="35477-120">Объект <strong>Variant</strong> (подтип <strong>String</strong>), представляющий инструкцию SQL, которая определяет объект <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="35477-120">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>.</span></span> <span data-ttu-id="35477-121">Если не указать этот аргумент, вы можете определить объект <strong>QueryDef</strong>, задав его свойство <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> до или после его добавления к коллекции.</span><span class="sxs-lookup"><span data-stu-id="35477-121">If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="35477-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35477-122">Return value</span></span>

<span data-ttu-id="35477-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="35477-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="35477-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="35477-124">Remarks</span></span>

<span data-ttu-id="35477-125">В рабочей области Microsoft Access, если указать в качестве имени какое-либо значение, кроме строки нулевой длины, при создании объекта **QueryDef**, полученный объект **QueryDef** будет автоматически добавлен к коллекции **[QueryDefs](querydefs-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="35477-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="35477-126">Если объект, указанный по имени, уже является элементом коллекции **QueryDefs**, возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="35477-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="35477-127">Вы можете создать временный объект **QueryDef**, указав в качестве имени строку нулевой длины при выполнении метода **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="35477-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="35477-128">Это также можно сделать, указав строку нулевой длины ("") в качестве значения свойства **[Name](querydef-name-property-dao.md)** нового объекта **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="35477-128">You can also accomplish this by setting the **[Name](querydef-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> 

<span data-ttu-id="35477-129">Временные объекты **QueryDef** полезны, если требуется регулярно использовать динамические инструкции SQL, не создавая постоянных объектов в коллекции **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="35477-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="35477-130">Временный объект **QueryDef** невозможно добавить к какой-либо коллекции, так как строка нулевой длины не является допустимым именем постоянного объекта **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="35477-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="35477-131">Вы всегда можете задать свойства **Name** и **SQL** нового объекта **QueryDef**, а затем добавить объект **QueryDef** к коллекции **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="35477-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="35477-132">Чтобы выполнить инструкцию SQL в объекте **QueryDef**, используйте метод **[Execute](querydef-execute-method-dao.md)** или **[OpenRecordset](database-openrecordset-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="35477-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](querydef-execute-method-dao.md)** or **[OpenRecordset](database-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="35477-133">Использование объекта **QueryDef** является предпочтительным способом выполнения SQL-запросов к серверу с базами данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="35477-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="35477-134">Чтобы удалить объект **QueryDef** из коллекции **QueryDefs** в базе данных ядра СУБД Microsoft Access, используйте метод **[Delete](querydefs-delete-method-dao.md)** для этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="35477-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](querydefs-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="35477-135">Пример</span><span class="sxs-lookup"><span data-stu-id="35477-135">Example</span></span>

<span data-ttu-id="35477-136">В этом примере используется метод **CreateQueryDef**, чтобы создать и выполнить временный и постоянный объекты **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="35477-136">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="35477-137">Функция GetrstTemp необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="35477-137">The GetrstTemp function is required for this procedure to run.</span></span>

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

В этом примере используются методы **CreateQueryDef** и **OpenRecordset**, а также свойство **SQL**, чтобы отправить запрос к таблице названий в примере базы данных Pubs из Microsoft SQL Server и получить название самой продаваемой книги, а также его идентификатор. <span data-ttu-id="35477-139">Затем этот пример отправляет запрос к таблице авторов и предлагает пользователю отправить премиальный чек каждому автору с учетом доли его лицензионных выплат (общая сумма премии составляет 1000 долл. США, а каждый автор должен получить определенный процент от этой суммы).</span><span class="sxs-lookup"><span data-stu-id="35477-139">The example then queries the table of authors and instructs the user to send a bonus check to each author based on his or her royalty share (the total bonus is $1,000 and each author should receive a percentage of that amount).</span></span>

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

<span data-ttu-id="35477-140">В приведенном ниже примере показано, как создать запрос с параметрами.</span><span class="sxs-lookup"><span data-stu-id="35477-140">The following example shows how to execute a parameter query.</span></span> <span data-ttu-id="35477-141">Запрос с именем **myQuery** создается с двумя параметрами: Param1 и Param2.</span><span class="sxs-lookup"><span data-stu-id="35477-141">A query named **myQuery** is created with two parameters, named Param1 and Param2.</span></span> <span data-ttu-id="35477-142">Для этого в качестве свойства SQL запроса задается инструкция языка SQL, определяющая параметры.</span><span class="sxs-lookup"><span data-stu-id="35477-142">To do this, the SQL property of the query is set to a Structured Query Language (SQL) statement that defines the parameters.</span></span>

<span data-ttu-id="35477-143">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="35477-143">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
