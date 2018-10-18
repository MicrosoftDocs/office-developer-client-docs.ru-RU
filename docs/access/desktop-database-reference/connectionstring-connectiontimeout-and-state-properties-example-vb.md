---
<span data-ttu-id="041be-101"><<<<<<< Название HEAD: ConnectionString, ConnectionTimeout и TOCTitle пример свойства состояния (VB): ConnectionString, ConnectionTimeout и пример свойства состояния (VB) === название: ConnectionString, ConnectionTimeout, Пример свойства состояния (VB) и TOCTitle: пример свойства ConnectionString, ConnectionTimeout и состояния (VB)</span><span class="sxs-lookup"><span data-stu-id="041be-101"><<<<<<< HEAD title: ConnectionString, ConnectionTimeout, and State Properties Example (VB) TOCTitle: ConnectionString, ConnectionTimeout, and State Properties Example (VB) ======= title: ConnectionString, ConnectionTimeout, and State properties example (VB) TOCTitle: ConnectionString, ConnectionTimeout, and State properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="041be-102">главные ms:assetid: abdd0262-8647-d545-60e0-13f99337df06 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249796(v=office.15) ms:contentKeyID: 48546984 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="041be-102">master ms:assetid: abdd0262-8647-d545-60e0-13f99337df06 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249796(v=office.15) ms:contentKeyID: 48546984 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="041be-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="041be-103"><<<<<<< HEAD</span></span>
# <a name="connectionstring-connectiontimeout-and-state-properties-example-vb"></a><span data-ttu-id="041be-104">ConnectionString, ConnectionTimeout, and State Properties Example (VB)</span><span class="sxs-lookup"><span data-stu-id="041be-104">ConnectionString, ConnectionTimeout, and State Properties Example (VB)</span></span>
=======
# <a name="connectionstring-connectiontimeout-and-state-properties-example-vb"></a><span data-ttu-id="041be-105">Пример свойства ConnectionString, ConnectionTimeout и состояния (VB)</span><span class="sxs-lookup"><span data-stu-id="041be-105">ConnectionString, ConnectionTimeout, and State properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="041be-106">master</span><span class="sxs-lookup"><span data-stu-id="041be-106">master</span></span>


<span data-ttu-id="041be-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="041be-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="041be-108">В этом примере демонстрируется различные способы использования свойства [ConnectionString](connectionstring-property-ado.md) для открытия объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="041be-108">This example demonstrates different ways of using the [ConnectionString](connectionstring-property-ado.md) property to open a [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="041be-109">Он также использует свойство [ConnectionTimeout](connectiontimeout-property-ado.md) , чтобы задать период времени ожидания и свойство [состояние](state-property-ado.md) для проверки состояния подключения.</span><span class="sxs-lookup"><span data-stu-id="041be-109">It also uses the [ConnectionTimeout](connectiontimeout-property-ado.md) property to set a connection timeout period, and the [State](state-property-ado.md) property to check the state of the connections.</span></span> <span data-ttu-id="041be-110">Функция GetState является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="041be-110">The GetState function is required for this procedure to run.</span></span>

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

