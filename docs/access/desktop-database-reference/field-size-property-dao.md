---
title: Свойство Field.Size (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 16ce8a9e63c18ded2738035f23e9a1baeff4cc8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293018"
---
# <a name="fieldsize-property-dao"></a>Свойство Field.Size (DAO)


**Область применения**: Access 2013, Office 2013


Задает или возвращает значение, которое указывает максимальный размер объекта **[Field](field-object-dao.md)** (в bytes).

## <a name="syntax"></a>Синтаксис

*выражение .* Размер

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Для объекта, еще не примежаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство доступно для чтения и записи.

Для полей (кроме полей типа Memo), содержащих данные символов, свойство **Size** указывает максимальное число символов, которые могут содержаться в поле. Для числовых полей свойство **Size** указывает количество необходимых для хранения данных.

Использование свойства **Size** зависит от объекта, который содержит коллекцию **Fields,** к которой применится объект **Field,** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, к</p></th>
<th><p>Использование</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Индекс</strong></p></td>
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


При создании объекта **Field** с типом данных, не текстовым, параметр свойства **[Type](field-type-property-dao.md)** автоматически определяет параметр свойства **Size;** вам не нужно его устанавливать. Однако для **объекта Field** с текстовым типом данных можно установить значение **Size** в любое число до максимального размера текста (255 для баз данных Microsoft Access). Если размер не установлен, поле будет иметь тот же размер, что и в базе данных.

Для объектов Long Binary и  Memo **Field** размер всегда имеет 0. Используйте свойство **[FieldSize](field-fieldsize-property-dao.md)** объекта **Field,** чтобы определить размер данных в определенной записи. Максимальный размер поля Long Binary или Memo ограничивается только системным ресурсом или максимальным размером, допустимым базой данных.

## <a name="example"></a>Пример

В этом примере показано свойство **Size** путем нумерации имен и размеров объектов **Field** в таблице Employees.

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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
