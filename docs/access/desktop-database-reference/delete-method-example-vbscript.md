---
title: Пример использования метода Delete (VBScript)
TOCTitle: Delete method example (VBScript)
ms:assetid: aa647263-334b-152b-1d5e-2abe57bd7d73
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249788(v=office.15)
ms:contentKeyID: 48546947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77859e4800a9a14935e56a906a2a99393b7c4169
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860443"
---
# <a name="delete-method-example-vbscript"></a>Пример использования метода Delete (VBScript)


**Применимо к**: Access 2013 | Office 2013

В этом примере с помощью метода [Delete](delete-method-ado-recordset.md) для удаления определенной записи из [набора записей](recordset-object-ado.md).

Используйте следующий пример в активную страницу сервера (ASP).

Используйте **Поиск** для найдите файл Adovbs.inc и помещения их в каталог, который планируется использовать. Скопируйте и вставьте следующий код в блокноте или другом текстовом редакторе и сохраните файл с именем **DeleteVBS.asp**. Результат можно просмотреть в браузере любого клиента.

Для выполнения в примере, попробуйте использовать пример [AddNew](addnew-method-example-vbscript.md) сначала добавить несколько записей. Затем можно попробовать удалить их. Просмотрите результаты в любой клиентского браузера.

```vb 
 
<!-- BeginDeleteVBS --> 
<%@ Language=VBScript %> 
<% ' use this meta tag instead of ADOVBS.inc%> 
<!-- METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
<TITLE>ADO Delete Method</TITLE> 
</HEAD> 
<STYLE> 
<!-- 
TH { 
 background-color: #008080; 
 font-family: 'Arial Narrow','Arial',sans-serif; 
 font-size: xx-small; 
 color: white; 
 } 
TD { 
 text-align: center; 
 background-color: #f7efde; 
 font-family: 'Arial Narrow','Arial',sans-serif; 
 font-size: xx-small; 
 } 
--> 
</STYLE> 
 
<BODY> 
<H3>ADO Delete Method</H3> 
 
<% 
 ' to integrate this code replace the DataSource value in the connection string 
 
 ' connection and recordset variables 
 Dim Cnxn, strCnxn 
 Dim rsCustomers, strSQLCustomers 
 
 ' create and open connection 
 Set Cnxn = Server.CreateObject("ADODB.Connection") 
 strCnxn="Provider='sqloledb';Data Source=" & _ 
 Request.ServerVariables("SERVER_NAME") & ";" & _ 
 "Integrated Security='SSPI';Initial Catalog='Northwind';" 
 Cnxn.Open strCnxn 
 ' create and open recordset 
 Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
 strSQLCustomers = "Customers" 
 rsCustomers.Open strSQLCustomers, Cnxn, adOpenKeyset, adLockOptimistic, adCmdTable 
 
 ' Move to designated record and delete it 
 If Not IsEmpty(Request.Form("WhichRecord")) Then 
 'Get value to move from Form Post method 
 Moves = Request.Form("WhichRecord") 
 
 rsCustomers.Move CInt(Moves) 
 If Not rsCustomers.EOF or rsCustomers.BOF Then 
 ' handle any db errors 
 On Error Resume Next 
 rsCustomers.Delete 1 
 If Cnxn.Errors.Count <> 0 Then 
 Response.Write "Cannot delete since there are related records in other tables." 
 Response.End 
 End If 
 rsCustomers.MoveFirst 
 On Error GoTo 0 
 Else 
 Response.Write "Not a Valid Record Number" 
 rsCustomers.MoveFirst 
 End If 
 End If 
%> 
 
<!-- BEGIN column header row for Customer Table--> 
<TABLE COLSPAN=8 CELLPADDING=5 BORDER=0> 
<TR> 
 <TH>Rec. #</TH> 
 <TH>Company Name</TH> 
 <TH>Contact Name</TH> 
 <TH>City</TH> 
</TR> 
 
 <% 
 ' Display ADO Data from Customer Table 
 ' Loop through Recordset adding one row to HTML Table each pass 
 Dim iCount 
 iCount = 0 
 Do Until rsCustomers.EOF %> 
 <TR> 
 <TD> <%= CStr(iCount) %> 
 <TD> <%= rsCustomers("CompanyName")%> </TD> 
 <TD> <%= rsCustomers("ContactName")%> </TD> 
 <TD> <%= rsCustomers("City")%> </TD> 
 </TR> 
 <% 
 iCount = iCount + 1 
 rsCustomers.MoveNext 
 Loop 
 %> 
</TABLE> 
 
<!-- Do Client side Input Data Validation Move to named record and Delete it --> 
<Center> 
<H4>Clicking Button Will Remove Designated Record</H4> 
<H5>There are <%=rsCustomers.RecordCount%> Records in this Set</H5> 
 
<Form Method=Post Action="Deletevbs.asp" Name=Form> 
 <Input Type=Text Name="WhichRecord" Size=3> 
 <Input Type=Button Name=cmdDelete Value="Delete Record"> 
</Form> 
 
</BODY> 
 
<Script Language = "VBScript"> 
Sub cmdDelete_OnClick 
 If IsNumeric(Document.Form.WhichRecord.Value) Then 
 Document.Form.WhichRecord.Value = CInt(Document.Form.WhichRecord.Value) 
 Dim Response 
 Response = MsgBox("Are You Sure About Deleting This Record?", vbYesNo, "ADO-ASP Example") 
 
 If Response = vbYes Then 
 Document.Form.Submit 
 End If 
 Else 
 MsgBox "You Must Enter a Valid Record Number",,"ADO-ASP Example" 
 End If 
End Sub 
</Script> 
 
<% 
 ' clean up 
 If rsCustomers.State = adStateOpen then 
 rsCustomers.Close 
 End If 
 If Cnxn.State = adStateOpen then 
 Cnxn.Close 
 End If 
%> 
</HTML> 
<!-- EndDeleteVBS --> 
```

