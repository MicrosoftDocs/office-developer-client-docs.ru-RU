---
title: Вызов хранимой процедуры с помощью команды
TOCTitle: Calling a stored procedure with a command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6578dbfc50ae8ffeaa31f49b694b37ba5fd534e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296712"
---
# <a name="calling-a-stored-procedure-with-a-command"></a>Вызов хранимой процедуры с помощью команды


**Область применения**: Access 2013, Office 2013

Вы также можете использовать команду при вызове хранимой процедуры. Следующий код вызывает хранимую процедуру в образце базы данных Northwind под названием CustOrdersOrders, которая определяется следующим образом:

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

Эта хранимая процедура аналогична команде, используемой в параметрах командного [объекта,](command-object-parameters.md)так как она принимает параметр ИД клиента и возвращает сведения о заказах этого клиента. В коде ниже эта хранимая процедура используется в качестве источника для ADO **Recordset.**

С помощью хранимой процедуры можно получить доступ к другой возможности ADO: метод обновления коллекции **Parameters.**  С помощью этого метода ADO может автоматически заполнять все сведения о параметрах, необходимых команде во время работы. При использовании этого метода производительность может быть неустойка, так как служба ADO должна запросить у источника данных сведения о параметрах.

Другие важные различия между кодом ниже и кодом в параметрах command [Object](command-object-parameters.md), где параметры были введены вручную. Во-первых, в этом коде свойство **Prepared** не имеет свойства **True,** так как это SQL Server хранимая процедура и предварительно компилироваться по определению. Во-вторых, свойство **CommandType** объекта **Command** изменено на **adCmdStoredProc** во втором примере, чтобы сообщить ADO, что команда является хранимой процедурой.

```vb 
 
'BeginAutoParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set CommandText equal to the stored procedure name. 
 objCmd.CommandText = "CustOrdersOrders" 
 objCmd.CommandType = adCmdStoredProc 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Automatically fill in parameter info from stored procedure. 
 objCmd.Parameters.Refresh 
 
 ' Set the param value. 
 objCmd(1) = "ALFKI" 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd(1) = "CACTU" 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
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
 Set objParm1 = Nothing 
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
 Set objParm1 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndAutoParamCmd 
```

