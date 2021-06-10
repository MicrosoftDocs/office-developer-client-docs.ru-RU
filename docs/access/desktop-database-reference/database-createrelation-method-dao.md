---
title: Метод Database.CreateRelation (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 365835bc579a431d34b65cd27ed4de4e12bca309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294955"
---
# <a name="databasecreaterelation-method-dao"></a>Метод Database.CreateRelation (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[Relation](relation-object-dao.md)** (только рабочие пространства Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражения* . CreateRelation ***(Имя***, ***Таблица***, ***ForeignTable***, ***Атрибуты***)

*выражение*: переменная, представляющая объект **Database**.

## <a name="parameters"></a>Параметры

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
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Подтип <strong>Variant</strong> <strong>(String),</strong> который однозначно называет новый объект <strong>Relation.</strong> Сведения о <strong><a href="connection-name-property-dao.md">допустимом</a></strong> имени Relation см. в свойстве <strong>Name.</strong></p></td>
</tr>
<tr class="even">
<td><p><em>Table</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Подтип <strong>Variant</strong> <strong>(String),</strong> который называет основную таблицу в связи. Если таблица не существует до того, как примыкать к объекту <strong>Relation,</strong> возникает ошибка времени запуска.</p></td>
</tr>
<tr class="odd">
<td><p><em>ForeignTable</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Подтип</strong> <strong>Variant (String),</strong> который называет иностранную таблицу в связи. Если таблица не существует до того, как примыкать к объекту <strong>Relation,</strong> возникает ошибка времени запуска.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, которые содержат сведения о типе отношений. Сведения см. <strong><a href="field-attributes-property-dao.md">в свойстве</a></strong> Атрибуты.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Relation

## <a name="remarks"></a>Примечания

Объект **Relation** предоставляет в движок базы данных Microsoft Access сведения о связи между полями в двух объектах **[TableDef](tabledef-object-dao.md)** или **[QueryDef.](querydef-object-dao.md)** Вы можете реализовать целостность ссылок с помощью свойства **Attributes.**

Если при использовании метода **CreateRelation** вы опустить одну или несколько необязательных частей, вы можете использовать соответствующее заявление о назначении для настройки или сброса соответствующего свойства перед тем, как примять новый объект к коллекции. После придатки объекта вы не сможете изменить его параметры свойств. См. разделы для отдельных свойств для получения дополнительных данных.

Прежде чем использовать метод **[Append](fields-append-method-dao.md)** на **объекте Relation,** необходимо примедить соответствующие объекты **[Field](field-object-dao.md)** для определения таблиц основных и внешних ключевых отношений.

Если имя относится к объекту, который уже входит в коллекцию,  или если имена объектов **Field,** предоставленные в подведомственных полях, являются недействительными, при использовании метода **Приложения** возникает ошибка времени запуска.

Нельзя установить или сохранить связь между реплицированной таблицей и локальной таблицей.

Чтобы удалить объект **Relation** из коллекции **[Relations,](relations-collection-dao.md)** используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.

## <a name="example"></a>Пример

В этом примере метод **CreateRelation** используется для создания связи между **TableDef** сотрудников и новым **TableDef** под названием Departments.  В этом примере также  показано, как  создание нового отношения также создает все необходимые индексы в иностранной таблице (индекс DepartmentsEmployees в таблице Employees).

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
