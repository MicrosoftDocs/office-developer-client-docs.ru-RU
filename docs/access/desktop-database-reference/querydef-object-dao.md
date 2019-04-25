---
title: Объект QueryDef (DAO)
TOCTitle: QueryDef Object
ms:assetid: 0b3d901c-345d-42a2-f5f1-fb09cc562e27
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845129(v=office.15)
ms:contentKeyID: 48543169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a94d34a2dbe8043e6db637b649f59047cf3f1dda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301059"
---
# <a name="querydef-object-dao"></a><span data-ttu-id="aa975-102">Объект QueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="aa975-102">QueryDef object (DAO)</span></span>

<span data-ttu-id="aa975-103">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa975-103">**Applies to:** Access 2013 | Office 2013</span></span> 

<span data-ttu-id="aa975-104">Объект **QueryDef** — это сохраняемое определение запроса в базе данных ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="aa975-104">A **QueryDef** object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa975-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa975-105">Remarks</span></span>

<span data-ttu-id="aa975-106">Объект **QueryDef** можно использовать для определения запроса.</span><span class="sxs-lookup"><span data-stu-id="aa975-106">You can use the **QueryDef** object to define a query.</span></span> <span data-ttu-id="aa975-107">Например, вы можете:</span><span class="sxs-lookup"><span data-stu-id="aa975-107">For example, you can:</span></span>

- <span data-ttu-id="aa975-108">Использовать свойство **SQL**, чтобы задать или вернуть определение запроса.</span><span class="sxs-lookup"><span data-stu-id="aa975-108">Use the **SQL** property to set or return the query definition.</span></span>

- <span data-ttu-id="aa975-109">Использовать коллекцию **Parameters** объекта **QueryDef**, чтобы задать или вернуть параметры запроса.</span><span class="sxs-lookup"><span data-stu-id="aa975-109">Use the **QueryDef** object's **Parameters** collection to set or return query parameters.</span></span>

- <span data-ttu-id="aa975-110">Использовать свойство **Type**, чтобы вернуть значение, которое указывает действие запроса: выбор записей из существующей таблицы, создание таблицы, вставка записей из одной таблицы в другую, удаление записей или обновление записей.</span><span class="sxs-lookup"><span data-stu-id="aa975-110">Use the **Type** property to return a value indicating whether the query selects records from an existing table, makes a new table, inserts records from one table into another table, deletes records, or updates records.</span></span>

- <span data-ttu-id="aa975-111">Использовать свойство **MaxRecords**, чтобы ограничить число записей, возвращаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="aa975-111">Use the **MaxRecords** property to limit the number of records returned from a query.</span></span>

- <span data-ttu-id="aa975-112">Использовать свойство **ODBCTimeout**, чтобы указать длительность ожидания перед возвращением запросом записей.</span><span class="sxs-lookup"><span data-stu-id="aa975-112">Use the **ODBCTimeout** property to indicate how long to wait before the query returns records.</span></span> <span data-ttu-id="aa975-113">Свойство **ODBCTimeout** применяется к любому запросу, обращающемуся к данным ODBC.</span><span class="sxs-lookup"><span data-stu-id="aa975-113">The **ODBCTimeout** property applies to any query that accesses ODBC data.</span></span>

- <span data-ttu-id="aa975-114">Использовать свойство **ReturnsRecords**, чтобы указать, что запрос возвращает записи.</span><span class="sxs-lookup"><span data-stu-id="aa975-114">Use the **ReturnsRecords** property to indicate that the query returns records.</span></span> <span data-ttu-id="aa975-115">Применение свойства **ReturnsRecords** допустимо только для запросов SQL к серверу.</span><span class="sxs-lookup"><span data-stu-id="aa975-115">The **ReturnsRecords** property is only valid on SQL pass-through queries.</span></span>

- <span data-ttu-id="aa975-116">Использовать свойство **Connect**, чтобы создать запрос SQL к серверу для базы данных ODC.</span><span class="sxs-lookup"><span data-stu-id="aa975-116">Use the **Connect** property to make an SQL pass-through query to an ODC database.</span></span>

