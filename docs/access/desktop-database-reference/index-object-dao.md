---
title: Объект Index — объекты доступа к данным (DAO)
TOCTitle: Index object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca0a975017b5c5396d23817716689b37433d8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291770"
---
# <a name="index-object-dao"></a><span data-ttu-id="51f7e-102">Объект Index (DAO)</span><span class="sxs-lookup"><span data-stu-id="51f7e-102">Index object (DAO)</span></span>

<span data-ttu-id="51f7e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51f7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51f7e-104">**Объекты** индекса определяют порядок записей, доступных из таблиц баз данных, а также то, принимаются ли дублирующиеся записи, обеспечивая эффективный доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="51f7e-104">**Index** objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data.</span></span> <span data-ttu-id="51f7e-105">Для внешних баз данных **объекты индекса** описывают индексы, установленные для внешних таблиц (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="51f7e-105">For external databases, **Index** objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="51f7e-106">Заметки</span><span class="sxs-lookup"><span data-stu-id="51f7e-106">Remarks</span></span>

<span data-ttu-id="51f7e-107">Ядр баз данных Microsoft Access использует индексы при присоединении к таблицам и создании объектов **[Recordset.](recordset-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="51f7e-107">The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects.</span></span> <span data-ttu-id="51f7e-108">Индексы определяют порядок, в котором объекты **Recordset** табли-типа возвращают записи, но не определяют порядок, в котором ядр баз данных Microsoft Access хранит записи в базовой таблице, или порядок, в котором любой другой тип объекта **Recordset** возвращает записи.</span><span class="sxs-lookup"><span data-stu-id="51f7e-108">Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.</span></span>

<span data-ttu-id="51f7e-109">С помощью **объекта Index** вы можете:</span><span class="sxs-lookup"><span data-stu-id="51f7e-109">With an **Index** object, you can:</span></span>

- <span data-ttu-id="51f7e-110">Используйте свойство **Required,** чтобы определить, требуются ли для объектов **[Field](field-object-dao.md)** в индексе значения, которые не являются NULL, а затем используйте свойство **IgnoreNulls,** чтобы определить, есть ли в значениях null записи индекса.</span><span class="sxs-lookup"><span data-stu-id="51f7e-110">Use the **Required** property to determine whether the **[Field](field-object-dao.md)** objects in the index require values that are not Null, and then use the **IgnoreNulls** property to determine whether the null values have index entries.</span></span>

- <span data-ttu-id="51f7e-111">Используйте свойства **Primary** **и Unique,** чтобы определить порядок и уникальность объекта **Index.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-111">Use the **Primary** and **Unique** properties to determine the ordering and uniqueness of the **Index** object.</span></span>

<span data-ttu-id="51f7e-112">Яд баз данных Microsoft Access автоматически поддерживает все индексы базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="51f7e-112">The Microsoft Access database engine maintains all base table indexes automatically.</span></span> <span data-ttu-id="51f7e-113">Он обновляет индексы при добавлении, изменении или удалении записей из базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="51f7e-113">It updates indexes whenever you add, change, or delete records from the base table.</span></span> <span data-ttu-id="51f7e-114">После создания базы данных периодически используйте **[метод CompactDatabase,](dbengine-compactdatabase-method-dao.md)** чтобы привести статистику индекса в последние данные.</span><span class="sxs-lookup"><span data-stu-id="51f7e-114">Once you create the database, use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method periodically to bring index statistics up-to-date.</span></span>

<span data-ttu-id="51f7e-115">При доступе к объекту **Recordset табли** с типом таблицы вы указываете порядок записей с помощью свойства **Index** объекта.</span><span class="sxs-lookup"><span data-stu-id="51f7e-115">When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property.</span></span> <span data-ttu-id="51f7e-116">Установите для этого свойства параметр **свойства Name** существующего объекта **Index** в коллекции **Indexes.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-116">Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection.</span></span> <span data-ttu-id="51f7e-117">Эта коллекция содержится **[объектом TableDef,](tabledef-object-dao.md)** который является объектом **Recordset,** который вы заполняете.</span><span class="sxs-lookup"><span data-stu-id="51f7e-117">This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.</span></span>

> [!NOTE]
> <span data-ttu-id="51f7e-118">Вам не нужно создавать индексы для таблицы, но для больших неиндексных таблиц доступ к определенной записи или обработке присоединения может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="51f7e-118">You don't have to create indexes for a table, but for large, unindexed tables, accessing a specific record or processing joins can take a long time.</span></span> <span data-ttu-id="51f7e-119">И наоборот, слишком большое количество индексов может замедлить обновление базы данных по мере изменения каждого индекса таблицы.</span><span class="sxs-lookup"><span data-stu-id="51f7e-119">Conversely, having too many indexes can slow down updates to the database as each of the table indexes is amended.</span></span>

<span data-ttu-id="51f7e-120">Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **Field** в индексе определяет порядок возвращаемой записи и, следовательно, определяет, какие методы доступа использовать для этого индекса.</span><span class="sxs-lookup"><span data-stu-id="51f7e-120">The **[Attributes](field-attributes-property-dao.md)** property of each **Field** object in the index determines the order of records returned and consequently determines which access techniques to use for that index.</span></span>

<span data-ttu-id="51f7e-121">Каждый **объект** **Field** в коллекции Fields объекта **Index** является компонентом индекса.</span><span class="sxs-lookup"><span data-stu-id="51f7e-121">Each **Field** object in the **Fields** collection of an **Index** object is a component of the index.</span></span> <span data-ttu-id="51f7e-122">Чтобы определить новый **объект Index,** задав его свойства перед его приложением к коллекции, сделав объект **Index** доступным для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="51f7e-122">To define a new **Index** object, set its properties before you append it to a collection, making the **Index** object available for subsequent use.</span></span>

> [!NOTE]
> <span data-ttu-id="51f7e-123">Параметр свойства **Name** существующего объекта **Index** можно изменить только в том случае, если для параметра свойства **[Updatable](connection-updatable-property-dao.md)** содержащегося объекта **TableDef** задайте **true.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-123">You can modify the **Name** property setting of an existing **Index** object only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="51f7e-124">При наборе первичного ключа для таблицы яма базы данных Microsoft Access автоматически определяет его в качестве основного индекса.</span><span class="sxs-lookup"><span data-stu-id="51f7e-124">When you set a primary key for a table, the Microsoft Access database engine automatically defines it as the primary index.</span></span> <span data-ttu-id="51f7e-125">Основной индекс состоит из одного или нескольких полей, которые уникальным образом идентифицируют все записи в таблице в предопределеном порядке.</span><span class="sxs-lookup"><span data-stu-id="51f7e-125">A primary index consists of one or more fields that uniquely identify all records in a table in a predefined order.</span></span> <span data-ttu-id="51f7e-126">Поскольку основное поле индекса должно быть уникальным, яма базы данных Microsoft Access автоматически задает для свойства **Unique** основного объекта **Index** **true**.</span><span class="sxs-lookup"><span data-stu-id="51f7e-126">Because the primary index field must be unique, the Microsoft Access database engine automatically sets the **Unique** property of the primary **Index** object to **True**.</span></span> <span data-ttu-id="51f7e-127">Если основной индекс состоит из нескольких полей, каждое поле может содержать повторяющиеся значения, но сочетание значений из всех индексных полей должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="51f7e-127">If the primary index consists of more than one field, each field can contain duplicate values, but the combination of values from all the indexed fields must be unique.</span></span> <span data-ttu-id="51f7e-128">Основной индекс состоит из ключа таблицы и всегда состоит из тех же полей, что и первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="51f7e-128">A primary index consists of a key for the table and is always made up of the same fields as the primary key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51f7e-129">Убедитесь, что данные соответствуют атрибутам нового индекса.</span><span class="sxs-lookup"><span data-stu-id="51f7e-129">Make sure your data complies with the attributes of your new index.</span></span> <span data-ttu-id="51f7e-130">Если индексу требуются уникальные значения, убедитесь, что в существующих записях данных нет дубликатов.</span><span class="sxs-lookup"><span data-stu-id="51f7e-130">If your index requires unique values, make sure that there are no duplicates in existing data records.</span></span> <span data-ttu-id="51f7e-131">Если дубликаты существуют, яма базы данных Microsoft Access не может создать индекс; захватимые результаты ошибки при попытке использовать метод Append в новом индексе.</span><span class="sxs-lookup"><span data-stu-id="51f7e-131">If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

<span data-ttu-id="51f7e-132">При создании отношения, которое обеспечивает целостность ссылок, яма базы данных Microsoft Access автоматически создает индекс со свойством **Foreign,** задав его в качестве внешнего ключа в таблице ссылок.</span><span class="sxs-lookup"><span data-stu-id="51f7e-132">When you create a relationship that enforces referential integrity, the Microsoft Access database engine automatically creates an index with the **Foreign** property, set as the foreign key in the referencing table.</span></span> <span data-ttu-id="51f7e-133">После того как вы установили отношение таблицы, яма базы данных Microsoft Access предотвращает добавления или изменения в базу данных, нарушающие эти отношения.</span><span class="sxs-lookup"><span data-stu-id="51f7e-133">After you've established a table relationship, the Microsoft Access database engine prevents additions or changes to the database that violate that relationship.</span></span> <span data-ttu-id="51f7e-134">Если вы установите для свойства **Attributes** объекта **[Relation](relation-object-dao.md)** разрешение каскадных обновлений и каскадных удалений, обдвижка базы данных Microsoft Access автоматически обновляет или удаляет записи в связанных таблицах.</span><span class="sxs-lookup"><span data-stu-id="51f7e-134">If you set the **Attributes** property of the **[Relation](relation-object-dao.md)** object to allow cascading updates and cascading deletes, the Microsoft Access database engine updates or deletes records in related tables automatically.</span></span>

1.  <span data-ttu-id="51f7e-135">Используйте метод **CreateIndex** для объекта **TableDef.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-135">Use the **CreateIndex** method on a **TableDef** object.</span></span>

2.  <span data-ttu-id="51f7e-136">Используйте метод **CreateField** в **объекте Index,** чтобы создать объект **Field** для каждого поля (столбца), включаемого в **объект Index.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-136">Use the **CreateField** method on the **Index** object to create a **Field** object for each field (column) to be included in the **Index** object.</span></span>

3.  <span data-ttu-id="51f7e-137">При **необходимости установите** свойства индекса.</span><span class="sxs-lookup"><span data-stu-id="51f7e-137">Set **Index** properties as needed.</span></span>

4.  <span data-ttu-id="51f7e-138">Append the **Field** object to the **Fields** collection.</span><span class="sxs-lookup"><span data-stu-id="51f7e-138">Append the **Field** object to the **Fields** collection.</span></span>

5.  <span data-ttu-id="51f7e-139">Append the **Index** object to the **Indexes** collection.</span><span class="sxs-lookup"><span data-stu-id="51f7e-139">Append the **Index** object to the **Indexes** collection.</span></span>

    > [!NOTE]
    > <span data-ttu-id="51f7e-140">Свойство **Clustered** игнорируется для баз данных, в которых используется ядер баз данных Microsoft Access, который не поддерживает кластерные индексы.</span><span class="sxs-lookup"><span data-stu-id="51f7e-140">The **Clustered** property is ignored for databases that use the Microsoft Access database engine, which doesn't support clustered indexes.</span></span>

## <a name="example"></a><span data-ttu-id="51f7e-141">Пример</span><span class="sxs-lookup"><span data-stu-id="51f7e-141">Example</span></span>

<span data-ttu-id="51f7e-142">В этом примере создается новый объект **Index,** он включается в коллекцию **Indexes** объекта Employees **TableDef,** а затем нумеруется коллекция **Indexes** **объекта TableDef.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-142">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**.</span></span> <span data-ttu-id="51f7e-143">Наконец, он нумерирует набор **записей,** сначала используя основной **индекс,** а затем с помощью нового **индекса.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-143">Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**.</span></span> <span data-ttu-id="51f7e-144">Процедура IndexOutput необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="51f7e-144">The IndexOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="51f7e-145">В этом примере метод **CreateIndex** используется для создания двух новых объектов **Index,** а затем их можно придать коллекции **Indexes** объекта Employees **TableDef.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-145">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="51f7e-146">Затем он нумерирует коллекцию **Indexes** объекта **TableDef,** коллекцию **Fields** новых объектов **Index** и коллекцию свойств новых объектов **Index.**</span><span class="sxs-lookup"><span data-stu-id="51f7e-146">It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="51f7e-147">Для запуска этой процедуры требуется функция CreateIndexOutput.</span><span class="sxs-lookup"><span data-stu-id="51f7e-147">The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
