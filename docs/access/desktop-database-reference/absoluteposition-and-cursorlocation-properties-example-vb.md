---
title: Пример использования свойств AbsolutePosition и CursorLocation (VB)
TOCTitle: AbsolutePosition and CursorLocation properties example (VB)
ms:assetid: 572c1a51-b7f4-5861-cfb9-960219e0a831
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249293(v=office.15)
ms:contentKeyID: 48544966
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a8a030a586edc715ac62580510f9cd200b21eb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282000"
---
# <a name="absoluteposition-and-cursorlocation-properties-example-vb"></a>Пример использования свойств AbsolutePosition и CursorLocation (VB)


**Область применения**: Access 2013, Office 2013

В этом примере показано, как свойство [AbsolutePosition](absoluteposition-property-ado.md) может отслеживать ход выполнения цикла, который нумерует все записи [объекта Recordset.](recordset-object-ado.md) Оно использует свойство [CursorLocation,](cursorlocation-property-ado.md) чтобы включить свойство **AbsolutePosition,** настроив курсор на клиентский курсор.

```vb 
 
'BeginAbsolutePositionVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQL As String 
 'record variables 
 Dim strMessage As String 
 
 'Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open Employee recordset with 
 ' Client-side cursor to enable AbsolutePosition property 
 Set rstEmployees = New ADODB.Recordset 
 strSQL = "employee" 
 rstEmployees.Open strSQL, strCnxn, adUseClient, adLockReadOnly, adCmdTable 
 
 ' Enumerate Recordset 
 Do While Not rstEmployees.EOF 
 ' Display current record information 
 strMessage = "Employee: " & rstEmployees!lname & vbCr & _ 
 "(record " & rstEmployees.AbsolutePosition & _ 
 " of " & rstEmployees.RecordCount & ")" 
 If MsgBox(strMessage, vbOKCancel) = vbCancel Then Exit Do 
 rstEmployees.MoveNext 
 Loop 
 
 ' clean up 
 rstEmployees.Close 
 Cnxn.Close 
 Set rstEmployees = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndAbsolutePositionVB 
```

