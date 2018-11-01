---
title: Создание и выполнение простой команды
TOCTitle: Creating and Executing a Simple Command
ms:assetid: 9ace1abe-cfae-0677-bc57-5cbda85b79db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249699(v=office.15)
ms:contentKeyID: 48546547
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0446654a6ad39246289690c95f160bd77dcde19d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886265"
---
# <a name="creating-and-executing-a-simple-command"></a><span data-ttu-id="d64e5-102">Создание и выполнение простой команды</span><span class="sxs-lookup"><span data-stu-id="d64e5-102">Creating and Executing a Simple Command</span></span>


<span data-ttu-id="d64e5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d64e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d64e5-104">Если не типичное использование объекта **команды** , в следующем коде показан базового метода с помощью объекта **команды** для выполнения команды в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="d64e5-104">Though not a typical usage of the **Command** object, the following code shows the basic method of using the **Command** object to execute a command against a data source.</span></span> <span data-ttu-id="d64e5-105">В этом случае это команда возвращает строку, поэтому он возвращает результаты выполнения команды в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d64e5-105">In this case, it is a row-returning command, so it returns the results of the command execution into a **Recordset** object.</span></span>

```vb 
 
 'BeginBasicCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objRs As New ADODB.Recordset 
 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = 'ALFKI' " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print "ALFKI" 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 'clean up 
 objRs.Close 
 objConn.Close 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Exit Sub 
 
ErrHandler: 
 'clean up 
 If objRs.State = adStateOpen Then 
 objRs.Close 
 End If 
 
 If objConn.State = adStateOpen Then 
 objConn.Close 
 End If 
 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndBasicCmd 
```

<span data-ttu-id="d64e5-106">Команду для выполнения указанного с помощью свойства **CommandText** .</span><span class="sxs-lookup"><span data-stu-id="d64e5-106">The command to be executed is specified with the **CommandText** property.</span></span>


> [!NOTE]
> <span data-ttu-id="d64e5-107">Примеры в данном разделе вызовите вспомогательную функцию, **GetNewConnection**, чтобы установить соединение с данным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="d64e5-107">Several examples in this section call a utility function, **GetNewConnection**, to establish a connection with the data provider.</span></span> <span data-ttu-id="d64e5-108">Чтобы избежать избыточности, оно указано только один раз:</span><span class="sxs-lookup"><span data-stu-id="d64e5-108">To avoid redundancy, it is listed only once:</span></span>

```vb 
 
'BeginNewConnection 
Private Function GetNewConnection() As ADODB.Connection 
 Dim oCn As New ADODB.Connection 
 Dim sCnStr As String 
 
 sCnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Integrated Security='SSPI';Database='Northwind';" 
 oCn.Open sCnStr 
 
 If oCn.State = adStateOpen Then 
 Set GetNewConnection = oCn 
 End If 
 
End Function 
'EndNewConnection 
```

