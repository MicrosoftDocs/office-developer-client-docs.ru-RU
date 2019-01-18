---
title: Свойство Field2.Size (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f1467414729f4ea82bc2779eeb2bd162465b5ccd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699039"
---
# <a name="field2size-property-dao"></a>Свойство Field2.Size (DAO)


**Применимо к**: Access 2013, Office 2013


Задает или возвращает значение, которое указывает максимальный размер в байтах, **поле2** объекта.

## <a name="syntax"></a>Синтаксис

*выражение* . Размер

*выражение* Переменная, которая представляет собой объект- **поле2** .

## <a name="remarks"></a>Замечания

Для объекта еще не добавляется в конец коллекции **[полей](fields-collection-dao.md)** это свойство соответствует чтения и записи.

Для полей (кроме полей типа Memo), которые содержат символ данных свойство **Size** указывает максимальное число символов, которое может содержать поля. Для числовых полей свойство **Size** указывает число байтов хранилища являются обязательными.

Использование **свойства Size** зависит от объекта, который содержит коллекцию **полей** , к которому добавляется объект **поле2** , как показано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект, добавляемый в конец</p></th>
<th><p>Применение</p></th>
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


При создании объекта **поле2** с типом данных, отличный от текста, значение свойства **типа** автоматически определяет значение свойства **размера** ; его настройка не требуется. Для объекта **поле2** с типом данных Text тем не менее, можно задать **размер** любое целое число до текст максимальный размер (255 для базами данных, ядро базы данных Microsoft Access). Если размер не установлен, это поле будет размер базы данных позволяет.

Объектам-Long Binary и Memo **поле2** **размер** всегда имеет значение 0. Используйте свойство **основании итогового** объекта **поле2** порядок определения размера данных в конкретной записи. Максимальный размер поля Long Binary или Memo ограничивается только системных ресурсов или максимальный размер, который позволяет базы данных.

## <a name="example"></a>Пример

В этом примере демонстрируется свойство **размер** перечисление имена и размеры объектов **поле2** в таблице сотрудников.

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
