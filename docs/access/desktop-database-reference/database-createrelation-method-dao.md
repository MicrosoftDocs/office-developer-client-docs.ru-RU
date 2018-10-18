---
title: Database.CreateRelation Method (DAO)
TOCTitle: CreateRelation Method
ms:assetid: e240c7e3-c293-5e19-afcc-34d9a5549c64
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835692(v=office.15)
ms:contentKeyID: 48548279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052969
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e1e3919cbb47ca00d6fe9f399cba0c77e91417e7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606818"
---
# <a name="databasecreaterelation-method-dao"></a>Database.CreateRelation Method (DAO)

**Применимо к**: Access 2013 | Office 2013

Создает новый объект **[связи](relation-object-dao.md)** (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражение* . CreateRelation (***имя***, ***таблицы***, ***таблицавнешнегоключа***, ***атрибуты***)

*выражение* Переменная, которая представляет собой объект **базы данных** .

### <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>String</strong> подтип), уникальным образом новый объект <strong>отношения</strong> . Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см допустимые имена <strong>отношения</strong> .</p></td>
</tr>
<tr class="even">
<td><p>Таблица</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>String</strong> подтип) с именем основной таблицы в отношении. Если в таблице не существует, перед добавлением объект <strong>отношения</strong> , возникает ошибка времени выполнения.</p></td>
</tr>
<tr class="odd">
<td><p>Таблицавнешнегоключа</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>String</strong> подтип) с именем таблицы внешнего в отношении. Если в таблице не существует, перед добавлением объект <strong>отношения</strong> , возникает ошибка времени выполнения.</p></td>
</tr>
<tr class="even">
<td><p>Атрибуты</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, который содержит сведения о типе отношения. Свойство <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> для получения дополнительных сведений см.</p></td>
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="return-value"></a>Возвращаемое значение
=======
### <a name="return-value"></a>Возвращаемое значение
>>>>>>> master

Связь

## <a name="remarks"></a>Замечания

Объект **отношения** сведения к ядру базы данных Microsoft Access об отношениях между полями в двух объектов **[TableDef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** . Целостность данных можно реализовать с помощью свойства **атрибуты** .

Если опустить одно или несколько частей необязательно при использовании метода **CreateRelation** , можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию. После добавления объекта, невозможно изменить любые параметры его свойства. Обратитесь к соответствующим разделам отдельных свойств для получения дополнительных сведений.

Прежде чем использовать метод **[Append](fields-append-method-dao.md)** на объект **связи** , необходимо добавить соответствующие объекты **[поля](field-object-dao.md)** для определения таблиц связи первичного и внешнего ключа.

Если имя ссылается на объект, который уже входит в коллекции или недопустимые имена объектов **поля** , представленные в подчиненных коллекции **полей** , то во время выполнения возникает ошибка при использовании метода **Append** .

Не удается установить или поддерживать связь между таблицей реплицированной и локальной таблицы.

Чтобы удалить объект **связи** из коллекции **[отношений](relations-collection-dao.md)** , используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов.

## <a name="example"></a>Пример

В этом примере используется метод **CreateRelation** для создания **связи** между сотрудниками **TableDef** и новые **TableDef** вызван отделов. В этом примере также показано, как создание нового **отношения** будет также создать необходимые **индексов** в таблице внешнего (DepartmentsEmployees Index в таблице «Сотрудники»).

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
