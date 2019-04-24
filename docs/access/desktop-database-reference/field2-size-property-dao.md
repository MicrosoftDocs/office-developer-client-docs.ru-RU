---
title: Свойство field2. size (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f1467414729f4ea82bc2779eeb2bd162465b5ccd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292687"
---
# <a name="field2size-property-dao"></a>Свойство field2. size (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает значение, которое указывает максимальный размер объекта **field2** в байтах.

## <a name="syntax"></a>Синтаксис

*Expression* . Размер

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Замечания

Для объекта, который еще не добавлен в коллекцию **[Fields](fields-collection-dao.md)** , это свойство доступно для чтения и записи.

Для полей (отличных от полей типа MEMO), содержащих символьные данные, свойство **size** указывает максимальное число знаков, которое может содержать поле. Для числовых полей свойство **size** указывает, сколько байтов хранения необходимо.

Использование свойства **size** зависит от объекта, содержащего коллекцию Fields, **** к которой добавляется объект **field2** , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, добавленный в</p></th>
<th><p>Использование</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>Не поддерживается</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Только для чтения</p></td>
</tr>
</tbody>
</table>


При создании объекта **field2** с типом данных, отличным от Text, параметр свойства **Type** автоматически определяет значение свойства **size** ; задавать его не нужно. Однако для объекта **field2** с типом данных Text можно задать любое целое число вплоть до максимального размера текста (255 для баз данных ядра СУБД Microsoft Access). **** Если размер не задан, размер поля будет максимально велик для базы данных.

Для больших двоичных объектов и полей MEMO **field2** **Размер** всегда равен 0. Используйте свойство **FieldSize** объекта **field2** , чтобы определить размер данных в определенной записи. Максимальный размер длинного двоичного поля или поля MEMO ограничен только системными ресурсами или максимальным размером, разрешенным в базе данных.

## <a name="example"></a>Пример

В этом примере показано свойство **size** , которое перечисляет имена и размеры объектов **field2** в таблице Employees.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
