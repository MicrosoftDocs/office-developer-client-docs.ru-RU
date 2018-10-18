---
<span data-ttu-id="0b5ba-101"><<<<<<< Название HEAD: ActiveConnection CommandText, пример свойств CommandTimeout (JScript) TOCTitle: ActiveConnection, CommandText, CommandTimeout, CommandType, размер и пример свойств направление (JScript) ms:assetid : 2a79222c-4dba-9c5a-fff7-c8dd2711801f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249056(v=office.15) ms:contentKeyID: 48543909 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0b5ba-101"><<<<<<< HEAD title: ActiveConnection, CommandText, CommandTimeout Properties Example (JScript) TOCTitle: ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction Properties Example (JScript) ms:assetid: 2a79222c-4dba-9c5a-fff7-c8dd2711801f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249056(v=office.15) ms:contentKeyID: 48543909 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activeconnection-commandtext-commandtimeout-commandtype-size-and-direction-properties-example-jscript"></a><span data-ttu-id="0b5ba-102">ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction Properties Example (JScript)</span><span class="sxs-lookup"><span data-stu-id="0b5ba-102">ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction Properties Example (JScript)</span></span>

<span data-ttu-id="0b5ba-103">=== Название: ActiveConnection, CommandText, пример свойств CommandTimeout (JScript) TOCTitle: ActiveConnection, CommandText, CommandTimeout, CommandType, размер и направление ms:assetid example(JScript) свойства: 2a79222c-4dba-9C5A-fff7-c8dd2711801f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249056(v=office.15) ms:contentKeyID: 48543909 ms.date: 10/17/2018 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0b5ba-103">======= title: ActiveConnection, CommandText, CommandTimeout properties example (JScript) TOCTitle: ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction properties example(JScript) ms:assetid: 2a79222c-4dba-9c5a-fff7-c8dd2711801f ms:mtpsurl: https://msdn.microsoft.com/library/JJ249056(v=office.15) ms:contentKeyID: 48543909 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activeconnection-commandtext-commandtimeout-commandtype-size-and-direction-properties-example-jscript"></a><span data-ttu-id="0b5ba-104">Пример свойства ActiveConnection, CommandText, CommandTimeout, CommandType, размер и направление (JScript)</span><span class="sxs-lookup"><span data-stu-id="0b5ba-104">ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction properties example (JScript)</span></span>
>>>>>>> <span data-ttu-id="0b5ba-105">master</span><span class="sxs-lookup"><span data-stu-id="0b5ba-105">master</span></span>

<span data-ttu-id="0b5ba-106">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b5ba-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0b5ba-107">В этом примере использует [ActiveConnection](activeconnection-property-ado.md), [CommandText](commandtext-property-ado.md), [CommandTimeout](commandtimeout-property-ado.md), [CommandType](commandtype-property-ado.md), [размер](size-property-ado.md)и [направление](direction-property-ado.md) свойства для выполнения хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="0b5ba-107">This example uses the [ActiveConnection](activeconnection-property-ado.md), [CommandText](commandtext-property-ado.md), [CommandTimeout](commandtimeout-property-ado.md), [CommandType](commandtype-property-ado.md), [Size](size-property-ado.md), and [Direction](direction-property-ado.md) properties to execute a stored procedure.</span></span> <span data-ttu-id="0b5ba-108">Скопируйте и вставьте следующий код в блокноте или другом текстовом редакторе и сохраните файл с именем **ActiveConnectionJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="0b5ba-108">Cut and paste the following code to Notepad or another text editor, and save it as **ActiveConnectionJS.asp**.</span></span>

```javascript
<!-- BeginActiveConnectionJS --> 
<%@LANGUAGE="JScript"%> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
<head> 
 <title>ActiveConnection, CommandText, CommandTimeout, CommandType, Size, and Direction Properties</title> 
<style> 
<!-- 
BODY { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
 } 
.thead { 
 background-color: #008080; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.thead2 { 
 background-color: #800000; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 color: white; 
 } 
.tbody { 
 text-align: center; 
 background-color: #f7efde; 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 font-size: x-small; 
 } 
--> 
</style> 
</head> 
 
<body bgcolor="White"> 
 
<% 
 var iRoyalty = parseInt(Request.Form("RoyaltyValue")); 
 // check user input 
 
 if (iRoyalty > -1) 
 { 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='pubs';Integrated Security='SSPI';"; 
 var cmdByRoyalty = Server.CreateObject("ADODB.Command"); 
 var rsByRoyalty = Server.CreateObject("ADODB.Recordset"); 
 var rsAuthor = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var filter, strMessage; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 cmdByRoyalty.CommandText = "byroyalty"; 
 cmdByRoyalty.CommandType = adCmdStoredProc; 
 cmdByRoyalty.CommandTimeOut = 15; 
 
 // The stored procedure called above is as follows: 
 // CREATE PROCEDURE byroyalty 
 // @percentage int 
 // AS 
 // SELECT au_id from titleauthor 
 // WHERE titleauthor.royaltyper = @percentage 
 // GO 
 
 prmByRoyalty = Server.CreateObject("ADODB.Parameter"); 
 prmByRoyalty.Type = adInteger; 
 prmByRoyalty.Size = 3; 
 prmByRoyalty.Direction = adParamInput; 
 prmByRoyalty.Value = iRoyalty; 
 cmdByRoyalty.Parameters.Append(prmByRoyalty); 
 
 cmdByRoyalty.ActiveConnection = Cnxn; 
 
 // recordset by Command - Execute 
 rsByRoyalty = cmdByRoyalty.Execute(); 
 
 // recordset by Recordset - Open 
 rsAuthor.Open("Authors", Cnxn); 
 
 while (!rsByRoyalty.EOF) 
 { 
 // set filter 
 filter = "au_id='" + rsByRoyalty("au_id") 
 rsAuthor.Filter = filter + "'"; 
 
 // start new line 
 strMessage = "<P>"; 
 
 // get data 
 strMessage += rsAuthor("au_fname") + " "; 
 strMessage += rsAuthor("au_lname") + " "; 
 
 // end line 
 strMessage += "</P>"; 
 
 // show data 
 Response.Write(strMessage); 
 
 // get next record 
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
 
 
<form method="POST" action="ActiveConnectionJS.asp"> 
 <p align="left">Enter royalty percentage to find (e.g., 40): <input type="text" name="RoyaltyValue" size="5"></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
&nbsp; 
 
 
</body> 
 
</html> 
<!-- EndActiveConnectionJS --> 
 
```

