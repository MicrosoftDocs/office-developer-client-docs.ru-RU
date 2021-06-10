---
title: Свойство Field.DataUpdatable (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: 08ca57b6-2d7c-36b4-7d51-b76ac5467163
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845029(v=office.15)
ms:contentKeyID: 48543104
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052988
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8678b825f509f483bf70d3aa2f3d767dbf7b0e32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293135"
---
# <a name="fielddataupdatable-property-dao"></a><span data-ttu-id="9b470-102">Свойство Field.DataUpdatable (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b470-102">Field.DataUpdatable property (DAO)</span></span>


<span data-ttu-id="9b470-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b470-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9b470-104">Возвращает значение, которое указывает, являются ли данные в поле, представленного объектом **[Field,](field-object-dao.md)** updatable.</span><span class="sxs-lookup"><span data-stu-id="9b470-104">Returns a value that indicates whether the data in the field represented by a **[Field](field-object-dao.md)** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b470-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b470-105">Syntax</span></span>

<span data-ttu-id="9b470-106">*выражения* . DataUpdatable</span><span class="sxs-lookup"><span data-stu-id="9b470-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="9b470-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="9b470-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b470-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b470-108">Remarks</span></span>

<span data-ttu-id="9b470-109">Используйте это свойство, чтобы определить, можно ли изменить параметр **[свойства Value](field-value-property-dao.md)** объекта **Field.**</span><span class="sxs-lookup"><span data-stu-id="9b470-109">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field** object.</span></span> <span data-ttu-id="9b470-110">Это свойство **всегда false** для объекта **Field,** **[свойством атрибутов](field-attributes-property-dao.md)** которого **является dbAutoIncrField.**</span><span class="sxs-lookup"><span data-stu-id="9b470-110">This property is always **False** on a **Field** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="9b470-111">**[](index-object-dao.md)** Свойство **DataUpdatable** можно использовать  для объектов Field, которые **[](fields-collection-dao.md)** примыкают к коллекции **[Полей объектов QueryDef,](querydef-object-dao.md)** **[Recordset](recordset-object-dao.md)** и **[Relation,](relation-object-dao.md)** но не коллекцию **Полей** объектов Index или **[TableDef.](tabledef-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="9b470-111">You can use the **DataUpdatable** property on **Field** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="9b470-112">Пример</span><span class="sxs-lookup"><span data-stu-id="9b470-112">Example</span></span>

<span data-ttu-id="9b470-113">В этом примере демонстрируется свойство **DataUpdatable** с помощью первого поля из шести различных **наборов записей.**</span><span class="sxs-lookup"><span data-stu-id="9b470-113">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**.</span></span> <span data-ttu-id="9b470-114">Для запуска этой процедуры требуется функция DataOutput.</span><span class="sxs-lookup"><span data-stu-id="9b470-114">The DataOutput function is required for this procedure to run.</span></span>

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

