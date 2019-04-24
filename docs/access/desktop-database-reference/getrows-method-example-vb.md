---
title: Пример использования метода GetRows (VB)
TOCTitle: GetRows method example (VB)
ms:assetid: 5a4e03de-0c89-ed93-7fe8-685906878e60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249311(v=office.15)
ms:contentKeyID: 48545041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 27bdc82b1ea8cd3fc019b036de98a921dd7bc9bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292239"
---
# <a name="getrows-method-example-vb"></a>Пример использования метода GetRows (VB)


**Область применения**: Access 2013, Office 2013

В этом примере метод [GetRows](getrows-method-ado.md) используется для получения указанного количества строк из объекта [Recordset](recordset-object-ado.md) и заполнения массива полученными данными. Метод **GetRows** будет возвращать меньше требуемого количества строк в двух случаях: либо при достижении [конца файла](bof-eof-properties-ado.md) , либо при попытке получить **** запись, которая была удалена другим пользователем. Функция возвращает **значение false** только в том случае, если происходит второй вариант. Для выполнения этой процедуры требуется функция Жетровсок.

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

