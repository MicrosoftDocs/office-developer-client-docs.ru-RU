---
title: Пример использования свойства ActiveCommand (VB)
TOCTitle: ActiveCommand property example (VB)
ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15)
ms:contentKeyID: 48545999
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 32ab8ba94570c98da03c3effc484490c327fd0a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282602"
---
# <a name="activecommand-property-example-vb"></a><span data-ttu-id="8364c-102">Пример использования свойства ActiveCommand (VB)</span><span class="sxs-lookup"><span data-stu-id="8364c-102">ActiveCommand property example (VB)</span></span>


<span data-ttu-id="8364c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8364c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8364c-104">В этом примере показано свойство [ActiveCommand](activecommand-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8364c-104">This example demonstrates the [ActiveCommand](activecommand-property-ado.md) property.</span></span>

<span data-ttu-id="8364c-105">Подпрограмме предоставляется объект [Recordset](recordset-object-ado.md) , свойство **ActiveCommand** которого используется для отображения текста команды и параметра, создавшего **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="8364c-105">A subroutine is given a [Recordset](recordset-object-ado.md) object whose **ActiveCommand** property is used to display the command text and parameter that created the **Recordset**.</span></span>

```vb 
 
'BeginActiveCommandVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim cmd As ADODB.Command 
 Dim rst As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 'record variables 
 Dim strPrompt As String 
 Dim strName As String 
 
 Set Cnxn = New ADODB.Connection 
 Set cmd = New ADODB.Command 
 
 strPrompt = "Enter an author's name (e.g., Ringer): " 
 strName = Trim(InputBox(strPrompt, "ActiveCommandX Example")) 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 'create SQL command string 
 cmd.CommandText = "SELECT * FROM Authors WHERE au_lname = ?" 
 cmd.Parameters.Append cmd.CreateParameter("LastName", adChar, adParamInput, 20, strName) 
 
 Cnxn.Open strCnxn 
 cmd.ActiveConnection = Cnxn 
 
 'create the recordset by executing command string 
 Set rst = cmd.Execute(, , adCmdText) 
 'see the results 
 Call ActiveCommandXprint(rst) 
 
 ' clean up 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndActiveCommandVB 
```

<span data-ttu-id="8364c-106">Процедуре **активекоммандкспринт** предоставляется только объект **Recordset** , но он должен напечатать текст команды и параметр, который создал **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="8364c-106">The **ActiveCommandXprint** routine is given only a **Recordset** object, yet it must print the command text and parameter that created the **Recordset**.</span></span> <span data-ttu-id="8364c-107">Это можно сделать, так как свойство **ActiveCommand** объекта **Recordset** получает связанный объект [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8364c-107">This can be done because the **Recordset** object's **ActiveCommand** property yields the associated [Command](command-object-ado.md) object.</span></span>

<span data-ttu-id="8364c-108">Свойство [CommandText](commandtext-property-ado.md) объекта **Command** возвращает параметризованную команду, которая создала **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="8364c-108">The **Command** object's [CommandText](commandtext-property-ado.md) property yields the parameterized command that created the **Recordset**.</span></span> <span data-ttu-id="8364c-109">Коллекция [Parameters](parameters-collection-ado.md) объекта **Command** возвращает значение, которое было заменено на заполнитель параметра команды ("**?**").</span><span class="sxs-lookup"><span data-stu-id="8364c-109">The **Command** object's [Parameters](parameters-collection-ado.md) collection yields the value that was substituted for the command's parameter placeholder ("**?**").</span></span>

<span data-ttu-id="8364c-110">Наконец, печатается сообщение об ошибке или имя автора и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="8364c-110">Finally, an error message or the author's name and ID are printed.</span></span>

```vb 
 
'BeginActiveCommandPrintVB 
Public Sub ActiveCommandXprint(rstp As ADODB.Recordset) 
 
 Dim strName As String 
 
 strName = rstp.ActiveCommand.Parameters.Item("LastName").Value 
 
 Debug.Print "Command text = '"; rstp.ActiveCommand.CommandText; "'" 
 Debug.Print "Parameter = '"; strName; "'" 
 
 If rstp.BOF = True Then 
 Debug.Print "Name = '"; strName; "', not found." 
 Else 
 Debug.Print "Name = '"; rstp!au_fname; " "; rstp!au_lname; _ 
 "', author ID = '"; rstp!au_id; "'" 
 End If 
 
 rstp.Close 
 Set rstp = Nothing 
End Sub 
'EndActiveCommandPrintVB 
```

