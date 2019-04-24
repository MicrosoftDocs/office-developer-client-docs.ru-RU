---
title: Коллекция indexes (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f731862e12a75f91d07ea7d012cc33dad5be0b55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291568"
---
# <a name="indexes-collection-dao"></a><span data-ttu-id="4eff7-102">Коллекция indexes (DAO)</span><span class="sxs-lookup"><span data-stu-id="4eff7-102">Indexes collection (DAO)</span></span>

<span data-ttu-id="4eff7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4eff7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4eff7-104">Коллекция **indexes** содержит все хранимые объекты **индекса** объекта **tabledef** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4eff7-104">An **Indexes** collection contains all the stored **Index** objects of a **TableDef** object (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="4eff7-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="4eff7-105">Remarks</span></span>

<span data-ttu-id="4eff7-106">При доступе к объекту Recordset табличного типа используйте свойство **index** объекта для указания порядка записей.</span><span class="sxs-lookup"><span data-stu-id="4eff7-106">When you access a table-type Recordset object, use the object's **Index** property to specify the order of records.</span></span> <span data-ttu-id="4eff7-107">ПриСвойте этому свойству значение свойства **Name** существующего **индекса** в коллекции **indexes** объекта **[tabledef](tabledef-object-dao.md)** , который является базовым для объекта **[Recordset](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="4eff7-107">Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection of the **[TableDef](tabledef-object-dao.md)** object underlying the **[Recordset](recordset-object-dao.md)** object.</span></span>

> [!NOTE]
> <span data-ttu-id="4eff7-108">Вы можете использовать метод **append** или **Delete** для коллекции **indexes** , только если значение свойства **[обновляемого](connection-updatable-property-dao.md)** объекта **tabledef** равно **true**.</span><span class="sxs-lookup"><span data-stu-id="4eff7-108">You can use the **Append** or **Delete** method on an **Indexes** collection only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="4eff7-109">После создания нового объекта **index** следует использовать метод **append** , чтобы добавить его в коллекцию **индексов** объекта **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="4eff7-109">After you create a new **Index** object, you should use the **Append** method to add it to the **TableDef** object's **Indexes** collection.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4eff7-110">Убедитесь, что данные соответствуют атрибутам нового индекса.</span><span class="sxs-lookup"><span data-stu-id="4eff7-110">Make sure your data complies with the attributes of your new index.</span></span> <span data-ttu-id="4eff7-111">Если для индекса требуются уникальные значения, убедитесь, что в существующих записях данных нет дубликатов.</span><span class="sxs-lookup"><span data-stu-id="4eff7-111">If your index requires unique values, make sure that there are no duplicates in existing data records.</span></span> <span data-ttu-id="4eff7-112">Если дубликаты существуют, ядро СУБД Microsoft Access не может создать индекс; При попытке использовать метод Append для нового индекса возникает перехватываемая ошибка.</span><span class="sxs-lookup"><span data-stu-id="4eff7-112">If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

## <a name="example"></a><span data-ttu-id="4eff7-113">Пример</span><span class="sxs-lookup"><span data-stu-id="4eff7-113">Example</span></span>

<span data-ttu-id="4eff7-114">В этом примере создается новый объект **index** , который добавляется в коллекцию **indexes** для Employees **tabledef**, а затем перечисляет коллекцию **indexes** объекта **tabledef**.</span><span class="sxs-lookup"><span data-stu-id="4eff7-114">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**.</span></span> <span data-ttu-id="4eff7-115">Наконец, он перечисляет **набор записей**, сначала используя первичный **индекс**, а затем с помощью нового **индекса**.</span><span class="sxs-lookup"><span data-stu-id="4eff7-115">Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**.</span></span> <span data-ttu-id="4eff7-116">Для выполнения этой процедуры требуется процедура Индексаутпут.</span><span class="sxs-lookup"><span data-stu-id="4eff7-116">The IndexOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="4eff7-117">В этом примере используется метод **креатеиндекс** для создания двух новых объектов **индекса** , а затем они добавляются в коллекцию **indexes** объекта Employees **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="4eff7-117">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="4eff7-118">Затем выполняется перечисление \*\*\*\* коллекции индексов объекта **tabledef** , коллекции **Fields** новых объектов **index** и коллекции свойств новых объектов **index** .</span><span class="sxs-lookup"><span data-stu-id="4eff7-118">It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="4eff7-119">Для выполнения этой процедуры требуется функция Креатеиндексаутпут.</span><span class="sxs-lookup"><span data-stu-id="4eff7-119">The CreateIndexOutput function is required for this procedure to run.</span></span>

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
