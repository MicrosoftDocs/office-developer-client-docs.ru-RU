---
title: Streams and Persistence
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5a6f49368def305964119edcb06b5bcc80c278d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314436"
---
# <a name="streams-and-persistence"></a>Потоки и сохраняемость


**Область применения**: Access 2013, Office 2013

Метод [Save объекта Recordset](recordset-object-ado.md) сохраняет или сохраняет объект **Recordset** в файле, а метод [Open](open-method-ado-recordset.md) восстанавливает **набор записей** из этого файла. [](save-method-ado.md)

С помощью ADO 2.5 методы **Save** и **Open** также могут сохранять **набор записей** в [объекте Stream.](stream-object-ado.md) Эта функция особенно полезна при работе с удаленной службой данных (RDS) и ASP (ASP).

Дополнительные сведения о том, как сохраняемость может использоваться самой собой на страницах ASP, см. в текущей документации ASP.

Ниже приводится несколько сценариев, которые показывают, как можно использовать объекты **Stream** и сохраняемость.

## <a name="scenario-1"></a>Сценарий 1

В этом сценарии набор **записей** просто сохраняется в файл, а затем в **stream.** Затем он открывает сохраняемого потока в другой **набор записей**.

```vb 
 
Dim rs1 As ADODB.Recordset 
Dim rs2 As ADODB.Recordset 
Dim stm As ADODB.Stream 
 
Set rs1 = New ADODB.Recordset 
Set rs2 = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
rs1.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""", adopenStatic, adLockReadOnly, adCmdText 
rs1.Save "c:\myfolder\mysubfolder\myrs.xml", adPersistXML 
rs1.Save stm, adPersistXML 
rs2.Open stm 
```

## <a name="scenario-2"></a>Сценарий 2

В этом сценарии набор **записей сохраняется** в **потоке** в формате XML. Затем поток **считывется** в строку, которую можно изучать, управлять или отображать.

```vb 
 
Dim rs As ADODB.Recordset 
Dim stm As ADODB.Stream 
Dim strRst As String 
 
Set rs = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
' Open, save, and close the recordset. 
rs.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
rs.Save stm, adPersistXML 
rs.Close 
Set rs = nothing 
 
' Put saved Recordset into a string variable. 
strRst = stm.ReadText(adReadAll) 
 
' Examine, manipulate, or display the XML data. 
... 
```

## <a name="scenario-3"></a>Сценарий 3

В этом примере кода показан код ASP, который сохраняет **объект Recordset** в качестве XML-кода непосредственно в **объекте Response:**

```vb 
 
... 
<% 
response.ContentType = "text/xml" 
 
' Create and open a Recordset. 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select * from Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
 
' Save Recordset directly into output stream. 
rs.Save Response, adPersistXML 
 
' Close Recordset. 
rs.Close 
Set rs = nothing 
%> 
... 
```

## <a name="scenario-4"></a>Сценарий 4

В этом сценарии код ASP записывает содержимое **recordset** в формате ADTG в клиент. Служба [курсоров Майкрософт для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) может использовать эти данные для создания отключенного **recordset.**

Новое свойство в URL-адресе RDS [DataControl](datacontrol-object-rds.md) [указывает](url-property-rds.md)на страницу ASP, которая создает **набор записей.** Это означает, что объект **Recordset** можно получить без RDS с помощью объекта [DataFactory](datafactory-object-rdsserver.md) на стороне сервера или пользователя, написав бизнес-объект. Это значительно упрощает модель программирования RDS.

Серверный код с именем https://server/directory/recordset.asp:

```vb 
 
<% 
Dim rs 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select au_fname, au_lname, phone from Authors", ""& _ 
 "Provider=sqloledb;Data Source=MyServer;" & _ 
 "Initial Catalog=Pubs;Integrated Security=SSPI;" 
response.ContentType = "multipart/mixed" 
rs.Save response, adPersistADTG 
%> 
```

Клиентский код:

```html 
 
<HTML> 
<HEAD> 
<TITLE>RDS Query Page</TITLE> 
</HEAD> 
<body> 
<CENTER> 
<H1>Remote Data Service 2.5</H1> 
<TABLE DATASRC="#DC1"> 
 <TR> 
 <TD><SPAN DATAFLD="au_fname"></SPAN></TD> 
 <TD><SPAN DATAFLD="au_lname"></SPAN></TD> 
 <TD><SPAN DATAFLD="phone"></SPAN></TD> 
 </TR> 
</TABLE> 

<BR> 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
 ID=DC1 HEIGHT=1 WIDTH = 1> 
 <PARAM NAME="URL" VALUE="https://server/directory/recordset.asp"> 
</OBJECT> 
 
</SCRIPT> 
</BODY> 
</HTML> 
```

Разработчики также могут использовать объект **Recordset** в клиенте:

```vb
... 
function GetRs() 
 { 
 rs = CreateObject("ADODB.Recordset"); 
 rs.Open "https://server/directory/recordset.asp" 
 DC1.SourceRecordset = rs; 
 } 
... 
```

