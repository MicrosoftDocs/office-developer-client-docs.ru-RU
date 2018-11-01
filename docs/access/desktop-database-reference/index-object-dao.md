---
title: Объекты объект индекса - доступ к данным (DAO)
TOCTitle: Index Object
ms:assetid: 92c32cad-ec8a-1243-1d18-83f50b269ecb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197655(v=office.15)
ms:contentKeyID: 48546380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d4ed801dfa746af3ad649738e32cec58afe17f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877081"
---
# <a name="index-object-dao"></a><span data-ttu-id="19ee0-102">Index Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="19ee0-102">Index Object (DAO)</span></span>

<span data-ttu-id="19ee0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19ee0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19ee0-104">Объекты **индекса** указать порядок записей, доступного из таблицы базы данных и принимаются ли повторяющихся записей, предоставляя эффективного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="19ee0-104">**Index** objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data.</span></span> <span data-ttu-id="19ee0-105">Для внешних баз данных объекты **индекса** описывают индексов, установленных для внешних таблиц (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="19ee0-105">For external databases, **Index** objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="19ee0-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="19ee0-106">Remarks</span></span>

<span data-ttu-id="19ee0-107">Ядро базы данных Microsoft Access использует индексы при его соединяет таблицы и создает объекты **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="19ee0-107">The Microsoft Access database engine uses indexes when it joins tables and creates **[Recordset](recordset-object-dao.md)** objects.</span></span> <span data-ttu-id="19ee0-108">Индексов определения порядка, в котором объектов **наборов записей** в таблице тип возврата записей, но они не определяют порядок, в котором хранятся записи в таблице базового ядро базы данных Microsoft Access или порядок, в которых любой другой тип **набора записей** Возвращает объект записей.</span><span class="sxs-lookup"><span data-stu-id="19ee0-108">Indexes determine the order in which table-type **Recordset** objects return records, but they don't determine the order in which the Microsoft Access database engine stores records in the base table or the order in which any other type of **Recordset** object returns records.</span></span>

<span data-ttu-id="19ee0-109">С помощью объекта **индекса** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="19ee0-109">With an **Index** object, you can:</span></span>

- <span data-ttu-id="19ee0-110">Свойство **необходимо** использовать для определения потребность в **[поле](field-object-dao.md)** объекты в индексе значения, которые не являются пустыми и затем свойство **IgnoreNulls** позволяет определить, имеют ли значения null записи индекса.</span><span class="sxs-lookup"><span data-stu-id="19ee0-110">Use the **Required** property to determine whether the **[Field](field-object-dao.md)** objects in the index require values that are not Null, and then use the **IgnoreNulls** property to determine whether the null values have index entries.</span></span>

- <span data-ttu-id="19ee0-111">Использование свойств **основной** и **Unique** для определения порядка и уникальности объекта **индекса** .</span><span class="sxs-lookup"><span data-stu-id="19ee0-111">Use the **Primary** and **Unique** properties to determine the ordering and uniqueness of the **Index** object.</span></span>

<span data-ttu-id="19ee0-112">Ядро базы данных Microsoft Access автоматически сохраняет все индексы базовая таблица.</span><span class="sxs-lookup"><span data-stu-id="19ee0-112">The Microsoft Access database engine maintains all base table indexes automatically.</span></span> <span data-ttu-id="19ee0-113">Индексы обновляется каждый раз, когда добавление, изменение или удаление записей из базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="19ee0-113">It updates indexes whenever you add, change, or delete records from the base table.</span></span> <span data-ttu-id="19ee0-114">После создания базы данных, метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** периодически для переноса актуальных статистику индекса.</span><span class="sxs-lookup"><span data-stu-id="19ee0-114">Once you create the database, use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method periodically to bring index statistics up-to-date.</span></span>

<span data-ttu-id="19ee0-115">При доступе к таблице тип объекта **набора записей** , указать порядок записей с помощью свойства **Index** объекта.</span><span class="sxs-lookup"><span data-stu-id="19ee0-115">When accessing a table-type **Recordset** object, you specify the order of records using the object's **Index** property.</span></span> <span data-ttu-id="19ee0-116">Этому свойству присвоено значение \*\*свойства Name существующего объекта **индексу** в коллекции **индексов** \*\* .</span><span class="sxs-lookup"><span data-stu-id="19ee0-116">Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection.</span></span> <span data-ttu-id="19ee0-117">Эта коллекция содержится объектом **[TableDef](tabledef-object-dao.md)** базового объекта **набора записей** , который заполнение.</span><span class="sxs-lookup"><span data-stu-id="19ee0-117">This collection is contained by the **[TableDef](tabledef-object-dao.md)** object underlying the **Recordset** object that you're populating.</span></span>

> [!NOTE]
> <P><span data-ttu-id="19ee0-118">У вас нет для создания индексов для таблицы, но для больших, неиндексированные таблиц, доступ к определенной записи или обработки соединения может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="19ee0-118">You don't have to create indexes for a table, but for large, unindexed tables, accessing a specific record or processing joins can take a long time.</span></span> <span data-ttu-id="19ee0-119">С другой стороны слишком много индексов может снизить обновления базы данных как всех индексов таблицы изменен.</span><span class="sxs-lookup"><span data-stu-id="19ee0-119">Conversely, having too many indexes can slow down updates to the database as each of the table indexes is amended.</span></span></P>

<span data-ttu-id="19ee0-120">Свойство **[атрибуты](field-attributes-property-dao.md)** каждого объекта **поля** в индексе определяет порядок возвращаемых записей и поэтому определяет, какой доступ к методах, используемых для этого индекса.</span><span class="sxs-lookup"><span data-stu-id="19ee0-120">The **[Attributes](field-attributes-property-dao.md)** property of each **Field** object in the index determines the order of records returned and consequently determines which access techniques to use for that index.</span></span>

<span data-ttu-id="19ee0-121">Каждый объект **поля** в коллекции **полей** **индекс** объекта является компонентом индекса.</span><span class="sxs-lookup"><span data-stu-id="19ee0-121">Each **Field** object in the **Fields** collection of an **Index** object is a component of the index.</span></span> <span data-ttu-id="19ee0-122">Чтобы определить новый объект **индекса** , задайте его свойства перед добавлением в коллекцию предоставление объект **индекса** для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="19ee0-122">To define a new **Index** object, set its properties before you append it to a collection, making the **Index** object available for subsequent use.</span></span>

> [!NOTE]
> <P><span data-ttu-id="19ee0-123"><STRONG>Свойства Name существующего объекта <STRONG>индекса</STRONG> </STRONG> можно изменить только в том случае, если значение свойства <STRONG><A href="connection-updatable-property-dao.md">с возможностью записи</A></STRONG> , содержащего объект <STRONG>TableDef</STRONG> имеет <STRONG>значение True</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="19ee0-123">You can modify the <STRONG>Name</STRONG> property setting of an existing <STRONG>Index</STRONG> object only if the <STRONG><A href="connection-updatable-property-dao.md">Updatable</A></STRONG> property setting of the containing <STRONG>TableDef</STRONG> object is <STRONG>True</STRONG>.</span></span></P>

<span data-ttu-id="19ee0-124">При установке первичный ключ для таблицы ядро базы данных Microsoft Access автоматически определяет его как основной индекса.</span><span class="sxs-lookup"><span data-stu-id="19ee0-124">When you set a primary key for a table, the Microsoft Access database engine automatically defines it as the primary index.</span></span> <span data-ttu-id="19ee0-125">Первичный индекс состоит из одного или нескольких полей, которые однозначно идентифицируют все записи в таблице в предопределенном порядке.</span><span class="sxs-lookup"><span data-stu-id="19ee0-125">A primary index consists of one or more fields that uniquely identify all records in a table in a predefined order.</span></span> <span data-ttu-id="19ee0-126">Так как поле первичного индекса должно быть уникальным, ядро базы данных Microsoft Access автоматически устанавливает свойство **Уникальный** основной **индекс** объекта значение **True**.</span><span class="sxs-lookup"><span data-stu-id="19ee0-126">Because the primary index field must be unique, the Microsoft Access database engine automatically sets the **Unique** property of the primary **Index** object to **True**.</span></span> <span data-ttu-id="19ee0-127">Если основной индекс состоит из нескольких полей, в каждом поле может содержать повторяющиеся значения, но сочетание значений из всех индексированных полей должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="19ee0-127">If the primary index consists of more than one field, each field can contain duplicate values, but the combination of values from all the indexed fields must be unique.</span></span> <span data-ttu-id="19ee0-128">Первичный индекс состоит из ключа для таблицы и всегда включает в себя все поля первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="19ee0-128">A primary index consists of a key for the table and is always made up of the same fields as the primary key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19ee0-129">Убедитесь, что ваши данные стандарту атрибуты нового индекса.</span><span class="sxs-lookup"><span data-stu-id="19ee0-129">Make sure your data complies with the attributes of your new index.</span></span> <span data-ttu-id="19ee0-130">Если индекс требуются уникальные значения, убедитесь, что существует без повторов в существующей записи данных.</span><span class="sxs-lookup"><span data-stu-id="19ee0-130">If your index requires unique values, make sure that there are no duplicates in existing data records.</span></span> <span data-ttu-id="19ee0-131">Если существуют дубликаты, ядро базы данных Microsoft Access не удается создать индекс; Это перехватываемые приводит к ошибке при попытке использовать метод Append на новый индекс.</span><span class="sxs-lookup"><span data-stu-id="19ee0-131">If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

<span data-ttu-id="19ee0-132">При создании отношения, которое обеспечивает целостность данных ядро базы данных Microsoft Access автоматически создает индекс с помощью свойства **внешнего** задаются в виде внешнего ключа в ссылающаяся таблица.</span><span class="sxs-lookup"><span data-stu-id="19ee0-132">When you create a relationship that enforces referential integrity, the Microsoft Access database engine automatically creates an index with the **Foreign** property, set as the foreign key in the referencing table.</span></span> <span data-ttu-id="19ee0-133">После установления связи между таблицами, ядро базы данных Microsoft Access не позволяет дополнения или изменения базы данных, нарушают этой связи.</span><span class="sxs-lookup"><span data-stu-id="19ee0-133">After you've established a table relationship, the Microsoft Access database engine prevents additions or changes to the database that violate that relationship.</span></span> <span data-ttu-id="19ee0-134">Если для свойства **атрибуты** объекта **[связи](relation-object-dao.md)** , чтобы разрешить каскадных обновление и удаление ядро базы данных Microsoft Access обновляет или удаляет записи из связанных таблиц автоматически.</span><span class="sxs-lookup"><span data-stu-id="19ee0-134">If you set the **Attributes** property of the **[Relation](relation-object-dao.md)** object to allow cascading updates and cascading deletes, the Microsoft Access database engine updates or deletes records in related tables automatically.</span></span>

1.  <span data-ttu-id="19ee0-135">Используйте метод **CreateIndex** для объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="19ee0-135">Use the **CreateIndex** method on a **TableDef** object.</span></span>

2.  <span data-ttu-id="19ee0-136">Используйте метод **CreateField** на объект **индекса** для создания объекта **поля** для каждого поля (столбца), включаемых в **индекс** объекта.</span><span class="sxs-lookup"><span data-stu-id="19ee0-136">Use the **CreateField** method on the **Index** object to create a **Field** object for each field (column) to be included in the **Index** object.</span></span>

3.  <span data-ttu-id="19ee0-137">При необходимости установите свойства **индекса** .</span><span class="sxs-lookup"><span data-stu-id="19ee0-137">Set **Index** properties as needed.</span></span>

4.  <span data-ttu-id="19ee0-138">Добавьте объект **поля** в коллекцию **полей** .</span><span class="sxs-lookup"><span data-stu-id="19ee0-138">Append the **Field** object to the **Fields** collection.</span></span>

5.  <span data-ttu-id="19ee0-139">Добавьте объект **индекса** в коллекцию **индексов** .</span><span class="sxs-lookup"><span data-stu-id="19ee0-139">Append the **Index** object to the **Indexes** collection.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="19ee0-140">Свойство <STRONG>Clustered</STRONG> игнорируется для баз данных, использующих ядро базы данных Microsoft Access, которые не поддерживают кластеризованных индексов.</span><span class="sxs-lookup"><span data-stu-id="19ee0-140">The <STRONG>Clustered</STRONG> property is ignored for databases that use the Microsoft Access database engine, which doesn't support clustered indexes.</span></span></P>



## <a name="example"></a><span data-ttu-id="19ee0-141">Пример</span><span class="sxs-lookup"><span data-stu-id="19ee0-141">Example</span></span>

<span data-ttu-id="19ee0-142">В этом примере создается новый объект **индекса** , добавляет в коллекцию **индексов** сотрудников **TableDef**и затем создается перечисление коллекции **индексов** **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="19ee0-142">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**.</span></span> <span data-ttu-id="19ee0-143">И, наконец перечисляются **записей**, сначала с помощью основной **индекса**, а затем используют нового **индекса**.</span><span class="sxs-lookup"><span data-stu-id="19ee0-143">Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**.</span></span> <span data-ttu-id="19ee0-144">Процедура IndexOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="19ee0-144">The IndexOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="19ee0-145">В этом примере используется метод **CreateIndex** для создания двух новых объектов **индекса** и добавляет их в коллекцию **индексов** сотрудников **TableDef** объекта.</span><span class="sxs-lookup"><span data-stu-id="19ee0-145">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="19ee0-146">Затем выполняется перечисление коллекции **индексов** объекта **TableDef** , коллекции **полей** новых объектов **индекса** и коллекции свойств новых объектов **индекса** .</span><span class="sxs-lookup"><span data-stu-id="19ee0-146">It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="19ee0-147">Функция CreateIndexOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="19ee0-147">The CreateIndexOutput function is required for this procedure to run.</span></span>

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
