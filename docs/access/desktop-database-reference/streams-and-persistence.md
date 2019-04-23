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
# <a name="streams-and-persistence"></a><span data-ttu-id="b9592-102">Потоки и сохраняемость</span><span class="sxs-lookup"><span data-stu-id="b9592-102">Streams and persistence</span></span>


<span data-ttu-id="b9592-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9592-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9592-104">Метод [Save](save-method-ado.md) объекта [Recordset](recordset-object-ado.md) сохраняет или сохраняет **набор записей** в файле, а метод [Open](open-method-ado-recordset.md) восстанавливает **набор записей** из этого файла. \*\*</span><span class="sxs-lookup"><span data-stu-id="b9592-104">The [Recordset](recordset-object-ado.md) object [Save](save-method-ado.md) method stores, or *persists*, a **Recordset** in a file, and the [Open](open-method-ado-recordset.md) method restores the **Recordset** from that file.</span></span>

<span data-ttu-id="b9592-105">С помощью ADO 2,5 методы **Save** и **Open** могут также сохранить объект **Recordset** в объекте [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b9592-105">With ADO 2.5, the **Save** and **Open** methods can persist a **Recordset** to a [Stream](stream-object-ado.md) object as well.</span></span> <span data-ttu-id="b9592-106">Эта функция особенно полезна при работе с удаленными службами данных (RDS) и ASP (Active Server Pages).</span><span class="sxs-lookup"><span data-stu-id="b9592-106">This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</span></span>

<span data-ttu-id="b9592-107">Для получения дополнительных сведений о том, как можно использовать сохраняемость на страницах ASP, ознакомьтесь с текущей документацией по ASP.</span><span class="sxs-lookup"><span data-stu-id="b9592-107">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</span></span>

<span data-ttu-id="b9592-108">Ниже приведено несколько сценариев, в которых показано, как можно использовать объекты **Stream** и сохраняемость.</span><span class="sxs-lookup"><span data-stu-id="b9592-108">The following are a few scenarios that show how **Stream** objects and persistence can be used.</span></span>

## <a name="scenario-1"></a><span data-ttu-id="b9592-109">Сценарий 1</span><span class="sxs-lookup"><span data-stu-id="b9592-109">Scenario 1</span></span>

<span data-ttu-id="b9592-110">В этом сценарии просто сохраняется **набор записей** в файл, а затем в **поток**.</span><span class="sxs-lookup"><span data-stu-id="b9592-110">This scenario simply saves a **Recordset** to a file and then to a **Stream**.</span></span> <span data-ttu-id="b9592-111">Затем он открывает постоянный поток в другом объекте **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b9592-111">It then opens the persisted stream into another **Recordset**.</span></span>

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

## <a name="scenario-2"></a><span data-ttu-id="b9592-112">Сценарий 2</span><span class="sxs-lookup"><span data-stu-id="b9592-112">Scenario 2</span></span>

<span data-ttu-id="b9592-113">В этом сценарии объект **Recordset** хранится в **потоке** в формате XML.</span><span class="sxs-lookup"><span data-stu-id="b9592-113">This scenario persists a **Recordset** into a **Stream** in XML format.</span></span> <span data-ttu-id="b9592-114">Затем он читает **поток** в строку, которую вы можете проверить, изменить или отобразить.</span><span class="sxs-lookup"><span data-stu-id="b9592-114">It then reads the **Stream** into a string that you can examine, manipulate, or display.</span></span>

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

## <a name="scenario-3"></a><span data-ttu-id="b9592-115">Сценарий 3</span><span class="sxs-lookup"><span data-stu-id="b9592-115">Scenario 3</span></span>

<span data-ttu-id="b9592-116">В этом примере кода показано, как код ASP сохраняет объект **Recordset** в виде XML непосредственно в объект **Response** :</span><span class="sxs-lookup"><span data-stu-id="b9592-116">This example code shows ASP code persisting a **Recordset** as XML directly to the **Response** object:</span></span>

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

## <a name="scenario-4"></a><span data-ttu-id="b9592-117">Сценарий 4</span><span class="sxs-lookup"><span data-stu-id="b9592-117">Scenario 4</span></span>

<span data-ttu-id="b9592-118">В этом сценарии код ASP записывает содержимое объекта **Recordset** в формате адтг в клиент.</span><span class="sxs-lookup"><span data-stu-id="b9592-118">In this scenario, ASP code writes the contents of the **Recordset** in ADTG format to the client.</span></span> <span data-ttu-id="b9592-119">[Служба курсора Майкрософт для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) может использовать эти данные для создания отключенного **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="b9592-119">The [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) can use this data to create a disconnected **Recordset**.</span></span>

<span data-ttu-id="b9592-120">Новое свойство в [элементе управления](datacontrol-object-rds.md)RDS данных ( [URL-адрес](url-property-rds.md)) указывает на ASP-страницу, создающую **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="b9592-120">A new property on the RDS [DataControl](datacontrol-object-rds.md), [URL](url-property-rds.md), points to the .asp page that generates the **Recordset**.</span></span> <span data-ttu-id="b9592-121">Это означает, что объект **Recordset** можно получить без RDS с использованием объекта факта [](datafactory-object-rdsserver.md) на стороне сервера или при написании бизнес-объекта пользователем.</span><span class="sxs-lookup"><span data-stu-id="b9592-121">This means a **Recordset** object can be obtained without RDS using the server-side [DataFactory](datafactory-object-rdsserver.md) object or the user writing a business object.</span></span> <span data-ttu-id="b9592-122">Это значительно упрощает модель программирования RDS.</span><span class="sxs-lookup"><span data-stu-id="b9592-122">This simplifies the RDS programming model significantly.</span></span>

<span data-ttu-id="b9592-123">Код на стороне сервера с именемhttps://server/directory/recordset.asp:</span><span class="sxs-lookup"><span data-stu-id="b9592-123">Server-side code, named https://server/directory/recordset.asp:</span></span>

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

<span data-ttu-id="b9592-124">Код на стороне клиента:</span><span class="sxs-lookup"><span data-stu-id="b9592-124">Client-side code:</span></span>

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

<span data-ttu-id="b9592-125">Кроме того, разработчики имеют возможность использовать объект **Recordset** в клиенте:</span><span class="sxs-lookup"><span data-stu-id="b9592-125">Developers also have the option of using a **Recordset** object on the client:</span></span>

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

