---
title: Свойство Field2.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a655cfa5c6f0427b1a26a01f01e991564ab8e387
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292890"
---
# <a name="field2attributes-property-dao"></a>Свойство Field2.Attributes (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает значение, которое указывает одну или несколько характеристик объекта **Field2.** Для чтения и записи, **Long**.

## <a name="syntax"></a>Синтаксис

*expression* .Attributes

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

Значение указывает характеристики поля, представленного объектом **Field2,** и может быть сочетанием этих констант.

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
<td><p>Поле сортироваться в порядке убывка (от Z до A или от 100 до 0); Этот параметр применяется только к объекту <strong>Field2</strong> в коллекции <strong>Fields</strong> объекта <strong>Index.</strong> Если опустить эту константу, поле сортируется в порядке возрастания (от А до Я или от 0 до 100). Это значение по умолчанию для полей <strong>Index</strong> и <strong>TableDef</strong> (только для рабочих областей Microsoft Access).</p></td>
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
<td><p>Поле сохраняет сведения о репликации для реплик; вы не можете удалить этот тип поля (только для рабочего пространства Microsoft Access).</p></td>
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


Для объекта, который еще не добавлен в коллекцию, это свойство предназначено для чтения и записи. Для объекта **Field2,** примыкаемого к приложению, доступность свойства **Attributes** зависит от объекта, который содержит коллекцию **Полей.**

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

В этом примере отображается свойство **Атрибуты** для **объектов Field2,** **Relation** и **TableDef** в базе данных Northwind.

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
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

