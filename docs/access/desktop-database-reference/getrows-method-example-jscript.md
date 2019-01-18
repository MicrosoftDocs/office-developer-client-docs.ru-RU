---
title: Пример использования метода GetRows (JScript)
TOCTitle: GetRows method example (JScript)
ms:assetid: 72d7e2d9-1e19-e993-0b0e-5310405c9b75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249466(v=office.15)
ms:contentKeyID: 48545620
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6da2dc9ff721adbb4bc0e533a02085adb534b0b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722041"
---
# <a name="getrows-method-example-jscript"></a>Пример использования метода GetRows (JScript)


**Применимо к**: Access 2013, Office 2013

В этом примере используется метод [получения строк](getrows-method-ado.md) для получения всех строк в таблице *Custiomers* из [набора записей](recordset-object-ado.md) и для заполнения массива с полученными данными. Метод **получения строк** возвращает меньше, чем требуемое число строк в двух случаях: если достигнут [конец файла](bof-eof-properties-ado.md) или если **Получение строк** попытались получить записи, которая была удалена другим пользователем. Функция возвращает **значение False** , только в том случае, если происходит второй вариант. Скопируйте и вставьте следующий код в блокноте или другом текстовом редакторе и сохраните файл с именем **GetRowsJS.asp**.

```javascript 
 
<!-- BeginGetRowsJS --> 
<%@ LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
 
<html> 
 
<head> 
<title>ADO Recordset.GetRows example (JScript)</title> 
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
 
<body bgcolor="white"> 
 
<h1>ADO Recordset.GetRows example (JScript)</h1> 
 <!-- Page text goes here --> 
<% 
 var Connect = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var mySQL = "select * from customers;"; 
 var showblank = " "; 
 var shownull = "-null-"; 
 
 var connTemp = Server.CreateObject("ADODB.Connection"); 
 
 try 
 { 
 connTemp.Open(Connect); 
 var rsTemp = Server.CreateObject("ADODB.Recordset"); 
 rsTemp.ActiveConnection = connTemp; 
 rsTemp.CursorLocation = adUseClient; 
 rsTemp.CursorType = adOpenKeyset; 
 rsTemp.LockType = adLockOptimistic; 
 rsTemp.Open(mySQL); 
 
 rsTemp.MoveFirst(); 
 
 if (rsTemp.RecordCount == 0) 
 { 
 Response.Write("No records matched "); 
 Response.Write (mySQL & "So cannot make table..."); 
 connTemp.Close(); 
 Response.End(); 
 } else 
 { 
 Response.Write('<table width="100%" border="2">'); 
 Response.Write('<tr class="thead2">'); 
 
 // Headings On The Table for each Field Name 
 for (var i=0; i<rsTemp.Fields.Count; i++) 
 { 
 fieldObject = rsTemp.fields(i); 
 Response.Write('<td width="' + Math.floor(100 / rsTemp.Fields.Count) + '%">' + fieldObject.name + "</td>"); 
 } 
 
 Response.Write("</tr>"); 
 
 // JScript doesn't support multi-dimensional arrays 
 // so we'll convert the returned array to a single 
 // dimensional JScript array and then display the data. 
 tempArray = rsTemp.GetRows(); 
 recArray = tempArray.toArray(); 
 
 var col = 1; 
 var maxCols = rsTemp.Fields.Count; 
 
 for (var thisField=0; thisField<recArray.length; thisField++) 
 { 
 if (col == 1) 
 Response.Write('<tr class="tbody">'); 
 if (recArray[thisField] == null) 
 recArray[thisField] = shownull; 
 if (recArray[thisField] == "") 
 recArray[thisField] = showblank; 
 Response.Write("<td>" + recArray[thisField] + "</td>"); 
 col++ 
 if (col > maxCols) 
 { 
 Response.Write("</tr>"); 
 col = 1; 
 } 
 } 
 Response.Write("</table>"); 
 } 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsTemp.State == adStateOpen) 
 rsTemp.Close; 
 if (connTemp.State == adStateOpen) 
 connTemp.Close; 
 rsTemp = null; 
 connTemp = null; 
 } 
%> 
 
</body> 
 
</html> 
<!-- EndGetRowsJS --> 
 
```

