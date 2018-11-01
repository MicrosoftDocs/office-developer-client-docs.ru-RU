---
title: Field2.DataUpdatable Property (DAO)
TOCTitle: DataUpdatable Property
ms:assetid: e6619c4e-26b1-777b-f0de-78fed3dbc890
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835966(v=office.15)
ms:contentKeyID: 48548377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f961bf727c016a025e5ebe7107c5082b1b63deb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885838"
---
# <a name="field2dataupdatable-property-dao"></a><span data-ttu-id="668b6-102">Field2.DataUpdatable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="668b6-102">Field2.DataUpdatable Property (DAO)</span></span>


<span data-ttu-id="668b6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="668b6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="668b6-104">Возвращает значение, указывающее, является ли данные в поля, представленного объектом **поле2** обновляемым.</span><span class="sxs-lookup"><span data-stu-id="668b6-104">Returns a value that indicates whether the data in the field represented by a **Field2** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="668b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="668b6-105">Syntax</span></span>

<span data-ttu-id="668b6-106">*выражение* . DataUpdatable</span><span class="sxs-lookup"><span data-stu-id="668b6-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="668b6-107">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="668b6-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="668b6-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="668b6-108">Remarks</span></span>

<span data-ttu-id="668b6-109">Это свойство можно используйте для определения, можно ли изменить параметр свойства **[Value](field-value-property-dao.md)** объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="668b6-109">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field2** object.</span></span> <span data-ttu-id="668b6-110">Это свойство всегда имеет **значение False** для объекта **поле2** , для свойства **[атрибуты](field-attributes-property-dao.md)** — это **dbAutoIncrField**.</span><span class="sxs-lookup"><span data-stu-id="668b6-110">This property is always **False** on a **Field2** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="668b6-111">Можно использовать свойство **DataUpdatable** **поле2** объектов, которые присоединяются к коллекции **[полей](fields-collection-dao.md)** **[QueryDef](querydef-object-dao.md)**, **[записей](recordset-object-dao.md)** и **[отношения](relation-object-dao.md)** объектов, но не коллекции **полей** **[ Индекс](index-object-dao.md)** объектов **[TableDef](tabledef-object-dao.md)** или.</span><span class="sxs-lookup"><span data-stu-id="668b6-111">You can use the **DataUpdatable** property on **Field2** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="668b6-112">Пример</span><span class="sxs-lookup"><span data-stu-id="668b6-112">Example</span></span>

<span data-ttu-id="668b6-113">В этом примере свойства **DataUpdatable** , с помощью первого поля из шести различных **наборов записей**.</span><span class="sxs-lookup"><span data-stu-id="668b6-113">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**.</span></span> <span data-ttu-id="668b6-114">Функция DataOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="668b6-114">The DataOutput function is required for this procedure to run.</span></span>

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

