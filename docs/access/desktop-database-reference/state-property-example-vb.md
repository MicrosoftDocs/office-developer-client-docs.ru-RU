---
title: Пример использования свойства State (VB)
TOCTitle: State property example (VB)
ms:assetid: e5a9abc6-9be7-5b70-a2da-9b678b3a8421
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250166(v=office.15)
ms:contentKeyID: 48548366
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fee1be7c599dbab649652331c958978916d3ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306379"
---
# <a name="state-property-example-vb"></a>Пример использования свойства State (VB)


**Область применения**: Access 2013, Office 2013

В этом примере [свойство state](state-property-ado.md) отображает сообщение при открытии асинхронных подключений и выполнении асинхронных команд.

```vb 
 
'BeginStateVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn1 As ADODB.Connection 
 Dim Cnxn2 As ADODB.Connection 
 Dim cmdChange As ADODB.Command 
 Dim cmdRestore As ADODB.Command 
 Dim strCnxn As String 
 Dim strSQL As String 
 
 ' Open two asynchronous connections, displaying 
 ' a message while connecting 
 Set Cnxn1 = New ADODB.Connection 
 Set Cnxn2 = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 Cnxn1.Open strCnxn, , , adAsyncConnect 
 Do Until Cnxn1.State <> adStateConnecting 
 Debug.Print "Opening first connection...." 
 Loop 
 
 Cnxn2.Open strCnxn, , , adAsyncConnect 
 Do Until Cnxn2.State <> adStateConnecting 
 Debug.Print "Opening second connection...." 
 Loop 
 
 ' Create two command objects 
 Set cmdChange = New ADODB.Command 
 cmdChange.ActiveConnection = Cnxn1 
 strSQL = "UPDATE Titles SET type = 'self_help' WHERE type = 'psychology'" 
 cmdChange.CommandText = strSQL 
 
 Set cmdRestore = New ADODB.Command 
 cmdRestore.ActiveConnection = Cnxn2 
 strSQL = "UPDATE Titles SET type = 'psychology' WHERE type = 'self_help'" 
 cmdRestore.CommandText = strSQL 
 
 ' Executing the commands, displaying a message 
 ' while they are executing 
 cmdChange.Execute , , adAsyncExecute 
 Do Until cmdChange.State <> adStateExecuting 
 Debug.Print "Change command executing...." 
 Loop 
 
 cmdRestore.Execute , , adAsyncExecute 
 Do Until cmdRestore.State <> adStateExecuting 
 Debug.Print "Restore command executing...." 
 Loop 
 
 ' clean up 
 Cnxn1.Close 
 Cnxn2.Close 
 Set Cnxn1 = Nothing 
 Set Cnxn2 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn1 Is Nothing Then 
 If Cnxn1.State = adStateOpen Then Cnxn1.Close 
 End If 
 Set Cnxn1 = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndStateVB 
```

