---
title: Свойство Recordset2.Index (DAO)
TOCTitle: Index Property
ms:assetid: 614bdf53-aca3-25ef-a23c-50095b345d20
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194872(v=office.15)
ms:contentKeyID: 48545209
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05a29ff9dbe720fe7c5539639b20e0abdc3c587b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307303"
---
# <a name="recordset2index-property-dao"></a><span data-ttu-id="e4b53-102">Свойство Recordset2.Index (DAO)</span><span class="sxs-lookup"><span data-stu-id="e4b53-102">Recordset2.Index property (DAO)</span></span>

<span data-ttu-id="e4b53-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4b53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4b53-104">Задает или возвращает значение, которое указывает имя текущего объекта **[Index](index-object-dao.md)** в объекта **[Recordset](recordset-object-dao.md)** табличного типа (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e4b53-104">Sets or returns a value that indicates the name of the current **[Index](index-object-dao.md)** object in a table-type **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b53-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4b53-105">Syntax</span></span>

<span data-ttu-id="e4b53-106">*expression* .Index</span><span class="sxs-lookup"><span data-stu-id="e4b53-106">*expression* .Index</span></span>

<span data-ttu-id="e4b53-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="e4b53-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b53-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4b53-108">Remarks</span></span>

<span data-ttu-id="e4b53-109">Записи в базовых таблицах не хранятся в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="e4b53-109">Records in base tables aren't stored in any particular order.</span></span> <span data-ttu-id="e4b53-110">Настройка свойства **Index** изменяет порядок записей, возвращаемых из базы данных; оно не влияет на порядок, в котором хранятся записи.</span><span class="sxs-lookup"><span data-stu-id="e4b53-110">Setting the **Index** property changes the order of records returned from the database; it doesn't affect the order in which the records are stored.</span></span>

<span data-ttu-id="e4b53-111">Указанный объект **Index** уже должен быть определен.</span><span class="sxs-lookup"><span data-stu-id="e4b53-111">The specified **Index** object must already be defined.</span></span> <span data-ttu-id="e4b53-112">Если вы задаете свойство **Index** для объекта **Index**, который не существует, или если свойство **Index** не задано при использовании метода **[Seek](recordset2-seek-method-dao.md)**, возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="e4b53-112">If you set the **Index** property to an **Index** object that doesn't exist or if the **Index** property isn't set when you use the **[Seek](recordset2-seek-method-dao.md)** method, a trappable error occurs.</span></span>

<span data-ttu-id="e4b53-113">Ознакомьтесь с коллекцией **Indexes** объекта **TableDef**, чтобы определить, что объекты **Index** доступны для объектов **Recordset** табличного типа, созданных на основе объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="e4b53-113">Examine the **Indexes** collection of a **TableDef** object to determine what **Index** objects are available to table-type **Recordset** objects created from that **TableDef** object.</span></span>

<span data-ttu-id="e4b53-114">Вы можете создать новый индекс для таблицы, создав новый объект **Index**, задав его свойства, добавив его в коллекцию **Indexes** базового объекта **TableDef** и повторно открыв объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e4b53-114">You can create a new index for the table by creating a new **Index** object, setting its properties, appending it to the **Indexes** collection of the underlying **TableDef** object, and then reopening the **Recordset** object.</span></span>

<span data-ttu-id="e4b53-115">Записи, возвращаемые из объекта **Recordset** табличного типа, можно упорядочить только по индексам, заданным для базового объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="e4b53-115">Records returned from a table-type **Recordset** object can be ordered only by the indexes defined for the underlying **TableDef** object.</span></span> <span data-ttu-id="e4b53-116">Чтобы отсортировать записи в другом порядке, можно открыть объект **Recordset** типа dynaset, мгновенный снимок или однонаправленный с помощью оператора SQL с предложением ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="e4b53-116">To sort records in some other order, you can open a dynaset–, snapshot–, or forward–only–type **Recordset** object by using an SQL statement with an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="e4b53-117">Вам не нужно создавать индексы для таблиц.</span><span class="sxs-lookup"><span data-stu-id="e4b53-117">You don't have to create indexes for tables.</span></span> <span data-ttu-id="e4b53-118">Для больших, неиндексированных таблиц доступ к определенной записи или создание объекта **Recordset** может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="e4b53-118">With large, unindexed tables, accessing a specific record or creating a **Recordset** object can take a long time.</span></span> <span data-ttu-id="e4b53-119">С другой стороны, создание слишком большого количества индексов замедляет обновление, добавление и удаление, так как все индексы автоматически обновляются.</span><span class="sxs-lookup"><span data-stu-id="e4b53-119">On the other hand, creating too many indexes slows down update, append, and delete operations because all indexes are automatically updated.</span></span>
> - <span data-ttu-id="e4b53-120">Записи, считываемые из таблиц без индексов, возвращаются без определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="e4b53-120">Records read from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="e4b53-121">Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **[Field](field-object-dao.md)** в объекте **Index** определяет порядок записей и соответственно определяет техники доступа для использования этого индекса.</span><span class="sxs-lookup"><span data-stu-id="e4b53-121">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that index.</span></span>
> - <span data-ttu-id="e4b53-122">Уникальный индекс помогает оптимизировать поиск записей.</span><span class="sxs-lookup"><span data-stu-id="e4b53-122">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="e4b53-123">Индексы не влияют на физический порядок базового объекта tableindexes и влияют только на то, как записи доступны  объекту **Recordset** табли с типом таблицы при выбранном индексе или при его открытом наборе записей.</span><span class="sxs-lookup"><span data-stu-id="e4b53-123">Indexes don't affect the physical order of a base tableindexes affect only how the records are accessed by the table-type **Recordset** object when a particular index is chosen or when **Recordset** is opened.</span></span>

## <a name="example"></a><span data-ttu-id="e4b53-124">Пример</span><span class="sxs-lookup"><span data-stu-id="e4b53-124">Example</span></span>

<span data-ttu-id="e4b53-125">В этом примере используется свойство **Index** для установки другого порядка записей для объекта **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="e4b53-125">This example uses the **Index** property to set different record orders for a table-type **Recordset**.</span></span>

```vb
    Sub IndexPropertyX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim rstEmployees As Recordset2 
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

<span data-ttu-id="e4b53-126">В этом примере показан метод **Seek**, позволяющий пользователю выполнить поиск продукта на основании на номере идентификатора.</span><span class="sxs-lookup"><span data-stu-id="e4b53-126">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset2 
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
