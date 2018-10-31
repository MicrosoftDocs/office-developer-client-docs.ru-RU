---
title: Пример использования метода GetRows (VB)
TOCTitle: GetRows method example (VB)
ms:assetid: 5a4e03de-0c89-ed93-7fe8-685906878e60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249311(v=office.15)
ms:contentKeyID: 48545041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10ea58f34b89e01770889e49265ef7bd399b546e
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863873"
---
# <a name="getrows-method-example-vb"></a><span data-ttu-id="966a7-102">Пример использования метода GetRows (VB)</span><span class="sxs-lookup"><span data-stu-id="966a7-102">GetRows method example (VB)</span></span>


<span data-ttu-id="966a7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="966a7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="966a7-104">В этом примере используется метод [получения строк](getrows-method-ado.md) для извлечения указанное число строк из [набора записей](recordset-object-ado.md) и для заполнения массива с полученными данными.</span><span class="sxs-lookup"><span data-stu-id="966a7-104">This example uses the [GetRows](getrows-method-ado.md) method to retrieve a specified number of rows from a [Recordset](recordset-object-ado.md) and to fill an array with the resulting data.</span></span> <span data-ttu-id="966a7-105">Метод **получения строк** возвращает меньше, чем требуемое число строк в двух случаях: если достигнут [конец файла](bof-eof-properties-ado.md) или если **Получение строк** попытались получить записи, которая была удалена другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="966a7-105">The **GetRows** method will return fewer than the desired number of rows in two cases: either if [EOF](bof-eof-properties-ado.md) has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user.</span></span> <span data-ttu-id="966a7-106">Функция возвращает **значение False** , только в том случае, если происходит второй вариант.</span><span class="sxs-lookup"><span data-stu-id="966a7-106">The function returns **False** only if the second case occurs.</span></span> <span data-ttu-id="966a7-107">Функция GetRowsOK является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="966a7-107">The GetRowsOK function is required for this procedure to run.</span></span>

```vb 
 
'BeginGetRowsVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQLEmployees As String 
 Dim strCnxn As String 
 ' array variable 
 Dim arrEmployees As Variant 
 ' detail variables 
 Dim strMessage As String 
 Dim intRows As Integer 
 Dim intRecord As Integer 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open recordset client-side to enable RecordCount 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployees = "SELECT fName, lName, hire_date FROM Employee ORDER BY lName" 
 rstEmployees.Open strSQLEmployees, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' get user input for number of rows 
 Do 
 strMessage = "Enter number of rows to retrieve:" 
 intRows = Val(InputBox(strMessage)) 
 
 ' if bad user input exit the loop 
 If intRows <= 0 Then 
 MsgBox "Please enter a positive number", vbOKOnly, "Not less than zero!" 
 ' if number of requested records is over the total 
 ElseIf intRows > rstEmployees.RecordCount Then 
 MsgBox "Not enough records in Recordset to retrieve " & intRows & " rows.", _ 
 vbOKOnly, "Over the available total" 
 Else 
 Exit Do 
 End If 
 Loop 
 
 ' else put the data in an array and print 
 arrEmployees = rstEmployees.GetRows(intRows) 
 
 Dim x As Integer, y As Integer 
 
 For x = 0 To intRows - 1 
 For y = 0 To 2 
 Debug.Print arrEmployees(y, x) & " "; 
 Next y 
 Debug.Print vbCrLf 
 Next x 
 
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
'EndGetRowsVB 
```

