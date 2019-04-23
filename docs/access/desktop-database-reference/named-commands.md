---
title: Именованные команды
TOCTitle: Named commands
ms:assetid: 1a4d77e0-1736-83ea-a3c6-f5398c0b01e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248948(v=office.15)
ms:contentKeyID: 48543518
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40ce95c5879f5da9615c66d132d6c4847fae1569
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288646"
---
# <a name="named-commands"></a><span data-ttu-id="8f899-102">Именованные команды</span><span class="sxs-lookup"><span data-stu-id="8f899-102">Named commands</span></span>


<span data-ttu-id="8f899-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f899-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8f899-104">Вы можете задать свойство **Name** для объекта **Command** , а затем выполнить команду, вызвав ее так, как если бы она была методом для свойства **Command** Object **ActiveConnection** .</span><span class="sxs-lookup"><span data-stu-id="8f899-104">You can set the **Name** property on a **Command** object and then execute the command by calling it as if it were a method on the **Command** object **ActiveConnection** property.</span></span> <span data-ttu-id="8f899-105">Это показано в следующем примере, в котором команда именуется *Customers*.</span><span class="sxs-lookup"><span data-stu-id="8f899-105">This is illustrated in the following example, in which the command is named *GetCustomers*.</span></span> <span data-ttu-id="8f899-106">Обратите внимание, что код передается в методе Customers в объявленном объекте Recordset и созданном экземпляре объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="8f899-106">Notice that the code passes in a declared and instantiated **Recordset** object to the GetCustomers "method."</span></span> <span data-ttu-id="8f899-107">Вы также можете передать параметры в "метод", если они необходимы для **команды**.</span><span class="sxs-lookup"><span data-stu-id="8f899-107">You can also pass in parameters to the "method" if they are required by the **Command**.</span></span>

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

