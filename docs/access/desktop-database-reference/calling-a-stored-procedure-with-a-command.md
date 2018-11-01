---
title: Вызов хранимой процедуры с помощью команды
TOCTitle: Calling a Stored Procedure with a Command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 05e68a18ccd97e33416c4603f033fb91acaf0210
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876003"
---
# <a name="calling-a-stored-procedure-with-a-command"></a>Вызов хранимой процедуры с помощью команды


**Применимо к**: Access 2013, Office 2013

Можно также использовать команду при вызове хранимой процедуры. Следующий код вызывает хранимую процедуру в образце базы данных Northwind, называется CustOrdersOrders, которое определяется следующим образом:

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

Эта процедура аналогична команды, используемой в [Объект параметров команды](command-object-parameters.md), в том, что она принимает параметр ID клиента и возвращает информацию о заказов этого клиента. В следующем примере кода в качестве источника используется эта хранимая процедура для набора **записей**ADO.

С помощью хранимая процедура позволяет получить доступ к другим возможность ADO: коллекции **параметров** метод **Refresh** . С помощью этого метода, ADO может автоматически заполнять все сведения о параметрах, необходимые для команды во время выполнения. Производительность снижается, в этот способ, поскольку ADO необходимо запросов к источнику данных для получения сведений о параметрах.

Существуют другие важные различия между приведенный ниже код и код, приведенный в [Объект параметров команды](command-object-parameters.md), где вручную введенные параметры. Во-первых этот код не свойства **подготовленных** значение **True,** так как они хранимая процедура SQL Server и компилироваться по определению. Во-вторых свойство **CommandType** объекта **команду** изменено на **adCmdStoredProc** во втором примере для оповещения ADO, что команда была хранимую процедуру.

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

