---
<span data-ttu-id="74020-101"><<<<<<< Название HEAD: IsolationLevel и TOCTitle пример свойств Mode (VB): IsolationLevel и пример свойств Mode (VB) === название: пример свойства IsolationLevel и режиме (VB) TOCTitle: IsolationLevel и режим Пример: свойства (VB)</span><span class="sxs-lookup"><span data-stu-id="74020-101"><<<<<<< HEAD title: IsolationLevel and Mode Properties Example (VB) TOCTitle: IsolationLevel and Mode Properties Example (VB) ======= title: IsolationLevel and Mode properties example (VB) TOCTitle: IsolationLevel and Mode properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="74020-102">главные ms:assetid: ac3ec2e7-199c-723c-ff3e-2aaf3e10aa94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249800(v=office.15) ms:contentKeyID: 48546999 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="74020-102">master ms:assetid: ac3ec2e7-199c-723c-ff3e-2aaf3e10aa94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249800(v=office.15) ms:contentKeyID: 48546999 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="74020-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="74020-103"><<<<<<< HEAD</span></span>
# <a name="isolationlevel-and-mode-properties-example-vb"></a><span data-ttu-id="74020-104">IsolationLevel and Mode Properties Example (VB)</span><span class="sxs-lookup"><span data-stu-id="74020-104">IsolationLevel and Mode Properties Example (VB)</span></span>
=======
# <a name="isolationlevel-and-mode-properties-example-vb"></a><span data-ttu-id="74020-105">Пример свойства IsolationLevel и режиме (VB)</span><span class="sxs-lookup"><span data-stu-id="74020-105">IsolationLevel and Mode properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="74020-106">master</span><span class="sxs-lookup"><span data-stu-id="74020-106">master</span></span>


<span data-ttu-id="74020-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="74020-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="74020-108">В этом примере используется свойство [Mode](mode-property-ado.md) открыть исключительных подключение и свойство [IsolationLevel](isolationlevel-property-ado.md) для открытия транзакций, которая проводится по отдельности других операций.</span><span class="sxs-lookup"><span data-stu-id="74020-108">This example uses the [Mode](mode-property-ado.md) property to open an exclusive connection, and the [IsolationLevel](isolationlevel-property-ado.md) property to open a transaction that is conducted in isolation of other transactions.</span></span>

```vb 
 
'BeginIsolationLevelVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstTitles As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Mode = adModeShareExclusive 
 Cnxn.IsolationLevel = adXactIsolated 
 Cnxn.Open strCnxn 
 
 ' open Titles table 
 Set rstTitles = New ADODB.Recordset 
 strSQLTitles = "titles" 
 rstTitles.Open strSQLTitles, Cnxn, adOpenDynamic, adLockPessimistic, adCmdTable 
 
 Cnxn.BeginTrans 
 
 ' Display connection mode 
 If Cnxn.Mode = adModeShareExclusive Then 
 MsgBox "Connection mode is exclusive." 
 Else 
 MsgBox "Connection mode is not exclusive." 
 End If 
 
 ' Display isolation level 
 If Cnxn.IsolationLevel = adXactIsolated Then 
 MsgBox "Transaction is isolated." 
 Else 
 MsgBox "Transaction is not isolated." 
 End If 
 
 ' Change the type of psychology titles 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "psychology" Then 
 rstTitles!Type = "self_help" 
 rstTitles.Update 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' Print current data in recordset 
 rstTitles.Requery 
 Do While Not rstTitles.EOF 
 Debug.Print rstTitles!Title & " - " & rstTitles!Type 
 rstTitles.MoveNext 
 Loop 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.RollbackTrans 
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
 If Cnxn.State = adStateOpen Then 
 Cnxn.RollbackTrans 
 Cnxn.Close 
 End If 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndIsolationLevelVB 
```

