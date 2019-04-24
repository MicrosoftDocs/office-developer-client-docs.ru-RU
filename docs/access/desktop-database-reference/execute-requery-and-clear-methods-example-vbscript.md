---
title: Пример использования методов Execute, Requery и Clear (VBScript)
TOCTitle: Execute, Requery, and Clear methods example (VBScript)
ms:assetid: 3999d3d8-693b-99ee-421a-7c67ff0e3cbf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249142(v=office.15)
ms:contentKeyID: 48544252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 698139e031535b3a678ae573ebcb747f3a92eea2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293310"
---
# <a name="execute-requery-and-clear-methods-example-vbscript"></a><span data-ttu-id="336fb-102">Пример использования методов Execute, Requery и Clear (VBScript)</span><span class="sxs-lookup"><span data-stu-id="336fb-102">Execute, Requery, and Clear methods example (VBScript)</span></span>


<span data-ttu-id="336fb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="336fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="336fb-104">В этом примере демонстрируется метод **EXECUTE** при выполнении как из объекта [Command](command-object-ado.md) , так и из объекта [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="336fb-104">This example demonstrates the **Execute** method when run from both a [Command](command-object-ado.md) object and a [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="336fb-105">Кроме того, он [](requery-method-ado.md) использует метод Requery для получения текущих данных в объекте [Recordset](recordset-object-ado.md), а метод [clear](clear-method-ado.md) — для очистки содержимого коллекции [Errors](errors-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="336fb-105">It also uses the [Requery](requery-method-ado.md) method to retrieve current data in a [recordset](recordset-object-ado.md), and the [Clear](clear-method-ado.md) method to clear the contents of the [Errors](errors-collection-ado.md) collection.</span></span> <span data-ttu-id="336fb-106">Для выполнения этой процедуры необходимы процедуры ExecuteCommand и Принтаутпут.</span><span class="sxs-lookup"><span data-stu-id="336fb-106">The ExecuteCommand and PrintOutput procedures are required for this procedure to run.</span></span>

<span data-ttu-id="336fb-107">Используйте приведенный ниже пример на активной серверной странице (ASP).</span><span class="sxs-lookup"><span data-stu-id="336fb-107">Use the following example in an Active Server Page (ASP).</span></span> <span data-ttu-id="336fb-108">Используйте **Find** , чтобы найти файл адовбс. Inc и разместить его в каталоге, который планируется использовать.</span><span class="sxs-lookup"><span data-stu-id="336fb-108">Use **Find** to locate the file Adovbs.inc and place it in the directory you plan to use.</span></span> <span data-ttu-id="336fb-109">Скопируйте и вставьте следующий код в Блокнот или другой текстовый редактор и сохраните его как **ексекутевбс. ASP**.</span><span class="sxs-lookup"><span data-stu-id="336fb-109">Cut and paste the following code into Notepad or another text editor, and save it as **ExecuteVBS.asp**.</span></span> <span data-ttu-id="336fb-110">Результаты можно просмотреть в любом клиентском браузере.</span><span class="sxs-lookup"><span data-stu-id="336fb-110">You can view the result in any client browser.</span></span>

```vb 
 
<!-- BeginExecuteVBS --> 
<%@ Language=VBScript %> 
<% ' use this meta tag instead of ADOVBS.inc%> 
<!-- METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4"  --> 
<HTML> 
<HEAD> 
<META name="VI60_DefaultClientScript"  content=VBScript> 
<META NAME="GENERATOR" Content="Microsoft Visual Studio 6.0"> 
<title>ADO Execute Method</title> 
<STYLE> 
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
</STYLE> 
</HEAD> 
 
<BODY> 
<H3>ADO Execute Method</H3> 
<HR> 
<H4>Recordset Retrieved Using Connection Object</H4> 
<!--- Recordsets retrieved using Execute method of Connection and Command Objects--> 
<%  
     ' connection, command and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
    Dim Cmd  
    Dim rsProducts, strSQLProducts 
 
    ' create and open connection 
    Set Cnxn = Server.CreateObject("ADODB.Connection")  
    strCnxn="Provider='sqloledb';Data Source=" & _ 
            Request.ServerVariables("SERVER_NAME") & ";" & _ 
            "Integrated Security='SSPI';Initial Catalog='Northwind';" 
    Cnxn.Open  strCnxn 
    ' create and open recordset 
    Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
    strSQLCustomers = "Customers" 
    rsCustomers.Open strSQLCustomers, Cnxn, adOpenKeyset, adLockOptimistic, adCmdTable 
 
    '1st Recordset using Connection - Execute 
    Set rsCustomers = Cnxn.Execute(strSQLCustomers)  
 
    Set Cmd = Server.CreateObject("ADODB.Command") 
    Cmd.ActiveConnection = Cnxn 
    strSQLProducts = "SELECT * From Products" 
    Cmd.CommandText = strSQLProducts 
 
    '2nd Recordset Cmd - execute  
    Set rsProducts = Cmd.Execute 
    %> 
    <TABLE COLSPAN=8 CELLPADDING=5 BORDER=0 ALIGN=CENTER> 
    <!-- BEGIN column header row for Customer Table--> 
    <TR CLASS=thead> 
      <TH>Company Name</TH> 
      <TH>Contact Name</TH> 
      <TH>City</TH> 
    </TR> 
 
    <!--Display ADO Data from Customer Table--> 
    <%  
    Do While Not rsCustomers.EOF %> 
      <TR CLASS=tbody> 
        <TD>  
        <%= rsCustomers("CompanyName")%>  
        </TD> 
        <TD> 
        <%= rsCustomers("ContactName") %>  
        </TD> 
        <TD>  
        <%= rsCustomers("City")%>  
        </TD> 
      </TR>  
      <%  
    rsCustomers.MoveNext  
    Loop  
    %> 
</TABLE> 
 
<HR> 
<H4>Recordset Retrieved Using Command Object</H4> 
 
<TABLE CELLPADDING=5 BORDER=0 ALIGN=CENTER WIDTH="80%"> 
 
<!-- BEGIN column header row for Product List Table--> 
<TR CLASS=thead2> 
  <TH>Product Name</TH> 
  <TH>Unit Price</TH> 
</TR> 
 
<!-- Display ADO Data Product List--> 
<% Do Until rsProducts.EOF %> 
  <TR CLASS=tbody> 
    <TD> 
    <%= rsProducts("ProductName")%>   
    </TD> 
    <TD>  
    <%= rsProducts("UnitPrice")%>  
    </TD> 
<%  
    rsProducts.MoveNext  
    Loop 
  
    ' clean up 
    If rsCustomers.State = adStateOpen then 
        rsCustomers.Close 
    End If 
    If rsProducts.State = adStateOpen then 
        rsProducts.Close 
    End If 
    If Cnxn.State = adStateOpen then 
        Cnxn.Close 
    End If 
    Set Cmd = Nothing 
    Set rsCustomers = Nothing 
    Set rsProducts = Nothing 
    Set Cnxn = Nothing 
%> 
</TABLE> 
 
</BODY> 
</HTML> 
<!-- EndExecuteVBS --> 
```

