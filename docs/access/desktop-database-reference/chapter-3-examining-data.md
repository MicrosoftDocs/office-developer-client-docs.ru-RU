---
title: Глава 3. Изучение данных
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcf837a02c40d11fecfa56b8aa34ac80a848411
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296460"
---
# <a name="chapter-3-examining-data"></a><span data-ttu-id="0ed3e-102">Глава 3. Изучение данных</span><span class="sxs-lookup"><span data-stu-id="0ed3e-102">Chapter 3: Examining data</span></span>

<span data-ttu-id="0ed3e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ed3e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ed3e-104">В главе 2 объясняется, как получить данные из источника данных в качестве объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="0ed3e-104">Chapter 2 explained how to retrieve data from a data source as a **Recordset** object.</span></span> <span data-ttu-id="0ed3e-105">В этой главе более **подробно рассматривается** набор записей, в том числе по навигации по набору **записей** и просмотру его данных.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-105">This chapter will discuss the **Recordset** in more detail, including how to navigate through the **Recordset** and view its data.</span></span>

<span data-ttu-id="0ed3e-106">**Записи имеют** методы и свойства, предназначенные для у прощего перемещения по ним и проверки их содержимого.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-106">**Recordsets** have methods and properties designed to make it easy to move through them and examine their contents.</span></span> <span data-ttu-id="0ed3e-107">В зависимости от функций, поддерживаемых поставщиком, некоторые методы или свойства **recordset** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-107">Depending on the functionality supported by the provider, some **Recordset** methods or properties might not be available.</span></span> <span data-ttu-id="0ed3e-108">Чтобы продолжить изучение объекта **Recordset,** рассмотрите объект **Recordset,** который будет возвращен из примера базы данных Northwind на Microsoft SQL Server 2000, используя следующий код:</span><span class="sxs-lookup"><span data-stu-id="0ed3e-108">To continue exploring the **Recordset** object, consider a **Recordset** that would be returned from the Northwind sample database on Microsoft SQL Server 2000, using the following code:</span></span>

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

<span data-ttu-id="0ed3e-109">Этот SQL возвращает набор **записей** с пятью строками (записями) и тремя столбцами (полями).</span><span class="sxs-lookup"><span data-stu-id="0ed3e-109">This SQL query returns a **Recordset** with five rows (records) and three columns (fields).</span></span> <span data-ttu-id="0ed3e-110">Значения для каждой строки показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-110">The values for each row are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ed3e-111">ПОЛЕ 0</span><span class="sxs-lookup"><span data-stu-id="0ed3e-111">FIELD 0</span></span><br />
<span data-ttu-id="0ed3e-112">Name = ProductID</span><span class="sxs-lookup"><span data-stu-id="0ed3e-112">Name = ProductID</span></span></p></th>
<th><p><span data-ttu-id="0ed3e-113">ПОЛЕ 1</span><span class="sxs-lookup"><span data-stu-id="0ed3e-113">FIELD 1</span></span><br />
<span data-ttu-id="0ed3e-114">Name = ProductName</span><span class="sxs-lookup"><span data-stu-id="0ed3e-114">Name = ProductName</span></span></p></th>
<th><p><span data-ttu-id="0ed3e-115">ПОЛЕ 2</span><span class="sxs-lookup"><span data-stu-id="0ed3e-115">FIELD 2</span></span><br />
<span data-ttu-id="0ed3e-116">Name = UnitPrice</span><span class="sxs-lookup"><span data-stu-id="0ed3e-116">Name = UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ed3e-117">7 </span><span class="sxs-lookup"><span data-stu-id="0ed3e-117">7</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-118">Органичное замеченное "По-разное" Боба</span><span class="sxs-lookup"><span data-stu-id="0ed3e-118">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-119">30.0000</span><span class="sxs-lookup"><span data-stu-id="0ed3e-119">30.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ed3e-120">14 </span><span class="sxs-lookup"><span data-stu-id="0ed3e-120">14</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-121">Тофу</span><span class="sxs-lookup"><span data-stu-id="0ed3e-121">Tofu</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-122">23.2500</span><span class="sxs-lookup"><span data-stu-id="0ed3e-122">23.2500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ed3e-123">28</span><span class="sxs-lookup"><span data-stu-id="0ed3e-123">28</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-124">Rssle Sauerkraut</span><span class="sxs-lookup"><span data-stu-id="0ed3e-124">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-125">45.6000</span><span class="sxs-lookup"><span data-stu-id="0ed3e-125">45.6000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ed3e-126">51</span><span class="sxs-lookup"><span data-stu-id="0ed3e-126">51</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-127">Manjimup : Apples</span><span class="sxs-lookup"><span data-stu-id="0ed3e-127">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-128">53.0000</span><span class="sxs-lookup"><span data-stu-id="0ed3e-128">53.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ed3e-129">74</span><span class="sxs-lookup"><span data-stu-id="0ed3e-129">74</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-130">Longlife Tofu</span><span class="sxs-lookup"><span data-stu-id="0ed3e-130">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="0ed3e-131">10.0000</span><span class="sxs-lookup"><span data-stu-id="0ed3e-131">10.0000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0ed3e-132">В следующем разделе объясняется, как найти текущее положение курсора в этом примере **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="0ed3e-132">The next section explains how to locate the current position of the cursor in this sample **Recordset**.</span></span>

<span data-ttu-id="0ed3e-133">В этой главе освещались следующие темы:</span><span class="sxs-lookup"><span data-stu-id="0ed3e-133">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="0ed3e-134">Locating the current record (ADO)</span><span class="sxs-lookup"><span data-stu-id="0ed3e-134">Locating the current record (ADO)</span></span>](locating-the-current-record.md)
- [<span data-ttu-id="0ed3e-135">Навигация по данным (ADO)</span><span class="sxs-lookup"><span data-stu-id="0ed3e-135">Navigating through the data (ADO)</span></span>](navigating-through-the-data.md)
- [<span data-ttu-id="0ed3e-136">Understanding Recordset structure (ADO)</span><span class="sxs-lookup"><span data-stu-id="0ed3e-136">Understanding Recordset structure (ADO)</span></span>](understanding-recordset-structure.md)
