---
title: Коллекция Indexes (DAO)
TOCTitle: Indexes Collection
ms:assetid: 26450e85-c79d-b12a-d760-dfc89c37f36c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191889(v=office.15)
ms:contentKeyID: 48543802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f731862e12a75f91d07ea7d012cc33dad5be0b55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291568"
---
# <a name="indexes-collection-dao"></a>Коллекция Indexes (DAO)

**Область применения**: Access 2013, Office 2013

Коллекция **Indexes** содержит все хранимые объекты **Индекса** объекта **TableDef** (только для рабочей области Microsoft Access).

## <a name="remarks"></a>Заметки

При доступе к объекту Recordset табли с помощью свойства **Index** укажите порядок записей. Установите для этого свойства параметр **свойства Name** существующего объекта **Index** в коллекции **Indexes** объекта **[TableDef,](tabledef-object-dao.md)** входящего в объект **[Recordset.](recordset-object-dao.md)**

> [!NOTE]
> Вы можете использовать метод **Append** или **Delete** для коллекции **Indexes,** только если для параметра **[updatable](connection-updatable-property-dao.md)** свойства содержащегося объекта **TableDef** задано **true.**

После создания объекта **Index** следует использовать метод **Append,** чтобы добавить его в коллекцию **Indexes** объекта **TableDef.**

> [!IMPORTANT]
> Убедитесь, что данные соответствуют атрибутам нового индекса. Если индексу требуются уникальные значения, убедитесь, что в существующих записях данных нет дубликатов. Если дубликаты существуют, яма базы данных Microsoft Access не может создать индекс; захватимые результаты ошибки при попытке использовать метод Append в новом индексе.

## <a name="example"></a>Пример

В этом примере создается новый объект **Index,** он включается в коллекцию **Indexes** объекта Employees **TableDef,** а затем нумеруется коллекция **Indexes** **объекта TableDef.** Наконец, он нумерирует набор **записей,** сначала используя основной **индекс,** а затем с помощью нового **индекса.** Процедура IndexOutput необходима для запуска этой процедуры.

```vb
    Sub IndexObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create new index, create and append Field 
     ' objects to its Fields collection. 
     Set idxNew = .CreateIndex("NewIndex") 
     
     With idxNew 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     
     ' Add new Index object to the Indexes collection 
     ' of the Employees table collection. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection of Employees 
     ' table. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Print report using old and new indexes. 
     IndexOutput rstEmployees, "PrimaryKey" 
     IndexOutput rstEmployees, idxNew.Name 
     rstEmployees.Close 
     
     ' Delete new Index because this is a 
     ' demonstration. 
     .Indexes.Delete idxNew.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub IndexOutput(rstTemp As Recordset, _ 
     strIndex As String) 
     ' Report function for FieldX. 
     
     With rstTemp 
     ' Set the index. 
     .Index = strIndex 
     .MoveFirst 
     Debug.Print "Recordset = " & .Name & _ 
     ", Index = " & .Index 
     Debug.Print " EmployeeID - Country - Name" 
     
     ' Enumerate the recordset using the specified 
     ' index. 
     Do While Not .EOF 
     Debug.Print " " & !EmployeeID & " - " & _ 
     !Country & " - " & !LastName & ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Sub 
```

<br/>

В этом примере метод **CreateIndex** используется для создания двух новых объектов **Index,** а затем их можно придать коллекции **Indexes** объекта Employees **TableDef.** Затем он нумерирует коллекцию **Indexes** объекта **TableDef,** коллекцию **Fields** новых объектов **Index** и коллекцию свойств новых объектов **Index.** Для запуска этой процедуры требуется функция CreateIndexOutput.

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
