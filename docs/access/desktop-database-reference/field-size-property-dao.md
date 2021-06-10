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


Задает или возвращает значение, которое указывает максимальный размер в bytes объекта **[Field.](field-object-dao.md)**

## <a name="syntax"></a>Синтаксис

*выражения* . Размер

*выражение*: переменная, представляющая объект **Field**.

## <a name="remarks"></a>Примечания

Для объекта, еще не примыкаемого к коллекции **[Fields,](fields-collection-dao.md)** это свойство является чтением и написанием.

Для полей (кроме полей типа Memo), содержащих данные символов, свойство **Size** указывает максимальное количество символов, которые может содержать поле. Для числовых полей свойство **Size** указывает, сколько запасов хранилища требуется.

Использование свойства **Size** зависит от объекта, который содержит коллекцию **Полей,** к которой примыкает объект **Field,** как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, приданный</p></th>
<th><p>Usage</p></th>
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


При создании объекта **Field** с типом данных, не текстовым, параметр **[Type](field-type-property-dao.md)** свойство автоматически определяет параметр **Свойства Size;** вам не нужно его устанавливать. Однако для **объекта Field** с типом текстовых  данных можно установить размер любого набора до максимального размера текста (255 для баз данных Microsoft Access). Если размер не установлен, поле будет таким же большим, как позволяет база данных.

Для объектов Long Binary и Memo **Field** **размер** всегда устанавливается до 0. Для определения размера данных  в определенной записи используйте свойство **[FieldSize](field-fieldsize-property-dao.md)** объекта Field. Максимальный размер поля Long Binary или Memo ограничен только ресурсами системы или максимальным размером, который позволяет база данных.

## <a name="example"></a>Пример

В этом примере демонстрируется свойство **Size** путем переумерия имен и размеров объектов **Field** в таблице Employees.

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
