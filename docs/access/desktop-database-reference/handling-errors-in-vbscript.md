---
title: Обработка ошибок на языке VBScript
TOCTitle: Handling errors in VBScript
ms:assetid: df8f96d5-b917-ddac-d274-6345b2499bf1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250135(v=office.15)
ms:contentKeyID: 48548222
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d1870f80c15d958fc1b28cf9ef165df0a834971c
ms.sourcegitcommit: 35b723efe168ae4bad461bd16b26f9a2412656f2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2021
ms.locfileid: "53139088"
---
# <a name="handling-errors-in-vbscript"></a>Обработка ошибок на языке VBScript


**Область применения**: Access 2013, Office 2013

Существует небольшая разница между методами, используемыми в Visual Basic и теми, которые используются с VBScript. Основное отличие состоит в том, что VBScript не поддерживает концепцию обработки ошибок, продолжая выполнение на метку. Другими словами, нельзя использовать On Error GoTo в VBScript. Вместо этого в VBScript используйте On Error Resume Next, а затем проверьте свойство **Err.Number** и свойство **Count** из коллекции **Ошибок,** как показано в следующем примере:

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

