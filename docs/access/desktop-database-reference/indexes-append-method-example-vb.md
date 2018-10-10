---
title: Indexes Append Method Example (VB)
TOCTitle: Indexes Append Method Example (VB)
ms:assetid: 71b18a5b-d000-5184-afac-c5d26b7f17e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249454(v=office.15)
ms:contentKeyID: 48545591
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffe5f156fba719cec07a9aec74a1c6639fe4a900
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480542"
---
# <a name="indexes-append-method-example-vb"></a><span data-ttu-id="7e842-102">Indexes Append Method Example (VB)</span><span class="sxs-lookup"><span data-stu-id="7e842-102">Indexes Append Method Example (VB)</span></span>


<span data-ttu-id="7e842-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e842-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7e842-104">Следующий код демонстрирует для создания нового индекса.</span><span class="sxs-lookup"><span data-stu-id="7e842-104">The following code demonstrates how to create a new index.</span></span> <span data-ttu-id="7e842-105">Индекс находится на два столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="7e842-105">The index is on two columns in the table.</span></span>

```vb 
 
' BeginCreateIndexVB 
Sub Main() 
 On Error GoTo CreateIndexError 
 
 Dim tbl As New Table 
 Dim idx As New ADOX.Index 
 Dim cat As New ADOX.Catalog 
 
 'Open the catalog. 
 ' Open the Catalog. 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Define the table and append it to the catalog 
 tbl.Name = "MyTable" 
 tbl.Columns.Append "Column1", adInteger 
 tbl.Columns.Append "Column2", adInteger 
 tbl.Columns.Append "Column3", adVarWChar, 50 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyTable' is added." 
 
 ' Define a multi-column index 
 idx.Name = "multicolidx" 
 idx.Columns.Append "Column1" 
 idx.Columns.Append "Column2" 
 
 ' Append the index to the table 
 tbl.Indexes.Append idx 
 Debug.Print "The index is appended to table 'MyTable'." 
 
 'Delete the table as this is a demonstration 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyTable' is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set idx = Nothing 
 Exit Sub 
 
CreateIndexError: 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set idx = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndCreateIndexVB 
```

