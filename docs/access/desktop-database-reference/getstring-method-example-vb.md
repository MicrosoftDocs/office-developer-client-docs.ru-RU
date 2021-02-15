---
title: Пример использования метода GetString (VB)
TOCTitle: GetString method example (VB)
ms:assetid: fa954e48-0810-9d71-4e24-f3ae2839105a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250280(v=office.15)
ms:contentKeyID: 48548849
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b874b4e53a60588668573fb58a206626d9cc81cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292183"
---
# <a name="getstring-method-example-vb"></a><span data-ttu-id="f7c57-102">Пример использования метода GetString (VB)</span><span class="sxs-lookup"><span data-stu-id="f7c57-102">GetString method example (VB)</span></span>


<span data-ttu-id="f7c57-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7c57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7c57-104">В этом примере демонстрируется [метод GetString.](getstring-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f7c57-104">This example demonstrates the [GetString](getstring-method-ado.md) method.</span></span>

<span data-ttu-id="f7c57-105">Предположим, что отладка проблемы с доступом к данным и быстрый простой способ печати текущего содержимого небольшого наборов [записей.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f7c57-105">Assume you are debugging a data access problem and want a quick, simple way of printing the current contents of a small [Recordset](recordset-object-ado.md).</span></span>

```vb 
 
'BeginGetStringVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim rstAuthors As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 Dim varOutput As Variant 
 
 ' specific variables 
 Dim strPrompt As String 
 Dim strState As String 
 
 ' open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' get user input 
 strPrompt = "Enter a state (CA, IN, KS, MD, MI, OR, TN, UT): " 
 strState = Trim(InputBox(strPrompt, "GetString Example")) 
 
 ' open recordset 
 Set rstAuthors = New ADODB.Recordset 
 strSQLAuthors = "SELECT au_fname, au_lname, address, city FROM Authors " & _ 
 "WHERE state = '" & strState & "'" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 If Not rstAuthors.EOF Then 
 ' Use all defaults: get all rows, TAB as column delimiter, 
 ' CARRIAGE RETURN as row delimiter, EMPTY-string as null delimiter 
 varOutput = rstAuthors.GetString(adClipString) 
 ' print output 
 Debug.Print "State = '" & strState & "'" 
 Debug.Print "Name Address City" & vbCr 
 Debug.Print varOutput 
 Else 
 Debug.Print "No rows found for state = '" & strState & "'" & vbCr 
 End If 
 
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
'EndGetStringVB 
```

