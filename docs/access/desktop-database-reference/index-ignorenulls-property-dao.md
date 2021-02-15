---
title: Свойство Index.IgnoreNulls (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6c306f76e34e24abb5065c627d9325b48c3acead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291805"
---
# <a name="indexignorenulls-property-dao"></a>Свойство Index.IgnoreNulls (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, имеют ли записи с значениями NULL в полях индекса записи индекса (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* IgnoreNulls

*выражение* Переменная, представляюная объект **Index.**

## <a name="remarks"></a>Заметки

Это свойство доступно для чтения и записи для нового объекта **[Index,](index-object-dao.md)** еще не приданного коллекции, и доступно только для чтения для существующего объекта **Index** в коллекции **[Indexes.](indexes-collection-dao.md)**

Чтобы ускорить процесс поиска записей, можно определить индекс для поля. Если вы разрешаете **null-записи** в индексном поле и ожидаете, что многие записи будут иметь **null,** вы можете установить для свойства  **IgnoreNulls** для объекта **Index** true, чтобы уменьшить объем места в хранилище, который используется индексом.

Параметры **свойства IgnoreNulls** и **[Required](field-required-property-dao.md)** property вместе определяют, есть ли запись с значением индекса **null** записью индекса.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если ignoreNulls</p></th>
<th><p>Обязательное —</p></th>
<th><p>Then</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Верно</p></td>
<td><p>Неверно</p></td>
<td><p>В поле индекса допускается значение null; запись индекса не добавлена.</p></td>
</tr>
<tr class="even">
<td><p>Неверно</p></td>
<td><p>Неверно</p></td>
<td><p>В поле индекса допускается значение null; Добавлена запись индекса.</p></td>
</tr>
<tr class="odd">
<td><p>True или False</p></td>
<td><p>Верно</p></td>
<td><p>Значение null не допускается в поле индекса; запись индекса не добавлена.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Пример

В этом примере свойству **IgnoreNulls** нового индекса устанавливается значение **True** или **False**  на основе ввода пользователем, а затем демонстрируется влияние на набор записей с записью, поле ключа которой содержит значение **Null.** 

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
