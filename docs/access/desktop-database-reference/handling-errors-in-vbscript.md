---
title: Обработка ошибок на языке сценариев VBScript
TOCTitle: Handling Errors in VBScript
ms:assetid: df8f96d5-b917-ddac-d274-6345b2499bf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250135(v=office.15)
ms:contentKeyID: 48548222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85af8f8840cdc74494f29d169cbccb3ce38cc6b4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862218"
---
# <a name="handling-errors-in-vbscript"></a><span data-ttu-id="f7e2a-102">Обработка ошибок на языке сценариев VBScript</span><span class="sxs-lookup"><span data-stu-id="f7e2a-102">Handling Errors in VBScript</span></span>


<span data-ttu-id="f7e2a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7e2a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7e2a-104">Отличается от методов, используемых в Visual Basic и тех, которые используются с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="f7e2a-104">There is little difference between the methods used in Visual Basic and those used with VBScript.</span></span> <span data-ttu-id="f7e2a-105">Основное различие заключается в том, что VBScript не поддерживает концепцию ошибок с продолжение выполнения на метку.</span><span class="sxs-lookup"><span data-stu-id="f7e2a-105">The primary difference is that VBScript does not support the concept of error handling by continuing execution at a label.</span></span> <span data-ttu-id="f7e2a-106">Другими словами On Error GoTo нельзя использовать в VBScript.</span><span class="sxs-lookup"><span data-stu-id="f7e2a-106">In other words, you cannot use On Error GoTo in VBScript.</span></span> <span data-ttu-id="f7e2a-107">Используйте в VBScript.</span><span class="sxs-lookup"><span data-stu-id="f7e2a-107">Instead, use in VBScript.</span></span> <span data-ttu-id="f7e2a-108">Вместо этого используйте On Error Resume Next и затем проверить **Err.Number** и свойство **Count** коллекции **ошибок** , как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="f7e2a-108">Instead, use On Error Resume Next and then check both **Err.Number** and the **Count** property of the **Errors** collection, as shown in the following example:</span></span>

```vb 
 
<!-- BeginErrorExampleVBS --> 
<HTML> 
<HEAD> 
<META NAME="GENERATOR" Content="Microsoft Visual Studio 6.0"> 
<TITLE>Error Handling example (VBScript)</TITLE> 
</HEAD> 
<BODY> 
 
<h1>Error Handling example (VBScript)</h1> 
 
<% 
 Dim errLoop 
 Dim strError 
 
 On Error Resume Next 
 
 ' Intentionally trigger an error. 
 Set cnn1 = Server.CreateObject("ADODB.Connection") 
 cnn1.Open "nothing" 
 
 If cnn1.Errors.Count > 0 Then 
 ' Enumerate Errors collection and display 
 ' properties of each Error object. 
 For Each errLoop In cnn1.Errors 
 strError = "Error #" & errLoop.Number & "<br>" & _ 
 " " & errLoop.Description & "<br>" & _ 
 " (Source: " & errLoop.Source & ")" & "<br>" & _ 
 " (SQL State: " & errLoop.SQLState & ")" & "<br>" & _ 
 " (NativeError: " & errLoop.NativeError & ")" & "<br>" 
 If errLoop.HelpFile = "" Then 
 strError = strError & _ 
 " No Help file available" & _ 
 "<br><br>" 
 Else 
 strError = strError & _ 
 " (HelpFile: " & errLoop.HelpFile & ")" & "<br>" & _ 
 " (HelpContext: " & errLoop.HelpContext & ")" & _ 
 "<br><br>" 
 End If 
 Response.Write ("<p>" & strError & "</p>") 
 Next 
 End If 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleVBS --> 
```

