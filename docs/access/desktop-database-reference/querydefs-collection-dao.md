---
title: QueryDefs Collection (DAO)
TOCTitle: QueryDefs Collection
ms:assetid: 6178c3a6-8301-16bf-4657-0fb113de0a36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194892(v=office.15)
ms:contentKeyID: 48545215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f210497a541efa40d8ddf2e5bfd43637706efce8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867449"
---
# <a name="querydefs-collection-dao"></a><span data-ttu-id="54c9c-102">QueryDefs Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="54c9c-102">QueryDefs Collection (DAO)</span></span>

<span data-ttu-id="54c9c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54c9c-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="54c9c-104">Коллекция **QueryDefs** содержит все объекты **QueryDef** объекта **базы данных** в базе данных ядра базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="54c9c-104">A **QueryDefs** collection contains all **QueryDef** objects of a **Database** object in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="54c9c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="54c9c-105">Remarks</span></span>

<span data-ttu-id="54c9c-106">Чтобы создать новый объект **QueryDef** , используйте метод **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="54c9c-106">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="54c9c-107">В рабочей области Microsoft Access Если указать строку для аргумента имени или явно задать свойство **Name** нового объекта **QueryDef** не – пустую строку будет создать постоянное **QueryDef** , который будет автоматически в коллекцию **QueryDefs** и на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="54c9c-107">In a Microsoft Access workspace, if you supply a string for the name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non–zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="54c9c-108">Временные объекта **QueryDef** приведет к передав строку нулевой длины в качестве аргумента имя и явно установки свойства **Name** в строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="54c9c-108">Supplying a zero-length string as the name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="54c9c-109">Для ссылки на объект **QueryDef** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="54c9c-109">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="54c9c-110">**QueryDefs** (0)</span><span class="sxs-lookup"><span data-stu-id="54c9c-110">**QueryDefs**(0)</span></span>

<span data-ttu-id="54c9c-111">**QueryDefs** («имя»)</span><span class="sxs-lookup"><span data-stu-id="54c9c-111">**QueryDefs**("name")</span></span>

<span data-ttu-id="54c9c-112">**QueryDefs**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="54c9c-112">**QueryDefs**\!\[name\]</span></span>

<span data-ttu-id="54c9c-113">Можно ссылаться на временные объекты **QueryDef** только с объектных переменных, назначенных им.</span><span class="sxs-lookup"><span data-stu-id="54c9c-113">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

## <a name="example"></a><span data-ttu-id="54c9c-114">Пример</span><span class="sxs-lookup"><span data-stu-id="54c9c-114">Example</span></span>

<span data-ttu-id="54c9c-115">В этом примере создается новый объект **QueryDef** и добавляет его в коллекцию **QueryDefs** объекта данных Northwind **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="54c9c-115">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object.</span></span> <span data-ttu-id="54c9c-116">Затем выполняется перечисление коллекции **QueryDefs** и коллекции **свойств** нового **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="54c9c-116">It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

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

<span data-ttu-id="54c9c-117">В этом примере используется метод **CreateQueryDef** для создания и выполнения временное и постоянное **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="54c9c-117">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="54c9c-118">Функция GetrstTemp является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="54c9c-118">The GetrstTemp function is required for this procedure to run.</span></span>

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

Приведенный ниже показано, как выполнить запрос параметра. <span data-ttu-id="54c9c-120">Коллекции параметров используется для задания параметра организации запроса myActionQuery до выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="54c9c-120">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="54c9c-121">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="54c9c-121">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Sub ExecParameterQuery()
    
        Dim dbs As DAO.Database
        Dim qdf As DAO.QueryDef
    
        Set dbs = CurrentDb
        Set qdf = dbs.QueryDefs("myActionQuery")
    
        'Set the value of the QueryDef's parameter
        qdf.Parameters("Organization").Value = "Microsoft"
    
        'Execute the query
        qdf.Execute dbFailOnError
    
        'Clean up
        qdf.Close
        Set qdf = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="54c9c-122">Следующем примере показано, как открыть записей, основанный на параметр запроса.</span><span class="sxs-lookup"><span data-stu-id="54c9c-122">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

