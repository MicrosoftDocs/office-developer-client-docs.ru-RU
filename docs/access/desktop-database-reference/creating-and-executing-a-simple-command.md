---
title: Создание и выполнение простой команды
TOCTitle: Creating and executing a simple command
ms:assetid: 9ace1abe-cfae-0677-bc57-5cbda85b79db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249699(v=office.15)
ms:contentKeyID: 48546547
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2229c7580acc6848551103d83b7bfcf981d37bef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295319"
---
# <a name="creating-and-executing-a-simple-command"></a><span data-ttu-id="b13b1-102">Создание и выполнение простой команды</span><span class="sxs-lookup"><span data-stu-id="b13b1-102">Creating and executing a simple command</span></span>


<span data-ttu-id="b13b1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b13b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b13b1-104">Хотя объект **Command** не является типичным, приведенный ниже код показывает базовый метод использования объекта **Command** для выполнения команды для источника данных.</span><span class="sxs-lookup"><span data-stu-id="b13b1-104">Though not a typical usage of the **Command** object, the following code shows the basic method of using the **Command** object to execute a command against a data source.</span></span> <span data-ttu-id="b13b1-105">В этом случае это команда, возвращающая строки, поэтому она возвращает результаты выполнения команды в объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b13b1-105">In this case, it is a row-returning command, so it returns the results of the command execution into a **Recordset** object.</span></span>

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

<span data-ttu-id="b13b1-106">Выполняемая команда указывается с помощью свойства **CommandText** .</span><span class="sxs-lookup"><span data-stu-id="b13b1-106">The command to be executed is specified with the **CommandText** property.</span></span>


> [!NOTE]
> <span data-ttu-id="b13b1-107">Несколько примеров в этом разделе вызывают служебную функцию, **жетневконнектион**, чтобы установить подключение к поставщику данных.</span><span class="sxs-lookup"><span data-stu-id="b13b1-107">Several examples in this section call a utility function, **GetNewConnection**, to establish a connection with the data provider.</span></span> <span data-ttu-id="b13b1-108">Чтобы избежать избыточности, он указывается только один раз:</span><span class="sxs-lookup"><span data-stu-id="b13b1-108">To avoid redundancy, it is listed only once:</span></span>

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

