---
title: Коллекция QueryDefs (DAO)
TOCTitle: QueryDefs Collection
ms:assetid: 6178c3a6-8301-16bf-4657-0fb113de0a36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194892(v=office.15)
ms:contentKeyID: 48545215
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 3543d882e0584c35c88a5475032d9fe5505f516c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303236"
---
# <a name="querydefs-collection-dao"></a><span data-ttu-id="4c4e0-102">Коллекция QueryDefs (DAO)</span><span class="sxs-lookup"><span data-stu-id="4c4e0-102">QueryDefs collection (DAO)</span></span>

<span data-ttu-id="4c4e0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c4e0-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="4c4e0-104">Коллекция **QueryDefs** содержит все объекты **QueryDef** объекта **Database** в базе данных ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-104">A **QueryDefs** collection contains all **QueryDef** objects of a **Database** object in a Microsoft Access database engine database.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4e0-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="4c4e0-105">Remarks</span></span>

<span data-ttu-id="4c4e0-106">Чтобы создать новый объект **QueryDef**, используйте метод **CreateQueryDef**.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-106">To create a new **QueryDef** object, use the **CreateQueryDef** method.</span></span> <span data-ttu-id="4c4e0-107">В рабочей области Microsoft Access, если указать строку для аргумента имени или явно задать строку ненулевой длины в качестве значения свойства **Name** нового объекта **QueryDef**, будет создан постоянный объект **QueryDef**, который будет автоматически добавлен в коллекцию **QueryDefs** и сохранен на диске.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-107">In a Microsoft Access workspace, if you supply a string for the name argument or if you explicitly set the **Name** property of the new **QueryDef** object to a non–zero-length string, you will create a permanent **QueryDef** that will automatically be appended to the **QueryDefs** collection and saved to disk.</span></span> <span data-ttu-id="4c4e0-108">Если указать строку ненулевой длины в качестве аргумента имени или явно задать строку нулевой длины в качестве значения свойства **Name**, будет создан временный объект **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-108">Supplying a zero-length string as the name argument or explicitly setting the **Name** property to a zero-length string will result in a temporary **QueryDef** object.</span></span>

<span data-ttu-id="4c4e0-109">Чтобы сослаться на объект **QueryDef** в коллекции по его порядковому номеру или по его свойству **Name**, используйте любую из указанных ниже синтаксических форм.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-109">To refer to a **QueryDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="4c4e0-110">**QueryDefs**(0)</span><span class="sxs-lookup"><span data-stu-id="4c4e0-110">**QueryDefs**(0)</span></span>

<span data-ttu-id="4c4e0-111">**QueryDefs**("имя")</span><span class="sxs-lookup"><span data-stu-id="4c4e0-111">**QueryDefs**("name")</span></span>

<span data-ttu-id="4c4e0-112">**QueryDefs**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="4c4e0-112">**QueryDefs**\!\[name\]</span></span>

<span data-ttu-id="4c4e0-113">Ссылаться на временные объекты **QueryDef** можно только по назначенным им объектным переменным.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-113">You can refer to temporary **QueryDef** objects only by the object variables that you have assigned to them.</span></span>

## <a name="example"></a><span data-ttu-id="4c4e0-114">Пример</span><span class="sxs-lookup"><span data-stu-id="4c4e0-114">Example</span></span>

<span data-ttu-id="4c4e0-115">В этом примере создается новый объект **QueryDef**, который добавляется в коллекцию **QueryDefs** объекта **Database** компании Northwind.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-115">This example creates a new **QueryDef** object and appends it to the **QueryDefs** collection of the Northwind **Database** object.</span></span> <span data-ttu-id="4c4e0-116">Затем выполняется перечисление коллекции **QueryDefs** и коллекции **Properties** нового объекта **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-116">It then enumerates the **QueryDefs** collection and the **Properties** collection of the new **QueryDef**.</span></span>

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

<span data-ttu-id="4c4e0-117">В этом примере используется метод **CreateQueryDef**, чтобы создать и выполнить временный и постоянный объекты **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-117">This example uses the **CreateQueryDef** method to create and execute both a temporary and a permanent **QueryDef**.</span></span> <span data-ttu-id="4c4e0-118">Функция GetrstTemp необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-118">The GetrstTemp function is required for this procedure to run.</span></span>

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

В приведенном ниже примере показано, как выполнить запрос параметра. <span data-ttu-id="4c4e0-120">Коллекция Parameters используется, чтобы задать параметр Organization запроса myActionQuery перед его выполнением.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-120">The Parameters collection is used to set the Organization parameter of the myActionQuery query before the query is executed.</span></span>

<span data-ttu-id="4c4e0-121">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4c4e0-121">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="4c4e0-122">В приведенном ниже примере показано, как открыть объект Recordset на основании запроса параметра.</span><span class="sxs-lookup"><span data-stu-id="4c4e0-122">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

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

