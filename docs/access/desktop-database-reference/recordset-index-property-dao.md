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
ms.openlocfilehash: b5f568889d020676be420186b49c9c50c444ee54
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926138"
---
# <a name="recordsetindex-property-dao"></a><span data-ttu-id="43166-102">Свойство Recordset.Index (DAO)</span><span class="sxs-lookup"><span data-stu-id="43166-102">Recordset.Index property (DAO)</span></span>

<span data-ttu-id="43166-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43166-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43166-104">Задает или возвращает значение, указывающее имя текущего объекта **[индекса](index-object-dao.md)** в таблице тип объекта **[набора записей](recordset-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="43166-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="43166-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43166-105">Syntax</span></span>

<span data-ttu-id="43166-106">*выражение* . Индекс</span><span class="sxs-lookup"><span data-stu-id="43166-106">*expression* .Index</span></span>

<span data-ttu-id="43166-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="43166-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="43166-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="43166-108">Remarks</span></span>

<span data-ttu-id="43166-109">Записи в базовые таблицы не сохраняются в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="43166-109">Records in base tables aren't stored in any particular order.</span></span> <span data-ttu-id="43166-110">Свойство **Index** изменяет порядок записей, возвращенных из базы данных; он не влияет на порядок, в котором хранятся записи.</span><span class="sxs-lookup"><span data-stu-id="43166-110">Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="43166-111">Указанный объект **индекса** уже должны быть определены.</span><span class="sxs-lookup"><span data-stu-id="43166-111">The specified **Index** object must already be defined.</span></span> <span data-ttu-id="43166-112">Если значение свойства **Index** объекта **индекса** , не существует или свойства **Index** не задано, при использовании метода **[Seek](recordset-seek-method-dao.md)** , то перехватываемые возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="43166-112">If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="43166-113">Проверьте коллекцию **индексов** **TableDef** объекта, чтобы определить, какие объекты **индекса** доступны для объектов тип таблицы **записей** , создаваемых с помощью этого объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="43166-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="43166-114">Можно создать новый индекс для таблицы путем создания объекта **индекса** , установка ее свойств, добавления в коллекцию **индексов** базового объекта **TableDef** и повторно открыть объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="43166-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="43166-115">Возвращенный объект **набора записей** в таблице типа записи могут быть упорядочены только с помощью индексов, определенных для базового объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="43166-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="43166-116">Чтобы отсортировать записи в некоторые другие порядке, можно открыть динамический набор –, моментальный снимок – или объекта **набора записей** прямого — только — тип с помощью инструкции SQL с предложение ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="43166-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>


> [!NOTE]
> - <span data-ttu-id="43166-117">У вас нет для создания индексов для таблиц.</span><span class="sxs-lookup"><span data-stu-id="43166-117">You don't have to create indexes for tables.</span></span> <span data-ttu-id="43166-118">С большой, неиндексированные таблиц доступ к определенной записи или создание объекта **набора записей** может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="43166-118">With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time.</span></span> <span data-ttu-id="43166-119">С другой стороны, создание слишком много индексов замедляет работу обновления, добавлять и удалять операции, так как все индексы обновляются автоматически.</span><span class="sxs-lookup"><span data-stu-id="43166-119">On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="43166-120">Чтение из таблицы без индексов записи возвращаются в определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="43166-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="43166-121">Свойство **[атрибуты](field-attributes-property-dao.md)** каждого объекта **[поля](field-object-dao.md)** в объекте **индекса** определяет порядок записей и следовательно определяет методы доступа для этого индекса.</span><span class="sxs-lookup"><span data-stu-id="43166-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="43166-122">Уникальный индекс помогает оптимизировать поиск записей.</span><span class="sxs-lookup"><span data-stu-id="43166-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="43166-123">Индексы не влияют на физический порядок базовая таблица индексов влияет только как записи обращением объекта **набора записей** в таблице тип при выборе определенного индекса или при открытии **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="43166-123">Indexes don't affect the physical order of a base table, indexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>


## <a name="example"></a><span data-ttu-id="43166-124">Пример</span><span class="sxs-lookup"><span data-stu-id="43166-124">Example</span></span>

<span data-ttu-id="43166-125">В этом примере используется свойство **индекса** Установка другой записи заказов для табличного типа **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="43166-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

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

<span data-ttu-id="43166-126">В этом примере демонстрируется использование метода **Seek** , позволяя пользователю выполнять поиск по идентификатору продукта.</span><span class="sxs-lookup"><span data-stu-id="43166-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

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

<span data-ttu-id="43166-127">Следующем примере показано, как использовать метод поиска для поиска записей в связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="43166-127">The following example shows how to use the Seek method to find a record in a linked table.</span></span>

<span data-ttu-id="43166-128">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="43166-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
