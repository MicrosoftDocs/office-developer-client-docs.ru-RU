---
title: Метод Database. Креатерелатион (DAO)
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
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="915ad-102">Метод Database. Креатерелатион (DAO)</span><span class="sxs-lookup"><span data-stu-id="915ad-102">Database.CreateRelation method (DAO)</span></span>

<span data-ttu-id="915ad-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="915ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="915ad-104">Создает новый объект **[relation](relation-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="915ad-104">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="915ad-105">.</span><span class="sxs-lookup"><span data-stu-id="915ad-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="915ad-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="915ad-106">Syntax</span></span>

<span data-ttu-id="915ad-107">*Expression* . Креатерелатион (***имя***, ***Таблица***, ***ForeignTable***, ***атрибуты***)</span><span class="sxs-lookup"><span data-stu-id="915ad-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="915ad-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="915ad-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="915ad-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="915ad-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="915ad-110">Имя</span><span class="sxs-lookup"><span data-stu-id="915ad-110">Name</span></span></p></th>
<th><p><span data-ttu-id="915ad-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="915ad-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="915ad-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="915ad-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="915ad-113">Описание</span><span class="sxs-lookup"><span data-stu-id="915ad-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="915ad-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="915ad-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="915ad-115">Необязательный</span><span class="sxs-lookup"><span data-stu-id="915ad-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="915ad-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="915ad-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="915ad-117"><strong>Variant</strong> (подтип<strong>String</strong> ), уникально названный новому объекту <strong>relation</strong> .</span><span class="sxs-lookup"><span data-stu-id="915ad-117">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object.</span></span> <span data-ttu-id="915ad-118">Сведения о допустимых именах <strong>отношений</strong> приведены в свойстве <strong><a href="connection-name-property-dao.md">Name</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="915ad-118">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="915ad-119"><em>Table</em></span><span class="sxs-lookup"><span data-stu-id="915ad-119"><em>Table</em></span></span></p></td>
<td><p><span data-ttu-id="915ad-120">Необязательный</span><span class="sxs-lookup"><span data-stu-id="915ad-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="915ad-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="915ad-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="915ad-122"><strong>Variant</strong> (подтип<strong>String</strong> ), который называет основную таблицу в отношении.</span><span class="sxs-lookup"><span data-stu-id="915ad-122">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation.</span></span> <span data-ttu-id="915ad-123">Если перед добавлением объекта <strong>relation</strong> таблица не существует, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="915ad-123">If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="915ad-124"><em>ForeignTable</em></span><span class="sxs-lookup"><span data-stu-id="915ad-124"><em>ForeignTable</em></span></span></p></td>
<td><p><span data-ttu-id="915ad-125">Необязательный</span><span class="sxs-lookup"><span data-stu-id="915ad-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="915ad-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="915ad-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="915ad-127"><strong>Variant</strong> (подтип<strong>String</strong> ), который называет внешнюю таблицу в отношении.</span><span class="sxs-lookup"><span data-stu-id="915ad-127">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation.</span></span> <span data-ttu-id="915ad-128">Если перед добавлением объекта <strong>relation</strong> таблица не существует, возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="915ad-128">If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="915ad-129"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="915ad-129"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="915ad-130">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="915ad-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="915ad-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="915ad-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="915ad-132">Константа или сочетание констант, содержащих сведения о типе связи.</span><span class="sxs-lookup"><span data-stu-id="915ad-132">A constant or combination of constants that contains information about the relationship type.</span></span> <span data-ttu-id="915ad-133">Дополнительные сведения см. в свойстве <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="915ad-133">See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="915ad-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="915ad-134">Return value</span></span>

<span data-ttu-id="915ad-135">Relation</span><span class="sxs-lookup"><span data-stu-id="915ad-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="915ad-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="915ad-136">Remarks</span></span>

<span data-ttu-id="915ad-137">Объект **relation** предоставляет сведения для ядра СУБД Microsoft Access относительно связи между полями в двух объектах **[tabledef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="915ad-137">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects.</span></span> <span data-ttu-id="915ad-138">Можно реализовать целостность ссылок с помощью свойства **Attributes** .</span><span class="sxs-lookup"><span data-stu-id="915ad-138">You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="915ad-139">Если опустить одну или несколько дополнительных частей при использовании метода **креатерелатион** , можно использовать соответствующий оператор присваивания для задания или сброса соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="915ad-139">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="915ad-140">После добавления объекта невозможно изменить параметры его свойств.</span><span class="sxs-lookup"><span data-stu-id="915ad-140">After you append the object, you can't alter any of its property settings.</span></span> <span data-ttu-id="915ad-141">См. разделы для отдельных свойств для получения дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="915ad-141">See the individual property topics for more details.</span></span>

<span data-ttu-id="915ad-142">Прежде чем можно будет использовать метод **[append](fields-append-method-dao.md)** для объекта **relation** , необходимо добавить соответствующие объекты **[field](field-object-dao.md)** , чтобы определить первичные и внешние таблицы связи.</span><span class="sxs-lookup"><span data-stu-id="915ad-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="915ad-143">Если имя ссылается на объект, который уже является членом коллекции, или если имена объекта **поля** , указанные в коллекции подчиненных **полей** , являются недопустимыми, при использовании метода **append** возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="915ad-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="915ad-144">Невозможно установить или поддерживать связь между реплицированной таблицей и локальной таблицей.</span><span class="sxs-lookup"><span data-stu-id="915ad-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="915ad-145">Чтобы удалить объект **relation** из коллекции **[связей](relations-collection-dao.md)** , используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="915ad-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="915ad-146">Пример</span><span class="sxs-lookup"><span data-stu-id="915ad-146">Example</span></span>

<span data-ttu-id="915ad-147">В этом примере используется метод **креатерелатион** для создания **отношения** между сотрудниками **tabledef** и новыми **tabledef** , называемыми отделами.</span><span class="sxs-lookup"><span data-stu-id="915ad-147">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments.</span></span> <span data-ttu-id="915ad-148">В этом примере также показано, как создание нового **отношения** также приведет к созданию необходимых **индексов** во внешней таблице (индекс департментсемплойис в таблице Employees).</span><span class="sxs-lookup"><span data-stu-id="915ad-148">This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
