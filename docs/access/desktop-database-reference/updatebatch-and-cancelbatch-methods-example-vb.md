---
title: Пример использования методов UpdateBatch и CancelBatch (VB)
TOCTitle: UpdateBatch and CancelBatch methods example (VB)
ms:assetid: 7efb80a1-3ec8-0747-5562-6a6c372b949b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249536(v=office.15)
ms:contentKeyID: 48545893
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e74e5bb72914be57268cc30dfd94874b08040b88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313603"
---
# <a name="updatebatch-and-cancelbatch-methods-example-vb"></a><span data-ttu-id="3d6c4-102">Пример использования методов UpdateBatch и CancelBatch (VB)</span><span class="sxs-lookup"><span data-stu-id="3d6c4-102">UpdateBatch and CancelBatch methods example (VB)</span></span>


<span data-ttu-id="3d6c4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d6c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d6c4-104">В этом примере демонстрируется метод [UpdateBatch](updatebatch-method-ado.md) в сочетании с [методом CancelBatch.](cancelbatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3d6c4-104">This example demonstrates the [UpdateBatch](updatebatch-method-ado.md) method in conjunction with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

```vb 
 
'BeginUpdateBatchVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 'connection and recordset variables 
 Dim rstTitles As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 'record variables 
 Dim strTitle As String 
 Dim strMessage As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset for batch uodate 
 Set rstTitles = New ADODB.Recordset 
 strSQLTitles = "titles" 
 rstTitles.Open strSQLTitles, Cnxn, adOpenKeyset, adLockBatchOptimistic, adCmdTable 
 
 rstTitles.MoveFirst 
 ' Loop through recordset and ask user if she wants 
 ' to change the type for a specified title. 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "psychology" Then 
 strTitle = rstTitles!Title 
 strMessage = "Title: " & strTitle & vbCr & _ 
 "Change type to self help?" 
 
 If MsgBox(strMessage, vbYesNo) = vbYes Then 
 rstTitles!Type = "self_help" 
 End If 
 End If 
 
 rstTitles.MoveNext 
 Loop 
 
 ' Ask the user if she wants to commit to all the 
 ' changes made above. 
 If MsgBox("Save all changes?", vbYesNo) = vbYes Then 
 rstTitles.UpdateBatch 
 Else 
 rstTitles.CancelBatch 
 End If 
 
 ' Print current data in recordset. 
 rstTitles.Requery 
 rstTitles.MoveFirst 
 Do While Not rstTitles.EOF 
 Debug.Print rstTitles!Title & " - " & rstTitles!Type 
 rstTitles.MoveNext 
 Loop 
 
 ' Restore original values because this is a demonstration. 
 rstTitles.MoveFirst 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "self_help" Then 
 rstTitles!Type = "psychology" 
 End If 
 rstTitles.MoveNext 
 Loop 
 rstTitles.UpdateBatch 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.Close 
 Set rstTitles = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstTitles Is Nothing Then 
 If rstTitles.State = adStateOpen Then rstTitles.Close 
 End If 
 Set rstTitles = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndUpdateBatchVB 
```

