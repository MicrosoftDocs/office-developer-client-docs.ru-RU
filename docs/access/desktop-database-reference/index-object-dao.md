---
title: Объект index — объекты доступа к данным (DAO)
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
# <a name="index-object-dao"></a><span data-ttu-id="8dbdd-102">Объект index (DAO)</span><span class="sxs-lookup"><span data-stu-id="8dbdd-102">Index object (DAO)</span></span>

<span data-ttu-id="8dbdd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8dbdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8dbdd-104">Объект **index** указывает порядок записей, доступ к которым осуществляется из таблиц базы данных, а также сведения о том, принимаются ли повторяющиеся записи, что обеспечивает эффективный доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-104">**Index** objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data.</span></span> <span data-ttu-id="8dbdd-105">Для внешних баз данных объекты **index** описывают индексы, установленные для внешних таблиц (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8dbdd-105">For external databases, **Index** objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="8dbdd-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="8dbdd-106">Remarks</span></span>

<span data-ttu-id="8dbdd-107">Ядро СУБД Microsoft Access использует индексы при присоединении таблиц и создании объектов **[Recordset](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-107">The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects.</span></span> <span data-ttu-id="8dbdd-108">Индексы определяют порядок, в котором объекты **Recordset** табличного типа возвращают записи, но не определяют порядок, в котором ядро СУБД Microsoft Access хранит записи в базовой таблице, или порядок, в котором любой другой тип **набора записей** объект возвращает записи.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-108">Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.</span></span>

<span data-ttu-id="8dbdd-109">С помощью объекта **index** можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8dbdd-109">With an **Index** object, you can:</span></span>

- <span data-ttu-id="8dbdd-110">Используйте свойство **Required** , чтобы определить, требуются ли для объектов **[field](field-object-dao.md)** в индексе значения, которые не равны NULL, а затем используйте свойство **игноренуллс** , чтобы определить, имеют ли значения NULL элементы индекса.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-110">Use the **Required** property to determine whether the **[Field](field-object-dao.md)** objects in the index require values that are not Null, and then use the **IgnoreNulls** property to determine whether the null values have index entries.</span></span>

- <span data-ttu-id="8dbdd-111">Используйте свойства **PRIMARY** и **UNIQUE** для определения порядка и уникальности объекта **index** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-111">Use the **Primary** and **Unique** properties to determine the ordering and uniqueness of the **Index** object.</span></span>

<span data-ttu-id="8dbdd-112">Ядро СУБД Microsoft Access автоматически обслуживает все индексы базовых таблиц.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-112">The Microsoft Access database engine maintains all base table indexes automatically.</span></span> <span data-ttu-id="8dbdd-113">Он обновляет индексы при каждом добавлении, изменении или удалении записей из базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-113">It updates indexes whenever you add, change, or delete records from the base table.</span></span> <span data-ttu-id="8dbdd-114">Когда вы создадите базу данных, используйте метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** периодически для получения статистики индекса в актуальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-114">Once you create the database, use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method periodically to bring index statistics up-to-date.</span></span>

<span data-ttu-id="8dbdd-115">При доступе к объекту **Recordset** табличного типа необходимо указать порядок записей с помощью свойства **index** объекта.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-115">When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property.</span></span> <span data-ttu-id="8dbdd-116">ПриСвойте этому свойству значение свойства **Name** существующего **индекса** в коллекции **indexes** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-116">Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection.</span></span> <span data-ttu-id="8dbdd-117">Эта коллекция находится в объекте **[tabledef](tabledef-object-dao.md)** , базовом объекте **Recordset** , который вы заполняете.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-117">This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.</span></span>

> [!NOTE]
> <span data-ttu-id="8dbdd-118">Вам не нужно создавать индексы для таблицы, но для больших неиндексированных таблиц доступ к определенной записи или обработка соединений может занять длительное время.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-118">You don't have to create indexes for a table, but for large, unindexed tables, accessing a specific record or processing joins can take a long time.</span></span> <span data-ttu-id="8dbdd-119">С другой стороны, наличие слишком большого количества индексов может замедлить обновление базы данных по мере уточнения каждого индекса таблицы.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-119">Conversely, having too many indexes can slow down updates to the database as each of the table indexes is amended.</span></span>

<span data-ttu-id="8dbdd-120">Свойство **[Attributes](field-attributes-property-dao.md)** каждого объекта **field** в индексе определяет порядок возврата записей и, соответственно, определяет методы доступа, которые необходимо использовать для этого индекса.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-120">The **[Attributes](field-attributes-property-dao.md)** property of each **Field** object in the index determines the order of records returned and consequently determines which access techniques to use for that index.</span></span>

<span data-ttu-id="8dbdd-121">Каждый объект **field** в коллекции **Fields** объекта **index** является компонентом индекса.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-121">Each **Field** object in the **Fields** collection of an **Index** object is a component of the index.</span></span> <span data-ttu-id="8dbdd-122">Чтобы определить новый объект **index** , задайте его свойства перед добавлением в коллекцию, сделав объект **индекса** доступным для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-122">To define a new **Index** object, set its properties before you append it to a collection, making the **Index** object available for subsequent use.</span></span>

> [!NOTE]
> <span data-ttu-id="8dbdd-123">Значение свойства **Name** существующего **индекса** можно изменить только в том случае, если значение свойства **[обновляемого](connection-updatable-property-dao.md)** объекта **tabledef** равно **true**.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-123">You can modify the **Name** property setting of an existing **Index** object only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="8dbdd-124">При задании первичного ключа для таблицы ядро СУБД Microsoft Access автоматически определяет его как первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-124">When you set a primary key for a table, the Microsoft Access database engine automatically defines it as the primary index.</span></span> <span data-ttu-id="8dbdd-125">Первичный индекс состоит из одного или нескольких полей, которые уникально идентифицируют все записи в таблице в предварительно заданном порядке.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-125">A primary index consists of one or more fields that uniquely identify all records in a table in a predefined order.</span></span> <span data-ttu-id="8dbdd-126">Так как поле основного индекса должно быть уникальным, ядро СУБД Microsoft Access автоматически устанавливает **значение true**для свойства **UNIQUE** объекта основного **индекса** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-126">Because the primary index field must be unique, the Microsoft Access database engine automatically sets the **Unique** property of the primary **Index** object to **True**.</span></span> <span data-ttu-id="8dbdd-127">Если первичный индекс состоит из нескольких полей, каждое поле может содержать повторяющиеся значения, но комбинация значений из всех индексированных полей должна быть уникальной.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-127">If the primary index consists of more than one field, each field can contain duplicate values, but the combination of values from all the indexed fields must be unique.</span></span> <span data-ttu-id="8dbdd-128">Первичный индекс состоит из ключа для таблицы и всегда состоит из тех же полей, что и первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-128">A primary index consists of a key for the table and is always made up of the same fields as the primary key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8dbdd-129">Убедитесь, что данные соответствуют атрибутам нового индекса.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-129">Make sure your data complies with the attributes of your new index.</span></span> <span data-ttu-id="8dbdd-130">Если для индекса требуются уникальные значения, убедитесь, что в существующих записях данных нет дубликатов.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-130">If your index requires unique values, make sure that there are no duplicates in existing data records.</span></span> <span data-ttu-id="8dbdd-131">Если дубликаты существуют, ядро СУБД Microsoft Access не может создать индекс; При попытке использовать метод Append для нового индекса возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-131">If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

<span data-ttu-id="8dbdd-132">При создании связи, которая применяет целостность ссылок, ядро СУБД Microsoft Access автоматически создает индекс с **внешним** свойством, установленным в качестве внешнего ключа в ссылающейся таблице.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-132">When you create a relationship that enforces referential integrity, the Microsoft Access database engine automatically creates an index with the **Foreign** property, set as the foreign key in the referencing table.</span></span> <span data-ttu-id="8dbdd-133">После установления связи таблицы ядро СУБД Microsoft Access предотвращает добавление или изменение базы данных, которая нарушает эту связь.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-133">After you've established a table relationship, the Microsoft Access database engine prevents additions or changes to the database that violate that relationship.</span></span> <span data-ttu-id="8dbdd-134">Если задать для свойства **Attributes** объекта **[relation](relation-object-dao.md)** разрешение каскадных обновлений и каскадных удаленИй, ядро СУБД Microsoft Access обновляет или удаляет записи в связанных таблицах автоматически.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-134">If you set the **Attributes** property of the **[Relation](relation-object-dao.md)** object to allow cascading updates and cascading deletes, the Microsoft Access database engine updates or deletes records in related tables automatically.</span></span>

1.  <span data-ttu-id="8dbdd-135">Используйте метод **креатеиндекс** для объекта **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-135">Use the **CreateIndex** method on a **TableDef** object.</span></span>

2.  <span data-ttu-id="8dbdd-136">Используйте метод **CreateField** для объекта **index** , чтобы создать объект **field** для каждого поля (столбца), включаемого в объект **index** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-136">Use the **CreateField** method on the **Index** object to create a **Field** object for each field (column) to be included in the **Index** object.</span></span>

3.  <span data-ttu-id="8dbdd-137">Задайте свойства **индекса** по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-137">Set **Index** properties as needed.</span></span>

4.  <span data-ttu-id="8dbdd-138">Добавьте объект **field** в коллекцию **Fields** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-138">Append the **Field** object to the **Fields** collection.</span></span>

5.  <span data-ttu-id="8dbdd-139">Добавьте объект **index** в коллекцию **indexes** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-139">Append the **Index** object to the **Indexes** collection.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8dbdd-140">Свойство **Clustered** игнорируется для баз данных, использующих ядро СУБД Microsoft Access, которое не поддерживает кластеризованные индексы.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-140">The **Clustered** property is ignored for databases that use the Microsoft Access database engine, which doesn't support clustered indexes.</span></span>

## <a name="example"></a><span data-ttu-id="8dbdd-141">Пример</span><span class="sxs-lookup"><span data-stu-id="8dbdd-141">Example</span></span>

<span data-ttu-id="8dbdd-142">В этом примере создается новый объект **index** , который добавляется в коллекцию **indexes** для Employees **tabledef**, а затем перечисляет коллекцию **indexes** объекта **tabledef**.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-142">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**.</span></span> <span data-ttu-id="8dbdd-143">Наконец, он перечисляет **набор записей**, сначала используя первичный **индекс**, а затем с помощью нового **индекса**.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-143">Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**.</span></span> <span data-ttu-id="8dbdd-144">Для выполнения этой процедуры требуется процедура Индексаутпут.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-144">The IndexOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="8dbdd-145">В этом примере используется метод **креатеиндекс** для создания двух новых объектов **индекса** , а затем они добавляются в коллекцию **indexes** объекта Employees **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-145">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="8dbdd-146">Затем выполняется перечисление \*\*\*\* коллекции индексов объекта **tabledef** , коллекции **Fields** новых объектов **index** и коллекции свойств новых объектов **index** .</span><span class="sxs-lookup"><span data-stu-id="8dbdd-146">It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="8dbdd-147">Для выполнения этой процедуры требуется функция Креатеиндексаутпут.</span><span class="sxs-lookup"><span data-stu-id="8dbdd-147">The CreateIndexOutput function is required for this procedure to run.</span></span>

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
