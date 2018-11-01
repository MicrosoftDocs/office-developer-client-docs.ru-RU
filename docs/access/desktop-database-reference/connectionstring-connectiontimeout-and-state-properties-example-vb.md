---
title: Пример использования свойств ConnectionString, ConnectionTimeout и State (VB)
TOCTitle: ConnectionString, ConnectionTimeout, and State properties example (VB)
ms:assetid: abdd0262-8647-d545-60e0-13f99337df06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249796(v=office.15)
ms:contentKeyID: 48546984
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf919661410ae207295c6b400938a5a534e39978
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888533"
---
# <a name="connectionstring-connectiontimeout-and-state-properties-example-vb"></a><span data-ttu-id="353c7-102">Пример использования свойств ConnectionString, ConnectionTimeout и State (VB)</span><span class="sxs-lookup"><span data-stu-id="353c7-102">ConnectionString, ConnectionTimeout, and State properties example (VB)</span></span>


<span data-ttu-id="353c7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="353c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="353c7-104">В этом примере демонстрируется различные способы использования свойства [ConnectionString](connectionstring-property-ado.md) для открытия объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="353c7-104">This example demonstrates different ways of using the [ConnectionString](connectionstring-property-ado.md) property to open a [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="353c7-105">Он также использует свойство [ConnectionTimeout](connectiontimeout-property-ado.md) , чтобы задать период времени ожидания и свойство [состояние](state-property-ado.md) для проверки состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="353c7-105">It also uses the [ConnectionTimeout](connectiontimeout-property-ado.md) property to set a connection timeout period, and the [State](state-property-ado.md) property to check the state of the connections.</span></span> <span data-ttu-id="353c7-106">Функция GetState является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="353c7-106">The GetState function is required for this procedure to run.</span></span>

```vb 
 
'BeginConnectionStringVB 
 
 'To integrate this code replace 
 'the database, DSN or Data Source values 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn1 As ADODB.Connection 
 Dim Cnxn2 As ADODB.Connection 
 Dim Cnxn3 As ADODB.Connection 
 Dim Cnxn4 As ADODB.Connection 
 
 ' Open a connection without using a Data Source Name (DSN) 
 Set Cnxn1 = New ADODB.Connection 
 Cnxn1.ConnectionString = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn1.Open 
 MsgBox "Cnxn1 state: " & GetState(Cnxn1.State) 
 
 ' Open a connection using a DSN and ODBC tags 
 ' It is assumed that you have create DSN 'Pubs' with a user name as 
 ' 'MyUserId' and password as 'MyPassword'. 
 Set Cnxn2 = New ADODB.Connection 
 Cnxn2.ConnectionString = "Data Source='Pubs';" & _ 
 "User ID='MyUserId';Password='MyPassword';" 
 Cnxn2.ConnectionTimeout = 30 
 Cnxn2.Open 
 MsgBox "Cnxn2 state: " & GetState(Cnxn2.State) 
 
 ' Open a connection using a DSN and OLE DB tags 
 ' It is assumed that you have create DSN 'Pubs1' with windows authentication. 
 Set Cnxn3 = New ADODB.Connection 
 Cnxn3.ConnectionString = "Data Source='Pubs1';" 
 Cnxn3.Open 
 MsgBox "Cnxn2 state: " & GetState(Cnxn3.State) 
 
 ' Open a connection using a DSN and individual 
 ' arguments instead of a connection string 
 ' It is assumed that you have create DSN 'Pubs' with a user name as 
 ' 'MyUserId' and password as 'MyPassword'. 
 Set Cnxn4 = New ADODB.Connection 
 Cnxn4.Open "Pubs", "MyUserId", "MyPassword" 
 MsgBox "Cnxn4 state: " & GetState(Cnxn4.State) 
 
 ' clean up 
 Cnxn1.Close 
 Cnxn2.Close 
 Cnxn3.Close 
 Cnxn4.Close 
 Set Cnxn1 = Nothing 
 Set Cnxn2 = Nothing 
 Set Cnxn3 = Nothing 
 Set Cnxn4 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn1 Is Nothing Then 
 If Cnxn1.State = adStateOpen Then Cnxn1.Close 
 End If 
 Set Cnxn1 = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Not Cnxn3 Is Nothing Then 
 If Cnxn3.State = adStateOpen Then Cnxn3.Close 
 End If 
 Set Cnxn3 = Nothing 
 
 If Not Cnxn4 Is Nothing Then 
 If Cnxn4.State = adStateOpen Then Cnxn4.Close 
 End If 
 Set Cnxn4 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
 
Public Function GetState(intState As Integer) As String 
 
 Select Case intState 
 Case adStateClosed 
 GetState = "adStateClosed" 
 Case adStateOpen 
 GetState = "adStateOpen" 
 End Select 
 
End Function 
'EndConnectionStringVB 
```

