---
title: Свойство Recordset.Index (DAO)
TOCTitle: Index Property
ms:assetid: 54626de0-eb51-31f2-bf24-e29cbfbbaa02
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194103(v=office.15)
ms:contentKeyID: 48544895
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052906
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f475635424cfb9ed8ddab4025d6a944bdedd39fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300527"
---
# <a name="recordsetindex-property-dao"></a><span data-ttu-id="fa237-102">Свойство Recordset.Index (DAO)</span><span class="sxs-lookup"><span data-stu-id="fa237-102">Recordset.Index property (DAO)</span></span>

<span data-ttu-id="fa237-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa237-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa237-104">Задает или возвращает значение, которое указывает имя текущего объекта **[Index](index-object-dao.md)** в объекта **[Recordset](recordset-object-dao.md)** табличного типа (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fa237-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa237-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa237-105">Syntax</span></span>

<span data-ttu-id="fa237-106">*expression* .Index</span><span class="sxs-lookup"><span data-stu-id="fa237-106">*expression* .Index</span></span>

<span data-ttu-id="fa237-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fa237-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa237-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa237-108">Remarks</span></span>

<span data-ttu-id="fa237-109">Записи в базовых таблицах не хранятся в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="fa237-109">Records in base tables aren't stored in any particular order.</span></span> <span data-ttu-id="fa237-110">Настройка свойства **Index** изменяет порядок записей, возвращаемых из базы данных; оно не влияет на порядок, в котором хранятся записи.</span><span class="sxs-lookup"><span data-stu-id="fa237-110">Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="fa237-111">Указанный объект **Index** уже должен быть определен.</span><span class="sxs-lookup"><span data-stu-id="fa237-111">The specified **Index** object must already be defined.</span></span> <span data-ttu-id="fa237-112">Если вы задаете свойство **Index** для объекта **Index**, который не существует, или если свойство **Index** не задано при использовании метода **[Seek](recordset-seek-method-dao.md)**, возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="fa237-112">If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="fa237-113">Ознакомьтесь с коллекцией **Indexes** объекта **TableDef**, чтобы определить, что объекты **Index** доступны для объектов **Recordset** табличного типа, созданных на основе объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="fa237-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="fa237-114">Вы можете создать новый индекс для таблицы, создав новый объект **Index**, задав его свойства, добавив его в коллекцию **Indexes** базового объекта **TableDef** и повторно открыв объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fa237-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="fa237-115">Записи, возвращаемые из объекта **Recordset** табличного типа, можно упорядочить только по индексам, заданным для базового объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="fa237-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="fa237-116">Чтобы отсортировать записи в другом порядке, можно открыть объект **Recordset** типа dynaset, мгновенный снимок или однонаправленный с помощью оператора SQL с предложением ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="fa237-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>


> [!NOTE]
> - <span data-ttu-id="fa237-117">Вам не нужно создавать индексы для таблиц.</span><span class="sxs-lookup"><span data-stu-id="fa237-117">You don't have to create indexes for tables.</span></span> <span data-ttu-id="fa237-118">Для больших, неиндексированных таблиц доступ к определенной записи или создание объекта **Recordset** может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="fa237-118">With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time.</span></span> <span data-ttu-id="fa237-119">С другой стороны, создание слишком большого количества индексов замедляет обновление, добавление и удаление, так как все индексы автоматически обновляются.</span><span class="sxs-lookup"><span data-stu-id="fa237-119">On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="fa237-120">Записи, считываемые из таблиц без индексов, возвращаются без определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="fa237-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="fa237-121">Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **[Field](field-object-dao.md)** в объекте **Index** определяет порядок записей и соответственно определяет техники доступа для использования этого индекса.</span><span class="sxs-lookup"><span data-stu-id="fa237-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="fa237-122">Уникальный индекс помогает оптимизировать поиск записей.</span><span class="sxs-lookup"><span data-stu-id="fa237-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="fa237-123">Индексы не влияют на физический порядок базовой таблицы, индексы влияет только на то, как обеспечивается доступ к записям со стороны объекта **Recordset** табличного типа, когда определенный индекс выбран или открыт объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fa237-123">Indexes don't affect the physical order of a base table, indexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>


## <a name="example"></a><span data-ttu-id="fa237-124">Пример</span><span class="sxs-lookup"><span data-stu-id="fa237-124">Example</span></span>

<span data-ttu-id="fa237-125">В этом примере используется свойство **Index** для установки другого порядка записей для объекта **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="fa237-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset 
       Dim idxLoop As Index 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees") 
       Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
       With rstEmployees 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In tdfEmployees.Indexes 
             .Index = idxLoop.Name 
             Debug.Print "Index = " & .Index 
             Debug.Print "  EmployeeID - PostalCode - Name" 
             .MoveFirst 
     
             ' Enumerate Recordset to show the order of records. 
             Do While Not .EOF 
                Debug.Print "    " & !EmployeeID & " - " & _ 
                   !PostalCode & " - " & !FirstName & " " & _ 
                   !LastName 
                .MoveNext 
             Loop 
     
          Next idxLoop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="fa237-126">В этом примере показан метод **Seek**, позволяющий пользователю выполнить поиск продукта на основании на номере идентификатора.</span><span class="sxs-lookup"><span data-stu-id="fa237-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="fa237-127">В приведенном ниже примере показано, как использовать метод Seek для поиска записи в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="fa237-127">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="fa237-128">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="fa237-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
