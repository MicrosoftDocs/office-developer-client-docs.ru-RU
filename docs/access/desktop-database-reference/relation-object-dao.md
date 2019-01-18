---
title: Объект отношения (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3eeaf8bf46d8673731243a1161ac578062a01f89
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716280"
---
# <a name="relation-object-dao"></a><span data-ttu-id="75a14-102">Объект отношения (DAO)</span><span class="sxs-lookup"><span data-stu-id="75a14-102">Relation object (DAO)</span></span>


<span data-ttu-id="75a14-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75a14-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75a14-104">Объект **связи** представляет связь между полями в таблицах и запросах (Microsoft Access базами данных, ядро только).</span><span class="sxs-lookup"><span data-stu-id="75a14-104">A **Relation** object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="75a14-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="75a14-105">Remarks</span></span>

<span data-ttu-id="75a14-106">Объект **связи** можно использовать для создания новых связей и проверить существующих связей между таблицами в базе данных.</span><span class="sxs-lookup"><span data-stu-id="75a14-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span>

<span data-ttu-id="75a14-107">Используется объект **связи** и его свойства, можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="75a14-107">Using a **Relation** object and its properties, you can:</span></span>

  - <span data-ttu-id="75a14-108">Укажите связи между полями в базовые таблицы (но не отношения, который включает в себя запроса или связанной таблицы).</span><span class="sxs-lookup"><span data-stu-id="75a14-108">Specify an enforced relationship between fields in base tables (but not a relationship that involves a query or a linked table).</span></span>

  - <span data-ttu-id="75a14-109">Установить необязательного отношения между любой тип таблицы или запроса — собственная или связанный.</span><span class="sxs-lookup"><span data-stu-id="75a14-109">Establish unenforced relationships between any type of table or query— native or linked.</span></span>

  - <span data-ttu-id="75a14-110">Свойство **имени** для ссылки на отношения между поля в указанной таблице основной и ссылающаяся таблица внешнего.</span><span class="sxs-lookup"><span data-stu-id="75a14-110">Use the **Name** property to refer to the relationship between the fields in the referenced primary table and the referencing foreign table.</span></span>

  - <span data-ttu-id="75a14-111">Свойство **атрибуты** определить, является ли связь между поля в таблице один к одному или один ко многим и как обеспечения целостности данных.</span><span class="sxs-lookup"><span data-stu-id="75a14-111">Use the **Attributes** property to determine whether the relationship between fields in the table is one-to-one or one-to-many and how to enforce referential integrity.</span></span>

  - <span data-ttu-id="75a14-112">Используйте свойство **Attributes** для определения ли ядро базы данных Microsoft Access можно выполнить обновление каскадных таблиц каскадных операций и удаления на основной и внешних таблиц.</span><span class="sxs-lookup"><span data-stu-id="75a14-112">Use the **Attributes** property to determine whether the Microsoft Access database engine can perform cascading update and cascading delete operations on primary and foreign tables.</span></span>

  - <span data-ttu-id="75a14-113">Используйте свойство **атрибуты** для определения, остается ли связь между поля в таблице объединение или правом объединение.</span><span class="sxs-lookup"><span data-stu-id="75a14-113">Use the **Attributes** property to determine whether the relationship between fields in the table is left join or right join.</span></span>

  - <span data-ttu-id="75a14-114">Используйте свойство **Name** из всех объектов **поля** в коллекции **полей** объект **связи** или возвращает имена полей в первичный ключ указанную таблицу или параметры свойства **ForeignName** Объекты **поля** или возвращает имена полей в внешний ключ ссылающаяся таблица.</span><span class="sxs-lookup"><span data-stu-id="75a14-114">Use the **Name** property of all **Field** objects in the **Fields** collection of a **Relation** object to set or return the names of the fields in the primary key of the referenced table, or the **ForeignName** property settings of the **Field** objects to set or return the names of the fields in the foreign key of the referencing table.</span></span>

<span data-ttu-id="75a14-115">При внесении изменений, которые нарушают связей, определенных для базы данных, то перехватываемые возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="75a14-115">If you make changes that violate the relationships established for the database, a trappable error occurs.</span></span> <span data-ttu-id="75a14-116">При запросе каскадные обновления или каскадных операций delete, ядро базы данных Microsoft Access также изменяет основной ключ или таблицы внешних ключей для обеспечения связи, которые можно установить.</span><span class="sxs-lookup"><span data-stu-id="75a14-116">If you request cascading update or cascading delete operations, the Microsoft Access database engine also modifies the primary key or foreign key tables to enforce the relationships you establish.</span></span>

<span data-ttu-id="75a14-117">Например базы данных Northwind содержит отношение между таблицы заказов и таблице Customers.</span><span class="sxs-lookup"><span data-stu-id="75a14-117">For example, the Northwind database contains a relationship between an Orders table and a Customers table.</span></span> <span data-ttu-id="75a14-118">Первичный ключ — это поле CustomerID в таблице клиентов, а в поле CustomerID в таблице Orders является внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="75a14-118">The CustomerID field of the Customers table is the primary key, and the CustomerID field of the Orders table is the foreign key.</span></span> <span data-ttu-id="75a14-119">Для ядра СУБД Microsoft Access для принятия новой записи в таблице Orders будет выполняться поиск в таблице Клиенты соответствие на поле CustomerID таблицы заказов.</span><span class="sxs-lookup"><span data-stu-id="75a14-119">For the Microsoft Access database engine to accept a new record in the Orders table, it searches the Customers table for a match on the CustomerID field of the Orders table.</span></span> <span data-ttu-id="75a14-120">Если ядро базы данных Microsoft Access не находит соответствие, он не принимает новую запись, и становится перехватываемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="75a14-120">If the Microsoft Access database engine doesn't find a match, it doesn't accept the new record, and a trappable error occurs.</span></span>

<span data-ttu-id="75a14-121">Если целостность данных, уникальный индекс должны уже существовать ключевого поля таблицы, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="75a14-121">When you enforce referential integrity, a unique index must already exist for the key field of the referenced table.</span></span> <span data-ttu-id="75a14-122">Ядро базы данных Microsoft Access автоматически создает индекс с установленным свойством **внешнего** в качестве внешнего ключа в ссылающаяся таблица.</span><span class="sxs-lookup"><span data-stu-id="75a14-122">The Microsoft Access database engine automatically creates an index with the **Foreign** property set to act as the foreign key in the referencing table.</span></span>

<span data-ttu-id="75a14-123">Чтобы создать новый объект **отношения** , используйте метод **CreateRelation** .</span><span class="sxs-lookup"><span data-stu-id="75a14-123">To create a new **Relation** object, use the **CreateRelation** method.</span></span> <span data-ttu-id="75a14-124">Для ссылки на объект **связи** в семействе сайтов, с его порядковый номер или **его свойства Name** , можно используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="75a14-124">To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="75a14-125">**Отношения** (0)</span><span class="sxs-lookup"><span data-stu-id="75a14-125">**Relations**(0)</span></span>

<span data-ttu-id="75a14-126">**Отношения** («имя»)</span><span class="sxs-lookup"><span data-stu-id="75a14-126">**Relations**("name")</span></span>

<span data-ttu-id="75a14-127">**Отношения**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="75a14-127">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="75a14-128">Пример</span><span class="sxs-lookup"><span data-stu-id="75a14-128">Example</span></span>

<span data-ttu-id="75a14-129">В этом примере показано, как управлять существующий объект **отношения** ввода данных.</span><span class="sxs-lookup"><span data-stu-id="75a14-129">This example shows how an existing **Relation** object can control data entry.</span></span> <span data-ttu-id="75a14-130">Процедура пытается добавить запись, намеренно неправильный идентификатор категории; Это вызывает обработчик ошибок.</span><span class="sxs-lookup"><span data-stu-id="75a14-130">The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

```vb 
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

<span data-ttu-id="75a14-131">В этом примере используется метод **CreateRelation** для создания **связи** между сотрудниками **TableDef** и новые **TableDef** вызван отделов.</span><span class="sxs-lookup"><span data-stu-id="75a14-131">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="75a14-132">Также показано, как создание нового **отношения** также создается необходимые **индексов** в таблице внешнего (DepartmentsEmployees Index в таблице «Сотрудники»).</span><span class="sxs-lookup"><span data-stu-id="75a14-132">It also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
