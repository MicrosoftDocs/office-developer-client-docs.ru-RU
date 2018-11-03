---
title: Потоки и сохраняемость
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a90031ac2f6d573631063edb0faf4893c2320d03
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944384"
---
# <a name="streams-and-persistence"></a><span data-ttu-id="a8ef2-102">Потоки и сохраняемость</span><span class="sxs-lookup"><span data-stu-id="a8ef2-102">Streams and persistence</span></span>


<span data-ttu-id="a8ef2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8ef2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8ef2-104">Хранилищ метод [Сохранить](save-method-ado.md) объект [набора записей](recordset-object-ado.md) , или *повторяется*, **записей** в файле и метод [Open](open-method-ado-recordset.md) восстанавливает **записей** из этого файла.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-104">The [Recordset](recordset-object-ado.md) object [Save](save-method-ado.md) method stores, or *persists*, a **Recordset** in a file, and the [Open](open-method-ado-recordset.md) method restores the **Recordset** from that file.</span></span>

<span data-ttu-id="a8ef2-105">С помощью ADO 2.5 способов **сохранения** и **открытия** можно сохранить **записей** в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a8ef2-105">With ADO 2.5, the **Save** and **Open** methods can persist a **Recordset** to a [Stream](stream-object-ado.md) object as well.</span></span> <span data-ttu-id="a8ef2-106">Эта функция особенно полезна при работе с удаленной службы данных (RDS) и Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="a8ef2-106">This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</span></span>

<span data-ttu-id="a8ef2-107">Дополнительные сведения об использовании сохраняемость в сам по себе на страницах ASP см текущего ASP.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-107">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</span></span>

<span data-ttu-id="a8ef2-108">Ниже приведены некоторые сценарии, в которых показано, как можно использовать **поток** объектов и сохранения.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-108">The following are a few scenarios that show how **Stream** objects and persistence can be used.</span></span>

## <a name="scenario-1"></a><span data-ttu-id="a8ef2-109">Сценарий 1</span><span class="sxs-lookup"><span data-stu-id="a8ef2-109">Scenario 1</span></span>

<span data-ttu-id="a8ef2-110">Этот сценарий просто сохраняет **записей** в файл, а затем **потока**.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-110">This scenario simply saves a **Recordset** to a file and then to a **Stream**.</span></span> <span data-ttu-id="a8ef2-111">Затем постоянных поток открывается в другой **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-111">It then opens the persisted stream into another **Recordset**.</span></span>

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

## <a name="scenario-2"></a><span data-ttu-id="a8ef2-112">Сценарий 2</span><span class="sxs-lookup"><span data-stu-id="a8ef2-112">Scenario 2</span></span>

<span data-ttu-id="a8ef2-113">Этот сценарий повторяется **записей** в **поток** в формате XML.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-113">This scenario persists a **Recordset** into a **Stream** in XML format.</span></span> <span data-ttu-id="a8ef2-114">Затем считывает **поток** в строку, которую можно проверить, работа с элементами управления или отображения.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-114">It then reads the **Stream** into a string that you can examine, manipulate, or display.</span></span>

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

## <a name="scenario-3"></a><span data-ttu-id="a8ef2-115">Сценарий 3</span><span class="sxs-lookup"><span data-stu-id="a8ef2-115">Scenario 3</span></span>

<span data-ttu-id="a8ef2-116">В этом примере кода показан код ASP сохранения **записей** как XML непосредственно в объект **ответа** :</span><span class="sxs-lookup"><span data-stu-id="a8ef2-116">This example code shows ASP code persisting a **Recordset** as XML directly to the **Response** object:</span></span>

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

## <a name="scenario-4"></a><span data-ttu-id="a8ef2-117">Сценарий 4</span><span class="sxs-lookup"><span data-stu-id="a8ef2-117">Scenario 4</span></span>

<span data-ttu-id="a8ef2-118">В этом сценарии ASP код записывает содержимое **набора записей** в формате ADTG клиента.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-118">In this scenario, ASP code writes the contents of the **Recordset** in ADTG format to the client.</span></span> <span data-ttu-id="a8ef2-119">[Служба курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) можно использовать эти данные для создания отключенного **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-119">The [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) can use this data to create a disconnected **Recordset**.</span></span>

<span data-ttu-id="a8ef2-120">Новое свойство на служб удаленных рабочих СТОЛОВ [DataControl](datacontrol-object-rds.md), [URL-адрес](url-property-rds.md)указывает на страницу .asp, которое создает **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-120">A new property on the RDS [DataControl](datacontrol-object-rds.md), [URL](url-property-rds.md), points to the .asp page that generates the **Recordset**.</span></span> <span data-ttu-id="a8ef2-121">Это означает, что объект **набора записей** можно получить без служб удаленных рабочих СТОЛОВ с помощью объекта [DataFactory](datafactory-object-rdsserver.md) на сервере или записи бизнес-объект пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-121">This means a **Recordset** object can be obtained without RDS using the server-side [DataFactory](datafactory-object-rdsserver.md) object or the user writing a business object.</span></span> <span data-ttu-id="a8ef2-122">Это значительно упрощает модель программирования служб удаленных рабочих СТОЛОВ.</span><span class="sxs-lookup"><span data-stu-id="a8ef2-122">This simplifies the RDS programming model significantly.</span></span>

<span data-ttu-id="a8ef2-123">Код на стороне сервера, с именемhttps://server/directory/recordset.asp:</span><span class="sxs-lookup"><span data-stu-id="a8ef2-123">Server-side code, named https://server/directory/recordset.asp:</span></span>

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

<span data-ttu-id="a8ef2-124">Код на стороне клиента:</span><span class="sxs-lookup"><span data-stu-id="a8ef2-124">Client-side code:</span></span>

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

<span data-ttu-id="a8ef2-125">Разработчики также имеют возможность использовать объект **набора записей** на стороне клиента:</span><span class="sxs-lookup"><span data-stu-id="a8ef2-125">Developers also have the option of using a **Recordset** object on the client:</span></span>

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

