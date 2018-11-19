---
title: Коллекции индексов (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a809afb8e38cf23faf43d5eb49c5edadaf70b2b1
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025835"
---
# <a name="indexes-collection-dao"></a><span data-ttu-id="abaea-102">Коллекции индексов (DAO)</span><span class="sxs-lookup"><span data-stu-id="abaea-102">Indexes collection (DAO)</span></span>

<span data-ttu-id="abaea-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="abaea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="abaea-104">Коллекции **индексов** содержит все хранимые объекты **индекс** объекта **TableDef** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="abaea-104">An **Indexes** collection contains all the stored **Index** objects of a **TableDef** object (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="abaea-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="abaea-105">Remarks</span></span>

<span data-ttu-id="abaea-106">При получении доступа к таблице тип объекта набора записей, используйте свойство **Index** объекта, чтобы указать порядок записей.</span><span class="sxs-lookup"><span data-stu-id="abaea-106">When you access a table-type Recordset object, use the object's **Index** property to specify the order of records.</span></span> <span data-ttu-id="abaea-107">Этому свойству присвоено значение \*\*свойства Name существующего объекта **индексу** в коллекции **индексов** объекта **[TableDef](tabledef-object-dao.md)** базового объекта **[набора записей](recordset-object-dao.md)** \*\* .</span><span class="sxs-lookup"><span data-stu-id="abaea-107">Set this property to the **Name** property setting of an existing **Index** object in the **Indexes** collection of the **[TableDef](tabledef-object-dao.md)** object underlying the **[Recordset](recordset-object-dao.md)** object.</span></span>

> [!NOTE]
> <span data-ttu-id="abaea-108">**Добавление** или **Удаление** метод на коллекцию **индексов** можно использовать только в том случае, если значение свойства **[с возможностью записи](connection-updatable-property-dao.md)** , содержащего объект **TableDef** имеет **значение True**.</span><span class="sxs-lookup"><span data-stu-id="abaea-108">You can use the **Append** or **Delete** method on an **Indexes** collection only if the **[Updatable](connection-updatable-property-dao.md)** property setting of the containing **TableDef** object is **True**.</span></span>

<span data-ttu-id="abaea-109">После создания объекта **индекса** , чтобы добавить его в коллекцию объектов **TableDef** **индексов** следует использовать метод **Append** .</span><span class="sxs-lookup"><span data-stu-id="abaea-109">After you create a new **Index** object, you should use the **Append** method to add it to the **TableDef** object's **Indexes** collection.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="abaea-110">Убедитесь, что ваши данные стандарту атрибуты нового индекса.</span><span class="sxs-lookup"><span data-stu-id="abaea-110">Make sure your data complies with the attributes of your new index.</span></span> <span data-ttu-id="abaea-111">Если индекс требуются уникальные значения, убедитесь, что существует без повторов в существующей записи данных.</span><span class="sxs-lookup"><span data-stu-id="abaea-111">If your index requires unique values, make sure that there are no duplicates in existing data records.</span></span> <span data-ttu-id="abaea-112">Если существуют дубликаты, ядро базы данных Microsoft Access не удается создать индекс; Это перехватываемые приводит к ошибке при попытке использовать метод Append на новый индекс.</span><span class="sxs-lookup"><span data-stu-id="abaea-112">If duplicates exist, the Microsoft Access database engine can't create the index; a trappable error results when you attempt to use the Append method on the new index.</span></span>

## <a name="example"></a><span data-ttu-id="abaea-113">Пример</span><span class="sxs-lookup"><span data-stu-id="abaea-113">Example</span></span>

<span data-ttu-id="abaea-114">В этом примере создается новый объект **индекса** , добавляет в коллекцию **индексов** сотрудников **TableDef**и затем создается перечисление коллекции **индексов** **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="abaea-114">This example creates a new **Index** object, appends it to the **Indexes** collection of the Employees **TableDef**, and then enumerates the **Indexes** collection of the **TableDef**.</span></span> <span data-ttu-id="abaea-115">И, наконец перечисляются **записей**, сначала с помощью основной **индекса**, а затем используют нового **индекса**.</span><span class="sxs-lookup"><span data-stu-id="abaea-115">Finally, it enumerates a **Recordset**, first using the primary **Index**, and then using the new **Index**.</span></span> <span data-ttu-id="abaea-116">Процедура IndexOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="abaea-116">The IndexOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="abaea-117">В этом примере используется метод **CreateIndex** для создания двух новых объектов **индекса** и добавляет их в коллекцию **индексов** сотрудников **TableDef** объекта.</span><span class="sxs-lookup"><span data-stu-id="abaea-117">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object.</span></span> <span data-ttu-id="abaea-118">Затем выполняется перечисление коллекции **индексов** объекта **TableDef** , коллекции **полей** новых объектов **индекса** и коллекции свойств новых объектов **индекса** .</span><span class="sxs-lookup"><span data-stu-id="abaea-118">It then enumerates the **Indexes** collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects.</span></span> <span data-ttu-id="abaea-119">Функция CreateIndexOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="abaea-119">The CreateIndexOutput function is required for this procedure to run.</span></span>

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
