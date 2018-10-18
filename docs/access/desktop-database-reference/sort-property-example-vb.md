---
<span data-ttu-id="b4c7c-101"><<<<<<< Название HEAD: TOCTitle примере свойство сортировки (VB): пример свойства сортировки (VB) === название: пример свойства сортировки (VB) TOCTitle: пример свойства сортировки (VB)</span><span class="sxs-lookup"><span data-stu-id="b4c7c-101"><<<<<<< HEAD title: Sort Property Example (VB) TOCTitle: Sort Property Example (VB) ======= title: Sort property example (VB) TOCTitle: Sort property example (VB)</span></span>
>>>>>>> <span data-ttu-id="b4c7c-102">главные ms:assetid: 6f981e5e-7ee8-e1e7-bea9-7c2081400391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249440(v=office.15) ms:contentKeyID: 48545539 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="b4c7c-102">master ms:assetid: 6f981e5e-7ee8-e1e7-bea9-7c2081400391 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249440(v=office.15) ms:contentKeyID: 48545539 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b4c7c-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b4c7c-103"><<<<<<< HEAD</span></span>
# <a name="sort-property-example-vb"></a><span data-ttu-id="b4c7c-104">Sort Property Example (VB)</span><span class="sxs-lookup"><span data-stu-id="b4c7c-104">Sort Property Example (VB)</span></span>
=======
# <a name="sort-property-example-vb"></a><span data-ttu-id="b4c7c-105">Пример свойства сортировки (VB)</span><span class="sxs-lookup"><span data-stu-id="b4c7c-105">Sort property example (VB)</span></span>
>>>>>>> <span data-ttu-id="b4c7c-106">master</span><span class="sxs-lookup"><span data-stu-id="b4c7c-106">master</span></span>


<span data-ttu-id="b4c7c-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4c7c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b4c7c-108">В этом примере используется свойство [сортировки](sort-property-ado.md) объекта [набора записей](recordset-object-ado.md) для изменения порядка строк **набора записей** , полученных из таблицы ***авторов*** базы данных ***Pubs*** .</span><span class="sxs-lookup"><span data-stu-id="b4c7c-108">This example uses the [Recordset](recordset-object-ado.md) object's [Sort](sort-property-ado.md) property to reorder the rows of a **Recordset** derived from the ***Authors*** table of the ***Pubs*** database.</span></span> <span data-ttu-id="b4c7c-109">Дополнительный служебной процедуры печатает каждую строку.</span><span class="sxs-lookup"><span data-stu-id="b4c7c-109">A secondary utility routine prints each row.</span></span>

```vb 
 
'BeginSortVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim Cnxn As New ADODB.Connection 
 Dim rstAuthors As New ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 Dim strTitle As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open client-side recordset to enable sort method 
 Set rstAuthors = New ADODB.Recordset 
 rstAuthors.CursorLocation = adUseClient 
 strSQLAuthors = "SELECT * FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' sort the recordset last name ascending 
 rstAuthors.Sort = "au_lname ASC, au_fname ASC" 
 ' show output 
 Debug.Print "Last Name Ascending:" 
 Debug.Print "First Name Last Name" & vbCr 
 
 rstAuthors.MoveFirst 
 Do Until rstAuthors.EOF 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname 
 rstAuthors.MoveNext 
 Loop 
 
 ' sort the recordset last name descending 
 rstAuthors.Sort = "au_lname DESC, au_fname ASC" 
 ' show output 
 Debug.Print "Last Name Descending" 
 Debug.Print "First Name Last Name" & vbCr 
 
 Do Until rstAuthors.EOF 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname 
 rstAuthors.MoveNext 
 Loop 
 
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
'EndSortVB 
```

<span data-ttu-id="b4c7c-110">Это дополнительный служебной процедуры, печатает заданный заголовок и содержимое указанного **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="b4c7c-110">This is the secondary utility routine that prints the given title, and the contents of the specified **Recordset**.</span></span>

```vb 
 
Attribute VB_Name = "Sort" 
```

