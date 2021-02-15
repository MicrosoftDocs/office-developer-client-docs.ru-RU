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

Объект **Relation** представляет отношение между полями в таблицах или запросах (только для баз данных ям баз данных Microsoft Access).

## <a name="remarks"></a>Заметки

Объект **Relation** можно использовать для создания новых отношений и изучения существующих отношений в базе данных.

С помощью **объекта Relation** и его свойств можно:

  - Укажите принудительное отношение между полями в базовых таблицах (но не отношение, которое включает запрос или связанную таблицу).

  - Установить неподтвержденные связи между любым типом таблицы или запроса — машинным или связанным.

  - Используйте свойство **Name** для ссылки на связь между полями в основной таблице, на которые ссылается ссылка, и внешней таблицей, на которые ссылается ссылка.

  - Используйте свойство **Attributes,** чтобы определить, является ли отношение между полями в таблице "один к одному" или "один-к-многим" и как обеспечить целостность ссылок.

  - Используйте свойство **Attributes,** чтобы определить, может ли яд баз данных Microsoft Access выполнять каскадные операции обновления и каскадного удаления в основных и внешних таблицах.

  - Используйте свойство **Attributes,** чтобы определить, является ли связь между полями в таблице левым или правым.

  - Используйте свойство **Name** всех объектов **Field** в коллекции **Fields** объекта **Relation,** чтобы установить или вернуть имена полей в первичном ключе таблицы, на который ссылается ссылка, или параметры свойств **ForeignName** объектов **Field,** чтобы установить или вернуть имена полей во внешнем ключе таблицы ссылок.

При внесении изменений, нарушающих отношения, установленные для базы данных, возникает перехируемая ошибка. Если вы запрашиваете операции каскадного обновления или каскадного удаления, модуль базы данных Microsoft Access также изменяет первичный ключ или таблицы внешних ключей для применения устанавливаемой связи.

Например, база данных Northwind содержит связь между таблицей Orders и таблицей Customers. Поле CustomerID таблицы Customers является первичным ключом, а поле CustomerID таблицы "Заказы" — внешней клавишей. Чтобы ядер баз данных Microsoft Access принять новую запись в таблице "Заказы", он выполняет поиск совпадения в таблице Customers в поле CustomerID таблицы "Заказы". Если яд баз данных Microsoft Access не находит совпадения, он не принимает новую запись, и возникает перехименовывуемая ошибка.

При обеспечении целостности ссылок для ключевого поля таблицы, на который ссылается ссылка, уже должен существовать уникальный индекс. Яд баз данных Microsoft Access автоматически создает индекс со свойством **Foreign,** который будет выступать в качестве внешнего ключа в таблице ссылок.

Чтобы создать новый **объект Relation,** используйте **метод CreateRelation.** Чтобы сослаться на **объект Relation** в коллекции по порядковому номеру или по его свойству **Name,** используйте любую из следующих синтаксис форм:

**Relations**(0)

**Relations**("name")

 \! Relations \[ name\]

## <a name="example"></a>Пример

В этом примере показано, как **существующий объект Relation** может управлять записью данных. Процедура пытается добавить запись с намеренно неправильным categoryID; Это запускает процедуру обработки ошибок.

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

В этом примере метод **CreateRelation** используется для создания отношения между **TableDef** Employees и новым **TableDef** под названием Departments.  В нем также показано, как при  создании нового отношения также будут создаваться все необходимые индексы во внешней таблице (индекс DepartmentsEmployees в таблице Employees). 

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
