---
title: Свойство Field.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 010c7a2aea777a93d1ced2d33d8743320dd05ada
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293156"
---
# <a name="fieldattributes-property-dao"></a>Свойство Field.Attributes (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает значение, которое определяет одну или несколько характеристик объекта **[Field](field-object-dao.md)**. Для чтения и записи, **Long**.

## <a name="syntax"></a>Синтаксис

*expression* .Attributes

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Комментарии

Значение определяет характеристики поля, представленного объектом **Field**, и может быть сочетанием данных констант.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbAutoIncrField</strong></p></td>
<td><p>Значение поля для новых записей автоматически увеличивается на уникальные длинное целочисленное значение, которое нельзя изменить (в рабочей области Microsoft Access, поддерживается только для таблиц базы данных ядра СУБД Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDescending</strong></p></td>
<td><p>Для поля выполняется сортировка по убыванию (от Я до А или 100 до 0); этот параметр применяется только для объекта <strong>Field</strong> в коллекции <strong>Fields</strong> объекта <strong>Index</strong>. Если опустить эту константу, поле сортируется в порядке возрастания (от А до Я или от 0 до 100). Это значение по умолчанию для полей <strong>Index</strong> и <strong>TableDef</strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>Размер поля закреплен (по умолчанию для числовых полей).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>Поле содержит сведения о гиперссылке (только для полей Memo).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>Поле сохраняет информацию о репликацию для реплик; вы не можете удалить этот тип поля (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>Можно изменить значение данного поля.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>Переменный размер поля (только для текстовых полей).</p></td>
</tr>
</tbody>
</table>


Для объекта, который еще не добавлен в коллекцию, это свойство предназначено для чтения и записи. Для добавленного объекта **Field** объект доступность свойства **Attributes** зависит от объекта, содержащего коллекцию **Fields**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если объект Field принадлежит к</p></th>
<th><p>тогда атрибуты будут</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>Index</strong></p></td>
<td><p>Чтение и запись до того момента, пока объект <strong>TableDef</strong>, который добавляется к объекту <strong>Index</strong>, добавляется к объекту <strong>Database</strong>; после чего свойство будет доступно только для чтения.</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>Recordset</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>Relation</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>


Если вы задаете несколько атрибутов, их можно объединить, суммируя соответствующие константы. Любые недопустимые значения игнорируются без сообщения об ошибке.

## <a name="example"></a>Пример

Этот пример отображает свойство **Attributes** для объектов **Field**, **Relation** и **TableDef** в базе данных Northwind.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

