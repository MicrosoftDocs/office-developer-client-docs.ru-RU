---
<<<<<<< Название HEAD: пример свойства CacheSize (JScript) TOCTitle: пример свойства CacheSize (JScript) === название: пример свойства CacheSize (JScript) TOCTitle: пример свойства CacheSize (JScript)
>>>>>>> главные ms:assetid: bee835cb-8d26-b8b7-4958-39261809b86c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249928(v=office.15) ms:contentKeyID: 48547473 ms.date: 09/18/2015 mtps_version: v=office.15
---

<<<<<<< HEAD
# <a name="cachesize-property-example-jscript"></a>CacheSize Property Example (JScript)
=======
# <a name="cachesize-property-example-jscript"></a>Пример свойства CacheSize (JScript)
>>>>>>> master


**Применимо к**: Access 2013 | Office 2013

В этом примере используется свойство [CacheSize](cachesize-property-ado.md) для отображения разницу в производительности для операции, выполняемой с и без 30 записи кэша. Скопируйте и вставьте следующий код в блокноте или другом текстовом редакторе и сохраните файл с именем **CacheSizeJS.asp**.

```javascript 
 
<!-- BeginCacheSizeJS --> 
<%@ Language="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<HTML> 
<HEAD> 
<<<<<<< HEAD
<title>CacheSize Property Example (JScript)</title> 
=======
<title>CacheSize property example (JScript)</title> 
>>>>>>> master
<style> 
<!-- 
body { 
 font-family: 'Verdana','Arial','Helvetica',sans-serif; 
 BACKGROUND-COLOR:white; 
 COLOR:black; 
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
</HEAD> 
<BODY> 
<<<<<<< HEAD
<h1>CacheSize Property Example (JScript)</h1> 
=======
<h1>CacheSize property example (JScript)</h1> 
>>>>>>> master
<% 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsCustomer = Server.CreateObject("ADODB.Recordset"); 
 // caching variables 
 var Now = new Date(); 
 var Start = Now.getTime(); 
 var End, Cache, NoCache 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn) 
 
 // open a recordset on the Employee table using client-side cursor 
 rsCustomer.CursorLocation = adUseClient; 
 rsCustomer.Open("Customers", strCnxn); 
 
 // loop through the recordset 20 times 
 for (var i=1; i<=20; i++) 
 { 
 rsCustomer.MoveFirst(); 
 while (!rsCustomer.EOF) 
 { 
 // do something with the record 
 var strTemp = new String(rsCustomer("CompanyName")); 
 rsCustomer.MoveNext(); 
 } 
 } 
 
 Now = new Date(); 
 End = Now.getTime(); 
 NoCache = End - Start; 
 
 // cache records in groups of 30 
 rsCustomer.MoveFirst(); 
 rsCustomer.CacheSize = 30; 
 
 Now = new Date(); 
 Start = Now.getTime(); 
 
 // loop through the recordset 20 times 
 for (var i=1; i<=20; i++) 
 { 
 rsCustomer.MoveFirst(); 
 while (!rsCustomer.EOF) 
 { 
 // do something with the record 
 var strTemp = new String(rsCustomer("CompanyName")); 
 rsCustomer.MoveNext(); 
 } 
 } 
 
 Now = new Date(); 
 End = Now.getTime(); 
 var Cache = End - Start; 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsCustomer.State == adStateOpen) 
 rsCustomer.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsCustomer = null; 
 Cnxn = null; 
 } 
%> 
 
 <table border="2"> 
 <tr class="thead2"> 
 <th>No Cache</th> 
 <th>30 Record Cache</th> 
 </tr> 
 <tr class="tbody"> 
 <td><%=NoCache%></td> 
 <td><%=Cache%></td> 
 </tr> 
 </table> 
 
</BODY> 
</HTML> 
<!-- EndCacheSizeJS --> 
 
```

