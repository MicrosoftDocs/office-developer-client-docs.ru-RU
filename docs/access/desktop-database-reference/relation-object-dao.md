---
title: Объект отношения (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49e8cdb7586af93ca17782ba0cb1071036c38eeb
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936954"
---
# <a name="relation-object-dao"></a>Объект отношения (DAO)


**Применимо к**: Access 2013, Office 2013

Объект **связи** представляет связь между полями в таблицах и запросах (Microsoft Access базами данных, ядро только).

## <a name="remarks"></a>Примечания

Объект **связи** можно использовать для создания новых связей и проверить существующих связей между таблицами в базе данных.

Используется объект **связи** и его свойства, можно выполнить следующие действия.

  - Укажите связи между полями в базовые таблицы (но не отношения, который включает в себя запроса или связанной таблицы).

  - Установить необязательного отношения между любой тип таблицы или запроса — собственная или связанный.

  - Свойство **имени** для ссылки на отношения между поля в указанной таблице основной и ссылающаяся таблица внешнего.

  - Свойство **атрибуты** определить, является ли связь между поля в таблице один к одному или один ко многим и как обеспечения целостности данных.

  - Используйте свойство **Attributes** для определения ли ядро базы данных Microsoft Access можно выполнить обновление каскадных таблиц каскадных операций и удаления на основной и внешних таблиц.

  - Используйте свойство **атрибуты** для определения, остается ли связь между поля в таблице объединение или правом объединение.

  - Используйте свойство **Name** из всех объектов **поля** в коллекции **полей** объект **связи** или возвращает имена полей в первичный ключ указанную таблицу или параметры свойства **ForeignName** Объекты **поля** или возвращает имена полей в внешний ключ ссылающаяся таблица.

При внесении изменений, которые нарушают связей, определенных для базы данных, то перехватываемые возникает ошибка. При запросе каскадные обновления или каскадных операций delete, ядро базы данных Microsoft Access также изменяет основной ключ или таблицы внешних ключей для обеспечения связи, которые можно установить.

Например базы данных Northwind содержит отношение между таблицы заказов и таблице Customers. Первичный ключ — это поле CustomerID в таблице клиентов, а в поле CustomerID в таблице Orders является внешний ключ. Для ядра СУБД Microsoft Access для принятия новой записи в таблице Orders будет выполняться поиск в таблице Клиенты соответствие на поле CustomerID таблицы заказов. Если ядро базы данных Microsoft Access не находит соответствие, он не принимает новую запись, и становится перехватываемые ошибки.

Если целостность данных, уникальный индекс должны уже существовать ключевого поля таблицы, на который указывает ссылка. Ядро базы данных Microsoft Access автоматически создает индекс с установленным свойством **внешнего** в качестве внешнего ключа в ссылающаяся таблица.

Чтобы создать новый объект **отношения** , используйте метод **CreateRelation** . Для ссылки на объект **связи** в семействе сайтов, с его порядковый номер или **его свойства Name** , можно используйте любой из следующих форм синтаксиса:

**Отношения** (0)

**Отношения** («имя»)

**Отношения**\!\[имя\]

## <a name="example"></a>Пример

В этом примере показано, как управлять существующий объект **отношения** ввода данных. Процедура пытается добавить запись, намеренно неправильный идентификатор категории; Это вызывает обработчик ошибок.

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

В этом примере используется метод **CreateRelation** для создания **связи** между сотрудниками **TableDef** и новые **TableDef** вызван отделов. Также показано, как создание нового **отношения** также создается необходимые **индексов** в таблице внешнего (DepartmentsEmployees Index в таблице «Сотрудники»).

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
