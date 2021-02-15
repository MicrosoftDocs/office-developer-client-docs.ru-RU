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

Создает новый объект **[Relation](relation-object-dao.md)** (только для рабочих пространств Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражение .* CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)

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
<td><p>Вариант <strong></strong> <strong>(подтип строки),</strong> который уникальным образом именует новый объект <strong>Relation.</strong> Сведения о <strong><a href="connection-name-property-dao.md">допустимом</a></strong> имени relation см. в <strong>свойстве Name.</strong></p></td>
</tr>
<tr class="even">
<td><p><em>Table</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Вариант <strong></strong> <strong>(подтип строки),</strong> который именует основную таблицу в связи. Если таблица не существует перед приложением объекта <strong>Relation,</strong> возникает ошибка во время запуска.</p></td>
</tr>
<tr class="odd">
<td><p><em>ForeignTable</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Вариант <strong></strong> <strong>(строка</strong> подтипа), который именует внешние таблицы в связи. Если таблица не существует перед приложением объекта <strong>Relation,</strong> возникает ошибка во время запуска.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, которые содержат сведения о типе связи. Подробные <strong><a href="field-attributes-property-dao.md">сведения см. в свойстве Attributes.</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Relation

## <a name="remarks"></a>Заметки

Объект **Relation** предоставляет механизму базы данных Microsoft Access сведения о связи между полями в двух **[объектах TableDef](tabledef-object-dao.md)** **[или QueryDef.](querydef-object-dao.md)** Вы можете реализовать целостность ссылок с помощью свойства **Attributes.**

Если при использовании метода **CreateRelation** опустить одну или несколько необязательных частей, можно использовать соответствующий отчет о назначении, чтобы установить или сбросить соответствующее свойство, прежде чем приместь новый объект в коллекцию. После того как вы примесь к объекту, вы не сможете изменить параметры его свойства. См. разделы для отдельных свойств для получения дополнительных данных.

Прежде чем использовать метод **[Append](fields-append-method-dao.md)** для объекта **Relation,** необходимо приложение соответствующих объектов **[Field,](field-object-dao.md)** чтобы определить таблицы отношений первичного и внешнего ключей.

Если имя ссылается на объект, который уже является членом коллекции, или если имена объектов **Field,** предоставленные в подчиненной коллекции **Fields,** недопустимы, при использовании метода **Append** возникает ошибка во время работы.

Установить или поддерживать связь между реплицируемыми таблицами и локальной таблицей нельзя.

Чтобы удалить объект **Relation** из коллекции **[Relations,](relations-collection-dao.md)** используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.

## <a name="example"></a>Пример

В этом примере метод **CreateRelation** используется для создания отношения между **TableDef** Employees и новым **TableDef** под названием Departments.  В этом примере также  показано, как  при создании нового отношения также создаются все необходимые индексы во внешней таблице (индекс DepartmentsEmployees в таблице Employees).

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
