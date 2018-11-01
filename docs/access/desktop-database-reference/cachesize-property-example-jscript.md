---
title: Пример использования свойства CacheSize (JScript)
TOCTitle: CacheSize property example (JScript)
ms:assetid: bee835cb-8d26-b8b7-4958-39261809b86c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249928(v=office.15)
ms:contentKeyID: 48547473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab8a8f3aa1bb968ebed86c5718c4f236a9d4fc3b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887798"
---
# <a name="cachesize-property-example-jscript"></a>Пример использования свойства CacheSize (JScript)


**Применимо к**: Access 2013, Office 2013

В этом примере используется свойство [CacheSize](cachesize-property-ado.md) для отображения разницу в производительности для операции, выполняемой с и без 30 записи кэша. Скопируйте и вставьте следующий код в блокноте или другом текстовом редакторе и сохраните файл с именем **CacheSizeJS.asp**.

```javascript 
 
<!-- BeginCacheSizeJS --> 
<%@ Language="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<HTML> 
<HEAD> 
<title>CacheSize property example (JScript)</title> 
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
<h1>CacheSize property example (JScript)</h1> 
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

