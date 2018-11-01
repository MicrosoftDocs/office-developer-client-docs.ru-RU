---
title: Параметры объекта команды
TOCTitle: Command Object Parameters
ms:assetid: b43bb20e-9d0a-b361-6845-d537ae667f0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249862(v=office.15)
ms:contentKeyID: 48547218
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3ce61f514e174595a458f66ea0a6c671ce5a9dc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880175"
---
# <a name="command-object-parameters"></a>Параметры объекта команды


**Применимо к**: Access 2013, Office 2013

Использование наиболее интересных для объекта **команды** показано в следующем примере, в котором можно было параметризованные был изменен текст команды SQL. Это позволяет использовать команды, передав в другое значение для параметра каждый раз. Поскольку свойство **подготовленных** объекта **команды** задано значение **True**, ADO потребует поставщика для компиляции команды, указанной в **CommandText** перед выполнением в первый раз. Он также будет сохранять скомпилированной команды в памяти. Это замедляет выполнение команды немного первого время выполнения из-за накладные расходы, необходимые для подготовки, но результаты в рост производительности каждый раз, когда после этого вызывается команда. Таким образом команды должны быть подготовлен только в том случае, если они будут использоваться несколько раз.

```vb 
 
'BeginManualParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set the CommandText as a parameterized SQL query. 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = ? " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Prepare command since we will be executing it more than once. 
 objCmd.Prepared = True 
 
 ' Create new parameter for CustomerID. Initial value is ALFKI. 
 Set objParm1 = objCmd.CreateParameter("CustId", adChar, _ 
 adParamInput, 5, "ALFKI") 
 objCmd.Parameters.Append objParm1 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd("CustId") = "CACTU" 
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
'EndManualParamCmd 
```

Не все поставщики поддерживают подготовленной команды. Если поставщик поддерживает команды подготовки, он возвращает ошибку, сразу же этому свойству присвоено **значение True**. Если он не возвращает ошибку, он игнорирует запрос на подготовку команды и свойству **подготовленных** присваивается **значение False**.

