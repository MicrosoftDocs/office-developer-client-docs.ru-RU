---
title: Пример использования метода Append для коллекции Procedures (VB)
TOCTitle: Procedures Append method example (VB)
ms:assetid: fa6c5e7a-6764-2208-26c8-f7fe4140dec3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250279(v=office.15)
ms:contentKeyID: 48548843
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e1df7d4914a247dac6f96a3709f0930bceea0ea
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726143"
---
# <a name="procedures-append-method-example-vb"></a><span data-ttu-id="108c6-102">Пример использования метода Append для коллекции Procedures (VB)</span><span class="sxs-lookup"><span data-stu-id="108c6-102">Procedures Append method example (VB)</span></span>


<span data-ttu-id="108c6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="108c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="108c6-104">Следующий код демонстрирует использование [процедуры](procedures-collection-adox.md) сбора метод [Append](append-method-adox-procedures.md) и объект [команды](command-object-ado.md) для создания новой процедуры в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="108c6-104">The following code demonstrates how to use a [Command](command-object-ado.md) object and the [Procedures](procedures-collection-adox.md) collection [Append](append-method-adox-procedures.md) method to create a new procedure in the underlying data source.</span></span>

```vb 
 
' BeginCreateProcedureVB 
Sub Main() 
 On Error GoTo CreateProcedureError 
 
 Dim cnn As New ADODB.Connection 
 Dim cmd As New ADODB.Command 
 Dim prm As ADODB.Parameter 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Create the parameterized command (Microsoft Jet specific) 
 Set cmd.ActiveConnection = cnn 
 cmd.CommandText = "PARAMETERS [CustId] Text;" & _ 
 "Select * From Customers Where CustomerId = [CustId]" 
 
 ' Open the Catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Create the new Procedure 
 cat.Procedures.Append "CustomerById", cmd 
 
 'Clean 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
CreateProcedureError: 
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
' EndCreateProcedureVB 
```

