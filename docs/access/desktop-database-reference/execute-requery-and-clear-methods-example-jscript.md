---
title: Пример использования методов Execute, Requery и Clear (JScript)
TOCTitle: Execute, Requery, and Clear methods example (JScript)
ms:assetid: 3c1f1913-f168-b8a9-8791-f4a0b1aa8273
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249157(v=office.15)
ms:contentKeyID: 48544306
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0556c40823facf5bdddbbe67874d6417b416674e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711730"
---
# <a name="execute-requery-and-clear-methods-example-jscript"></a>Пример использования методов Execute, Requery и Clear (JScript)


**Применимо к**: Access 2013, Office 2013

В этом примере демонстрируется использование метода **Execute** при вызове из объекта [команды](command-object-ado.md) и объект [подключения](connection-object-ado.md) . Он также использует метод [повторный запрос](requery-method-ado.md) для получения текущих данных в [набор записей](recordset-object-ado.md)и метод [снимите флажок](clear-method-ado.md) , чтобы удалить содержимое семейства [Errors](errors-collection-ado.md) . (Семейство **Errors** осуществляется через объект **подключения** из свойства [ActiveConnection](activeconnection-property-ado.md) [набора записей](recordset-object-ado.md)). Имя файла **ExecuteJS.asp**.

```javascript 
 
<!-- BeginExecuteJS --> 
<%@LANGUAGE="JScript"%> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<% 
 strLastName = new String(Request.Form("AuthorLName")); 
 
 if (strLastName.indexOf("undefined") > -1) 
 strLastName = ""; 
%> 
 
<html> 
 
<head> 
<title>Execute, Requery and Clear methods example (JScript)</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
--> 
</style> 
</head> 
 
<body bgcolor="White"> 
<h1>Execute, Requery and Clear methods example (JScript)</h1> 
<% 
 if (strLastName.length > 0) 
 { 
 // command and recordset variables 
 var Connect = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='pubs';Integrated Security='SSPI';"; 
 var Cnxn = Server.CreateObject("ADODB.Connection"); 
 var cmdAuthor = Server.CreateObject("ADODB.Command"); 
 var rsAuthor = Server.CreateObject("ADODB.Recordset"); 
 var rsAuthor2 = Server.CreateObject("ADODB.Recordset"); 
 var SQLAuthor2, strMessage, strMessage2; 
 var Err, ErrCount; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(Connect); 
 
 // command object parameters 
 cmdAuthor.CommandText = "SELECT * FROM Authors WHERE au_lname = ?"; 
 cmdAuthor.Parameters.Append(cmdAuthor.CreateParameter("Last Name", adChar, adParamInput, 20, strLastName)); 
 cmdAuthor.ActiveConnection = Cnxn; 
 
 // recordset from command.execute 
 rsAuthor = cmdAuthor.Execute(); 
 
 // recordset from connection.execute 
 SQLAuthor2 = "SELECT * FROM Authors"; 
 rsAuthor2 = Cnxn.Execute(SQLAuthor2); 
 
 // check for errors 
 ErrCount = Cnxn.errors.count; 
 if(ErrCount !== 0) //write the errors 
 { 
 for(Err = 0; Err = ErrCount; Err++){ 
 Err = Cnxn.errors.item; 
 Response.Write(Err); 
 } 
 // clean out any existing errors 
 Cnxn.Errors.Clear; 
 } 
 
 // show the data 
 Response.Write("<HR><HR>"); 
 
 // first recordset 
 Response.Write("<b>Command.Execute results</b>") 
 while (!rsAuthor.EOF) 
 { 
 // build output string by starting a new line 
 strMessage = "<P>"; 
 strMessage += "<br>"; 
 
 // recordset data 
 strMessage += rsAuthor("au_fname") + " "; 
 strMessage += rsAuthor("au_lname") + " "; 
 
 // end the line 
 strMessage += "</P>"; 
 
 // show the results 
 Response.Write(strMessage); 
 
 // get next record 
 rsAuthor.MoveNext; 
 } 
 
 Response.Write("<HR><HR>"); 
 
 // second recordset 
 Response.Write("<b>Connection.Execute results</b>") 
 while (!rsAuthor2.EOF) 
 { 
 // start a new line 
 strMessage2 = "<P>"; 
 
 // first and last name are in first column 
 strMessage2 += rsAuthor2("au_fname") + " " 
 strMessage2 += rsAuthor2("au_lname") + " "; 
 
 // end the line 
 strMessage2 += "</P>"; 
 
 // show results 
 Response.Write(strMessage2); 
 
 // get next record 
 rsAuthor2.MoveNext; 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsAuthor.State == adStateOpen) 
 rsAuthor.Close; 
 if (rsAuthor2.State == adStateOpen) 
 rsAuthor2.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsAuthor1 = null; 
 rsAuthor2 = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<hr> 
 
 
<form method="POST" action="ExecuteJS.asp" id=form1 name=form1> 
 <p align="left">Enter last name of author to find (e.g., Ringer): <input type="text" name="AuthorLName" size="40"></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
</body> 
 
</html> 
<!-- EndExecuteJS --> 
 
```

