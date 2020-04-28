---
title: Пример использования свойств Command и CommandText (VB)
TOCTitle: Command and CommandText properties example (VB)
ms:assetid: 6bf35604-401b-0727-85e8-ac2ecda368df
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249425(v=office.15)
ms:contentKeyID: 48545462
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99570fc54cc7393d3dff7c51e81df086696b58f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296194"
---
# <a name="command-and-commandtext-properties-example-vb"></a><span data-ttu-id="919c8-102">Пример использования свойств Command и CommandText (VB)</span><span class="sxs-lookup"><span data-stu-id="919c8-102">Command and CommandText properties example (VB)</span></span>


<span data-ttu-id="919c8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="919c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="919c8-104">В приведенном ниже коде показано, как использовать свойство [Command](command-property-adox.md) для обновления текста процедуры.</span><span class="sxs-lookup"><span data-stu-id="919c8-104">The following code demonstrates how to use the [Command](command-property-adox.md) property to update the text of a procedure.</span></span>

```vb 
 
' BeginProcedureTextVB 
Sub Main() 
 On Error GoTo ProcedureTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the Command 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Update the CommandText 
 cmd.CommandText = "Select CustomerId, CompanyName, ContactName " & _ 
 "From Customers " & _ 
 "Where CustomerId = [CustId]" 
 
 ' Update the Procedure 
 Set cat.Procedures("CustomerById").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureTextError: 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndProcedureTextVB 
```

