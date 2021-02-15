---
title: Свойство Field2.DataUpdatable (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: e6619c4e-26b1-777b-f0de-78fed3dbc890
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835966(v=office.15)
ms:contentKeyID: 48548377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a57ff2daeaaaab202daad55f01eebc6bdf86dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292841"
---
# <a name="field2dataupdatable-property-dao"></a><span data-ttu-id="3f407-102">Свойство Field2.DataUpdatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f407-102">Field2.DataUpdatable property (DAO)</span></span>


<span data-ttu-id="3f407-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f407-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3f407-104">Возвращает значение, которое указывает, могут ли данные в поле, представляемом объектом **Field2,** быть updatable.</span><span class="sxs-lookup"><span data-stu-id="3f407-104">Returns a value that indicates whether the data in the field represented by a **Field2** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f407-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f407-105">Syntax</span></span>

<span data-ttu-id="3f407-106">*выражение .* DataUpdatable</span><span class="sxs-lookup"><span data-stu-id="3f407-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="3f407-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="3f407-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f407-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="3f407-108">Remarks</span></span>

<span data-ttu-id="3f407-109">Используйте это свойство, чтобы определить, можно ли изменить параметр свойства **[Value](field-value-property-dao.md)** объекта **Field2.**</span><span class="sxs-lookup"><span data-stu-id="3f407-109">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field2** object.</span></span> <span data-ttu-id="3f407-110">Это свойство всегда имеет **свойство False** для **объекта Field2,** свойство **[Attributes](field-attributes-property-dao.md)** которого **— dbAutoIncrField.**</span><span class="sxs-lookup"><span data-stu-id="3f407-110">This property is always **False** on a **Field2** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="3f407-111">Свойство **DataUpdatable** можно использовать для объектов **Field2,** которые будут приданы коллекции **[Fields](fields-collection-dao.md)** объектов **[QueryDef,](querydef-object-dao.md)** **[Recordset](recordset-object-dao.md)** и **[Relation,](relation-object-dao.md)** но не коллекции **Fields** объектов **[Index](index-object-dao.md)** или **[TableDef.](tabledef-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="3f407-111">You can use the **DataUpdatable** property on **Field2** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="3f407-112">Пример</span><span class="sxs-lookup"><span data-stu-id="3f407-112">Example</span></span>

<span data-ttu-id="3f407-113">В этом примере показано свойство **DataUpdatable,** использующее первое поле из шести различных **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="3f407-113">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**.</span></span> <span data-ttu-id="3f407-114">Для запуска этой процедуры требуется функция DataOutput.</span><span class="sxs-lookup"><span data-stu-id="3f407-114">The DataOutput function is required for this procedure to run.</span></span>

```vb 
Sub DataUpdatableX() 
 
 Dim dbsNorthwind As Database 
 Dim rstNorthwind As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Open and print report about a table-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a dynaset-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenDynaset) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a snapshot-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenSnapshot) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a forward-only-type Recordset. 
 Set rstNorthwind = .OpenRecordset("Employees", _ 
 dbOpenForwardOnly) 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on 
 ' a select query. 
 Set rstNorthwind = _ 
 .OpenRecordset("Current Product List") 
 DataOutput rstNorthwind 
 
 ' Open and print report about a Recordset based on a 
 ' select query that calculates totals. 
 Set rstNorthwind = .OpenRecordset("Order Subtotals") 
 DataOutput rstNorthwind 
 
 .Close 
 End With 
 
End Sub 
 
Function DataOutput(rstTemp As Recordset) 
 
 With rstTemp 
 Debug.Print "Recordset: " & .Name & ", "; 
 Select Case .Type 
 Case dbOpenTable 
 Debug.Print "dbOpenTable" 
 Case dbOpenDynaset 
 Debug.Print "dbOpenDynaset" 
 Case dbOpenSnapshot 
 Debug.Print "dbOpenSnapshot" 
 Case dbOpenForwardOnly 
 Debug.Print "dbOpenForwardOnly" 
 End Select 
 Debug.Print " Field: " & .Fields(0).Name & ", " & _ 
 "DataUpdatable = " & .Fields(0).DataUpdatable 
 Debug.Print 
 .Close 
 End With 
 
End Function 
 
```

