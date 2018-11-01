---
title: Поиск метода и индекса пример свойства (VB)
TOCTitle: Seek Method and Index property example (VB)
ms:assetid: c3ddb72c-2b19-53c8-9779-2c503486e44e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249957(v=office.15)
ms:contentKeyID: 48547577
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 692dcd7e046935aa447d6d39de574dd3d3e6b129
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871873"
---
# <a name="seek-method-and-index-property-example-vb"></a><span data-ttu-id="76a01-102">Поиск метода и индекса пример свойства (VB)</span><span class="sxs-lookup"><span data-stu-id="76a01-102">Seek Method and Index property example (VB)</span></span>


<span data-ttu-id="76a01-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76a01-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76a01-104">В этом примере используется метод [Seek](seek-method-ado.md) и свойства [Index](index-property-ado.md) объекта [набора записей](recordset-object-ado.md) в сочетании с заданным ***Идентификатор сотрудника***, найдите имя сотрудника в таблице ***Employees*** базы данных Nwind.mdb.</span><span class="sxs-lookup"><span data-stu-id="76a01-104">This example uses the [Recordset](recordset-object-ado.md) object's [Seek](seek-method-ado.md) method and [Index](index-property-ado.md) property in conjunction with a given ***Employee ID***, to locate the employee's name in the ***Employees*** table of the Nwind.mdb database.</span></span>

```vb 
 
'BeginSeekVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' To integrate this code replace the data source 
 ' in the connection string 
 
 'recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strSQLEmployees As String 
 
 Dim strID As String 
 Dim strPrompt As String 
 strPrompt = "Enter an EmployeeID (e.g., 1 to 9)" 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\Office\Samples\northwind.mdb';" 
 Cnxn.Open strCnxn 
 
 ' open recordset server-side for indexing 
 Set rstEmployees = New ADODB.Recordset 
 rstEmployees.CursorLocation = adUseServer 
 strSQLEmployees = "employees" 
 rstEmployees.Open strSQLEmployees, strCnxn, adOpenKeyset, adLockReadOnly, adCmdTableDirect 
 
 ' Does this provider support Seek and Index? 
 If rstEmployees.Supports(adIndex) And rstEmployees.Supports(adSeek) Then 
 rstEmployees.Index = "PrimaryKey" 
 ' Display all the employees 
 rstEmployees.MoveFirst 
 Do While rstEmployees.EOF = False 
 Debug.Print rstEmployees!EmployeeId; ": "; rstEmployees!firstname; " "; _ 
 rstEmployees!LastName 
 rstEmployees.MoveNext 
 Loop 
 
 ' Prompt the user for an EmployeeID between 1 and 9 
 rstEmployees.MoveFirst 
 Do 
 strID = LCase(Trim(InputBox(strPrompt, "Seek Example"))) 
 ' Quit if strID is a zero-length string (CANCEL, null, etc.) 
 If Len(strID) = 0 Then Exit Do 
 If Len(strID) = 1 And strID >= "1" And strID <= "9" Then 
 rstEmployees.Seek Array(strID), adSeekFirstEQ 
 If rstEmployees.EOF Then 
 Debug.Print "Employee not found." 
 Else 
 Debug.Print strID; ": Employee='"; rstEmployees!firstname; " "; _ 
 rstEmployees!LastName; "'" 
 End If 
 End If 
 Loop 
 End If 
 
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
'EndSeekVB 
```

