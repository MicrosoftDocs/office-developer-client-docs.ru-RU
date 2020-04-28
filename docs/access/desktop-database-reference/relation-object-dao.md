---
title: Объект Relation (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3eeaf8bf46d8673731243a1161ac578062a01f89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307051"
---
# <a name="relation-object-dao"></a>Объект Relation (DAO)


**Область применения**: Access 2013, Office 2013

Объект **relation** представляет связь между полями в таблицах или запросах (только базы данных ядра СУБД Microsoft Access).

## <a name="remarks"></a>Примечания

Объект **relation** можно использовать для создания новых связей и проверки существующих связей в базе данных.

Используя объект **relation** и его свойства, вы можете:

  - Указание принудительного отношения между полями в базовых таблицах (но не отношение, включающее запрос или связанную таблицу).

  - Установите непринудительные связи между любым типом таблицы или запросом (собственными или связанными).

  - Используйте свойство **Name** , чтобы сослаться на связь между полями в главной таблице, указанной в ссылке, и внешней таблице, ссылающейся на нее.

  - Используйте свойство **Attributes** , чтобы определить, является ли связь между полями в таблице "один к одному" или "один-ко-многим", а также как обеспечить целостность ссылок.

  - Используйте свойство **Attributes** , чтобы определить, может ли ядро СУБД Microsoft Access выполнять каскадное обновление и каскадные операции удаления для основной и внешней таблиц.

  - Используйте свойство **Attributes** , чтобы определить, является ли связь между полями в таблице левой или с правой присоединением.

  - Используйте свойство **Name** для всех объектов **field** в коллекции **Fields** объекта **relation** , чтобы задать или вернуть имена полей в первичном ключе указанной таблицы, или параметры свойства **фореигннаме** объектов **field** , чтобы задать или вернуть имена полей в внешнем ключе ссылающейся таблицы.

При внесении изменений, которые нарушают связи, установленные для базы данных, возникает перехватываемая ошибка. Если вы запрашиваете каскадное обновление или каскадное удаление, ядро СУБД Microsoft Access также изменяет таблицы первичного ключа или внешнего ключа для применения устанавливаемых отношений.

Например, база данных Northwind содержит связь между таблицей Orders и таблицей Customers. Поле CustomerID таблицы Customers — это первичный ключ, а поле CustomerID таблицы Orders — это внешний ключ. Чтобы ядро СУБД Microsoft Access принимало новую запись в таблице Orders, она ищет в таблице Customers значение, соответствующее полю CustomerID таблицы Orders. Если ядро СУБД Microsoft Access не находит соответствующее значение, оно не принимает новую запись и возникает перехватываемая ошибка.

При применении ссылочной целостности для ключевого поля указанной таблицы должен существовать уникальный индекс. Ядро СУБД Microsoft Access автоматически создает индекс с **внешним** свойством, равным внешнему ключу в ссылающейся таблице.

Чтобы создать новый объект **relation** , используйте метод **креатерелатион** . Чтобы сослаться на объект **relation** в коллекции по его порядковому номеру или по значению свойства **Name** , используйте любую из следующих синтаксических форм:

**Отношения**(0)

**Отношения**("имя")

**Имя отношения**\!\[\]

## <a name="example"></a>Пример

В этом примере показано, как существующий объект **relation** может управлять вводом данных. Процедура пытается добавить запись с намеренно неправильным идентификатором CategoryID; Это запускает процедуру обработки ошибок.

```vb 
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

В этом примере используется метод **креатерелатион** для создания **отношения** между сотрудниками **tabledef** и новыми **tabledef** , называемыми отделами. Кроме того, показано, как создание нового **отношения** также приведет к созданию необходимых **индексов** во внешней таблице (индекс департментсемплойис в таблице Employees).

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
