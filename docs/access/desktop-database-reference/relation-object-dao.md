---
title: Объект Relation (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3eeaf8bf46d8673731243a1161ac578062a01f89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307051"
---
# <a name="relation-object-dao"></a><span data-ttu-id="a5b5b-102">Объект Relation (DAO)</span><span class="sxs-lookup"><span data-stu-id="a5b5b-102">Relation object (DAO)</span></span>


<span data-ttu-id="a5b5b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5b5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a5b5b-104">Объект **Relation** представляет отношение между полями в таблицах или запросах (только для баз данных ям баз данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a5b5b-104">A **Relation** object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b5b-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="a5b5b-105">Remarks</span></span>

<span data-ttu-id="a5b5b-106">Объект **Relation** можно использовать для создания новых отношений и изучения существующих отношений в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span>

<span data-ttu-id="a5b5b-107">С помощью **объекта Relation** и его свойств можно:</span><span class="sxs-lookup"><span data-stu-id="a5b5b-107">Using a **Relation** object and its properties, you can:</span></span>

  - <span data-ttu-id="a5b5b-108">Укажите принудительное отношение между полями в базовых таблицах (но не отношение, которое включает запрос или связанную таблицу).</span><span class="sxs-lookup"><span data-stu-id="a5b5b-108">Specify an enforced relationship between fields in base tables (but not a relationship that involves a query or a linked table).</span></span>

  - <span data-ttu-id="a5b5b-109">Установить неподтвержденные связи между любым типом таблицы или запроса — машинным или связанным.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-109">Establish unenforced relationships between any type of table or query— native or linked.</span></span>

  - <span data-ttu-id="a5b5b-110">Используйте свойство **Name** для ссылки на связь между полями в основной таблице, на которые ссылается ссылка, и внешней таблицей, на которые ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-110">Use the **Name** property to refer to the relationship between the fields in the referenced primary table and the referencing foreign table.</span></span>

  - <span data-ttu-id="a5b5b-111">Используйте свойство **Attributes,** чтобы определить, является ли отношение между полями в таблице "один к одному" или "один-к-многим" и как обеспечить целостность ссылок.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-111">Use the **Attributes** property to determine whether the relationship between fields in the table is one-to-one or one-to-many and how to enforce referential integrity.</span></span>

  - <span data-ttu-id="a5b5b-112">Используйте свойство **Attributes,** чтобы определить, может ли яд баз данных Microsoft Access выполнять каскадные операции обновления и каскадного удаления в основных и внешних таблицах.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-112">Use the **Attributes** property to determine whether the Microsoft Access database engine can perform cascading update and cascading delete operations on primary and foreign tables.</span></span>

  - <span data-ttu-id="a5b5b-113">Используйте свойство **Attributes,** чтобы определить, является ли связь между полями в таблице левым или правым.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-113">Use the **Attributes** property to determine whether the relationship between fields in the table is left join or right join.</span></span>

  - <span data-ttu-id="a5b5b-114">Используйте свойство **Name** всех объектов **Field** в коллекции **Fields** объекта **Relation,** чтобы установить или вернуть имена полей в первичном ключе таблицы, на который ссылается ссылка, или параметры свойств **ForeignName** объектов **Field,** чтобы установить или вернуть имена полей во внешнем ключе таблицы ссылок.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-114">Use the **Name** property of all **Field** objects in the **Fields** collection of a **Relation** object to set or return the names of the fields in the primary key of the referenced table, or the **ForeignName** property settings of the **Field** objects to set or return the names of the fields in the foreign key of the referencing table.</span></span>

<span data-ttu-id="a5b5b-115">При внесении изменений, нарушающих отношения, установленные для базы данных, возникает перехируемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-115">If you make changes that violate the relationships established for the database, a trappable error occurs.</span></span> <span data-ttu-id="a5b5b-116">Если вы запрашиваете операции каскадного обновления или каскадного удаления, модуль базы данных Microsoft Access также изменяет первичный ключ или таблицы внешних ключей для применения устанавливаемой связи.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-116">If you request cascading update or cascading delete operations, the Microsoft Access database engine also modifies the primary key or foreign key tables to enforce the relationships you establish.</span></span>

<span data-ttu-id="a5b5b-117">Например, база данных Northwind содержит связь между таблицей Orders и таблицей Customers.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-117">For example, the Northwind database contains a relationship between an Orders table and a Customers table.</span></span> <span data-ttu-id="a5b5b-118">Поле CustomerID таблицы Customers является первичным ключом, а поле CustomerID таблицы "Заказы" — внешней клавишей.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-118">The CustomerID field of the Customers table is the primary key, and the CustomerID field of the Orders table is the foreign key.</span></span> <span data-ttu-id="a5b5b-119">Чтобы ядер баз данных Microsoft Access принять новую запись в таблице "Заказы", он выполняет поиск совпадения в таблице Customers в поле CustomerID таблицы "Заказы".</span><span class="sxs-lookup"><span data-stu-id="a5b5b-119">For the Microsoft Access database engine to accept a new record in the Orders table, it searches the Customers table for a match on the CustomerID field of the Orders table.</span></span> <span data-ttu-id="a5b5b-120">Если яд баз данных Microsoft Access не находит совпадения, он не принимает новую запись, и возникает перехименовывуемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-120">If the Microsoft Access database engine doesn't find a match, it doesn't accept the new record, and a trappable error occurs.</span></span>

<span data-ttu-id="a5b5b-121">При обеспечении целостности ссылок для ключевого поля таблицы, на который ссылается ссылка, уже должен существовать уникальный индекс.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-121">When you enforce referential integrity, a unique index must already exist for the key field of the referenced table.</span></span> <span data-ttu-id="a5b5b-122">Яд баз данных Microsoft Access автоматически создает индекс со свойством **Foreign,** который будет выступать в качестве внешнего ключа в таблице ссылок.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-122">The Microsoft Access database engine automatically creates an index with the **Foreign** property set to act as the foreign key in the referencing table.</span></span>

<span data-ttu-id="a5b5b-123">Чтобы создать новый **объект Relation,** используйте **метод CreateRelation.**</span><span class="sxs-lookup"><span data-stu-id="a5b5b-123">To create a new **Relation** object, use the **CreateRelation** method.</span></span> <span data-ttu-id="a5b5b-124">Чтобы сослаться на **объект Relation** в коллекции по порядковому номеру или по его свойству **Name,** используйте любую из следующих синтаксис форм:</span><span class="sxs-lookup"><span data-stu-id="a5b5b-124">To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="a5b5b-125">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="a5b5b-125">**Relations**(0)</span></span>

<span data-ttu-id="a5b5b-126">**Relations**("name")</span><span class="sxs-lookup"><span data-stu-id="a5b5b-126">**Relations**("name")</span></span>

<span data-ttu-id="a5b5b-127"> \! Relations \[ name\]</span><span class="sxs-lookup"><span data-stu-id="a5b5b-127">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="a5b5b-128">Пример</span><span class="sxs-lookup"><span data-stu-id="a5b5b-128">Example</span></span>

<span data-ttu-id="a5b5b-129">В этом примере показано, как **существующий объект Relation** может управлять записью данных.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-129">This example shows how an existing **Relation** object can control data entry.</span></span> <span data-ttu-id="a5b5b-130">Процедура пытается добавить запись с намеренно неправильным categoryID; Это запускает процедуру обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="a5b5b-130">The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

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

<span data-ttu-id="a5b5b-131">В этом примере метод **CreateRelation** используется для создания отношения между **TableDef** Employees и новым **TableDef** под названием Departments. </span><span class="sxs-lookup"><span data-stu-id="a5b5b-131">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="a5b5b-132">В нем также показано, как при  создании нового отношения также будут создаваться все необходимые индексы во внешней таблице (индекс DepartmentsEmployees в таблице Employees). </span><span class="sxs-lookup"><span data-stu-id="a5b5b-132">It also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
