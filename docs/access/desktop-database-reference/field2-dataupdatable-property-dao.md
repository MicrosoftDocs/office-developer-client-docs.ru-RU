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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698962"
---
# <a name="field2dataupdatable-property-dao"></a>Свойство Field2.DataUpdatable (DAO)


**Применимо к**: Access 2013, Office 2013


Возвращает значение, указывающее, является ли данные в поля, представленного объектом **поле2** обновляемым.

## <a name="syntax"></a>Синтаксис

*выражение* . DataUpdatable

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Это свойство можно используйте для определения, можно ли изменить параметр свойства **[Value](field-value-property-dao.md)** объекта **поле2** . Это свойство всегда имеет **значение False** для объекта **поле2** , для свойства **[атрибуты](field-attributes-property-dao.md)** — это **dbAutoIncrField**.

Можно использовать свойство **DataUpdatable** **поле2** объектов, которые присоединяются к коллекции **[полей](fields-collection-dao.md)** **[QueryDef](querydef-object-dao.md)**, **[записей](recordset-object-dao.md)** и **[отношения](relation-object-dao.md)** объектов, но не коллекции **полей** **[ Индекс](index-object-dao.md)** объектов **[TableDef](tabledef-object-dao.md)** или.

## <a name="example"></a>Пример

В этом примере свойства **DataUpdatable** , с помощью первого поля из шести различных **наборов записей**. Функция DataOutput является обязательным для выполнения этой процедуры.

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

