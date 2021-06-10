---
title: Метод Database.CreateRelation (DAO)
TOCTitle: CreateRelation Method
ms:assetid: e240c7e3-c293-5e19-afcc-34d9a5549c64
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835692(v=office.15)
ms:contentKeyID: 48548279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052969
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 365835bc579a431d34b65cd27ed4de4e12bca309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294955"
---
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="3f986-102">Метод Database.CreateRelation (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f986-102">Database.CreateRelation method (DAO)</span></span>

<span data-ttu-id="3f986-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f986-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f986-104">Создает новый объект **[Relation](relation-object-dao.md)** (только рабочие пространства Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3f986-104">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3f986-105">.</span><span class="sxs-lookup"><span data-stu-id="3f986-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f986-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f986-106">Syntax</span></span>

<span data-ttu-id="3f986-107">*выражения* . CreateRelation ***(Имя***, ***Таблица***, ***ForeignTable***, ***Атрибуты***)</span><span class="sxs-lookup"><span data-stu-id="3f986-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="3f986-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="3f986-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f986-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f986-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f986-110">Имя</span><span class="sxs-lookup"><span data-stu-id="3f986-110">Name</span></span></p></th>
<th><p><span data-ttu-id="3f986-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="3f986-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="3f986-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3f986-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="3f986-113">Описание</span><span class="sxs-lookup"><span data-stu-id="3f986-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f986-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="3f986-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="3f986-115">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="3f986-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f986-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3f986-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3f986-117">Подтип <strong>Variant</strong> <strong>(String),</strong> который однозначно называет новый объект <strong>Relation.</strong></span><span class="sxs-lookup"><span data-stu-id="3f986-117">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object.</span></span> <span data-ttu-id="3f986-118">Сведения о <strong><a href="connection-name-property-dao.md">допустимом</a></strong> имени Relation см. в свойстве <strong>Name.</strong></span><span class="sxs-lookup"><span data-stu-id="3f986-118">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f986-119"><em>Table</em></span><span class="sxs-lookup"><span data-stu-id="3f986-119"><em>Table</em></span></span></p></td>
<td><p><span data-ttu-id="3f986-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="3f986-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f986-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3f986-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3f986-122">Подтип <strong>Variant</strong> <strong>(String),</strong> который называет основную таблицу в связи.</span><span class="sxs-lookup"><span data-stu-id="3f986-122">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation.</span></span> <span data-ttu-id="3f986-123">Если таблица не существует до того, как примыкать к объекту <strong>Relation,</strong> возникает ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="3f986-123">If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f986-124"><em>ForeignTable</em></span><span class="sxs-lookup"><span data-stu-id="3f986-124"><em>ForeignTable</em></span></span></p></td>
<td><p><span data-ttu-id="3f986-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="3f986-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f986-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3f986-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3f986-127"><strong>Подтип</strong> <strong>Variant (String),</strong> который называет иностранную таблицу в связи.</span><span class="sxs-lookup"><span data-stu-id="3f986-127">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation.</span></span> <span data-ttu-id="3f986-128">Если таблица не существует до того, как примыкать к объекту <strong>Relation,</strong> возникает ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="3f986-128">If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f986-129"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="3f986-129"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="3f986-130">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="3f986-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="3f986-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3f986-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3f986-132">Константа или сочетание констант, которые содержат сведения о типе отношений.</span><span class="sxs-lookup"><span data-stu-id="3f986-132">A constant or combination of constants that contains information about the relationship type.</span></span> <span data-ttu-id="3f986-133">Сведения см. <strong><a href="field-attributes-property-dao.md">в свойстве</a></strong> Атрибуты.</span><span class="sxs-lookup"><span data-stu-id="3f986-133">See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="3f986-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f986-134">Return value</span></span>

<span data-ttu-id="3f986-135">Relation</span><span class="sxs-lookup"><span data-stu-id="3f986-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="3f986-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f986-136">Remarks</span></span>

<span data-ttu-id="3f986-137">Объект **Relation** предоставляет в движок базы данных Microsoft Access сведения о связи между полями в двух объектах **[TableDef](tabledef-object-dao.md)** или **[QueryDef.](querydef-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="3f986-137">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects.</span></span> <span data-ttu-id="3f986-138">Вы можете реализовать целостность ссылок с помощью свойства **Attributes.**</span><span class="sxs-lookup"><span data-stu-id="3f986-138">You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="3f986-139">Если при использовании метода **CreateRelation** вы опустить одну или несколько необязательных частей, вы можете использовать соответствующее заявление о назначении для настройки или сброса соответствующего свойства перед тем, как примять новый объект к коллекции.</span><span class="sxs-lookup"><span data-stu-id="3f986-139">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="3f986-140">После придатки объекта вы не сможете изменить его параметры свойств.</span><span class="sxs-lookup"><span data-stu-id="3f986-140">After you append the object, you can't alter any of its property settings.</span></span> <span data-ttu-id="3f986-141">См. разделы для отдельных свойств для получения дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="3f986-141">See the individual property topics for more details.</span></span>

<span data-ttu-id="3f986-142">Прежде чем использовать метод **[Append](fields-append-method-dao.md)** на **объекте Relation,** необходимо примедить соответствующие объекты **[Field](field-object-dao.md)** для определения таблиц основных и внешних ключевых отношений.</span><span class="sxs-lookup"><span data-stu-id="3f986-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="3f986-143">Если имя относится к объекту, который уже входит в коллекцию,  или если имена объектов **Field,** предоставленные в подведомственных полях, являются недействительными, при использовании метода **Приложения** возникает ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="3f986-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="3f986-144">Нельзя установить или сохранить связь между реплицированной таблицей и локальной таблицей.</span><span class="sxs-lookup"><span data-stu-id="3f986-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="3f986-145">Чтобы удалить объект **Relation** из коллекции **[Relations,](relations-collection-dao.md)** используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3f986-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="3f986-146">Пример</span><span class="sxs-lookup"><span data-stu-id="3f986-146">Example</span></span>

<span data-ttu-id="3f986-147">В этом примере метод **CreateRelation** используется для создания связи между **TableDef** сотрудников и новым **TableDef** под названием Departments. </span><span class="sxs-lookup"><span data-stu-id="3f986-147">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="3f986-148">В этом примере также  показано, как  создание нового отношения также создает все необходимые индексы в иностранной таблице (индекс DepartmentsEmployees в таблице Employees).</span><span class="sxs-lookup"><span data-stu-id="3f986-148">This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
