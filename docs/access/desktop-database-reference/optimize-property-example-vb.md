---
<span data-ttu-id="c4020-101"><<<<<<< HEAD заголовок: TOCTitle оптимизировать примере свойство (VB): оптимизировать примере свойство (VB) === заголовок: оптимизация пример свойства (VB) TOCTitle: оптимизировать пример свойства (VB)</span><span class="sxs-lookup"><span data-stu-id="c4020-101"><<<<<<< HEAD title: Optimize Property Example (VB) TOCTitle: Optimize Property Example (VB) ======= title: Optimize property example (VB) TOCTitle: Optimize property example (VB)</span></span>
>>>>>>> <span data-ttu-id="c4020-102">главные ms:assetid: f4576247-6057-c1fe-013d-74feaab33174 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250240(v=office.15) ms:contentKeyID: 48548686 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="c4020-102">master ms:assetid: f4576247-6057-c1fe-013d-74feaab33174 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250240(v=office.15) ms:contentKeyID: 48548686 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c4020-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="c4020-103"><<<<<<< HEAD</span></span>
# <a name="optimize-property-example-vb"></a><span data-ttu-id="c4020-104">Optimize Property Example (VB)</span><span class="sxs-lookup"><span data-stu-id="c4020-104">Optimize Property Example (VB)</span></span>
=======
# <a name="optimize-property-example-vb"></a><span data-ttu-id="c4020-105">Оптимизация пример свойства (VB)</span><span class="sxs-lookup"><span data-stu-id="c4020-105">Optimize property example (VB)</span></span>
>>>>>>> <span data-ttu-id="c4020-106">master</span><span class="sxs-lookup"><span data-stu-id="c4020-106">master</span></span>


<span data-ttu-id="c4020-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4020-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4020-108">В этом примере демонстрируется динамических свойство оптимизировать [поля](field-object-ado.md) объектов.</span><span class="sxs-lookup"><span data-stu-id="c4020-108">This example demonstrates the [Field](field-object-ado.md) objects dynamic Optimize property.</span></span> <span data-ttu-id="c4020-109">Поле ***zip*** таблицы ***авторов*** в базе данных ***Pubs*** не индексируются.</span><span class="sxs-lookup"><span data-stu-id="c4020-109">The ***zip*** field of the ***Authors*** table in the ***Pubs*** database is not indexed.</span></span> <span data-ttu-id="c4020-110">Свойства [оптимизировать](optimize-property-dynamic-ado.md) значение **True** в поле ***zip*** авторизует ADO для построения индекса, которая улучшает производительность метод [поиска](find-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c4020-110">Setting the [Optimize](optimize-property-dynamic-ado.md) property to **True** on the ***zip*** field authorizes ADO to build an index that improves the performance of the [Find](find-method-ado.md) method.</span></span>

```vb 
 
'BeginOptimizeVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 ' recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim rstAuthors As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' open recordset client-side to enable index creation 
 Set rstAuthors = New ADODB.Recordset 
 rstAuthors.CursorLocation = adUseClient 
 strSQLAuthors = "SELECT * FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 ' Create the index 
 rstAuthors!zip.Properties("Optimize") = True 
 ' Find Akiko Yokomoto 
 rstAuthors.Find "zip = '94595'" 
 
 ' show results 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname & " " & _ 
 rstAuthors!address & " " & rstAuthors!city & " " & rstAuthors!State 
 rstAuthors!zip.Properties("Optimize") = False 'Delete the index 
 
 ' clean up 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOptimizeVB 
```

