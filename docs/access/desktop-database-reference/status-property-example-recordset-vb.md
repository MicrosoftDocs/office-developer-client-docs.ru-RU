---
<span data-ttu-id="37821-101"><<<<<<< Название HEAD: пример свойства состояния (записей) (VB) TOCTitle: пример свойства состояния (записей) (VB) === название: пример свойства состояния (записей) (VB) TOCTitle: пример свойства состояния (записей) (VB)</span><span class="sxs-lookup"><span data-stu-id="37821-101"><<<<<<< HEAD title: Status Property Example (Recordset) (VB) TOCTitle: Status Property Example (Recordset) (VB) ======= title: Status property example (Recordset) (VB) TOCTitle: Status property example (Recordset) (VB)</span></span>
>>>>>>> <span data-ttu-id="37821-102">главные ms:assetid: 97ddd465-88ed-81dd-3714-1841f1c87611 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249677(v=office.15) ms:contentKeyID: 48546476 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="37821-102">master ms:assetid: 97ddd465-88ed-81dd-3714-1841f1c87611 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249677(v=office.15) ms:contentKeyID: 48546476 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="37821-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="37821-103"><<<<<<< HEAD</span></span>
# <a name="status-property-example-recordset-vb"></a><span data-ttu-id="37821-104">Status Property Example (Recordset) (VB)</span><span class="sxs-lookup"><span data-stu-id="37821-104">Status Property Example (Recordset) (VB)</span></span>
=======
# <a name="status-property-example-recordset-vb"></a><span data-ttu-id="37821-105">Пример свойства состояния (записей) (VB)</span><span class="sxs-lookup"><span data-stu-id="37821-105">Status property example (Recordset) (VB)</span></span>
>>>>>>> <span data-ttu-id="37821-106">master</span><span class="sxs-lookup"><span data-stu-id="37821-106">master</span></span>


<span data-ttu-id="37821-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37821-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37821-108">В этом примере используется свойство [состояние](status-property-ado-recordset.md) для отображения записи, которые были изменены в пакетной операции до пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="37821-108">This example uses the [Status](status-property-ado-recordset.md) property to display which records have been modified in a batch operation before a batch update has occurred.</span></span>

```vb 
 
'BeginStatusRecordsetVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 ' connection and recordset variables 
 Dim rstTitles As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset for batch update 
 Set rstTitles = New ADODB.Recordset 
 strSQLTitles = "Titles" 
 rstTitles.Open strSQLTitles, Cnxn, adOpenKeyset, adLockBatchOptimistic, adCmdTable 
 
 ' change the type of psychology titles 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "psychology" Then rstTitles!Type = "self_help" 
 rstTitles.MoveNext 
 Loop 
 
 ' display Title ID and status 
 rstTitles.MoveFirst 
 Do Until rstTitles.EOF 
 If rstTitles.Status = adRecModified Then 
 Debug.Print rstTitles!title_id & " - Modified" 
 Else 
 Debug.Print rstTitles!title_id 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.Close 
 Set rstTitles = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstTitles Is Nothing Then 
 If rstTitles.State = adStateOpen Then 
 ' Cancel the update because this is a demonstration 
 rstTitles.CancelBatch 
 rstTitles.Close 
 End If 
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
'EndStatusRecordsetVB 
```

