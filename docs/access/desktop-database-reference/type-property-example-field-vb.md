---
<span data-ttu-id="2fd91-101"><<<<<<< Название HEAD: пример свойства типа (поле) (VB) TOCTitle: пример свойства типа (поле) (VB) === название: пример свойства типа (поле) (VB) TOCTitle: пример свойства типа (поле) (VB)</span><span class="sxs-lookup"><span data-stu-id="2fd91-101"><<<<<<< HEAD title: Type Property Example (Field) (VB) TOCTitle: Type Property Example (Field) (VB) ======= title: Type property example (Field) (VB) TOCTitle: Type property example (Field) (VB)</span></span>
>>>>>>> <span data-ttu-id="2fd91-102">главные ms:assetid: ff9e26a8-898d-ec89-5093-69c66dbb05ba ms:mtpsurl: https://msdn.microsoft.com/library/JJ250314(v=office.15) ms:contentKeyID: 48548966 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2fd91-102">master ms:assetid: ff9e26a8-898d-ec89-5093-69c66dbb05ba ms:mtpsurl: https://msdn.microsoft.com/library/JJ250314(v=office.15) ms:contentKeyID: 48548966 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2fd91-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2fd91-103"><<<<<<< HEAD</span></span>
# <a name="type-property-example-field-vb"></a><span data-ttu-id="2fd91-104">Type Property Example (Field) (VB)</span><span class="sxs-lookup"><span data-stu-id="2fd91-104">Type Property Example (Field) (VB)</span></span>
=======
# <a name="type-property-example-field-vb"></a><span data-ttu-id="2fd91-105">Пример свойства типа (поле) (VB)</span><span class="sxs-lookup"><span data-stu-id="2fd91-105">Type property example (Field) (VB)</span></span>
>>>>>>> <span data-ttu-id="2fd91-106">master</span><span class="sxs-lookup"><span data-stu-id="2fd91-106">master</span></span>


<span data-ttu-id="2fd91-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fd91-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2fd91-108">В этом примере показано свойство [типа](type-property-ado.md) , отображая имя константы, соответствующее значение свойства [типа](type-property-ado.md) всех объектов [поля](field-object-ado.md) в таблице ***сотрудников*** .</span><span class="sxs-lookup"><span data-stu-id="2fd91-108">This example demonstrates the [Type](type-property-ado.md) property by displaying the name of the constant that corresponds to the value of the [Type](type-property-ado.md) property of all the [Field](field-object-ado.md) objects in the ***Employees*** table.</span></span> <span data-ttu-id="2fd91-109">Функция FieldType является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="2fd91-109">The FieldType function is required for this procedure to run.</span></span>

```vb 
 
'BeginTypeFieldVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstEmployees As ADODB.Recordset 
 Dim fld As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLEmployee As String 
 Dim FieldType As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employees table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployee = "employee" 
 rstEmployees.Open strSQLEmployee, Cnxn, , , adCmdTable 
 'rstEmployees.Open strSQLEmployee, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 ' the above two lines of code are identical 
 
 Debug.Print "Fields in Employees Table:" & vbCr 
 
 ' Enumerate Fields collection of Employees table 
 For Each fld In rstEmployees.Fields 
 ' translate field-type code to text 
 Select Case fld.Type 
 Case adChar 
 FieldType = "adChar" 
 Case adVarChar 
 FieldType = "adVarChar" 
 Case adSmallInt 
 FieldType = "adSmallInt" 
 Case adUnsignedTinyInt 
 FieldType = "adUnsignedTinyInt" 
 Case adDBTimeStamp 
 FieldType = "adDBTimeStamp" 
 End Select 
 ' show results 
 Debug.Print " Name: " & fld.Name & vbCr & _ 
 " Type: " & FieldType & vbCr 
 Next fld 
 
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
 
 Set fld = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndTypeFieldVB 
```