<span data-ttu-id="aa975-117">Также можно создавать временные объекты **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="aa975-117">You can also create temporary **QueryDef** objects.</span></span> <span data-ttu-id="aa975-118">В отличие от постоянных объектов **QueryDef** временные объекты **QueryDef** не сохраняются на диске и не добавляются в коллекцию **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="aa975-118">Unlike permanent **QueryDef** objects, temporary **QueryDef** objects are not saved to disk or appended to the **QueryDefs** collection.</span></span> <span data-ttu-id="aa975-119">Временные объекты **QueryDef** удобно использовать для запросов, которые нужно неоднократно запускать во время выполнения, но не требуется сохранять на диск, в частности, если создаются их инструкции SQL во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="aa975-119">Temporary **QueryDef** objects are useful for queries that you must run repeatedly during run time but do not not need to save to disk, particularly if you create their SQL statements during run time.</span></span>

<span data-ttu-id="aa975-120">Постоянный объект **QueryDef** в рабочей области Microsoft Access можно рассматривать как скомпилированную инструкцию SQL.</span><span class="sxs-lookup"><span data-stu-id="aa975-120">You can think of a permanent **QueryDef** object in a Microsoft Access workspace as a compiled SQL statement.</span></span> <span data-ttu-id="aa975-121">Если запрос запускается из постоянного объекта **QueryDef**, он выполняется быстрее, чем при запуске эквивалентной инструкции SQL с помощью метода **OpenRecordset**.</span><span class="sxs-lookup"><span data-stu-id="aa975-121">If you execute a query from a permanent **QueryDef** object, the query will run faster than if you run the equivalent SQL statement from the **OpenRecordset** method.</span></span> <span data-ttu-id="aa975-122">Это объясняется тем, что ядру СУБД Microsoft Access не нужно компилировать запрос перед его выполнением.</span><span class="sxs-lookup"><span data-stu-id="aa975-122">This is because the Microsoft Access database engine doesn't need to compile the query before executing it.</span></span>

<span data-ttu-id="aa975-123">Предпочтительный способ использования диалекта SQL внешнего ядра СУБД с доступом через ядро СУБД Microsoft Access состоит в применении объектов **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="aa975-123">The preferred way to use the native SQL dialect of an external database engine accessed through the Microsoft Access database engine is through **QueryDef** objects.</span></span> <span data-ttu-id="aa975-124">Например, можно создать запрос Microsoft SQL Server и сохранить его в объекте **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="aa975-124">For example, you can create a Microsoft SQL Server query and store it in a **QueryDef** object.</span></span> <span data-ttu-id="aa975-125">Если нужно использовать запрос SQL не на основе ядра СУБД Microsoft Access, потребуется предоставить строку свойства **Connect**, указывающую на внешний источник данных.</span><span class="sxs-lookup"><span data-stu-id="aa975-125">When you need to use a non-Microsoft Access database engine SQL query, you must provide a **Connect** property string that points to the external data source.</span></span> <span data-ttu-id="aa975-126">Запросы с допустимыми свойствами **Connect** обходят ядро СУБД Microsoft Access и передаются непосредственно к серверу внешней базы данных для обработки.</span><span class="sxs-lookup"><span data-stu-id="aa975-126">Queries with valid **Connect** properties bypass the Microsoft Access database engine and pass the query directly to the external database server for processing.</span></span>

