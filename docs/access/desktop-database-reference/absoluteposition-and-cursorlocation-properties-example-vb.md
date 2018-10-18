---
<span data-ttu-id="37144-101"><<<<<<< Название HEAD: AbsolutePosition и TOCTitle пример свойства CursorLocation (VB): ms:assetid AbsolutePosition и пример свойства CursorLocation (VB): 572c1a51-b7f4-5861-cfb9-960219e0a831 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249293(v=office.15) мс: contentKeyID: 48544966 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="37144-101"><<<<<<< HEAD title: AbsolutePosition and CursorLocation Properties Example (VB) TOCTitle: AbsolutePosition and CursorLocation Properties Example (VB) ms:assetid: 572c1a51-b7f4-5861-cfb9-960219e0a831 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249293(v=office.15) ms:contentKeyID: 48544966 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="absoluteposition-and-cursorlocation-properties-example-vb"></a><span data-ttu-id="37144-102">AbsolutePosition and CursorLocation Properties Example (VB)</span><span class="sxs-lookup"><span data-stu-id="37144-102">AbsolutePosition and CursorLocation Properties Example (VB)</span></span>
<span data-ttu-id="37144-103">=== Название: пример свойства AbsolutePosition и CursorLocation (VB) TOCTitle: AbsolutePosition и CursorLocation ms:assetid пример (VB) свойства: 572c1a51-b7f4-5861-cfb9-960219e0a831 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249293(v=office.15) ms:contentKeyID: 48544966 MS.Date: 10/17/2018 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="37144-103">======= title: AbsolutePosition and CursorLocation properties example (VB) TOCTitle: AbsolutePosition and CursorLocation properties example (VB) ms:assetid: 572c1a51-b7f4-5861-cfb9-960219e0a831 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249293(v=office.15) ms:contentKeyID: 48544966 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="absoluteposition-and-cursorlocation-properties-example-vb"></a><span data-ttu-id="37144-104">Пример свойства AbsolutePosition и CursorLocation (VB)</span><span class="sxs-lookup"><span data-stu-id="37144-104">AbsolutePosition and CursorLocation properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="37144-105">master</span><span class="sxs-lookup"><span data-stu-id="37144-105">master</span></span>


<span data-ttu-id="37144-106">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="37144-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="37144-107">В этом примере показано, как свойство [AbsolutePosition](absoluteposition-property-ado.md) можно отслеживать цикл, который перечисляет все записи из [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="37144-107">This example demonstrates how the [AbsolutePosition](absoluteposition-property-ado.md) property can track the progress of a loop that enumerates all the records of a [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="37144-108">Свойство [CursorLocation](cursorlocation-property-ado.md) используется для включения свойство **AbsolutePosition** , установив курсор на курсор клиента.</span><span class="sxs-lookup"><span data-stu-id="37144-108">It uses the [CursorLocation](cursorlocation-property-ado.md) property to enable the **AbsolutePosition** property by setting the cursor to a client cursor.</span></span>

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

