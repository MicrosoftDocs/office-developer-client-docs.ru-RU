---
title: Пример использования свойства IndexNulls (VB)
TOCTitle: IndexNulls property example (VB)
ms:assetid: 69b5661c-931e-3a1c-d60e-96a0f93b9494
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249414(v=office.15)
ms:contentKeyID: 48545417
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 488e37f53218a7dabfa6248ea1da7630f82818a6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699690"
---
# <a name="indexnulls-property-example-vb"></a>Пример использования свойства IndexNulls (VB)

**Применимо к**: Access 2013, Office 2013

В этом примере демонстрируется свойство [IndexNulls](indexnulls-property-adox.md) [индекса](index-object-adox.md). Код создает новый индекс и задает значение **IndexNulls** на основе ввода пользователя (из поля со списком с именем List1). Затем **индекс** добавляется **сотрудников** [в таблице](table-object-adox.md) в [каталог](catalog-object-adox.md) *"Борей"* . Новый **индекс** применяется к [набору записей](recordset-object-ado.md) , основанного на таблице **Employees** и открывается **набора записей** . Новая запись добавляется к таблице **Employees** **нулевое** значение в индексированных полей. Отображение этой новой записи зависит от значения свойства **IndexNulls** .

```vb
    ' IndexNullsVB 
    Sub Main() 
     On Error GoTo IndexNullsXError 
     
     Dim cnn As New ADODB.Connection 
     Dim catNorthwind As New ADOX.Catalog 
     Dim idxNew As New ADOX.Index 
     Dim rstEmployees As New ADODB.Recordset 
     Dim varBookmark As Variant 
     
     ' Connect the catalog. 
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source='c:\Program Files\" & _ 
     "Microsoft Office\Office\Samples\Northwind.mdb';" 
     
     Set catNorthwind.ActiveConnection = cnn 
     
     ' Append Country column to new index 
     idxNew.Columns.Append "Country" 
     idxNew.Name = "NewIndex" 
     
     Dim Response 
     Response = MsgBox("Allow 'Null' index? Otherwise ignore 'Null' index.", vbYesNo) 
     '"Allow 'Null' index? Otherwise ignore 'Null' index." 
     ', vbYesNo + vbCritical + vbDefaultButton2,,,, 
     If Response = vbYes Then ' User chose Yes. 
     idxNew.IndexNulls = adIndexNullsAllow 
     Else ' User chose No. 
     idxNew.IndexNulls = adIndexNullsIgnore 
     End If 
     
     'Append new index to Employees table 
     catNorthwind.Tables("Employees").Indexes.Append idxNew 
     
     rstEmployees.Index = idxNew.Name 
     rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
     adLockOptimistic, adCmdTableDirect 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Bookmark the newly added record 
     varBookmark = .Bookmark 
     
     ' Use the new index to set the order of the records. 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IndexNulls = " & idxNew.IndexNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IndexNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = varBookmark 
     .Delete 
     
     .Close 
     End With 
     
     'Clean up 
     Set rstEmployees = Nothing 
     catNorthwind.Tables("Employees").Indexes.Delete idxNew.Name 
     cnn.Close 
     Set cnn = Nothing 
     Set catNorthwind = Nothing 
     Set idxNew = Nothing 
     Exit Sub 
     
    IndexNullsXError: 
     
     If Not rstEmployees Is Nothing Then 
     If rstEmployees.State = adStateOpen Then rstEmployees.Close 
     End If 
     Set rstEmployees = Nothing 
     
     ' Delete new Index because this is a demonstration. 
     If Not catNorthwind Is Nothing Then 
     catNorthwind.Tables("Employees").Indexes.Delete idxNew.Name 
     End If 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     Set catNorthwind = Nothing 
     Set idxNew = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
     
    End Sub 
    ' EndIndexNullsVB
```
