---
<span data-ttu-id="98ef5-101"><<<<<<< Название HEAD: пример свойства ActiveCommand (JScript) TOCTitle: ms:assetid пример свойства ActiveCommand (JScript): ae67b69c-23d9-8c88-763a-a9a63499be32 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249824(v=office.15) ms:contentKeyID: 48547070 ms.date: 09/18 / 2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="98ef5-101"><<<<<<< HEAD title: ActiveCommand Property Example (JScript) TOCTitle: ActiveCommand Property Example (JScript) ms:assetid: ae67b69c-23d9-8c88-763a-a9a63499be32 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249824(v=office.15) ms:contentKeyID: 48547070 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-example-jscript"></a><span data-ttu-id="98ef5-102">ActiveCommand Property Example (JScript)</span><span class="sxs-lookup"><span data-stu-id="98ef5-102">ActiveCommand Property Example (JScript)</span></span>

<span data-ttu-id="98ef5-103">=== Название: пример свойства ActiveCommand (JScript) TOCTitle: ms:assetid пример (JScript) свойство ActiveCommand: ae67b69c-23d9-8c88-763a-a9a63499be32 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249824(v=office.15) ms:contentKeyID: 48547070 ms.date: 10/17/2018 mtps_version: v = Office.15</span><span class="sxs-lookup"><span data-stu-id="98ef5-103">======= title: ActiveCommand property example (JScript) TOCTitle: ActiveCommand property example (JScript) ms:assetid: ae67b69c-23d9-8c88-763a-a9a63499be32 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249824(v=office.15) ms:contentKeyID: 48547070 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-example-jscript"></a><span data-ttu-id="98ef5-104">Пример свойства ActiveCommand (JScript)</span><span class="sxs-lookup"><span data-stu-id="98ef5-104">ActiveCommand property example (JScript)</span></span>
>>>>>>> <span data-ttu-id="98ef5-105">master</span><span class="sxs-lookup"><span data-stu-id="98ef5-105">master</span></span>

<span data-ttu-id="98ef5-106">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="98ef5-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="98ef5-107">В этом примере демонстрируется свойство [ActiveCommand](activecommand-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="98ef5-107">This example demonstrates the [ActiveCommand](activecommand-property-ado.md) property.</span></span> <span data-ttu-id="98ef5-108">Скопируйте и вставьте следующий код в блокноте или другом текстовом редакторе и сохраните файл с именем **ActiveCommandJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="98ef5-108">Cut and paste the following code to Notepad or another text editor, and save it as **ActiveCommandJS.asp**.</span></span>

```javascript
<!-- BeginActiveCommandJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<% 
 // user input 
 strName = new String(Request.Form("ContactName")) 
%> 
 
<html> 
 
<head> 
<<<<<<< HEAD
<title>ActiveCommand Property Example (JScript)</title> 
=======
<title>ActiveCommand property example (JScript)</title> 
>>>>>>> master
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
 
<<<<<<< HEAD
<h1>ActiveCommand Property Example (JScript)</h1> 
=======
<h1>ActiveCommand property example (JScript)</h1> 
>>>>>>> master
 
<% 
if (strName.length > 0) 
 { 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var cmdContact = Server.CreateObject("ADODB.Command"); 
 var rsContact = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var strMessage; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 // Open a recordset using a command object 
 cmdContact.CommandText = "SELECT ContactName FROM Customers WHERE City = ?"; 
 cmdContact.ActiveConnection = Cnxn; 
 // create parameter and insert variable value 
 cmdContact.Parameters.Append(cmdContact.CreateParameter("ContactName", adChar, adParamInput, 30, strName)); 
 
 rsContact = cmdContact.Execute(); 
 
 while(!rsContact.EOF){ 
 // start new line 
 strMessage = "<P>"; 
 
 // get data 
 strMessage += rsContact("ContactName") 
 
 // end the line 
 strMessage += "</P>"; 
 
 // show data 
 Response.Write(strMessage); 
 
 // get next record 
 rsContact.MoveNext; 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // 'clean up 
 if (rsContact.State == adStateOpen) 
 rsContact.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsContact = null; 
 Cnxn = null; 
 } 
 } 
%> 
 
<hr> 
 
 
<form method="POST" action="ActiveCommandJS.asp"> 
 <p align="left">Enter city of customer to find (e.g., Paris): <input type="text" name="ContactName" size="40" value=""></p> 
 <p align="left"><input type="submit" value="Submit" name="B1"><input type="reset" value="Reset" name="B2"></p> 
</form> 
</body> 
 
</html> 
<!-- EndActiveCommandJS --> 
 
```

