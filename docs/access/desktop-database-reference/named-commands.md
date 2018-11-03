---
title: Именованные команды
TOCTitle: Named commands
ms:assetid: 1a4d77e0-1736-83ea-a3c6-f5398c0b01e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248948(v=office.15)
ms:contentKeyID: 48543518
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45609ba0db81cf9ab807d2ea97c146a32028b884
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947835"
---
# <a name="named-commands"></a><span data-ttu-id="799e9-102">Именованные команды</span><span class="sxs-lookup"><span data-stu-id="799e9-102">Named commands</span></span>


<span data-ttu-id="799e9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="799e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="799e9-104">Можно задать свойство **Name** объекта **команды** и затем выполните команду путем вызова его, как если бы метод **ActiveConnection** свойства объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="799e9-104">You can set the **Name** property on a **Command** object and then execute the command by calling it as if it were a method on the **Command** object **ActiveConnection** property.</span></span> <span data-ttu-id="799e9-105">Это показано в следующем примере, в котором команда с именем *GetCustomers*.</span><span class="sxs-lookup"><span data-stu-id="799e9-105">This is illustrated in the following example, in which the command is named *GetCustomers*.</span></span> <span data-ttu-id="799e9-106">Обратите внимание на то, что код передает в объект **набора записей** объявленные и инициализированный GetCustomers «метод».</span><span class="sxs-lookup"><span data-stu-id="799e9-106">Notice that the code passes in a declared and instantiated **Recordset** object to the GetCustomers "method."</span></span> <span data-ttu-id="799e9-107">Можно также передать в параметрах «метод» если они являются обязательными в **команду**.</span><span class="sxs-lookup"><span data-stu-id="799e9-107">You can also pass in parameters to the "method" if they are required by the **Command**.</span></span>

```vb 
 
'BeginNamedCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objRs As New ADODB.Recordset 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 
 objCmd.CommandText = "SELECT CustomerID, CompanyName FROM Customers" 
 objCmd.CommandType = adCmdText 
 
 'Name the command. 
 objCmd.Name = "GetCustomers" 
 
 objCmd.ActiveConnection = objConn 
 
 ' Execute using Command.Name from the Connection. 
 objConn.GetCustomers objRs 
 
 ' Display. 
 Do While Not objRs.EOF 
 Debug.Print objRs(0) & vbTab & objRs(1) 
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
'EndNamedCmd 
```

