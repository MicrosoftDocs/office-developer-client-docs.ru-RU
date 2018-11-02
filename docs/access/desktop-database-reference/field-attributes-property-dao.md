---
title: Свойство Field.Attributes (DAO)
TOCTitle: Attributes Property
ms:assetid: 8e6f6afb-1a89-7315-c129-cf7ff19e0ca9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197380(v=office.15)
ms:contentKeyID: 48546287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f57c35b01e17f3544428cde0ca7b8d85daa3d0c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928413"
---
# <a name="fieldattributes-property-dao"></a>Свойство Field.Attributes (DAO)


**Применимо к**: Access 2013, Office 2013


Задает или возвращает значение, указывающее, один или несколько характеристик объекта **[поля](field-object-dao.md)** . Чтение и запись **времени**.

## <a name="syntax"></a>Синтаксис

*выражение* . Атрибуты

*выражение* Переменная, которая представляет собой объект- **поля** .

## <a name="remarks"></a>Примечания

Значение указывает характеристики поля, представленного объектом **поля** и может быть комбинацией этих констант.

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
<td><p>Значение поля для добавления новых записей автоматически увеличивается уникальный длинное целое число, которое нельзя изменить (в рабочую область Microsoft Access поддерживается только для таблиц базы данных ядра базы данных Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDescending</strong></p></td>
<td><p>Поле по убыванию (от я до А или 100 до 0); Этот параметр применяется только к объекта <strong>поля</strong> в коллекцию <strong>полей</strong> объекта <strong>индекса</strong> . Если опустить этой константы поле сортироваться в восходящем (A-Z или 0 до 100) порядке. Это значение по умолчанию для <strong>индексирования</strong> и <strong>TableDef</strong> полей (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFixedField</strong></p></td>
<td><p>Размер поля имеет фиксированную (по умолчанию для числовых полей).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbHyperlinkField</strong></p></td>
<td><p>Поле содержит сведения о гиперссылках (только для полей Memo).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSystemField</strong></p></td>
<td><p>В поле хранится репликации сведения о репликах; не удается удалить этот тип поля (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbUpdatableField</strong></p></td>
<td><p>Можно изменить значение поля.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVariableField</strong></p></td>
<td><p>Размер поля — переменная (только для текстовых полей).</p></td>
</tr>
</tbody>
</table>


Для объекта еще не добавляется в конец коллекции это свойство соответствует чтения и записи. Для объекта **поля** присоединенных доступности свойство **Attributes** зависит от объекта, который содержит коллекцию **полей** .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если принадлежит объект поля</p></th>
<th><p>Атрибуты — это</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>индекса</strong></p></td>
<td><p>Чтение и запись, пока не используется в качестве объекта <strong>TableDef</strong> , добавляемый в объект <strong>индекса</strong> для объекта <strong>базы данных</strong> ; Выберите свойство доступно только для чтения.</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>набора записей</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Отношения</strong> объектов</p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>TableDef</strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
</tbody>
</table>


Если задано несколько атрибутов, их можно объединить суммируются соответствующие константы. Недопустимые значения, пропускаются без создания ошибку.

## <a name="example"></a>Пример

В этом примере отображаются свойства **атрибуты** для **полей**, **связь**и **TableDef** объектов базы данных Northwind.

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

