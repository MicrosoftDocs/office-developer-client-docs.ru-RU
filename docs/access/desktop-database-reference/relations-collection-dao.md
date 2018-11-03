---
title: Коллекции отношений (DAO)
TOCTitle: Relations Collection
ms:assetid: 8929b5cc-cf52-03f2-8cf5-7f45276d258e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197067(v=office.15)
ms:contentKeyID: 48546153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc8fa9bb24035e344ddb8e15179d4edd128abf7d
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936849"
---
# <a name="relations-collection-dao"></a><span data-ttu-id="9924d-102">Коллекции отношений (DAO)</span><span class="sxs-lookup"><span data-stu-id="9924d-102">Relations collection (DAO)</span></span>


<span data-ttu-id="9924d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9924d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9924d-104">Коллекция **отношения** содержит сохраненные объекты **отношений** объектов **базы данных** (базы данных ядра базы данных Microsoft Access только).</span><span class="sxs-lookup"><span data-stu-id="9924d-104">A **Relations** collection contains stored **Relation** objects of a **Database** object (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="9924d-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="9924d-105">Remarks</span></span>

<span data-ttu-id="9924d-106">Объект **связи** можно использовать для создания новых связей и проверить существующих связей между таблицами в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9924d-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span> <span data-ttu-id="9924d-107">Чтобы добавить объект **отношения** в коллекции **отношений** , сначала создайте его с помощью метода **CreateRelation** и затем добавьте его в коллекцию **отношений** с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="9924d-107">To add a **Relation** object to the **Relations** collection, first create it with the **CreateRelation** method, and then append it to the **Relations** collection with the **Append** method.</span></span> <span data-ttu-id="9924d-108">Объект **отношения** сохраняется при закрытии объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="9924d-108">This will save the **Relation** object when you close the **Database** object.</span></span> <span data-ttu-id="9924d-109">Чтобы удалить объект **связи** из коллекции, используйте метод **Delete** .</span><span class="sxs-lookup"><span data-stu-id="9924d-109">To remove a **Relation** object from the collection, use the **Delete** method.</span></span>

<span data-ttu-id="9924d-110">Для ссылки на объект **связи** в семействе сайтов, с его порядковый номер или **его свойства Name** , можно используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="9924d-110">To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="9924d-111">**Отношения** (0)</span><span class="sxs-lookup"><span data-stu-id="9924d-111">**Relations**(0)</span></span>

<span data-ttu-id="9924d-112">**Отношения** («имя»)</span><span class="sxs-lookup"><span data-stu-id="9924d-112">**Relations**("name")</span></span>

<span data-ttu-id="9924d-113">**Отношения**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="9924d-113">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="9924d-114">Пример</span><span class="sxs-lookup"><span data-stu-id="9924d-114">Example</span></span>

<span data-ttu-id="9924d-115">В этом примере показано, как управлять существующий объект **отношения** ввода данных.</span><span class="sxs-lookup"><span data-stu-id="9924d-115">This example shows how an existing **Relation** object can control data entry.</span></span> <span data-ttu-id="9924d-116">Процедура пытается добавить запись, намеренно неправильный идентификатор категории; Это вызывает обработчик ошибок.</span><span class="sxs-lookup"><span data-stu-id="9924d-116">The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

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

<span data-ttu-id="9924d-117">В этом примере используется метод **CreateRelation** для создания **связи** между сотрудниками **TableDef** и новые **TableDef** вызван отделов.</span><span class="sxs-lookup"><span data-stu-id="9924d-117">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="9924d-118">Также показано, как создание нового **отношения** также создается необходимые **индексов** в таблице внешнего (DepartmentsEmployees Index в таблице «Сотрудники»).</span><span class="sxs-lookup"><span data-stu-id="9924d-118">It also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
