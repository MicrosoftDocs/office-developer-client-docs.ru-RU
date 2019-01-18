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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716882"
---
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="c9900-102">Метод Database.CreateRelation (DAO)</span><span class="sxs-lookup"><span data-stu-id="c9900-102">Database.CreateRelation method (DAO)</span></span>

<span data-ttu-id="c9900-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9900-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9900-104">Создает новый объект **[связи](relation-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c9900-104">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="c9900-105">.</span><span class="sxs-lookup"><span data-stu-id="c9900-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="c9900-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9900-106">Syntax</span></span>

<span data-ttu-id="c9900-107">*выражение* . CreateRelation (***имя***, ***таблицы***, ***таблицавнешнегоключа***, ***атрибуты***)</span><span class="sxs-lookup"><span data-stu-id="c9900-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="c9900-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="c9900-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9900-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9900-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9900-110">Имя</span><span class="sxs-lookup"><span data-stu-id="c9900-110">Name</span></span></p></th>
<th><p><span data-ttu-id="c9900-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="c9900-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c9900-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c9900-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="c9900-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c9900-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9900-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="c9900-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="c9900-115">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c9900-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="c9900-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c9900-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c9900-117"><strong>Variant</strong> (<strong>String</strong> подтип), уникальным образом новый объект <strong>отношения</strong> .</span><span class="sxs-lookup"><span data-stu-id="c9900-117">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object.</span></span> <span data-ttu-id="c9900-118">Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см допустимые имена <strong>отношения</strong> .</span><span class="sxs-lookup"><span data-stu-id="c9900-118">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9900-119"><em>Table</em></span><span class="sxs-lookup"><span data-stu-id="c9900-119"><em>Table</em></span></span></p></td>
<td><p><span data-ttu-id="c9900-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c9900-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="c9900-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c9900-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c9900-122"><strong>Variant</strong> (<strong>String</strong> подтип) с именем основной таблицы в отношении.</span><span class="sxs-lookup"><span data-stu-id="c9900-122">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation.</span></span> <span data-ttu-id="c9900-123">Если в таблице не существует, перед добавлением объект <strong>отношения</strong> , возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="c9900-123">If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9900-124"><em>Таблицавнешнегоключа</em></span><span class="sxs-lookup"><span data-stu-id="c9900-124"><em>ForeignTable</em></span></span></p></td>
<td><p><span data-ttu-id="c9900-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c9900-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="c9900-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c9900-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c9900-127"><strong>Variant</strong> (<strong>String</strong> подтип) с именем таблицы внешнего в отношении.</span><span class="sxs-lookup"><span data-stu-id="c9900-127">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation.</span></span> <span data-ttu-id="c9900-128">Если в таблице не существует, перед добавлением объект <strong>отношения</strong> , возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="c9900-128">If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9900-129"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="c9900-129"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="c9900-130">Необязательный</span><span class="sxs-lookup"><span data-stu-id="c9900-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="c9900-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c9900-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c9900-132">Константа или сочетание констант, который содержит сведения о типе отношения.</span><span class="sxs-lookup"><span data-stu-id="c9900-132">A constant or combination of constants that contains information about the relationship type.</span></span> <span data-ttu-id="c9900-133">Свойство <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="c9900-133">See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="c9900-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9900-134">Return value</span></span>

<span data-ttu-id="c9900-135">Relation</span><span class="sxs-lookup"><span data-stu-id="c9900-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="c9900-136">Замечания</span><span class="sxs-lookup"><span data-stu-id="c9900-136">Remarks</span></span>

<span data-ttu-id="c9900-137">Объект **отношения** сведения к ядру базы данных Microsoft Access об отношениях между полями в двух объектов **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="c9900-137">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects.</span></span> <span data-ttu-id="c9900-138">Целостность данных можно реализовать с помощью свойства **атрибуты** .</span><span class="sxs-lookup"><span data-stu-id="c9900-138">You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="c9900-139">Если опустить одно или несколько частей необязательно при использовании метода **CreateRelation** , можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="c9900-139">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="c9900-140">После добавления объекта, невозможно изменить любые параметры его свойства.</span><span class="sxs-lookup"><span data-stu-id="c9900-140">After you append the object, you can't alter any of its property settings.</span></span> <span data-ttu-id="c9900-141">Обратитесь к соответствующим разделам отдельных свойств для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="c9900-141">See the individual property topics for more details.</span></span>

<span data-ttu-id="c9900-142">Прежде чем использовать метод **[Append](fields-append-method-dao.md)** на объект **связи** , необходимо добавить соответствующие объекты **[поля](field-object-dao.md)** для определения таблиц связи первичного и внешнего ключа.</span><span class="sxs-lookup"><span data-stu-id="c9900-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="c9900-143">Если имя ссылается на объект, который уже входит в коллекции или недопустимые имена объектов **поля** , представленные в подчиненных коллекции **полей** , то во время выполнения возникает ошибка при использовании метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="c9900-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="c9900-144">Не удается установить или поддерживать связь между таблицей реплицированной и локальной таблицы.</span><span class="sxs-lookup"><span data-stu-id="c9900-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="c9900-145">Чтобы удалить объект **связи** из коллекции **[отношений](relations-collection-dao.md)** , используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="c9900-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="c9900-146">Пример</span><span class="sxs-lookup"><span data-stu-id="c9900-146">Example</span></span>

<span data-ttu-id="c9900-147">В этом примере используется метод **CreateRelation** для создания **связи** между сотрудниками **TableDef** и новые **TableDef** вызван отделов.</span><span class="sxs-lookup"><span data-stu-id="c9900-147">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="c9900-148">В этом примере также показано, как создание нового **отношения** будет также создать необходимые **индексов** в таблице внешнего (DepartmentsEmployees Index в таблице «Сотрудники»).</span><span class="sxs-lookup"><span data-stu-id="c9900-148">This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
