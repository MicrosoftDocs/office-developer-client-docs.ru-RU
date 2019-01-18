---
title: Потоки и сохраняемость
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5a6f49368def305964119edcb06b5bcc80c278d2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709308"
---
# <a name="streams-and-persistence"></a>Потоки и сохраняемость


**Применимо к**: Access 2013, Office 2013

Хранилищ метод [Сохранить](save-method-ado.md) объект [набора записей](recordset-object-ado.md) , или *повторяется*, **записей** в файле и метод [Open](open-method-ado-recordset.md) восстанавливает **записей** из этого файла.

С помощью ADO 2.5 способов **сохранения** и **открытия** можно сохранить **записей** в объект [потока](stream-object-ado.md) . Эта функция особенно полезна при работе с удаленной службы данных (RDS) и Active Server Pages (ASP).

Дополнительные сведения об использовании сохраняемость в сам по себе на страницах ASP см текущего ASP.

Ниже приведены некоторые сценарии, в которых показано, как можно использовать **поток** объектов и сохранения.

## <a name="scenario-1"></a>Сценарий 1

Этот сценарий просто сохраняет **записей** в файл, а затем **потока**. Затем постоянных поток открывается в другой **набор записей**.

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

Этот сценарий повторяется **записей** в **поток** в формате XML. Затем считывает **поток** в строку, которую можно проверить, работа с элементами управления или отображения.

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

В этом примере кода показан код ASP сохранения **записей** как XML непосредственно в объект **ответа** :

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

В этом сценарии ASP код записывает содержимое **набора записей** в формате ADTG клиента. [Служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) можно использовать эти данные для создания отключенного **набора записей**.

Новое свойство на служб удаленных рабочих СТОЛОВ [DataControl](datacontrol-object-rds.md), [URL-адрес](url-property-rds.md)указывает на страницу .asp, которое создает **набор записей**. Это означает, что объект **набора записей** можно получить без служб удаленных рабочих СТОЛОВ с помощью объекта [DataFactory](datafactory-object-rdsserver.md) на сервере или записи бизнес-объект пользователя. Это значительно упрощает модель программирования служб удаленных рабочих СТОЛОВ.

Код на стороне сервера, с именемhttps://server/directory/recordset.asp:

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

Код на стороне клиента:

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

Разработчики также имеют возможность использовать объект **набора записей** на стороне клиента:

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

