---
title: Метод Database. Креатерелатион (DAO)
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
# <a name="databasecreaterelation-method-dao"></a>Метод Database. Креатерелатион (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[relation](relation-object-dao.md)** (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*Expression* . Креатерелатион (***имя***, ***Таблица***, ***ForeignTable***, ***атрибуты***)

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (подтип<strong>String</strong> ), уникально названный новому объекту <strong>relation</strong> . Сведения о допустимых именах <strong>отношений</strong> приведены в свойстве <strong><a href="connection-name-property-dao.md">Name</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>Table</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (подтип<strong>String</strong> ), который называет основную таблицу в отношении. Если перед добавлением объекта <strong>relation</strong> таблица не существует, возникает ошибка времени выполнения.</p></td>
</tr>
<tr class="odd">
<td><p><em>ForeignTable</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (подтип<strong>String</strong> ), который называет внешнюю таблицу в отношении. Если перед добавлением объекта <strong>relation</strong> таблица не существует, возникает ошибка времени выполнения.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, содержащих сведения о типе связи. Дополнительные сведения <strong><a href="field-attributes-property-dao.md"></a></strong> см. в свойстве Attributes.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Relation

## <a name="remarks"></a>Замечания

Объект **relation** предоставляет сведения для ядра СУБД Microsoft Access относительно связи между полями в двух объектах **[tabledef](tabledef-object-dao.md)** или **[QueryDef](querydef-object-dao.md)** . Можно реализовать целостность ссылок с помощью свойства **Attributes** .

Если опустить одну или несколько дополнительных частей при использовании метода **креатерелатион** , можно использовать соответствующий оператор присваивания для задания или сброса соответствующего свойства перед добавлением нового объекта в коллекцию. После добавления объекта невозможно изменить параметры его свойств. См. разделы для отдельных свойств для получения дополнительных данных.

Прежде чем можно будет использовать метод **[append](fields-append-method-dao.md)** для объекта **relation** , необходимо добавить соответствующие объекты **[field](field-object-dao.md)** , чтобы определить первичные и внешние таблицы связи.

Если имя ссылается на объект, который уже является членом коллекции, или если имена объекта **поля** , указанные в коллекции подчиненных **полей** , являются недопустимыми, при использовании метода **append** возникает ошибка во время выполнения.

Невозможно установить или поддерживать связь между реплицированной таблицей и локальной таблицей.

Чтобы удалить объект **relation** из коллекции **[связей](relations-collection-dao.md)** , используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.

## <a name="example"></a>Пример

В этом примере используется метод **креатерелатион** для создания **отношения** между сотрудниками **tabledef** и новыми **tabledef** , называемыми отделами. В этом примере также показано, как создание нового **отношения** также приведет к созданию необходимых **индексов** во внешней таблице (индекс департментсемплойис в таблице Employees).

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
