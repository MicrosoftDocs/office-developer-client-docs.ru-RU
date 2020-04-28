---
title: Пример использования свойств ActualSize и DefinedSize (VB)
TOCTitle: ActualSize and DefinedSize properties example (VB)
ms:assetid: fc268c63-c4b3-f633-1efb-aaf88354efd4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250291(v=office.15)
ms:contentKeyID: 48548884
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a629ac6305cab7289ea2d931f5a87c399bbe31b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281910"
---
# <a name="actualsize-and-definedsize-properties-example-vb"></a><span data-ttu-id="a7534-102">Пример использования свойств ActualSize и DefinedSize (VB)</span><span class="sxs-lookup"><span data-stu-id="a7534-102">ActualSize and DefinedSize properties example (VB)</span></span>


<span data-ttu-id="a7534-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7534-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a7534-104">В этом примере используются свойства [ActualSize](actualsize-property-ado.md) и [DefinedSize](definedsize-property-ado.md) для отображения определенного размера и фактического размера поля.</span><span class="sxs-lookup"><span data-stu-id="a7534-104">This example uses the [ActualSize](actualsize-property-ado.md) and [DefinedSize](definedsize-property-ado.md) properties to display the defined size and actual size of a field.</span></span>

```vb 
 
'BeginActualSizeVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstStores As ADODB.Recordset 
 Dim SQLStores As String 
 Dim strCnxn As String 
 'record variables 
 Dim strMessage As String 
 
 ' Open a recordset for the Stores table 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 Set rstStores = New ADODB.Recordset 
 
 SQLStores = "Suppliers" 
 rstStores.Open SQLStores, strCnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines of code are identical as the default values for 
 'CursorType and LockType arguments match those indicated 
 
 ' Loop through the recordset displaying the contents 
 ' of the store_name field, the field's defined size, 
 ' and its actual size. 
 rstStores.MoveFirst 
 
 Do Until rstStores.EOF 
 strMessage = "Company name: " & rstStores!CompanyName & _ 
 vbCrLf & "Defined size: " & _ 
 rstStores!CompanyName.DefinedSize & _ 
 vbCrLf & "Actual size: " & _ 
 rstStores!CompanyName.ActualSize & vbCrLf 
 
 MsgBox strMessage, vbOKCancel, "ADO ActualSize Property (Visual Basic)" 
 rstStores.MoveNext 
 Loop 
 
 ' clean up 
 rstStores.Close 
 Set rstStores = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstStores Is Nothing Then 
 If rstStores.State = adStateOpen Then rstStores.Close 
 End If 
 Set rstStores = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndActualSizeVB 
```

