---
title: Свойство field2. доПускает обновление (DAO)
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
# <a name="field2dataupdatable-property-dao"></a><span data-ttu-id="3bb90-102">Свойство field2. доПускает обновление (DAO)</span><span class="sxs-lookup"><span data-stu-id="3bb90-102">Field2.DataUpdatable property (DAO)</span></span>


<span data-ttu-id="3bb90-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bb90-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3bb90-104">Возвращает значение, которое указывает, является ли данные в поле, представленном объектом **field2** , обновляемым.</span><span class="sxs-lookup"><span data-stu-id="3bb90-104">Returns a value that indicates whether the data in the field represented by a **Field2** object is updatable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb90-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bb90-105">Syntax</span></span>

<span data-ttu-id="3bb90-106">*Expression* . Обновляемые с возможностью обновления</span><span class="sxs-lookup"><span data-stu-id="3bb90-106">*expression* .DataUpdatable</span></span>

<span data-ttu-id="3bb90-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="3bb90-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bb90-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3bb90-108">Remarks</span></span>

<span data-ttu-id="3bb90-109">Используйте это свойство, чтобы определить, можно ли изменить значение свойства **[value](field-value-property-dao.md)** объекта **field2** .</span><span class="sxs-lookup"><span data-stu-id="3bb90-109">Use this property to determine whether you can change the **[Value](field-value-property-dao.md)** property setting of a **Field2** object.</span></span> <span data-ttu-id="3bb90-110">Это свойство всегда имеет **значение false** для объекта **field2** , свойство **[Attributes](field-attributes-property-dao.md)** которого равно **дбаутоинкрфиелд**.</span><span class="sxs-lookup"><span data-stu-id="3bb90-110">This property is always **False** on a **Field2** object whose **[Attributes](field-attributes-property-dao.md)** property is **dbAutoIncrField**.</span></span>

<span data-ttu-id="3bb90-111">Можно использовать свойство с **возможностью обновления** для объектов **field2** , добавленных в коллекцию Fields объектов **[](fields-collection-dao.md)** **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** и **[relation](relation-object-dao.md)** , но не коллекцию **Fields** объекта **[ Объекты index](index-object-dao.md)** или **[tabledef](tabledef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="3bb90-111">You can use the **DataUpdatable** property on **Field2** objects that are appended to the **[Fields](fields-collection-dao.md)** collection of **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)**, and **[Relation](relation-object-dao.md)** objects, but not the **Fields** collection of **[Index](index-object-dao.md)** or **[TableDef](tabledef-object-dao.md)** objects.</span></span>

## <a name="example"></a><span data-ttu-id="3bb90-112">Пример</span><span class="sxs-lookup"><span data-stu-id="3bb90-112">Example</span></span>

<span data-ttu-id="3bb90-113">В этом примере показано свойство с **возможностью обновления** данных, использующее первое поле из шести разных **наборов записей**.</span><span class="sxs-lookup"><span data-stu-id="3bb90-113">This example demonstrates the **DataUpdatable** property using the first field from six different **Recordsets**.</span></span> <span data-ttu-id="3bb90-114">Для выполнения этой процедуры требуется функция Output.</span><span class="sxs-lookup"><span data-stu-id="3bb90-114">The DataOutput function is required for this procedure to run.</span></span>

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

