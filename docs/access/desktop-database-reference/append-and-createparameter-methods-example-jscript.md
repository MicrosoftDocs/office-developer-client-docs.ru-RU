---
title: Пример использования методов Append и CreateParameter (JScript)
TOCTitle: Append and CreateParameter methods example (JScript)
ms:assetid: 77de4191-12f1-cd6b-1805-02546fe0a942
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249494(v=office.15)
ms:contentKeyID: 48545737
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 844cb85e4e760f9d6c92fdc4d6ec8996fcc167ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297146"
---
# <a name="append-and-createparameter-methods-example-jscript"></a><span data-ttu-id="63a6e-102">Пример использования методов Append и CreateParameter (JScript)</span><span class="sxs-lookup"><span data-stu-id="63a6e-102">Append and CreateParameter methods example (JScript)</span></span>


<span data-ttu-id="63a6e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63a6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63a6e-104">В этом примере используются [методы Append](append-method-ado.md) и [CreateParameter](createparameter-method-ado.md) для выполнения хранимой процедуры с входным параметром.</span><span class="sxs-lookup"><span data-stu-id="63a6e-104">This example uses the [Append](append-method-ado.md) and [CreateParameter](createparameter-method-ado.md) methods to execute a stored procedure with an input parameter.</span></span> <span data-ttu-id="63a6e-105">Включите следующий код в Блокнот или другой текстовый редактор и сохраните его как **AppendJS.asp.**</span><span class="sxs-lookup"><span data-stu-id="63a6e-105">Cut and paste the following code to Notepad or another text editor, and save it as **AppendJS.asp**.</span></span>

```javascript 
 
<!-- BeginAppendJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
<head> 
 <title>Append and CreateParameter methods example (JScript)</title> 
<style> 
<!-- 
body { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
--> 
</style> 
</head> 
 
<body> 
<h1>Append and CreateParameter methods example (JScript)</h1> 
<% 
 // verify user-input 
 var iRoyalty = parseInt(Request.Form("RoyaltyValue")); 
 if (iRoyalty > -1) 
 { 
 
 // connection, recordset and command variables 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='pubs';Integrated Security='SSPI';"; 
 var Cnxn = Server.CreateObject("ADODB.Connection"); 
 var cmdByRoyalty = Server.CreateObject("ADODB.Command"); 
 var rsByRoyalty = Server.CreateObject("ADODB.Recordset"); 
 var rsAuthor = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var strMessage; 
 
 try 
 { 
 // open connection and set cursor location 
 Cnxn.Open(strCnxn); 
 Cnxn.CursorLocation = adUseClient; 
 
 // command object initial parameters 
 cmdByRoyalty.CommandText = "byroyalty"; 
 cmdByRoyalty.CommandType = adCmdStoredProc; 
 
 // create the new parameter and append to 
 // the Command object's parameters collection 
 var prmByRoyalty = cmdByRoyalty.CreateParameter("percentage", adInteger, adParamInput); 
 cmdByRoyalty.Parameters.Append(prmByRoyalty); 
 prmByRoyalty.Value = iRoyalty; 
 
 cmdByRoyalty.ActiveConnection = Cnxn; 
 
 // execute command 
 rsByRoyalty = cmdByRoyalty.Execute(); 
 
 // display results 
 rsAuthor.Open("Authors", Cnxn); 
 
 
 while (!rsByRoyalty.EOF) 
 { 
 rsAuthor.Filter = "au_id='" + rsByRoyalty.Fields("au_id") + "'"; 
 
 // start new line 
 strMessage = "<P>"; 
 
 // recordset data 
 strMessage += rsAuthor.Fields("au_fname") + " "; 
 strMessage += rsAuthor.Fields("au_lname") + " "; 
 
 // end the line 
 strMessage += "</P>"; 
 
 // show result 
 Response.Write(strMessage); 
 
 // et next record 
 rsByRoyalty.MoveNext; 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsByRoyalty.State == adStateOpen) 
 rsByRoyalty.Close; 
 if (rsAuthor.State == adStateOpen) 
 rsAuthor.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsByRoyalty = null; 
 rsAuthor = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<hr> 
 
 
<form method="POST" action="AppendJS.asp" id=form1 name=form1> 
 <p align="left">Enter royalty percentage to find (e.g., 40): <input type="text" name="RoyaltyValue" size="5"></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
&nbsp; 
 
 
</body> 
 
</html> 
<!-- EndAppendJS --> 
 
```