<span data-ttu-id="aa975-127">Чтобы создать новый объект **QueryDef**, используйте метод **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="aa975-127">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="aa975-128">В рабочей области Microsoft Access, если указать строку для аргумента имени или явно задать строку ненулевой длины в качестве значения свойства **Name** нового объекта **QueryDef**, будет создан постоянный объект **QueryDef**, который будет автоматически добавлен в коллекцию **QueryDefs** и сохранен на диске.</span><span class="sxs-lookup"><span data-stu-id="aa975-128">In a Microsoft Access workspace, if you supply a string for the name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non–zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="aa975-129">Если указать строку ненулевой длины в качестве аргумента имени или явно задать строку нулевой длины в качестве значения свойства **Name**, будет создан временный объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="aa975-129">Supplying a zero-length string as the name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="aa975-130">Чтобы сослаться на объект **QueryDef** в коллекции по его порядковому номеру или по его свойству **Name**, используйте любую из указанных ниже синтаксических форм.</span><span class="sxs-lookup"><span data-stu-id="aa975-130">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="aa975-131">QueryDefs(0)</span><span class="sxs-lookup"><span data-stu-id="aa975-131">QueryDefs(0)</span></span>

<span data-ttu-id="aa975-132">QueryDefs("name")</span><span class="sxs-lookup"><span data-stu-id="aa975-132">QueryDefsname</span></span>

<span data-ttu-id="aa975-133">QueryDefs\!\[ name\]</span><span class="sxs-lookup"><span data-stu-id="aa975-133">QueryDefs\!\[ name\]</span></span>

<span data-ttu-id="aa975-134">Ссылаться на временные объекты **QueryDef** можно только по назначенным им объектным переменным.</span><span class="sxs-lookup"><span data-stu-id="aa975-134">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

<span data-ttu-id="aa975-135">**Ссылка, предоставляемая** сообществом [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="aa975-135">**Link provided byCommunity Member Icon** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="aa975-136">UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="aa975-136">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="aa975-137">Запросы: документирование SQL в Word</span><span class="sxs-lookup"><span data-stu-id="aa975-137">Queries: Document SQL to Word</span></span>](https://www.utteraccess.com/wiki/index.php/queries:_document_sql_to_word)

## <a name="example"></a><span data-ttu-id="aa975-138">Пример</span><span class="sxs-lookup"><span data-stu-id="aa975-138">Example</span></span>

<span data-ttu-id="aa975-139">В этом примере создается новый объект **QueryDef**, который добавляется в коллекцию **QueryDefs** объекта **Database** компании Northwind.</span><span class="sxs-lookup"><span data-stu-id="aa975-139">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object.</span></span> <span data-ttu-id="aa975-140">Затем выполняется перечисление коллекции **QueryDefs** и коллекции **Properties** нового объекта **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="aa975-140">It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

```vb
    Sub QueryDefX() 
     
       Dim dbsNorthwind As Database 
       Dim qdfNew As QueryDef 
       Dim qdfLoop As QueryDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new QueryDef object. Because it has a  
       ' name, it is automatically appended to the  
       ' QueryDefs collection. 
       Set qdfNew = dbsNorthwind.CreateQueryDef("NewQueryDef", _ 
             "SELECT * FROM Categories") 
     
       With dbsNorthwind 
          Debug.Print .QueryDefs.Count & _ 
             " QueryDefs in " & .Name 
     
          ' Enumerate QueryDefs collection. 
          For Each qdfLoop In .QueryDefs 
             Debug.Print "  " & qdfLoop.Name 
          Next qdfLoop 
     
          With qdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new  
             ' QueryDef object. 
             For Each prpLoop In .Properties 
                On Error Resume Next 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
                On Error Goto 0 
             Next prpLoop 
          End With 
     
          ' Delete new QueryDef because this is a  
          ' demonstration. 
          .QueryDefs.Delete qdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="aa975-141">В этом примере используется метод **CreateQueryDef**, чтобы создать и выполнить временный и постоянный объекты **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="aa975-141">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="aa975-142">Функция GetrstTemp необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="aa975-142">The GetrstTemp function is required for this procedure to run.</span></span>

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

<span data-ttu-id="aa975-143">В следующем примере показано, как заменить инструкцию SQL в сохраненном запросе.</span><span class="sxs-lookup"><span data-stu-id="aa975-143">The following example shows how to replace the Structured Query Language (SQL) statement in a saved query.</span></span>

<span data-ttu-id="aa975-144">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="aa975-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    ‘To change the Where clause in a saved query  
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

