---
title: Свойство Field. доПускает обновление (DAO)
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
# <a name="fielddataupdatable-property-dao"></a>Свойство Field. доПускает обновление (DAO)


**Область применения**: Access 2013, Office 2013


Возвращает значение, которое указывает, можно ли обновлять данные в поле, представленном объектом **[field](field-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*Expression* . Обновляемые с возможностью обновления

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Комментарии

Используйте это свойство, чтобы определить, можно ли изменить значение свойства **[value](field-value-property-dao.md)** объекта **field** . Это свойство всегда имеет **значение false** для объекта **field** , свойство **[Attributes](field-attributes-property-dao.md)** которого равно **дбаутоинкрфиелд**.

Свойство с **возможностью обновления** данных можно использовать для объектов **field** , добавляемых в коллекцию Fields **[](fields-collection-dao.md)** объектов **[QueryDef](querydef-object-dao.md)**, **[Recordset](recordset-object-dao.md)** и **[relation](relation-object-dao.md)** , но не для коллекции **Fields** **[индекса ](index-object-dao.md)** объекты **[tabledef](tabledef-object-dao.md)** .

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

