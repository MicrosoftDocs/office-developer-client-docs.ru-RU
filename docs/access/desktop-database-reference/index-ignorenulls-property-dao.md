---
title: Index.IgnoreNulls Property (DAO)
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
ms.openlocfilehash: b6c190b7a61e26ff6e4abedc1a19bde26a1de426
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481631"
---
# <a name="indexignorenulls-property-dao"></a>Index.IgnoreNulls Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Задает или возвращает значение, указывающее, имеют ли записи, для которых значения Null в полях индекса записи индекса (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . IgnoreNulls

*выражение* Переменная, которая представляет объект **индекса** .

## <a name="remarks"></a>Замечания

Это свойство является чтение и запись для нового объекта **[индекс](index-object-dao.md)** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **индексу** в коллекции **[индексов](indexes-collection-dao.md)** .

Чтобы ускорить процесс поиска записей, можно определить индекс для поля. Если разрешить **значение null,** записей в индексированных полей и рассчитывают многие из записей должен иметь **значение null**, можно задать свойству **IgnoreNulls** **индекс** объекта значение **True** для сокращения объема дискового пространства, который использует индекс.

Настройка свойства **IgnoreNulls** и настройки свойства **[необходимые](field-required-property-dao.md)** вместе определить, имеет ли запись с **нулевое** значение индекса элемента.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Если IgnoreNulls</p></th>
<th><p>Который требуется</p></th>
<th><p>То</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Истина</p></td>
<td><p>Ложь</p></td>
<td><p>Значение null разрешено в поле индекса; не добавлена запись индекса.</p></td>
</tr>
<tr class="even">
<td><p>Ложь</p></td>
<td><p>Ложь</p></td>
<td><p>Значение null разрешено в поле индекса; добавлена запись индекса.</p></td>
</tr>
<tr class="odd">
<td><p>True (Истина) или False (Ложь)</p></td>
<td><p>True</p></td>
<td><p>Нулевое значение не является допустимым в поле индекса; не добавлена запись индекса.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Пример

В этом примере присваивает свойству **IgnoreNulls** нового **индекса** значение **True** или **False** на основе ввода пользователя, а затем влияние на **набора записей** с записью, чьи ключевое поле содержит значение **Null** .

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
