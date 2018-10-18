---
<span data-ttu-id="0ea21-101"><<<<<<< Название HEAD: ActualSize и TOCTitle пример: свойства DefinedSize (JScript): ActualSize и пример: свойства DefinedSize (JScript) ms:assetid: cf8d6cb6-3446-c193-8774-db41c4d14a2b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250032(v=office.15) мс: contentKeyID: 48547811 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0ea21-101"><<<<<<< HEAD title: ActualSize and DefinedSize Properties Example (JScript) TOCTitle: ActualSize and DefinedSize Properties Example (JScript) ms:assetid: cf8d6cb6-3446-c193-8774-db41c4d14a2b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250032(v=office.15) ms:contentKeyID: 48547811 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="actualsize-and-definedsize-properties-example-jscript"></a><span data-ttu-id="0ea21-102">ActualSize and DefinedSize Properties Example (JScript)</span><span class="sxs-lookup"><span data-stu-id="0ea21-102">ActualSize and DefinedSize Properties Example (JScript)</span></span>

<span data-ttu-id="0ea21-103">=== Название: пример свойства ActualSize и DefinedSize (JScript) TOCTitle: ActualSize и DefinedSize ms:assetid пример (JScript) свойства: cf8d6cb6-3446-c193-8774-db41c4d14a2b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250032(v=office.15) ms:contentKeyID: 48547811 ms.date: 10 / 16/2018 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0ea21-103">======= title: ActualSize and DefinedSize properties example (JScript) TOCTitle: ActualSize and DefinedSize properties example (JScript) ms:assetid: cf8d6cb6-3446-c193-8774-db41c4d14a2b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250032(v=office.15) ms:contentKeyID: 48547811 ms.date: 10/16/2018 mtps_version: v=office.15</span></span>
---

# <a name="actualsize-and-definedsize-properties-example-jscript"></a><span data-ttu-id="0ea21-104">Пример свойства ActualSize и DefinedSize (JScript)</span><span class="sxs-lookup"><span data-stu-id="0ea21-104">ActualSize and DefinedSize properties example (JScript)</span></span>
>>>>>>> <span data-ttu-id="0ea21-105">master</span><span class="sxs-lookup"><span data-stu-id="0ea21-105">master</span></span>

<span data-ttu-id="0ea21-106">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ea21-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0ea21-107">В этом примере с помощью свойства [ActualSize](actualsize-property-ado.md) и [DefinedSize](definedsize-property-ado.md) для отображения определенного размера и фактический размер поля.</span><span class="sxs-lookup"><span data-stu-id="0ea21-107">This example uses the [ActualSize](actualsize-property-ado.md) and [DefinedSize](definedsize-property-ado.md) properties to display the defined size and actual size of a field.</span></span> <span data-ttu-id="0ea21-108">Скопируйте и вставьте следующий код в блокноте или другом текстовом редакторе и сохраните файл с именем **ActualSizeJS.asp**.</span><span class="sxs-lookup"><span data-stu-id="0ea21-108">Cut and paste the following code to Notepad or another text editor, and save it as **ActualSizeJS.asp**.</span></span>

```javascript
<!-- BeginActualSizeJS --> 
<%@LANGUAGE="JScript" %> 
<%// use this meta tag instead of adojavas.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<html> 
 
<head> 
<<<<<<< HEAD
 <title>ActualSize and DefinedSize Properties Example (JScript)</title> 
=======
 <title>ActualSize and DefinedSize properties example (JScript)</title> 
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
</head> 
 
<body bgcolor="White"> 
 
<h1>ADO ActualSize and DefinedSize Properties (JScript)</h1> 
<% 
 // connection and recordset variables 
 var Cnxn = Server.CreateObject("ADODB.Connection") 
 var strCnxn = "Provider='sqloledb';Data Source=" + Request.ServerVariables("SERVER_NAME") + ";" + 
 "Initial Catalog='Northwind';Integrated Security='SSPI';"; 
 var rsSuppliers = Server.CreateObject("ADODB.Recordset"); 
 // display variables 
 var fld, strMessage; 
 
 try 
 { 
 // open connection 
 Cnxn.Open(strCnxn); 
 
 // Open a recordset on the stores table 
 rsSuppliers.Open("Suppliers", strCnxn); 
 
 // build table headers 
 Response.Write("<table>"); 
 Response.Write('<tr class="thead2"><th>Field Value</th>'); 
 Response.Write("<th>Defined Size</th>"); 
 Response.Write("<th>Actual Size</th></tr>"); 
 
 while (!rsSuppliers.EOF) 
 { 
 // start a new line 
 strMessage = '<tr class="tbody">'; 
 
 // Display the contents of the chosen field with 
 // its defined size and actual size 
 fld = rsSuppliers("CompanyName"); 
 strMessage += '<td align="left">' + fld.Value + "</td>" 
 strMessage += "<td>" + fld.DefinedSize + "</td>"; 
 strMessage += "<td>" + fld.ActualSize + "</td>"; 
 
 // end the line 
 strMessage += "</tr>"; 
 
 // display data 
 Response.Write(strMessage); 
 
 // get next record 
 rsSuppliers.MoveNext; 
 
 } 
 // close the table 
 Response.Write("</table>"); 
 } 
 catch (e) 
 { 
 Response.Write(e.message); 
 } 
 finally 
 { 
 // clean up 
 if (rsSuppliers.State == adStateOpen) 
 rsSuppliers.Close; 
 if (Cnxn.State == adStateOpen) 
 Cnxn.Close; 
 rsSuppliers = null; 
 Cnxn = null; 
 } 
%> 
 
</body> 
 
</html> 
<!-- EndActualSizeJS --> 
 
```

