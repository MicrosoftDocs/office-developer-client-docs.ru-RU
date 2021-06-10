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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292232"
---
# <a name="getrows-method-example-jscript"></a><span data-ttu-id="38a82-102">Пример использования метода GetRows (JScript)</span><span class="sxs-lookup"><span data-stu-id="38a82-102">GetRows method example (JScript)</span></span>


<span data-ttu-id="38a82-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38a82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38a82-104">В этом примере метод [GetRows](getrows-method-ado.md) позволяет извлекать все строки таблицы *Custiomers* из [recordset](recordset-object-ado.md) и заполнять массив полученными данными.</span><span class="sxs-lookup"><span data-stu-id="38a82-104">This example uses the [GetRows](getrows-method-ado.md) method to retrieve all rows of the *Custiomers* table from a [Recordset](recordset-object-ado.md) and to fill an array with the resulting data.</span></span> <span data-ttu-id="38a82-105">Метод **GetRows** возвращает меньше строк, чем нужно в двух случаях: если достигнуто значение [EOF](bof-eof-properties-ado.md) или метод **GetRows** пытается получить запись, удаленную другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="38a82-105">The **GetRows** method will return fewer than the desired number of rows in two cases: either if [EOF](bof-eof-properties-ado.md) has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user.</span></span> <span data-ttu-id="38a82-106">Функция возвращает значение **False** только при возникновении второго случая.</span><span class="sxs-lookup"><span data-stu-id="38a82-106">The function returns **False** only if the second case occurs.</span></span> <span data-ttu-id="38a82-107">Вырезать и вклеить следующий код для Блокнот или другого редактора текста и сохранить его как **GetRowsJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="38a82-107">Cut and paste the following code to Notepad or another text editor, and save it as **GetRowsJS.asp**.</span></span>

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

