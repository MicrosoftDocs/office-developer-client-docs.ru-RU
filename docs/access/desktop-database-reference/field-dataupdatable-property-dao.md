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
# <a name="fielddataupdatable-property-dao"></a>Свойство Field.DataUpdatable (DAO)


**Область применения**: Access 2013, Office 2013


Возвращает значение, которое указывает, могут ли данные в поле, представляемом объектом **[Field,](field-object-dao.md)** быть updatable.

## <a name="syntax"></a>Синтаксис

*выражение .* DataUpdatable

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Используйте это свойство, чтобы определить, можно ли изменить параметр свойства **[Value](field-value-property-dao.md)** объекта **Field.** Это свойство всегда имеет **свойство False** для объекта **Field,** свойство **[Attributes](field-attributes-property-dao.md)** которого **— dbAutoIncrField.**

Свойство **DataUpdatable** можно использовать для объектов **Field,** которые примеся к коллекции **[Fields](fields-collection-dao.md)** объектов **[QueryDef,](querydef-object-dao.md)** **[Recordset](recordset-object-dao.md)** и **[Relation,](relation-object-dao.md)** но не к коллекции **Fields** объектов **[Index](index-object-dao.md)** или **[TableDef.](tabledef-object-dao.md)**

## <a name="example"></a>Пример

В этом примере показано свойство **DataUpdatable,** использующее первое поле из шести различных **наборов записей.** Для запуска этой процедуры требуется функция DataOutput.

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

