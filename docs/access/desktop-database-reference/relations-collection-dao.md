---
title: Коллекция связей (DAO)
TOCTitle: Relations Collection
ms:assetid: 8929b5cc-cf52-03f2-8cf5-7f45276d258e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197067(v=office.15)
ms:contentKeyID: 48546153
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc60e36abbb353a178864b488a738fcf3247e1a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306974"
---
# <a name="relations-collection-dao"></a><span data-ttu-id="b9c0b-102">Коллекция связей (DAO)</span><span class="sxs-lookup"><span data-stu-id="b9c0b-102">Relations collection (DAO)</span></span>


<span data-ttu-id="b9c0b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9c0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9c0b-104">Коллекция **отношениях** содержит хранимые объекты **relation** объекта **Database** (только базы данных ядра СУБД Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b9c0b-104">A **Relations** collection contains stored **Relation** objects of a **Database** object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9c0b-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9c0b-105">Remarks</span></span>

<span data-ttu-id="b9c0b-106">Объект **relation** можно использовать для создания новых связей и проверки существующих связей в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b9c0b-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span> <span data-ttu-id="b9c0b-107">Чтобы добавить объект **relation** в коллекцию **связей** , сначала создайте его с помощью метода **креатерелатион** , а затем добавьте его в коллекцию **связей** с помощью метода **append** .</span><span class="sxs-lookup"><span data-stu-id="b9c0b-107">To add a **Relation** object to the **Relations** collection, first create it with the **CreateRelation** method, and then append it to the **Relations** collection with the **Append** method.</span></span> <span data-ttu-id="b9c0b-108">При закрытии объекта **базы данных** объект **relation** будет сохранен.</span><span class="sxs-lookup"><span data-stu-id="b9c0b-108">This will save the **Relation** object when you close the **Database** object.</span></span> <span data-ttu-id="b9c0b-109">Чтобы удалить объект **relation** из коллекции, используйте метод **Delete** .</span><span class="sxs-lookup"><span data-stu-id="b9c0b-109">To remove a **Relation** object from the collection, use the **Delete** method.</span></span>

<span data-ttu-id="b9c0b-110">Чтобы сослаться на объект **relation** в коллекции по его порядковому номеру или по значению свойства **Name** , используйте любую из следующих синтаксических форм:</span><span class="sxs-lookup"><span data-stu-id="b9c0b-110">To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="b9c0b-111">**Отношения** нуль</span><span class="sxs-lookup"><span data-stu-id="b9c0b-111">**Relations**(0)</span></span>

<span data-ttu-id="b9c0b-112">**Отношения** ("имя")</span><span class="sxs-lookup"><span data-stu-id="b9c0b-112">**Relations**("name")</span></span>

<span data-ttu-id="b9c0b-113">**Имя отношения**\!\[\]</span><span class="sxs-lookup"><span data-stu-id="b9c0b-113">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="b9c0b-114">Пример</span><span class="sxs-lookup"><span data-stu-id="b9c0b-114">Example</span></span>

<span data-ttu-id="b9c0b-115">В этом примере показано, как существующий объект **relation** может управлять вводом данных.</span><span class="sxs-lookup"><span data-stu-id="b9c0b-115">This example shows how an existing **Relation** object can control data entry.</span></span> <span data-ttu-id="b9c0b-116">Процедура пытается добавить запись с намеренно неправильным идентификатором CategoryID; Это запускает процедуру обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="b9c0b-116">The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

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

<span data-ttu-id="b9c0b-117">В этом примере используется метод **креатерелатион** для создания **отношения** между сотрудниками **tabledef** и новыми **tabledef** , называемыми отделами.</span><span class="sxs-lookup"><span data-stu-id="b9c0b-117">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="b9c0b-118">Кроме того, показано, как создание нового **отношения** также приведет к созданию необходимых **индексов** во внешней таблице (индекс департментсемплойис в таблице Employees).</span><span class="sxs-lookup"><span data-stu-id="b9c0b-118">It also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
