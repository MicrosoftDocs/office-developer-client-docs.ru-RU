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
# <a name="field2dataupdatable-property-dao"></a>Свойство field2. доПускает обновление (DAO)


**Область применения**: Access 2013, Office 2013


Возвращает значение, которое указывает, является ли данные в поле, представленном объектом **field2** , обновляемым.

## <a name="syntax"></a>Синтаксис

*Expression* . Обновляемые с возможностью обновления

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Замечания

Используйте это свойство, чтобы определить, можно ли изменить значение свойства **[value](field-value-property-dao.md)** объекта **field2** . Это свойство всегда имеет **значение false** для объекта **field2** , свойство **[Attributes](field-attributes-property-dao.md)** которого равно **дбаутоинкрфиелд**.

Можно использовать свойство с **возможностью обновления** для объектов **field2** , добавленных в коллекцию Fields объектов **[](fields-collection-dao.md)** **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** и **[relation](relation-object-dao.md)** , но не коллекцию **Fields** объекта **[ Объекты index](index-object-dao.md)** или **[tabledef](tabledef-object-dao.md)** .

## <a name="example"></a>Пример

В этом примере показано свойство с **возможностью обновления** данных, использующее первое поле из шести разных **наборов записей**. Для выполнения этой процедуры требуется функция Output.

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

