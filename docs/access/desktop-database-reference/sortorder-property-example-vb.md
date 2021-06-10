---
title: Пример использования свойства SortOrder (VB)
TOCTitle: SortOrder property example (VB)
ms:assetid: 97937644-e3ef-06dc-d8ba-55ecaf7ac1ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249675(v=office.15)
ms:contentKeyID: 48546472
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58bde31a3386e3c129933d02e6464de5bc18fd68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308626"
---
# <a name="sortorder-property-example-vb"></a><span data-ttu-id="ab014-102">Пример использования свойства SortOrder (VB)</span><span class="sxs-lookup"><span data-stu-id="ab014-102">SortOrder property example (VB)</span></span>

<span data-ttu-id="ab014-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab014-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab014-104">В этом примере показано свойство [SortOrder](sortorder-property-adox.md) [столбца,](column-object-adox.md) который был придан коллекции [Столбцы](columns-collection-adox.md) [индекса.](index-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="ab014-104">This example demonstrates the [SortOrder](sortorder-property-adox.md) property of a [Column](column-object-adox.md) that has been appended to the [Columns](columns-collection-adox.md) collection of an [Index](index-object-adox.md).</span></span> <span data-ttu-id="ab014-105">Код привносим восходящий индекс в столбец Страна в таблице **Employees,** а затем отображает записи.</span><span class="sxs-lookup"><span data-stu-id="ab014-105">The code appends an ascending index to the Country column in the **Employees** table, then displays the records.</span></span> <span data-ttu-id="ab014-106">Затем код придает убывающий индекс в столбец Страна в таблице **Employees** и снова отображает записи.</span><span class="sxs-lookup"><span data-stu-id="ab014-106">Then the code appends a descending index to the Country column in the **Employees** table and displays the records again.</span></span> <span data-ttu-id="ab014-107">Показана разница между восходящими и нисходящими индексами.</span><span class="sxs-lookup"><span data-stu-id="ab014-107">The difference between ascending and descending indexes is shown.</span></span>


```vb 
 
' BeginSortOrderVB 
Sub Main() 
 On Error GoTo SortOrderXError 
 
 Dim cnn As New ADODB.Connection 
 Dim catNorthwind As New ADOX.Catalog 
 Dim idxAscending As New ADOX.Index 
 Dim idxDescending As New ADOX.Index 
 Dim rstEmployees As New ADODB.Recordset 
 
 ' Connect the catalog. 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set catNorthwind.ActiveConnection = cnn 
 
 ' Append Country column to new index 
 idxAscending.Columns.Append "Country" 
 idxAscending.Columns("Country").SortOrder = adSortAscending 
 idxAscending.Name = "Ascending" 
 idxAscending.IndexNulls = adIndexNullsAllow 
 
 'Append new index to Employees table 
 catNorthwind.Tables("Employees").Indexes.Append idxAscending 
 
 rstEmployees.Index = idxAscending.Name 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
 adLockOptimistic, adCmdTableDirect 
 
 With rstEmployees 
 .MoveFirst 
 Debug.Print "Index = " & .Index 
 Debug.Print " Country - Name" 
 
 ' Enumerate the Recordset. The value of the 
 ' IndexNulls property will determine if the newly 
 ' added record appears in the output. 
 Do While Not .EOF 
 Debug.Print " " & !Country & " - " & _ 
 !FirstName & " " & !LastName 
 .MoveNext 
 Loop 
 
 .Close 
 End With 
 
 ' Append Country column to new index 
 idxDescending.Columns.Append "Country" 
 idxDescending.Columns("Country").SortOrder = adSortDescending 
 idxDescending.Name = "Descending" 
 idxDescending.IndexNulls = adIndexNullsAllow 
 
 'Append descending index to Employees table 
 catNorthwind.Tables("Employees").Indexes.Append idxDescending 
 
 rstEmployees.Index = idxDescending.Name 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
 adLockOptimistic, adCmdTableDirect 
 
 With rstEmployees 
 .MoveFirst 
 Debug.Print "Index = " & .Index 
 Debug.Print " Country - Name" 
 
 ' Enumerate the Recordset. The value of the 
 ' IndexNulls property will determine if the newly 
 ' added record appears in the output. 
 Do While Not .EOF 
 Debug.Print " " & !Country & " - " & _ 
 !FirstName & " " & !LastName 
 .MoveNext 
 Loop 
 
 .Close 
 End With 
 
 ' Delete new Indexes because this is a demonstration. 
 catNorthwind.Tables("Employees").Indexes.Delete idxAscending.Name 
 catNorthwind.Tables("Employees").Indexes.Delete idxDescending.Name 
 
 'Clean up 
 cnn.Close 
 Set catNorthwind = Nothing 
 Set idxAscending = Nothing 
 Set idxDescending = Nothing 
 Set rstEmployees = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
SortOrderXError: 
 
 Set catNorthwind = Nothing 
 Set idxAscending = Nothing 
 Set idxDescending = Nothing 
 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndSortOrderVB 
```

