---
title: Параметры объекта команды
TOCTitle: Command object parameters
ms:assetid: b43bb20e-9d0a-b361-6845-d537ae667f0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249862(v=office.15)
ms:contentKeyID: 48547218
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5d6dc4f9c3dcd039154db74e578ed91aa62fb01
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944909"
---
# <a name="command-object-parameters"></a><span data-ttu-id="d69d8-102">Параметры объекта команды</span><span class="sxs-lookup"><span data-stu-id="d69d8-102">Command object parameters</span></span>

<span data-ttu-id="d69d8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d69d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d69d8-104">Использование наиболее интересных для объекта **команды** показано в следующем примере, в котором можно было параметризованные был изменен текст команды SQL.</span><span class="sxs-lookup"><span data-stu-id="d69d8-104">A more interesting use for the **Command** object is shown in the next example, in which the text of the SQL command has been modified to make it parameterized.</span></span> <span data-ttu-id="d69d8-105">Это позволяет использовать команды, передав в другое значение для параметра каждый раз.</span><span class="sxs-lookup"><span data-stu-id="d69d8-105">This makes it possible to reuse the command, passing in a different value for the parameter each time.</span></span> <span data-ttu-id="d69d8-106">Поскольку свойство **подготовленных** объекта **команды** задано значение **True**, ADO потребует поставщика для компиляции команды, указанной в **CommandText** перед выполнением в первый раз.</span><span class="sxs-lookup"><span data-stu-id="d69d8-106">Because the **Prepared** property on the **Command** object is set equal to **True**, ADO will require the provider to compile the command specified in **CommandText** before executing it for the first time.</span></span> <span data-ttu-id="d69d8-107">Он также будет сохранять скомпилированной команды в памяти.</span><span class="sxs-lookup"><span data-stu-id="d69d8-107">It also will retain the compiled command in memory.</span></span> <span data-ttu-id="d69d8-108">Это замедляет выполнение команды немного первого время выполнения из-за накладные расходы, необходимые для подготовки, но результаты в рост производительности каждый раз, когда после этого вызывается команда.</span><span class="sxs-lookup"><span data-stu-id="d69d8-108">This slows the execution of the command slightly the first time it is executed because of the overhead required to prepare it, but results in a performance gain each time the command is called thereafter.</span></span> <span data-ttu-id="d69d8-109">Таким образом команды должны быть подготовлен только в том случае, если они будут использоваться несколько раз.</span><span class="sxs-lookup"><span data-stu-id="d69d8-109">Thus, commands should be prepared only if they will be used more than once.</span></span>

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

<span data-ttu-id="d69d8-110">Не все поставщики поддерживают подготовленной команды.</span><span class="sxs-lookup"><span data-stu-id="d69d8-110">Not all providers support prepared commands.</span></span> <span data-ttu-id="d69d8-111">Если поставщик поддерживает команды подготовки, он возвращает ошибку, сразу же этому свойству присвоено **значение True**.</span><span class="sxs-lookup"><span data-stu-id="d69d8-111">If the provider does not support command preparation, it might return an error as soon as this property is set to **True**.</span></span> <span data-ttu-id="d69d8-112">Если он не возвращает ошибку, он игнорирует запрос на подготовку команды и свойству **подготовленных** присваивается **значение False**.</span><span class="sxs-lookup"><span data-stu-id="d69d8-112">If it does not return an error, it ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

